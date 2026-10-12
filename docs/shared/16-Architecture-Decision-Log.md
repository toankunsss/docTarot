# Cosmic Diary — Decision Log

| Thuộc tính | Giá trị |
|---|---|
| Phiên bản | 0.1 |
| Ngày | 10/10/2026 |
| Trạng thái | BASELINED FOR DRAFTING |
| Phạm vi | Quyết định sản phẩm và kiến trúc làm cơ sở viết đặc tả |

## Quy ước

Các quyết định dưới đây được Product Owner ủy quyền cho BA lựa chọn để tiếp tục xây dựng tài liệu. Chúng được xem là baseline hiện hành, có thể thay đổi qua Change Request. Mọi thay đổi phải đánh giá tác động tới requirement, UX, API, dữ liệu và kiểm thử.

## Decision Register

| ID | Quyết định | Lựa chọn được chốt | Lý do | Tác động chính |
|---|---|---|---|---|
| DEC-001 | Thị trường/ngôn ngữ MVP | Việt Nam, tiếng Việt; thiết kế sẵn khả năng localization | Giảm phạm vi nội dung và QA, phù hợp giai đoạn kiểm chứng | `vi-VN` là locale mặc định; chuỗi UI không hard-code |
| DEC-002 | Độ tuổi tối thiểu | 18+ | Giảm rủi ro consent và nội dung cảm xúc/bói toán với trẻ vị thành niên | Age gate, Terms và Privacy bắt buộc |
| DEC-003 | Vai trò AI | Hybrid: dữ liệu nền đã duyệt + AI diễn giải có ràng buộc | Cân bằng cá nhân hóa, chất lượng và chi phí | Prompt/version, moderation, fallback và audit bắt buộc |
| DEC-004 | Mobile authentication | Guest-first; cho phép nâng cấp/liên kết Apple hoặc Google | Giảm ma sát lần đầu nhưng vẫn hỗ trợ đồng bộ | Guest identity, merge và account-linking API |
| DEC-005 | Website account | Không đăng nhập trong MVP | Giữ website SEO-first và giảm scope | Web result không lưu cloud; CTA sang App |
| DEC-006 | Tarot artwork | Bộ bài Cosmic Diary tự sở hữu/thuê thiết kế với quyền thương mại đầy đủ | Tránh phụ thuộc license bên ngoài | Phải có asset/license register trước production |
| DEC-007 | Lá bài ngược | Không dùng reversal trong MVP | Giảm gấp đôi khối lượng nội dung và QA | Schema vẫn dự phòng `orientation`, mặc định `upright` |
| DEC-008 | Horoscope | Nội dung nền do biên tập duyệt; AI hỗ trợ biến thể; phát hành hằng ngày | Có kiểm soát biên tập và vẫn cá nhân hóa | CMS workflow và content version bắt buộc |
| DEC-009 | Tử vi/ngũ hành | Ngoài MVP; nghiên cứu cho Phase 2 | Đây là hệ nghiệp vụ riêng, dễ gây phình phạm vi | Không hiển thị trong MVP; giữ trong roadmap |
| DEC-010 | Monetization MVP | Một gói Premium subscription tháng/năm; không rewarded ads | Entitlement đơn giản, dễ đo conversion | Store purchase, restore, server validation |
| DEC-011 | Quyền lợi Premium | Không giới hạn Tarot theo fair-use, lịch sử đầy đủ, diễn giải sâu, không quảng cáo; Free có quota cấu hình từ xa | Tạo khác biệt rõ mà không hard-code con số | Quota là remote config; giá/quota cụ thể chốt trước release |
| DEC-012 | CMS | Headless CMS hỗ trợ preview, RBAC, version và webhook | Rút ngắn thời gian phát triển | Cần adapter để tránh khóa chặt nhà cung cấp |
| DEC-013 | Numerology | Pythagorean; MVP chỉ dùng ngày sinh để tính Life Path | Giảm tranh luận chuẩn hóa tên tiếng Việt | Name-based numbers để Phase 1.1 |
| DEC-014 | Compatibility | MVP dựa trên Sun sign với ma trận 12x12 được biên tập | Kết quả ổn định, giải thích được | Không tuyên bố birth-chart compatibility |
| DEC-015 | Daily timezone | Theo timezone IANA hiện tại của người dùng; một ngày tính từ 00:00–23:59 local | Phù hợp trải nghiệm hằng ngày | Chống lạm dụng đổi timezone bằng server rules |
| DEC-016 | Guest merge | Dữ liệu guest chưa trùng được nhập vào tài khoản; dữ liệu server thắng khi xung đột; không merge entitlement | Dễ giải thích và giảm mất dữ liệu | Cần preview/summary merge và idempotency |
| DEC-017 | Chia sẻ | Chỉ chia sẻ nội dung kết quả đã được làm sạch; không gồm tên, ngày sinh, mood/note; link hết hạn sau 30 ngày và có thể thu hồi | Bảo vệ dữ liệu cá nhân | Public share token ngẫu nhiên, revocable |
| DEC-018 | Notification | Tách service, engagement và marketing; marketing cần opt-in riêng | Tuân thủ consent và dễ quản lý | Preference theo category; audit consent |
| DEC-019 | CMS roles | Writer, Editor, Approver, Administrator; nguyên tắc least privilege | Đủ cho workflow nội dung MVP | Writer không publish; Approver mới publish |
| DEC-020 | NFR baseline | MVP mục tiêu 99,9% API availability/tháng; p95 read API dưới 500 ms, write dưới 800 ms, không tính latency AI; AI có timeout/fallback | Có metric kiểm chứng được nhưng thực tế cho MVP | Load test, SLO dashboard và alerting |

## Các tham số vẫn phải cấu hình trước phát hành

| ID | Tham số | Trạng thái |
|---|---|---|
| CFG-001 | Số lượt Tarot miễn phí/ngày | PROPOSED: 3; cấu hình từ xa |
| CFG-002 | Thời gian trial Premium | PROPOSED: 7 ngày nếu store/marketing cho phép |
| CFG-003 | Giá tháng/năm | OPEN — cần nghiên cứu thị trường và store pricing |
| CFG-004 | Retention diary/history sau xóa tài khoản | PROPOSED: xóa/anonymize trong 30 ngày, backup theo chu kỳ tối đa 90 ngày |
| CFG-005 | AI timeout trước fallback | PROPOSED: 12 giây |

