# Portfolio CV - Hứa Đức Trung

## Giới thiệu

Website portfolio cá nhân giới thiệu Hứa Đức Trung, định hướng Frontend Developer. Trang trình bày phần giới thiệu, kỹ năng, một số dự án tiêu biểu và thông tin liên hệ. Giao diện được thiết kế responsive, ưu tiên trải nghiệm trên điện thoại và mở rộng cho máy tính bảng, máy tính để bàn.

## Chức năng

- Điều hướng đến các mục Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Trình bày thông tin cá nhân, kỹ năng và dự án dưới dạng lưới.
- Hiển thị ảnh đại diện và ảnh minh họa dự án.
- Bố cục thích ứng theo kích thước màn hình, có hiệu ứng cuộn đến mục và trạng thái tương tác cơ bản.
- Cung cấp liên kết email và hồ sơ mạng nghề nghiệp ở phần liên hệ.

## Công nghệ

- HTML5: cấu trúc nội dung và các vùng ngữ nghĩa.
- CSS3: giao diện, Flexbox, CSS Grid, biến CSS và media query responsive.
- Không dùng framework, thư viện JavaScript, trình đóng gói hay bước build.
- Nginx (tùy chọn): phục vụ trang tĩnh khi chạy bằng Docker.

## Yêu cầu môi trường

Để xem trang trực tiếp, chỉ cần trình duyệt web hiện đại. Không bắt buộc cài Node.js, npm hoặc Python.

Để chạy máy chủ phát triển cục bộ, cần cài Python 3. Để chạy bằng Docker, cần cài Docker Desktop (Windows/macOS) hoặc Docker Engine (Linux) và khởi động Docker trước khi chạy lệnh.

## Cài đặt

1. Tải hoặc sao chép toàn bộ thư mục dự án về máy; cần giữ nguyên cấu trúc `index.html`, `assets/css/` và `assets/img/`.
2. Mở thư mục dự án trong VS Code hoặc trình soạn thảo khác.
3. Có thể mở `index.html` trực tiếp bằng trình duyệt. Để kiểm tra qua HTTP, hãy chạy máy chủ theo hướng dẫn bên dưới.

Không cần cài thêm package hay chạy lệnh build.

## Cấu hình và tùy chỉnh

- Nội dung, tiêu đề, mô tả và thông tin liên hệ: chỉnh sửa trong `index.html`.
- Màu sắc, phông chữ, khoảng cách và chiều rộng bố cục: chỉnh các biến trong `:root` ở `assets/css/styles.css`.
- Breakpoint responsive hiện dùng 768px cho tablet và 1280px cho desktop.
- Ảnh nằm trong `assets/img/`. Khi thay ảnh, giữ nguyên đường dẫn tương ứng trong HTML hoặc cập nhật đường dẫn trong HTML theo tên file mới.
- Trước khi xuất bản, hãy thay email `duc.trung@example.com`, cập nhật URL GitHub/LinkedIn thực tế và kiểm tra các liên kết dự án đang để `#`.

## Chạy thử

### Windows

Mở PowerShell tại thư mục dự án rồi chạy:

```powershell
py -m http.server 8000
```

Nếu lệnh `py` không có trên máy, thử `python -m http.server 8000`. Mở <http://localhost:8000> trong trình duyệt. Nhấn `Ctrl+C` trong PowerShell để dừng máy chủ.

### macOS

Mở Terminal, chuyển đến thư mục dự án rồi chạy:

```bash
python3 -m http.server 8000
```

Mở <http://localhost:8000> trong trình duyệt. Nhấn `Control+C` để dừng máy chủ.

### Linux

Mở Terminal, chuyển đến thư mục dự án rồi chạy:

```bash
python3 -m http.server 8000
```

Mở <http://localhost:8000> trong trình duyệt. Nhấn `Ctrl+C` để dừng máy chủ.

### Docker

Cần Docker đang chạy. Lệnh bên dưới gắn thư mục dự án vào Nginx chỉ đọc; không cần tạo Dockerfile.

**Windows PowerShell** (chạy tại thư mục dự án):

```powershell
docker run --rm --name portfolio-web -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

**macOS/Linux** (chạy tại thư mục dự án):

```bash
docker run --rm --name portfolio-web -p 8080:80 -v "$(pwd):/usr/share/nginx/html:ro" nginx:alpine
```

Mở <http://localhost:8080>. Nhấn `Ctrl+C` trong cửa sổ đang chạy để dừng container. Nếu cổng 8080 đã được sử dụng, đổi phần `8080:80` thành một cổng trống khác, ví dụ `8081:80`, rồi mở cổng tương ứng trên trình duyệt.

## Thông tin liên hệ

- Tác giả: Hứa Đức Trung
- Email đang hiển thị trong trang: `duc.trung@example.com` (địa chỉ mẫu, cần thay bằng email thật trước khi công khai).
- GitHub: `github.com/huaductrung` (cần kiểm tra và cập nhật liên kết thật trong `index.html`).
- LinkedIn: `linkedin.com/in/huaductrung` (cần kiểm tra và cập nhật liên kết thật trong `index.html`)awfrdfaaww