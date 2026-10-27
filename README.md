 # Portfolio CV cá nhân

## Tên dự án

**Portfolio CV cá nhân – Bùi Vũ Hoàng**

## Mô tả

Website hồ sơ cá nhân dạng portfolio, giới thiệu thông tin, kỹ năng, các dự án tiêu biểu và kênh liên hệ. Giao diện được xây dựng theo hướng mobile-first, hiển thị phù hợp trên điện thoại, máy tính bảng và máy tính.

## Chức năng

- Điều hướng nhanh đến các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Trình bày phần giới thiệu, vai trò chuyên môn và ảnh đại diện.
- Hiển thị danh sách kỹ năng và các dự án mẫu.
- Cung cấp liên kết liên hệ qua email, GitHub và LinkedIn.
- Bố cục responsive: lưới dự án có 1 cột trên màn hình nhỏ, 2 cột từ 768px và 3 cột từ 1280px.
- Hỗ trợ điều hướng bằng bàn phím và tùy chọn giảm chuyển động của hệ điều hành.

Các liên kết chi tiết dự án hiện là liên kết mẫu; trang chưa có backend hoặc chức năng JavaScript.

## Công nghệ

- HTML5: cấu trúc nội dung ngữ nghĩa.
- CSS3: giao diện, responsive, Flexbox, CSS Grid và custom properties.
- Python 3 (tùy chọn): chạy máy chủ HTTP phục vụ trang tĩnh khi phát triển.
- Docker và Nginx (tùy chọn): chạy trang trong container để thử nghiệm.

Dự án không dùng framework, không cần Node.js/npm và không có bước build.

## Yêu cầu môi trường

- Trình duyệt hiện đại như Chrome, Firefox, Edge hoặc Safari.
- Một trong các hệ điều hành Windows, macOS hoặc Linux.
- Để chạy máy chủ phát triển: Python 3 đã được cài đặt. Có thể mở `index.html` trực tiếp, nhưng máy chủ HTTP giúp kiểm tra gần với môi trường triển khai hơn.
- Để chạy bằng container: Docker Engine; trên Windows hoặc macOS có thể dùng Docker Desktop.
- Không cần kết nối Internet để xem trang cơ bản sau khi đã có mã nguồn và tài nguyên ảnh.

## Cài đặt

1. Tải mã nguồn hoặc sao chép repository về máy.
2. Mở terminal tại thư mục dự án, nơi chứa `index.html`.
3. Kiểm tra cấu trúc tối thiểu sau:

```text
index.html
assets/
	css/
		styles.css
	img/
		avatar.jpg
```

Không cần cài dependency. Nếu tải về dưới dạng tệp ZIP, hãy giải nén trước khi chạy.

## Cấu hình và tùy chỉnh

- Sửa nội dung, tiêu đề trang, mô tả SEO, tên tác giả, thông tin liên hệ và liên kết dự án trong `index.html`.
- Đổi ảnh đại diện bằng cách thay `assets/img/avatar.jpg`, hoặc cập nhật đường dẫn ảnh trong `index.html` cho khớp với tên tệp mới.
- Chỉnh màu sắc, kích thước, khoảng cách và breakpoint responsive trong `assets/css/styles.css`.
- Thay các liên kết `href="#"` trong thẻ dự án và thông tin GitHub/LinkedIn bằng địa chỉ thật.
- Một số thông tin hiện là nội dung mẫu: phần metadata và mô tả ảnh còn tên Nguyễn Văn An, trong khi phần giới thiệu hiển thị Bùi Vũ Hoàng. Hãy cập nhật nhất quán trước khi xuất bản. Email `an.nguyen@example.com` cũng là địa chỉ ví dụ.

## Chạy thử

### Windows

Mở PowerShell tại thư mục dự án và chạy:

```powershell
py -m http.server 8000
```

Mở <http://localhost:8000> trong trình duyệt. Nếu lệnh `py` không có trên máy, cài Python 3 hoặc thử `python -m http.server 8000`.

### macOS

Mở Terminal tại thư mục dự án và chạy:

```bash
python3 -m http.server 8000
```

Mở <http://localhost:8000> trong trình duyệt.

### Linux

Mở terminal tại thư mục dự án và chạy:

```bash
python3 -m http.server 8000
```

Mở <http://localhost:8000> trong trình duyệt. Trên một số bản phân phối, cài Python 3 bằng trình quản lý gói của hệ điều hành nếu lệnh chưa có.

> **Dừng máy chủ:** nhấn `Ctrl+C` trong cửa sổ terminal đang chạy máy chủ.

### Chạy bằng Docker

Không cần tạo Dockerfile. Các lệnh dưới đây dùng image `nginx:alpine`, chia sẻ thư mục hiện tại vào web root của Nginx ở chế độ chỉ đọc và ánh xạ cổng máy chủ `8080` sang cổng container `80`. Chạy lệnh tại thư mục dự án.

**Windows PowerShell:**

```powershell
docker run --rm -d --name portfolio-cv -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

**macOS hoặc Linux:**

```bash
docker run --rm -d --name portfolio-cv -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

Mở <http://localhost:8080> để xem trang. Dừng container bằng:

```bash
docker stop portfolio-cv
```

Trên Windows, hãy bảo đảm Docker Desktop đang chạy và được cấp quyền chia sẻ ổ đĩa/thư mục chứa dự án nếu Docker yêu cầu.

## Thông tin liên hệ

Thông tin đang có trong trang là dữ liệu mẫu, vui lòng xác nhận hoặc thay bằng thông tin thật trước khi công khai:

- Email: `an.nguyen@example.com`
- GitHub: `github.com/nguyenvanan`
- LinkedIn: `linkedin.com/in/nguyenvanan`

Các địa chỉ trên được khai báo trong `index.html`.
