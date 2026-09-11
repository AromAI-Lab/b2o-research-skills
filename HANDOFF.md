> ⚠️ **File này đã cũ (bản 10/09, viết khi MVP chưa build).**
> Bản bàn giao đang dùng nằm ở repo khác: `~/Downloads/loc-lead-chung-cu/HANDOFF.md`
> (github.com/AromAI-Lab/loc-lead-chung-cu). Đọc file đó thay cho file này.

---

# Bàn giao phiên làm việc — Build to Own, dự án lọc lead chung cư

*Cập nhật: 10/09/2026 · Dùng để mở phiên Claude mới mà không phải kể lại từ đầu*

## 1. Bối cảnh 1 phút

Mai Hương (10X System / AromAI Lab) học cohort **Build to Own – Affitor** (Campus: build2own.dev/app). Demo Day **20/09/2026**. Sản phẩm đang xây: **tool AI chấm điểm & lọc lead** cho **sale căn hộ chung cư** ở HN/HCM, **bán trực tiếp cho sale cá nhân** (không qua sàn).

Repo public đã nộp: **github.com/AromAI-Lab/b2o-research-skills** (nằm ở `~/Downloads/b2o-research-skills` trên MacBook, xác thực GitHub bằng `gh auth login`).

## 2. Đã xong (03/09, đã nộp Campus trước 19:30)

**Bài 3 — bộ 3 skill tự viết** (`skills/`):
- `market-research` — quy trình 6 bước → 1-page research; v0.2 đã thêm mục "Rủi ro nền tảng dữ liệu/phân phối" vào Bước 6
- `competitor-teardown` — mổ xẻ 6 lớp (architecture, auth, client surface, data & AI, pricing, GTM) + phân loại điểm yếu cấu trúc/thực thi/bản địa
- `product-positioning` — ICP, giá, USP + `checklists/differentiation-check.md` (chấm 5 tiêu chí × 2 điểm, USP < 7/10 bị loại)

**Bài 1 + 2 — chạy thử thật** (`examples/bds-ai-sales-agent/`):
`research.md` · `teardown-structurely.md` · `teardown-roof-ai.md` · `positioning.md` · `risks-and-mitigation.md`

**Khác biệt so với skill demo trong lớp:** hai lăng kính Global + Việt Nam; ma trận khoảng trống có chấm điểm (đau/tiền/moat); bước differentiation check bắt buộc.

## 3. Kết luận cốt lõi (đừng research lại)

**Định vị chốt:** Cho sale chung cư ≥ 1 năm nghề, tự chạy ads 10–20 tr/tháng, nhận 30–80 lead/tháng. Tool cho biết trong 10 giây lead nào **Ảo** để bỏ, lead nào **Nóng** để gọi trước.

**USP đã qua kiểm tra khác biệt:**
- Giữ: phát hiện lead **Ảo** (9/10) · tiêu chí chấm riêng **chung cư VN** (9/10) · **không cần OA/CRM/cài đặt** (8/10) · tool + khoá huấn luyện 10X (8/10)
- **Bị loại:** "chấm Nóng/Ấm/Lạnh" (5/10 — trùng ~80 % với Roof AI đã có thang 10 điểm Hot/Warm/Cold) · "rẻ hơn tool US 20 lần" (4/10 — tính từ)

**Giá:** ra mắt 249 k/tháng, gói 3 tháng 599 k, free 30 lead đầu. Mục tiêu 6 tháng: 349 k + gói Pro cho sàn 1,5–3 tr/tháng.

**5 rủi ro & hướng xử lý đã chốt:**

| | Rủi ro | Hướng xử lý |
|---|---|---|
| R1 | Zalo **không có API cho tài khoản cá nhân**; tool giả lập → khoá tài khoản khách. OA có API từ 2,5 tr/năm nhưng sale cá nhân không có OA | MVP đi đường **dán/chụp màn hình hội thoại**; OA webhook là gói Pro cho sàn. **Không** dùng API không chính thức (zca-js) |
| R2 | Luật BVDLCN 2026 (hiệu lực 01/01/2026): chat có SĐT/khoản vay = nhạy cảm; gửi LLM nước ngoài = chuyển xuyên biên giới; phạt tới 3 tỷ | **Ẩn danh hoá trước khi gọi AI**, không lưu chat gốc (retention 30 ngày), soạn DPA 1 trang |
| R3 | 80 % sale mới bỏ nghề trong 6 tháng; H1/2026 DN BĐS giải thể gấp 2,2 lần | Chỉ bán cho sale **≥ 1 năm đang chạy ads**; **thu trước 3 tháng**; bán "tiết kiệm tiền ads" chứ không bán "phần mềm" |
| R4 | Batdongsan (đã có pay-per-lead, tuyên bố hướng AI 8/2026), Meey, Callio có thể nhúng scoring | Đứng ở chỗ họ không muốn đứng: chấm lead **Ảo** từ mọi nguồn — nền tảng bán lead không tự nhận lead mình bán là ảo. Soát 3 tháng/lần |
| R5 | Sale trả 100 k–1 tr cho phần mềm nhưng 10–20 tr cho ads | Neo vào "lead" không neo vào "phần mềm"; đòn bẩy riêng: **tool + khoá huấn luyện** (đối thủ tool không có khoá, đối thủ khoá không có tool) |

**Giả định lớn nhất chưa kiểm chứng:** sale có chịu **dán/chụp hội thoại từng lead** để đổi lấy điểm số không, và có trả 249 k/tháng không. Đây là quyết định Type 1 — phải biết trước khi build. Nếu ≤ 2/5 sale nói có → đổi ICP sang sàn có Zalo OA.

## 4. Việc còn lại, theo thứ tự

1. **Viết bộ tiêu chí chấm điểm chung cư** — 4 mức Nóng/Ấm/Lạnh/Ảo, tín hiệu riêng của chung cư: khả năng vay (lãi 13–15 %), tiến độ thanh toán, đã xem dự án nào, hỏi giá/m² hay hỏi chung chung, số lạ/không nghe máy. Nền có sẵn: skill `bds-lead-qualifier` trong AromAI-Lab. → Đây vừa là moat vừa là công cụ để phỏng vấn.
2. **Phỏng vấn 5 sale** ≥ 1 năm nghề đang chạy ads — kịch bản + bảng ghi kết quả (chưa soạn).
3. **Build MVP** — luồng: dán/ảnh hội thoại → ẩn danh hoá → LLM chấm theo bộ tiêu chí → trả điểm + lý do + việc nên làm tiếp.
4. **Bài Demo Day 5 phút** (20/09).

**Đang vướng:** chưa có email Kyma → chưa tiến hành được (chị Hương ghi chú 10/09, chi tiết hỏi lại chị).

## 5. Cách làm việc chị muốn

Tiếng Việt; khung có cấu trúc, nêu rõ **dữ kiện / giả định / suy luận**; chỉ ra rủi ro **kèm giải pháp đã nghiên cứu**, không chỉ liệt kê vấn đề; tối đa 2 câu hỏi làm rõ trước khi bắt tay; với việc kỹ thuật (terminal, git, dev) thì **hướng dẫn từng bước và kiểm tra hiểu**, không tự làm rồi bàn giao. Không tâng bốc, sẵn sàng phản biện.

**Thao tác git chị đã thạo:** `git status` → `git add .` → `git commit -m "..."` → `git push`.
