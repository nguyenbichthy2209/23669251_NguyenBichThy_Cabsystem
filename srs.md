
# Bước 1: Xác định ngữ cảnh nghiệp vụ và vấn đề nghiệp vụ
Trả lời: khách hàng muốn giải quyết vấn đề gì, tại sao ko thể đáp ứng, mục tiêu kinh doanh, gái trị hệ thống tạo ra so với hệ thống cũ, ai sẽ là người ử dụng hệ thống
# Ngữ cảnh nghiệp vụ (Business Context)
- Công ty ABC là doanh nghiệp cung cấp dịch vụ đặt xe trực tuyến. Hiện tại, khách hàng đặt xe bằng cách liên hệ tổng đài hoặc sử dụng một ứng dụng đơn giản. Quy trình hoạt động liên quan đến khách hàng đặt chuyến, doanh nghiệp tìm và phân công tài xế, tài xế thực hiện chuyến đi, sau đó tính cước và thanh toán.Do nhu cầu phục vụ số lượng lớn khách hàng và tài xế cũng như nhu cầu mở rộng trong tương lai, công ty muốn xây dựng CAB System – một nền tảng đặt xe mới, phục vụ ít nhất ba nhóm người dùng chính: khách hàng, tài xế và nhân viên vận hành.
# Vấn đề nghiệp vụ (Business Problem)
-Phân công tài xế chủ yếu thủ công, làm giảm hiệu quả vận hành và khó đáp ứng khi số lượng chuyến tăng.
-Khách hàng khó theo dõi trạng thái chuyến đi, chẳng hạn hệ thống đang tìm tài xế hay tài xế nào đã nhận chuyến.
-Thông tin thanh toán chưa được quản lý tập trung.
-Bộ phận vận hành gặp khó khăn khi mở rộng hệ thống.
-Hệ thống hiện tại chưa hỗ trợ tốt việc quản lý xuyên suốt quy trình từ đặt xe → tìm tài xế → thực hiện chuyến → tính cước → thanh toán → thông báo → đánh giá.
-Công ty cần một hệ thống có khả năng mở rộng và phát triển thêm tính năng mà không phải xây dựng lại toàn bộ ứng dụng.

# Bước 2: Xác định các stakeholder và vai trò/Vẽ ma trận stakeholder
# Xác định các Stakeholder
| Stakeholder | Vai trò |
|---|---|
| Khách hàng (Customer) | Người sử dụng dịch vụ đặt xe; thực hiện đặt xe, theo dõi chuyến đi, thanh toán và đánh giá tài xế. |
| Tài xế (Driver) | Người cung cấp dịch vụ vận chuyển; nhận hoặc từ chối chuyến, thực hiện chuyến và cập nhật trạng thái chuyến đi. |
| Nhân viên vận hành (Operator) | Quản lý khách hàng, tài xế, phương tiện và chuyến đi; theo dõi hoạt động và hỗ trợ xử lý sự cố. |
| Ban lãnh đạo (Management) | Đưa ra mục tiêu và yêu cầu kinh doanh; theo dõi báo cáo, doanh thu và hiệu quả hoạt động của hệ thống. |
| Nhà cung cấp thanh toán | Đối tác bên ngoài thực hiện xử lý các giao dịch thanh toán điện tử cho hệ thống CAB. |
# Vẽ ma trận stakeholder: để biết mức độ ảnh hưởng của các vai trò trong hệ thống
                     ## Ma trận Stakeholder

Ma trận Stakeholder được sử dụng để xác định mức độ quyền lực và mức độ quan tâm của các bên liên quan đối với hệ thống.

| Quyền lực / Mức độ quan tâm | Quan tâm thấp | Quan tâm cao |
|---|---|---|
| **Quyền lực cao** | **Duy trì sự hài lòng:** Nhà cung cấp thanh toán | **Quản lý chặt chẽ:** Ban lãnh đạo, Nhân viên vận hành |
| **Quyền lực thấp** | **Theo dõi:** Chưa xác định | **Cập nhật thông tin thường xuyên:** Khách hàng, Tài xế |
        
# Bước 3: Business Goal 
nên đặt tên là BG01...ví dụ BG01 tăng hiệu quả thanh toán thì mục đích->cho phép thanh toán bằng tiền mặt, chuyển khoản, onl.
Vd:BG01: giảm thời gian tim tài xế:
  cho phép tìm tài xế tự động
## Business Goals

- **BG01: Giảm thời gian tìm tài xế:** Cho phép hệ thống tự động tìm và phân công tài xế phù hợp.

- **BG02: Nâng cao trải nghiệm khách hàng:** Cho phép khách hàng đặt xe và theo dõi trạng thái chuyến đi thuận tiện.

- **BG03: Nâng cao hiệu quả vận hành:** Giảm việc phân công tài xế thủ công và hỗ trợ quản lý chuyến đi.

- **BG04: Quản lý thanh toán tập trung:** Quản lý tính cước và kết quả thanh toán của chuyến đi.

- **BG05: Hỗ trợ quản lý và ra quyết định:** Cung cấp báo cáo về chuyến đi, doanh thu và hiệu quả hoạt động.

- **BG06: Đảm bảo khả năng mở rộng:** Hỗ trợ số lượng lớn khách hàng, tài xế và khả năng bổ sung chức năng trong tương lai.

## Bước 4: Xác định phạm vi (Scope)

### Trong phạm vi

- Quản lý khách hàng: tài khoản, thông tin cá nhân và lịch sử chuyến đi.
- Quản lý tài xế và phương tiện: hồ sơ, phương tiện, trạng thái hoạt động và vị trí.
- Đặt xe: điểm đón, điểm đến, loại xe và tạo yêu cầu chuyến.
- Tìm và phân công tài xế: tự động tìm tài xế phù hợp và xử lý khi tài xế từ chối hoặc không phản hồi.
- Quản lý chuyến đi: theo dõi và cập nhật trạng thái chuyến.
- Tính cước và thanh toán: hỗ trợ tiền mặt và thanh toán điện tử.
- Thông báo: gửi thông báo liên quan đến đặt xe, tài xế, chuyến đi và thanh toán.
- Đánh giá sau chuyến: khách hàng đánh giá tài xế.
- Quản trị hệ thống: quản lý khách hàng, tài xế, phương tiện, chuyến đi và phân quyền.
- Báo cáo: số lượng chuyến, doanh thu, tỷ lệ hoàn thành, tỷ lệ hủy và hiệu quả tài xế.

### Ngoài phạm vi

- Chi tiết cách tính cước.
- Tiêu chí ưu tiên tài xế.
- Thời gian tài xế phải phản hồi.
- Chính sách hủy chuyến.
- Cách xử lý khi mất kết nối mạng.
- Thời gian lưu trữ dữ liệu.

# Bước 5: Chuyển đổi Business Requirement
VD: BR02:Tìm tài xế, hệ thống cho phép tìm tài xế phù hợp với chuyến đi
VD: BR03: Theo dõi chuyến đi: kh có thể theo dõi chuyến đi trong quá trình di chuyển
# Business Requirements
| Mã | Tên | Diễn giải |
|---|---|---|
| BR01 | Quản lý đặt xe | Hỗ trợ khách hàng tạo yêu cầu đặt xe theo điểm đón, điểm đến và loại xe. |
| BR02 | Tìm và phân công tài xế | Tự động tìm tài xế phù hợp, ưu tiên tài xế gần và sẵn sàng nhận chuyến. |
| BR03 | Quản lý chuyến đi | Theo dõi và cập nhật trạng thái chuyến đi từ khi đặt xe đến khi hoàn thành. |
| BR04 | Quản lý khách hàng | Quản lý tài khoản, thông tin cá nhân và lịch sử chuyến đi của khách hàng. |
| BR05 | Quản lý tài xế và phương tiện | Quản lý hồ sơ tài xế, phương tiện, vị trí và trạng thái hoạt động. |
| BR06 | Tính cước và thanh toán | Tính tiền chuyến đi và hỗ trợ thanh toán bằng tiền mặt hoặc điện tử. |
| BR07 | Quản lý thông báo | Gửi thông báo cho khách hàng và tài xế về các sự kiện liên quan đến chuyến đi. |
| BR08 | Đánh giá tài xế | Cho phép khách hàng đánh giá tài xế sau khi chuyến đi hoàn thành. |
| BR09 | Quản lý vận hành | Hỗ trợ nhân viên theo dõi chuyến đi, tài xế và xử lý các trường hợp gặp sự cố. |
| BR10 | Báo cáo hoạt động | Cung cấp báo cáo về chuyến đi, doanh thu, tỷ lệ hoàn thành, tỷ lệ hủy và hiệu quả tài xế. |
| BR11 | Khả năng mở rộng | Hỗ trợ số lượng lớn người dùng và cho phép bổ sung dịch vụ, thanh toán, thông báo trong tương lai. |

# Bước 6: Business Process(Quy trình nghiệp vụ)
VD: khách hàng tạo chuyến đi, hệ thống xác nhận(vị trí đón,đến),tìm tài xế, 
# Bước 7: Viết functional requirement phân rã yêu cầu về chức năng
VD: FR01:Xác định vị trí khách
FR02:Tìm tài xế sẵn có
FR03: Lọc theo loại xe
F04: Tính khoảng cách từ điểm đi đến điểm đón
#Phân rã quản lý khcahs hàng: đăng ký, đăng nhập, cập nhật thông tin, xem thông tin 
# Functional Requirement
## Quản lý khách hàng
- FR01: Đăng ký tài khoản khách hàng.
- FR02: Đăng nhập hệ thống.
- FR03: Cập nhật thông tin cá nhân.
- FR04: Xem thông tin cá nhân.
- FR05: Xem lịch sử chuyến đi.
## Đặt xe và tìm tài xế
- FR06: Nhập điểm đón.
- FR07: Nhập điểm đến.
- FR08: Lựa chọn loại xe.
- FR09: Gửi yêu cầu đặt xe.
- FR10: Xác định vị trí khách hàng.
- FR11: Tìm tài xế đang sẵn sàng.
- FR12: Lọc tài xế theo loại xe phù hợp.
- FR13: Tính khoảng cách giữa tài xế và điểm đón.
- FR14: Ưu tiên tài xế gần và phù hợp.
- FR15: Gửi yêu cầu chuyến đến tài xế.
- FR16: Tìm tài xế khác khi tài xế từ chối hoặc không phản hồi.
- FR17: Thông báo cho khách hàng khi không tìm được tài xế.
## Quản lý tài xế
- FR18: Đăng ký tài khoản tài xế.
- FR19: Đăng nhập tài khoản tài xế.
- FR20: Cập nhật hồ sơ tài xế.
- FR21: Cập nhật thông tin phương tiện.
- FR22: Cập nhật trạng thái sẵn sàng nhận chuyến.
- FR23: Cập nhật vị trí tài xế.
- FR24: Nhận thông báo chuyến mới.
- FR25: Chấp nhận chuyến.
- FR26: Từ chối chuyến.
## Quản lý chuyến đi
- FR27: Hiển thị trạng thái đang tìm tài xế.
- FR28: Hiển thị thông tin tài xế nhận chuyến.
- FR29: Hiển thị thời gian dự kiến tài xế đến.
- FR30: Cập nhật trạng thái tài xế đã đến điểm đón.
- FR31: Cập nhật trạng thái đã đón khách.
- FR32: Cập nhật trạng thái đang di chuyển.
- FR33: Cập nhật trạng thái hoàn thành chuyến.
- FR34: Cho phép khách hàng theo dõi trạng thái chuyến đi.
## Tính cước và thanh toán
- FR35: Tính cước chuyến đi sau khi hoàn thành.
- FR36: Hiển thị số tiền khách hàng phải trả.
- FR37: Thanh toán bằng tiền mặt.
- FR38: Thanh toán điện tử.
- FR39: Gửi yêu cầu thanh toán đến nhà cung cấp thanh toán.
- FR40: Nhận kết quả giao dịch thanh toán.
- FR41: Thông báo khi thanh toán thành công.
- FR42: Thông báo khi thanh toán thất bại.
- FR43: Cho phép xử lý lại thanh toán thất bại theo chính sách.
## Quản lý thông báo
- FR44: Thông báo khi yêu cầu đặt xe được tiếp nhận.
- FR45: Thông báo khi có tài xế nhận chuyến.
- FR46: Thông báo khi tài xế đến điểm đón.
- FR47: Thông báo khi chuyến đi hoàn thành.
- FR48: Thông báo kết quả thanh toán.
- FR49: Thông báo chuyến mới cho tài xế.
- FR50: Thông báo thay đổi liên quan đến chuyến đang thực hiện.
## Đánh giá tài xế
- FR51: Hiển thị chức năng đánh giá sau khi chuyến hoàn thành.
- FR52: Cho phép khách hàng đánh giá tài xế.
- FR53: Lưu kết quả đánh giá tài xế.
## Quản lý vận hành
- FR54: Quản lý thông tin khách hàng.
- FR55: Quản lý thông tin tài xế.
- FR56: Quản lý phương tiện.
- FR57: Quản lý chuyến đi.
- FR58: Xem các chuyến đang diễn ra.
- FR59: Xem trạng thái tài xế.
- FR60: Hỗ trợ xử lý chuyến bị lỗi.
- FR61: Tra cứu lịch sử giao dịch.
- FR62: Phân quyền chức năng quản trị.
- FR63: Lưu vết các thao tác quan trọng.
## Báo cáo
- FR64: Thống kê số lượng chuyến đi.
- FR65: Thống kê doanh thu.
- FR66: Thống kê tỷ lệ chuyến hoàn thành.
- FR67: Thống kê tỷ lệ chuyến bị hủy.
- FR68: Báo cáo hiệu quả hoạt động của tài xế.
# Bước 8: Business rule và exception(quy tắc nghiệp vụ và ngoại lệ)
## 1. Business Rules – Quy tắc nghiệp vụ
| Mã | Quy tắc nghiệp vụ | Diễn giải |
|---|---|---|
| BRU01 | Chỉ tài xế sẵn sàng mới được xét nhận chuyến | Hệ thống chỉ tìm các tài xế đang ở trạng thái sẵn sàng và phù hợp với yêu cầu chuyến. |
| BRU02 | Ưu tiên tài xế phù hợp và gần khách hàng | Việc tìm tài xế dựa trên vị trí, trạng thái sẵn sàng và các tiêu chí vận hành khác. |
| BRU03 | Tự động tìm tài xế khác nếu tài xế không nhận | Nếu tài xế từ chối hoặc không phản hồi, hệ thống tiếp tục tìm tài xế khác mà khách hàng không cần đặt lại. |
| BRU04 | Tài xế phải cập nhật trạng thái chuyến | Tài xế cập nhật các trạng thái: đã đến điểm đón, đã đón khách, đang di chuyển và hoàn thành chuyến. |
| BRU05 | Tính cước sau khi chuyến hoàn thành | Sau khi chuyến hoàn thành, hệ thống xác định số tiền khách hàng phải trả. |
| BRU06 | Hỗ trợ nhiều hình thức thanh toán | Khách hàng có thể thanh toán bằng tiền mặt hoặc thanh toán điện tử. |
| BRU07 | Không lưu thông tin thanh toán nhạy cảm | Hệ thống CAB không lưu trực tiếp thông tin nhạy cảm của thẻ hoặc tài khoản thanh toán. |
| BRU08 | Người dùng phải được xác thực | Khách hàng và tài xế phải được xác thực trước khi sử dụng các chức năng yêu cầu tài khoản. |
| BRU09 | Chức năng quản trị phải được phân quyền | Nhân viên chỉ được thực hiện các thao tác quản trị phù hợp với quyền được cấp. |
| BRU10 | Đánh giá sau khi hoàn thành chuyến | Khách hàng có thể đánh giá tài xế sau khi chuyến đi hoàn thành. |
## 2. Exceptions – Ngoại lệ
| Mã | Ngoại lệ | Cách xử lý |
|---|---|---|
| EX01 | Tài xế từ chối chuyến | Hệ thống tiếp tục tìm tài xế khác. |
| EX02 | Tài xế không phản hồi | Hệ thống tiếp tục tìm tài xế khác. |
| EX03 | Không tìm được tài xế | Hệ thống thông báo rõ ràng cho khách hàng. |
| EX04 | Thanh toán điện tử thất bại | Thông báo cho khách hàng và cho phép xử lý lại theo chính sách doanh nghiệp. |
| EX05 | Chuyến đi gặp lỗi | Nhân viên vận hành kiểm tra và hỗ trợ xử lý. |
| EX06 | Mất kết nối mạng | Chưa xác định cách xử lý, cần làm rõ với khách hàng. |
| EX07 | Khách hàng hủy chuyến | Chính sách hủy chuyến chưa được xác định, cần làm rõ với khách hàng. |
| EX08 | Tài xế không phản hồi trong thời gian quy định | Thời gian phản hồi chưa được xác định, cần làm rõ với khách hàng. |
## Bước 9: Mô hình hóa dữ liệu
### Xác định các thực thể trong ERD
- **Khách hàng** (customer_id, full_name, email, phone, password, address)
- **Tài xế** (driver_id, full_name, email, phone, password, status, current_location)
- **Phương tiện** (vehicle_id, driver_id, vehicle_type, license_plate, vehicle_name)
- **Chuyến đi** (trip_id, customer_id, driver_id, pickup_location, destination, vehicle_type, status, start_time, end_time)
- **Thanh toán** (payment_id, trip_id, amount, payment_method, payment_status, payment_time)
- **Đánh giá** (rating_id, trip_id, customer_id, driver_id, score, comment)
- **Thông báo** (notification_id, user_id, content, notification_type, status, created_at)
- **Nhân viên vận hành** (operator_id, full_name, email, password, role)
- **Lịch sử giao dịch** (transaction_id, payment_id, amount, status, transaction_time)
- 
# Bước 10: Non functional requirement
## Non-Functional Requirements
| Mã | Tên | Diễn giải |
|---|---|---|
| NFR01 | Hiệu năng | Hệ thống phải hoạt động ổn định vào các thời điểm nhu cầu đặt xe tăng cao. |
| NFR02 | Khả năng mở rộng | Hệ thống phải có khả năng phục vụ số lượng lớn khách hàng và tài xế. |
| NFR03 | Mở rộng độc lập | Các thành phần của hệ thống phải có khả năng mở rộng độc lập khi tải tăng. |
| NFR04 | Độ tin cậy | Lỗi ở chức năng thanh toán hoặc thông báo không được làm toàn bộ hệ thống đặt xe ngừng hoạt động. |
| NFR05 | Khả năng triển khai | Cho phép triển khai chức năng mới từng phần và hạn chế ảnh hưởng đến các chức năng đang hoạt động. |
| NFR06 | Xác thực | Khách hàng và tài xế phải được xác thực trước khi sử dụng các chức năng yêu cầu tài khoản. |
| NFR07 | Phân quyền | Các chức năng quản trị phải được kiểm soát quyền truy cập. |
| NFR08 | Bảo mật dữ liệu | Thông tin cá nhân, phương tiện, vị trí và dữ liệu giao dịch phải được bảo vệ. |
| NFR09 | Bảo mật thanh toán | Không lưu trực tiếp thông tin nhạy cảm của thẻ hoặc tài khoản thanh toán trong CAB System. |
| NFR10 | Khả năng kiểm tra | Hệ thống phải lưu vết các thao tác quan trọng để phục vụ kiểm tra khi xảy ra sự cố. |
| NFR11 | Khả năng mở rộng chức năng | Có thể bổ sung loại dịch vụ, phương thức thanh toán và nhà cung cấp thông báo mới mà không phải xây dựng lại toàn bộ hệ thống. |
| NFR12 | Khả năng bảo trì | Có thể thay đổi một số thành phần kỹ thuật mà không phải xây dựng lại toàn bộ ứng dụng. |
# Bước 11: Vẽ use case
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/84806b90-0d8d-4977-a9bb-c81b46e08680" />
# Bước 12: Đặc tả Use Case

### UC01 - Đăng ký tài khoản khách hàng

| Thuộc tính | Nội dung |
|---|---|
| **Mã Use Case** | UC01 |
| **Tên Use Case** | Đăng ký tài khoản khách hàng |
| **Actor** | Khách hàng |
| **Mô tả** | Cho phép khách hàng tạo tài khoản để sử dụng CAB System. |
| **Tiền điều kiện** | Khách hàng chưa có tài khoản. |
| **Hậu điều kiện** | Tài khoản khách hàng được tạo trong hệ thống. |
| **Luồng chính** | 1. Khách hàng chọn đăng ký.<br>2. Khách hàng nhập thông tin cá nhân.<br>3. Khách hàng gửi yêu cầu đăng ký.<br>4. Hệ thống kiểm tra thông tin.<br>5. Hệ thống tạo tài khoản. |
| **Ngoại lệ** | Thông tin không hợp lệ → Hệ thống thông báo cho khách hàng kiểm tra lại. |

---

### UC02 - Đặt xe

| Thuộc tính | Nội dung |
|---|---|
| **Mã Use Case** | UC02 |
| **Tên Use Case** | Đặt xe |
| **Actor** | Khách hàng |
| **Mô tả** | Cho phép khách hàng tạo yêu cầu đặt xe. |
| **Tiền điều kiện** | Khách hàng đã đăng nhập và được xác thực. |
| **Hậu điều kiện** | Yêu cầu đặt xe được tạo và hệ thống bắt đầu tìm tài xế. |
| **Luồng chính** | 1. Khách hàng nhập điểm đón.<br>2. Khách hàng nhập điểm đến.<br>3. Khách hàng chọn loại xe.<br>4. Khách hàng gửi yêu cầu đặt xe.<br>5. Hệ thống tiếp nhận yêu cầu.<br>6. Hệ thống bắt đầu tìm tài xế phù hợp. |
| **Ngoại lệ** | Không tìm được tài xế → Hệ thống thông báo cho khách hàng. |
---

### UC03 - Tìm và phân công tài xế

| Thuộc tính | Nội dung |
|---|---|
| **Mã Use Case** | UC03 |
| **Tên Use Case** | Tìm và phân công tài xế |
| **Actor** | Khách hàng, Tài xế |
| **Mô tả** | Tìm và phân công tài xế phù hợp cho yêu cầu đặt xe của khách hàng. |
| **Tiền điều kiện** | Khách hàng đã tạo yêu cầu đặt xe. |
| **Hậu điều kiện** | Tài xế được phân công cho chuyến hoặc khách hàng được thông báo không tìm được tài xế. |
| **Luồng chính** | 1. Hệ thống xác định vị trí liên quan đến yêu cầu.<br>2. Hệ thống tìm tài xế đang sẵn sàng.<br>3. Hệ thống xác định tài xế phù hợp dựa trên vị trí và tiêu chí vận hành.<br>4. Hệ thống ưu tiên tài xế phù hợp và gần khách hàng.<br>5. Hệ thống gửi yêu cầu chuyến cho tài xế.<br>6. Tài xế chấp nhận chuyến.<br>7. Hệ thống phân công tài xế.<br>8. Hệ thống thông báo cho khách hàng. |
| **Luồng thay thế** | Tài xế từ chối hoặc không phản hồi → Hệ thống tiếp tục tìm tài xế khác mà khách hàng không cần đặt lại. |
| **Ngoại lệ** | Không tìm được tài xế phù hợp → Hệ thống thông báo rõ ràng cho khách hàng. |

---

### UC04 - Thực hiện chuyến đi

| Thuộc tính | Nội dung |
|---|---|
| **Mã Use Case** | UC04 |
| **Tên Use Case** | Thực hiện chuyến đi |
| **Actor** | Tài xế |
| **Mô tả** | Cho phép tài xế thực hiện và cập nhật trạng thái chuyến đi. |
| **Tiền điều kiện** | Tài xế đã chấp nhận và được phân công chuyến. |
| **Hậu điều kiện** | Chuyến đi được hoàn thành. |
| **Luồng chính** | 1. Tài xế di chuyển đến điểm đón.<br>2. Tài xế cập nhật trạng thái "Đã đến điểm đón".<br>3. Tài xế đón khách.<br>4. Tài xế cập nhật "Đã đón khách".<br>5. Tài xế cập nhật "Đang di chuyển".<br>6. Tài xế đến điểm đến.<br>7. Tài xế cập nhật "Hoàn thành chuyến". |
| **Ngoại lệ** | Chuyến đi gặp lỗi → Nhân viên vận hành hỗ trợ xử lý. |

---

### UC05 - Thanh toán

| Thuộc tính | Nội dung |
|---|---|
| **Mã Use Case** | UC05 |
| **Tên Use Case** | Thanh toán |
| **Actor** | Khách hàng, Nhà cung cấp thanh toán |
| **Mô tả** | Xử lý tính cước và thanh toán sau khi chuyến đi hoàn thành. |
| **Tiền điều kiện** | Chuyến đi đã hoàn thành. |
| **Hậu điều kiện** | Kết quả thanh toán được ghi nhận. |
| **Luồng chính** | 1. Hệ thống xác định số tiền phải trả.<br>2. Hệ thống hiển thị số tiền.<br>3. Khách hàng chọn phương thức thanh toán.<br>4. Nếu thanh toán điện tử, hệ thống gửi yêu cầu đến nhà cung cấp thanh toán.<br>5. Hệ thống nhận kết quả giao dịch.<br>6. Hệ thống ghi nhận kết quả.<br>7. Hệ thống thông báo cho khách hàng. |
| **Luồng thay thế** | Khách hàng chọn thanh toán bằng tiền mặt. |
| **Ngoại lệ** | Thanh toán điện tử thất bại → Thông báo cho khách hàng và cho phép xử lý lại theo chính sách doanh nghiệp. |

---

### UC06 - Đánh giá tài xế

| Thuộc tính | Nội dung |
|---|---|
| **Mã Use Case** | UC06 |
| **Tên Use Case** | Đánh giá tài xế |
| **Actor** | Khách hàng |
| **Mô tả** | Cho phép khách hàng đánh giá tài xế sau chuyến đi. |
| **Tiền điều kiện** | Chuyến đi đã hoàn thành. |
| **Hậu điều kiện** | Đánh giá của khách hàng được lưu vào hệ thống. |
| **Luồng chính** | 1. Khách hàng xem chuyến đã hoàn thành.<br>2. Khách hàng chọn chức năng đánh giá.<br>3. Khách hàng nhập đánh giá.<br>4. Khách hàng gửi đánh giá.<br>5. Hệ thống lưu kết quả đánh giá. |

---

### UC07 - Quản lý vận hành

| Thuộc tính | Nội dung |
|---|---|
| **Mã Use Case** | UC07 |
| **Tên Use Case** | Quản lý vận hành |
| **Actor** | Nhân viên vận hành |
| **Mô tả** | Cho phép nhân viên theo dõi và quản lý hoạt động của CAB System. |
| **Tiền điều kiện** | Nhân viên đã đăng nhập và có quyền phù hợp. |
| **Hậu điều kiện** | Các thao tác quản lý được hệ thống ghi nhận. |
| **Luồng chính** | 1. Nhân viên đăng nhập.<br>2. Nhân viên chọn chức năng quản lý.<br>3. Xem thông tin khách hàng, tài xế, phương tiện hoặc chuyến đi.<br>4. Theo dõi các chuyến đang diễn ra.<br>5. Kiểm tra trạng thái tài xế.<br>6. Hỗ trợ xử lý chuyến gặp lỗi.<br>7. Hệ thống ghi nhận thao tác. |
| **Ngoại lệ** | Nhân viên không có quyền thực hiện thao tác → Hệ thống từ chối truy cập. |

---

### UC08 - Xem báo cáo
| Thuộc tính | Nội dung |
|---|---|
| **Mã Use Case** | UC08 |
| **Tên Use Case** | Xem báo cáo |
| **Actor** | Ban lãnh đạo / Người dùng có quyền |
| **Mô tả** | Cho phép theo dõi các báo cáo về hoạt động kinh doanh của CAB System. |
| **Tiền điều kiện** | Người dùng đã đăng nhập và có quyền xem báo cáo. |
| **Hậu điều kiện** | Báo cáo được hiển thị cho người dùng. |
| **Luồng chính** | 1. Người dùng chọn chức năng báo cáo.<br>2. Hệ thống tổng hợp dữ liệu.<br>3. Hệ thống hiển thị số lượng chuyến.<br>4. Hiển thị doanh thu.<br>5. Hiển thị tỷ lệ chuyến hoàn thành và tỷ lệ hủy.<br>6. Hiển thị hiệu quả hoạt động của tài xế. |
| **Ngoại lệ** | Người dùng không có quyền → Hệ thống từ chối truy cập. |
# Bước 13: Tiêu chí chấp nhận (Acceptance Criteria)- nhờ nó mới được nghiệm thu, cho biết khi nào dự án hoàn thành và được nghiệm thu
## Tiêu chí chấp nhận (Acceptance Criteria)
| Mã | Chức năng | Tiêu chí chấp nhận |
|---|---|---|
| AC01 | Đăng ký tài khoản | Khách hàng có thể đăng ký tài khoản và hệ thống ghi nhận thông tin hợp lệ. |
| AC02 | Đăng nhập | Khách hàng và tài xế có thể đăng nhập và sử dụng các chức năng phù hợp với tài khoản. |
| AC03 | Đặt xe | Khách hàng có thể nhập điểm đón, điểm đến, chọn loại xe và gửi yêu cầu đặt xe. |
| AC04 | Tìm tài xế | Hệ thống tìm tài xế dựa trên vị trí, trạng thái sẵn sàng và các tiêu chí vận hành. |
| AC05 | Phân công tài xế | Khi tài xế chấp nhận chuyến, hệ thống ghi nhận tài xế cho chuyến và thông báo cho khách hàng. |
| AC06 | Tài xế từ chối/không phản hồi | Hệ thống tiếp tục tìm tài xế khác mà không yêu cầu khách hàng đặt lại chuyến. |
| AC07 | Không tìm được tài xế | Hệ thống thông báo rõ ràng cho khách hàng khi không tìm được tài xế phù hợp. |
| AC08 | Theo dõi chuyến đi | Khách hàng có thể xem tài xế nhận chuyến, thời gian dự kiến đến và trạng thái hiện tại của chuyến. |
| AC09 | Cập nhật chuyến đi | Tài xế có thể cập nhật các trạng thái: đã đến điểm đón, đã đón khách, đang di chuyển và hoàn thành. |
| AC10 | Tính cước | Sau khi chuyến hoàn thành, hệ thống xác định và hiển thị số tiền khách hàng phải trả. |
| AC11 | Thanh toán | Khách hàng có thể thanh toán bằng tiền mặt hoặc phương thức thanh toán điện tử. |
| AC12 | Thanh toán thất bại | Khi thanh toán điện tử thất bại, hệ thống thông báo cho khách hàng và cho phép xử lý lại theo chính sách. |
| AC13 | Thông báo | Khách hàng và tài xế nhận được thông báo tại các sự kiện liên quan đến chuyến đi. |
| AC14 | Đánh giá tài xế | Sau khi hoàn thành chuyến, khách hàng có thể gửi đánh giá tài xế. |
| AC15 | Quản lý vận hành | Nhân viên vận hành có thể theo dõi chuyến, trạng thái tài xế và hỗ trợ xử lý chuyến gặp lỗi. |
| AC16 | Phân quyền | Người dùng không có quyền không thể thực hiện các thao tác quản trị nhạy cảm. |
| AC17 | Báo cáo | Hệ thống cung cấp báo cáo về số chuyến, doanh thu, tỷ lệ hoàn thành, tỷ lệ hủy và hiệu quả tài xế. |
# Bước 14: Truy xuất nguồn gốc yêu cầu(Traceability requirements)-RTM(ma trận truy xuất nguồn gốc yêu cầu)
## Truy xuất nguồn gốc yêu cầu
## Requirement Traceability Matrix (RTM)
| ID | Business Goal | Business Requirement | Functional Requirement | Use Case | Acceptance Criteria |
|---|---|---|---|---|---|
| RTM01 | BG01 - Giảm thời gian tìm tài xế | BR02 - Tìm và phân công tài xế | FR10-FR17 - Xác định vị trí, tìm và phân công tài xế | UC03 - Tìm và phân công tài xế | AC04-AC07 |
| RTM02 | BG02 - Nâng cao trải nghiệm khách hàng | BR01 - Quản lý đặt xe | FR06-FR09 - Tạo yêu cầu đặt xe | UC02 - Đặt xe | AC03 |
| RTM03 | BG02 - Nâng cao trải nghiệm khách hàng | BR03 - Quản lý chuyến đi | FR27-FR34 - Theo dõi và cập nhật trạng thái chuyến | UC04 - Thực hiện chuyến đi | AC08-AC09 |
| RTM04 | BG02 - Nâng cao trải nghiệm khách hàng | BR04 - Quản lý khách hàng | FR01-FR05 - Đăng ký, đăng nhập, cập nhật và xem thông tin, lịch sử chuyến | UC01 - Đăng ký tài khoản | AC01-AC02 |
| RTM05 | BG03 - Nâng cao hiệu quả vận hành | BR05 - Quản lý tài xế và phương tiện | FR18-FR26 - Quản lý hồ sơ, phương tiện, trạng thái và nhận chuyến | UC04 - Thực hiện chuyến đi | AC02, AC09 |
| RTM06 | BG04 - Quản lý thanh toán tập trung | BR06 - Tính cước và thanh toán | FR35-FR43 - Tính cước và xử lý thanh toán | UC05 - Thanh toán | AC10-AC12 |
| RTM07 | BG02 - Nâng cao trải nghiệm khách hàng | BR07 - Quản lý thông báo | FR44-FR50 - Gửi thông báo cho khách hàng và tài xế | UC02, UC03, UC04, UC05 | AC13 |
| RTM08 | BG02 - Nâng cao trải nghiệm khách hàng | BR08 - Đánh giá tài xế | FR51-FR53 - Gửi và lưu đánh giá tài xế | UC06 - Đánh giá tài xế | AC14 |
| RTM09 | BG03 - Nâng cao hiệu quả vận hành | BR09 - Quản lý vận hành | FR54-FR63 - Quản lý và giám sát hoạt động hệ thống | UC07 - Quản lý vận hành | AC15-AC16 |
| RTM10 | BG05 - Hỗ trợ quản lý kinh doanh | BR10 - Báo cáo hoạt động | FR64-FR68 - Thống kê và báo cáo hoạt động | UC08 - Xem báo cáo | AC17 |
| RTM11 | BG06 - Tăng khả năng mở rộng | Yêu cầu khả năng mở rộng | NFR02, NFR03, NFR11, NFR12 | Không áp dụng trực tiếp | Kiểm thử khả năng mở rộng |
