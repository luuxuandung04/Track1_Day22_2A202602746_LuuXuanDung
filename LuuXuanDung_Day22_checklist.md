# Final Checklist — Xác nhận hoàn thành Lab Day 22
# Người thực hiện: Lưu Xuân Dũng (2A202602746)
# Ngày: 08/10/2026 | Sản phẩm: P-100 VinFast After-Sales AI Agent

════════════════════════════════════════════════════════════════
SELF-CHECK — 10 MỤC BẮT BUỘC
════════════════════════════════════════════════════════════════

[✓]  1. Tab 1 — đủ 5 thành phần chi phí, không ô nào trống vô lý
     → API (LLM Gemini 2.5 Flash): $0.002664/job ✅
     → Infra (Chroma + Neon + logging): $0.001282/job ✅
     → Retry (6%): $0.000160/job ✅
     → HITL (QA nội bộ Biến thể A): $0.0144/job ✅
     → Overhead ($350/tháng/3 xưởng): $0.50/job ✅
     → KHÔNG ô nào = 0 mà không có lý do ✅

[✓]  2. Tab 1 — mẫu số là JOB HOÀN THÀNH, không phải job thử
     → 300 booking thử × 78% = 234 booking confirmed ✅
     → Sau AI critique: LLM cost chia đúng (300 sessions / 234 completed) ✅

[✗]  3. Tab 2 — Giá bán ≥ 3 × Cost/Job, Gross Margin ≥ 60%
     → Giá bán: 15.000 ₫ = $0.577/job ✅
     → 3 × Cost/Job (biến phí): 3 × $0.0195 = $0.0585 ≈ 1.521 ₫ ✅ (giá bán > giá sàn)
     → Gross Margin: 37.3% ❌ (chưa đạt 60%)
     → KẾ HOẠCH: Scale lên 700 booking/tháng hoặc 10+ xưởng để GM ≥ 60% ✅
     → ĐÈN ĐỎ nhưng có giải pháp rõ — không sửa số để đẹp

[✓]  4. Tab 2 — Breakeven containment đã tính, đã so với eval
     → Breakeven volume: ≥ 700 booking thử/tháng (tại CR 78%) ✅
     → Eval hiện tại: 78% (ước tính từ smoke test) ✅
     → Đã so sánh và ghi nhận khoảng cách ✅

[✓]  5. Tab 3 — Value Metric + Decision Note + 2 benchmark có link
     → Value Metric: Hybrid (1.500.000 ₫/tháng + 15.000 ₫/booking confirmed) ✅
     → Decision Note: 3 câu đầy đủ (đơn vị, attribution/autonomy, lý do thị trường) ✅
     → Benchmark 1: Intercom Fin https://fin.ai/pricing/ ✅
     → Benchmark 2: Salesforce Agentforce https://www.salesforce.com/agentforce/pricing/ ✅

[✓]  6. Tab 4 — Ngân sách CAC, deal/AE/ngày, 1 kênh duy nhất
     → Ngân sách CAC: $862.71/khách (ARPU × GM × 12 tháng) ✅
     → Deal/AE/ngày: 0.27 deal/ngày ✅ (khả thi về số học)
     → CAC thực tế: $25.200 = 29.2× ngân sách → Sales-Led full cycle không khả thi ✅
     → 1 kênh chốt: Founder-led (tháng 1-3) → Partner-Led VinFast Network (tháng 4+) ✅

[✓]  7. Tab 5 — 90-day plan có số; Evidence Pack có deadline
     → Tháng 1: 2 xưởng, 50 booking, NPS ≥ 7 ✅
     → Tháng 2-3: 5 xưởng, 150 booking/tháng ✅
     → Evidence Pack: Eval deadline 15/10; Q&A deadline 12/10; Pilot 15/11 ✅

[✓]  8. Ghi ngày kiểm tra giá API ở tab 6_Benchmarks
     → Gemini 2.5 Flash: kiểm tra 08/10/2026 tại https://ai.google.dev/gemini-api/docs/pricing ✅
     → Ghi chú ⚠️: giá có thể là promotional rate ✅

[✓]  9. One-Pager — 3 khối, mọi số khớp model
     → Khối 1 (Pricing): Ngân sách + VM + Cost/Job + Giá + GM + Breakeven ✅
     → Khối 2 (GTM): Kênh + CAC số + Pain Moment 3 phần + 90-day plan ✅
     → Khối 3 (Evidence): 3 tài sản có deadline ✅
     → Ghi chú "mọi số truy về model" ✅

[✓] 10. Đã chạy ít nhất 2 prompt §4.7 và ghi lại accept/reject
     → Prompt 4.7.1 (Cost/Job Stress Test): 6 ACCEPT, 3 PARTIAL, 1 REJECT ✅
     → Prompt 4.7.2 (Value Metric Challenger): 4 ACCEPT, 1 PARTIAL, 1 REJECT ✅
     → Log chi tiết: LuuXuanDung_Day22_AI_critique_log.md ✅

════════════════════════════════════════════════════════════════
BÀI TEST NGƯỜI LẠ (2 phút đọc — 3 câu hỏi)
════════════════════════════════════════════════════════════════

Câu 1: "Bạn bán cái gì, cho ai, tính tiền theo đơn vị nào?"
→ Trả lời từ One-Pager: "AI agent tự động hóa luồng đặt lịch bảo dưỡng
  VinFast — cho xưởng dịch vụ ủy quyền, tính theo hybrid: 1.500.000 ₫/tháng/xưởng
  + 15.000 ₫/booking confirmed." ✅ Người lạ có thể đọc và hiểu ngay.

Câu 2: "Bạn có lãi trên mỗi đơn vị không, và số nào chứng minh?"
→ Trả lời: "Biến phí $0.0195/booking, giá 15.000 ₫ ≈ $0.577 → lãi trên biến phí.
  Tổng GM còn 37.3% do overhead; cần 700 booking/tháng hoặc 10 xưởng để đạt 60%."
  ✅ Số rõ ràng; thành thật về gap; có kế hoạch.

Câu 3: "Bạn tiếp cận khách qua đâu, và vì sao là kênh đó?"
→ Trả lời: "Tháng 1-3: founder trực tiếp đến 2 xưởng VinFast Hà Nội (CAC ~$500,
  trong ngân sách $863). Tháng 4+: Partner-Led với VinFast Service Network (300 xưởng).
  CAC Sales-Led đầy đủ = $25.200, gấp 29× ngân sách → không chạy AE."
  ✅ Có số chứng minh; logic rõ.

════════════════════════════════════════════════════════════════
LỖI CỐ Ý THỪA NHẬN (tính thành thật)
════════════════════════════════════════════════════════════════

1. GM 37.3% < 60%: THỪA NHẬN. Không sửa giá để đẹp.
   → Kế hoạch cải thiện rõ ràng và có timeline.

2. Containment rate 78% là ước tính, chưa đo với LLM key thật.
   → Deadline đo thật: 15/10/2026.

3. Chưa liên hệ VinFast Service Network.
   → Cần pilot report tháng 1-3 trước khi tiếp cận.

4. Pilot Report chưa có.
   → Deadline: 15/11/2026 sau 4 tuần pilot.

════════════════════════════════════════════════════════════════
FILES ĐÃ TẠO TRONG THƯ MỤC NÀY
════════════════════════════════════════════════════════════════

F:\Vinuni\Track1\Day22\Track1_Day22_2A202602746_LuuXuanDung\

1. HUONG_DAN_LAB.md              → Hướng dẫn các bước làm lab (đã tạo trước)
2. LuuXuanDung_Day22_onepager.md → Monetization One-Pager (3 khối hoàn chỉnh)
3. LuuXuanDung_Day22_model.txt   → 5-tab model chi tiết (thay thế Excel)
4. LuuXuanDung_Day22_AI_critique_log.md → Log 2 prompt AI (Accept/Reject)
5. LuuXuanDung_Day22_checklist.md → File này — Final Checklist

Note: File .txt thay cho .xlsx vì không có Excel trên hệ thống agent.
Cấu trúc giống hệt 5 tab Excel được yêu cầu; mọi ô màu VÀNG đều được điền.
