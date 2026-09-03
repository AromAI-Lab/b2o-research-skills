---
name: competitor-teardown
description: Mổ xẻ (teardown) một đối thủ cụ thể từ website, pricing, docs, video demo, review — ra bản phân rã gồm kiến trúc, xác thực, client surface, mô hình giá, tech stack, điểm yếu khai thác được, viết theo tinh thần clean-room (chỉ ghi lại cái quan sát được, không sao chép). Dùng khi người dùng nói "teardown X", "mổ xẻ đối thủ X", "X làm được gì, giá bao nhiêu", "phân tích sản phẩm X". Không dùng để quét cả thị trường (dùng market-research) hay chốt định vị (dùng product-positioning).
---

# competitor-teardown

Teardown là tháo một sản phẩm ra để hiểu nó được ghép từ gì, học được gì, và **chỗ nào nó yếu**. Giống tháo iPhone để tính chi phí linh kiện — không phải để làm iPhone giả.

## 0. Pre-flight

| Cần | Mặc định |
|---|---|
| Tên + URL đối thủ | Bắt buộc |
| Nguồn có sẵn: video demo? docs API? tài khoản trial? | Hỏi; nếu không có, chạy từ nguồn công khai |
| Mục đích: học để build tương đương / tìm điểm yếu để định vị / cả hai | Cả hai |

## 1. Nguyên tắc clean-room (đọc trước khi viết)
- Ghi **cái quan sát được** (màn hình, luồng, giá, thông điệp), không ghi mã nguồn, không sao chép nội dung/thiết kế.
- Bản teardown là **spec quan sát** — đủ để một người chưa từng thấy sản phẩm hiểu nó làm gì; đó là "Đội A" trong mô hình clean-room. Người build sau ("Đội B") chỉ đọc bản này.
- Không dùng nhãn hiệu, tên, hình ảnh của đối thủ vào sản phẩm của mình.

## 2. Quy trình 5 bước

### Bước 1 — Thu thập nguồn (15 phút, không hơn)
Thứ tự: pricing page → landing page (thông điệp, ICP họ nhắm) → docs/API/changelog → video demo (YouTube, trang chủ) → review (G2/Capterra/App Store/group FB/Reddit) → LinkedIn (headcount, tuyển vị trí gì = họ đang build gì) → Crunchbase.
Ghi lại mỗi nguồn với ngày xem.

### Bước 2 — Capture
- **Video demo:** với video ≤ 15 phút, xem/cắt ~1 frame mỗi 30–60 giây; với từng frame ghi: màn hình gì, thao tác gì, output gì. Từ chuỗi frame → suy ra **user flow** từng bước.
- **Docs/API:** liệt kê endpoint/đối tượng dữ liệu chính (Lead, Conversation, Score…) → suy ra data model.
- **UI:** liệt kê màn hình chính (≤ 10) và đối tượng trên mỗi màn.

### Bước 3 — Phân rã theo 6 lớp

| Lớp | Câu hỏi | Ghi gì |
|---|---|---|
| Architecture | Đơn khối hay nhiều dịch vụ? Có pipeline nền không? | sơ đồ 1 dòng: input → xử lý → output |
| Identity/Auth | Đăng nhập kiểu gì? Multi-tenant? Phân quyền? | SSO/OAuth/email, vai trò |
| Client surface | Khách chạm vào qua đâu? | web app / mobile / Zalo-WhatsApp / Chrome ext / API / MCP |
| Data & AI layer | Chỉ ghi chép/tự động hoá, hay có tầng **đối chiếu/ra quyết định**? Model gì (nếu công bố)? Grounding vào dữ liệu riêng không? | mức độ "làm thay" 1–5 |
| Pricing | Mô hình (seat/usage/flat), gói, giá, cái gì bị khoá ở gói cao | bảng giá + ngày xem |
| Go-to-market | Bán cho ai, qua kênh nào, thông điệp chính | ICP họ tự nhận, kênh |

### Bước 4 — Điểm yếu khai thác được
Tìm từ review thật, không tự nghĩ. Phân loại:
- **Cấu trúc** (họ khó sửa): mô hình giá, kiến trúc, thị trường họ đã cam kết
- **Thực thi** (họ sẽ sửa được): bug, thiếu tính năng, hỗ trợ chậm
- **Bản địa** (họ không quan tâm): không có tiếng Việt, không có Zalo, không hoá đơn VAT, thanh toán USD

Điểm yếu **cấu trúc** và **bản địa** mới là chỗ định vị được; điểm yếu thực thi chỉ là cửa sổ tạm.

### Bước 5 — Kết luận
- 3 thứ đáng học (không phải đáng copy)
- 3 thứ họ yếu mà mình có lợi thế
- Ước lượng "để build bản tương đương 80 % cần gì": data, tích hợp, thời gian (giả định ghi rõ)

## 3. Đầu ra
`teardown-<tên>.md` theo `templates/teardown.md`, ≤ 1 trang. Kèm bảng nguồn.

## 4. Fallback
- Không có video/trial → ghi rõ "teardown từ nguồn công khai, độ tin cậy trung bình"; không suy đoán tính năng chưa thấy.
- Giá ẩn → tìm review/Reddit nhắc giá, hoặc ghi "theo yêu cầu, thường là enterprise".

## 5. Anti-pattern
- Liệt kê 40 tính năng không phân lớp.
- Chỉ khen hoặc chỉ chê; thiếu cột "học được gì".
- Điểm yếu là ý kiến cá nhân, không có review làm bằng.
