# Báo cáo kiểm thử

## Thông tin kiểm thử

- Dự án: Portfolio CV - Hứa Đức Trung
- Ngày kiểm thử: 2026-10-27
- Phạm vi: kiểm tra thủ công trang tĩnh `index.html` trên trình duyệt Chromium tích hợp, mở từ file local.
- Kích thước viewport đã kiểm tra: desktop 1350px và mobile 375px (chiều rộng CSS viewport).
- Tổng quan: **Chưa đạt để phát hành**. Trang hiển thị được và các luồng điều hướng cơ bản hoạt động, nhưng có lỗi cấu trúc HTML ở thẻ dự án Weather Dashboard và nhiều liên kết chưa có đích thật.

## Kết quả theo tiêu chí

### 1. Tính đúng đắn - Chưa đạt

- Tiêu đề trang, phần giới thiệu, kỹ năng và liên hệ hiển thị; bấm mục “Kỹ năng” chuyển đúng đến `#skills`.
- 5/5 ảnh trong tài liệu tải được tại thời điểm kiểm tra.
- Thẻ ảnh của Weather Dashboard thiếu dấu `>` kết thúc. Trình duyệt vẫn hiển thị ảnh nhưng cấu trúc DOM của thẻ dự án bị sai; thẻ blog nằm ngoài lưới dự án.
- Văn bản thay thế của ảnh đại diện ghi “Nguyễn Văn An”, không khớp tên đang hiển thị “Hứa Đức Trung”.

### 2. UI/UX - Đạt một phần

- Bố cục thay đổi theo breakpoint; CSS định nghĩa lưới 3 cột từ 1280px, 2 cột từ 768px và 1 cột trên màn hình nhỏ.
- Kiểm tra ở viewport 1350px và 375px không phát hiện tràn ngang. Menu nội trang và nút gọi hành động hiển thị.
- Cấu trúc thẻ dự án sai làm phần dự án thiếu nhất quán; menu có thể xuống dòng trên màn hình hẹp. Liên kết hồ sơ và nút xem dự án chưa dẫn đến trang đích.
- Ảnh chụp: [Desktop](screenshots/desktop.png), [Mobile](screenshots/mobile.png), [Khu vực dự án](screenshots/projects_desktop.png).

### 3. Khả năng vận hành - xử lý lỗi - Đạt một phần

- Trang mở trực tiếp từ file local; điều hướng nội trang đến `#skills` hoạt động.
- Không phát hiện tràn ngang ở hai kích thước đã kiểm tra; tất cả ảnh được tham chiếu đều tải thành công trong lần chạy này.
- Có 6 liên kết `href="#"` không dẫn đến nội dung hoặc trang thật. Chưa có xử lý trạng thái lỗi, tải dữ liệu API hoặc kiểm thử gửi biểu mẫu; đây là website tĩnh.

### 4. Bảo mật - Đạt trong phạm vi kiểm tra tĩnh

- Trang không có biểu mẫu nhập liệu, mã JavaScript ứng dụng, tài khoản, xử lý phiên hoặc backend; bề mặt tấn công phía ứng dụng hiện thấp.
- Đây không phải kiểm thử xâm nhập hay rà quét phụ thuộc. Chưa kiểm tra cấu hình HTTPS, header bảo mật, máy chủ lưu trữ hoặc rủi ro phát sinh khi tích hợp dịch vụ bên ngoài.

### 5. Chất lượng mã nguồn - Chưa đạt

- HTML có các vùng ngữ nghĩa như `header`, `nav`, `main`, `section`, `article`, `footer`; CSS được chia theo khu vực và dùng biến, Flexbox, Grid, media query.
- Lỗi thẻ `<img>` Weather Dashboard làm sai cấu trúc DOM. Alt ảnh đại diện không khớp tên; ảnh dự án đầu tiên có `alt` rỗng; tên dự án và mô tả một số thẻ cần được rà soát.
- README mô tả Todo App và Weather Dashboard như sản phẩm có chức năng, nhưng mã hiện tại chỉ hiển thị nội dung tĩnh; chưa thấy mã gọi API hoặc logic ứng dụng.

### 6. Khả năng triển khai - Đạt một phần

- Đây là website tĩnh, không cần cài package hay build; có thể phục vụ bằng máy chủ tĩnh. README có hướng dẫn cho Windows, macOS, Linux và Docker/Nginx.
- Đã kiểm tra cách mở file local; chưa chạy thử container Docker, chưa kiểm tra triển khai trên hosting/HTTPS và chưa có pipeline CI/CD.
- Trước khi phát hành cần sửa HTML, thay email mẫu và cập nhật các liên kết `#`.

## Minh chứng

- [Ảnh giao diện desktop](screenshots/desktop.png)
- [Ảnh giao diện mobile](screenshots/mobile.png)
- [Ảnh khu vực dự án](screenshots/projects_desktop.png)

Ảnh được chụp trực tiếp từ trang local trong quá trình kiểm thử ngày 2026-10-27. Kết quả chỉ phản ánh phạm vi và môi trường nêu ở trên; chưa thay thế cho kiểm thử trên nhiều trình duyệt, kiểm thử tự động hoặc đánh giá bảo mật chuyên sâu.
