# Teardown — Roof AI

*URL: roofai.com · Nước: Canada (Montréal) · Ngày: 2026-09-03 · Nguồn dùng: pricing / features / blog (khung qualify, quan điểm CEO về guardrails) / PitchBook / Crunchbase / G2 · Độ tin cậy: **trung bình** (G2 chưa có review; số liệu do hãng tự công bố) · Chạy bằng skill `competitor-teardown` v0.1*

## Họ là ai
Bán **lớp AI hội thoại cắm vào website brokerage** — chat với khách ẩn danh, trả lời listing/khu vực/mortgage, lọc ý định, rồi **route** về đúng agent theo rule. Thành lập 2015–16, ~8 nhân viên, chỉ gọi ~$350 K ([PitchBook](https://pitchbook.com/profiles/company/120335-14), [Crunchbase](https://www.crunchbase.com/organization/roofai)); 100+ brokerage khách (BHHS, Baird & Warner, Edina Realty) ([roofai.com/about-us](https://www.roofai.com/about-us/)).

## User flow quan sát được (từ features/blog)
1. Khách ẩn danh vào website sàn → widget chat, AI có MLS trả lời listing, khu vực, mortgage.
2. AI "qualifies intent, validates contact info"; khi khách muốn xem nhà hoặc AI không trả lời được → xin email/SĐT.
3. Route theo rule: office, lãnh thổ, lịch rảnh, chuyên môn, mức giá, ngôn ngữ.
4. Agent nhận email/record CRM kèm ngữ cảnh hội thoại.
5. **Khung chấm điểm Roof khuyến nghị** (blog): 7 câu (mua/bán + lý do, timeline + sự kiện ép, tài chính pre-approved/cash, tiêu chí/ngân sách, người quyết định, có agent chưa, bước tiếp) → **thang 10: Timeline 0–3, Financing 0–3, Criteria 0–2, Engagement 0–2 → Hot 8–10 / Warm 5–7 / Cold 0–4** ([Roof blog](https://www.roofai.com/blog/questions-teams-should-answer)). "AI-qualified leads" chỉ mở ở gói Intelligence.

## Phân rã 6 lớp

| Lớp | Quan sát | Nguồn |
|---|---|---|
| Architecture | Web widget → LLM hybrid (ChatGPT + LLM khác, guardrails fair-housing, **LLM bị chặn khỏi dữ liệu real-time**) → MLS (RETS/RESO) + roster agent (API/SFTP, sync 2 lần/ngày) → routing → email/CRM | [CEO on guardrails](https://www.roofai.com/blog/roof-ai-ceo-on-chatgpt-and-the-need-for-guardrails) |
| Identity/Auth | Theo website/brokerage; multi-office chỉ ở Full Service | roofai.com/pricing |
| Client surface | Web chat là chính; SMS follow-up gói cao; CRM: FUB, Salesforce, HubSpot; Zapier, API. **Không Messenger/WhatsApp/Zalo** | roofai.com/features |
| Data & AI layer | Grounding tốt nhất trong nhóm (MLS live, dữ liệu công ty). Mức làm thay: **2/5** (self-serve; custom training chỉ Full Service) | roofai.com |
| Pricing | Free (5 lead/tháng); Core $299/tháng (trả quý) hoặc $349; Intelligence $599/$749; Full Service custom. Không setup fee, không hợp đồng. Đơn vị = **website** (xem 03/09/2026) | roofai.com/pricing |
| Go-to-market | ICP: brokerage 100+ agent, luxury, relocation, mortgage upsell; kênh SEO/blog so sánh; case study Briggs Freeman 7,5 % lead-to-close | roofai.com |

## Điểm yếu

| Loại | Điểm yếu | Bằng chứng |
|---|---|---|
| Cấu trúc | Chỉ inbound web chat; không outbound/nurture, không voice; phụ thuộc MLS (VN không có MLS) | roofai.com/features |
| Cấu trúc | 8 người, $350 K vốn sau ~10 năm → rủi ro tồn tại, khó mở rộng thị trường | PitchBook |
| Thực thi | G2 0 review, profile chưa claim; danh sách tích hợp không đầy đủ; số liệu tự công bố | [G2](https://www.g2.com/products/roof-ai/reviews) |
| Bản địa (VN) | Routing có "language" nhưng không tiếng Việt; USD; bán theo website — sale cá nhân VN không có website | roofai.com |

## Kết luận
- **Đáng học:** 1. **Thang 10 điểm minh bạch** Hot/Warm/Cold với trọng số rõ (timeline & financing nặng nhất) — có thể dịch thẳng sang chung cư VN. 2. Chặn LLM khỏi dữ liệu real-time, chỉ ground vào nguồn tin cậy — nguyên tắc chống bịa. 3. **Free tier 5 lead** để tự lan truyền.
- **Họ yếu, mình mạnh:** 1. Chỉ web chat — sale VN sống trên Zalo/Messenger, không website. 2. Không có mức **Ảo** — ở VN lead ảo từ ads/data chợ đen là nỗi đau số 1. 3. Bán theo website cho sàn 100+ agent — mình bán lẻ.
- **Build tương đương 80 % cần:** bộ tiêu chí + trọng số (1 tuần với chuyên môn sẵn có), pipeline chấm điểm từ văn bản hội thoại, giao diện mobile; **không cần** MLS/routing. Thời gian: 2 tuần cho 1 người + AI (giả định như trên).

**Lưu ý cho `product-positioning`:** vì Roof đã có thang Hot/Warm/Cold, USP "chấm Nóng/Ấm/Lạnh" **sẽ trùng >70 %** và bị differentiation check loại. Khác biệt phải nằm ở mức **Ảo**, tiêu chí chung cư VN, kênh Zalo, và không cần OA/website.
