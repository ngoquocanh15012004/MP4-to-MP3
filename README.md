# Video to Audio Converter

Một ứng dụng web cho phép người dùng chuyển đổi các tệp video MP4 thành tệp âm thanh MP3. Ứng dụng có tính năng xác thực người dùng, cho phép người dùng xem lịch sử chuyển đổi và tải xuống các tệp đã chuyển đổi

![Ảnh](https://postimg.cc/V0qBMkRd)
## Tính năng

*   **Xác thực người dùng**: Đăng ký, đăng nhập và đăng xuất.
*   **Chuyển đổi MP4 sang MP3**: Tải lên tệp MP4 và chuyển đổi chúng thành định dạng MP3.
*   **Tải lên bằng cách kéo và thả**: Giao diện người dùng thân thiện để dễ dàng tải tệp lên.
*   **Xử lý không đồng bộ (5 files/lần)**: Các tệp được đưa vào hàng đợi và được xử lý ở chế độ nền bởi một máy chủ chuyển đổi riêng biệt.
*   **Lịch sử chuyển đổi**: Người dùng đã đăng nhập có thể xem lịch sử các tệp đã chuyển đổi của họ.
*   **Tải xuống tệp**: Tải xuống các tệp âm thanh đã được chuyển đổi.
## Cấu trúc dự án

```
├── src/main/java/            # Mã nguồn Java
│   ├── Controller/           # Servlets điều khiển luồng ứng dụng
│   ├── Model/                # Lớp Bean, BO (Business Objects), và DAO (Data Access Objects)
│   └── Server_2/             # Máy chủ socket độc lập để xử lý chuyển đổi
│
└── src/main/webapp/          # Tài nguyên web
    ├── CSS/                  # Tệp CSS
    ├── WEB-INF/              # Thư viện và cấu hình web (web.xml)
    └── *.jsp                 # Các trang JSP cho giao diện người dùng
```
## Công nghệ sử dụng

* ![Java](https://img.shields.io/badge/-Java-007396?logo=java&logoColor=fff&style=flat-square)
* ![HTML5](https://img.shields.io/badge/-HTML5-E34F26?logo=html5&logoColor=fff&style=flat-square)
* ![CSS3](https://img.shields.io/badge/-CSS3-1572B6?logo=css3&logoColor=fff&style=flat-square)
* ![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?logo=javascript&logoColor=000&style=flat-square)
* ![MySQL](https://img.shields.io/badge/-MySQL-4479A1?logo=mysql&logoColor=fff&style=flat-square)
* ![Apache Tomcat](https://img.shields.io/badge/-Apache%20Tomcat-F8DC75?logo=apachetomcat&logoColor=000&style=flat-square)
* ![FFmpeg](https://img.shields.io/badge/-FFmpeg-007808?logo=ffmpeg&logoColor=fff&style=flat-square)
* ![Socket.io](https://img.shields.io/badge/-Socket-010101?logo=socket.io&logoColor=fff&style=flat-square)

## Điều kiện tiên quyết

*   JDK 21 hoặc mới hơn
*   Apache Tomcat v9.0 hoặc mới hơn
*   Máy chủ MySQL
*   [FFmpeg](https://ffmpeg.org/download.html) được cài đặt và có thể truy cập được từ dòng lệnh (trong PATH của hệ thống).


## Cài đặt và Chạy dự án

1.  **Clone repository:**
    ```bash
    git clone https://github.com/ngoquocanh15012004/MP4-to-MP3.git
    ```

2.  **Thiết lập cơ sở dữ liệu:**
    *   Tạo một cơ sở dữ liệu MySQL có tên `dulieultm`.
    *   Thực thi các câu lệnh SQL sau để tạo các bảng cần thiết:

3.  **Chạy Máy chủ Chuyển đổi:**
    *   Biên dịch và chạy lớp Java `Server_2.ConvertServer`. Máy chủ này sẽ lắng nghe trên cổng `7749` để xử lý các yêu cầu chuyển đổi tệp.
    *   Máy chủ này sẽ tạo các thư mục `queues` và `results` trong thư mục gốc của dự án để quản lý các tệp.

4.  **Triển khai Ứng dụng Web:**
    *   Nhập dự án vào một IDE hỗ trợ Java Web như Eclipse.
    *   Triển khai ứng dụng `video2audio` lên máy chủ Apache Tomcat của bạn.

5.  **Truy cập Ứng dụng:**
    *   Mở trình duyệt web và điều hướng đến `http://localhost:8080/video2audio` (thay `8080` bằng cổng của máy chủ Tomcat nếu khác).


## Authors

- [@ngoquocanh](https://www.github.com/ngoquocanh15012004)

