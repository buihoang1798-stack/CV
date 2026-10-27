# BÁO CÁO KIỂM THỬ

- **Dự án:** Portfolio CV cá nhân
- **Phiên bản:** v1.0
- **Ngày kiểm thử:** 27/10/2026
- **Phạm vi:** Kiểm tra thủ công trang tĩnh `index.html` trên trình duyệt tích hợp, tại giao diện desktop và mobile; kết hợp rà soát mã nguồn HTML/CSS.

## 1. Tính đúng đắn — Đạt một phần

- Trang mở được; tiêu đề trang và nội dung chính hiển thị.
- Kiểm tra trên trình duyệt: cả 4 thẻ dự án và 5 ảnh đều tải thành công; các liên kết điều hướng chính đều trỏ đến phần tử có thật.
- **Chưa đạt hoàn toàn:** Liên kết xem chi tiết dự án và GitHub/LinkedIn vẫn dùng `href="#"`; nội dung liên hệ là dữ liệu mẫu. Tên trong phần giới thiệu là Bùi Vũ Hoàng nhưng tên ở logo, metadata và mô tả ảnh vẫn là Nguyễn Văn An.

**Minh chứng:** [Giao diện desktop](screenshots/desktop.png), [khu vực dự án](screenshots/projects.png).

## 2. UI/UX — Đạt một phần

- Bố cục hiển thị ở cả desktop và mobile; lưới dự án lần lượt có 3 cột và 1 cột tại hai kích thước đã kiểm tra.
- Không phát hiện tràn ngang ở viewport desktop 1330 px và mobile 390 px. Có điều hướng chính, nút kêu gọi hành động, trạng thái focus bằng CSS và hỗ trợ `prefers-reduced-motion` trong mã nguồn.
- Đã kiểm tra trực quan qua ảnh chụp; chưa thực hiện đánh giá chính thức bằng công cụ tiếp cận hoặc thử nghiệm người dùng.

**Minh chứng:** [Giao diện desktop](screenshots/desktop.png), [giao diện mobile](screenshots/mobile.png).

## 3. Khả năng vận hành - xử lý lỗi — Đạt một phần

- Trang tĩnh mở trực tiếp trong trình duyệt; các ảnh đại diện và ảnh minh họa dự án đều tải trong lần kiểm tra.
- Dự án không có backend hoặc luồng xử lý dữ liệu động. Vì vậy, xử lý lỗi máy chủ/API và thông báo lỗi cho người dùng không áp dụng cho phiên bản hiện tại; chưa có kiểm thử lỗi mạng hoặc môi trường hosting thực tế.

**Minh chứng:** [Giao diện desktop](screenshots/desktop.png), [khu vực dự án](screenshots/projects.png).

## 4. Bảo mật — Đạt trong phạm vi rà soát cơ bản

- Rà soát mã nguồn tĩnh: trang không có biểu mẫu nhập liệu, mã JavaScript, backend hoặc thư viện bên thứ ba được nhúng; không thấy luồng xử lý dữ liệu người dùng trong phạm vi kiểm tra.
- Đây không phải kiểm thử xâm nhập hay đánh giá bảo mật chuyên sâu. Cần đánh giá cấu hình máy chủ và HTTPS riêng khi triển khai công khai.

**Minh chứng:** giao diện trang tĩnh trong [ảnh desktop](screenshots/desktop.png); kết quả rà soát được giới hạn ở `index.html` và `assets/css/styles.css`.

## 5. Chất lượng mã nguồn — Đạt một phần

- HTML dùng các vùng nội dung ngữ nghĩa; CSS được tách riêng, dùng biến giao diện, bố cục Flexbox/Grid và breakpoint responsive. Ảnh có văn bản thay thế.
- Cần đồng bộ tên và metadata giữa các phần; thay các liên kết mẫu bằng URL thật. Chưa chạy linter, kiểm tra tự động hoặc bộ kiểm thử mã nguồn.

**Minh chứng:** giao diện và nội dung trang trong [ảnh desktop](screenshots/desktop.png) và [ảnh khu vực dự án](screenshots/projects.png).

## 6. Khả năng triển khai — Đạt một phần

- Đây là website tĩnh gồm HTML, CSS và tài nguyên ảnh; không cần cài dependency hoặc chạy bước build theo cấu trúc hiện tại. Có thể phục vụ bằng web server tĩnh.
- Chưa triển khai lên hosting thực tế; repository hiện chưa có cấu hình CI/CD hoặc xác minh domain, HTTPS và đường dẫn tài nguyên sau triển khai.

**Minh chứng:** cấu trúc trang và tài nguyên hiển thị tại [ảnh desktop](screenshots/desktop.png) và [ảnh mobile](screenshots/mobile.png).

## Tổng kết

Phiên bản hiện tại phù hợp để xem thử như một portfolio tĩnh và đã thể hiện được bố cục responsive cơ bản. Trước khi phát hành công khai, cần cập nhật thông tin cá nhân và các liên kết còn là placeholder, sau đó kiểm thử lại trên hosting mục tiêu.