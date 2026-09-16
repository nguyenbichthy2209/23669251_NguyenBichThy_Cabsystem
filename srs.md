
# Bước 1: Xác định ngữ cảnh nghiệp vụ và vấn đề nghiệp vụ
Trả lời: khách hàng muốn giải quyết vấn đề gì, tại sao ko thể đáp ứng, mục tiêu kinh doanh, gía trị hệ thống tạo ra so với hệ thống cũ, ai sẽ là người sử dụng hệ thống
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
| Tài xế (Driver) | Người cung cấp dịch vụ vận chuyển; nhận hoặc từ chối chuyến, cập nhật trạng thái chuyến đi. |
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

- **BG01 – Giảm việc phân công tài xế thủ công:** Hệ thống hỗ trợ tự động tìm tài xế đang sẵn sàng và phù hợp với loại xe khách hàng chọn.

- **BG02 – Nâng cao trải nghiệm khách hàng:** Cho phép khách hàng đặt xe và theo dõi trạng thái chuyến đi trên hệ thống.

- **BG03 – Nâng cao hiệu quả vận hành:** Quản lý tập trung khách hàng, tài xế, phương tiện và chuyến đi.

- **BG04 – Quản lý cước và thanh toán:** Ghi nhận số tiền phải trả và trạng thái thanh toán của từng chuyến.

- **BG05 – Hỗ trợ quản lý hoạt động:** Cung cấp các số liệu cơ bản về chuyến đi và doanh thu.

- **BG06 – Hỗ trợ mở rộng trong tương lai:** Cho phép bổ sung GPS, thanh toán điện tử và các kênh thông báo trong các phiên bản sau.

## Bước 4: Xác định phạm vi (Scope)

### Trong phạm vi

- Đăng ký tài khoản khách hàng.
- Đăng nhập hệ thống.
- Cập nhật thông tin cá nhân.
- Xem lịch sử chuyến đi.
- Quản lý thông tin tài xế.
- Quản lý phương tiện.
- Cập nhật trạng thái Sẵn sàng/Bận của tài xế.
- Cập nhật khu vực hoạt động của tài xế.
- Nhập điểm đón.
- Nhập điểm đến.
- Chọn loại xe.
- Tạo yêu cầu đặt xe.
- Tìm tài xế đang sẵn sàng.
- Lọc tài xế theo loại phương tiện và khu vực.
- Gửi yêu cầu chuyến cho tài xế.
- Tài xế chấp nhận hoặc từ chối chuyến.
- Tìm tài xế khác khi tài xế từ chối.
- Thông báo khi không tìm được tài xế.
- Hiển thị thông tin tài xế đã nhận chuyến.
- Tài xế cập nhật trạng thái chuyến đi.
- Khách hàng theo dõi trạng thái chuyến.
- Ghi nhận số tiền cước.
- Thanh toán bằng tiền mặt.
- Hiển thị thông báo trong hệ thống.
- Đánh giá tài xế.
- Nhân viên vận hành quản lý dữ liệu cơ bản.
- Phân quyền chức năng quản trị.
- Báo cáo cơ bản về số chuyến và doanh thu.

### Ngoài phạm vi

- Theo dõi GPS theo thời gian thực.
- Hiển thị bản đồ theo dõi xe trực tiếp.
- Tích hợp Google Maps hoặc Mapbox.
- Tính tài xế gần nhất bằng tọa độ GPS.
- Tính ETA dựa trên giao thông thời gian thực.
- Tích hợp cổng thanh toán điện tử thật như MoMo, VNPay hoặc Stripe.
- Push Notification qua Firebase.
- SMS hoặc email tự động.
- Tự động timeout khi tài xế không phản hồi.
- Chính sách hủy chuyến phức tạp.
- Xử lý mất kết nối mạng.
- Quy trình xử lý sự cố chuyến đi phức tạp.
- Audit log đầy đủ.
- Dashboard hoặc Business Intelligence nâng cao.
- Báo cáo tỷ lệ hủy và hiệu quả tài xế chuyên sâu.


# Bước 5: Chuyển đổi Business Requirement
VD: BR02:Tìm tài xế, hệ thống cho phép tìm tài xế phù hợp với chuyến đi
VD: BR03: Theo dõi chuyến đi: kh có thể theo dõi chuyến đi trong quá trình di chuyển
# Business Requirements
| Mã | Tên | Diễn giải |
|---|---|---|
| BR01 | Quản lý khách hàng | Hỗ trợ khách hàng đăng ký, đăng nhập, cập nhật thông tin và xem lịch sử chuyến. |
| BR02 | Quản lý tài xế và phương tiện | Quản lý hồ sơ tài xế, phương tiện và trạng thái hoạt động. |
| BR03 | Quản lý đặt xe | Cho phép khách hàng nhập thông tin và gửi yêu cầu đặt xe. |
| BR04 | Tìm và phân công tài xế | Tìm tài xế sẵn sàng, đúng loại xe và phù hợp khu vực để gửi yêu cầu chuyến. |
| BR05 | Quản lý chuyến đi | Theo dõi và cập nhật trạng thái chuyến từ khi tài xế nhận đến khi hoàn thành. |
| BR06 | Quản lý thanh toán | Ghi nhận cước và thanh toán tiền mặt trong phiên bản hiện tại. |
| BR07 | Quản lý thông báo | Hiển thị các thông báo liên quan đến chuyến trong hệ thống. |
| BR08 | Đánh giá tài xế | Cho phép khách hàng đánh giá tài xế sau khi chuyến hoàn thành. |
| BR09 | Quản lý vận hành | Cho phép nhân viên quản lý khách hàng, tài xế, phương tiện và chuyến đi. |
| BR10 | Báo cáo cơ bản | Hiển thị tổng số chuyến, số chuyến hoàn thành và tổng doanh thu. |

# Bước 6: Business Process(Quy trình nghiệp vụ)
VD: khách hàng tạo chuyến đi, hệ thống xác nhận(vị trí đón,đến),tìm tài xế, 
1. Khách hàng đăng nhập vào hệ thống.
2. Khách hàng nhập điểm đón.
3. Khách hàng nhập điểm đến.
4. Khách hàng chọn loại xe.
5. Khách hàng gửi yêu cầu đặt xe.
6. Hệ thống tạo chuyến với trạng thái **Đang tìm tài xế**.
7. Hệ thống tìm tài xế đang ở trạng thái **Sẵn sàng**.
8. Hệ thống lọc tài xế theo loại phương tiện và khu vực hoạt động.
9. Hệ thống gửi yêu cầu chuyến cho tài xế.
10. Tài xế xem yêu cầu chuyến.
11. Tài xế chấp nhận hoặc từ chối chuyến.
12. Nếu tài xế từ chối, hệ thống tiếp tục tìm tài xế khác.
13. Nếu không có tài xế phù hợp, hệ thống thông báo cho khách hàng.
14. Nếu tài xế chấp nhận, hệ thống phân công tài xế cho chuyến.
15. Hệ thống chuyển trạng thái tài xế sang **Bận**.
16. Khách hàng xem thông tin tài xế đã nhận chuyến.
17. Tài xế cập nhật trạng thái **Đã đến điểm đón**.
18. Tài xế cập nhật trạng thái **Đã đón khách**.
19. Tài xế cập nhật trạng thái **Đang di chuyển**.
20. Tài xế cập nhật trạng thái **Hoàn thành**.
21. Hệ thống chuyển trạng thái tài xế về **Sẵn sàng**.
22. Hệ thống ghi nhận số tiền cước.
23. Khách hàng thanh toán bằng tiền mặt.
24. Hệ thống ghi nhận kết quả thanh toán.
25. Khách hàng có thể đánh giá tài xế.
# Bước 7: Viết functional requirement phân rã yêu cầu về chức năng
VD: FR01:Xác định vị trí khách
FR02:Tìm tài xế sẵn có
FR03: Lọc theo loại xe
F04: Tính khoảng cách từ điểm đi đến điểm đón
#Phân rã quản lý khcahs hàng: đăng ký, đăng nhập, cập nhật thông tin, xem thông tin 
# Functional Requirement
## Quản lý khách hàng
- **FR01:** Đăng ký tài khoản khách hàng.
- **FR02:** Đăng nhập hệ thống.
- **FR03:** Cập nhật thông tin cá nhân.
- **FR04:** Xem lịch sử chuyến đi.
## Quản lý tài xế và phương tiện
- **FR05:** Tạo và cập nhật hồ sơ tài xế.
- **FR06:** Tạo và cập nhật thông tin phương tiện.
- **FR07:** Cập nhật trạng thái Sẵn sàng/Bận.
- **FR08:** Cập nhật khu vực hoạt động của tài xế.
## Đặt xe
- **FR09:** Nhập điểm đón.
- **FR10:** Nhập điểm đến.
- **FR11:** Chọn loại xe.
- **FR12:** Gửi yêu cầu đặt xe.
## Tìm tài xế
- **FR13:** Tìm tài xế đang ở trạng thái Sẵn sàng.
- **FR14:** Lọc tài xế theo loại phương tiện và khu vực.
- **FR15:** Gửi yêu cầu chuyến cho tài xế.
- **FR16:** Tài xế chấp nhận hoặc từ chối chuyến.
- **FR17:** Tìm tài xế khác khi tài xế từ chối.
- **FR18:** Thông báo khi không tìm được tài xế phù hợp.
## Quản lý chuyển đi
- **FR19:** Hiển thị thông tin tài xế đã nhận chuyến.
- **FR20:** Tài xế cập nhật trạng thái chuyến.
- **FR21:** Khách hàng xem trạng thái hiện tại của chuyến.
- **FR22:** Hoàn thành và lưu thông tin chuyến đi.
## Thanh toán
- **FR23:** Ghi nhận số tiền cước chuyến đi.
- **FR24:** Hiển thị số tiền khách hàng phải trả.
- **FR25:** Cho phép khách hàng chọn phương thức thanh toán.
- **FR26:** Ghi nhận thanh toán bằng tiền mặt.
- **FR27:** Gửi yêu cầu thanh toán điện tử.
- **FR28:** Ghi nhận kết quả thanh toán điện tử.
- **FR29:** Thông báo kết quả thanh toán cho khách hàng.
## Thông báo
- **FR30:** Tạo thông báo khi tài xế nhận chuyến.
- **FR31:** Tạo thông báo khi chuyến hoàn thành.
## Đánh giá
- **FR32:** Khách hàng gửi điểm đánh giá và nhận xét cho tài xế.
## Quản lý vận hành
- **FR33:** Quản lý thông tin khách hàng.
- **FR34:** Quản lý thông tin tài xế.
- **FR35:** Quản lý thông tin phương tiện.
- **FR36:** Xem và quản lý thông tin chuyến đi.
- **FR37:** Kiểm soát quyền truy cập chức năng quản trị.
## Báo cáo cơ bản
- **FR38:** Xem tổng số chuyến.
- **FR39:** Xem số chuyến đã hoàn thành.
- **FR40:** Xem tổng doanh thu.
# Bước 8: Business rule và exception(quy tắc nghiệp vụ và ngoại lệ)
## 1. Business Rules – Quy tắc nghiệp vụ
| Mã | Quy tắc nghiệp vụ | Diễn giải |
|---|---|---|
| BRU01 | Chỉ tài xế sẵn sàng mới được xét nhận chuyến | Hệ thống chỉ tìm tài xế có trạng thái Sẵn sàng. |
| BRU02 | Tài xế phải phù hợp với loại xe và khu vực | Loại phương tiện và khu vực hoạt động của tài xế phải phù hợp với yêu cầu chuyến. |
| BRU03 | Tìm tài xế khác khi tài xế từ chối | Nếu tài xế từ chối, hệ thống tiếp tục tìm tài xế phù hợp khác. |
| BRU04 | Một tài xế chỉ thực hiện một chuyến tại một thời điểm | Khi tài xế nhận chuyến, trạng thái được chuyển sang Bận. |
| BRU05 | Trạng thái chuyến phải được cập nhật theo trình tự | Đã đến điểm đón → Đã đón khách → Đang di chuyển → Hoàn thành. |
| BRU06 | Chỉ ghi nhận cước sau khi chuyến hoàn thành | Hệ thống ghi nhận cước khi chuyến ở trạng thái Hoàn thành. |
| BRU07 | Khách hàng được chọn phương thức thanh toán | Hệ thống hỗ trợ tiền mặt và thanh toán điện tử. |
| BRU08 | Không lưu thông tin thanh toán nhạy cảm | CAB System không lưu trực tiếp thông tin thẻ hoặc tài khoản thanh toán nhạy cảm. |
| BRU09 | Thanh toán phải gắn với chuyến đi | Mỗi bản ghi thanh toán phải thuộc về một chuyến cụ thể. |
| BRU10 | Người dùng phải được xác thực | Người dùng phải đăng nhập trước khi sử dụng chức năng yêu cầu tài khoản. |
| BRU11 | Chức năng quản trị phải được phân quyền | Chỉ nhân viên có quyền mới thực hiện chức năng quản trị. |
| BRU12 | Chỉ đánh giá chuyến đã hoàn thành | Khách hàng chỉ đánh giá tài xế sau khi chuyến hoàn thành. |
## 2. Exceptions – Ngoại lệ
| Mã | Ngoại lệ | Cách xử lý |
|---|---|---|
| EX01 | Thông tin đặt xe không hợp lệ | Hệ thống yêu cầu khách hàng kiểm tra và nhập lại. |
| EX02 | Tài xế từ chối chuyến | Hệ thống tiếp tục tìm tài xế phù hợp khác. |
| EX03 | Không tìm được tài xế | Hệ thống thông báo cho khách hàng. |
| EX04 | Cập nhật trạng thái chuyến không hợp lệ | Hệ thống từ chối cập nhật và thông báo cho tài xế. |
| EX05 | Thanh toán điện tử thất bại | Hệ thống ghi nhận trạng thái thất bại, thông báo cho khách hàng và cho phép thử lại. |
| EX06 | Người dùng không có quyền | Hệ thống từ chối truy cập chức năng quản trị. |

### Xác định các thực thể trong ERD
- **Khách hàng** (`customer_id`, `full_name`, `email`, `phone`, `password`, `address`)
- **Tài xế** (`driver_id`, `full_name`, `email`, `phone`, `password`, `status`, `service_area`)
- **Phương tiện** (`vehicle_id`, `driver_id`, `vehicle_type`, `license_plate`, `vehicle_name`)
- **Chuyến đi** (`trip_id`, `customer_id`, `driver_id`, `pickup_location`, `destination`, `pickup_area`, `vehicle_type`, `status`, `fare`, `start_time`, `end_time`)
- **Thanh toán** (`payment_id`, `trip_id`, `amount`, `payment_method`, `payment_status`, `payment_time`, `provider_transaction_id`)
- **Đánh giá** (`rating_id`, `trip_id`, `customer_id`, `driver_id`, `score`, `comment`)
- **Thông báo** (`notification_id`, `user_id`, `content`, `notification_type`, `status`, `created_at`)
- **Nhân viên vận hành** (`operator_id`, `full_name`, `email`, `password`, `role`)
- 
# Bước 10: Non functional requirement
## Non-Functional Requirements
| Mã | Tên | Diễn giải |
|---|---|---|
| NFR01 | Hiệu năng | Các chức năng thông thường phải phản hồi trong thời gian hợp lý. |
| NFR02 | Khả năng mở rộng | Hệ thống có thể phục vụ thêm khách hàng, tài xế và bổ sung chức năng trong tương lai. |
| NFR03 | Độ tin cậy | Dữ liệu tài khoản, chuyến đi và thanh toán phải được lưu chính xác. |
| NFR04 | Tính độc lập chức năng | Lỗi ở thanh toán hoặc thông báo không được làm toàn bộ chức năng đặt xe ngừng hoạt động. |
| NFR05 | Xác thực | Người dùng phải được xác thực trước khi sử dụng các chức năng yêu cầu tài khoản. |
| NFR06 | Phân quyền | Chức năng quản trị phải được kiểm soát quyền truy cập. |
| NFR07 | Bảo mật dữ liệu | Thông tin cá nhân, phương tiện và dữ liệu giao dịch phải được bảo vệ. |
| NFR08 | Bảo mật thanh toán | CAB System không lưu trực tiếp thông tin nhạy cảm của thẻ hoặc tài khoản thanh toán. |
| NFR09 | Khả năng bảo trì | Mã nguồn phải được tổ chức rõ ràng để dễ sửa đổi và bổ sung. |
# Bước 11: Vẽ use case
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/84806b90-0d8d-4977-a9bb-c81b46e08680" />
# Bước 12: Đặc tả Use Case

## UC01 – Quản lý tài khoản khách hàng

| Thuộc tính | Nội dung |
|---|---|
| **Mã Use Case** | UC01 |
| **Tên Use Case** | Quản lý tài khoản khách hàng |
| **Actor** | Khách hàng |
| **Mô tả** | Cho phép khách hàng đăng ký, đăng nhập, cập nhật thông tin cá nhân và xem lịch sử chuyến. |
| **Tiền điều kiện** | Khách hàng có kết nối với hệ thống. |
| **Hậu điều kiện** | Thông tin tài khoản hoặc lịch sử chuyến được hiển thị/cập nhật theo thao tác. |
| **Luồng chính** | 1. Khách hàng chọn chức năng tài khoản.<br>2. Hệ thống hiển thị chức năng phù hợp.<br>3. Khách hàng thực hiện đăng ký, đăng nhập, cập nhật thông tin hoặc xem lịch sử chuyến.<br>4. Hệ thống kiểm tra dữ liệu.<br>5. Hệ thống lưu hoặc hiển thị kết quả. |
| **Ngoại lệ** | Thông tin không hợp lệ hoặc thông tin đăng nhập sai → Hệ thống thông báo cho khách hàng. |

---

## UC02 – Đặt xe

| Thuộc tính | Nội dung |
|---|---|
| **Mã Use Case** | UC02 |
| **Tên Use Case** | Đặt xe |
| **Actor** | Khách hàng |
| **Mô tả** | Cho phép khách hàng tạo yêu cầu đặt xe. |
| **Tiền điều kiện** | Khách hàng đã đăng nhập. |
| **Hậu điều kiện** | Yêu cầu đặt xe được tạo với trạng thái Đang tìm tài xế. |
| **Luồng chính** | 1. Khách hàng nhập điểm đón.<br>2. Nhập điểm đến.<br>3. Chọn loại xe.<br>4. Gửi yêu cầu đặt xe.<br>5. Hệ thống kiểm tra thông tin.<br>6. Hệ thống tạo yêu cầu chuyến. |
| **Ngoại lệ** | Thông tin đặt xe không hợp lệ → Hệ thống yêu cầu nhập lại. |

---

## UC03 – Tìm và phân công tài xế

| Thuộc tính | Nội dung |
|---|---|
| **Mã Use Case** | UC03 |
| **Tên Use Case** | Tìm và phân công tài xế |
| **Actor** | Khách hàng, Tài xế |
| **Mô tả** | Tìm tài xế sẵn sàng, phù hợp loại phương tiện và khu vực cho yêu cầu đặt xe. |
| **Tiền điều kiện** | Yêu cầu đặt xe đã được tạo. |
| **Hậu điều kiện** | Tài xế được phân công hoặc khách hàng được thông báo không tìm được tài xế. |
| **Luồng chính** | 1. Hệ thống tìm tài xế có trạng thái Sẵn sàng.<br>2. Hệ thống lọc theo loại phương tiện và khu vực.<br>3. Hệ thống gửi yêu cầu chuyến cho tài xế.<br>4. Tài xế chấp nhận chuyến.<br>5. Hệ thống phân công tài xế cho chuyến.<br>6. Hệ thống chuyển tài xế sang trạng thái Bận.<br>7. Hệ thống hiển thị thông tin tài xế và tạo thông báo cho khách hàng. |
| **Luồng thay thế** | Tài xế từ chối → Hệ thống tiếp tục tìm tài xế phù hợp khác. |
| **Ngoại lệ** | Không còn tài xế phù hợp → Hệ thống thông báo cho khách hàng. |

---

## UC04 – Thực hiện chuyến đi

| Thuộc tính | Nội dung |
|---|---|
| **Mã Use Case** | UC04 |
| **Tên Use Case** | Thực hiện chuyến đi |
| **Actor** | Tài xế, Khách hàng |
| **Mô tả** | Cho phép tài xế cập nhật và khách hàng theo dõi trạng thái chuyến. |
| **Tiền điều kiện** | Tài xế đã nhận chuyến. |
| **Hậu điều kiện** | Chuyến được lưu ở trạng thái Hoàn thành và tài xế trở về trạng thái Sẵn sàng. |
| **Luồng chính** | 1. Tài xế cập nhật Đã đến điểm đón.<br>2. Tài xế cập nhật Đã đón khách.<br>3. Tài xế cập nhật Đang di chuyển.<br>4. Khách hàng xem trạng thái hiện tại.<br>5. Tài xế cập nhật Hoàn thành.<br>6. Hệ thống lưu chuyến và chuyển tài xế về Sẵn sàng.<br>7. Hệ thống tạo thông báo chuyến hoàn thành. |
| **Ngoại lệ** | Trạng thái cập nhật không hợp lệ → Hệ thống từ chối cập nhật. |

---

## UC05 – Thanh toán

| Thuộc tính | Nội dung |
|---|---|
| **Mã Use Case** | UC05 |
| **Tên Use Case** | Thanh toán |
| **Actor chính** | Khách hàng |
| **Actor phụ** | Nhà cung cấp thanh toán |
| **Mô tả** | Cho phép khách hàng thanh toán chuyến đi bằng tiền mặt hoặc thanh toán điện tử. |
| **Tiền điều kiện** | Chuyến đã hoàn thành và số tiền cước đã được ghi nhận. |
| **Hậu điều kiện** | Phương thức và kết quả thanh toán được lưu trong hệ thống. |
| **Luồng chính** | 1. Hệ thống hiển thị số tiền phải trả.<br>2. Khách hàng chọn phương thức thanh toán.<br>3. Khách hàng chọn thanh toán điện tử.<br>4. Hệ thống gửi yêu cầu đến nhà cung cấp thanh toán.<br>5. Nhà cung cấp thanh toán trả kết quả.<br>6. Hệ thống ghi nhận kết quả giao dịch.<br>7. Hệ thống thông báo kết quả cho khách hàng. |
| **Luồng thay thế** | Khách hàng chọn tiền mặt → Hệ thống ghi nhận phương thức tiền mặt và kết quả thanh toán. |
| **Ngoại lệ** | Thanh toán điện tử thất bại → Hệ thống ghi nhận trạng thái thất bại, thông báo cho khách hàng và cho phép thử lại. |

---

## UC06 – Đánh giá tài xế

| Thuộc tính | Nội dung |
|---|---|
| **Mã Use Case** | UC06 |
| **Tên Use Case** | Đánh giá tài xế |
| **Actor** | Khách hàng |
| **Mô tả** | Cho phép khách hàng gửi điểm và nhận xét cho tài xế sau chuyến. |
| **Tiền điều kiện** | Chuyến đã hoàn thành. |
| **Hậu điều kiện** | Đánh giá được lưu trong hệ thống. |
| **Luồng chính** | 1. Khách hàng chọn chuyến đã hoàn thành.<br>2. Nhập điểm đánh giá.<br>3. Nhập nhận xét.<br>4. Gửi đánh giá.<br>5. Hệ thống lưu đánh giá. |

---

## UC07 – Quản lý vận hành

| Thuộc tính | Nội dung |
|---|---|
| **Mã Use Case** | UC07 |
| **Tên Use Case** | Quản lý vận hành |
| **Actor** | Nhân viên vận hành |
| **Mô tả** | Cho phép nhân viên quản lý dữ liệu vận hành của CAB System. |
| **Tiền điều kiện** | Nhân viên đã đăng nhập và có quyền phù hợp. |
| **Hậu điều kiện** | Dữ liệu được hiển thị hoặc cập nhật theo thao tác hợp lệ. |
| **Luồng chính** | 1. Nhân viên chọn chức năng quản lý.<br>2. Quản lý thông tin khách hàng.<br>3. Quản lý thông tin tài xế.<br>4. Quản lý thông tin phương tiện.<br>5. Xem và quản lý thông tin chuyến đi. |
| **Ngoại lệ** | Nhân viên không có quyền → Hệ thống từ chối truy cập. |

---

## UC08 – Xem báo cáo cơ bản

| Thuộc tính | Nội dung |
|---|---|
| **Mã Use Case** | UC08 |
| **Tên Use Case** | Xem báo cáo cơ bản |
| **Actor** | Ban lãnh đạo / Người dùng có quyền |
| **Mô tả** | Cho phép xem các số liệu hoạt động cơ bản của CAB System. |
| **Tiền điều kiện** | Người dùng đã đăng nhập và có quyền xem báo cáo. |
| **Hậu điều kiện** | Báo cáo được hiển thị. |
| **Luồng chính** | 1. Người dùng chọn chức năng Báo cáo.<br>2. Hệ thống tổng hợp dữ liệu.<br>3. Hiển thị tổng số chuyến.<br>4. Hiển thị số chuyến đã hoàn thành.<br>5. Hiển thị tổng doanh thu. |
| **Ngoại lệ** | Người dùng không có quyền → Hệ thống từ chối truy cập. |

---

# Bước 13: Tiêu chí chấp nhận (Acceptance Criteria)- nhờ nó mới được nghiệm thu, cho biết khi nào dự án hoàn thành và được nghiệm thu
## Tiêu chí chấp nhận (Acceptance Criteria)
| Mã | Chức năng | Tiêu chí chấp nhận |
|---|---|---|
| AC01 | Quản lý tài khoản | Khách hàng có thể đăng ký, đăng nhập và cập nhật thông tin hợp lệ. |
| AC02 | Lịch sử chuyến | Khách hàng xem được các chuyến đã lưu của mình. |
| AC03 | Đặt xe | Khách hàng nhập được điểm đón, điểm đến, loại xe và gửi yêu cầu đặt xe. |
| AC04 | Tìm tài xế | Hệ thống tìm được tài xế Sẵn sàng, phù hợp loại phương tiện và khu vực. |
| AC05 | Phân công tài xế | Khi tài xế chấp nhận, hệ thống gán tài xế cho chuyến và chuyển tài xế sang Bận. |
| AC06 | Tài xế từ chối | Hệ thống tiếp tục tìm tài xế phù hợp khác. |
| AC07 | Không tìm được tài xế | Hệ thống thông báo rõ cho khách hàng. |
| AC08 | Theo dõi chuyến | Khách hàng xem được trạng thái hiện tại của chuyến. |
| AC09 | Cập nhật chuyến | Tài xế cập nhật được các trạng thái chuyến theo đúng trình tự. |
| AC10 | Hoàn thành chuyến | Hệ thống lưu chuyến hoàn thành và chuyển tài xế về Sẵn sàng. |
| AC11 | Cước chuyến | Hệ thống ghi nhận và hiển thị số tiền phải trả. |
| AC12 | Chọn phương thức thanh toán | Khách hàng chọn được tiền mặt hoặc thanh toán điện tử. |
| AC13 | Thanh toán tiền mặt | Hệ thống ghi nhận được thanh toán tiền mặt. |
| AC14 | Thanh toán điện tử | Hệ thống gửi yêu cầu thanh toán điện tử và ghi nhận kết quả trả về. |
| AC15 | Thanh toán thất bại | Hệ thống thông báo khi thanh toán điện tử thất bại và cho phép thử lại. |
| AC16 | Thông báo chuyến | Hệ thống tạo thông báo khi tài xế nhận chuyến và khi chuyến hoàn thành. |
| AC17 | Đánh giá | Khách hàng gửi được điểm và nhận xét cho tài xế sau chuyến hoàn thành. |
| AC18 | Quản lý vận hành | Nhân viên vận hành quản lý được khách hàng, tài xế, phương tiện và chuyến đi thuộc quyền. |
| AC19 | Phân quyền | Người dùng không có quyền không thể truy cập chức năng quản trị. |
| AC20 | Báo cáo | Người có quyền xem được tổng số chuyến, số chuyến hoàn thành và tổng doanh thu. |

# Bước 14: Truy xuất nguồn gốc yêu cầu (Traceability Requirements) - RTM (Ma trận truy xuất nguồn gốc yêu cầu)
## Truy xuất nguồn gốc yêu cầu
## Requirement Traceability Matrix (RTM)
| ID | Business Goal | Business Requirement | Functional Requirement | Use Case | Acceptance Criteria |
|---|---|---|---|---|---|
| RTM01 | BG02 | BR01 – Quản lý khách hàng | FR01–FR04 | UC01 – Quản lý tài khoản khách hàng | AC01–AC02 |
| RTM02 | BG03 | BR02 – Quản lý tài xế và phương tiện | FR05–FR08 | UC03, UC04, UC07 | AC04–AC05, AC09–AC10, AC18 |
| RTM03 | BG02 | BR03 – Quản lý đặt xe | FR09–FR12 | UC02 – Đặt xe | AC03 |
| RTM04 | BG01 | BR04 – Tìm và phân công tài xế | FR13–FR18 | UC03 – Tìm và phân công tài xế | AC04–AC07 |
| RTM05 | BG02 | BR05 – Quản lý chuyến đi | FR19–FR22 | UC04 – Thực hiện chuyến đi | AC08–AC10 |
| RTM06 | BG04 | BR06 – Quản lý thanh toán | FR23–FR29 | UC05 – Thanh toán | AC11–AC15 |
| RTM07 | BG02 | BR07 – Quản lý thông báo | FR30–FR31 | UC03, UC04 | AC16 |
| RTM08 | BG02 | BR08 – Đánh giá tài xế | FR32 | UC06 – Đánh giá tài xế | AC17 |
| RTM09 | BG03 | BR09 – Quản lý vận hành | FR33–FR37 | UC07 – Quản lý vận hành | AC18–AC19 |
| RTM10 | BG05 | BR10 – Báo cáo cơ bản | FR38–FR40 | UC08 – Xem báo cáo cơ bản | AC20 |
| RTM11 | BG06 | Khả năng mở rộng | NFR02, NFR09, NFR10 | Không áp dụng trực tiếp | Kiểm thử phi chức năng |
