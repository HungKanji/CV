# 📦 CHANGELOG — Lịch Sử Phát Hành (Release Notes)

Mọi thay đổi đáng chú ý, tính năng mới, bản vá lỗi và các hạn chế kỹ thuật của dự án **Cyber Portfolio & Personal CV — Phạm Quốc Hùng (@HùngKanji)** đều được ghi chép chi tiết tại tài liệu này.

Định dạng tài liệu dựa trên chuẩn [Keep a Changelog](https://keepachangelog.com/vi/1.0.0/) và quy tắc đánh số phiên bản ngữ nghĩa [Semantic Versioning](https://semver.org/lang/vi/).

---

## [v1.0.0] — Phiên bản Chính thức Đầu tiên (Initial Stable Release)
- **Phiên bản:** `v1.0` (`v1.0.0`)
- **Ngày phát hành:** `05/11/2026`
- **Trạng thái:** Đạt chuẩn nghiệm thu toàn bộ tiêu chí `AC-01` đến `AC-07` và vượt qua 12/12 ca kiểm thử (`TC-01` đến `TC-12`).

---

### ✨ Chức năng mới (Added)
1. **Kiến trúc HTML5 Ngữ nghĩa Hoàn chỉnh (`AC-01`, `AC-04`, `AC-06`):**
   - Xây dựng cấu trúc trang chuẩn SEO & Accessibility với đầy đủ 5 phân khu cốt lõi: Header & Điều hướng (`<header>`, `<nav>`), Giới thiệu bản thân (`#about`), Kỹ năng công nghệ (`#skills`), Dự án tiêu biểu (`#projects`), và Liên hệ (`#contact`), cùng chân trang (`<footer>`).
   - Bổ sung đầy đủ khai báo `<html lang="vi">`, thẻ `<meta name="viewport">`, thuộc tính `aria-label` cho vùng điều hướng và văn bản thay thế `alt` cho 100% hình ảnh.
2. **Giao diện Cyber Neon & Hệ thống Đa Chủ đề (Multi-Theme Engine):**
   - Thiết kế hệ thống biến màu CSS (`:root` Design Tokens) kết hợp nút chuyển đổi trực tiếp giữa 3 chủ đề: **Neon·Cyber** (`blackpink`), **Aincrad·SAO** (`aincrad`), và **Jett·Radiant** (`valorant`).
3. **Hiệu ứng Tương tác Động (Interactive Visual Effects):**
   - **HTML5 Canvas Particle & Laser Network:** Tạo hệ thống 55 hạt năng lượng đa sắc chuyển động trên nền lưới Cyber 3D và tự động vẽ tia laser kết nối với con trỏ chuột trong phạm vi `150px`.
   - **Typewriter Effect:** Hiệu ứng gõ và xóa chữ tự động hiển thị luân phiên 3 vai trò chuyên môn tại khu vực Hero.
   - **Hologram Avatar & Cyber Marquee:** Khung ảnh đại diện đổi màu 7 sắc cầu vồng kèm huy hiệu nổi (`LEVEL 99 DEV`, `@HùngKanji`) và dải băng chuyền chữ chạy liên tục.
4. **Hệ thống Bố cục Responsive Đa Thiết bị (`AC-02`, `AC-07`):**
   - Áp dụng triết lý **Mobile-First**结合 **Flexbox** và **CSS Grid**, tự động điều chỉnh bố cục mượt mà qua 3 breakpoint chính (`360px` Mobile, `768px` Tablet, `1280px` Desktop) và các kích thước phụ (`375px` iPhone SE, `1024px` iPad ngang).
5. **Biểu mẫu Liên hệ & Thanh Mạng xã hội Tương tác:**
   - Cung cấp form gửi tin nhắn có kiểm tra trường bắt buộc (`required`) và định dạng thư điện tử (`type="email"`), tích hợp thanh liên kết nhanh tới Email, GitHub và LinkedIn.

---

### 🛠️ Lỗi đã sửa (Fixed)
1. **Khắc phục triệt để lỗi tràn khung và thanh cuộn ngang trên Mobile (`AC-03`, `TC-01`, `TC-08`):**
   - Chuẩn hóa mô hình hộp bằng `*, *::before, *::after { box-sizing: border-box !important; }`, thiết lập `img { max-width: 100%; height: auto; }` và khóa tràn ngang bằng `overflow-x: hidden` trên thẻ `body`. Kết quả đo thực tế trên trình duyệt Chromium headless đạt `scrollWidth = 360px` tại viewport `360px` và `scrollWidth = 768px` tại viewport `768px`.
2. **Xử lý xung đột CSS gây mất nền tối và chìm chữ tiêu đề:**
   - Khắc phục hiện tượng các quy tắc mặc định trong `assets/css/styles.css` ghi đè làm nền `.hero`, `.section` bị chuyển sang màu trắng bằng cách khóa cứng nền trong suốt (`background-color: transparent !important`) trên các phân khu con và giữ nền tối sâu `--bg-deep: #06060e` trên `body`.
   - Sửa lỗi chữ tiêu đề `.hero-title` bị mờ trên nền sáng/tối bằng dải chuyển sắc 4 màu có độ tương phản cao kèm `drop-shadow`.
3. **Sửa lỗi thanh điều hướng (`<nav>`) bị tràn trên màn hình hẹp (`TC-02`):**
   - Áp dụng `flex-wrap: wrap` và khoảng cách `gap` hợp lý cho `.header-inner` và `.nav-list`, giúp 4 mục điều hướng và nút đổi theme tự động sắp xếp gọn gàng trên màn hình `360px`.
4. **Sửa lỗi iOS Safari tự động phóng to cỡ chữ gây vỡ bố cục (`TC-05`):**
   - Cân chỉnh thang đo chữ linh hoạt (`clamp()`) và cấu hình `text-size-adjust` giúp giao diện trên iPhone SE (`375px`) giữ nguyên tỷ lệ lề và phông chữ chuẩn.

---

### ⚠️ Hạn chế còn tồn tại (Known Limitations)
1. **Biểu mẫu liên hệ chưa kết nối máy chủ Backend (`<form action="#" method="POST">`):**
   - Hiện tại form liên hệ chỉ dừng ở mức kiểm tra hợp lệ phía trình duyệt (Client-side HTML5 Validation). Khi người dùng nhấn *"Gửi tin nhắn"*, dữ liệu chưa được gửi tới máy chủ thực tế hoặc dịch vụ lưu trữ email (như EmailJS, Formspree).
2. **Trạng thái giao diện (Theme) chưa được lưu bền vững vào `localStorage`:**
   - Khi người dùng chuyển sang chủ đề `Aincrad·SAO` hoặc `Jett·Radiant`, nếu tải lại trang (`F5`), giao diện sẽ quay về chủ đề mặc định `Neon·Cyber` (`data-theme="blackpink"`).
3. **Các liên kết `"Xem chi tiết →"` ở thẻ Dự án đang dùng đường dẫn giả lập (`href="#"`):**
   - Các thẻ dự án hiện mang tính chất trưng bày giao diện, chưa trỏ tới trang mô tả chi tiết từng dự án hoặc kho mã nguồn GitHub riêng lẻ của từng sản phẩm.
4. **Phụ thuộc vào mạng Internet cho tài nguyên CDN & Định dạng ảnh chưa đồng nhất:**
   - Khi chạy ở môi trường hoàn toàn ngoại tuyến (Offline), các biểu tượng FontAwesome 6.4.0 và phông chữ Google Fonts sẽ chuyển về phông hệ thống mặc định.
   - Một số ảnh minh họa dự án vẫn đang sử dụng định dạng `.jfif` và `.png` dung lượng gốc thay vì định dạng tối ưu cho web thế hệ mới như `.webp` hoặc `.avif`.
5. **Tối ưu hiệu năng Canvas trên thiết bị di động cấu hình thấp:**
   - Hiệu ứng `#cyberCanvas` hiện luôn khởi tạo 55 hạt chuyển động liên tục qua `requestAnimationFrame`, chưa tự động giảm số lượng hạt hoặc tạm dừng khi người dùng bật chế độ tiết kiệm pin / `prefers-reduced-motion`.