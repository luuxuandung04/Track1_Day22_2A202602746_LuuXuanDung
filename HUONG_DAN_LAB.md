# 📋 HƯỚNG DẪN LÀM BÀI LAB – DAY 22: MONETIZATION & GTM

> **Tổng thời gian:** 120 phút  
> **Mục tiêu:** Định nghĩa 1 job, tính Cost/Job đủ 5 thành phần, chốt Value Metric, chọn 1 kênh GTM có số chứng minh, và ráp Monetization One-Pager.  
> **Câu chốt:** *"Chạy được là bài toán kỹ thuật. Bán được là bài toán sinh tồn."*

---

## 📁 TÀI LIỆU ĐI KÈM

Tải từ: [Google Drive](https://drive.google.com/drive/folders/1lAN_fxwtTr1fOHm1SoPR7OH3F0Z8D5Ya?usp=drive_link)

| File | Dùng để |
|------|---------|
| `day22_monetization_model.xlsx` | 5 tab làm việc + 2 tab tham chiếu. **Chỉ điền vào ô MÀU VÀNG.** |
| `day22_one_pager_template.docx` | Khung nộp bài – Monetization One-Pager |

**Quy ước màu trong Excel:**

| Màu | Ý nghĩa |
|-----|---------|
| 🟡 Vàng | Ô bạn phải điền |
| ⬜ Xám | Công thức tự tính – không sửa |
| 🟩 Xanh lá | Đạt ngưỡng |
| 🟥 Đỏ | Không đạt – phải quay lại sửa giả định |

**Bản đồ các tab Excel:**

| Tab | Tên | Vai trò |
|-----|-----|---------|
| 0 | 0_README | Quy ước, ngày chốt giá, thứ tự làm |
| 1 | 1_Cost_Job | Tab nặng nhất – tính Cost/Job đủ 5 thành phần |
| 2 | 2_Pricing | Giá sàn, giá trần, Gross Margin, stress test |
| 3 | 3_Value_Metric | Chấm điểm Attribution × Autonomy → gợi ý Value Metric |
| 4 | 4_Channel_Fit | Ngân sách CAC, số deal/AE/ngày, chấm điểm 3 kênh |
| 5 | 5_90Day_Plan | Kế hoạch 90 ngày + checklist Evidence Pack |
| 6 | 6_Benchmarks | Bảng giá tham chiếu có nguồn – chỉ đọc |

---

## 🗺️ TỔNG QUAN 6 TRẠM

| Trạm | Nội dung | Thời gian | Output |
|------|---------|-----------|--------|
| 1 | Ngân sách khách & định nghĩa Job | 15' | 1 câu định vị + định nghĩa Job |
| 2 | Value Metric | 20' | Value Metric + lý do defendable |
| 3 | Cost/Job, giá sàn & giá trần ⭐ | 30' | Cost/Job + giá + GM + breakeven |
| 4 | Kênh phân phối & Affordability Test | 20' | Kênh + số chứng minh |
| 5 | Pain Moment & 90-Day Plan | 15' | Pain moment cụ thể + plan 3 giai đoạn |
| 6 | Evidence Pack & ráp One-Pager | 20' | One-Pager hoàn chỉnh |

> ⚠️ **Bấm giờ từng trạm.** Hết giờ thì chuyển trạm, kể cả khi chưa hoàn hảo – bạn quay lại hoàn thiện ở Trạm 6.

---

## 🚉 TRẠM 1 – NGÂN SÁCH KHÁCH & ĐỊNH NGHĨA JOB (15 phút)

**Mục tiêu:** Xác định tiền của khách đến từ ngân sách nào, và định nghĩa chính xác "1 job" là gì.

### Các bước thực hiện

**Bước 1 (4'):** Viết 2 phiên bản một câu mô tả sản phẩm:
- **Phiên bản A** – Đóng gói kiểu công cụ / nền tảng
- **Phiên bản B** – Đóng gói kiểu thay thế một công việc đang có người làm

| Cách đóng gói | Khách xếp vào | Câu hỏi khách tự đặt ra |
|--------------|--------------|------------------------|
| "Nền tảng AI cho…" | Ngân sách phần mềm | "Tôi có cần thêm một nền tảng nữa không?" |
| "Công cụ hỗ trợ…" | Ngân sách phần mềm | "Tool này khác gì cái tôi đang dùng?" |
| "Thay ca trực đêm" | Ngân sách nhân sự | "Rẻ hơn lương 1 người không?" |
| "Xử lý xong X việc/tháng" | Ngân sách vận hành | "Đơn giá mỗi việc là bao nhiêu?" |

**Bước 2 (3'):** Với mỗi phiên bản, trả lời:
- Ai ký duyệt?
- Tiền lấy từ ngân sách nào? (Phần mềm / Nhân sự / Vận hành / Marketing)

**Bước 3 (3'):** Chọn 1 phiên bản. Viết 1 câu lý do – **dựa trên ngân sách, không dựa trên "nghe hay hơn".**

**Bước 4 (5'):** Điền **S1 Tab 1** – định nghĩa "1 job". Kiểm tra bằng 3 câu:
1. Khách có coi job này là giá trị không? (không phải "1 lần gọi API")
2. Bạn đếm được nó tự động không?
3. Định nghĩa có chặt như Intercom ("khách xác nhận xong hoặc không hỏi lại") chưa?

### ✅ Kết quả mong đợi
> 1 câu định vị + tên ngân sách + định nghĩa Job viết được thành câu.

### ❌ Dấu hiệu Fail
- Câu định vị chỉ nói công nghệ, không nói công việc bị thay thế
- Job định nghĩa theo kỹ thuật: "1 request" hoặc "1 lần gọi API"
- Job quá rộng: "1 khách hàng hài lòng" → không đếm được

---

## 🚉 TRẠM 2 – VALUE METRIC (20 phút)

**Mục tiêu:** Chọn đơn vị tính tiền và bảo vệ được lựa chọn đó.

### Bốn lựa chọn Value Metric

| | Seat | Usage | Outcome | Hybrid |
|---|------|-------|---------|--------|
| **Cách tính** | Phí cố định / user | Theo lượt dùng | Theo kết quả đạt được | Phí nền + usage |
| **Ưu điểm** | Dễ hiểu, dễ bán | Chi phí ↔ doanh thu cùng chiều | Align đúng giá trị | Cân bằng rủi ro 2 bên |
| **Nhược điểm** | Âm biên nếu user dùng nhiều | Khách sợ hoá đơn vượt trần | Phải đo được attribution | Phức tạp khi giải thích |
| **Dùng khi** | AI là feature phụ | AI là core, dùng nhiều | AI tự chạy, kết quả đo được | Chưa chắc chắn |

### Ma trận Attribution × Autonomy

```
                  AUTONOMY THẤP          AUTONOMY CAO
                  (cần người)            (AI tự chạy)
ATTRIBUTION CAO   ┌─────────────┐        ┌═════════════╗
(đo được)         │   Usage     │        ║   OUTCOME   ║
                  └─────────────┘        └═════════════╝
ATTRIBUTION THẤP  ┌─────────────┐        ┌─────────────┐
(chưa đo được)    │ Seat/Hybrid │        │   Usage     │
                  └─────────────┘        └─────────────┘
```

### Các bước thực hiện

**Bước 1 (6'):** Mở tab `3_Value_Metric`. Trả lời 5 câu Attribution + 5 câu Autonomy. **Trả lời theo thực tế hôm nay, không theo kế hoạch quý sau.**

**Bước 2 (3'):** Đọc gợi ý của model. Đối chiếu với ma trận ở trên.

**Bước 3 (6'):** Benchmark ngược: tìm **2 sản phẩm thật** cùng loại job với bạn, ghi lại họ tính tiền theo đơn vị gì, giá bao nhiêu, **kèm link nguồn.**

**Bước 4 (5'):** Chốt Value Metric. Viết **Decision Note 3 câu:**
1. Tôi chọn đơn vị nào?
2. Attribution và Autonomy của tôi ở mức nào – bằng chứng gì?
3. Nếu chọn khác gợi ý của model, lý do thị trường là gì?

> 💡 Lý do thị trường hợp lệ: *"Khách phân khúc này chưa quen trả theo kết quả"*  
> ❌ Lý do không hợp lệ: *"Tôi thấy hợp hơn"*

### ✅ Kết quả mong đợi
> Value Metric đã chốt + 2 sản phẩm benchmark có link + Decision Note 3 câu.

### ❌ Dấu hiệu Fail
- Chọn Outcome khi chưa đo được Attribution
- Chọn Seat cho AI agent chạy liên tục
- Benchmark nhớ mang máng, không có link nguồn

> 🔁 **Nếu bí:** Chạy **Prompt 4.7.2** (Value Metric Challenger) – xem phần Bộ Prompt bên dưới.

---

## 🚉 TRẠM 3 – COST/JOB, GIÁ SÀN & GIÁ TRẦN ⭐ (30 phút)

**Mục tiêu:** Ra được một con số Cost/Job có thể bảo vệ trước CFO, rồi từ đó ra vùng giá bán.

### Công thức cốt lõi

```
Cost/Job = ( API + Infra + HITL + Retry + Overhead ) / Số job HOÀN THÀNH
```

> ⚠️ **Mẫu số là job HOÀN THÀNH, KHÔNG PHẢI job đã thử!**

### 5 thành phần chi phí

| Thành phần | Gồm những gì | Mức độ hay bị quên |
|-----------|-------------|-------------------|
| **API** | Token LLM (input/output/cache), STT, TTS, embedding | Ai cũng nhớ |
| **Infra** | Server, vector DB, telephony, storage, logging | Ít người tính |
| **HITL** | Người kiểm tra / sửa / xử lý ca AI làm không xong | ⚠️ Hay quên nhất |
| **Retry** | API timeout, gọi lại 2–3 lần, tốn gấp đôi token | ⚠️ Hay quên nhất |
| **Overhead** | R&D, sales, support phân bổ | Thường để riêng khi tính GM |

### HITL – Phân biệt 2 biến thể

| | Biến thể A | Biến thể B |
|--|-----------|-----------|
| **Bạn bán gì** | Phần mềm | Outcome / Managed service |
| **Ai xử lý ca escalate** | Khách tự xử lý | **Bạn** phải giao kết quả |
| **HITL vào COGS của bạn?** | ❌ Không | ✅ Có – vào thẳng |
| **Ảnh hưởng** | Cost/Job thấp hơn | Cost/Job cao hơn nhiều lần |

> ⚠️ Hai biến thể cho ra Cost/Job chênh nhau nhiều lần. **Phải nói rõ mình ở biến thể nào.**

### Các bước thực hiện

**Bước 1 (3'):** Cập nhật giá API. Mở tab `6_Benchmarks`, kiểm tra các dòng có dấu ⏳, mở trang giá gốc, cập nhật nếu đã đổi. **Ghi ngày bạn kiểm tra.**

**Bước 2 (7'):** Tính chi phí LLM cho 1 job. Điền **S3:**
- Số lượt hội thoại
- Token input cache được vs fresh
- Token output / lượt
- Ghi lại % tiết kiệm nhờ cache
- Nếu không cần realtime: thử giá Batch (−50%) và ghi con số thứ hai

**Bước 3 (4'):** Điền **S4** (Speech nếu có) + **S5** (Infra).

**Bước 4 (4'):** Điền **S6** (Retry) + **S7** (HITL):
- Retry: **đừng để 0%** – chưa đo thì dùng 5–10% và ghi rõ là ước tính
- HITL: chọn Biến thể A hay B và viết 1 câu lý do

**Bước 5 (4'):** Đọc Cost/Job và tính giá sàn trong Tab 2:
- **Giá sàn = 3 × Cost/Job**
- Nếu Cost/Job nhỏ đến mức vô lý → bạn đang quên một khoản, quay lại S5–S7

**Bước 6 (5'):** Neo giá trần – điền 2 con số neo:

| Cách neo giá trần | Công thức | Ví dụ |
|------------------|-----------|-------|
| Theo giá trị tạo ra | Charge 10–25% giá trị | Tiết kiệm 100tr/tháng → charge 10–25tr |
| Theo nhân công | Charge 50–70% lương vị trí bị thay | Lương 10tr/tháng → charge 5–7tr |

**Bước 7 (3'):** Stress test – đọc bảng sensitivity và ô Breakeven containment:
- Containment phải đạt bao nhiêu % để GM ≥ 60%?
- Đối chiếu với eval của bạn
- Nếu đang ở dưới ngưỡng → viết 1 câu: bạn sẽ tăng containment, tăng giá, hay đổi biến thể HITL?

### ✅ Kết quả mong đợi – bắt buộc có 5 con số

```
[ ] Cost/Job                     = ______
[ ] Giá sàn (= 3 × Cost/Job)     = ______
[ ] Giá bán đề xuất              = ______
[ ] Gross Margin                 = ______%   (mục tiêu ≥ 60%)
[ ] Breakeven containment        = ______%   (so với eval hiện tại: ______%)
```

### ❌ Dấu hiệu Fail & cách sửa

| Bẫy | Dấu hiệu | Sửa thế nào |
|-----|---------|------------|
| Chỉ tính token API | GM > 85% | Điền đủ Infra + Retry + HITL |
| Chia cho job thử thay vì hoàn thành | Cost/Job thấp hơn thực tế | Mẫu số phải là job completed (S2) |
| Retry = 0% | Ô S6 trống | Dùng 5–10%, ghi là ước tính |
| Quên HITL | S7 trống ở Biến thể B | 5% sai cũng phải có người xử lý |
| Dùng giá khuyến mại như giá vĩnh viễn | Không có ngày kiểm tra | Ghi ngày + tính thêm kịch bản giá list |

> ⚠️ **Đèn đỏ ở Tab 2: đừng sửa giá cho đẹp.** Quay lại Tab 1 và đổi mô hình kinh doanh.

> 🔁 **Nếu bí:** Chạy **Prompt 4.7.1** (Cost/Job Stress Test) – xem phần Bộ Prompt bên dưới.

---

## 🚉 TRẠM 4 – KÊNH PHÂN PHỐI & AFFORDABILITY TEST (20 phút)

**Mục tiêu:** Chọn đúng 1 kênh cho 90 ngày đầu, và chứng minh bằng số rằng bạn nuôi nổi kênh đó.

> ⚠️ **Nguyên tắc sống còn:** Chạy song song 3 kênh với đội 5 người = không kênh nào đủ sâu.

### So sánh 3 kênh GTM

| | PLG | Sales-Led | Partner-Led |
|--|-----|-----------|-------------|
| **Cơ chế** | User tự tìm, tự dùng, tự mua | Team đi gặp, demo, chốt từng khách | Cắm vào platform đã có sẵn khách |
| **CAC** | Thấp | Cao | Thấp (đòn bẩy partner) |
| **Dùng khi** | Sản phẩm tự giải thích, giá thấp | Sản phẩm phức tạp, giá cao | Có platform phù hợp và quan hệ thật |

### 3 công cụ tính toán có nguồn

**Công cụ 1 – Ngưỡng sàn Inside Sales (Tunguz, 2016):**
```
Số deal 1 AE phải chốt / năm  =  Quota năm / ACV
ACV $3.000 → 167 deal/năm ≈ 0,7 deal / ngày → khả thi ✅
ACV $500   → 1.000 deal/năm ≈ 4 deal / ngày  → bất khả thi ❌
```

**Công cụ 2 – Channel Affordability Test:**
```
Ngân sách CAC  =  ARPU_tháng × Gross Margin × Số tháng payback cho phép
```

| Phân khúc | CAC Payback cho phép |
|----------|---------------------|
| SMB | < 12 tháng |
| Mid-market | < 18 tháng |
| Enterprise | < 24 tháng |

**Công cụ 3 – Đối chiếu cost-per-opportunity (ICONIQ 2026):**

| Chỉ số | Mức (theo phân khúc) |
|-------|---------------------|
| Cost per lead | $500 · $600 · $800 |
| Cost per opportunity | $6.300 · $8.000 · $11.200 |

### Các bước thực hiện

**Bước 1 (5'):** Mở tab `4_Channel_Fit`. Nhập ARPU/tháng và phân khúc → ra ngân sách CAC.

**Bước 2 (4'):** Nhập quota AE/năm và ACV → ra số deal/AE/ngày làm việc:
- ≤ ~1 deal/ngày → Sales-Led khả thi ✅
- > 1 deal/ngày → 🟥 không chạy được

**Bước 3 (4'):** Tính CAC thực tế:
```
CAC thực tế ≈ Cost per opportunity / Win rate
```
So với ngân sách CAC ở bước 1. **Lệch bao nhiêu lần? Ghi con số đó lại.**

**Bước 4 (4'):** Chấm điểm 3 kênh trong scorecard (6 tiêu chí × 1–5). **Chốt 1 kênh duy nhất.**

**Bước 5 (3'):** Nếu rơi vào vùng không khả thi, chọn 1 trong 3 lối thoát:

| Lối thoát | Làm gì | Đánh đổi |
|----------|-------|---------|
| Giảm giá xuống | Đơn giản hoá đến mức khách tự mua | Mất phân khúc lớn |
| Tăng giá lên | Bán kèm service / triển khai | Chậm hơn, cần đội triển khai |
| Đi Partner-Led | Cắm vào platform đã có khách | Chia margin, phụ thuộc partner |

### ✅ Kết quả mong đợi

```
[ ] Ngân sách CAC / khách        = ______
[ ] Số deal / AE / ngày          = ______
[ ] CAC thực tế ước tính         = ______   → lệch ______ lần
[ ] Kênh đã chốt                 = PLG / Sales-Led / Partner-Led
[ ] Nếu Partner-Led: TÊN partner = ______   · Đã nói chuyện chưa? ______
```

### ❌ Dấu hiệu Fail
- Chọn 2–3 kênh "để linh hoạt"
- Partner-Led không có tên công ty cụ thể
- PLG với ARPU cao (ai tự bỏ vài trăm đô/tháng mà không nói chuyện với ai?)

> 🔁 **Nếu bí:** Chạy **Prompt 4.7.3** (Channel Reality Check).

---

## 🚉 TRẠM 5 – PAIN MOMENT & 90-DAY PLAN (15 phút)

**Mục tiêu:** Biến kênh trừu tượng thành một điểm chạm cụ thể, và kế hoạch 90 ngày ai đọc cũng làm theo được.

### Công thức Pain Moment

```
Pain Moment  =  MẤY GIỜ  +  ĐANG LÀM GÌ  +  DÙNG APP NÀO
```

| | Ví dụ đọc được ✅ | Ví dụ không đọc được ❌ |
|--|------------------|----------------------|
| | "23h, dev push PR, không ai review → tắc nghẽn. Lúc đó họ đang ở GitHub → sản phẩm phải là GitHub App, không phải website riêng." | "Khách cần AI khi làm việc." |

> ⚠️ **Pain Moment quyết định kênh phân phối – không phải ngược lại.**

### Nguyên tắc nhúng sản phẩm

```
✗ Đừng bắt khách mở tab mới
✗ Đừng bắt tải app mới
✗ Đừng bắt học workflow mới
```

Sản phẩm AI thắng lớn không tạo thói quen mới – chúng **nhúng vào thói quen cũ.**

### Các bước thực hiện

**Bước 1 (5'):** Viết Pain Moment theo đúng công thức 3 phần ở trên.

**Bước 2 (3'):** Từ Pain Moment suy ra **điểm nhúng:** sản phẩm của bạn phải nằm ở đâu để có mặt đúng lúc đó?
- Một app trong marketplace?
- Một số hotline?
- Một plugin / webhook?
- Một extension IDE?

**Bước 3 (7'):** Điền **90-Day Plan** trong tab `5_90Day_Plan`, 3 giai đoạn:

| Giai đoạn | Mục tiêu điển hình | Phải ghi rõ |
|----------|-------------------|------------|
| **Tháng 1** | Hiểu sâu – số ít khách, làm tận tay | Bao nhiêu khách? Ai đi gặp? Thu được data gì? |
| **Tháng 2–3** | Đòn bẩy – nhân rộng qua kênh đã chọn | Cơ chế nhân rộng là gì? KPI nào? |
| **Tháng 4+** | Mở rộng – chỉ sau khi thắng tuyệt đối 1 ngách | Ngách tiếp theo là gì? Dựa trên bằng chứng nào? |

> ⚠️ **Đừng cố scale ngay.** Kế hoạch "tháng 1 lấy 200 khách ở 5 ngành" là kế hoạch chưa ai từng thử làm.

### ✅ Kết quả mong đợi
> Pain Moment đủ 3 phần + điểm nhúng cụ thể + 90-Day Plan có số và tên người chịu trách nhiệm.

### ❌ Dấu hiệu Fail
- Pain Moment chung chung: "khi khách cần hỗ trợ"
- Kế hoạch không có số
- Tháng 1 đã đặt mục tiêu scale

---

## 🚉 TRẠM 6 – EVIDENCE PACK & RÁP ONE-PAGER (20 phút)

**Mục tiêu:** Gói 5 trạm trước thành 1 trang đưa được cho người lạ.

### Tại sao cần Evidence Pack?

> Khách vỗ tay ở demo. Nhưng về công ty, Procurement và IT sẽ hỏi 3 câu:
> 1. AI này có hallucinate không? Nếu nó nói sai với khách của tôi thì sao?
> 2. Data của tôi có bị dùng để train model không?
> 3. Startup này chết thì data của tôi ở đâu?
>
> **Không trả lời được bằng văn bản → deal chết ở Procurement.**

### Các bước thực hiện

**Bước 1 (7'):** Điền checklist Evidence Pack trong tab `5_90Day_Plan`:

| Tài sản | Nếu đã có | Nếu chưa có |
|--------|---------|-----------|
| **Eval Results** | Con số cụ thể: "xử lý đúng __%; __% còn lại chuyển người" | Ai làm · deadline · đo bằng bộ eval nào |
| **Procurement Q&A** | 3 câu trả lời cho 3 câu hỏi của Procurement ở trên | Ai làm · deadline |
| **Pilot Report** | "__ tuần, __ lượt, tỷ lệ thành công __%, tiết kiệm __" | Pilot với ai · bắt đầu khi nào |

> ⚠️ **Ô nào chưa có thì ghi deadline, đừng bỏ trống.** Một Evidence Pack thành thật về khoảng trống tốt hơn một Evidence Pack bịa.

**Bước 2 (10'):** Ráp One-Pager – mở `day22_one_pager_template.docx`, chép các con số đã chốt từ Excel sang. 3 khối:

| Khối | Nội dung |
|-----|---------|
| **1. Pricing** | Ngân sách khách · Value Metric + lý do · Cost/Job · Giá đề xuất · GM · Breakeven containment · cách neo giá |
| **2. GTM** | Kênh + số chứng minh (ngân sách CAC vs CAC thực tế) · Pain Moment 3 phần · 90-day plan |
| **3. Evidence** | 3 tài sản – đã có gì, thiếu gì, deadline |

**Bước 3 (3'):** Tự kiểm tra bằng **"bài test người lạ"** – đưa One-Pager cho một nhóm khác đọc trong 2 phút. Họ phải trả lời được không cần hỏi lại quá 3 câu:
1. Bạn bán cái gì, cho ai, tính tiền theo đơn vị nào?
2. Bạn có lãi trên mỗi đơn vị không, và con số nào chứng minh?
3. Bạn tiếp cận khách qua đâu, và vì sao là kênh đó?

### ✅ Kết quả mong đợi
> One-Pager đầy đủ 3 khối, mọi con số đều truy được về một ô trong Excel.

---

## 🤖 BỘ PROMPT PHẢN BIỆN (English-only)

> Quy tắc dùng AI: AI là công cụ phản biện, **không phải tác giả.** Với mỗi điểm AI nêu: **accept** (sửa theo), **reject** (giữ, có lý do), hoặc **partial**. Mọi sửa đổi phải do **bạn** viết lại.

### Prompt 4.7.1 – Cost/Job Stress Test (dùng sau khi điền xong Tab 1)

```
Act as a ruthless CFO and a skeptical infrastructure engineer.
Review the Cost/Job model for an AI product below.

Do NOT rewrite my numbers. Perform a stress test:

1. MISSING COST CATEGORIES
   List every cost category I have omitted or underestimated for
   THIS specific product type. Focus especially on:
   - Retry and timeout costs
   - Human-in-the-loop cost, and WHO actually bears it
   - Observability, logging, eval running costs
   - Egress, storage, vector DB growth over time
   For each, estimate a realistic value at my stated volume.

2. DENOMINATOR CHECK
   Am I dividing by jobs ATTEMPTED or jobs COMPLETED?
   Recalculate Cost/Job using completed jobs only.
   State the difference as a percentage.

3. TOKEN MATH AUDIT
   Recompute my LLM cost per job from the token counts and
   list prices I provided. Flag any arithmetic error.
   Tell me how much prompt caching and batch pricing would save,
   and whether batch is viable for my latency requirement.

4. PRICE VOLATILITY
   Which of the prices I used are promotional or likely to change
   within 6 months? Recompute Cost/Job at list price.

5. BREAKEVEN SENSITIVITY
   Solve for the minimum success/containment rate required to hit
   60% gross margin at my proposed price. Show the algebra.
   Then show Cost/Job and gross margin at success rates of
   50%, 60%, 70%, 80%, 90%.

6. THE ONE NUMBER THAT KILLS ME
   Identify the single input that, if wrong by 2x, breaks the model.

Be direct and highly critical. Use my numbers, show your arithmetic.
Do not be encouraging. Find the problems before my investors do.

[Paste your Tab 1 assumptions here]
```

### Prompt 4.7.2 – Value Metric Challenger (khi phân vân Seat / Usage / Outcome / Hybrid)

```
My AI product:
- What it does: [describe the job it completes]
- Definition of one job: [your exact definition]
- Target buyer: [B2B SME / Enterprise / prosumer, industry, geography]
- Whose budget it comes from: [software / headcount / operations]
- Autonomy today: [does it complete jobs end-to-end, or need a human?]
- Attribution today: [can I measure that the outcome was caused by
  my AI? what evidence do I have — eval results, logs, A/B?]
- Cost/Job: [number] · Proposed price: [number]

Task:
1. Recommend a value metric (Seat / Usage / Outcome / Hybrid)
   and explain the reasoning against the Attribution x Autonomy
   framework.
2. ATTACK my own preferred choice, which is [your choice].
   Give me the three hardest questions a skeptical buyer or
   investor would ask about it.
3. Name 3 REAL products that charge for a similar job. For each,
   state their value metric and current published price, and give
   the URL.
4. Describe the exact customer behaviour that would make my
   chosen metric lose money, and how a hybrid structure would
   cap that downside.

Be specific about numbers. Flag any figure you are unsure about.
```

### Prompt 4.7.3 – Channel Reality Check (khi chọn kênh GTM)

```
I am choosing ONE go-to-market channel for the next 90 days.

My numbers:
- ARPU: [number] per month · Gross margin: [%]
- Segment: [SMB / mid-market / enterprise]
- CAC budget I computed: [number] per customer
- Chosen channel: [PLG / Sales-Led / Partner-Led]
- Pain moment: [time + what the customer is doing + which app]

Task:
1. Compute how many deals one AE must close per year and per
   working day at my ACV. Tell me plainly whether a sales-led
   motion is arithmetically possible at my price point.
2. Compare my CAC budget against realistic cost-per-opportunity
   benchmarks. State the gap as a multiple.
3. Stress test my pain moment. Is it specific enough to name
   an integration surface?
4. If my chosen channel is Partner-Led: what must be true about
   the partner's incentives? What is the fastest way to falsify
   this plan within 2 weeks?
5. Give me the strongest argument AGAINST my chosen channel.

Be blunt. I would rather be wrong now than in month 3.
```

### Prompt 4.7.4 – Procurement Objection Simulator (chuẩn bị Evidence Pack)

```
Act as the IT security lead and the procurement manager of a
mid-sized company evaluating my AI vendor. You are risk-averse
and have no incentive to say yes.

My product: [describe]
My Evidence Pack currently contains: [list what you actually have]

Task:
1. Write the 10 questions you would send me before approving
   this purchase. Order by how likely they are to kill the deal.
2. For each question, tell me what a SATISFACTORY written answer
   looks like — format and specificity level, not content.
3. Identify which answer is currently weakest and would stall deal.
4. Tell me the minimum viable Evidence Pack for an early-stage
   company that cannot yet have SOC 2.

Do not soften anything. Write as you would internally.
```

### Prompt 4.7.5 – One-Pager Defensibility Check (trước khi nộp)

```
I wrote this Monetization One-Pager for an AI product:
"[paste your one-pager]"

Evaluate it the way a Series A investor reading 50 decks today would:

1. For each number, can you tell WHY it is that number and not
   another? List any unjustified number.
2. Which claim would you push back on first?
3. Could a competing founder write this with their own numbers
   swapped in? Point to sentences that make it too generic.
4. Is the pricing internally consistent — Cost/Job, price, GM,
   and breakeven actually agree arithmetically?
5. Does the chosen channel follow logically from ARPU and
   pain moment, or were they decided independently?
6. Suggest ONE specific edit that would make this 10x more
   defensible.

Be brutally honest.
```

---

## ✅ FINAL CHECKLIST – TRƯỚC KHI NỘP

```
[ ]  1. Tab 1 – đủ 5 thành phần chi phí, không ô nào trống vô lý
[ ]  2. Tab 1 – mẫu số là JOB HOÀN THÀNH, không phải job thử
[ ]  3. Tab 2 – Giá bán ≥ 3 × Cost/Job, Gross Margin ≥ 60%
[ ]  4. Tab 2 – Breakeven containment đã tính, đã so với eval
[ ]  5. Tab 3 – Value Metric + Decision Note + 2 benchmark có link
[ ]  6. Tab 4 – Ngân sách CAC, deal/AE/ngày, 1 kênh duy nhất
[ ]  7. Tab 5 – 90-day plan có số; Evidence Pack có deadline
[ ]  8. Ghi ngày kiểm tra giá API ở tab 6_Benchmarks
[ ]  9. One-Pager – 3 khối, mọi số khớp Excel
[ ] 10. Đã chạy ít nhất 2 prompt ở §4.7 và ghi lại accept/reject
```

> **Minimum bar:** Một người lạ mở file Excel và đọc One-Pager phải hiểu được – bạn bán gì, cho ai, tính tiền thế nào, có lãi trên mỗi đơn vị không, và tiếp cận khách qua đâu – mà không cần hỏi lại quá 3 câu.

---

## 📤 NỘP BÀI

| Mục | Yêu cầu |
|-----|---------|
| **Nộp khi nào** | Trước buổi tiếp theo |
| **Nộp ở đâu** | Submit link repo trực tiếp trên Vlearn |
| **Tên repo** | `Track1_Day22_MHV_HoVaTen` |
| **Tên file** | `[Tên]_Day22_model.xlsx` và `[Tên]_Day22_onepager.pdf` |
| **Bao gồm** | (1) File Excel 5 tab hoàn chỉnh · (2) Monetization One-Pager (PDF hoặc DOCX) |

---

## 📊 RUBRIC CHẤM ĐIỂM (100 điểm)

| # | Tiêu chí | Điểm | Lưu ý |
|---|---------|------|-------|
| 1 | **Cost/Job Rigor** | 30 | HITL hoặc Retry = 0 mà không có lý do → mất ≥10 điểm; GM > 85% → coi như thiếu chi phí |
| 2 | **Value Metric Justification** | 25 | Chấm chất lượng lập luận, không chấm lựa chọn; chọn Outcome không có Attribution → tối đa 10/25 |
| 3 | **Channel Evidence** | 20 | Partner-Led không có tên công ty → tối đa 8/20; chọn > 1 kênh → trừ 5 điểm |
| 4 | **Pain Moment & 90-Day Plan** | 15 | Pain Moment chung chung → 0 điểm phần này |
| 5 | **Evidence Pack Readiness** | 10 | Ô trống không có deadline → 0 điểm dòng đó |

| Band | Điểm | Ý nghĩa |
|------|------|---------|
| Outstanding | 90–100 | Có thể đem đi gặp khách hoặc nhà đầu tư ngay |
| Strong | 75–89 | Đủ trình sếp, cần làm rõ 1–2 điểm |
| Pass | 60–74 | Hiểu khái niệm nhưng số liệu còn yếu |
| Needs rework | 40–59 | Sai một khái niệm core |
| Fail | < 40 | Chưa đạt minimum bar |

---

## 💬 CÂU CHỐT MANG THEO

> *"Chạy được là bài toán kỹ thuật. Bán được là bài toán sinh tồn."*

> *"Giá là Value Metric, không phải con số. Chọn sai đơn vị thì mọi mức giá đều sai."*

> *"Không có Eval thì không có Attribution. Không có Attribution thì đừng bán Outcome."*

> *"Chia cho job HOÀN THÀNH, không phải job đã thử."*

> *"HITL và Retry là hai cục hay quên nhất – và là hai cục giết biên lợi nhuận."*

> *"GM 85% ở mô hình AI thường không phải bạn giỏi – mà là bạn quên một khoản."*

> *"Pain Moment quyết định kênh phân phối – không phải ngược lại."*

> *"Partner-Led không có tên công ty thì chưa phải là kênh."*

> *"Pricing là giả thuyết, không phải chân lý. Không dám đổi giá mới là thất bại."*

---

*Tài liệu này tổng hợp từ hướng dẫn Lab Day 22 – Track 1. Ngày tổng hợp: 08/10/2026.*
