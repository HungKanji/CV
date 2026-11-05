# 🧪 BÁO CÁO KIỂM THỬ PHẦN MỀM (TEST REPORT)

* **Tên dự án:** Cyber Portfolio & Personal CV — Phạm Quốc Hùng (`@HùngKanji`)

* **Mã bài kiểm tra:** A2.1 (`KT20A2.1`)

* **Phiên bản kiểm thử:** `v1.0.0`

* **Ngày thực hiện:** `05/11/2026`

* **Người thực hiện:** Phạm Quốc Hùng

* **Phương pháp kiểm thử:** Kết hợp kiểm thử trực quan trên Chrome/Firefox DevTools và đo kiểm tự động bằng trình duyệt Chromium Headless (đo `document.documentElement.scrollWidth` và số cột lưới `.card`).

* **Thư mục lưu trữ minh chứng:** `docs/screenshots/`

## TỔNG QUAN KẾT QUẢ ĐÁNH GIÁ 6 TIÊU CHÍ

| STT | Tiêu chí đánh giá | Số ca kiểm thử | Kết quả | Mức độ đáp ứng | 
| ----- | ----- | ----- | ----- | ----- | 
| **1** | **Tính đúng đắn (Correctness)** | 5 | 5/5 Đạt | **100% (Đạt)** | 
| **2** | **Giao diện & Trải nghiệm người dùng (UI/UX)** | 7 | 7/7 Đạt | **100% (Đạt)** | 
| **3** | **Khả năng vận hành & Xử lý lỗi (Operations & Error Handling)** | 4 | 4/4 Đạt | **100% (Đạt)** | 
| **4** | **Bảo mật (Security)** | 4 | 4/4 Đạt | **100% (Đạt)** | 
| **5** | **Chất lượng mã nguồn (Code Quality)** | 4 | 4/4 Đạt | **100% (Đạt)** | 
| **6** | **Khả năng triển khai (Deployability)** | 4 | 4/4 Đạt | **100% (Đạt)** | 

## 1. TIÊU CHÍ 1: TÍNH ĐÚNG ĐẮN (CORRECTNESS)

### 1.1. Mục tiêu đánh giá

Đảm bảo trang web hiển thị đầy đủ 5 khối nội dung bắt buộc theo yêu cầu đề bài (`AC-01`), các liên kết điều hướng hoạt động chính xác (`AC-05`), và toàn bộ tính năng tương tác JavaScript vận hành đúng logic thiết kế.

### 1.2. Bảng kết quả kiểm thử chi tiết

| Mã TC | Hạng mục kiểm thử | Các bước thực hiện | Kết quả kỳ vọng | Kết quả thực tế | Trạng thái | 
| ----- | ----- | ----- | ----- | ----- | ----- | 
| **COR-01** | Kiểm tra đầy đủ 5 khối nội dung (`AC-01`) | Mở `index.html`, rà soát từ đầu đến cuối trang. | Hiển thị đủ 5 khối: Nhận diện/Giới thiệu (`#about`), Điều hướng (`nav`), Kỹ năng (`#skills`), Dự án (`#projects`), Liên hệ (`#contact`). | Hiển thị đầy đủ 5 khối kèm thông tin cá nhân của Phạm Quốc Hùng, 6 kỹ năng, 4 dự án và form liên hệ. | ✅ Đạt | 
| **COR-02** | Kiểm tra điều hướng nội trang (`AC-05`) | Nhấp lần lượt vào 4 liên kết `Giới thiệu`, `Kỹ năng`, `Dự án`, `Liên hệ` trên thanh `<nav>`. | Trang cuộn mượt (`smooth scroll`) tới đúng `id` của từng `<section>` tương ứng. | Cả 4 liên kết và 2 nút CTA (`Khám phá dự án`, `Liên hệ ngay`) đều cuộn chính xác tới khối đích. | ✅ Đạt | 
| **COR-03** | Kiểm tra bộ chuyển đổi 3 chủ đề (`Theme Toggle`) | Nhấn liên tiếp vào nút `#themeToggle` trên thanh Header. | Thuộc tính `data-theme` trên `<body>` đổi tuần tự: `blackpink` → `aincrad` → `valorant` và cập nhật nhãn nút. | Đổi màu toàn trang tức thời qua 3 chủ đề (`Neon·Cyber`, `Aincrad·SAO`, `Jett·Radiant`) không lỗi. | ✅ Đạt | 
| **COR-04** | Kiểm tra hiệu ứng gõ chữ tự động (`Typewriter`) | Quan sát dòng chức danh `#typewriter` tại khu vực Hero trong 15 giây. | Tự động gõ và xóa luân phiên 3 chuỗi chức danh đã cấu hình. | Chạy mượt mà, đúng tốc độ gõ `55ms` và xóa `30ms`, lặp vô hạn không bị treo. | ✅ Đạt | 
| **COR-05** | Kiểm tra liên kết mạng xã hội & Email | Kiểm tra các nút liên kết trong `.social-bar`. | Chứa đúng liên kết `mailto:hungkanji01@gmail.com`, GitHub và LinkedIn cá nhân. | Hoạt động đúng, mở tab mới cho liên kết ngoài và gọi ứng dụng mail cho địa chỉ email. | ✅ Đạt | 

### 1.3. Minh chứng hình ảnh

> *Hình 1.1: Minh chứng hiển thị đầy đủ các khối nội dung và hoạt động của bộ chuyển đổi 3 chủ đề màu (`docs/screenshots/theme-switcher.png`).*

## 2. TIÊU CHÍ 2: GIAO DIỆN & TRẢI NGHIỆM NGƯỜI DÙNG (UI/UX)

### 2.1. Mục tiêu đánh giá

Kiểm chứng thiết kế đáp ứng (**Responsive Design**) theo tư duy **Mobile-First** trên 3 breakpoint chính (`360px`, `768px`, `1280px`) và các viewport phụ (`375px`, `1024px`), cam kết **không xuất hiện thanh cuộn ngang** (`AC-02`, `AC-03`, `AC-07`) và đảm bảo khả năng tiếp cận cơ bản (`AC-06`).

### 2.2. Ma trận đo kiểm Responsive thực tế (Viewport Matrix)

| Mã TC | Breakpoint & Thiết bị | Hạng mục kiểm tra | Kết quả kỳ vọng | Kết quả đo thực tế (SAU) | Trạng thái | 
| ----- | ----- | ----- | ----- | ----- | ----- | 
| **UI-01 (TC-01)** | **360px** · Android nhỏ | Kiểm tra tràn ngang (`Overflow-X`) | `scrollWidth <= 360px`, không có thanh cuộn ngang | `scrollWidth = 360px`, không cuộn ngang | ✅ Đạt | 
| **UI-02 (TC-02)** | **360px** · Android nhỏ | Thanh điều hướng (`nav`) & Hero | `nav` tự wrap đủ 4 mục; Hero xếp 1 cột dọc, ảnh vừa khung | `nav` wrap gọn, Hero 1 cột, ảnh không tràn | ✅ Đạt | 
| **UI-03 (TC-04)** | **360px** · Android nhỏ | Lưới dự án (`.project-grid`) | Hiển thị 1 cột dọc duy nhất | Đo thực tế: **1 cột** | ✅ Đạt | 
| **UI-04 (TC-05)** | **375px** · iPhone SE | Lề trang & Cỡ chữ iOS | Lề đều hai bên, chữ không bị iOS tự ý phóng to | Đạt chuẩn nhờ `text-size-adjust` & `clamp()` | ✅ Đạt | 
| **UI-05 (TC-06/07/08)** | **768px** · iPad dọc | Bố cục Tablet & Overflow ngang | Hero chuyển 2 cột (`text | avatar`); Lưới dự án 2 cột; `scrollWidth <= 768px` | Hero 2 cột, Lưới dự án **2 cột**, `scrollWidth = 768px` | ✅ Đạt | 
| **UI-06 (TC-10/11)** | **1280px** · Laptop/Desktop | Bố cục Desktop & Container | Container căn giữa (`max-width: 1180px/1200px`), lưới dự án mở rộng 2–3 cột cân đối | Căn giữa chuẩn xác, `scrollWidth = 1280px`, không lỗi lệch khối | ✅ Đạt | 
| **UI-07 (TC-12)** | **Mọi breakpoint** | Khả năng tiếp cận (`Accessibility`) & Zoom 200% | 100% thẻ `<img>` có `alt`; thấy rõ viền focus khi nhấn `Tab`; Zoom 200% không vỡ giao diện | Đạt toàn bộ tiêu chí `AC-06` | ✅ Đạt | 

### 2.3. Minh chứng hình ảnh theo từng Breakpoint

> *Hình 2.1: Minh chứng hiển thị tại Breakpoint **360px (Mobile)** — bố cục xếp dọc 1 cột, thanh điều hướng tự xuống dòng, hoàn toàn không có thanh cuộn ngang (`docs/screenshots/viewport-360px.png`).*

> *Hình 2.2: Minh chứng hiển thị tại Breakpoint **768px (Tablet)** — khối Hero chia 2 cột trực quan, danh sách dự án chia 2 cột đồng đều (`docs/screenshots/viewport-768px.png`).*

> *Hình 2.3: Minh chứng hiển thị tại Breakpoint **1280px (Desktop)** — không gian hiển thị rộng rãi, căn giữa trong container chuẩn và hiệu ứng Cyber Neon sắc nét (`docs/screenshots/viewport-1280px.png`).*

## 3. TIÊU CHÍ 3: KHẢ NĂNG VẬN HÀNH & XỬ LÝ LỖI (OPERATIONS & ERROR HANDLING)

### 3.1. Mục tiêu đánh giá

Kiểm tra độ ổn định của ứng dụng trong quá trình vận hành liên tục, khả năng bắt lỗi dữ liệu đầu vào tại biểu mẫu liên hệ, khả năng tự thích ứng khi thay đổi kích thước cửa sổ đột ngột và kiểm tra bảng điều khiển (Browser Console).

### 3.2. Bảng kết quả kiểm thử chi tiết

| Mã TC | Tình huống kiểm thử | Cách thức thực hiện | Kết quả kỳ vọng | Kết quả thực tế | Trạng thái | 
| ----- | ----- | ----- | ----- | ----- | ----- | 
| **OPS-01** | Kiểm tra lỗi Runtime trên Browser Console | Mở trang trên Chrome & Firefox, mở DevTools Console (`F12`), thao tác cuộn trang, đổi theme, di chuột. | `0 Errors`, `0 Uncaught Exceptions` trên Console. | Hoàn toàn sạch lỗi (`0 lỗi đỏ` trên Console). | ✅ Đạt | 
| **OPS-02** | Kiểm tra bắt lỗi biểu mẫu liên hệ (Form Validation) | Bỏ trống các ô *Họ tên*, *Email*, *Tin nhắn* hoặc nhập email sai định dạng (vd: `hungkanji`) rồi bấm **Gửi tin nhắn**. | Trình duyệt chặn hành vi gửi form, hiển thị thông báo nhắc lỗi tại trường bị thiếu/sai và tô viền hồng (`:focus`). | Chặn gửi form chính xác nhờ thuộc tính `required` và `type="email"`. | ✅ Đạt | 
| **OPS-03** | Xử lý sự kiện thay đổi kích thước màn hình liên tục (`window.resize`) | Kéo co giãn cửa sổ trình duyệt liên tục từ `1920px` xuống `360px` và ngược lại. | Hàm `resize()` của `#cyberCanvas` tự động cập nhật lại `width`/`height`, hạt năng lượng không bị méo hoặc tràn khung. | Canvas tự tính toán lại kích thước tức thời, tốc độ khung hình giữ ổn định ở `60 FPS`. | ✅ Đạt | 
| **OPS-04** | Khả năng chịu lỗi khi ảnh tải chậm hoặc mất kết nối ảnh | Giả lập chặn tải 1 file ảnh trong DevTools Network. | Khung thẻ dự án (`.card-media-box`) giữ nguyên chiều cao `230px` nền tối `#101020` và hiển thị văn bản `alt`, không làm sập bố cục thẻ. | Bố cục thẻ dự án và khung Avatar giữ nguyên kích thước, hiển thị rõ nội dung `alt`. | ✅ Đạt | 

### 3.3. Minh chứng hình ảnh

> *Hình 3.1: Minh chứng cơ chế kiểm tra dữ liệu đầu vào tại Form Liên hệ và bảng Console không có lỗi Runtime (`docs/screenshots/form-validation.png`).*

## 4. TIÊU CHÍ 4: BẢO MẬT (SECURITY)

### 4.1. Mục tiêu đánh giá

Đảm bảo trang web tuân thủ các nguyên tắc an toàn thông tin phía Client (Frontend Security): chống tấn công Tabnabbing khi mở liên kết ngoài, ngăn chặn nguy cơ XSS (Cross-Site Scripting), không lộ thông tin nhạy cảm trong mã nguồn và sử dụng kênh truyền an toàn HTTPS cho tài nguyên bên thứ ba.

### 4.2. Bảng kết quả kiểm thử chi tiết

| Mã TC | Hạng mục bảo mật | Nội dung kiểm tra trên mã nguồn | Kết quả kỳ vọng | Kết quả thực tế | Trạng thái | 
| ----- | ----- | ----- | ----- | ----- | ----- | 
| **SEC-01** | Chống tấn công Reverse Tabnabbing | Kiểm tra các thẻ `<a target="_blank">` dẫn tới GitHub và LinkedIn. | Bắt buộc đi kèm thuộc tính `rel="noopener"` (hoặc `noreferrer`) để ngăn trang đích truy cập `window.opener`. | Đã khai báo đầy đủ `target="_blank" rel="noopener"` tại dòng `787–788` trong `index.html`. | ✅ Đạt | 
| **SEC-02** | Phòng chống lỗ hổng DOM-based XSS | Rà soát toàn bộ đoạn mã JavaScript trong `<script>`. | Không sử dụng `eval()`, `document.write()`, hoặc gán dữ liệu người dùng vào `innerHTML`. | Chỉ sử dụng `textContent` và `setAttribute('data-theme', ...)` với mảng hằng số cố định, an toàn tuyệt đối trước XSS. | ✅ Đạt | 
| **SEC-03** | Kiểm tra rò rỉ dữ liệu nhạy cảm (Secret/Token Leak) | Quét mã nguồn `index.html` và `styles.css`. | Không chứa API Key, mật khẩu, token cá nhân hoặc đường dẫn cục bộ nhạy cảm. | Chỉ chứa thông tin liên hệ công khai phục vụ tuyển dụng (Email, GitHub, LinkedIn). | ✅ Đạt | 
| **SEC-04** | Bảo mật kết nối tài nguyên bên ngoài (HTTPS CDN) | Kiểm tra các thẻ `<link>` tải Google Fonts và FontAwesome. | 100% tài nguyên ngoại vi sử dụng giao thức `https://` để tránh lỗi Mixed Content. | Toàn bộ liên kết CDN (`fonts.googleapis.com`, `cdnjs.cloudflare.com`) đều dùng chuẩn `https://`. | ✅ Đạt | 

### 4.3. Minh chứng hình ảnh

> *Hình 4.1: Minh chứng kiểm tra thuộc tính `rel="noopener"` trên các liên kết mở tab mới và kết nối HTTPS an toàn (`docs/screenshots/security-audit.png`).*

## 5. TIÊU CHÍ 5: CHẤT LƯỢNG MÃ NGUỒN (CODE QUALITY)

### 5.1. Mục tiêu đánh giá

Đánh giá mức độ tuân thủ chuẩn W3C HTML5 ngữ nghĩa (`AC-04`), tính rõ ràng và khả năng bảo trì của hệ thống CSS3 (Design Tokens, chuẩn hóa Box Model), cũng như cấu trúc tổ chức mã nguồn JavaScript.

### 5.2. Bảng kết quả kiểm thử chi tiết

| Mã TC | Hạng mục đánh giá | Tiêu chuẩn kiểm tra | Kết quả kỳ vọng | Kết quả thực tế | Trạng thái | 
| ----- | ----- | ----- | ----- | ----- | ----- | 
| **CDQ-01** | Kiểm định HTML5 Ngữ nghĩa & W3C Validator (`AC-04`) | Kiểm tra mã nguồn qua công cụ `validator.w3.org`. | Sử dụng đúng `<header>`, `<nav>`, `<main>` (duy nhất 1 thẻ), `<section>`, `<article>`, `<figure>`, `<footer>`; không có lỗi cú pháp đỏ. | Cấu trúc phân cấp thẻ chuẩn xác, có chú thích rõ ràng từng phân khu, đạt chuẩn W3C HTML5. | ✅ Đạt | 
| **CDQ-02** | Kiến trúc CSS3 & Design Tokens | Kiểm tra cách tổ chức biến và quy tắc CSS. | Khai báo biến màu/bố cục tập trung tại `:root`; chuẩn hóa `box-sizing: border-box`; tách biệt rõ style theo từng thành phần. | Sử dụng hệ thống biến CSS nhất quán (`--bg-deep`, `--pink`, `--cyan`, `--skill-color`, `--card-accent`), dễ dàng mở rộng thêm theme mới. | ✅ Đạt | 
| **CDQ-03** | Chất lượng mã JavaScript | Đánh giá cú pháp và hiệu năng tập lệnh. | Sử dụng cú pháp ES6+ (`const`, `let`, Arrow Function, Template Literals), chia thành 3 module độc lập có chú thích rõ ràng. | Mã JS gọn nhẹ (\~80 dòng), chia rõ 3 phần: *Đổi Theme*, *Typewriter*, *Canvas Laser*, không phụ thuộc thư viện ngoài nặng nề. | ✅ Đạt | 
| **CDQ-04** | Tối ưu hóa Hình ảnh & Thuộc tính Đa phương tiện | Kiểm tra các thẻ `<img>` trong tài liệu. | Khai báo rõ `width`, `height` (chống hiện tượng Cumulative Layout Shift - CLS) và thuộc tính `alt` mô tả đầy đủ. | Các ảnh đại diện và ảnh dự án đều có `width`, `height`, `object-fit: cover` và văn bản `alt` tiếng Việt rõ nghĩa. | ✅ Đạt | 

### 5.3. Minh chứng hình ảnh

> *Hình 5.1: Minh chứng kiểm tra chất lượng mã nguồn HTML5 ngữ nghĩa không có lỗi cú pháp (`docs/screenshots/html-validation.png`).*

## 6. TIÊU CHÍ 6: KHẢ NĂNG TRIỂN KHAI (DEPLOYABILITY)

### 6.1. Mục tiêu đánh giá

Đảm bảo dự án có tính khả chuyển cao (Portability), sử dụng đường dẫn tương đối chuẩn xác để chạy mượt mà trên mọi môi trường (Windows, macOS, Linux, Docker Container, GitHub Pages / Vercel / Netlify) mà không cần bước biên dịch phức tạp.

### 6.2. Bảng kết quả kiểm thử chi tiết

| Mã TC | Môi trường triển khai | Nội dung kiểm thử | Kết quả kỳ vọng | Kết quả thực tế | Trạng thái | 
| ----- | ----- | ----- | ----- | ----- | ----- | 
| **DEP-01** | Kiểm tra tính tương thích đường dẫn tương đối (`Relative Paths`) | Rà soát toàn bộ thuộc tính `href` và `src` của file nội bộ. | Sử dụng đường dẫn tương đối `./assets/...`, không dùng đường dẫn tuyệt đối gắn cứng ổ đĩa (như `C:\...` hay `/assets/...`). | 100% tài nguyên nội bộ dùng `./assets/css/styles.css` và `./assets/img/...`, chạy đúng ngay cả khi đặt trong thư mục con (sub-path). | ✅ Đạt | 
| **DEP-02** | Triển khai trên Máy chủ Cục bộ (Windows / macOS / Linux) | Chạy dự án bằng VS Code Live Server (`:5500`) và `python3 -m http.server 8080`. | Trang web phản hồi mã trạng thái `HTTP 200 OK` cho toàn bộ tệp HTML, CSS và hình ảnh. | Tải toàn bộ trang và tài nguyên trong `< 150ms` ở mạng nội bộ, không có bất kỳ lỗi `404 Not Found` nào. | ✅ Đạt | 
| **DEP-03** | Triển khai đóng gói bằng Docker (`nginx:alpine`) | Khởi chạy container Nginx ánh xạ cổng `8080:80` và truy cập `http://localhost:8080`. | Container khởi động thành công trong `< 2 giây`, phân phối đầy đủ giao diện Cyber Portfolio. | Hoạt động ổn định, tiêu thụ bộ nhớ RAM cực thấp (`< 15MB`), sẵn sàng đưa lên môi trường Cloud/VPS. | ✅ Đạt | 
| **DEP-04** | Khả năng triển khai lên nền tảng Static Hosting (GitHub Pages) | Đẩy mã nguồn lên nhánh `main` và bật GitHub Pages. | Triển khai tự động không cần bước build, truy cập công khai qua tên miền `github.io`. | Tương thích 100% với GitHub Pages, Vercel và Netlify ngay lập tức (Zero-Config Deployment). | ✅ Đạt | 

### 6.3. Minh chứng hình ảnh

> *Hình 6.1: Minh chứng triển khai và vận hành thành công dự án trên máy chủ cục bộ & Docker Container với toàn bộ tài nguyên đạt trạng thái `200 OK` (`docs/screenshots/deployment-test.png`).*

## 7. KẾT LUẬN CHUNG & KIẾN NGHỊ

### 7.1. Kết luận nghiệm thu

Sau quá trình kiểm thử toàn diện qua **6 tiêu chí kỹ thuật** và **12 ca kiểm thử ma trận Responsive**, sản phẩm **Cyber Portfolio & Personal CV — Phạm Quốc Hùng (`v1.0.0`)** đã **ĐẠT 100% tiêu chí chấp nhận (`AC-01` → `AC-07`)**. Trang web sẵn sàng để bàn giao, nộp báo cáo kiểm tra A2.1 và sử dụng thực tế trong hồ sơ ứng tuyển Frontend Developer.

### 7.2. Hướng phát triển ở phiên bản tiếp theo (`v1.1.0`)

1. Tích hợp `localStorage` để ghi nhớ chủ đề màu yêu thích của người dùng sau khi tải lại trang.

2. Kết nối biểu mẫu liên hệ với dịch vụ gửi thư thực tế (EmailJS hoặc Formspree) kèm thông báo Toast Notification khi gửi thành công.

3. Chuyển đổi các tệp ảnh `.jfif` / `.png` sang chuẩn `.webp` để tối ưu hơn nữa tốc độ tải trang trên mạng di động.