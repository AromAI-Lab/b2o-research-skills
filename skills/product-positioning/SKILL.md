---
name: product-positioning
description: Định vị sản phẩm từ kết quả nghiên cứu thị trường — chốt chân dung khách hàng mục tiêu (ICP), mức giá dự kiến, và USP đã qua kiểm tra khác biệt (differentiation check) đối chiếu với ma trận đối thủ. Dùng khi người dùng nói "định vị sản phẩm", "ICP là ai", "bán giá bao nhiêu", "USP của mình là gì", "mình khác đối thủ chỗ nào". Yêu cầu có sẵn research.md (từ market-research); không dùng để quét thị trường hay mổ xẻ đối thủ.
---

# product-positioning

Định vị = chọn **một chỗ đứng** trên bản đồ đã vẽ ở `market-research`, sao cho một nhóm khách cụ thể thấy mình là lựa chọn hiển nhiên, và đối thủ không dễ đứng vào cùng chỗ.

Đề bài Build to Own nhấn mạnh: **phải tìm ra sự khác biệt, không sao chép**. Skill này ép điều đó bằng bước 4.

## 0. Pre-flight — điều kiện chạy
- Bắt buộc có `research.md` với ma trận khoảng trống đã chấm điểm. Không có → dừng, yêu cầu chạy `market-research` trước. Không tự bịa ma trận.
- Nên có ≥ 1 `teardown-*.md` của đối thủ trực tiếp.
- Hỏi (nếu chưa rõ): lợi thế riêng của founder/công ty là gì (data, quan hệ, chuyên môn ngành, kênh phân phối sẵn có)? — đây là nguyên liệu để khác biệt bền.

## 1. Quy trình 5 bước

### Bước 1 — ICP (chân dung khách hàng mục tiêu)
Chọn **một** ICP chính. Viết theo khung:

| Trường | Nội dung |
|---|---|
| Ai (vai trò, quy mô) | ví dụ: môi giới BĐS cá nhân 2–5 năm nghề, 30–80 lead/tháng |
| Bối cảnh kích hoạt | tình huống khiến họ đi tìm giải pháp tuần này |
| Việc cần làm (JTBD) | "khi [tình huống], tôi muốn [..] để [..]" |
| Cách họ đang làm | thủ công / công cụ nào / thuê ai |
| Nỗi đau đo được | mất bao nhiêu giờ / tiền / deal mỗi tháng |
| Người trả tiền | có phải chính họ không |
| Kênh chạm | Zalo / Facebook group / hội thảo / giới thiệu |
| Tín hiệu "không phải ICP" | ai giống nhưng KHÔNG nên bán cho |

Dòng cuối rất quan trọng: ICP quá rộng là lỗi phổ biến nhất.

### Bước 2 — Giá dự kiến
Ba mốc, mỗi mốc có lý do:
- **Sàn** — chi phí vận hành/khách/tháng × 3 (AI token, hạ tầng, hỗ trợ)
- **Tham chiếu thị trường** — dải giá từ `research.md` Bước 6, quy đổi VND; ghi rõ đối thủ Global thường không áp được thẳng vào VN
- **Giá trị** — 10–20 % giá trị tạo ra cho khách/tháng (từ nỗi đau đo được ở Bước 1)

Chọn mô hình: flat / theo seat / theo usage / theo kết quả. Nêu vì sao mô hình đó hợp với hành vi mua ở VN (thói quen trả theo tháng qua chuyển khoản, ngại thẻ, cần hoá đơn…).
Đề xuất 1 giá ra mắt + 1 giá mục tiêu sau 6 tháng.

### Bước 3 — Sinh USP ứng viên (5–7 cái)
Sinh nhiều rồi mới lọc. Mỗi USP viết dạng: *"Chỉ có [sản phẩm] [làm được X] cho [ICP] vì [lý do đối thủ không làm được]"*.
Nguồn để sinh: ô trống điểm cao trong ma trận; điểm yếu **cấu trúc** và **bản địa** của đối thủ từ teardown; lợi thế riêng của founder.

### Bước 4 — Differentiation check (bắt buộc, không bỏ qua)
Chạy `checklists/differentiation-check.md` cho **từng** USP ứng viên. Tóm tắt:

1. **Trùng lặp:** USP này có đối thủ nào trong danh sách đã nói/đã làm chưa? Ước lượng % trùng. > 70 % → loại hoặc viết lại.
2. **Có bằng chứng:** khách có thể kiểm chứng USP trong 1 buổi dùng thử không? Không → chỉ là slogan.
3. **Bền:** đối thủ copy trong bao lâu? < 1 tháng → không phải USP, là tính năng.
4. **Gắn với ICP:** ICP có quan tâm không? (USP hay nhưng ICP không cần = vô nghĩa)
5. **Gắn với lợi thế riêng:** có xuất phát từ data/quan hệ/chuyên môn mình có mà đối thủ không có?

Chấm 5 tiêu chí × (0/1/2). USP ≥ 7/10 mới được giữ. Ghi bảng chấm vào output — **đây là bằng chứng "không copy" để nộp**.

### Bước 5 — Chốt định vị
Chọn 1 USP chính + tối đa 2 phụ. Viết positioning statement:

> Dành cho **[ICP]** đang **[nỗi đau]**, **[sản phẩm]** là **[loại sản phẩm]** giúp **[kết quả đo được]**. Khác với **[đối thủ/cách cũ]**, chúng tôi **[USP chính]**.

Kèm: 3 điều **không làm** (để giữ định vị), và 1 giả định lớn nhất cần kiểm chứng với 5 khách thật trong 2 tuần.

## 2. Đầu ra
`positioning.md` theo `templates/positioning.md`, ≤ 1 trang + bảng differentiation check.

## 3. Fallback
- Tất cả USP ứng viên < 7/10 → **đó là kết quả có giá trị**: ngách này khó khác biệt, quay lại ma trận chọn ô khác hoặc thu hẹp ICP. Không ép ra USP giả.
- Không biết chi phí vận hành → ước lượng token/khách/tháng từ kịch bản dùng điển hình, ghi rõ giả định.

## 4. Anti-pattern
- USP là tính từ: "nhanh hơn, rẻ hơn, dễ dùng hơn" (ai cũng nói được).
- ICP là "doanh nghiệp vừa và nhỏ".
- Giá chọn bằng cách lấy giá đối thủ US chia đôi.
- Bỏ bước 4 vì "mình biết mình khác rồi".
