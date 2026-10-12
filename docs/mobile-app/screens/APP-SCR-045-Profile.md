# APP-SCR-045 — Tôi

| Thuộc tính | Giá trị |
|---|---|
| Screen ID | APP-SCR-045 |
| Module | APP-09 — Profile and Settings |
| Route | `/profile` |
| Phiên bản | 1.0 |
| Trạng thái | DRAFT — chi tiết hóa theo ảnh giao diện tham chiếu |

## 1. Tên và mục đích màn hình

- **Tên màn hình:** Tôi.
- **Mục đích:** Hiển thị hồ sơ tóm tắt, trạng thái gói sử dụng, lời nhắn cá nhân trong ngày và cung cấp một trung tâm điều hướng tới các chức năng tài khoản, cài đặt, bảo mật và pháp lý.
- **Actor chính:** Người dùng Guest hoặc người dùng đã đăng nhập.
- **Điểm vào:** Nhấn tab “Tôi”; nhấn avatar trên Home/Tarot/Cung Hoàng Đạo; quay lại từ màn cài đặt con; deep link hợp lệ.
- **Điểm ra:** Chỉnh sửa hồ sơ, Premium, cài đặt thông báo, lịch nhắc, quyền riêng tư, pháp lý, đăng xuất, xóa tài khoản, Profile chi tiết và các tab chính.

### Thành phần quan sát được từ ảnh

- Card hồ sơ có avatar, tên “Linh Đan”, cung Song Ngư, ngày sinh, nhãn năng lượng và huy hiệu nhỏ.
- Card gói sử dụng hiển thị “Gói Miễn Phí”, nhãn “Cơ bản”, số lượt Tarot và CTA “Nâng Cấp”.
- Banner “Lời Nhắn Vũ Trụ Hôm Nay”.
- Nhóm “Tài khoản & Hội viên”: Chỉnh sửa hồ sơ, Gói Premium.
- Nhóm “Cài đặt & Nhắc nhở”: Cài đặt thông báo, Lịch nhắc.
- Nhóm “Bảo mật & Pháp lý”: Quyền riêng tư, Giới thiệu & Pháp lý.
- Nhóm “Hành động”: Đăng xuất, Xóa tài khoản.
- Cuối màn có tên sản phẩm và phiên bản.
- Bottom navigation có Trang Chủ, Bói Tarot, Cung Đạo và Tôi.

> **Lưu ý:** Theo thiết kế này, APP-SCR-045 đồng thời là Profile tóm tắt và Settings Hub. APP-SCR-047 Account Management không cần là một màn trung gian riêng nếu toàn bộ các nhóm điều hướng đã nằm tại đây.

## 2. Chức năng tổng quan

- **Xem hồ sơ tóm tắt:** Hiển thị avatar, tên, cung, ngày sinh, trạng thái năng lượng và gói hiện tại.
- **Quản lý gói:** Hiển thị quyền lợi/lượt còn lại và mở luồng nâng cấp hoặc quản lý Premium.
- **Xem lời nhắn hôm nay:** Hiển thị một câu nhắn Vũ trụ ngắn và mở nội dung liên quan khi nhấn.
- **Quản lý hồ sơ:** Mở màn cập nhật tên, ngày sinh, giờ/nơi sinh và avatar.
- **Quản lý thông báo:** Bật/tắt thông báo và đặt lịch nhắc.
- **Quản lý quyền riêng tư:** Xem và thay đổi các lựa chọn dữ liệu cá nhân.
- **Xem pháp lý:** Mở điều khoản, chính sách quyền riêng tư và thông tin ứng dụng.
- **Quản lý phiên:** Đăng xuất bằng dialog xác nhận.
- **Xóa tài khoản:** Mở luồng nguy hiểm có cảnh báo và xác thực lại.
- **Điều hướng chính:** Chuyển giữa Trang Chủ, Bói Tarot, Cung Đạo và Tôi.

## 3. Đặc tả thành phần giao diện

| STT | Thành phần | Loại | Bắt buộc | Chỉnh sửa | Dùng để làm gì | Khi thao tác | Kết quả hiển thị hoặc điều hướng |
|---|---|---|---|---|---|---|---|
| 1 | Card hồ sơ | Card | Có | Không trực tiếp | Tổng hợp thông tin người dùng | Nhấn | Mở hồ sơ chi tiết/APP-SCR-033 hoặc APP-SCR-027; màn đích cần xác nhận |
| 2 | Avatar | Avatar/Button | Có | Qua Edit Profile | Nhận diện người dùng | Nhấn | Mở APP-SCR-046 tại phần thay ảnh |
| 3 | Huy hiệu cạnh avatar | Badge/Button | Không | Không | Hiển thị cấp bậc hoặc trạng thái | Nhấn | Mở bottom sheet giải thích; ý nghĩa cần xác nhận |
| 4 | Tên hiển thị | Text | Có | Qua Edit Profile | Hiển thị tên đang sử dụng | Nhấn | Mở APP-SCR-046 và focus trường tên |
| 5 | Cung cá nhân | Text/Badge | Có khi có ngày sinh | Không | Hiển thị cung Mặt Trời | Nhấn | Mở APP-SCR-027 Personal Zodiac |
| 6 | Ngày sinh | Text | Có | Qua Edit Profile | Hiển thị dữ liệu hồ sơ | Nhấn | Mở APP-SCR-046 và focus ngày sinh |
| 7 | Nhãn “Năng lượng” | Chip/Button | Có khi có dữ liệu | Không | Hiển thị trạng thái năng lượng cá nhân | Nhấn | Mở bottom sheet giải thích hoặc APP-SCR-034; cần xác nhận |
| 8 | Card gói sử dụng | Card | Có | Không | Hiển thị gói hiện tại và quyền lợi | Nhấn | Gói thường: APP-SCR-053; Premium: APP-SCR-056 |
| 9 | Tên gói | Text | Có | Không | Nhận biết Free/Premium | Không thao tác | Hiển thị trạng thái quyền hiện hành |
| 10 | Nhãn “Cơ bản/PRO” | Badge | Có | Không | Phân biệt cấp gói | Không thao tác | Không điều hướng |
| 11 | Số lượt Tarot | Text | Có | Không | Hiển thị lượt còn lại hoặc hạn mức | Không thao tác | Nội dung cập nhật theo kỳ; hạn mức cần xác nhận |
| 12 | CTA “Nâng Cấp” | Button | Có với gói thường | Không | Mở quyền lợi Premium | Nhấn | Mở APP-SCR-053 Premium Paywall |
| 13 | CTA quản lý gói | Button | Có với Premium | Không | Quản lý thuê bao | Nhấn | Mở APP-SCR-056 Manage Subscription |
| 14 | Banner “Lời Nhắn Vũ Trụ Hôm Nay” | Banner/Card | Có | Không | Hiển thị lời nhắn ngắn theo ngày | Nhấn | Mở APP-SCR-012 hoặc APP-SCR-026 tùy nguồn nội dung; cần xác nhận |
| 15 | “Chỉnh sửa hồ sơ” | Navigation row | Có | Không | Cập nhật ngày sinh, giờ sinh, avatar và tên | Nhấn | Mở APP-SCR-046 Edit Profile |
| 16 | “Gói Premium” | Navigation row | Có | Không | Xem quyền lợi hoặc quản lý gói | Nhấn | Chưa Premium: APP-SCR-053; đã Premium: APP-SCR-056 |
| 17 | “Cài đặt thông báo” | Navigation row | Có | Không | Quản lý các nhóm thông báo | Nhấn hàng | Mở APP-SCR-041 Notification Settings |
| 18 | Nút trạng thái thông báo | Switch/Button | Có | Có | Bật/tắt nhanh thông báo tổng | Nhấn | Cập nhật nếu đã có quyền; nếu quyền OS tắt thì mở hướng dẫn hệ điều hành |
| 19 | “Lịch nhắc” | Navigation row | Có | Không | Đặt giờ nhắc Tarot/năng lượng | Nhấn | Mở APP-SCR-042 Reminder Schedule |
| 20 | Tóm tắt lịch nhắc | Text | Có khi đã cấu hình | Không | Hiển thị giờ đang áp dụng | Không thao tác | Ví dụ: 08:00 và 21:30; nội dung theo cấu hình thật |
| 21 | “Quyền riêng tư” | Navigation row | Có | Không | Quản lý dữ liệu và lựa chọn riêng tư | Nhấn | Mở APP-SCR-048 Privacy Settings |
| 22 | “Giới thiệu & Pháp lý” | Navigation row | Có | Không | Xem điều khoản và chính sách | Nhấn | Mở APP-SCR-051 About and Legal |
| 23 | “Đăng xuất” | Action row | Theo điều kiện | Không | Kết thúc phiên tài khoản | Nhấn | Mở dialog APP-SCR-052 ngay trên màn Tôi |
| 24 | “Xóa tài khoản” | Destructive row | Theo điều kiện | Không | Mở luồng xóa tài khoản | Nhấn | Mở APP-SCR-050 Delete Account |
| 25 | Cảnh báo cạnh Xóa tài khoản | Icon | Có | Không | Thể hiện mức độ nguy hiểm | Không thao tác riêng | Không điều hướng |
| 26 | Tên sản phẩm | Text | Có | Không | Nhận diện ứng dụng | Không thao tác | Không điều hướng |
| 27 | Phiên bản ứng dụng | Text | Có | Không | Hỗ trợ nhận biết phiên bản | Nhấn nhiều lần nếu có chế độ ẩn | `Cần xác nhận`; mặc định không thao tác |
| 28 | Tab “Trang Chủ” | Bottom tab | Có | Không | Điều hướng về Home | Nhấn | Mở APP-SCR-011 Home |
| 29 | Tab “Bói Tarot” | Bottom tab | Có | Không | Điều hướng tới Tarot | Nhấn | Mở APP-SCR-016 Tarot Hub |
| 30 | Tab “Cung Đạo” | Bottom tab | Có | Không | Điều hướng tới Cung Hoàng Đạo | Nhấn | Mở APP-SCR-024; quyền Premium xử lý tại màn đích |
| 31 | Tab “Tôi” | Bottom tab | Có | Không | Xác định tab hiện tại | Nhấn lại | Cuộn lên đầu; không mở chồng màn |
| 32 | Pull-to-refresh | Gesture | Không | N/A | Làm mới hồ sơ, gói và lượt | Kéo xuống | Cập nhật các khối; không thay đổi cài đặt |

## 4. Use Case

### UC-ME-01 — Xem màn Tôi

| Trường | Nội dung |
|---|---|
| Use Case ID | UC-ME-01 |
| Name | Xem hồ sơ và cài đặt |
| Description | Hiển thị hồ sơ tóm tắt, gói sử dụng và các nhóm cài đặt |
| Actor | Guest hoặc người dùng đã đăng nhập |
| Preconditions | Đã hoàn tất onboarding và có phiên ứng dụng hợp lệ |
| Trigger | Nhấn tab “Tôi” hoặc avatar từ màn khác |
| Main Flow | 1. Hệ thống hiển thị cấu trúc và skeleton. 2. Hệ thống tải hồ sơ, gói, lượt và lịch nhắc. 3. Hệ thống hiển thị các hàng phù hợp với trạng thái tài khoản. 4. Người dùng chọn chức năng. |
| Alternative Flow | Guest không có thao tác đăng xuất tài khoản; có CTA tạo/đăng nhập tài khoản nếu cần. |
| Exception Rules | Lỗi hồ sơ hoặc gói hiển thị Retry theo khối; các hàng cài đặt cục bộ vẫn dùng được. |
| Postconditions | Người dùng xem được trạng thái hiện hành và các hành động hợp lệ. |

### UC-ME-02 — Chỉnh sửa hồ sơ

| Trường | Nội dung |
|---|---|
| Use Case ID | UC-ME-02 |
| Name | Mở chỉnh sửa hồ sơ |
| Description | Cập nhật thông tin dùng để cá nhân hóa |
| Actor | Người dùng |
| Preconditions | Màn Tôi đã hiển thị |
| Trigger | Nhấn “Chỉnh sửa hồ sơ”, avatar, tên hoặc ngày sinh |
| Main Flow | 1. Hệ thống mở APP-SCR-046 đúng section. 2. Người dùng chỉnh sửa và lưu. 3. Quay lại màn Tôi. 4. Hệ thống cập nhật card hồ sơ và các kết quả phụ thuộc. |
| Alternative Flow | Người dùng hủy chỉnh sửa; dữ liệu cũ được giữ nguyên. |
| Exception Rules | Nếu lưu lỗi, giữ dữ liệu nhập ở APP-SCR-046 và cho Retry. |
| Postconditions | Hồ sơ hiển thị dữ liệu mới sau khi lưu thành công. |

### UC-ME-03 — Nâng cấp hoặc quản lý Premium

| Trường | Nội dung |
|---|---|
| Use Case ID | UC-ME-03 |
| Name | Quản lý gói sử dụng |
| Description | Mở Paywall hoặc màn quản lý thuê bao theo trạng thái hiện tại |
| Actor | Người dùng |
| Preconditions | Trạng thái gói đã xác định |
| Trigger | Nhấn card gói, “Nâng Cấp” hoặc hàng “Gói Premium” |
| Main Flow | 1. Hệ thống kiểm tra entitlement. 2. Nếu chưa Premium, mở APP-SCR-053. 3. Nếu đã Premium, mở APP-SCR-056. 4. Khi quay lại, cập nhật trạng thái gói. |
| Alternative Flow | Trạng thái pending hiển thị rõ và dẫn APP-SCR-055/056 theo flow thanh toán. |
| Exception Rules | Không xác định được gói thì hiển thị Retry; không giả trạng thái Premium. |
| Postconditions | Người dùng được chuyển tới đúng màn quản lý gói. |

### UC-ME-04 — Đăng xuất

| Trường | Nội dung |
|---|---|
| Use Case ID | UC-ME-04 |
| Name | Kết thúc phiên tài khoản |
| Description | Đăng xuất sau xác nhận |
| Actor | Người dùng đã đăng nhập |
| Preconditions | Có phiên đăng nhập; hàng “Đăng xuất” hiển thị |
| Trigger | Nhấn “Đăng xuất” |
| Main Flow | 1. Hệ thống mở dialog APP-SCR-052. 2. Người dùng xác nhận. 3. Hệ thống khóa nút và kết thúc phiên. 4. Hệ thống mở APP-SCR-004. |
| Alternative Flow | Người dùng chọn “Hủy” hoặc đóng dialog; giữ nguyên màn Tôi. |
| Exception Rules | Đăng xuất lỗi thì đóng loading, hiển thị thông báo và cho thử lại; không xử lý hai lần. |
| Postconditions | Phiên đăng nhập kết thúc; tài khoản không bị xóa. |

### UC-ME-05 — Xóa tài khoản

| Trường | Nội dung |
|---|---|
| Use Case ID | UC-ME-05 |
| Name | Mở luồng xóa tài khoản |
| Description | Điều hướng tới quy trình xóa có cảnh báo |
| Actor | Người dùng có tài khoản |
| Preconditions | Có tài khoản máy chủ và đủ quyền thực hiện |
| Trigger | Nhấn “Xóa tài khoản” |
| Main Flow | 1. Hệ thống mở APP-SCR-050. 2. Hiển thị tác động và điều kiện. 3. Người dùng xác thực/xác nhận. 4. Hệ thống xử lý theo chính sách. |
| Alternative Flow | Guest thấy “Xóa dữ liệu trên thiết bị” nếu nghiệp vụ hỗ trợ; cần xác nhận. |
| Exception Rules | Không xóa trực tiếp từ hàng trên màn Tôi; mọi thao tác phải qua APP-SCR-050. |
| Postconditions | Chưa có dữ liệu bị xóa cho tới khi hoàn tất xác nhận ở màn con. |

## 5. Business Rules

### BR1. Hiển thị theo trạng thái tài khoản

- Guest không hiển thị email hoặc hành động đăng xuất tài khoản.
- Người dùng đăng nhập hiển thị “Đăng xuất”.
- “Xóa tài khoản” chỉ áp dụng khi có tài khoản máy chủ; trường hợp Guest cần nhãn riêng nếu cho phép xóa dữ liệu cục bộ.

### BR2. Hồ sơ tóm tắt

- Tên, avatar, cung và ngày sinh lấy từ hồ sơ hiện hành.
- Thiếu tên dùng “Bạn”; thiếu avatar dùng ảnh mặc định.
- Thiếu ngày sinh thì không suy đoán cung; hiển thị “Chưa xác định” và CTA chỉnh hồ sơ.

### BR3. Trạng thái gói

- Gói hiển thị phải khớp entitlement đã xác minh.
- Người dùng thường thấy “Gói Miễn Phí/Cơ bản” và CTA “Nâng Cấp”.
- Người dùng Premium thấy tên gói, ngày gia hạn/hết hạn nếu phù hợp và CTA quản lý.
- Không hiển thị Premium chỉ dựa trên cache quá hạn.

### BR4. Lượt Tarot

- Lượt còn lại hiển thị theo kỳ và quyền hiện hành.
- Premium có hạn mức cao hơn người dùng thường.
- Hạn mức và thời điểm reset là `Cần xác nhận`.

### BR5. Thông báo

- Nút bật/tắt nhanh phải phản ánh đồng thời lựa chọn trong ứng dụng và quyền hệ điều hành.
- Nếu quyền hệ điều hành bị tắt, không hiển thị trạng thái như đang hoạt động; phải cung cấp CTA mở cài đặt thiết bị.

### BR6. Lịch nhắc

- Dòng tóm tắt chỉ hiển thị lịch đang hoạt động.
- Thời gian phải dùng định dạng phù hợp ngôn ngữ thiết bị.
- Thay đổi lịch thực hiện tại APP-SCR-042, không chỉnh trực tiếp trên màn Tôi.

### BR7. Hành động nguy hiểm

- “Xóa tài khoản” đặt cuối và tách biệt bằng màu, icon và mô tả; không truyền đạt chỉ bằng màu.
- “Đăng xuất” không xóa tài khoản hoặc dữ liệu máy chủ.
- Chống nhấn lặp cho đăng xuất và xóa tài khoản.

### BR8. Phiên bản ứng dụng

- Phiên bản lấy từ bản build hiện hành.
- Không ghi cứng số phiên bản trong nội dung quản trị.

### BR9. Điều hướng

- Màn Tôi là Settings Hub; màn con quay lại đây và giữ vị trí cuộn.
- APP-SCR-047 được loại khỏi luồng nếu không có nhu cầu quản lý tài khoản riêng ngoài các nhóm đã hiển thị.

## 6. Validation

| Trường hoặc hành động | Điều kiện hợp lệ | Điều kiện không hợp lệ | Thông báo hiển thị |
|---|---|---|---|
| Hiển thị cung | Có ngày sinh hợp lệ | Thiếu hoặc ngày không hợp lệ | “Hãy bổ sung ngày sinh để xem cung của bạn.” |
| Mở Premium | Xác định được trạng thái gói | Không tải được entitlement | “Không thể kiểm tra gói hiện tại. Vui lòng thử lại.” |
| Bật thông báo | App và OS cho phép | Quyền OS bị từ chối | “Thông báo đang bị tắt trên thiết bị. Mở Cài đặt để cho phép.” |
| Mở lịch nhắc | Có quyền thông báo hoặc vẫn cho cấu hình trước | Không tải được cấu hình | “Không thể tải lịch nhắc. Vui lòng thử lại.” |
| Đăng xuất | Có phiên đăng nhập | Guest hoặc phiên đã hết | Ẩn hàng hoặc hiển thị “Phiên đăng nhập đã kết thúc.” |
| Xóa tài khoản | Có tài khoản và đã xác thực theo yêu cầu | Guest/không đủ quyền | “Không thể xóa tài khoản ở trạng thái hiện tại.” |
| Nhấn lặp | Chưa có thao tác đang xử lý | Đang loading | Không gửi thêm yêu cầu |

## 7. Trạng thái màn hình

| Trạng thái | Nội dung hiển thị | Thành phần được thao tác | Hành động tiếp theo |
|---|---|---|---|
| Loading lần đầu | Skeleton card hồ sơ/gói; các nhóm cài đặt ổn định | Bottom navigation | Chờ dữ liệu |
| Guest | Hồ sơ cục bộ, gói Free, CTA tài khoản nếu có; không có Đăng xuất tài khoản | Chỉnh hồ sơ, Premium, cài đặt | Tạo/đăng nhập tài khoản nếu muốn |
| Đã đăng nhập Free | Hồ sơ, gói Free, lượt còn lại và đầy đủ nhóm | Tất cả hành động phù hợp | Nâng cấp hoặc quản lý cài đặt |
| Premium | Gói Premium và CTA quản lý | Quản lý thuê bao | APP-SCR-056 |
| Thiếu hồ sơ | Giá trị có sẵn và nhắc bổ sung | Chỉnh hồ sơ | APP-SCR-046 |
| Lỗi một phần | Khối hồ sơ/gói lỗi có Retry; nhóm cài đặt khác vẫn dùng | Retry hoặc mở màn con | Tải lại riêng khối |
| Lỗi toàn màn | Bottom navigation, thông báo và Retry | Retry hoặc đổi tab | Tải lại màn Tôi |
| Offline | Banner offline; dữ liệu cache và cài đặt cục bộ | Xem cache; hạn chế thao tác cần mạng | Kết nối lại |
| Đang đăng xuất | Dialog có progress; nút bị khóa | Không | Chờ kết quả |

## 8. Thông báo

| Mã | Trường hợp | Nội dung thông báo | Kiểu hiển thị | Thời điểm đóng |
|---|---|---|---|---|
| ME-M01 | Lỗi hồ sơ/gói | “Không thể tải thông tin. Vui lòng thử lại.” | Inline + Retry | Khi tải thành công |
| ME-M02 | Quyền thông báo OS tắt | “Thông báo đang bị tắt trên thiết bị. Mở Cài đặt để cho phép.” | Banner/Dialog | Khi mở Settings hoặc đóng |
| ME-M03 | Đăng xuất thất bại | “Không thể đăng xuất. Vui lòng thử lại.” | Dialog/Inline | Khi Retry hoặc Hủy |
| ME-M04 | Mất mạng | “Bạn đang ngoại tuyến. Một số thay đổi cần kết nối mạng.” | Banner | Khi có mạng lại |
| ME-M05 | Thiếu ngày sinh | “Hãy bổ sung ngày sinh để xem cung của bạn.” | Inline | Khi hồ sơ đủ dữ liệu |
| ME-M06 | Cập nhật gói thành công | “Gói của bạn đã được cập nhật.” | Snackbar | Tự đóng theo thời gian chuẩn |

## 9. Hiệu ứng và phản hồi

- Hàng điều hướng và CTA có trạng thái nhấn rõ; toàn bộ hàng có thể nhấn, không chỉ chevron.
- Switch thông báo chuyển trạng thái sau khi quyền được xác nhận; lỗi thì trả về trạng thái trước.
- Dialog đăng xuất xuất hiện giữa màn với nền mờ; nút “Đăng xuất” chuyển loading khi xác nhận.
- Card Premium cập nhật trạng thái khi quay lại từ mua/khôi phục gói.
- Pull-to-refresh chỉ làm mới hồ sơ, entitlement, lượt và lịch; không thay đổi lựa chọn cài đặt.
- Khi Reduce Motion bật, dùng đổi opacity ngắn thay cho scale/slide trang trí.
- Lỗi một khối không làm các nhóm cài đặt khác dịch chuyển bất thường.

## 10. Điều hướng

| Hành động | Điều kiện | Màn hình hoặc trạng thái đích | Dữ liệu cần giữ |
|---|---|---|---|
| Nhấn card hồ sơ | Có hồ sơ | APP-SCR-033 hoặc APP-SCR-027; `Cần xác nhận` | Hồ sơ hiện hành |
| Nhấn avatar/tên/ngày sinh | Luôn khả dụng | APP-SCR-046 | Section tương ứng |
| Nhấn cung | Có ngày sinh | APP-SCR-027 | Cung hiện hành |
| Nhấn “Nâng Cấp” | Chưa Premium | APP-SCR-053 | Màn nguồn và quyền lợi hiện tại |
| Nhấn card gói | Premium | APP-SCR-056 | Entitlement hiện tại |
| Nhấn lời nhắn hôm nay | Có nội dung | APP-SCR-012 hoặc APP-SCR-026; `Cần xác nhận` | Ngày và nguồn nội dung |
| Nhấn “Cài đặt thông báo” | Luôn khả dụng | APP-SCR-041 | Không |
| Nhấn switch thông báo | Quyền OS phù hợp | Cập nhật tại chỗ | Trạng thái trước khi xử lý |
| Nhấn “Lịch nhắc” | Luôn khả dụng | APP-SCR-042 | Lịch hiện hành |
| Nhấn “Quyền riêng tư” | Luôn khả dụng | APP-SCR-048 | Không |
| Nhấn “Giới thiệu & Pháp lý” | Luôn khả dụng | APP-SCR-051 | Không |
| Nhấn “Đăng xuất” | Đã đăng nhập | Dialog APP-SCR-052 | Màn Tôi phía sau |
| Xác nhận đăng xuất | Phiên hợp lệ | APP-SCR-004 | Không |
| Nhấn “Xóa tài khoản” | Có tài khoản | APP-SCR-050 | Trạng thái tài khoản |
| Nhấn tab “Trang Chủ” | Luôn khả dụng | APP-SCR-011 | Không |
| Nhấn tab “Bói Tarot” | Luôn khả dụng | APP-SCR-016 | Không |
| Nhấn tab “Cung Đạo” | Luôn khả dụng | APP-SCR-024 | Không |
| Nhấn tab “Tôi” | Đang ở màn | Cuộn lên đầu | Không |

## 11. Tiêu chí nghiệm thu

- Khi người dùng mở tab “Tôi”, hệ thống hiển thị card hồ sơ, gói, lời nhắn, bốn nhóm chức năng, phiên bản và bottom navigation đúng thứ tự.
- Khi hồ sơ có tên, avatar, cung và ngày sinh, card hiển thị đúng dữ liệu hiện hành.
- Khi thiếu ngày sinh, hệ thống không suy đoán cung và hiển thị hướng dẫn bổ sung.
- Khi người dùng Free nhấn “Nâng Cấp”, hệ thống mở APP-SCR-053.
- Khi người dùng Premium nhấn card gói, hệ thống mở APP-SCR-056 và không hiển thị CTA mua sai trạng thái.
- Khi nhấn “Chỉnh sửa hồ sơ”, hệ thống mở APP-SCR-046; sau khi lưu và quay lại, card cập nhật dữ liệu mới.
- Khi quyền hệ điều hành tắt, switch thông báo không được hiển thị như đang hoạt động và cung cấp CTA mở Settings.
- Khi nhấn “Lịch nhắc”, hệ thống mở APP-SCR-042 với lịch hiện hành.
- Khi nhấn “Quyền riêng tư” hoặc “Giới thiệu & Pháp lý”, hệ thống mở đúng màn con; quay lại giữ vị trí cuộn.
- Khi nhấn “Đăng xuất”, hệ thống chỉ mở dialog APP-SCR-052; chưa xác nhận thì không kết thúc phiên.
- Khi xác nhận đăng xuất, hệ thống xử lý một lần và mở APP-SCR-004; không xóa tài khoản.
- Khi nhấn “Xóa tài khoản”, hệ thống mở APP-SCR-050; không xóa trực tiếp từ màn Tôi.
- Khi người dùng Guest, hàng “Đăng xuất” tài khoản bị ẩn hoặc thay bằng hành động phù hợp đã được duyệt.
- Khi một khối tải lỗi, các hàng cài đặt khác và bottom navigation vẫn hoạt động; khối lỗi có Retry riêng.
- Khi mất mạng, hệ thống giữ dữ liệu cache và thông báo rõ thao tác nào cần kết nối.
- Khi dùng screen reader, mỗi hàng được đọc bằng tên, mô tả, trạng thái và “nút” nếu có thể nhấn.
- Khi tăng cỡ chữ, hàng tăng chiều cao và không cắt mô tả hoặc chevron.

## Điểm cần xác nhận

1. Nhấn card hồ sơ mở APP-SCR-033 Hồ sơ khám phá bản thân hay APP-SCR-027 Hồ sơ cung cá nhân.
2. Ý nghĩa và màn giải thích của huy hiệu cạnh avatar.
3. “Năng lượng: Nước mộng mơ” là nhãn tĩnh, kết quả tính toán hay lối vào APP-SCR-034.
4. Lời Nhắn Vũ Trụ Hôm Nay mở APP-SCR-012 hay APP-SCR-026.
5. Hạn mức Tarot của gói Free/Premium và thời điểm reset.
6. Guest có được hiển thị “Xóa dữ liệu trên thiết bị” thay cho “Xóa tài khoản” hay không.
7. APP-SCR-047 Account Management có chính thức được loại khỏi luồng vì APP-SCR-045 đã là Settings Hub hay vẫn cần cho một số chức năng tài khoản nâng cao.
8. Phiên bản có hỗ trợ thao tác ẩn khi nhấn nhiều lần hay chỉ là text.
