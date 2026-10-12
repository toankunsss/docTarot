# Cosmic Diary — Requirement Discovery

| Thuộc tính | Giá trị |
|---|---|
| Phiên bản | 0.1 |
| Ngày | 10/10/2026 |
| Trạng thái | BASELINED FOR DRAFTING — PO đã ủy quyền BA lựa chọn phương án |
| Người soạn | Senior Business Analyst |
| Phạm vi | Mobile App, Public Website và Shared Platform |

## Lịch sử thay đổi

| Phiên bản | Ngày | Nội dung | Trạng thái |
|---|---|---|---|
| 0.1 | 10/10/2026 | Khởi tạo Requirement Discovery, đề xuất MVP và danh sách câu hỏi ưu tiên | DRAFT |
| 0.2 | 10/10/2026 | Baseline các lựa chọn Q-01–Q-24 qua Decision Log để tiếp tục đặc tả | BASELINED FOR DRAFTING |

## Mục lục

1. [Quy ước trạng thái](#1-quy-ước-trạng-thái)
2. [Đánh giá tổng quan](#2-đánh-giá-tổng-quan)
3. [Phạm vi Mobile App](#3-phạm-vi-mobile-app)
4. [Phạm vi Website](#4-phạm-vi-website)
5. [Nghiệp vụ dùng chung](#5-nghiệp-vụ-dùng-chung)
6. [Điểm chưa rõ, trùng lặp và rủi ro](#6-điểm-chưa-rõ-trùng-lặp-và-rủi-ro)
7. [MVP đề xuất](#7-mvp-đề-xuất)
8. [Câu hỏi Product Owner cần xác nhận](#8-câu-hỏi-product-owner-cần-xác-nhận)
9. [Cấu trúc tài liệu cuối cùng](#9-cấu-trúc-tài-liệu-cuối-cùng)
10. [Kế hoạch xây dựng tài liệu](#10-kế-hoạch-xây-dựng-tài-liệu)
11. [Requirement Traceability Matrix khởi tạo](#11-requirement-traceability-matrix-khởi-tạo)

## 1. Quy ước trạng thái

| Trạng thái | Ý nghĩa |
|---|---|
| CONFIRMED | Đã được Product Owner xác nhận |
| PROPOSED | Phương án BA đề xuất, chưa phải yêu cầu chính thức |
| OPEN | Thiếu quyết định hoặc cần làm rõ |
| DEFERRED | Hợp lệ nhưng chưa triển khai trong giai đoạn hiện tại |
| OUT_OF_SCOPE | Không thuộc phạm vi đã thống nhất |

Trong phiên bản 0.1, chỉ các thông tin được nêu trực tiếp trong yêu cầu đầu vào mới mang trạng thái **CONFIRMED**. Mọi con số, thuật toán, giới hạn sử dụng, giá bán và quyết định kiến trúc chưa được Product Owner trả lời đều là **OPEN** hoặc **PROPOSED**.

## 2. Đánh giá tổng quan

### 2.1 Tầm nhìn và mô hình sản phẩm

Cosmic Diary là hệ sinh thái nội dung và trải nghiệm cá nhân hóa trong lĩnh vực Tarot, chiêm tinh, cung hoàng đạo, thần số học và chăm sóc cảm xúc. Hệ sinh thái gồm ba phần:

| Thành phần | Vai trò chính | Trạng thái |
|---|---|---|
| Mobile App | Trải nghiệm cá nhân hóa, tương tác hằng ngày, lưu dữ liệu cá nhân và giữ chân người dùng | CONFIRMED |
| Public Website | Sản phẩm miễn phí độc lập, tăng trưởng SEO/social và chuyển đổi sang App | CONFIRMED |
| Shared Platform | API, dữ liệu, CMS, định danh, nội dung và đo lường dùng chung | CONFIRMED |

### 2.2 Mục tiêu kinh doanh theo sản phẩm

| Mã | Sản phẩm | Mục tiêu | Chỉ số cần xác nhận |
|---|---|---|---|
| BG-APP-01 | Mobile | Tạo thói quen sử dụng hằng ngày | DAU/MAU, D1/D7/D30 retention, streak participation |
| BG-APP-02 | Mobile | Chuyển đổi người dùng miễn phí sang trả phí | Trial-to-paid, free-to-paid, MRR, churn |
| BG-APP-03 | Mobile | Tạo trải nghiệm khám phá bản thân an toàn, tích cực | Satisfaction, save/share rate, complaint rate |
| BG-WEB-01 | Website | Thu hút organic traffic từ nội dung và công cụ miễn phí | Organic sessions, indexed pages, ranking, CTR |
| BG-WEB-02 | Website | Chuyển đổi web-to-app | CTA click, QR scan, store visit, attributed install |
| BG-WEB-03 | Website | Tăng nhận diện và khả năng chia sẻ | Referral traffic, share rate, backlinks |
| BG-SHARED-01 | Shared | Duy trì một nguồn dữ liệu và quy tắc nhất quán | Content parity, sync errors, publishing lead time |

Các ngưỡng KPI cụ thể hiện là **OPEN**.

### 2.3 Actors và stakeholders ban đầu

| Nhóm | Nhu cầu chính |
|---|---|
| Khách chưa đăng nhập | Trải nghiệm nhanh nội dung/công cụ miễn phí |
| Người dùng đã đăng nhập | Cá nhân hóa, lưu lịch sử, đồng bộ dữ liệu |
| Người dùng Premium | Quyền lợi trả phí và quản lý thuê bao |
| Content Editor | Soạn, xem trước, lên lịch và xuất bản nội dung |
| Content Approver | Duyệt nội dung trước khi công khai |
| CMS Administrator | Quản lý người dùng CMS, vai trò và cấu hình |
| Customer Support | Tra cứu trạng thái tài khoản/giao dịch trong phạm vi được phép |
| Product/Marketing/SEO | Quản lý chiến dịch, nội dung và theo dõi chuyển đổi |
| Hệ thống thanh toán/App Store/Google Play | Xác thực giao dịch và trạng thái thuê bao |
| Dịch vụ AI | Hỗ trợ tạo/diễn giải nội dung theo chính sách được duyệt |

## 3. Phạm vi Mobile App

### 3.1 Phạm vi chức năng đã xác nhận

| Module | Phạm vi | Mục tiêu chính | Ghi chú trạng thái |
|---|---|---|---|
| APP-01 | Authentication & Onboarding | Tạo danh tính và hồ sơ cá nhân hóa | CONFIRMED; Guest Mode cần làm rõ quyền |
| APP-02 | Home & Daily Cosmic Insight | Tạo điểm chạm hằng ngày | CONFIRMED; nguồn nội dung OPEN |
| APP-03 | Tarot Reading | Trải bài 1/3 lá, diễn giải, lưu và chia sẻ | CONFIRMED; AI, quota và reversal OPEN |
| APP-04 | Zodiac & Horoscope | Nội dung cung và dự báo định kỳ | CONFIRMED; mức cá nhân hóa OPEN |
| APP-05 | Zodiac Compatibility | Đánh giá tương hợp hai cung | CONFIRMED; thuật toán OPEN |
| APP-06 | Numerology & Fortune Profile | Hồ sơ thần số học/ngũ hành/tử vi | CONFIRMED; hệ quy chiếu OPEN |
| APP-07 | Cosmic Diary | Nhật ký cảm xúc và lịch sử trải nghiệm | CONFIRMED; dữ liệu nhạy cảm cần chính sách |
| APP-08 | Notifications & Gamification | Nhắc quay lại, streak, rewards, badges | CONFIRMED; cơ chế thưởng OPEN |
| APP-09 | Profile & Settings | Quản lý tài khoản, riêng tư và tùy chọn | CONFIRMED |
| APP-10 | Monetization | Freemium, subscription, IAP, rewarded ads | CONFIRMED; gói/giá/quyền lợi OPEN |

### 3.2 Vai trò riêng của Mobile App

- Lưu và khai thác hồ sơ cá nhân sâu hơn Website.
- Hỗ trợ push notification, daily check-in, streak và in-app purchase.
- Cung cấp nhật ký cảm xúc, lịch sử Tarot và thống kê cá nhân.
- Là điểm đến chính của chuyển đổi từ Website.

### 3.3 Ranh giới cần giữ

- Yêu cầu SEO, robots, sitemap, structured data và quản trị trang công khai không thuộc tài liệu Mobile.
- Mobile có thể dùng nội dung do CMS quản lý nhưng không chứa nghiệp vụ vận hành CMS.
- Quy tắc Tarot, Zodiac, Numerology, entitlement và analytics dùng chung chỉ được định nghĩa chuẩn tại `shared/`; tài liệu Mobile chỉ tham chiếu.

## 4. Phạm vi Website

### 4.1 Phạm vi chức năng đã xác nhận

| Module | Phạm vi | Mục tiêu chính | Ghi chú trạng thái |
|---|---|---|---|
| WEB-01 | Marketing Landing Page | Giới thiệu và thúc đẩy tải App | CONFIRMED |
| WEB-02 | Free Tarot Online | Cung cấp giá trị tức thời và tạo traffic/share | CONFIRMED; quota/login OPEN |
| WEB-03 | Zodiac Discovery | Nội dung cung hoàng đạo và SEO | CONFIRMED |
| WEB-04 | Zodiac Compatibility | Công cụ tương hợp dễ chia sẻ | CONFIRMED; thuật toán OPEN |
| WEB-05 | Numerology Tools | Công cụ miễn phí và nội dung liên quan | CONFIRMED; dữ liệu đầu vào OPEN |
| WEB-06 | Tarot Knowledge Library | Thư viện 78 lá và hướng dẫn | CONFIRMED |
| WEB-07 | Blog & Content Hub | Mở rộng cụm nội dung SEO | CONFIRMED |
| WEB-08 | App Download & Conversion | Deep link, QR và attribution | CONFIRMED; nhà cung cấp OPEN |
| WEB-09 | SEO Management | Kiểm soát index, metadata và schema | CONFIRMED |
| WEB-10 | CMS Administration | Quản lý và xuất bản nội dung | CONFIRMED; CMS riêng hay bên thứ ba OPEN |

### 4.2 Vai trò riêng của Website

- Cho phép sử dụng các công cụ cốt lõi mà không bắt buộc cài App.
- Xây dựng topic cluster SEO quanh Tarot, Zodiac và Numerology.
- Tạo nội dung có URL ổn định, index được và chia sẻ tốt.
- Đo đầy đủ hành trình từ landing page/công cụ đến store và install.

### 4.3 Ranh giới cần giữ

- Nhật ký cảm xúc, push notification, streak và IAP không mặc định thuộc Website.
- Website có thể cho đăng nhập để đồng bộ nhưng đây là quyết định **OPEN**, không tự động suy ra từ Shared Authentication.
- CMS là giao diện quản trị nội bộ; cần tách khỏi public website về quyền truy cập và tài liệu trang.

## 5. Nghiệp vụ dùng chung

| Mã miền | Nghiệp vụ chuẩn dùng chung | Sản phẩm sử dụng | Trạng thái |
|---|---|---|---|
| SHR-TAROT | Bộ 78 lá, xuôi/ngược, spread, randomization, diễn giải và version | App, Web, CMS | OPEN về bộ bài và AI |
| SHR-ZODIAC | Xác định cung, timezone, cusp và nội dung horoscope | App, Web, CMS | OPEN về quy tắc biên |
| SHR-COMPAT | Mô hình điểm và diễn giải tương hợp | App, Web | OPEN |
| SHR-NUM | Công thức thần số học và chuẩn hóa tên/ngày sinh | App, Web | OPEN |
| SHR-CONTENT | Workflow, locale, lịch xuất bản, version và rollback | App, Web, CMS | OPEN |
| SHR-IDENTITY | Guest/user identity, liên kết tài khoản, consent và session | App, Web | OPEN |
| SHR-ENTITLEMENT | Free/Premium, quota, purchase validation và restoration | App, Web/API | OPEN |
| SHR-DATA | Dữ liệu cá nhân, lưu trữ, xóa, export và audit | Toàn hệ sinh thái | OPEN |
| SHR-ANALYTICS | Taxonomy sự kiện, consent, attribution và KPI | Toàn hệ sinh thái | OPEN |
| SHR-AI | Prompt/version, nguồn tri thức, moderation, fallback và cost control | App, Web, CMS | OPEN |

Nguyên tắc đề xuất: Shared Platform là nguồn chuẩn cho dữ liệu/quy tắc; App và Web không tự cài đặt các công thức khác nhau. Nội dung đã xuất bản cần có `content_version` để kết quả cũ vẫn truy vết được.

## 6. Điểm chưa rõ, trùng lặp và rủi ro

### 6.1 Các điểm cần làm rõ

| ID | Vấn đề | Tác động |
|---|---|---|
| GAP-01 | Chưa xác định AI tạo toàn bộ kết quả, biên tập nội dung có sẵn hay mô hình lai | Kiến trúc, chi phí, chất lượng, pháp lý |
| GAP-02 | Chưa xác định thị trường/ngôn ngữ phát hành đầu tiên | Nội dung, privacy, store policy, localization |
| GAP-03 | Chưa có định nghĩa gói Free/Premium, quota và giá | UX, entitlement, API, doanh thu |
| GAP-04 | Chưa xác định Website có tài khoản và đồng bộ lịch sử hay không | Authentication, data model, scope MVP |
| GAP-05 | “Astrology”, “tử vi”, “ngũ hành” và “horoscope” có thể là các hệ khác nhau | Nội dung dễ mâu thuẫn, scope phình to |
| GAP-06 | Chưa xác định nguồn/bản quyền bộ bài và hình ảnh 78 lá | Khả năng phát hành và chi phí |
| GAP-07 | Chưa xác định độ tuổi tối thiểu và cách xử lý dữ liệu cảm xúc | Privacy, consent, safety |
| GAP-08 | Chưa xác định CMS tự xây hay dùng giải pháp có sẵn | Timeline, chi phí, vận hành |
| GAP-09 | Chưa có KPI và baseline thành công của MVP | Không thể nghiệm thu mục tiêu kinh doanh |

### 6.2 Trùng lặp hợp lệ nhưng phải dùng một nguồn chuẩn

Tarot, Zodiac, Compatibility và Numerology xuất hiện ở cả App và Web. Đây là reuse nghiệp vụ, không phải hai bộ quy tắc. Mỗi sản phẩm được phép có presentation, quota hoặc CTA khác nhau; kết quả cốt lõi phải tham chiếu rule/version tại `shared/`.

### 6.3 Rủi ro nghiệp vụ chính

| ID | Rủi ro | Mức | Ứng phó đề xuất |
|---|---|---|---|
| RSK-01 | Nội dung bị hiểu như tư vấn y tế, tài chính hoặc quyết định chắc chắn | Cao | Disclaimer, tone policy, prohibited claims, safety review |
| RSK-02 | Kết quả AI thiếu nhất quán hoặc gây tổn thương | Cao | Grounding, prompt/version control, moderation, fallback nội dung duyệt sẵn |
| RSK-03 | Thu thập ngày/giờ/nơi sinh và nhật ký cảm xúc vượt nhu cầu | Cao | Data minimization, consent riêng, retention và delete/export |
| RSK-04 | Vi phạm bản quyền hình ảnh/bộ bài/nội dung | Cao | Asset provenance và license register trước phát hành |
| RSK-05 | App/Web trả kết quả khác nhau cho cùng đầu vào | Cao | Shared rules API, contract tests, versioned content |
| RSK-06 | Scope MVP quá rộng, không đủ nội dung chất lượng | Cao | Chọn một vòng lặp giá trị cốt lõi; defer phần chuyên sâu |
| RSK-07 | SEO bị ảnh hưởng bởi nội dung AI mỏng/lặp | Trung bình/Cao | Editorial workflow, unique value, canonical và quality gates |
| RSK-08 | Chi phí AI tăng khó kiểm soát | Trung bình/Cao | Cache, quota, model routing, cost telemetry, fallback |
| RSK-09 | Subscription/restore/refund sai trạng thái | Cao | Server-side validation, idempotency, reconciliation và audit |

## 7. MVP đề xuất

Đây là phương án **PROPOSED**, dùng để PO lựa chọn chứ chưa phải phạm vi chính thức.

### 7.1 Mobile MVP

Vòng lặp giá trị đề xuất: **Onboarding tối giản → Daily Insight → Tarot 1/3 lá → lưu lịch sử → quay lại qua reminder**.

| Nhóm | Bao gồm trong MVP đề xuất | Ngoài MVP đề xuất |
|---|---|---|
| Account | Guest, Apple/Google, hồ sơ ngày sinh tối thiểu, xóa tài khoản | Social graph, nhiều hồ sơ |
| Daily | Home, thông điệp ngày, Card of the Day, check-in đơn giản | Badges/reward economy phức tạp |
| Tarot | Chủ đề cơ bản, 1/3 lá, xuôi/ngược nếu được duyệt, kết quả, lưu/chia sẻ | Spread nâng cao, reader marketplace |
| Zodiac | Cung cá nhân, horoscope ngày; thư viện 12 cung | Dự báo cá nhân theo birth chart đầy đủ |
| Diary | Mood + ghi chú, lịch sử Tarot cơ bản | Phân tích nâng cao, coaching |
| Retention | Reminder opt-in, streak cơ bản | Gamification nhiều tầng |
| Monetization | Một gói subscription với entitlement rõ; restore purchase | Nhiều tier, consumable IAP, rewarded ads nếu chưa có bằng chứng |

Compatibility, Numerology/Fortune Profile đầy đủ, thống kê diary nâng cao và hệ badges được đề xuất **DEFERRED** để giảm rủi ro phạm vi.

### 7.2 Website MVP

Vòng lặp giá trị đề xuất: **Search/Social landing → công cụ/nội dung hữu ích → chia sẻ hoặc CTA tải App**.

| Nhóm | Bao gồm trong MVP đề xuất | Ngoài MVP đề xuất |
|---|---|---|
| Marketing | Landing, feature, download CTA, FAQ, legal/footer | A/B testing platform tùy chỉnh |
| Tarot | 1 lá, 3 lá, chủ đề, kết quả, share, CTA App | Tài khoản và đồng bộ lịch sử nếu chưa xác nhận |
| Zodiac | Hub 12 cung, detail, horoscope ngày | Dự báo tuần/tháng tự động quy mô lớn |
| Library | 78 trang lá bài và hướng dẫn cốt lõi | Kho nội dung dài chưa qua biên tập |
| Conversion | QR, store links, UTM/campaign tracking | Deferred deep-link journeys phức tạp |
| SEO | Metadata, canonical, sitemap, robots, OG, schema, internal links | SEO automation nâng cao |
| CMS | Article/Tarot/Zodiac, draft-review-publish, preview, RBAC cơ bản | Workflow nhiều cấp và localization phức tạp |

Compatibility và Numerology tool được đề xuất đưa vào Phase 1.1 sau khi công thức được xác nhận.

## 8. Câu hỏi Product Owner cần xác nhận

> Cập nhật 10/10/2026: Product Owner đã ủy quyền BA tự lựa chọn phương án để tiếp tục. Các lựa chọn và lý do được baseline tại [`shared/16-Architecture-Decision-Log.md`](shared/16-Architecture-Decision-Log.md). Các câu hỏi dưới đây được giữ lại nhằm bảo toàn lịch sử truy vết; những tham số giá/quota cụ thể vẫn là cấu hình cần chốt trước phát hành.

### 8.1 Nhóm P0 — chặn việc chốt MVP hoặc kiến trúc

Vui lòng trả lời trước các câu Q-01 đến Q-12. Có thể trả lời bằng mã lựa chọn và ghi chú, ví dụ: `Q-01: B — Việt Nam trước`.

| ID | Câu hỏi | Phương án và đánh đổi | BA đề xuất |
|---|---|---|---|
| Q-01 | Thị trường/ngôn ngữ phát hành đầu tiên? | A. Việt Nam/VI: nhanh và tập trung; B. Quốc tế/EN: thị trường lớn nhưng tăng compliance/content; C. VI+EN: phủ rộng nhưng gấp đôi QA | A |
| Q-02 | Đối tượng và độ tuổi tối thiểu? | 13+, 16+ hoặc 18+ ảnh hưởng consent, nội dung và store rating | 16+ hoặc 18+ sau rà soát pháp lý |
| Q-03 | Vai trò AI trong Tarot/horoscope? | A. Nội dung duyệt sẵn: ổn định, ít cá nhân hóa; B. AI tự sinh: linh hoạt, rủi ro cao; C. Hybrid: nền tảng duyệt sẵn + AI diễn giải | C |
| Q-04 | MVP Mobile có bắt buộc tài khoản? | A. Guest-first: ít ma sát nhưng khó đồng bộ; B. Login-first: dữ liệu tốt nhưng giảm conversion; C. Guest rồi nâng cấp tài khoản | C |
| Q-05 | Website MVP có đăng nhập/đồng bộ lịch sử? | Có: trải nghiệm xuyên nền tảng nhưng tăng scope; Không: nhanh, SEO-first | Không trong MVP |
| Q-06 | Bộ bài/hình ảnh Tarot nào được dùng và quyền khai thác đã có chưa? | Tự sở hữu, thuê thiết kế, public domain hoặc licensed deck | Cần xác nhận trước production |
| Q-07 | Có dùng lá ngược trong MVP không? | Có: giàu ý nghĩa nhưng tăng gấp đôi content/QA; Không: đơn giản hơn | Không, trừ khi là khác biệt thương hiệu |
| Q-08 | Nguồn horoscope và tần suất xuất bản? | Biên tập, đối tác, AI-hybrid; ngày/tuần/tháng | Hybrid; ngày trong MVP |
| Q-09 | “Tử vi/ngũ hành” theo trường phái nào và có thuộc MVP không? | Hệ Việt/Đông phương cần dữ liệu/quy tắc riêng, không đồng nhất với Western Zodiac | DEFERRED khỏi MVP |
| Q-10 | Mô hình kiếm tiền MVP? | A. Subscription; B. IAP consumable; C. Ads; D. Kết hợp | Một subscription; chưa dùng rewarded ads |
| Q-11 | Free/Premium khác nhau ở quyền lợi nào? | Cần chốt quota, lịch sử, nội dung sâu, quảng cáo và trial; chưa điền số khi PO chưa duyệt | PO cung cấp nguyên tắc; BA lập bảng entitlement |
| Q-12 | CMS tự xây hay dùng nền tảng có sẵn? | SaaS/headless: nhanh nhưng phụ thuộc; custom: linh hoạt nhưng tốn công | Headless CMS nếu đáp ứng preview/RBAC/version |

### 8.2 Nhóm P1 — cần trước khi hoàn thành SRS

| ID | Câu hỏi |
|---|---|
| Q-13 | KPI mục tiêu 90 ngày đầu cho App và Website là gì? |
| Q-14 | Quốc gia lưu trữ dữ liệu, thời hạn lưu diary/history và quy trình export/delete? |
| Q-15 | Các phương thức đăng nhập chính xác theo từng nền tảng; email/password có cần không? |
| Q-16 | Công thức Numerology sử dụng Pythagorean, Chaldean hay hệ khác; có xử lý tên tiếng Việt thế nào? |
| Q-17 | Compatibility chỉ dựa trên Sun sign hay có thêm birth chart/yếu tố khác? |
| Q-18 | Daily content đổi theo múi giờ người dùng hay theo một múi giờ hệ thống? |
| Q-19 | Sau khi Guest tạo dữ liệu rồi đăng nhập, merge theo quy tắc nào khi tài khoản đã có dữ liệu? |
| Q-20 | Cho phép chia sẻ dữ liệu cá nhân nào; link chia sẻ công khai tồn tại bao lâu và có thể thu hồi không? |
| Q-21 | Notification nào là transactional, engagement hoặc marketing; consent từng loại ra sao? |
| Q-22 | Vai trò CMS và ma trận duyệt nội dung mong muốn (Writer/Editor/Approver/Admin)? |
| Q-23 | Nhà cung cấp analytics, attribution, AI và payment backend đã được chọn chưa? |
| Q-24 | SLA/availability, lượng người dùng dự kiến và ngân sách vận hành giai đoạn đầu? |

## 9. Cấu trúc tài liệu cuối cùng

```text
docs/
├── 00-Requirement-Discovery.md
├── mobile-app/
│   ├── 00-Mobile-Document-Index.md
│   ├── 01-Mobile-Product-Vision-and-BRD.md
│   ├── 02-Mobile-Scope-and-Feature-Catalog.md
│   ├── 03-Mobile-Actors-and-Personas.md
│   ├── 04-Mobile-User-Journeys-and-Flows.md
│   ├── 05-Mobile-Functional-Requirements.md
│   ├── 06-Mobile-Business-Rules.md
│   ├── 07-Mobile-User-Stories.md
│   ├── 08-Mobile-Screen-Specifications.md
│   ├── 09-Mobile-Data-Requirements.md
│   ├── 10-Mobile-API-Requirements.md
│   ├── 11-Mobile-Non-Functional-Requirements.md
│   ├── 12-Mobile-Analytics-and-Tracking.md
│   ├── 13-Mobile-Privacy-Security-and-Consent.md
│   ├── 14-Mobile-Monetization-and-Entitlements.md
│   ├── 15-Mobile-Test-and-Acceptance-Catalog.md
│   ├── 16-Mobile-Traceability-Matrix.md
│   ├── 17-Mobile-Open-Questions-and-Decisions.md
│   ├── 18-Mobile-MVP-Scope.md
│   ├── 19-Mobile-Product-Roadmap.md
│   └── 20-Mobile-Development-Backlog.md
├── website/
│   ├── 00-Website-Document-Index.md
│   ├── 01-Website-Product-Vision-and-BRD.md
│   ├── 02-Website-Scope-and-Feature-Catalog.md
│   ├── 03-Website-Information-Architecture.md
│   ├── 04-Website-User-Journeys-and-Flows.md
│   ├── 05-Website-Functional-Requirements.md
│   ├── 06-Website-Business-Rules.md
│   ├── 07-Website-User-Stories.md
│   ├── 08-Website-Page-Specifications.md
│   ├── 09-Website-SEO-Requirements.md
│   ├── 10-Website-CMS-Requirements.md
│   ├── 11-Website-Data-and-API-Requirements.md
│   ├── 12-Website-Non-Functional-Requirements.md
│   ├── 13-Website-Analytics-and-Conversion.md
│   ├── 14-Website-Test-and-Acceptance-Catalog.md
│   ├── 15-Website-Traceability-Matrix.md
│   ├── 16-Website-Open-Questions-and-Decisions.md
│   ├── 17-Website-MVP-Scope.md
│   ├── 18-Website-Product-Roadmap.md
│   └── 19-Website-Development-Backlog.md
└── shared/
    ├── 00-Shared-Document-Index.md
    ├── 01-Shared-Domain-Glossary.md
    ├── 02-Shared-Business-Rules.md
    ├── 03-Tarot-Domain-Specification.md
    ├── 04-Zodiac-and-Horoscope-Specification.md
    ├── 05-Compatibility-Specification.md
    ├── 06-Numerology-and-Fortune-Specification.md
    ├── 07-Identity-Consent-and-Access.md
    ├── 08-Content-Lifecycle-and-CMS-Contract.md
    ├── 09-Entitlement-and-Payment-Contract.md
    ├── 10-Shared-Data-Dictionary-and-ERD.md
    ├── 11-Shared-API-Contract.md
    ├── 12-Analytics-Event-Taxonomy.md
    ├── 13-AI-Content-Safety-and-Governance.md
    ├── 14-Privacy-Retention-and-Deletion.md
    ├── 15-Shared-Non-Functional-Requirements.md
    ├── 16-Architecture-Decision-Log.md
    └── 17-Master-Traceability-Matrix.md
```

## 10. Kế hoạch xây dựng tài liệu

| Giai đoạn | Đầu ra | Điều kiện hoàn thành |
|---|---|---|
| 1. Discovery | Tài liệu này, glossary sơ bộ, decision/open-question log | PO trả lời P0; các giả định được gắn trạng thái |
| 2. Scope Baseline | BRD, feature catalog, MVP Mobile/Web, out-of-scope | PO duyệt hai MVP độc lập |
| 3. Shared Domain | Tarot/Zodiac/Numerology, identity, content, entitlement, privacy | Không còn quy tắc cốt lõi mâu thuẫn |
| 4. Functional Analysis | FR, flows, screen/page specs, data và API requirements | Mỗi flow có trạng thái/ngoại lệ/acceptance criteria |
| 5. Quality Attributes | NFR, security, accessibility, observability, localization | Mỗi NFR có metric và phương pháp kiểm thử |
| 6. Delivery Planning | Roadmap và backlog riêng cho App/Web | Story có dependency, DoD và traceability |
| 7. Quality Review | RTM tổng, consistency/completeness review | Không có ID trùng; mọi MVP story truy vết đến goal/test |

Trình tự thực hiện sau khi PO phản hồi: chốt Decision Log → cập nhật MVP → viết Shared Business Rules trước → viết Mobile và Website song song theo cùng hợp đồng → lập backlog → kiểm tra truy vết.

## 11. Requirement Traceability Matrix khởi tạo

| Business Goal | Capability/Module | Requirement Set dự kiến | Screen/Page dự kiến | API/Rule liên quan | Test/Metric | Trạng thái |
|---|---|---|---|---|---|---|
| BG-APP-01 | APP-02 Daily Insight | APP-FR-Home-* | APP-SCR-Home | SHR-CONTENT, Daily API | Retention, content load AC | PROPOSED |
| BG-APP-01 | APP-03 Tarot | APP-FR-Tarot-* | APP-SCR-Tarot-* | SHR-TAROT, Reading API | Completion/save rate, flow AC | PROPOSED |
| BG-APP-02 | APP-10 Monetization | APP-FR-Paywall-* | APP-SCR-Paywall | SHR-ENTITLEMENT | Conversion, restore/refund AC | PROPOSED |
| BG-WEB-01 | WEB-02/03/06/07 | WEB-FR-Content-* | WEB-PAGE-* | SHR-CONTENT, Public Content API | Organic sessions, index QA | PROPOSED |
| BG-WEB-02 | WEB-08 Conversion | WEB-FR-Conversion-* | WEB-PAGE-Download | Attribution contract | CTA/store/install funnel | PROPOSED |
| BG-SHARED-01 | Shared Platform | SHARED-BR-* | N/A | Versioned shared contracts | Contract tests, sync error rate | PROPOSED |

Mã chi tiết sẽ chỉ được cấp khi từng requirement được viết; không tái sử dụng hoặc đổi ý nghĩa mã sau khi đã baseline.

## Liên kết tài liệu liên quan

- Chưa có. Các liên kết sẽ được bổ sung sau khi cấu trúc thư mục được Product Owner duyệt.

