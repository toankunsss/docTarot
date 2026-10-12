# APP-SCR-011 — Home

| Thuộc tính | Giá trị |
|---|---|
| Screen ID | APP-SCR-011 |
| Module | APP-02 — Home and Daily Cosmic Insight |
| Route | `/home` |
| Phiên bản | 1.0 |
| Trạng thái | DRAFT — chi tiết hóa theo ảnh giao diện tham chiếu |

## 1. Tên và mục đích màn hình

- **Tên màn hình:** Trang Chủ.
- **Mục đích:** Cung cấp tổng quan cá nhân hóa trong ngày, cho phép người dùng điểm danh cảm xúc, xem hoặc rút lá bài Tarot hôm nay, theo dõi các chỉ số và truy cập nhanh các chức năng khám phá bản thân.
- **Actor chính:** Người dùng Guest hoặc người dùng đã đăng nhập.
- **Điểm vào:** Sau khi hoàn tất onboarding; nhấn tab “Trang Chủ”; mở ứng dụng khi đã có phiên; quay lại từ màn con; deep link hợp lệ.
- **Điểm ra:** Điểm danh cảm xúc, Tarot hôm nay, chi tiết chỉ số, Bói bài, Trực giác, Bản đồ sao, Hợp đôi, Cung Sao và Profile.

### Thành phần quan sát được từ ảnh

- Header có logo Aura Luna, số dư Sao và avatar.
- Có nhãn ngày “Hôm nay” và một chip hành động ở phía phải.
- Lời chào cá nhân hóa hiển thị tên người dùng.
- Card “Điểm Danh Cảm Xúc” có bốn lựa chọn cảm xúc, một lựa chọn đang được chọn và CTA.
- Card Tarot hôm nay có ảnh lá bài, tên lá, thông điệp và CTA rút bài.
- Khối “Chỉ Số Hôm Nay” có bốn chỉ số phần trăm.
- Khối “Lối Tắt Nhanh” có Bói Bài, Trực Giác, Bản Đồ Sao và Hợp Đôi.
- Bottom navigation có Trang Chủ, Bài Tarot, Cung Sao và Tôi.

> **Lưu ý:** Một số nhãn nhỏ trong ảnh chưa đủ rõ để xác định tuyệt đối. Các nội dung này được đánh dấu `Cần xác nhận`, không được coi là yêu cầu đã chốt.

## 2. Chức năng tổng quan

- **Thông tin tài khoản:** Hiển thị số dư Sao và avatar của người dùng hiện tại. Nhấn avatar mở Profile.
- **Lời chào cá nhân hóa:** Hiển thị lời chào theo thời điểm và tên; nếu thiếu tên thì dùng “Chào bạn”.
- **Điểm danh cảm xúc:** Cho phép chọn nhanh một mood và chuyển sang màn ghi nhận chi tiết.
- **Tarot hôm nay:** Hiển thị trạng thái chưa rút hoặc đã rút, lá bài đại diện và thông điệp trong ngày.
- **Chỉ số hôm nay:** Hiển thị bốn chỉ số theo phần trăm và cho phép xem giải thích chi tiết.
- **Lối tắt nhanh:** Điều hướng tới Bói bài, Trực giác, Bản đồ sao và Hợp đôi.
- **Điều hướng chính:** Chuyển giữa Trang Chủ, Bài Tarot, Cung Sao và Tôi.
- **Làm mới:** Kéo xuống để cập nhật dữ liệu Home mà không tạo lại kết quả Tarot hoặc ghi trùng check-in.

## 3. Đặc tả thành phần giao diện

| STT | Thành phần | Loại | Bắt buộc | Chỉnh sửa | Dùng để làm gì | Khi thao tác | Kết quả hiển thị hoặc điều hướng |
|---|---|---|---|---|---|---|---|
| 1 | Logo “Aura Luna” | Logo/Button | Có | Không | Nhận diện thương hiệu | Nhấn | Cuộn Home lên đầu; không mở chồng màn Home |
| 2 | Số dư Sao | Badge/Button | Có | Không | Hiển thị số Sao hiện có | Nhấn | Mở bottom sheet giải thích số dư và cách sử dụng; nội dung cần xác nhận |
| 3 | Avatar | Avatar/Button | Có | Theo hồ sơ | Nhận biết tài khoản đang dùng | Nhấn | Mở APP-SCR-045 Profile |
| 4 | Nhãn “Hôm nay” | Label | Có | Không | Xác định phạm vi thời gian của dữ liệu | Không thao tác | Hiển thị ngày hiện tại theo múi giờ người dùng |
| 5 | Chip phía phải đầu màn | Chip/Button | Không | Không | Hành động nhanh xuất hiện trong ảnh | Nhấn | `Cần xác nhận` tên, mục đích và màn đích |
| 6 | Lời chào và tên | Text | Có | Không trực tiếp | Cá nhân hóa Home | Không thao tác | Hiển thị theo thời điểm và tên; thiếu tên dùng “Chào bạn” |
| 7 | Card “Điểm Danh Cảm Xúc” | Card | Có | Có | Ghi nhận trạng thái cảm xúc hôm nay | Nhấn card | Mở APP-SCR-014 Daily Check-in |
| 8 | Bốn lựa chọn cảm xúc | Selectable item | Có | Có | Chọn nhanh mood hiện tại | Nhấn một mood | Chuyển trạng thái chọn; chỉ một mood được chọn tại một thời điểm |
| 9 | CTA của Điểm Danh Cảm Xúc | Button | Có | Không | Chuyển sang ghi nhận chi tiết | Nhấn | Có mood: mở APP-SCR-014 và điền sẵn; chưa có mood: hiển thị lỗi inline |
| 10 | Card Tarot hôm nay | Card | Có | Không | Hiển thị trải nghiệm lá bài trong ngày | Nhấn | Chưa rút: mở APP-SCR-013 chờ lật; đã rút: mở đúng kết quả đã lưu |
| 11 | Ảnh lá bài | Image/Button | Có | Không | Đại diện trực quan cho lá bài | Nhấn | Giống hành vi của card Tarot hôm nay |
| 12 | Tên lá và thông điệp | Text | Có khi đã rút | Không | Tóm tắt Tarot trong ngày | Không thao tác | Chỉ hiển thị sau khi có kết quả hợp lệ |
| 13 | CTA “Rút bài hôm nay” | Button | Có khi chưa rút | Không | Bắt đầu trải nghiệm lá bài hôm nay | Nhấn | Mở APP-SCR-013; khóa nút trong khi xử lý |
| 14 | CTA “Xem lại” | Button | Có khi đã rút | Không | Xem lại kết quả trong ngày | Nhấn | Mở APP-SCR-013 đúng kết quả; không cấp lá mới |
| 15 | Khối “Chỉ Số Hôm Nay” | Section | Có | Không | Tổng hợp nhanh các chỉ số | Không thao tác | Hiển thị bốn chỉ số và phần trăm tương ứng |
| 16 | Từng chỉ số | Row/Card | Có | Không | Hiển thị tên, icon và tỷ lệ | Nhấn | Mở bottom sheet giải thích thuộc Home hoặc APP-SCR-012; `Cần xác nhận` |
| 17 | “Xem tất cả” tại Chỉ Số | Text Button | Không | Không | Xem nội dung đầy đủ | Nhấn | Mở APP-SCR-012 Daily Insight Detail |
| 18 | “Bói Bài” | Shortcut | Có | Không | Mở trung tâm Tarot | Nhấn | Mở APP-SCR-016 Tarot Hub |
| 19 | “Trực Giác” | Shortcut | Có | Không | Mở tính năng Trực giác | Nhấn | `Cần xác nhận` Screen ID và nghiệp vụ; chưa có màn đích trong danh mục hiện tại |
| 20 | “Bản Đồ Sao” | Shortcut | Có | Không | Xem bản đồ sao cá nhân | Nhấn | Đủ dữ liệu: mở APP-SCR-058 Birth Chart; thiếu dữ liệu: hiển thị hướng dẫn bổ sung |
| 21 | “Hợp Đôi” | Shortcut | Có | Không | Kiểm tra độ tương hợp | Nhấn | Mở APP-SCR-028 Compatibility Input |
| 22 | Tab “Trang Chủ” | Bottom tab | Có | Không | Điều hướng về Home | Nhấn khi đang chọn | Cuộn lên đầu; không tải lại ngoài ý muốn |
| 23 | Tab “Bài Tarot” | Bottom tab | Có | Không | Điều hướng tới Tarot | Nhấn | Mở APP-SCR-016 Tarot Hub |
| 24 | Tab “Cung Sao” | Bottom tab | Có | Không | Điều hướng tới Zodiac | Nhấn | Premium: mở APP-SCR-024; thường: mở APP-SCR-053 sau khi chủ động nhấn |
| 25 | Tab “Tôi” | Bottom tab | Có | Không | Điều hướng tới hồ sơ | Nhấn | Mở APP-SCR-045 Profile |
| 26 | Pull-to-refresh | Gesture | Không | N/A | Làm mới dữ liệu Home | Kéo xuống | Hiển thị progress và cập nhật từng khối; không tạo lại kết quả đã có |

## 4. Use Case

### UC-HOME-01 — Xem tổng quan trong ngày

| Trường | Nội dung |
|---|---|
| Use Case ID | UC-HOME-01 |
| Name | Xem tổng quan Home |
| Description | Hiển thị dữ liệu cá nhân hóa và các hành động chính của ngày |
| Actor | Guest hoặc người dùng đã đăng nhập |
| Preconditions | Đã hoàn tất onboarding và có phiên ứng dụng hợp lệ |
| Trigger | Mở ứng dụng hoặc nhấn tab “Trang Chủ” |
| Main Flow | 1. Hệ thống hiển thị cấu trúc Home và skeleton theo khối. 2. Hệ thống tải hồ sơ, mood, Tarot và chỉ số hôm nay. 3. Từng khối thay skeleton bằng dữ liệu tương ứng. 4. Người dùng cuộn và chọn chức năng cần dùng. |
| Alternative Flow | Thiếu tên thì hiển thị “Chào bạn”. Thiếu dữ liệu cá nhân hóa thì hiển thị CTA hoàn thiện hồ sơ. |
| Exception Rules | Lỗi một khối không khóa các khối khác. Lỗi toàn màn vẫn cho phép đổi tab và Retry. |
| Postconditions | Home hiển thị dữ liệu mới nhất hoặc dữ liệu cache có thời điểm cập nhật. |

### UC-HOME-02 — Điểm danh cảm xúc nhanh

| Trường | Nội dung |
|---|---|
| Use Case ID | UC-HOME-02 |
| Name | Chọn cảm xúc từ Home |
| Description | Chọn mood và chuyển sang luồng ghi nhận chi tiết |
| Actor | Người dùng |
| Preconditions | Khối Điểm Danh Cảm Xúc tải thành công |
| Trigger | Nhấn một biểu tượng cảm xúc |
| Main Flow | 1. Hệ thống đánh dấu mood được chọn. 2. Người dùng nhấn CTA. 3. Hệ thống mở APP-SCR-014 với mood đã điền sẵn. 4. Sau khi lưu, người dùng quay về Home và card hiển thị trạng thái hoàn tất. |
| Alternative Flow | Nhấn toàn bộ card trước khi chọn mood thì APP-SCR-014 mở mà chưa điền sẵn. |
| Exception Rules | Nhấn CTA khi chưa chọn mood thì không điều hướng và hiển thị “Vui lòng chọn cảm xúc của bạn.” |
| Postconditions | Mood chỉ được ghi chính thức sau khi lưu thành công tại APP-SCR-014. |

### UC-HOME-03 — Rút hoặc xem lại lá bài hôm nay

| Trường | Nội dung |
|---|---|
| Use Case ID | UC-HOME-03 |
| Name | Sử dụng Tarot hôm nay |
| Description | Rút lá bài lần đầu hoặc xem lại kết quả của ngày |
| Actor | Người dùng |
| Preconditions | Card Tarot hôm nay tải thành công |
| Trigger | Nhấn card hoặc CTA Tarot |
| Main Flow | 1. Hệ thống kiểm tra trạng thái của ngày. 2. Nếu chưa có kết quả, mở APP-SCR-013 ở trạng thái chờ lật. 3. Nếu đã có kết quả, mở đúng lá đã lưu. 4. Khi quay về, Home cập nhật ảnh, tên lá và thông điệp. |
| Alternative Flow | Nếu hết lượt, hiển thị giải thích và CTA Premium theo chính sách đã duyệt. |
| Exception Rules | Retry hoặc nhấn liên tục không được cấp nhiều lá cho cùng một lần xử lý. |
| Postconditions | Home phản ánh đúng trạng thái Tarot của ngày. |

### UC-HOME-04 — Mở lối tắt nhanh

| Trường | Nội dung |
|---|---|
| Use Case ID | UC-HOME-04 |
| Name | Điều hướng bằng lối tắt |
| Description | Mở nhanh một chức năng khám phá từ Home |
| Actor | Người dùng |
| Preconditions | Home hiển thị danh sách lối tắt |
| Trigger | Nhấn một lối tắt |
| Main Flow | 1. Hệ thống nhận diện lối tắt. 2. Hệ thống kiểm tra dữ liệu và quyền truy cập. 3. Hệ thống mở đúng màn đích. |
| Alternative Flow | Nhấn “Bản Đồ Sao” khi thiếu dữ liệu sinh thì hiển thị hướng dẫn bổ sung. |
| Exception Rules | Tính năng chưa có màn đích hoặc chưa phát hành phải hiển thị thông báo rõ, không mở màn trắng. |
| Postconditions | Màn đích mở đúng ngữ cảnh; quay lại giữ vị trí cuộn Home. |

### UC-HOME-05 — Làm mới Home

| Trường | Nội dung |
|---|---|
| Use Case ID | UC-HOME-05 |
| Name | Làm mới dữ liệu Home |
| Description | Cập nhật các khối dữ liệu mà không tạo bản ghi hoặc kết quả trùng |
| Actor | Người dùng |
| Preconditions | Đang ở đầu danh sách Home |
| Trigger | Kéo màn hình xuống |
| Main Flow | 1. Hệ thống hiển thị indicator. 2. Hệ thống làm mới từng khối. 3. Khối thành công cập nhật nội dung. 4. Indicator đóng khi quá trình kết thúc. |
| Alternative Flow | Khối nào không thay đổi thì giữ nguyên trạng thái và dữ liệu. |
| Exception Rules | Khối lỗi hiển thị Retry riêng; không xóa dữ liệu cũ còn hợp lệ. |
| Postconditions | Home hiển thị dữ liệu mới nhất có thể sử dụng. |

## 5. Business Rules

### BR1. Dữ liệu theo ngày

- Mood, Tarot và chỉ số phải dùng cùng ngày nghiệp vụ theo múi giờ người dùng.
- Khi qua ngày mới, Home tải dữ liệu ngày mới; dữ liệu ngày trước không bị ghi đè.

### BR2. Lời chào cá nhân hóa

- Dùng tên hiển thị từ hồ sơ hiện hành.
- Thiếu tên thì hiển thị “Chào bạn”; không hiển thị email, mã tài khoản hoặc giá trị rỗng.

### BR3. Điểm danh cảm xúc

- Chỉ một mood được chọn tại một thời điểm.
- Mood chọn tại Home là dữ liệu tạm cho đến khi người dùng lưu tại APP-SCR-014.
- Nếu đã check-in, card hiển thị mood đã lưu và hành động xem/chỉnh sửa.

### BR4. Tarot hôm nay

- Kết quả đã cấp phải ổn định trong cùng ngày; refresh hoặc retry không tạo lá khác.
- Người dùng Premium được trải bài nhiều lần hơn người dùng thường.
- Hạn mức cụ thể theo ngày hoặc theo kỳ là `Cần xác nhận`.

### BR5. Quyền Premium

- Cung Sao và nội dung chuyên sâu chỉ hiển thị đầy đủ khi entitlement còn hiệu lực.
- Người dùng thường được xem teaser/badge Premium.
- Chỉ mở APP-SCR-053 sau khi người dùng chủ động nhấn nội dung bị khóa.

### BR6. Chỉ số hôm nay

- Mỗi chỉ số hiển thị tên, icon và giá trị từ 0% đến 100%.
- Tên chính thức của bốn chỉ số trong ảnh cần được xác nhận trước baseline.
- Nội dung chỉ mang tính tham khảo; không khẳng định y tế, tài chính hoặc định mệnh.

### BR7. Lỗi độc lập theo khối

- Lỗi Check-in, Tarot hoặc Chỉ số không làm mất các khối còn lại.
- Mỗi khối lỗi có Retry riêng.
- Retry không tạo thao tác ghi hoặc kết quả trùng.

### BR8. Lối tắt nhanh

- Thứ tự mặc định theo ảnh: Bói Bài, Trực Giác, Bản Đồ Sao, Hợp Đôi.
- Không tự thay đổi thứ tự theo hành vi nếu chưa có yêu cầu cá nhân hóa được phê duyệt.
- Lối tắt chưa phát hành phải được ẩn hoặc hiển thị trạng thái “Sắp ra mắt”; không mở màn trắng.

### BR9. Bottom navigation

- Home luôn chọn tab “Trang Chủ”.
- Nhấn lại tab đang chọn chỉ cuộn lên đầu.
- Chuyển tab không làm mất kết quả check-in hoặc Tarot đã lưu.

## 6. Validation

| Trường hoặc hành động | Điều kiện hợp lệ | Điều kiện không hợp lệ | Thông báo hiển thị |
|---|---|---|---|
| Chọn mood | Mood thuộc danh sách đang hỗ trợ | Không có hoặc giá trị không hợp lệ | “Vui lòng chọn cảm xúc của bạn.” |
| Mở Tarot hôm nay | Ngày và phiên hợp lệ | Không tải được trạng thái hoặc kết quả | “Không thể tải lá bài hôm nay. Vui lòng thử lại.” |
| Mở Bản Đồ Sao | Có ngày, giờ và nơi sinh đủ dùng | Thiếu giờ hoặc nơi sinh | “Hãy bổ sung giờ và nơi sinh để xem bản đồ sao chính xác.” |
| Mở nội dung Premium | Entitlement còn hiệu lực | Không có hoặc đã hết hạn | Hiển thị teaser và CTA “Khám phá Premium” |
| Làm mới Home | Có mạng hoặc cache hợp lệ | Mất mạng và không có cache | “Không thể cập nhật dữ liệu. Vui lòng kiểm tra kết nối.” |
| Nhấn CTA liên tục | Chưa có thao tác đang xử lý | Đang loading | Không tạo yêu cầu mới; giữ nút ở trạng thái loading |

## 7. Trạng thái màn hình

| Trạng thái | Nội dung hiển thị | Thành phần được thao tác | Hành động tiếp theo |
|---|---|---|---|
| Loading lần đầu | Header, bottom navigation và skeleton từng card | Đổi tab; mở Profile nếu phiên đã sẵn sàng | Chờ từng khối tải xong |
| Có dữ liệu | Toàn bộ nội dung theo ảnh | Tất cả hành động hợp lệ | Chọn card, lối tắt hoặc tab |
| Chưa check-in | Bốn mood và CTA ghi nhận | Chọn mood hoặc mở APP-SCR-014 | Điểm danh cảm xúc |
| Đã check-in | Mood đã lưu và trạng thái hoàn tất | Xem hoặc chỉnh sửa | Mở APP-SCR-014 |
| Chưa rút Tarot | Mặt sau lá bài và CTA “Rút bài hôm nay” | Rút bài | Mở APP-SCR-013 |
| Đã rút Tarot | Ảnh, tên lá, thông điệp và CTA “Xem lại” | Xem lại | Mở đúng kết quả APP-SCR-013 |
| Thiếu hồ sơ | Khối liên quan hiển thị “Chưa đủ thông tin” | Bổ sung hồ sơ | Mở APP-SCR-046 |
| Lỗi một phần | Khối lỗi có thông báo và Retry; khối khác giữ dữ liệu | Retry hoặc dùng khối khác | Tải lại riêng khối |
| Lỗi toàn màn | Header, bottom navigation, thông báo và Retry | Retry hoặc đổi tab | Tải lại Home |
| Offline có cache | Banner offline, dữ liệu gần nhất và thời điểm cập nhật | Xem cache; dùng thao tác offline được hỗ trợ | Kết nối lại để cập nhật |
| Không đủ quyền Premium | Teaser, badge Premium và CTA | Mở thông tin Premium | APP-SCR-053 |

## 8. Thông báo

| Mã | Trường hợp | Nội dung thông báo | Kiểu hiển thị | Thời điểm đóng |
|---|---|---|---|---|
| HOME-M01 | Chưa chọn mood | “Vui lòng chọn cảm xúc của bạn.” | Inline trong card | Khi chọn mood |
| HOME-M02 | Không tải được một khối | “Không thể tải nội dung. Vui lòng thử lại.” | Inline + Retry | Khi Retry thành công |
| HOME-M03 | Mất mạng | “Bạn đang ngoại tuyến. Một số nội dung có thể chưa được cập nhật.” | Banner | Khi có mạng lại |
| HOME-M04 | Thiếu dữ liệu bản đồ sao | “Hãy bổ sung giờ và nơi sinh để xem bản đồ sao chính xác.” | Bottom sheet | Khi đóng hoặc chọn CTA |
| HOME-M05 | Tính năng chưa phát hành | “Tính năng này đang được hoàn thiện.” | Toast/Snackbar | Tự đóng theo thời gian chuẩn |
| HOME-M06 | Không tải được Tarot | “Không thể tải lá bài hôm nay. Vui lòng thử lại.” | Inline trong card | Khi Retry thành công |

## 9. Hiệu ứng và phản hồi

- Card và nút giảm nhẹ độ sáng hoặc scale khi nhấn; không làm bố cục nhảy.
- Mood được chọn đổi nền, viền và có dấu chọn; không truyền đạt chỉ bằng màu.
- Pull-to-refresh hiển thị indicator ở đầu màn và dừng khi quá trình hoàn tất hoặc hết thời gian chờ.
- Tarot reveal chỉ diễn ra trong APP-SCR-013; Home không tự lật bài.
- Bottom sheet trượt từ dưới lên và có nền mờ; vuốt xuống hoặc nhấn vùng nền để đóng nếu hành động không bắt buộc.
- Khi Reduce Motion được bật, thay scale/slide bằng đổi opacity ngắn và cập nhật trạng thái tức thời.
- Loading không che bottom navigation; người dùng vẫn có thể rời Home.
- Khi một khối lỗi, chỉ khối đó chuyển sang trạng thái lỗi; bố cục các khối khác không bị thay đổi.

## 10. Điều hướng

| Hành động | Điều kiện | Màn hình hoặc trạng thái đích | Dữ liệu cần giữ |
|---|---|---|---|
| Nhấn avatar | Luôn khả dụng | APP-SCR-045 Profile | Vị trí cuộn Home |
| Nhấn CTA mood | Có mood hoặc mở luồng trống | APP-SCR-014 Daily Check-in | Mood đang chọn và ngày hiện tại |
| Nhấn Tarot hôm nay | Card tải thành công | APP-SCR-013 | Ngày và kết quả đã cấp nếu có |
| Nhấn “Xem tất cả” chỉ số | Có dữ liệu | APP-SCR-012 | Ngày hiện tại |
| Nhấn “Bói Bài” | Còn quyền/lượt phù hợp | APP-SCR-016 | Nguồn mở là Home |
| Nhấn “Trực Giác” | Tính năng đã phát hành | `Cần xác nhận` | Nguồn mở là Home |
| Nhấn “Bản Đồ Sao” | Đủ dữ liệu sinh | APP-SCR-058 | Hồ sơ sinh hiện hành |
| Nhấn “Bản Đồ Sao” | Thiếu dữ liệu sinh | Bottom sheet và APP-SCR-046 | Danh sách trường còn thiếu |
| Nhấn “Hợp Đôi” | Luôn khả dụng | APP-SCR-028 | Hồ sơ hoặc cung của người dùng nếu có |
| Nhấn tab “Bài Tarot” | Luôn khả dụng | APP-SCR-016 | Không |
| Nhấn tab “Cung Sao” | Có Premium | APP-SCR-024 | Cung cá nhân nếu có |
| Nhấn tab “Cung Sao” | Không có Premium | APP-SCR-053 | Màn nguồn và quyền lợi được chọn |
| Nhấn tab “Tôi” | Luôn khả dụng | APP-SCR-045 | Không |

## 11. Tiêu chí nghiệm thu

- Khi người dùng mở Home, hệ thống hiển thị header, lời chào, Điểm Danh Cảm Xúc, Tarot hôm nay, Chỉ Số Hôm Nay, Lối Tắt Nhanh và bottom navigation đúng thứ tự.
- Khi hồ sơ có tên hiển thị, lời chào sử dụng đúng tên; khi thiếu tên, hệ thống hiển thị “Chào bạn”.
- Khi người dùng chọn một mood, chỉ mood đó có trạng thái được chọn và CTA giữ đúng giá trị khi mở APP-SCR-014.
- Khi người dùng nhấn CTA mà chưa chọn mood, hệ thống không ghi nhận và hiển thị “Vui lòng chọn cảm xúc của bạn.”
- Khi hôm nay chưa có lá Tarot, card hiển thị CTA rút bài; khi đã có, card hiển thị đúng lá và CTA xem lại.
- Khi người dùng refresh hoặc nhấn liên tục CTA Tarot, hệ thống không tạo nhiều kết quả cho cùng một lần xử lý.
- Khi nhấn “Bói Bài”, “Bản Đồ Sao” hoặc “Hợp Đôi”, hệ thống mở đúng màn đích và giữ vị trí cuộn Home khi quay lại.
- Khi nhấn “Bản Đồ Sao” nhưng thiếu giờ hoặc nơi sinh, hệ thống không tạo bản đồ suy đoán và cung cấp CTA bổ sung dữ liệu.
- Khi người dùng thường nhấn tab “Cung Sao”, hệ thống giải thích quyền lợi Premium và chỉ mở Paywall sau thao tác đó.
- Khi một khối tải lỗi, các khối còn lại và bottom navigation vẫn sử dụng được; khối lỗi có Retry riêng.
- Khi mất mạng và có cache, hệ thống hiển thị dữ liệu gần nhất kèm banner offline; khi không có cache, hệ thống hiển thị hành động thử lại.
- Khi dùng screen reader, mỗi lối tắt được đọc bằng tên và kết quả điều hướng; mỗi chỉ số được đọc cả tên và phần trăm.
- Khi tăng cỡ chữ, card tăng chiều cao và nội dung không bị cắt hoặc chồng lấn.

## Điểm cần xác nhận

1. Tên và màn đích chính xác của chip ở góc phải phần đầu màn.
2. Tên chính thức của bốn mood trong card “Điểm Danh Cảm Xúc”.
3. Tên chính thức của bốn “Chỉ Số Hôm Nay”.
4. “Trực Giác” là tính năng gì, Screen ID nào và có yêu cầu Premium hay không.
5. APP-SCR-058 Birth Chart cần được bổ sung chính thức vào index và viết đặc tả riêng.
6. Số dư Sao dùng để làm gì và có màn lịch sử riêng hay chỉ dùng bottom sheet giải thích.
7. Hạn mức Tarot cụ thể của người dùng thường và Premium.
8. Nhấn một chỉ số mở bottom sheet trên Home hay mở APP-SCR-012.
