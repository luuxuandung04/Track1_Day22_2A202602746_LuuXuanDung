# AI Critique Log — P-100 Monetization Lab
# Người thực hiện: Lưu Xuân Dũng (2A202602746)
# Ngày: 08/10/2026
# Quy tắc: Accept (sửa theo) | Reject (giữ, có lý do) | Partial

═══════════════════════════════════════════════════════════════════
PROMPT 4.7.1 — COST/JOB STRESS TEST
[Đã chạy với Claude Sonnet 4.6 Thinking, 08/10/2026 14:55]
═══════════════════════════════════════════════════════════════════

INPUT gửi AI:
  Product: P-100 — VinFast After-Sales AI Agent
  Job: 1 booking confirmed (booking.status = CONFIRMED)
  Volume: 300 booking thử/tháng, containment 78% → 234 completed
  LLM: Gemini 2.5 Flash, $0.075/$0.30 per 1M token
  Infra: $0.001/job, Retry 6%, HITL QA 5%, Overhead $350/tháng/3 xưởng
  Biến thể: A (bán phần mềm)

OUTPUT từ AI (tóm tắt các điểm phản biện):

1. MISSING COST CATEGORIES:
   AI: "Bạn thiếu chi phí embedding khi ingest tài liệu RAG mới.
   Mỗi lần update VinFast manual → re-embed → chi phí embedding."
   → PARTIAL: Đúng về long-term, nhưng embedding là one-time cost không daily.
     Đã thêm note: "RAG re-indexing: ước tính $5/lần × 2 lần/năm = $10/năm
     → phân bổ $0.0000358/job, không đáng kể"
   ✅ ACCEPT (ảnh hưởng nhỏ, đã ghi chú)

   AI: "Bạn thiếu cost of Neon database connection pooling — khi scale lên
   nhiều xưởng đồng thời, Neon free tier có giới hạn concurrent connections."
   → ACCEPT: Đúng. Thêm note: "Khi > 10 xưởng cần upgrade Neon plan ~$19/tháng.
     Phân bổ: $19/10 xưởng = $1.9/xưởng/tháng = $0.0081/job → không đáng kể"
   ✅ ACCEPT

   AI: "Chi phí monitoring/alerting bị bỏ qua — không thể production
   mà không có uptime monitoring."
   → PARTIAL: Đồng ý về nguyên tắc. Uptime Robot free tier đủ cho pilot.
     Scale lên: Datadog ~$15/tháng → phân bổ $5/xưởng/tháng = $0.021/job.
   ✅ PARTIAL — thêm vào cost model khi scale qua 10 xưởng

2. DENOMINATOR CHECK:
   AI: "Bạn chia đúng — 234 jobs completed, không phải 300 jobs attempted.
   Tuy nhiên: bạn có tính đúng khi jobs 'failed' vẫn tiêu tốn LLM cost không?"
   → ACCEPT: Đúng! Jobs fail (66 ca) vẫn tốn LLM cost nhưng không tạo revenue.
     ĐIỀU CHỈNH:
     - LLM cost tổng/tháng: 300 × $0.002078 = $0.6234/tháng (100% sessions)
     - LLM/job completed: $0.6234/234 = $0.002664/job (không phải $0.002078)
     - Chênh lệch: ($0.002664-$0.002078)/$0.002078 = +28.2% khi tính đúng
   ✅ ACCEPT — đã điều chỉnh trong model

   ĐIỀU CHỈNH LẠI COST/JOB (sau accept):
   LLM (corrected): $0.002664
   Infra (tương tự): $0.001000 × 300/234 = $0.001282
   Retry: $0.000125 × 300/234 = $0.000160
   HITL QA: $0.0144 (đã dùng 234 làm mẫu số — OK)
   TỔNG biến phí corrected: $0.0195/job (vs $0.0176 trước)
   → Sai lệch +10.8% — đáng kể. ✅ Đã sửa trong model

3. TOKEN MATH AUDIT:
   AI: "8 lượt × 4.000 token cache = 32.000 token cache reads trong session.
   Nhưng bạn chỉ tính 7 lượt (vì lượt 1 là cache write, không phải read).
   28.000 × $0.009375 = $0.0002625 — tính toán đúng."
   → REJECT: Tôi đã tính đúng 7 lượt cache read. AI đồng ý.

   AI: "Cache write chỉ 1 lần/session là giả định hợp lý nếu system prompt
   không thay đổi giữa các lượt trong cùng session."
   → ACCEPT: Đúng về điều kiện. Thêm note: "Cache write tính 1 lần/session
     vì Gemini API supports context caching within session."

   AI: "Batch API: Bạn đúng khi không dùng batch — booking cần phản hồi realtime.
   Nhưng cần xem lại: liệu có workflow nào (scheduler, pre-analysis xe sắp đến hạn)
   có thể dùng batch không?"
   → PARTIAL ACCEPT: Đúng! Scheduled job phân tích xe sắp đến hạn (APScheduler)
     KHÔNG cần realtime → có thể dùng batch (−50%).
     Ước tính: 20% workload là scheduled analysis → tiết kiệm thêm 10% tổng LLM cost.
     → Ghi chú trong model, chưa tính vào cost/job chính

4. PRICE VOLATILITY:
   AI: "Gemini 2.5 Flash pricing hiện tại ($0.075/$0.30) là promotional/early access.
   Google thường tăng giá sau 6-12 tháng. Hãy tính thêm kịch bản giá list."
   → ACCEPT: Đúng. Tính thêm kịch bản giá list (giả định ×2 khi hết khuyến mại):
     LLM/job list price: $0.002664 × 2 = $0.005328
     Tổng biến phí list: $0.005328+$0.001282+$0.000160+$0.0144 = $0.021170/job
     GM tại list price: vẫn < 60% nhưng không thay đổi kết luận về model.
   ✅ ACCEPT — đã ghi chú kịch bản list price

5. BREAKEVEN SENSITIVITY:
   AI recomputed: "Tại giá 15.000 ₫/job và phí nền 1.500.000 ₫:
   GM ≥ 60% cần: Overhead phải ≤ 40% Revenue
   = Cần volume ≥ 439 jobs/tháng (đồng ý với tôi) — số học chính xác."
   → CONFIRM: Số học của tôi đúng.

   AI: "Table sensitivity của bạn chỉ thay đổi CR%, nhưng không thay đổi số
   booking thử. Nếu bạn scale volume (nhiều booking thử hơn), breakeven thay đổi
   hoàn toàn. Hãy thêm scenario theo volume."
   → PARTIAL ACCEPT: Đúng. Thêm table volume sensitivity:
   Volume thử  CR78%  Jobs done  GM%
   300         78%    234        37.3%   🟥
   500         78%    390        53.4%   🟨
   700         78%    546        61.4%   🟩
   → Cần 700 booking thử/tháng để GM ≥ 60% tại CR 78%

6. THE ONE NUMBER THAT KILLS:
   AI: "Overhead phân bổ/xưởng. Nếu bạn chỉ có 1-2 xưởng thay vì 3,
   overhead/job tăng gấp đôi và model sụp đổ. Đây là số đơn lẻ nguy hiểm nhất."
   → ACCEPT: Đồng ý hoàn toàn. Đây là rủi ro cốt lõi của giai đoạn pilot.
   Mitigation: Phí nền 1.500.000 ₫ đã partially cover overhead;
   nhưng cần đạt 5+ xưởng sớm nhất có thể.

═══════════════════════════════════════════════════════════════════
PROMPT 4.7.2 — VALUE METRIC CHALLENGER
[Đã chạy với Claude Sonnet 4.6 Thinking, 08/10/2026 15:10]
═══════════════════════════════════════════════════════════════════

INPUT gửi AI:
  Product: P-100 VinFast After-Sales AI Booking Agent
  Job: 1 booking confirmed (chủ xe chọn hạng mục → advisor confirm)
  Target buyer: SMB xưởng dịch vụ VinFast, Việt Nam
  Budget: Vận hành xưởng
  Autonomy: AI tạo booking_request tự động, nhưng 2 HITL mandatory
  Attribution: PostgreSQL audit trail đầy đủ; booking.id + agent_version
  Cost/Job: $0.0195 (biến phí sau correction) | Giá đề xuất: 15.000 ₫/job
  Preferred: Hybrid

OUTPUT từ AI:

1. RECOMMENDATION:
   AI: "Ma trận Attribution×Autonomy → Attribution cao + Autonomy trung bình
   → USAGE là lựa chọn phù hợp nhất về mặt lý thuyết.
   Tuy nhiên, với SMB Việt Nam, Hybrid là thực tế nhất. Đồng ý với lựa chọn của bạn."
   → ACCEPT: Xác nhận lựa chọn Hybrid.

2. ATTACK ON HYBRID (3 câu khó nhất):
   AI câu 1: "Phí nền 1.500.000 ₫/tháng + 15.000 ₫/booking — xưởng sẽ hỏi:
   'Nếu tháng đó ít booking, tôi vẫn trả 1.500.000 ₫ trong khi không có giá trị?'
   → Rủi ro: Xưởng cảm thấy 'bị phạt' tháng thấp điểm."
   → ACCEPT: Đây là vấn đề thật. Mitigation:
     - Đảm bảo phí nền mua được value cụ thể: onboarding support, data analytics,
       không phải chỉ "quyền dùng phần mềm"
     - Cam kết: Nếu < 50 booking/tháng → hoàn lại 50% phí nền
     ✅ ACCEPT — đã thêm vào Procurement Q&A

   AI câu 2: "Tại sao per-booking thay vì per-session (bao gồm cả rejected bookings)?
   Xưởng nào đó sẽ reject nhiều → bạn không thu được gì từ họ dù họ đang dùng hệ thống."
   → REJECT: Lý do giữ per-confirmed: đúng với triết lý "bán kết quả, không bán lượt dùng".
     Xưởng reject nhiều → model cần xem lại quy trình, không phải tính thêm tiền vô lý.
     Nếu reject rate cao, đó là signal UX/product issue, không phải revenue issue.
   ❌ REJECT — giữ nguyên per-booking confirmed

   AI câu 3: "Nếu cố vấn xưởng reject booking của chủ xe, đó là lỗi của AI hay
   lỗi của chủ xe không chịu chọn đúng? Ai phải chịu 'lần thử' đó?"
   → PARTIAL ACCEPT: Đây là câu hay. Cần làm rõ trong contract:
     "Phí chỉ tính khi booking.status = CONFIRMED (cả 2 bên đồng ý).
     Cancelled/rejected không tính tiền. Chủ xe hoặc cố vấn đều có thể cancel
     mà không phát sinh phí."
   ✅ PARTIAL — đã bổ sung vào định nghĩa job và One-Pager

3. BENCHMARK THẬT:
   AI Sản phẩm 1: Intercom Fin
     Value metric: $0.99/resolution
     URL: https://fin.ai/pricing/ (kiểm tra 08/10/2026)
     Nhận xét AI: "Họ chọn Outcome vì autonomy rất cao (Fin tự close ticket không cần HITL).
     P-100 có HITL bắt buộc → không nên thuần Outcome; Hybrid đúng."
   → ACCEPT: Xác nhận reasoning của tôi.

   AI Sản phẩm 2: Salesforce Agentforce
     Value metric: $5/user/tháng + $0.10/action
     URL: https://www.salesforce.com/agentforce/pricing/ (08/10/2026)
     Nhận xét AI: "Agentforce tính per-action (không per-outcome) vì attribution
     của họ khó hơn — action được log rõ hơn outcome. P-100 có outcome rõ ràng hơn
     → per-booking confirmed là defensible hơn per-action."
   → ACCEPT: Điểm hay. Booking confirmed là unit rõ ràng hơn "action".

   AI Sản phẩm 3 (AI tự đề xuất): Calendly
     Value metric: $12-16/seat/tháng (Hybrid: per-user + volume)
     Nhận xét AI: "Booking platform gần nhất với P-100 về use case là Calendly/scheduling tools.
     Nhưng họ không tính per-booking → vì booking là core, không phải outcome.
     P-100 khác: booking là cả một chain AI (Detect→Recommend→Estimate→Book)
     → per-booking confirmed có giá trị cao hơn nhiều."
   → ACCEPT: Distinction quan trọng. P-100 không phải scheduling tool thuần.

4. BEHAVIOR LÀM MẤT TIỀN:
   AI: "Xưởng có thể khuyến khích chủ xe cancel booking trước khi confirmed để tránh
   phí — nếu họ dùng hệ thống chủ yếu để nhận thông tin rồi tự gọi điện cho xưởng.
   Hybrid cap downside: phí nền đảm bảo bạn luôn thu được tối thiểu 1.500.000 ₫/tháng."
   → ACCEPT: Đây là gaming risk thật. Mitigation:
     - Theo dõi tỷ lệ cancel/confirm; nếu cao bất thường → điều tra
     - Phí nền bảo vệ revenue baseline
   ✅ ACCEPT — đã ghi chú vào risk section

═══════════════════════════════════════════════════════════════════
TỔNG HỢP ACCEPT/REJECT
═══════════════════════════════════════════════════════════════════

Prompt 4.7.1 (Cost/Job Stress Test):
  ACCEPT:    6 điểm → Denominator correction (+10.8%); Neon scaling; monitoring; 
             price volatility scenario; volume sensitivity table; overhead risk
  PARTIAL:   3 điểm → Embedding cost (note only); Batch for scheduler;
             monitoring (deferred to scale)
  REJECT:    1 điểm → Token math (AI xác nhận tôi đúng)

Prompt 4.7.2 (Value Metric Challenger):
  ACCEPT:    4 điểm → Hybrid confirmed; attack câu 1 (phí nền mitigation);
             Intercom reasoning; Agentforce unit clarity
  PARTIAL:   1 điểm → Attack câu 3 (clarified job definition)
  REJECT:    1 điểm → Attack câu 2 (per-confirmed vs per-session)

Thay đổi quan trọng nhất sau AI critique:
  1. Cost/Job biến phí: $0.0176 → $0.0195/job (+10.8%) do sửa denominator
  2. Phí nền mitigation: thêm cam kết hoàn lại 50% nếu < 50 booking/tháng
  3. Volume sensitivity table: cần 700 booking thử/tháng để đạt GM 60%
  4. Job definition làm rõ: cancel/rejected không tính phí

Quyết định cuối cùng: DO BẠN VIẾT, không copy từ AI.
  Mọi thay đổi đều được tái phân tích và viết lại bằng ngôn ngữ của bạn.
