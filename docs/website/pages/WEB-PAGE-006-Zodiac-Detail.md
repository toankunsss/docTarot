# WEB-PAGE-006 — Zodiac Detail

| Thuộc tính | Giá trị |
|---|---|
| Page ID | WEB-PAGE-006 |
| Module | WEB-03 |
| Route | `/zodiac/:sign` |
| Phiên bản | 0.1 |
| Trạng thái | DRAFT |

## Mục đích

Trang SEO chi tiết cung và horoscope.

## Entry Points

Search, nav, internal link.

## Page Components

- Header và navigation.
- Nội dung chính của **Zodiac Detail**.
- Breadcrumb/internal links khi phù hợp.
- CTA tải/mở App ở vị trí không cản trở giá trị chính.
- Footer, legal và consent controls.

## Data Sources

Zodiac, Published Content, SEO. Nội dung public chỉ lấy revision Published và có content version.

## User Actions

Chọn cung, đổi period, share.

## Navigation & SEO

- Route canonical ổn định; slug cũ redirect 301 khi thay đổi.
- Metadata, canonical, Open Graph và structured data phản ánh nội dung thực tế.
- Draft/preview/search nội bộ áp dụng noindex theo policy.
- Internal links không tạo vòng lặp hoặc orphan page.

## Page States

| State | Yêu cầu |
|---|---|
| Loading | Giữ layout ổn định và ưu tiên nội dung chính |
| Empty | Giải thích và liên kết tới nội dung thay thế |
| Error | Status code đúng, Retry hoặc navigation an toàn |
| Success | Nội dung render server-side/hydrate không sai khác |
| Withdrawn | Purge cache; dùng 410, fallback hoặc redirect theo SEO policy |

## Responsive & Accessibility

- Mobile-first; hoạt động ở mobile, tablet và desktop.
- Keyboard navigation, visible focus, screen reader, contrast và zoom 200%.
- Animation tôn trọng Reduce Motion.

## Analytics & Conversion

Ghi page view, CTA, tool completion và outbound store click theo consent. Không fingerprint và không gửi dữ liệu nhạy cảm.

## Related Flows

- Module: `WEB-03`.
- [Full End-to-End System Flows](../../shared/18-End-to-End-System-Flows.md).
- [Decision Log](../../shared/16-Architecture-Decision-Log.md).

## Acceptance Baseline

- Given URL hợp lệ và content Published, when truy cập, then trang trả nội dung, metadata và canonical chính xác.
- Given content không tồn tại/withdrawn, when truy cập, then status code và fallback/redirect đúng policy.
- Given JavaScript lỗi, when trang nội dung SEO tải, then nội dung cốt lõi và navigation cơ bản vẫn sử dụng được.
- Given viewport/assistive technology được hỗ trợ, when tương tác, then mọi chức năng chính dùng được.

