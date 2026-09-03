# b2o-research-skills

Bộ 3 skill cho Claude Code / Claude Desktop để **đọc một thị trường** theo quy trình lặp lại được:
nghiên cứu thị trường 1 trang → mổ xẻ đối thủ (teardown) → định vị sản phẩm có kiểm tra khác biệt.

Viết trong khuôn khổ chương trình **Build to Own – Buổi 3** (bài tập 3, bổ trợ), dùng để hoàn thành bài tập 1 và 2,
sau đó tái sử dụng cho từng ngành khách hàng của 10X System (BĐS, bảo hiểm, nông sản, giáo dục…).

> Nguyên tắc: *cái gì lặp lại hoặc đi theo quy trình từng bước thì đóng gói thành skill cho AI chạy.*
> Skill giữ **quy trình + tiêu chuẩn đầu ra**; AI lo phần thực thi; con người giữ 2 việc: đặt mục tiêu và đánh giá.

## Ba skill và chuỗi chạy

| # | Skill | Đầu vào | Đầu ra | Phục vụ |
|---|-------|---------|--------|---------|
| 1 | `market-research` | ngành + phạm vi địa lý + góc nhìn sản phẩm | `research.md` 1 trang: tổng quan, danh sách đối thủ, teardown tóm tắt + giá, ma trận khoảng trống | Bài tập 1 |
| 2 | `competitor-teardown` | 1 đối thủ (URL / video demo / docs) | `teardown-<tên>.md`: kiến trúc, auth, client surface, pricing, tech stack, điểm yếu | Bài tập 1 (phần sâu) |
| 3 | `product-positioning` | research + teardown | `positioning.md`: ICP, giá dự kiến, USP **đã qua kiểm tra khác biệt** | Bài tập 2 |

```
market-research  ──►  competitor-teardown (x N đối thủ)  ──►  product-positioning
   (bản đồ)                 (mổ xẻ)                          (chọn chỗ đứng)
```

Có thể chạy độc lập từng skill. Skill 3 sẽ từ chối chạy nếu chưa có ma trận khoảng trống từ skill 1.

## Điểm khác so với skill demo trong lớp

Skill demo của giảng viên thiên về Global-first / US và kết thúc ở bước viết spec.
Bộ này thêm 3 thứ vì nhu cầu của 10X System:

1. **Hai lăng kính địa lý bắt buộc** – mỗi báo cáo có cột *Global* và cột *Việt Nam* (giá, đối thủ, hành vi mua) thay vì một thị trường.
2. **Ma trận khoảng trống chấm điểm** – ô trống được chấm theo 3 tiêu chí (độ đau, khả năng trả tiền, độ khó copy) để không chọn khoảng trống "trống vì không ai cần".
3. **Differentiation check** – skill 3 bắt buộc đối chiếu từng USP ứng viên với ma trận đối thủ; USP trùng > 70 % bị loại hoặc phải viết lại. Đây là bước ép "không sao chép" mà đề bài yêu cầu.

## Cài đặt

Skill của Claude Code nằm trong thư mục `.claude/skills/<tên-skill>/SKILL.md` (của dự án) hoặc `~/.claude/skills/` (dùng chung mọi dự án).

```bash
git clone https://github.com/AromAI-Lab/b2o-research-skills.git
# dùng chung cho mọi dự án
mkdir -p ~/.claude/skills
cp -r b2o-research-skills/skills/* ~/.claude/skills/
```

Sau đó trong Claude Code gõ `/market-research`, `/competitor-teardown`, `/product-positioning`
hoặc chỉ cần nói "nghiên cứu thị trường ngành X" – Claude tự nhận diện skill qua `description`.

## Cấu trúc

```
skills/
  market-research/
    SKILL.md                       quy trình 6 bước + tiêu chuẩn đầu ra
    templates/one-page-research.md khung 1 trang
  competitor-teardown/
    SKILL.md
    templates/teardown.md
  product-positioning/
    SKILL.md
    templates/positioning.md
    checklists/differentiation-check.md
examples/
  bds-ai-sales-agent/              chạy thử đủ 3 skill trên ngách "AI lọc lead căn hộ chung cư, bán cho sale cá nhân"
    research.md                    skill 1 → Bài tập 1 (1-page research)
    teardown-structurely.md        skill 2
    teardown-roof-ai.md            skill 2
    positioning.md                 skill 3 → Bài tập 2 (ICP, giá, USP + bảng differentiation check)
    risks-and-mitigation.md        nghiên cứu sâu 5 rủi ro + phương án + khuyến nghị
```

## Bài học sau lần chạy đầu (feedback loop)

- Chuẩn "≤ 700 từ" của skill 1 không thực tế với tiếng Việt + 10 đối thủ + link nguồn → sửa thành ≈ 1 trang A4 / 1.200–1.700 từ.
- Differentiation check **loại đúng USP mà founder định dùng** ("chấm Nóng/Ấm/Lạnh" trùng ~80 % với Roof AI) và ép tìm khác biệt thật (mức "Ảo", tiêu chí chung cư VN, không cần OA). Đây là lý do bước này bắt buộc.
- Rủi ro lớn nhất không lộ ra ở bước research thị trường mà ở bước rủi ro nền tảng (Zalo không có API cá nhân) → skill 1 v0.2 nên thêm mục "Rủi ro nền tảng phân phối/dữ liệu" vào Bước 6.

## Tác giả

Mai Hương – 10X System / AromAI Lab. Viết cho Build to Own cohort 2026.
