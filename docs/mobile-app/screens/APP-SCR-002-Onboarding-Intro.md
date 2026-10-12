# APP-SCR-002 — Onboarding Intro

| Thuộc tính | Giá trị |
|---|---|
| Screen ID | APP-SCR-002 |
| Module | APP-01 |
| Route | `/onboarding` |
| Phiên bản | 0.1 |
| Trạng thái | DRAFT |

## Mục đích

Giới thiệu giá trị cốt lõi của Cosmic Diary.

## Entry Points

Splash/onboarding/settings.

## UI Components

- Header/navigation phù hợp ngữ cảnh.
- Vùng nội dung chính của **Onboarding Intro**.
- Trạng thái hành động chính và hành động phụ.
- Feedback inline, error và retry.

## Data Sources

Identity, Profile, Consent. Dữ liệu phải mang version khi phụ thuộc nội dung hoặc quy tắc nghiệp vụ.

## User Actions

Tiếp tục, quay lại, xác nhận, bỏ qua phần tùy chọn.

## Navigation

- Chỉ điều hướng sau khi validation và authorization thành công.
- Deep link phải kiểm tra session, consent và entitlement trước khi mở đích.
- Back phải giữ draft hợp lệ hoặc cảnh báo nếu dữ liệu chưa lưu.

## Validation

- Validation client dùng cho UX; server vẫn là nguồn quyết định.
- Không chấp nhận dữ liệu ngoài schema/version được hỗ trợ.
- Chống double submit; thao tác ghi quan trọng phải idempotent.

## UI States

| State | Yêu cầu |
|---|---|
| Loading | Skeleton/progress phù hợp; không khóa vô thời hạn |
| Empty | Giải thích rõ và cung cấp hành động tiếp theo |
| Error | Thông báo thân thiện, mã correlation khi cần hỗ trợ, có Retry an toàn |
| Offline | Dùng cache đúng hạn hoặc thông báo không khả dụng; không giả thành công |
| Success | Phản hồi rõ, cập nhật state và điều hướng nhất quán |

## Accessibility

- Hỗ trợ screen reader, focus order, font scaling và contrast.
- Không truyền đạt trạng thái chỉ bằng màu sắc.
- Tôn trọng Reduce Motion đối với animation.

## Analytics

Chỉ ghi screen view, hành động và kết quả kỹ thuật theo taxonomy. Không gửi ngày sinh thô, mood, diary note, câu hỏi Tarot, token hoặc dữ liệu nhận diện không cần thiết.

## Related Requirements & Flows

- Module: `APP-01`.
- Nguồn đặc tả: [Tài liệu liên quan](../01-APP-01-Authentication-and-Onboarding.md).
- Shared rules: [Decision Log](../../shared/16-Architecture-Decision-Log.md).

## Acceptance Baseline

- Given actor đủ quyền và dữ liệu hợp lệ, when thực hiện hành động chính, then hệ thống hoàn tất đúng nghiệp vụ và hiển thị Success state.
- Given dữ liệu không hợp lệ, when gửi, then hệ thống không ghi dữ liệu và hiển thị lỗi tại trường liên quan.
- Given request timeout/retry, when gửi lại, then không tạo giao dịch hoặc bản ghi trùng.
- Given actor không đủ quyền/entitlement, when truy cập, then hệ thống chặn an toàn và đưa ra hành động phù hợp.

