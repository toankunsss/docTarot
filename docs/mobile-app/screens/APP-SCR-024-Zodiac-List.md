# APP-SCR-024 — Cung Hoàng Đạo

| Thuộc tính | Giá trị |
|---|---|
| Screen ID | APP-SCR-024 |
| Module | APP-04 — Zodiac |
| Route | `/zodiac` |
| Phiên bản | 1.0 |
| Trạng thái | DRAFT — chi tiết hóa theo ảnh giao diện tham chiếu |

## 1. Tên và mục đích màn hình

- **Tên màn hình:** Cung Hoàng Đạo.
- **Mục đích:** Hiển thị tổng quan chiêm tinh cá nhân trong ngày, bao gồm cung của người dùng, hồ sơ Mặt Trời–Mặt Trăng–Cung Mọc, Tín hiệu Vũ trụ và các tiện ích chiêm tinh liên quan.
- **Actor chính:** Người dùng Guest hoặc người dùng đã đăng nhập; một số nội dung yêu cầu Premium.
- **Điểm vào:** Nhấn tab “Hoàng Đạo/Cung Sao”; lối tắt từ Home; deep link; quay lại từ màn chi tiết.
- **Điểm ra:** Hồ sơ cung cá nhân, Tín hiệu Vũ trụ, Độ tương hợp, So sánh đã lưu, Bản đồ sao, tìm kiếm cung, Profile và Paywall.

### Thành phần quan sát được từ ảnh

- Header có tiêu đề “Cung Hoàng Đạo”, tìm kiếm, thông tin và tài khoản.
- Khối “Năng lượng thiên thể” hiển thị lời chào ngắn và trạng thái Mặt Trăng “Trăng non”.
- Card cung cá nhân hiển thị Song Ngư, ngày 19/02–20/03, mức tương thích hôm nay 96%, nguyên tố, hành tinh bảo hộ, hình ảnh nội dung và CTA xem hồ sơ cá nhân.
- Card Premium “Tín hiệu Vũ trụ” hiển thị ngày, nội dung tổng quan và ba chỉ số Tình cảm, Công việc, Năng lượng.
- Khối “Lối tắt chiêm tinh” gồm Độ tương hợp, So sánh đã lưu và Hồ sơ của tôi.
- Bottom navigation có bốn tab: Trang Chủ, Bói Tarot, Hoàng Đạo và Tôi.

> **Lưu ý:** Thiết kế tham chiếu thể hiện một Zodiac Hub cá nhân hóa, không phải danh sách 12 cung. Screen ID được giữ nguyên để không làm đứt liên kết tài liệu; tên nghiệp vụ được cập nhật thành “Cung Hoàng Đạo”.

## 2. Chức năng tổng quan

- **Nhận biết ngữ cảnh chiêm tinh:** Hiển thị năng lượng thiên thể và pha Mặt Trăng hiện tại.
- **Xem cung cá nhân:** Hiển thị cung Mặt Trời, khoảng ngày, nguyên tố, hành tinh bảo hộ và mức tương thích trong ngày.
- **Mở hồ sơ cá nhân:** Điều hướng tới hồ sơ Mặt Trời, Mặt Trăng và Cung Mọc.
- **Xem Tín hiệu Vũ trụ:** Người dùng Premium xem phân tích theo ngày; người dùng thường xem teaser và CTA mở Premium.
- **Xem chỉ số trong ngày:** Hiển thị Tình cảm, Công việc và Năng lượng theo phần trăm.
- **Truy cập tiện ích:** Mở Độ tương hợp, kết quả so sánh đã lưu và Bản đồ sao/Hồ sơ chiêm tinh.
- **Tìm kiếm và khám phá:** Cho phép tìm một cung hoặc nội dung chiêm tinh nếu chức năng tìm kiếm được phê duyệt.
- **Điều hướng chính:** Chuyển giữa Trang Chủ, Bói Tarot, Hoàng Đạo và Tôi.

## 3. Đặc tả thành phần giao diện

| STT | Thành phần | Loại | Bắt buộc | Chỉnh sửa | Dùng để làm gì | Khi thao tác | Kết quả hiển thị hoặc điều hướng |
|---|---|---|---|---|---|---|---|
| 1 | Biểu tượng chiêm tinh | Icon | Có | Không | Nhận diện module | Không thao tác | Không điều hướng |
| 2 | Tiêu đề “Cung Hoàng Đạo” | Text | Có | Không | Xác định màn hiện tại | Không thao tác | Không điều hướng |
| 3 | Tìm kiếm | Icon Button | Không | Không | Tìm cung hoặc nội dung chiêm tinh | Nhấn | Mở search overlay/màn tìm kiếm; phạm vi cần xác nhận |
| 4 | Thông tin | Icon Button | Không | Không | Giải thích nội dung chiêm tinh và tính tham khảo | Nhấn | Mở bottom sheet thông tin thuộc APP-SCR-024 |
| 5 | Tài khoản | Avatar/Icon Button | Có | Theo hồ sơ | Truy cập hồ sơ cá nhân | Nhấn | Mở APP-SCR-045 Profile |
| 6 | Nhãn “Năng lượng thiên thể” | Label | Có | Không | Định danh phần mở đầu trong ngày | Không thao tác | Không điều hướng |
| 7 | Lời dẫn năng lượng | Text | Có | Không | Tóm tắt trạng thái chung | Không thao tác | Hiển thị nội dung theo ngày |
| 8 | Chip pha Mặt Trăng | Chip/Button | Có | Không | Hiển thị pha Mặt Trăng hiện tại | Nhấn | Mở bottom sheet giải thích pha Mặt Trăng; cần xác nhận |
| 9 | Card cung cá nhân | Card | Có | Không | Tổng hợp cung và dữ liệu chiêm tinh chính | Nhấn | Mở APP-SCR-027 Personal Zodiac |
| 10 | Biểu tượng cung | Icon | Có | Không | Nhận diện cung cá nhân | Không thao tác | Hiển thị đúng cung theo hồ sơ |
| 11 | Tên cung và khoảng ngày | Text | Có | Không | Hiển thị cung Mặt Trời | Không thao tác | Ví dụ: Song Ngư, 19/02–20/03 |
| 12 | Badge “Của bạn” | Badge | Có | Không | Đánh dấu đây là cung của người dùng | Không thao tác | Không điều hướng |
| 13 | Tương thích hôm nay | Indicator | Có | Không | Hiển thị điểm tương thích/năng lượng của ngày | Nhấn | Mở giải thích chỉ số; ý nghĩa “tương thích” cần xác nhận |
| 14 | Đoạn mô tả cung | Text | Có | Không | Tóm tắt tính cách/năng lượng trong ngày | Không thao tác | Tối đa số dòng theo thiết kế; nội dung tham khảo |
| 15 | Nguyên tố | Info card | Có | Không | Hiển thị nguyên tố của cung | Nhấn | Mở bottom sheet giải thích nguyên tố |
| 16 | Hành tinh bảo hộ | Info card | Có | Không | Hiển thị hành tinh chủ quản | Nhấn | Mở bottom sheet giải thích hành tinh |
| 17 | Banner hình ảnh trong card | Image/Card | Có | Không | Minh họa insight chiêm tinh | Nhấn | Mở nội dung chi tiết liên quan; màn đích cần xác nhận |
| 18 | CTA “Xem hồ sơ cá nhân” | Button | Có | Không | Xem Big Three | Nhấn | Mở APP-SCR-027 tại tổng quan Mặt Trời, Mặt Trăng, Cung Mọc |
| 19 | Card “Tín hiệu Vũ trụ” | Premium card | Có | Không | Hiển thị dự báo cá nhân theo ngày | Nhấn | Premium: mở APP-SCR-026; thường: mở APP-SCR-053 sau thao tác chủ động |
| 20 | Badge “Premium” | Badge | Có với nội dung khóa | Không | Thể hiện quyền truy cập | Không thao tác | Không tự mở Paywall |
| 21 | Ngày áp dụng | Text | Có | Không | Xác định ngày của tín hiệu | Không thao tác | Dùng ngày theo múi giờ người dùng |
| 22 | Nội dung tổng quan | Text | Có | Không | Tóm tắt Tín hiệu Vũ trụ | Không thao tác | Premium xem đầy đủ/teaser theo chính sách |
| 23 | Chỉ số “Tình cảm” | Progress row | Có | Không | Hiển thị tỷ lệ và mô tả tình cảm | Nhấn | Mở diễn giải chỉ số trong APP-SCR-026 hoặc bottom sheet; cần xác nhận |
| 24 | Chỉ số “Công việc” | Progress row | Có | Không | Hiển thị tỷ lệ và mô tả công việc | Nhấn | Giống hành vi chỉ số Tình cảm |
| 25 | Chỉ số “Năng lượng” | Progress row | Có | Không | Hiển thị tỷ lệ và mô tả năng lượng | Nhấn | Giống hành vi chỉ số Tình cảm |
| 26 | CTA “Xem tín hiệu hôm nay” | Button | Có | Không | Mở phân tích đầy đủ | Nhấn | Premium: APP-SCR-026; thường: APP-SCR-053 |
| 27 | “Độ tương hợp” | Shortcut row | Có | Không | Kiểm tra độ hòa hợp giữa hai cung | Nhấn | Mở APP-SCR-028 Compatibility Input |
| 28 | “So sánh đã lưu” | Shortcut row | Có | Không | Xem các kết quả tương hợp đã lưu | Nhấn | Mở APP-SCR-030 Saved Compatibility |
| 29 | “Hồ sơ của tôi” | Shortcut row | Có | Không | Khám phá Mặt Trời, Mặt Trăng, Cung Mọc | Nhấn | Mở APP-SCR-027; nếu ý nghĩa là Bản đồ sao thì cần đổi sang APP-SCR-058 |
| 30 | Câu trích dẫn cuối màn | Quote card | Không | Không | Tạo điểm kết thúc nhẹ nhàng | Không thao tác | Nội dung thay đổi theo cấu hình nếu có |
| 31 | Tab “Trang Chủ” | Bottom tab | Có | Không | Điều hướng về Home | Nhấn | Mở APP-SCR-011 |
| 32 | Tab “Bói Tarot” | Bottom tab | Có | Không | Điều hướng tới Tarot | Nhấn | Mở APP-SCR-016 |
| 33 | Tab “Hoàng Đạo” | Bottom tab | Có | Không | Xác định tab hiện tại | Nhấn lại | Cuộn lên đầu; không mở chồng màn |
| 34 | Tab “Tôi” | Bottom tab | Có | Không | Điều hướng tới Profile | Nhấn | Mở APP-SCR-045 |
| 35 | Pull-to-refresh | Gesture | Không | N/A | Làm mới dữ liệu theo ngày | Kéo xuống | Cập nhật pha trăng, chỉ số và nội dung; không đổi dữ liệu hồ sơ |

## 4. Use Case

### UC-ZODIAC-01 — Xem tổng quan Cung Hoàng Đạo

| Trường | Nội dung |
|---|---|
| Use Case ID | UC-ZODIAC-01 |
| Name | Xem tổng quan chiêm tinh cá nhân |
| Description | Hiển thị cung cá nhân, Tín hiệu Vũ trụ và các tiện ích liên quan |
| Actor | Người dùng |
| Preconditions | Có phiên ứng dụng hợp lệ; đã hoàn tất onboarding |
| Trigger | Nhấn tab “Hoàng Đạo” |
| Main Flow | 1. Hệ thống hiển thị cấu trúc và skeleton. 2. Hệ thống tải hồ sơ sinh, pha trăng và nội dung trong ngày. 3. Hệ thống hiển thị cung cá nhân và Tín hiệu Vũ trụ theo quyền. 4. Người dùng chọn nội dung cần xem. |
| Alternative Flow | Thiếu ngày sinh thì hiển thị CTA hoàn thiện hồ sơ thay cho kết quả cung cá nhân. |
| Exception Rules | Lỗi một khối không khóa các khối khác. Không hiển thị cung suy đoán khi thiếu dữ liệu. |
| Postconditions | Màn hiển thị dữ liệu mới nhất hoặc cache có thời điểm cập nhật. |

### UC-ZODIAC-02 — Xem hồ sơ cung cá nhân

| Trường | Nội dung |
|---|---|
| Use Case ID | UC-ZODIAC-02 |
| Name | Mở hồ sơ Mặt Trời, Mặt Trăng và Cung Mọc |
| Description | Xem diễn giải chiêm tinh cá nhân dựa trên hồ sơ sinh |
| Actor | Người dùng |
| Preconditions | Có ngày sinh; Mặt Trăng/Cung Mọc cần thêm dữ liệu theo quy tắc tính |
| Trigger | Nhấn card cung hoặc “Xem hồ sơ cá nhân” |
| Main Flow | 1. Hệ thống kiểm tra dữ liệu sinh. 2. Nếu đủ, mở APP-SCR-027. 3. Màn đích hiển thị các kết quả có căn cứ. |
| Alternative Flow | Chỉ đủ ngày sinh thì vẫn hiển thị Mặt Trời và đánh dấu các mục khác “Chưa xác định”. |
| Exception Rules | Thiếu dữ liệu không được tự suy đoán; hiển thị CTA mở APP-SCR-046. |
| Postconditions | Người dùng xem được hồ sơ đúng với dữ liệu sinh hiện hành. |

### UC-ZODIAC-03 — Xem Tín hiệu Vũ trụ

| Trường | Nội dung |
|---|---|
| Use Case ID | UC-ZODIAC-03 |
| Name | Xem tín hiệu chiêm tinh trong ngày |
| Description | Mở phân tích đầy đủ theo Tình cảm, Công việc và Năng lượng |
| Actor | Người dùng |
| Preconditions | Card đã tải; trạng thái Premium đã xác định |
| Trigger | Nhấn card hoặc “Xem tín hiệu hôm nay” |
| Main Flow | 1. Hệ thống kiểm tra quyền. 2. Người dùng Premium được mở APP-SCR-026 đúng ngày và cung. 3. Nội dung chi tiết hiển thị ba nhóm phân tích. |
| Alternative Flow | Người dùng thường xem teaser và chọn CTA Premium để mở APP-SCR-053. |
| Exception Rules | Không xác định được quyền thì hiển thị Retry; không mở nội dung khóa hoặc Paywall tự động. |
| Postconditions | Người dùng xem nội dung được phép hoặc hiểu rõ cách mở khóa. |

### UC-ZODIAC-04 — Mở tiện ích chiêm tinh

| Trường | Nội dung |
|---|---|
| Use Case ID | UC-ZODIAC-04 |
| Name | Điều hướng bằng lối tắt chiêm tinh |
| Description | Mở Độ tương hợp, So sánh đã lưu hoặc Hồ sơ cá nhân |
| Actor | Người dùng |
| Preconditions | Danh sách lối tắt hiển thị |
| Trigger | Nhấn một hàng lối tắt |
| Main Flow | 1. Hệ thống nhận diện mục được chọn. 2. Kiểm tra dữ liệu/quyền cần thiết. 3. Mở đúng màn đích. |
| Alternative Flow | Nếu chưa có kết quả so sánh đã lưu, APP-SCR-030 hiển thị empty state và CTA tạo so sánh mới. |
| Exception Rules | Màn đích lỗi tải thì giữ nguồn điều hướng và cho Retry. |
| Postconditions | Màn đích mở đúng ngữ cảnh; quay lại giữ vị trí cuộn. |

### UC-ZODIAC-05 — Xem giải thích pha Mặt Trăng

| Trường | Nội dung |
|---|---|
| Use Case ID | UC-ZODIAC-05 |
| Name | Xem ý nghĩa pha Mặt Trăng |
| Description | Giải thích trạng thái pha trăng đang hiển thị |
| Actor | Người dùng |
| Preconditions | Có dữ liệu pha Mặt Trăng |
| Trigger | Nhấn chip “Trăng non” hoặc pha tương ứng |
| Main Flow | 1. Hệ thống mở bottom sheet. 2. Hiển thị tên pha trăng, khoảng thời gian và ý nghĩa tham khảo. 3. Người dùng đóng sheet để trở về màn. |
| Alternative Flow | Không có. |
| Exception Rules | Không tải được nội dung giải thích thì hiển thị Retry trong sheet. |
| Postconditions | Không làm thay đổi dữ liệu màn. |

## 5. Business Rules

### BR1. Xác định cung cá nhân

- Cung Mặt Trời cần ngày sinh hợp lệ.
- Mặt Trăng và Cung Mọc chỉ hiển thị khi đủ dữ liệu theo quy tắc tính đã duyệt.
- Thiếu dữ liệu phải hiển thị “Chưa xác định”; không suy đoán.

### BR2. Dữ liệu theo ngày

- Pha Mặt Trăng, Tín hiệu Vũ trụ và các chỉ số dùng ngày theo múi giờ người dùng.
- Khi qua ngày mới, nội dung cập nhật; dữ liệu hồ sơ sinh không thay đổi.

### BR3. Premium

- Tín hiệu Vũ trụ đầy đủ là quyền lợi Premium.
- Người dùng thường có thể xem teaser và badge Premium.
- Paywall chỉ mở sau khi người dùng chủ động nhấn card/CTA bị khóa.
- Đóng Paywall quay lại đúng vị trí trên APP-SCR-024.

### BR4. Chỉ số phần trăm

- Giá trị nằm từ 0% đến 100%.
- Thanh tiến độ, con số và nhãn chữ phải thống nhất.
- Phần trăm không được trình bày như xác suất chắc chắn xảy ra sự kiện.

### BR5. Nội dung tham khảo

- Không dùng ngôn ngữ khẳng định y tế, tài chính, pháp lý hoặc định mệnh.
- Nội dung phải hướng tới tự phản chiếu và gợi ý tích cực.

### BR6. Lỗi độc lập theo khối

- Lỗi card cung, Tín hiệu Vũ trụ hoặc lối tắt không làm hỏng toàn màn.
- Khối lỗi có Retry riêng và không xóa cache còn hợp lệ.

### BR7. Giữ ngữ cảnh

- Khi quay lại từ màn con, giữ vị trí cuộn.
- Nhấn lại tab “Hoàng Đạo” cuộn lên đầu.

### BR8. Lối tắt

- Thứ tự mặc định theo ảnh: Độ tương hợp, So sánh đã lưu, Hồ sơ của tôi.
- Hàng lối tắt có thể nhấn toàn vùng, không chỉ nút mũi tên.

## 6. Validation

| Trường hoặc hành động | Điều kiện hợp lệ | Điều kiện không hợp lệ | Thông báo hiển thị |
|---|---|---|---|
| Hiển thị cung cá nhân | Có ngày sinh hợp lệ | Thiếu hoặc ngày không hợp lệ | “Hãy bổ sung ngày sinh để xem cung của bạn.” |
| Mở Big Three | Có dữ liệu cần thiết | Thiếu giờ hoặc nơi sinh | “Hãy bổ sung giờ và nơi sinh để xem Mặt Trăng và Cung Mọc chính xác.” |
| Mở Tín hiệu Vũ trụ | Premium còn hiệu lực | Không có/hết hạn | Hiển thị teaser và CTA “Khám phá Premium” |
| Hiển thị chỉ số | Giá trị từ 0–100 | Ngoài khoảng hoặc thiếu | Ẩn giá trị lỗi và hiển thị “Chưa có dữ liệu hôm nay.” |
| Mở so sánh đã lưu | Có phiên và quyền xem dữ liệu | Không có dữ liệu | Empty state “Bạn chưa lưu kết quả tương hợp nào.” |
| Làm mới | Có mạng hoặc cache hợp lệ | Mất mạng và không có cache | “Không thể cập nhật dữ liệu. Vui lòng kiểm tra kết nối.” |

## 7. Trạng thái màn hình

| Trạng thái | Nội dung hiển thị | Thành phần được thao tác | Hành động tiếp theo |
|---|---|---|---|
| Loading lần đầu | Header, bottom navigation và skeleton card | Đổi tab; mở Profile nếu phiên sẵn sàng | Chờ từng khối tải |
| Có dữ liệu Premium | Đầy đủ cung cá nhân, tín hiệu và chỉ số | Tất cả hành động hợp lệ | Xem chi tiết hoặc mở tiện ích |
| Người dùng thường | Card tín hiệu có teaser, badge và CTA khóa | Mở Premium hoặc dùng tiện ích miễn phí | APP-SCR-053 khi chủ động nhấn |
| Thiếu ngày sinh | Card cung thay bằng hướng dẫn | Hoàn thiện hồ sơ | APP-SCR-046 |
| Thiếu giờ/nơi sinh | Mặt Trời hiển thị; Mặt Trăng/Cung Mọc chưa xác định | Bổ sung hồ sơ | APP-SCR-046 |
| Chưa có so sánh đã lưu | Empty state tại APP-SCR-030 | Tạo so sánh mới | APP-SCR-028 |
| Lỗi một phần | Khối lỗi có Retry; khối khác giữ dữ liệu | Retry hoặc dùng khối khác | Tải lại riêng khối |
| Lỗi toàn màn | Header, bottom navigation, thông báo và Retry | Retry hoặc đổi tab | Tải lại APP-SCR-024 |
| Offline có cache | Banner offline, cache và thời điểm cập nhật | Xem cache; hạn chế thao tác cần mạng | Kết nối lại |

## 8. Thông báo

| Mã | Trường hợp | Nội dung thông báo | Kiểu hiển thị | Thời điểm đóng |
|---|---|---|---|---|
| ZOD-M01 | Thiếu ngày sinh | “Hãy bổ sung ngày sinh để xem cung của bạn.” | Inline trong card | Khi hồ sơ đủ dữ liệu |
| ZOD-M02 | Thiếu giờ/nơi sinh | “Hãy bổ sung giờ và nơi sinh để xem Mặt Trăng và Cung Mọc chính xác.” | Bottom sheet | Khi đóng hoặc chọn CTA |
| ZOD-M03 | Lỗi một khối | “Không thể tải nội dung. Vui lòng thử lại.” | Inline + Retry | Khi Retry thành công |
| ZOD-M04 | Mất mạng | “Bạn đang ngoại tuyến. Nội dung có thể chưa được cập nhật.” | Banner | Khi có mạng lại |
| ZOD-M05 | Không có dữ liệu chỉ số | “Chưa có dữ liệu hôm nay.” | Inline | Khi dữ liệu có sẵn |
| ZOD-M06 | Chưa có so sánh | “Bạn chưa lưu kết quả tương hợp nào.” | Empty state | Khi tạo/lưu kết quả đầu tiên |

## 9. Hiệu ứng và phản hồi

- Card và hàng lối tắt có trạng thái nhấn rõ; không làm bố cục nhảy.
- Thanh phần trăm chuyển từ 0 tới giá trị khi dữ liệu tải xong; Reduce Motion hiển thị giá trị tức thời.
- Bottom sheet thông tin hoặc pha trăng trượt từ dưới lên, nền sau tối nhẹ.
- CTA Premium hiển thị trạng thái loading khi kiểm tra quyền; chống nhấn lặp.
- Pull-to-refresh hiển thị indicator ở đầu màn và không thay đổi dữ liệu hồ sơ sinh.
- Lỗi một khối chỉ thay nội dung của khối đó; các khu vực khác giữ nguyên vị trí.
- Chuyển màn dùng animation điều hướng chuẩn của ứng dụng.

## 10. Điều hướng

| Hành động | Điều kiện | Màn hình hoặc trạng thái đích | Dữ liệu cần giữ |
|---|---|---|---|
| Nhấn avatar | Luôn khả dụng | APP-SCR-045 Profile | Vị trí cuộn |
| Nhấn tìm kiếm | Tính năng được phê duyệt | Search overlay/màn tìm kiếm; `Cần xác nhận` | Từ khóa nếu có |
| Nhấn thông tin | Luôn khả dụng | Bottom sheet thông tin | Không |
| Nhấn pha Mặt Trăng | Có dữ liệu | Bottom sheet giải thích | Pha trăng và ngày |
| Nhấn card cung | Có ngày sinh | APP-SCR-027 Personal Zodiac | Hồ sơ hiện hành |
| Nhấn card cung | Thiếu ngày sinh | APP-SCR-046 Edit Profile | Trường còn thiếu |
| Nhấn “Xem hồ sơ cá nhân” | Đủ hoặc có một phần dữ liệu | APP-SCR-027 | Big Three hiện hành |
| Nhấn “Xem tín hiệu hôm nay” | Premium | APP-SCR-026 Horoscope Detail | Cung và ngày hiện tại |
| Nhấn “Xem tín hiệu hôm nay” | Không Premium | APP-SCR-053 Premium Paywall | Màn nguồn và quyền lợi Tín hiệu Vũ trụ |
| Nhấn “Độ tương hợp” | Luôn khả dụng | APP-SCR-028 | Cung người dùng nếu có |
| Nhấn “So sánh đã lưu” | Có phiên phù hợp | APP-SCR-030 | Không |
| Nhấn “Hồ sơ của tôi” | Theo nội dung hiện tại | APP-SCR-027 hoặc APP-SCR-058; `Cần xác nhận` | Hồ sơ sinh |
| Nhấn tab “Trang Chủ” | Luôn khả dụng | APP-SCR-011 | Không |
| Nhấn tab “Bói Tarot” | Luôn khả dụng | APP-SCR-016 | Không |
| Nhấn tab “Hoàng Đạo” | Đang ở màn | Cuộn lên đầu | Không |
| Nhấn tab “Tôi” | Luôn khả dụng | APP-SCR-045 | Không |

## 11. Tiêu chí nghiệm thu

- Khi người dùng mở màn, hệ thống hiển thị header, năng lượng thiên thể, card cung cá nhân, Tín hiệu Vũ trụ, lối tắt và bottom navigation đúng thứ tự.
- Khi hồ sơ có ngày sinh hợp lệ, card hiển thị đúng cung, biểu tượng và khoảng ngày.
- Khi thiếu ngày sinh, hệ thống không suy đoán cung và hiển thị CTA hoàn thiện hồ sơ.
- Khi thiếu giờ hoặc nơi sinh, hệ thống vẫn cho xem Mặt Trời nhưng đánh dấu Mặt Trăng/Cung Mọc “Chưa xác định”.
- Khi người dùng nhấn “Xem hồ sơ cá nhân”, hệ thống mở APP-SCR-027 với đúng hồ sơ.
- Khi Premium nhấn “Xem tín hiệu hôm nay”, hệ thống mở APP-SCR-026 đúng cung và ngày.
- Khi người dùng thường nhấn nội dung Premium, hệ thống hiển thị quyền lợi và chỉ mở APP-SCR-053 sau thao tác chủ động.
- Khi hiển thị chỉ số, phần trăm, thanh tiến độ và nội dung mô tả phải thống nhất.
- Khi nhấn “Độ tương hợp”, “So sánh đã lưu” hoặc “Hồ sơ của tôi”, toàn bộ hàng có tác dụng và mở đúng màn đích.
- Khi nhấn lại tab “Hoàng Đạo”, màn cuộn lên đầu và không mở thêm một instance.
- Khi một khối lỗi, các khối khác và bottom navigation vẫn thao tác được; khối lỗi có Retry riêng.
- Khi mất mạng và có cache, hệ thống hiển thị dữ liệu gần nhất kèm banner offline; không giả dữ liệu mới.
- Khi dùng screen reader, chỉ số được đọc cả tên, mô tả và phần trăm; icon không có nhãn mơ hồ.
- Khi tăng cỡ chữ, card tăng chiều cao và không cắt tên cung, mô tả hoặc CTA.
- Khi Reduce Motion bật, thanh chỉ số hiển thị trực tiếp và bottom sheet dùng hiệu ứng mờ ngắn.

## Điểm cần xác nhận

1. APP-SCR-024 giữ tên “Zodiac List” hay chính thức đổi thành “Zodiac Hub/Cung Hoàng Đạo”.
2. Icon tìm kiếm tìm trong 12 cung, bài viết chiêm tinh hay toàn bộ module.
3. Ý nghĩa chính xác của chỉ số “Tương thích hôm nay 96%”.
4. Nhấn banner hình ảnh trong card cung mở nội dung nào.
5. Nhấn từng chỉ số Tình cảm, Công việc, Năng lượng mở bottom sheet hay APP-SCR-026.
6. “Hồ sơ của tôi” mở APP-SCR-027 Personal Zodiac hay APP-SCR-058 Birth Chart.
7. Pha Mặt Trăng có bottom sheet giải thích hay chỉ là thông tin tĩnh.
8. Nội dung nào được xem miễn phí trong Tín hiệu Vũ trụ và độ dài teaser cho người dùng thường.
