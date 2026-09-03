TÀI LIỆU PHÂN TÍCH NGHIỆP VỤ
Dự án CAB System — Nền tảng đặt xe (Công ty ABC)
Thời gian xây dựng và triển khai sản phẩm: 7 tuần   |   Giai đoạn: Phân tích sơ khởi (Discovery)
B1–B2. Ngữ cảnh nghiệp vụ & Vấn đề nghiệp vụ
Doanh nghiệp: Công ty ABC cung cấp dịch vụ đặt xe trực tuyến.
Hiện trạng: Khách hàng đặt xe qua tổng đài hoặc một app đơn giản.
Vấn đề nghiệp vụ (Business Problem)
#	Vấn đề	Hệ quả
1	Phân công tài xế thủ công	Chậm, không tối ưu, khó mở rộng
2	Khách hàng không theo dõi được trạng thái chuyến đi	Trải nghiệm kém, tăng cuộc gọi hỗ trợ
3	Thông tin thanh toán không tập trung	Khó đối soát, khó báo cáo doanh thu
4	Vận hành khó mở rộng hệ thống hiện tại	Không đáp ứng được tăng trưởng
Mong muốn của Ban lãnh đạo: Một nền tảng CAB mới, phục vụ số lượng lớn khách hàng/tài xế, kiến trúc mở để phát triển tính năng trong tương lai.
B3. Mục tiêu nghiệp vụ (Business Objectives)
#	Mục tiêu	Loại
BO01	Tự động hóa việc tìm & phân công tài xế thay cho quy trình thủ công	Vận hành
BO02	Cho khách hàng theo dõi real-time trạng thái chuyến đi	Trải nghiệm khách hàng
BO03	Tập trung hóa dữ liệu thanh toán, tích hợp cổng thanh toán ngoài	Tài chính
BO04	Kiến trúc mở rộng độc lập theo từng thành phần	Kỹ thuật/Chiến lược
BO05	Cung cấp công cụ quản trị & báo cáo	Quản lý
BO06	Đảm bảo an toàn dữ liệu và có thể truy vết (audit)	Bảo mật/Tuân thủ
Lưu ý: các chỉ tiêu định lượng cụ thể (SLA, KPI...) chưa được khách hàng chốt — cần làm rõ trước khi sang bước tiếp theo.
B4. Phạm vi (Scope)
Trong phạm vi (In-scope)
●	Quản lý tài khoản Khách hàng, Tài xế, Nhân viên vận hành
●	Tạo yêu cầu đặt xe (điểm đón, điểm đến, loại xe)
●	Tìm kiếm & phân công tài xế, có cơ chế fallback khi từ chối/không phản hồi
●	Theo dõi trạng thái chuyến đi theo thời gian thực
●	Cập nhật vị trí tài xế
●	Tính cước & thanh toán (tiền mặt + cổng thanh toán điện tử bên thứ ba)
●	Thông báo đa sự kiện, kiến trúc mở rộng kênh
●	Giao diện quản trị: quản lý KH/tài xế/phương tiện/chuyến đi, phân quyền, tra cứu lịch sử
●	Báo cáo: số chuyến, doanh thu, tỷ lệ hoàn thành/hủy, hiệu quả tài xế
●	Đánh giá tài xế sau chuyến
●	Xác thực, phân quyền, bảo vệ dữ liệu, audit log
Ngoài phạm vi / chưa xác định (cần khách hàng chốt)
●	Công thức tính cước chi tiết
●	Tiêu chí ưu tiên tài xế cụ thể (thuật toán matching)
●	Thời gian tối đa tài xế phải phản hồi
●	Chính sách hủy chuyến
●	Cách xử lý khi mất kết nối mạng
●	Thời gian lưu trữ dữ liệu
●	Danh sách nhà cung cấp thanh toán ngoài cụ thể
⚠ Hành động bắt buộc trước khi sang B5: BA cần gặp lại khách hàng xác nhận scope trước khi chính thức chuyển sang đặc tả Business Requirements.
B5. Business Requirements (BR)
STT	Tên BR	Diễn giải
BR01	Đặt chuyến xe	Hệ thống cho phép khách hàng tạo yêu cầu đặt xe, cung cấp điểm đón và điểm đến, chọn loại xe
BR02	Tìm & phân công tài xế	Tự động xác định, đề xuất tài xế phù hợp theo vị trí/trạng thái; xử lý từ chối/không phản hồi bằng cách tìm tài xế khác mà không cần khách hàng tạo lại yêu cầu
BR03	Theo dõi chuyến đi thời gian thực	Cung cấp trạng thái cập nhật liên tục: đang tìm tài xế, đã nhận, ETA, đến điểm đón, di chuyển, hoàn thành
BR04	Quản lý hồ sơ tài xế & phương tiện	Tài xế đăng ký/được tạo tài khoản, cập nhật hồ sơ, phương tiện, trạng thái hoạt động
BR05	Tính cước & thanh toán	Tính tiền theo loại dịch vụ và dữ liệu chuyến; hỗ trợ tiền mặt & điện tử qua cổng ngoài; không lưu dữ liệu thẻ nhạy cảm
BR06	Thông báo đa kênh	Gửi thông báo tại các mốc sự kiện quan trọng; kiến trúc cho phép bổ sung kênh mới
BR07	Quản trị vận hành	Giao diện cho nhân viên quản lý KH/tài xế/phương tiện/chuyến đi, xử lý sự cố, tra cứu lịch sử, phân quyền
BR08	Báo cáo & thống kê	Số chuyến, doanh thu, tỷ lệ hoàn thành/hủy, hiệu quả tài xế
BR09	Đánh giá sau chuyến	Khách hàng xem lịch sử, số tiền đã trả, đánh giá tài xế
BR10	Bảo mật & xác thực	Xác thực người dùng, kiểm soát truy cập quản trị, bảo vệ dữ liệu, audit log
B6. Business Process (Quy trình nghiệp vụ chính)
Quy trình cốt lõi: Từ đặt xe đến hoàn thành chuyến (sơ đồ Mermaid — dán vào trình soạn thảo hỗ trợ Mermaid, ví dụ mermaid.live, để xem trực quan):
flowchart TD
    A[Khách hàng nhập điểm đón/điểm đến, chọn loại xe] --> B[Khách hàng gửi yêu cầu đặt xe]
    B --> C[Hệ thống tìm tài xế phù hợp gần khách hàng]
    C --> D{Tài xế có phản hồi trong thời gian quy định?}
    D -- Chấp nhận --> E[Tài xế được gán vào chuyến]
    D -- Từ chối/Không phản hồi --> F[Hệ thống tìm tài xế kế tiếp]
    F --> D
    D -- Không còn tài xế phù hợp --> G[Thông báo khách hàng: không tìm được tài xế]
    E --> H[Thông báo khách hàng: tài xế đã nhận chuyến + ETA]
    H --> I[Tài xế di chuyển đến điểm đón]
    I --> J[Tài xế cập nhật: đã đến điểm đón]
    J --> K[Tài xế cập nhật: đã đón khách]
    K --> L[Tài xế cập nhật: đang di chuyển]
    L --> M[Tài xế cập nhật: hoàn thành chuyến]
    M --> N[Hệ thống tính cước]
    N --> O{Phương thức thanh toán?}
    O -- Tiền mặt --> Q[Ghi nhận thanh toán tiền mặt]
    O -- Điện tử --> P[Gọi cổng thanh toán bên ngoài]
    P --> R{Giao dịch thành công?}
    R -- Có --> Q
    R -- Không --> S[Thông báo lỗi thanh toán, cho phép thử lại theo chính sách]
    S --> O
    Q --> T[Thông báo kết quả thanh toán cho khách hàng]
    T --> U[Khách hàng đánh giá tài xế]
 
Các quy trình phụ liên quan
●	Quy trình đăng ký/xác thực tài khoản (khách hàng, tài xế)
●	Quy trình tài xế chuyển trạng thái sẵn sàng nhận chuyến
●	Quy trình nhân viên vận hành xử lý chuyến bị lỗi
●	Quy trình tạo báo cáo định kỳ
B7. Phân rã Yêu cầu chức năng (FR)
BR	FR	Mô tả
BR01	FR01	Khách hàng nhập/chọn điểm đón, điểm đến
BR01	FR02	Khách hàng chọn loại xe, xem giá ước tính
BR01	FR03	Khách hàng gửi yêu cầu đặt xe
BR02	FR04	Xác định danh sách tài xế phù hợp theo vị trí & trạng thái
BR02	FR05	Gửi đề xuất chuyến, chờ phản hồi trong thời gian quy định
BR02	FR06	Tự động chuyển tài xế kế tiếp nếu bị từ chối/hết thời gian
BR02	FR07	Thông báo khách hàng khi không tìm được tài xế
BR03	FR08	Khách hàng xem trạng thái chuyến đi thời gian thực
BR03	FR09	Khách hàng xem vị trí tài xế & ETA
BR04	FR10	Tài xế đăng ký / nhân viên tạo tài khoản tài xế
BR04	FR11	Tài xế cập nhật hồ sơ & phương tiện
BR04	FR12	Tài xế chuyển trạng thái hoạt động
BR04	FR13	Ghi nhận vị trí tài xế thời gian thực
BR04	FR14	Tài xế cập nhật trạng thái chuyến
		
BR05	FR15	Tính cước theo loại dịch vụ & dữ liệu chuyến
BR05	FR16	Khách hàng chọn phương thức thanh toán
BR05	FR17	Gọi API cổng thanh toán bên thứ ba
BR05	FR18	Xử lý & thông báo khi giao dịch điện tử thất bại
BR06	FR19	Thông báo khách hàng tại các mốc sự kiện
BR06	FR20	Thông báo tài xế: chuyến mới, thay đổi liên quan
BR07	FR21	Nhân viên xem chuyến đang diễn ra & trạng thái tài xế
BR07	FR22	Nhân viên xử lý chuyến gặp sự cố
BR07	FR23	Nhân viên tra cứu lịch sử giao dịch/chuyến đi
BR07	FR24	Phân quyền chức năng quản trị theo vai trò
BR08	FR25	Xuất báo cáo thống kê
BR09	FR26	Khách hàng xem lịch sử chuyến & thanh toán
BR09	FR27	Khách hàng đánh giá tài xế
BR10	FR28	Xác thực khách hàng/tài xế
BR10	FR29	Ghi log audit trail
B8. Business Rules & Exception Handling
#	Loại	Quy tắc / Ngoại lệ	Xử lý
BRL01	Rule	Chỉ tài xế "sẵn sàng" mới được đề xuất chuyến	Loại tài xế bận/offline khỏi matching
BRL02	Exception	Tài xế không phản hồi trong thời gian quy định	Tự động chuyển tài xế tiếp theo, không yêu cầu KH tạo lại
BRL03	Exception	Không tìm được tài xế phù hợp	Thông báo rõ ràng cho KH, cho phép hủy/thử lại
BRL04	Rule	Không lưu trực tiếp dữ liệu thẻ/tài khoản nhạy cảm	Chỉ lưu token/tham chiếu giao dịch từ cổng ngoài
BRL05	Exception	Giao dịch điện tử thất bại	Thông báo KH, cho phép retry theo chính sách (cần làm rõ)
BRL06	Rule	Một số thao tác quản trị chỉ dành cho quyền cao hơn	Role-based access control
BRL07	Rule	Thao tác nhạy cảm phải được ghi log	Audit trail bắt buộc
BRL08	Exception	Lỗi phân hệ thanh toán/thông báo	Không được làm gián đoạn chức năng đặt xe cốt lõi
Open items cần Business Analyst làm rõ với khách hàng
●	Công thức/cách tính cước
●	Tiêu chí và thứ tự ưu tiên chọn tài xế
●	Thời gian tối đa tài xế phải phản hồi
●	Chính sách hủy chuyến
●	Cách xử lý khi mất kết nối mạng giữa chuyến
●	Thời gian lưu trữ dữ liệu (retention policy)
B9. Data Modeling (ERD sơ khởi)
Mô hình dữ liệu mức khái niệm (sơ đồ Mermaid ERD — dán vào mermaid.live để xem trực quan):
erDiagram
    CUSTOMER ||--o{ TRIP : requests
    DRIVER ||--o{ TRIP : fulfills
    DRIVER ||--|| VEHICLE : drives
    TRIP ||--|| PAYMENT : has
    TRIP ||--o| RATING : receives
    TRIP ||--o{ TRIP_STATUS_LOG : tracked_by
    DRIVER ||--o{ DRIVER_LOCATION : reports
    CUSTOMER ||--o{ NOTIFICATION : receives
    DRIVER ||--o{ NOTIFICATION : receives
    OPERATOR ||--o{ AUDIT_LOG : performs
    TRIP ||--o{ DRIVER_OFFER : generates_offers
    DRIVER ||--o{ DRIVER_OFFER : receives_offer
 
    CUSTOMER {
        string customer_id PK
        string full_name
        string phone
        string email
    }
    DRIVER {
        string driver_id PK
        string full_name
        string phone
        string status
    }
    VEHICLE {
        string vehicle_id PK
        string driver_id FK
        string plate_number
        string vehicle_type
    }
    TRIP {
        string trip_id PK
        string customer_id FK
        string driver_id FK
        string pickup_location
        string dropoff_location
        string status
    }
    DRIVER_OFFER {
        string offer_id PK
        string trip_id FK
        string driver_id FK
        string response
    }
    TRIP_STATUS_LOG {
        string log_id PK
        string trip_id FK
        string status
        datetime changed_at
    }
    DRIVER_LOCATION {
        string location_id PK
        string driver_id FK
        float latitude
        float longitude
    }
    PAYMENT {
        string payment_id PK
        string trip_id FK
        decimal amount
        string method
        string status
    }
    RATING {
        string rating_id PK
        string trip_id FK
        int score
    }
    NOTIFICATION {
        string notification_id PK
        string recipient_id
        string event_type
    }
    OPERATOR {
        string operator_id PK
        string full_name
        string role
    }
    AUDIT_LOG {
        string log_id PK
        string operator_id FK
        string action
    }
 
Đây là mô hình dữ liệu mức khái niệm, phục vụ phân tích — chưa phải thiết kế database vật lý.
B10. Non-Functional Requirements (NFR)
#	Nhóm	Yêu cầu
NFR01	Hiệu năng	Hoạt động ổn định vào thời điểm nhu cầu tăng cao (peak load)
NFR02	Scalability	Các thành phần mở rộng độc lập khi tải tăng
NFR03	Reliability	Lỗi thanh toán/thông báo không làm ngừng chức năng đặt xe
NFR04	Deployability	Triển khai tính năng mới từng phần, hạn chế ảnh hưởng
NFR05	Bảo mật	Xác thực bắt buộc; kiểm soát truy cập; bảo vệ dữ liệu cá nhân/vị trí/giao dịch
NFR06	Auditability	Lưu vết thao tác quan trọng phục vụ điều tra sự cố
NFR07	Extensibility	Bổ sung dịch vụ/thanh toán/kênh thông báo mới không viết lại hệ thống
NFR08	Tuân thủ	Không lưu dữ liệu thẻ nhạy cảm (cân nhắc PCI-DSS — cần xác nhận)
B11. Use Case Diagram
Sơ đồ use case (Mermaid — dán vào mermaid.live để xem trực quan):
graph TD
    Customer((Khách hàng))
    Driver((Tài xế))
    Operator((Nhân viên vận hành))
    PaymentGateway((Cổng thanh toán ngoài))
 
    Customer --> UC1[Đăng ký/Đăng nhập]
    Customer --> UC2[Đặt chuyến xe]
    Customer --> UC3[Theo dõi trạng thái chuyến đi]
    Customer --> UC4[Xem lịch sử & thanh toán]
    Customer --> UC5[Đánh giá tài xế]
 
    Driver --> UC1
    Driver --> UC6[Cập nhật hồ sơ & phương tiện]
    Driver --> UC7[Chuyển trạng thái sẵn sàng]
    Driver --> UC8[Nhận/Từ chối chuyến]
    Driver --> UC9[Cập nhật trạng thái chuyến đi]
 
    Operator --> UC1
    Operator --> UC10[Quản lý KH/Tài xế/Phương tiện]
    Operator --> UC11[Xử lý chuyến gặp sự cố]
    Operator --> UC12[Tra cứu lịch sử giao dịch]
    Operator --> UC13[Xem báo cáo thống kê]
 
    UC2 -.include.-> UC14[Tìm & phân công tài xế]
    UC9 -.include.-> UC15[Tính cước]
    UC15 -.include.-> UC16[Xử lý thanh toán]
    UC16 --> PaymentGateway
    UC2 -.include.-> UC17[Gửi thông báo]
    UC8 -.include.-> UC17
    UC9 -.include.-> UC17
    UC16 -.include.-> UC17
 
B12. Đặc tả Use Case (mẫu — 2 UC tiêu biểu)
UC02 — Đặt chuyến xe
Mục	Nội dung
Tác nhân chính	Khách hàng
Tác nhân phụ	Hệ thống matching (UC14)
Mô tả	Khách hàng tạo yêu cầu đặt xe với điểm đón, điểm đến và loại xe
Điều kiện tiên quyết	Khách hàng đã đăng nhập
Điều kiện kết thúc (thành công)	Yêu cầu được ghi nhận, chuyển sang bước tìm tài xế
Luồng chính	1. KH nhập điểm đón, điểm đến  2. Hệ thống hiển thị loại xe khả dụng & giá ước tính  3. KH chọn loại xe  4. KH xác nhận đặt xe  5. Hệ thống ghi nhận, chuyển trạng thái "đang tìm tài xế"  6. Thực hiện UC14
Luồng phụ	3a. Không có loại xe khả dụng tại khu vực → thông báo KH
Ngoại lệ	Mất kết nối khi gửi yêu cầu → cách xử lý cần làm rõ với khách hàng
UC14 — Tìm & phân công tài xế
Mục	Nội dung
Tác nhân chính	Hệ thống (tác vụ tự động)
Tác nhân phụ	Tài xế
Mô tả	Hệ thống xác định và đề xuất tài xế phù hợp cho một chuyến đi
Điều kiện tiên quyết	Có yêu cầu đặt xe hợp lệ ở trạng thái "đang tìm tài xế"
Điều kiện kết thúc (thành công)	Một tài xế được gán vào chuyến
Luồng chính	1. Lọc tài xế "sẵn sàng" gần điểm đón  2. Xếp hạng theo tiêu chí ưu tiên (cần làm rõ)  3. Gửi đề xuất tới tài xế cao nhất  4. Tài xế chấp nhận  5. Gán tài xế vào chuyến, cập nhật trạng thái, thông báo KH
Luồng phụ (E1)	Tài xế từ chối/không phản hồi → quay lại bước 2 với tài xế kế tiếp
Luồng phụ (E2)	Không còn tài xế phù hợp → thông báo KH, kết thúc UC ở trạng thái "không tìm được tài xế"
B13. Acceptance Criteria (AC) — mẫu theo BR02
●	AC1: Khi khách hàng gửi yêu cầu, hệ thống chỉ đề xuất chuyến cho tài xế đang "sẵn sàng"
●	AC2: Nếu tài xế không phản hồi trong thời gian quy định, hệ thống tự động chuyển đề xuất sang tài xế kế tiếp mà không cần khách hàng thao tác lại
●	AC3: Nếu không còn tài xế phù hợp, khách hàng nhận thông báo rõ ràng trong vòng X giây (ngưỡng cần xác nhận)
●	AC4: Toàn bộ các lần đề xuất/phản hồi của tài xế cho một chuyến được ghi log để tra cứu
Áp dụng khuôn mẫu tương tự cho từng BR/FR còn lại khi đặc tả chi tiết.
B14. Ma trận Truy xuất Nguồn gốc Yêu cầu (RTM — khung mẫu)
BR	FR	Use Case	Thiết kế	Test Case	Trạng thái
BR01	FR01–FR03	UC02			Chưa bắt đầu
BR02	FR04–FR07	UC14			Chưa bắt đầu
BR03	FR08–FR09	UC03			Chưa bắt đầu
BR04	FR10–FR14	UC06,UC07,UC09			Chưa bắt đầu
BR05	FR15–FR18	UC15,UC16			Chưa bắt đầu
BR06	FR19–FR20	UC17			Chưa bắt đầu
BR07	FR21–FR24	UC10,UC11,UC12			Chưa bắt đầu
BR08	FR25	UC13			Chưa bắt đầu
BR09	FR26–FR27	UC04,UC05			Chưa bắt đầu
BR10	FR28–FR29	UC01			Chưa bắt đầu
Tổng hợp: Vấn đề cần xác nhận với khách hàng trước khi sang thiết kế
●	Công thức tính cước cụ thể (theo km, thời gian, loại xe, giờ cao điểm...?)
●	Tiêu chí & thuật toán ưu tiên chọn tài xế
●	Thời gian chờ phản hồi tối đa của tài xế trước khi chuyển sang tài xế khác
●	Chính sách hủy chuyến (điều kiện, phí, ai được hủy)
●	Cách xử lý khi mất kết nối mạng giữa khách hàng/tài xế và hệ thống
●	Chính sách lưu trữ & thời gian lưu dữ liệu (đặc biệt vị trí, giao dịch)
●	Nhà cung cấp thanh toán ngoài dự kiến tích hợp (đánh giá tuân thủ, ví dụ PCI-DSS)
●	Các chỉ tiêu SLA/hiệu năng cụ thể (thời gian phản hồi, % uptime...)
