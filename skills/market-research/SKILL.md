---
name: market-research
description: Nghiên cứu thị trường 1 trang (1-page research) cho một ngành/ngách theo quy trình 6 bước — tổng quan, danh sách đối thủ, teardown tóm tắt kèm giá, ma trận khoảng trống có chấm điểm. Dùng khi người dùng nói "nghiên cứu thị trường", "market research", "đọc thị trường ngành X", "đối thủ trong ngách Y là ai", hoặc cần bản đồ ngành trước khi định vị sản phẩm. Không dùng khi chỉ cần mổ xẻ 1 đối thủ cụ thể (dùng competitor-teardown) hoặc đã có research và cần chốt ICP/USP (dùng product-positioning).
---

# market-research

Mục tiêu: trong **một trang** trả lời được 4 câu: thị trường này là gì và to bao nhiêu, ai đang chơi, họ bán cái gì với giá nào, chỗ nào còn trống mà đáng vào.

Tư duy nền: đọc thị trường như đọc bản đồ trước khi chọn chỗ đứng. Không nhảy vào một đối thủ; quét cả bản đồ, phân tầng, rồi mới zoom.

## 0. Pre-flight — hỏi trước khi chạy (bắt buộc)

Chỉ hỏi cái nào **chưa rõ** từ yêu cầu. Tối đa 3 câu, gộp thành 1 lượt.

| Cần biết | Vì sao | Mặc định nếu người dùng không trả lời |
|---|---|---|
| Ngành/ngách cụ thể (1 câu) | "AI cho BĐS" quá rộng; "AI chấm điểm lead cho môi giới BĐS thứ cấp" mới quét được | Dừng, không đoán |
| Phạm vi địa lý | Quyết định đối thủ và mức giá | Hai lăng kính: Global (tham chiếu US/SEA) + Việt Nam |
| Góc nhìn sản phẩm | Quét dưới góc "mình định bán gì" để ma trận có ý nghĩa | Nếu chưa có, quét trung lập và ghi rõ |
| Ai đọc báo cáo | Founder / nhà đầu tư / khách hàng → đổi độ sâu | Founder tự dùng để ra quyết định |

Nếu người dùng đưa yêu cầu mơ hồ kiểu "research thị trường AI đi" → **verify lại trước**, không chạy. Đây là bước rẻ nhất để tránh 1 giờ research sai hướng.

## 1. Quy trình 6 bước

### Bước 1 — Định nghĩa ranh giới thị trường
- Viết 1 câu định nghĩa ngách: *[ai] dùng [cái gì] để [làm gì] thay vì [cách cũ]*.
- Liệt kê 2–3 ngách **liền kề** và nói rõ vì sao loại ra (để người đọc biết ranh giới).
- Ghi giả định về khách hàng trả tiền (người dùng ≠ người trả tiền trong nhiều ngành B2B).

### Bước 2 — Tổng quan thị trường (Global + Việt Nam)
Tìm bằng web search, **mỗi số liệu phải có nguồn + năm**. Không có nguồn → ghi "ước lượng" và cách ước lượng.
- Quy mô: TAM/SAM nếu có báo cáo; nếu không, ước lượng bottom-up (số khách tiềm năng × giá × tỷ lệ thâm nhập hợp lý).
- Xu hướng 12–24 tháng: 3 lực đẩy, 2 lực cản.
- Việt Nam: quy mô người dùng, mức sẵn sàng chi trả, kênh mua chủ đạo (Zalo/Facebook/đại lý…), rào cản (pháp lý, thói quen, thanh toán).

### Bước 3 — Lập danh sách đối thủ (10–15, chia 3 tầng)
| Tầng | Định nghĩa | Số lượng |
|---|---|---|
| Trực tiếp | Cùng khách, cùng job-to-be-done | 4–6 |
| Gián tiếp | Khác sản phẩm, cùng ngân sách của khách | 3–5 |
| Thay thế | Cách "tự làm"/thủ công/công cụ tổng quát (Excel, ChatGPT, thuê người) | 2–3 |

Với mỗi đối thủ ghi: tên, nước, năm thành lập, phân khúc khách, funding/traction nếu có (nguồn), 1 câu "họ hứa gì".
Tầng "thay thế" **không được bỏ** — ở Việt Nam đối thủ lớn nhất thường là "làm tay + Zalo".

### Bước 4 — Teardown tóm tắt kèm giá
Cho 4–6 đối thủ trực tiếp, mỗi đối thủ 5 dòng:
- Tính năng lõi (3 gạch đầu dòng)
- Mô hình giá + mức giá (USD và/hoặc VND, ghi gói nào, nguồn, ngày xem)
- Tầng công nghệ: chỉ "ghi chép/tự động hoá đơn thuần" hay có "tầng đối chiếu/ra quyết định"
- Điểm mạnh 1 dòng · Điểm yếu 1 dòng (từ review thật: G2, Capterra, App Store, group Facebook, Reddit)
- Cần mổ sâu hơn? → đánh dấu để chạy `competitor-teardown`

### Bước 5 — Ma trận khoảng trống (market matrix)
Chọn 2 trục **có ý nghĩa với khách hàng**, không phải trục kỹ thuật. Trục gợi ý:
- Phân khúc khách (cá nhân / team nhỏ / doanh nghiệp)
- Mức độ "làm thay" (công cụ hỗ trợ → agent tự chạy)
- Giá (freemium / <$30 / $30–100 / enterprise)
- Ngôn ngữ & bản địa hoá (English-only / có tiếng Việt / built-for-VN)

Đặt từng đối thủ vào ô. Ô trống → **chấm điểm trước khi gọi là cơ hội**:

| Tiêu chí | 1 | 3 | 5 |
|---|---|---|---|
| Độ đau (khách có tự tìm giải pháp không?) | không ai than | có than trên group/forum | đang trả tiền cho cách tệ hơn |
| Khả năng trả tiền | không có ngân sách | có nhưng nhỏ | đã có dòng ngân sách sẵn |
| Độ khó copy (moat) | 1 tuần ai cũng làm được | cần domain expertise | cần dữ liệu/quan hệ/pháp lý riêng |

Ô nào ≥ 11/15 mới đưa vào phần "cơ hội". Ô trống điểm thấp ghi rõ "trống vì không đáng vào".

### Bước 6 — Kết luận 5 dòng
- Khoảng trống đáng vào nhất + điểm
- Đối thủ nguy hiểm nhất và vì sao
- Mức giá thị trường đang chấp nhận (dải min–max)
- 1 rủi ro lớn nhất (ví dụ: nền tảng lớn ra tính năng đè)
- Bước tiếp theo: chạy `competitor-teardown` cho ai, rồi `product-positioning`

## 2. Tiêu chuẩn đầu ra

- File `research.md` theo `templates/one-page-research.md`. **Tối đa ~700 từ + 2 bảng** — vượt là chưa chắt lọc.
- Mọi con số có nguồn (link + năm) hoặc ghi rõ là ước lượng.
- Phân biệt rõ trong văn bản: **Dữ kiện** / **Giả định** / **Suy luận**.
- Giá luôn ghi kèm ngày xem vì SaaS đổi giá thường xuyên.
- Không dùng tính từ rỗng ("tiềm năng lớn", "bùng nổ") nếu không có số đi kèm.

## 3. Nguồn ưu tiên (thứ tự)
1. Trang pricing/docs chính chủ của đối thủ
2. Review người dùng thật (G2, Capterra, Product Hunt, App Store/Play Store, group Facebook ngành, Reddit)
3. Báo cáo ngành có tên (Statista, Grand View, McKinsey, VNDirect, Vietnam Briefing…) — ghi năm
4. Crunchbase/LinkedIn cho funding, headcount
5. Tin tức chỉ để lấy xu hướng, không lấy số quy mô

## 4. Fallback
- Không tìm được giá công khai → ghi "giá theo yêu cầu", tìm review nhắc giá, hoặc để trống có chú thích. Không bịa.
- Thị trường VN gần như chưa có đối thủ → đó **là dữ kiện quan trọng**, ghi rõ và phân tích 2 khả năng: chưa ai cần / chưa ai làm.
- Quá nhiều đối thủ (>30) → ngách chưa đủ hẹp, quay lại Bước 1 thu hẹp.

## 5. Anti-pattern
- Liệt kê 30 đối thủ không phân tầng.
- Ma trận mà đối thủ dồn hết vào 1 ô → chọn sai trục.
- Kết luận "thị trường lớn, cơ hội nhiều" không có ô nào được chấm điểm.
- Chỉ nhìn Global và bỏ cột Việt Nam (hoặc ngược lại).
