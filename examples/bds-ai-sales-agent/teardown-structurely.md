# Teardown — Structurely

*URL: structurely.com · Nước: US (Ames, Iowa) · Ngày: 2026-09-03 · Nguồn dùng: pricing / landing / docs FUB integration / review G2-Capterra-Trustpilot / PitchBook / PR Newswire · Độ tin cậy: **trung bình-cao** (không có trial; user flow lấy từ docs tích hợp và review) · Chạy bằng skill `competitor-teardown` v0.1*

## Họ là ai
Bán **AI ISA (inside sales agent) nhắn tin/gọi/email thay người** cho team BĐS, mortgage, home services với lời hứa "thay ISA, giảm 67 % chi phí". Thành lập 2015–16, ~14 nhân viên, gọi ~$5,4 M qua 9 vòng; **CapStone Holdings mua 06/01/2026**, sau đó đổi sang giá theo credit ([PR Newswire](https://www.prnewswire.com/news-releases/capstone-holdings-inc-acquires-structurely-positioning-the-company-for-the-next-era-of-ai-driven-sales-automation-302652663.html), [PitchBook](https://pitchbook.com/profiles/company/185935-42)). Claim 13 M hội thoại AI, khách UWM, Rocket, Zillow/FUB.

## User flow quan sát được (từ docs tích hợp Follow Up Boss)
1. Lead vào CRM (FUB) → agent gắn tag `Structurely: Active` hoặc enroll qua embedded app.
2. AI "Aisa Holmes" nhắn SMS/email theo cây kịch bản; nurture tới 12+ tháng.
3. Câu hỏi qualify: **thời điểm mua (timeframe), ngân sách, đã pre-approved/cần tài chính?, khu vực, đang làm việc với agent nào chưa**.
4. Lead trả lời đủ trường hoặc NLP phát hiện câu hỏi ngoài kịch bản → gắn tag `Structurely: Needs Agent Follow up`, agent nhận SMS/email.
5. Agent thấy transcript trong timeline FUB + các trường qualify đã điền; mute AI bằng cách gỡ tag. ([FUB integration](https://www.followupboss.com/integrations/structurely))

## Phân rã 6 lớp

| Lớp | Quan sát | Nguồn |
|---|---|---|
| Architecture | CRM tag/webhook → conversation engine (cây kịch bản + LLM fine-tune, dataset có người duyệt) → SMS/voice/email gateway → ghi disposition ngược CRM | structurely.com, FUB docs |
| Identity/Auth | Account theo team/company; white-label cho CRM (FUB, Bonzo, MarketSharp); Enterprise có compliance review | structurely.com/pricing |
| Client surface | Web app + embedded app trong FUB; SMS, voice, email; tích hợp FUB, HubSpot, Salesforce, BoomTown, Bonzo, MarketSharp; API/Zapier. **Không Messenger/WhatsApp/Zalo** | structurely.com |
| Data & AI layer | "Fine-tuned AI", không nêu model; grounding = kịch bản + trường CRM, không MLS. **Không có điểm số** — nóng/lạnh = "đã trả lời + đủ trường + chưa có agent". Mức làm thay: **4/5** | Perspective AI, FUB docs |
| Pricing | Team **$499/tháng + $0,08/credit + $2.000 onboarding**; Company **$999 + $0,06/credit + $2.500**; Enterprise custom. 1 credit = 1 SMS reply / 10 s voice / 2 email. Annual; month-to-month +20 %. Không free trial. (Trước 1/2026: $299–499 theo volume — nhiều site còn dẫn giá cũ) (xem 03/09/2026) | structurely.com/pricing |
| Go-to-market | ICP tự nhận: Mortgage, Real Estate, Home Services, Private Aviation, white-label CRM; kênh = marketplace CRM; thông điệp "AI ISA replacement" | structurely.com |

## Điểm yếu

| Loại | Điểm yếu | Bằng chứng |
|---|---|---|
| Cấu trúc | Qualification "channel-driven, không conversation-driven"; không có điểm số → agent không xếp hạng được trong tệp lớn | [Perspective AI](https://getperspective.ai/blog/best-ai-isa-tools-real-estate-2026-inside-sales-agents-ranked) |
| Cấu trúc | Sau CapStone: sàn vào $499 + $2.000 onboarding → **bỏ trống phân khúc agent nhỏ** | structurely.com/pricing |
| Thực thi | Capterra 4.2/5 (6 review): "Charged after cancellation. Ghosted", "US number assigned to Canada – never worked"; Trustpilot 2.7/5 (7): "sales rep never showed up" (5/2026); G2: "bot gets tripped up" | [Capterra](https://www.capterra.com/p/236097/Structurely/), [Trustpilot](https://www.trustpilot.com/review/structurely.com), [G2](https://www.g2.com/products/structurely/reviews) |
| Bản địa (VN) | Không tiếng Việt, không Zalo, số điện thoại chỉ US/CA, USD | structurely.com |

## Kết luận
- **Đáng học:** 1. Handoff bằng **tag trong CRM của khách** — không bắt đổi tool. 2. Giá theo **credit/action** thay vì per-seat — khớp với đơn vị "lead" mà sale VN đã quen trả. 3. Bộ 5 câu qualify (timeframe / budget / financing / location / có agent chưa) là khung tốt để dịch sang chung cư VN.
- **Họ yếu, mình mạnh:** 1. Không chấm điểm số — mình có 4 mức Nóng/Ấm/Lạnh/**Ảo**. 2. Giá và onboarding cho team lớn — mình bán lẻ cho sale. 3. Zero Zalo/tiếng Việt.
- **Build tương đương 80 % cần:** bộ tiêu chí qualify BĐS VN (đã có nền từ bds-lead-qualifier), pipeline OCR/dán hội thoại → LLM → điểm + lý do, giao diện mobile-first; **không cần** tầng SMS/voice/CRM-sync ở MVP. Thời gian: 2–3 tuần cho 1 người + AI (giả định: dùng LLM API, không train).
