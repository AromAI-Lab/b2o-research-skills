# AI chấm điểm & chăm sóc lead cho môi giới BĐS — Nghiên cứu thị trường 1 trang

*Ngày: 2026-09-03 · Người đọc: founder (10X System) · Góc nhìn sản phẩm: công cụ tự chấm điểm & ưu tiên lead từ hội thoại Zalo/Messenger cho sàn và môi giới BĐS Việt Nam · Chạy bằng skill `market-research` v0.1*

## 1. Ranh giới
**Định nghĩa:** Sale **căn hộ chung cư** (sơ cấp dự án và thứ cấp) dùng AI đọc hội thoại inbound (Zalo, Messenger, form) để **chấm điểm mức độ sẵn sàng mua và tự chăm sóc lead lạnh**, thay vì tự đọc và đoán bằng cảm tính.
**Loại ra:** (a) AI sản xuất nội dung/video listing — bản đồ đối thủ khác hẳn, chạy riêng; (b) AI định giá / tư vấn đầu tư cho người mua — người trả tiền khác; (c) CRM quản lý giỏ hàng cho sàn — bán cho sàn, không phải sale, chỉ là đối thủ gián tiếp; (d) đất nền, nhà phố — hành vi hỏi/mua khác chung cư (pháp lý, thanh toán tiến độ), để sau.
**Người trả tiền (dữ kiện từ founder):** **sale cá nhân**, bán trực tiếp cho sale, không qua sàn. Hệ quả: giá phải ở mức một sale tự trả được hằng tháng, mua qua Zalo/Facebook, không có quy trình duyệt ngân sách.
**Giả định:** sale chung cư nhận lead chủ yếu từ quảng cáo Facebook/Zalo và sàn phân bổ, xử lý trên tài khoản Zalo cá nhân; sale sơ cấp có volume lead cao (nhiều lead ảo) hơn thứ cấp.

## 2. Tổng quan

| | Global (tham chiếu US) | Việt Nam |
|---|---|---|
| Quy mô | AI in real estate toàn cầu ước $404.9 tỷ (2026), CAGR 33.9 % đến 2030 — số của [The Business Research Company](https://www.thebusinessresearchcompany.com/report/ai-in-real-estate-global-market-report); *gộp cả proptech nên chỉ dùng để thấy xu hướng, không dùng làm TAM cho ngách này* | Không có báo cáo riêng. **Ước lượng bottom-up:** ~300.000 người hành nghề môi giới, ~40.000 có chứng chỉ ([VARS/Bộ Xây dựng, 3/2026, qua CafeF](https://cafef.vn/chi-10-moi-gioi-bat-dong-san-co-chung-chi-hanh-nghe-188260329091606181.chn)). *Giả định* sale chung cư chiếm ~30–40 % số hành nghề (~100.000 người; chưa có số tách riêng). Nếu 3 % (3.000 sale) trả 250.000 đ/tháng → ~9 tỷ đ/năm SAM bán lẻ cho sale. Bán lẻ = churn cao theo mùa thị trường, cần tính vào |
| Lực đẩy | 1. 97 % công ty môi giới lớn ở US xác nhận agent dùng AI hằng ngày (Delta Media, qua [CafeF](https://cafef.vn/ai-dang-bienco-dat-thanh-nhung-chuyen-vien-tu-van-bds-nhat-nao-18826050205584832.chn)) 2. CRM lớn (Follow Up Boss, Lofty) đã nhúng AI scoring 3. Giá token giảm → tool chấm điểm rẻ | 1. CafeF ghi "~70 % môi giới HN/HCM đã dùng AI trong công việc" (*số tự khảo sát, chưa kiểm chứng phương pháp*) 2. Zalo là kênh inbound mặc định, chưa có tool chấm điểm hội thoại Zalo chuyên BĐS 3. Thị trường 2026 siết chứng chỉ → sàn chuyên nghiệp hoá, có ngân sách tool |
| Lực cản | 1. Nền tảng lớn ra tính năng "đè" 2. Tool US giá $299–999/tháng, không dùng được cho VN | 1. Thói quen "làm tay + Zalo" miễn phí 2. Sàn ngại thay CRM đang dùng 3. Data hội thoại nằm rải rác nhiều tài khoản Zalo cá nhân |
| Kênh mua chủ đạo | CRM marketplace, quote-gated sales | Zalo OA, group Facebook môi giới, hội thảo, giới thiệu qua sàn |
| Mức sẵn sàng chi trả | $69–$1.000/tháng/team ([Luxury Presence](https://www.luxurypresence.com/blogs/follow-up-boss-pricing/)) | Chatbot/CRM VN đang bán 200.000–1.600.000 đ/tháng ([Bizfly](https://bizfly.vn/techblog/bang-gia-chatbot-gia-re-hop-ly-pho-bien-nhat-hien-nay.html), [Getfly](https://getfly.vn/bang-gia.html)) → dải giá VN chấp nhận thấp hơn US ~10–20 lần |

## 3. Đối thủ (theo tầng)

| Tầng | Tên | Nước | Khách | Traction/funding | "Họ hứa gì" |
|---|---|---|---|---|---|
| Trực tiếp | Structurely | US | team/sàn | mua lại bởi CapStone 1/2026, đổi sang giá theo credit ([AI Tools Bakery](https://aitoolsbakery.com/blog/structurely-alternatives/)) | AI nhắn tin chăm lead thay ISA, 20+ CRM |
| Trực tiếp | Follow Up Boss (AI) | US | agent → team 30 người | CRM phổ biến nhất mảng agent US | CRM có sẵn AI ưu tiên lead |
| Trực tiếp | Lofty (Chime) | US | team | quote-gated | All-in-one CRM + AI ISA |
| Trực tiếp | Roof AI | US/CA | sàn lớn | enterprise | Lớp AI hội thoại cắm vào CRM có sẵn |
| Trực tiếp | Ylopo (Raiya) | US | team | bundle ~$295–695+/tháng | Lead gen + AI nurture |
| Gián tiếp | Getfly / Meey CRM / Landsoft / SlimCRM | VN | sàn | Getfly công khai giá; Meey trong hệ sinh thái Meey Land | CRM BĐS, tự động Zalo/ZNS, **không có chấm điểm AI** |
| Gián tiếp | Fchat / AhaChat / Botbanhang | VN | shop, SME | giá công khai 190k–2tr/tháng | Chatbot kịch bản Messenger/Zalo, không chuyên BĐS |
| Gián tiếp | F1, CallSphere, Shift AI (voice) | VN | sàn lớn | nêu tên trên CafeF, chưa thấy giá | Voice bot / lead automation cho sàn lớn |
| Thay thế | Làm tay + Zalo + Excel | VN | mọi môi giới | — | miễn phí, quen tay |
| Thay thế | ChatGPT/Gemini dán hội thoại vào hỏi | VN | môi giới trẻ | — | miễn phí, không hệ thống |

## 4. Teardown tóm tắt + giá (đối thủ trực tiếp)

**Structurely** — US
- Lõi: AI text/email trả lời lead 24/7 · đặt lịch · đẩy lead nóng về CRM
- Giá: **mâu thuẫn giữa nguồn** — G2 ghi $299–1.499/tháng theo số contact (cập nhật 10/2024, [G2](https://www.g2.com/products/structurely/pricing)); Layer3 ghi $99–499 ([Layer3](https://www.layer3labs.io/comparisons/best-ai-chatbot-for-real-estate)); AI Tools Bakery ghi sau 1/2026 là $499/$999 + $0,06–0,08/credit, onboarding $2.000+. *Suy luận: đang dịch chuyển lên enterprise, bỏ trống phân khúc nhỏ.*
- Tầng công nghệ: có tầng hội thoại + đối chiếu ý định (ra quyết định nóng/lạnh)
- Mạnh: huấn luyện riêng cho BĐS, xử lý objection · Yếu: phải có CRM riêng; sau khi đổi giá, review than đắt (cần mổ sâu)
- Mổ sâu: **có**

**Follow Up Boss** — US
- Lõi: CRM · Smart Summaries · Suggested Tasks · predictive lead prioritization (từ gói Pro)
- Giá: Grow $69/user · Pro $499/10 user · Platform $1.000/30 user (xem 03/09/2026, [Luxury Presence](https://www.luxurypresence.com/blogs/follow-up-boss-pricing/))
- Tầng công nghệ: ưu tiên lead bằng dữ liệu CRM (hành vi web, email) — **không đọc hội thoại chat**
- Mạnh: giá minh bạch, hệ sinh thái · Yếu: AI là phụ, không có Zalo, không tiếng Việt
- Mổ sâu: có (để học cách họ định nghĩa "lead priority")

**Lofty** — US
- Lõi: CRM + IDX web + AI ISA nhắn tin + scoring
- Giá: ~$449–899/tháng, quote-gated (03/09/2026, Layer3)
- Tầng: tự động hoá + scoring
- Mạnh: gom 1 chỗ · Yếu: đắt, phải bỏ CRM cũ
- Mổ sâu: không

**Roof AI** — US/CA
- Lõi: chat + SMS qualification, routing, compliance cho brokerage
- Giá: enterprise, nguồn thứ cấp ước $199–499 (AI Tools Bakery)
- Tầng: lớp AI cắm vào CRM có sẵn — **mô hình gần nhất với ý tưởng của mình**
- Mạnh: không bắt đổi CRM · Yếu: chỉ cho sàn lớn
- Mổ sâu: **có**

**Nhóm CRM VN (Getfly, Meey, Landsoft)**
- Lõi: quản lý giỏ hàng, pipeline, gửi ZNS; Getfly Startup 521.000 đ/tháng/3 user, Pro 1.568.000 đ ([Getfly](https://getfly.vn/bang-gia.html), 03/09/2026)
- Tầng: ghi chép + tự động hoá đơn thuần, **không có tầng AI ra quyết định**
- Mạnh: đã ở trong sàn, có Zalo · Yếu: không đọc hội thoại, không chấm điểm

## 5. Ma trận khoảng trống

Trục dọc: **mức "làm thay"** · Trục ngang: **bản địa hoá**

| | Global / English-only | VN, chung mọi ngành | VN, chuyên BĐS + Zalo |
|---|---|---|---|
| Chatbot kịch bản (trả lời theo cây) | Tidio, Manychat | Fchat, AhaChat, Botbanhang | — (đau 2 · tiền 3 · moat 1 = **6**, không đáng) |
| Chấm điểm & ưu tiên lead từ hội thoại | Structurely, FUB, Lofty (bán cho team, $299+) | — (đau 3 · tiền 2 · moat 2 = 7) | **TRỐNG** (đau 4 · tiền 3 · moat 3 = **10 ✅**) |
| Agent tự chăm sóc + đẩy lịch xem nhà | Roof AI, Ylopo, Structurely | — | — (đau 4 · tiền 2 · moat 2 = 8; *bước 2, sale cá nhân khó trả thêm*) |

Chấm điểm ô ✅: **Đau 4** — sale chung cư sơ cấp nhận nhiều lead ảo từ ads, than trên group và đang tự lọc bằng tay 30–60 phút/ngày; **Tiền 3** (hạ từ 4 vì người trả là sale cá nhân, không phải sàn) — sale đã quen trả 200–400 k/tháng cho Fchat/AhaChat/ads tool nhưng nhạy giá và bỏ khi thị trường chậm; **Moat 3** — cần bộ tiêu chí Nóng/Ấm/Lạnh/Ảo riêng cho chung cư (hỏi giá/m², tầng, view, tiến độ thanh toán, vay ngân hàng) + dữ liệu hội thoại Zalo thật, tool tổng quát không có.

## 6. Kết luận
- **Khoảng trống đáng vào:** *Chấm điểm & ưu tiên lead chung cư từ hội thoại Zalo, bán lẻ cho sale* — 10/15. Không đối thủ trực tiếp nào ở VN; đối thủ US bán cho team, không Zalo, không tiếng Việt, giá gấp 20–50 lần mức sale VN trả được. **Điểm trừ duy nhất là sức mua của người trả tiền** — phải bù bằng giá thấp, volume, và onboarding tự phục vụ.
- **Đối thủ nguy hiểm nhất:** không phải Structurely mà là **Meey / Batdongsan.com.vn / Getfly nhúng AI scoring vào CRM sẵn có**, hoặc chính chủ đầu tư/sàn phân bổ lead đã chấm điểm sẵn cho sale. *Suy luận, chưa thấy tín hiệu công khai.*
- **Dải giá thị trường VN chấp nhận (sale cá nhân):** 150.000–400.000 đ/tháng, tham chiếu Fchat Pro 199 k, AhaChat Pro 300–400 k; trả theo tháng/quý qua chuyển khoản, cần kích hoạt trong 5 phút.
- **Rủi ro lớn nhất:** (1) churn theo chu kỳ thị trường chung cư — sale bỏ nghề khi thị trường chậm; (2) Zalo siết API/OA cho bên thứ ba; (3) CRM VN ra tính năng tương đương bằng một bản cập nhật.
- **Bước tiếp:** `competitor-teardown` cho **Structurely** (học cách định nghĩa lead nóng/lạnh và pricing lỗi) và **Roof AI** (mô hình "lớp AI cắm vào CRM sẵn có") → `product-positioning`.

---
*Dữ kiện = có link. Giả định = ghi rõ. Suy luận = in nghiêng. Giá SaaS US mâu thuẫn giữa nguồn → ghi cả ba, không chọn bừa.*
