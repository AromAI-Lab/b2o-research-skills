# [Tên tạm: LeadLọc] — Định vị sản phẩm

*Ngày: 2026-09-03 · Dựa trên: research.md, teardown-structurely.md, teardown-roof-ai.md, risks-and-mitigation.md · Lợi thế riêng của founder: (1) bộ tiêu chí Nóng/Ấm/Lạnh/Ảo đã dùng thật trong bds-lead-qualifier; (2) kênh sẵn có bán cho môi giới BĐS (Zalo OA, workshop, khoá học 10X); (3) hiểu hội thoại chốt sale chung cư VN · Chạy bằng skill `product-positioning` v0.1*

## 1. ICP

| Trường | Nội dung |
|---|---|
| Ai | Sale căn hộ chung cư (sơ cấp dự án là chính, thứ cấp phụ) tại HN/HCM, **≥ 1 năm nghề**, thuộc sàn nhưng **tự bỏ tiền chạy ads** 10–20 tr/tháng, nhận 30–80 lead/tháng |
| Bối cảnh kích hoạt | Vừa đổ 15 tr ads, 50 lead về, gọi 2 ngày toàn "hỏi cho biết", "để em xem lại", số không nghe máy; thị trường 2026 "10 người bán 1 người mua" |
| JTBD | Khi lead từ ads đổ về nhiều mà thời gian gọi có hạn, tôi muốn biết **ngay** lead nào đáng gọi trước và lead nào ảo, để không đốt thêm ads và giờ vào tệp xấu |
| Cách đang làm | Đọc chat bằng cảm tính, gọi lần lượt, ghi Excel/không ghi; hỏi đồng nghiệp "khách này ok không" |
| Nỗi đau đo được | *Ước lượng* 30–60 phút/ngày đọc-lọc; 30–40 % lead ads là ảo/không đủ tài chính (lead 200–500 k/lead → 3–6 tr/tháng tiền ads đổ vào lead ảo) |
| Người trả tiền | Chính sale (dữ kiện từ founder) |
| Kênh chạm | Zalo OA + group Facebook môi giới + workshop Zoom miễn phí của 10X (funnel đã có) |
| **Không phải ICP** | Sale mới < 6 tháng (80 % bỏ nghề, không có lead riêng); sale chỉ nhận lead sàn phân bổ (không có động cơ lọc); sàn/CĐT muốn tích hợp CRM (để gói Pro tháng 6+) |

## 2. Giá

| Mốc | Con số | Lý do |
|---|---|---|
| Sàn (chi phí × 3) | ~45 k/tháng | *Giả định* 60 lead × ~150 đ token + hạ tầng ≈ 15 k/khách/tháng |
| Tham chiếu thị trường | 99 k–1 tr/tháng | Fchat 99–999 k, AhaChat 200 k–1 tr, Getfly ~160 k/user (research.md §2, §6) |
| Giá trị (10–20 % giá trị tạo ra) | 300–600 k/tháng | Nếu loại đúng 10 lead ảo/tháng ≈ tiết kiệm 2–5 tr ads + 5 giờ gọi |
| **Giá ra mắt** | **249 k/tháng, thu 3 tháng = 599 k** (≈ 200 k/tháng); free 30 lead đầu | Mô hình: flat + gói trả trước — vì sale VN quen trả theo tháng/quý qua chuyển khoản, và trả trước chống churn theo mùa (R3). Không per-seat (sale = 1 người), không per-lead ở giai đoạn đầu (khó định nghĩa "qualified", R5) |
| Giá mục tiêu 6 tháng | 349 k/tháng; gói Pro cho sàn có Zalo OA 1,5–3 tr/tháng/team | Khi có số liệu "tiết kiệm ads" thật để chứng minh |

## 3. USP ứng viên → kiểm tra khác biệt

Chấm theo `checklists/differentiation-check.md`: T1 trùng lặp · T2 kiểm chứng được · T3 độ bền · T4 ICP cần · T5 gắn lợi thế riêng — mỗi tiêu chí 0/1/2, giữ khi ≥ 7/10.

| USP ứng viên | Đối thủ gần nhất | % trùng | T1 | T2 | T3 | T4 | T5 | Tổng | QĐ |
|---|---|---|---|---|---|---|---|---|---|
| 1. "AI chấm điểm lead Nóng/Ấm/Lạnh cho môi giới" | Roof AI (Hot/Warm/Cold 10 điểm), FUB predictive prioritization | ~80 % | 0 | 2 | 0 | 2 | 1 | **5** | **loại** — chỉ là bản dịch |
| 2. "Phát hiện lead **Ảo** trước khi tốn tiền ads và giờ gọi" (số ảo, data chợ đen, hỏi cho biết, đối thủ dò giá) | Không đối thủ nào có mức "Ảo"; chatbot VN không chấm | ~15 % | 2 | 2 | 1 | 2 | 2 | **9** | **giữ — USP chính** |
| 3. "Không cần Zalo OA, không cần cài gì, không đổi CRM — dán hội thoại là có kết quả trong 10 giây" | Structurely/Roof đều cần CRM/website; CRM VN cần OA/ZNS | ~20 % | 2 | 2 | 1 | 2 | 1 | **8** | giữ — USP phụ |
| 4. "Tiêu chí chấm riêng cho **chung cư VN**: khả năng vay 13–15 %, tiến độ thanh toán, đã xem dự án nào, hỏi giá/m² hay hỏi chung" | Roof qualify theo MLS/US; chatbot VN generic | ~25 % | 2 | 1 | 2 | 2 | 2 | **9** | giữ — USP phụ (moat) |
| 5. "Rẻ hơn tool US 20 lần" | Fchat/AhaChat cũng rẻ | ~60 % | 1 | 2 | 0 | 1 | 0 | **4** | loại — tính từ |
| 6. "Tool + huấn luyện chốt sale bằng AI trong một gói" | Không tool nào kèm huấn luyện; khoá học không kèm tool | ~10 % | 2 | 1 | 2 | 1 | 2 | **8** | giữ — làm kênh & giữ chân, không đưa lên headline |
| 7. "Có DPA và ẩn danh hoá theo Luật BVDLCN 2026" | Không đối thủ VN nào nói | ~5 % | 2 | 1 | 1 | 0 | 1 | **5** | viết lại — ICP sale không quan tâm; **giữ cho gói Pro bán sàn** |

**Câu hỏi bẫy đã tự hỏi:** (a) Che tên đi, USP 1 đọc y như Roof AI → đúng là loại. (b) "Đầu tiên tại VN" của USP 2 có phải chỉ vì đối thủ Global chưa dịch? Không — Roof/Structurely *không có* khái niệm lead ảo vì thị trường US không có data chợ đen và lead form 10 k; đây là khác biệt cấu trúc, T3 = 1 vì CRM VN vẫn có thể copy trong 3–6 tháng, moat thật là tiêu chí + data (USP 4).

## 4. Định vị chốt

> Dành cho **sale chung cư đã ≥ 1 năm nghề, tự chạy ads và ngập trong lead từ Facebook/Zalo**, đang **mất 3–6 triệu tiền ads và hàng giờ gọi mỗi tháng vào lead ảo**, **LeadLọc** là **trợ lý AI lọc lead trên Zalo** giúp **biết trong 10 giây lead nào Ảo để bỏ, lead nào Nóng để gọi trước**. Khác với **CRM và chatbot đang có (chỉ ghi chép và trả lời tự động)** và **tool US (cần CRM, $299+/tháng, không Zalo)**, chúng tôi **chấm theo tiêu chí chung cư Việt Nam, có mức "Ảo" riêng, không cần OA, không cần cài gì — dán hội thoại là xong**.

USP phụ: 1. Tiêu chí chung cư VN (vay, tiến độ, dự án đã xem) — moat theo thời gian. 2. Đi kèm huấn luyện chốt sale bằng AI của 10X.

**Không làm (để giữ định vị):**
1. Không tự động nhắn tin thay sale trên Zalo cá nhân (R1 — khoá tài khoản khách).
2. Không làm CRM, không quản lý giỏ hàng — cắm vào cái sale đang dùng.
3. Không mở rộng sang đất nền/nhà phố trước khi có 100 sale chung cư trả tiền.

**Giả định lớn nhất cần kiểm chứng (2 tuần, 5 sale ≥ 1 năm nghề đang chạy ads):** sale có chịu **dán/chụp hội thoại** mỗi lead để đổi lấy điểm số không, và có trả 249 k/tháng không. Nếu ≥ 3/5 nói có → build MVP đường A (R1). Nếu ≤ 2/5 → chuyển sang gói Pro cho sàn có OA, đổi ICP.
