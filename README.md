# ⚡ Cyber Portfolio & Personal CV — Phạm Quốc Hùng (@HùngKanji)

![Version](https://img.shields.io/badge/version-v1.0.0-ff2a85?style=for-the-badge)
![HTML5](https://img.shields.io/badge/HTML5-Semantic-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-Flexbox_%26_Grid-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6%2B-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Responsive](https://img.shields.io/badge/Responsive-Mobile--First-00f5d4?style=for-the-badge)

---

## 1. Tên dự án
**Cyber Portfolio & Personal CV — Phạm Quốc Hùng (@HùngKanji)**  
*(Mã bài tập/dự án: KT20A2.1 — Website Portfolio CV Responsive)*

---

## 2. Mô tả dự án
**Cyber Portfolio & Personal CV** là trang web hồ sơ năng lực cá nhân tĩnh (Static Web Application) được thiết kế theo phong cách **Gloss Black kết hợp Neon & Cyber Gaming UI**, phát triển dựa trên tư duy **Mobile-First Responsive**. 

Dự án giúp nhà tuyển dụng (HR), trưởng nhóm kỹ thuật (Tech Lead) và khách truy cập nắm bắt toàn diện thông tin của ứng viên **Phạm Quốc Hùng** (vị trí ứng tuyển, kỹ năng công nghệ, dự án tiêu biểu và phương thức liên hệ) trong vòng chưa đầy 30 giây trên mọi kích thước màn hình từ điện thoại nhỏ (`360px`), máy tính bảng (`768px`) đến màn hình máy tính lớn (`1280px+`).

---

## 3. Chức năng chính
1. **Header & Điều hướng thông minh (`<header>`, `<nav>`):**
   - Thanh điều hướng cố định (`sticky`) tích hợp hiệu ứng kính mờ (`backdrop-filter: blur(20px)`).
   - Tự động xuống dòng (`flex-wrap`) trên màn hình nhỏ và cuộn mượt (`scroll-behavior: smooth`) tới đúng từng phân khu nội dung.
2. **Hệ thống chuyển đổi đa giao diện (Multi-Theme Switcher):**
   - Chuyển đổi tức thời giữa 3 bảng màu chủ đạo ngay trên thanh điều hướng mà không cần tải lại trang:
     - `Neon·Cyber` (`data-theme="blackpink"`): Tông Hồng Neon `#ff2a85` & Xanh Cyan `#00f5d4`.
     - `Aincrad·SAO` (`data-theme="aincrad"`): Tông Tím Huyền Ảo `#7209b7` & Xanh Băng `#4cc9f0`.
     - `Jett·Radiant` (`data-theme="valorant"`): Tông Đỏ Valorant `#ff4655` & Trắng Ánh Kim `#ece8e1`.
3. **Khối Nhận diện & Giới thiệu (`#about` - Hero Section):**
   - Hiệu ứng chữ chuyển sắc 4 màu động (`shineText`) kết hợp hiệu ứng gõ chữ tự động (**Typewriter Effect**) luân phiên 3 chức danh.
   - Bảng thống kê nhanh 3 chỉ số (`04+ Dự án Web/Game`, `100% Responsive UI`, `240Hz Tư duy Tốc độ`).
   - Khung ảnh đại diện **Hologram 7 màu** kèm huy hiệu nổi chuyển động.
4. **Hiệu ứng Đồ họa Hạt Năng lượng & Tia Laser (`#cyberCanvas`):**
   - Tích hợp HTML5 Canvas tạo 55 hạt năng lượng đa sắc chuyển động tự do và tự động nối tia laser xanh Cyan khi con trỏ chuột di chuyển lại gần trong bán kính `150px`.
5. **Dải băng chuyền Cyber Marquee:**
   - Thanh chữ chạy ngang liên tục tạo điểm nhấn thị giác giữa khối giới thiệu và kỹ năng.
6. **Khối Kỹ năng Công nghệ (`#skills` - Tech Stack & Arsenal):**
   - Hiển thị 6 nhóm kỹ năng cốt lõi (`HTML5`, `CSS3 / Flexbox / Grid`, `JavaScript ES6+`, `Responsive Design`, `Git & GitHub`, `Figma / Wireframe`) kèm biểu tượng FontAwesome và thanh tiến trình năng lực (`Level Bar` từ `86%` đến `95%`).
7. **Khối Dự án Tiêu biểu (`#projects` - Featured Showcase):**
   - Trưng bày 4 dự án tiêu biểu (*Dự án Javalorant*, *Ứng dụng HTLMHT*, *C++SGO*, *Game Chết*) bằng bố cục **CSS Grid co giãn thông minh** (1 cột trên Mobile → 2 cột trên Tablet → 2–3 cột trên Desktop), đi kèm thẻ tag công nghệ và hiệu ứng phóng ảnh khi di chuột.
8. **Khối Liên hệ & Kết nối (`#contact`):**
   - Biểu mẫu liên hệ trực관 (Họ tên, Email, Tin nhắn) có kiểm tra dữ liệu đầu vào (`required`, `type="email"`).
   - Thanh mạng xã hội nổi kết nối trực tiếp tới Email, GitHub và LinkedIn cá nhân.

---

## 4. Công nghệ sử dụng
| Hạng mục | Công nghệ / Thư viện | Chi tiết áp dụng |
| :--- | :--- | :--- |
| **Ngôn ngữ đánh dấu** | **HTML5 Ngữ nghĩa (Semantic HTML5)** | Sử dụng chuẩn các thẻ `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<figure>`, `<footer>`, thuộc tính `aria-label` và `alt`. |
| **Ngôn ngữ tạo kiểu** | **CSS3 Modern Layout** | Biến CSS (`:root` Design Tokens), `Flexbox`, `CSS Grid`, `@keyframes` Animation, `Glassmorphism`, `Media Queries` chuẩn Mobile-First. |
| **Ngôn ngữ kịch bản** | **Vanilla JavaScript (ES6+)** | Xử lý DOM (Theme Switcher, Typewriter Effect) và đồ họa 2D (`HTML5 Canvas API` tương tác chuột). |
| **Typography** | **Google Fonts** | `Space Grotesk` (Tiêu đề), `Plus Jakarta Sans` (Nội dung), `JetBrains Mono` (Code/Badge). |
| **Biểu tượng (Icons)** | **FontAwesome 6.4.0 (CDN)** | Hệ thống icon kỹ năng, mạng xã hội và nút hành động. |
| **Đóng gói & Triển khai** | **Docker & Nginx (Tùy chọn)** | Hỗ trợ chạy container hóa thông qua `nginx:alpine`. |

---

## 5. Yêu cầu môi trường
Dự án là ứng dụng web tĩnh thuần túy (Static Frontend), yêu cầu môi trường rất nhẹ:
- **Hệ điều hành:** Windows 10/11, macOS (Intel / Apple Silicon), hoặc bất kỳ bản phân phối Linux nào (Ubuntu, Debian, Fedora, Arch...).
- **Trình duyệt web hiện đại:** Google Chrome (`>= 90`), Mozilla Firefox (`>= 88`), Microsoft Edge (`>= 90`), hoặc Apple Safari (`>= 14`) có bật JavaScript và hỗ trợ HTML5 Canvas.
- **Kết nối Internet:** Cần thiết để tải Google Fonts và FontAwesome Icons từ CDN.
- **Công cụ chạy máy chủ cục bộ (Chọn 1 trong các công cụ sau):**
  - Visual Studio Code + Tiện ích mở rộng **Live Server**.
  - **Python 3.x** (sử dụng module `http.server` có sẵn).
  - **Node.js** (`>= 16.x`, sử dụng `npx serve` hoặc `http-server`).
  - **Docker Engine** (`>= 20.10`) & **Docker Compose** (nếu chạy bằng container).

---

## 6. Cài đặt

### 6.1. Cấu trúc thư mục chuẩn
Đảm bảo thư mục dự án của bạn tuân thủ đúng cấu trúc sau:
```text
KT20A2.1/
├── index.html                  # File giao diện chính tích hợp Cyber UI & Script
├── README.md                   # Tài liệu hướng dẫn cài đặt & sử dụng
├── CHANGELOG.md                # Lịch sử phát hành phiên bản (Release Notes)
├── test_report.md              # Báo cáo kiểm thử 6 tiêu chí kèm minh chứng
├── Dockerfile                  # (Tùy chọn) Cấu hình đóng gói Docker image
├── assets/
│   ├── css/
│   │   └── styles.css          # File CSS nền tảng Mobile-First & Responsive
│   └── img/
│       ├── hung.jpg            # Ảnh đại diện cá nhân
│       ├── jett.jfif           # Ảnh minh họa khối Liên hệ
│       ├── javalorant.png      # Ảnh dự án Javalorant
│       ├── lmht.jfif           # Ảnh dự án Ứng dụng HTLMHT
│       ├── csgo.jfif           # Ảnh dự án C++SGO
│       └── pubg.jfif           # Ảnh dự án Game Chết
└── docs/
    └── screenshots/            # Thư mục lưu trữ ảnh chụp minh chứng kiểm thử
        ├── viewport-360px.png
        ├── viewport-768px.png
        ├── viewport-1280px.png
        ├── theme-switcher.png
        ├── form-validation.png
        └── html-validation.png
```

### 6.2. Hướng dẫn tải mã nguồn theo từng Hệ điều hành

#### 🪟 Trên Windows (Command Prompt / PowerShell / Git Bash)
```powershell
# Bước 1: Mở PowerShell hoặc Git Bash và di chuyển tới thư mục lưu trữ
cd C:\Users\%USERNAME%\Desktop

# Bước 2: Clone kho lưu trữ từ GitHub (hoặc giải nén file KT20A2.1.zip)
git clone https://github.com/hungkanji/KT20A2.1.git

# Bước 3: Di chuyển vào thư mục dự án
cd KT20A2.1
```

#### 🍎 Trên macOS (Terminal)
```bash
# Bước 1: Mở Terminal (Cmd + Space -> gõ Terminal) và vào thư mục làm việc
cd ~/Projects

# Bước 2: Clone dự án từ GitHub
git clone https://github.com/hungkanji/KT20A2.1.git

# Bước 3: Truy cập vào thư mục dự án
cd KT20A2.1
```

#### 🐧 Trên Linux (Ubuntu / Debian / Fedora)
```bash
# Bước 1: Cài đặt Git nếu chưa có (ví dụ trên Ubuntu/Debian)
sudo apt update && sudo apt install -y git

# Bước 2: Clone mã nguồn dự án về máy
git clone https://github.com/hungkanji/KT20A2.1.git

# Bước 3: Di chuyển vào thư mục dự án
cd KT20A2.1
```

#### 🐳 Trên Docker (Đa nền tảng)
Nếu chưa có sẵn file `Dockerfile` trong thư mục gốc, bạn có thể tạo nhanh bằng lệnh sau:
```dockerfile
# Nội dung file Dockerfile
FROM nginx:alpine
COPY . /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
```
Sau đó tiến hành đóng gói (build) Docker Image:
```bash
docker build -t hungkanji-portfolio:v1.0 .
```

---

## 7. Cấu hình
Dự án sử dụng kiến trúc tĩnh (Static HTML/CSS/JS) nên không yêu cầu tệp biến môi trường `.env`. Bạn có thể tùy biến nhanh các thông số sau trực tiếp trong file `index.html`:

1. **Cấu hình Bảng màu Giao diện (`:root` và `body[data-theme]`):**
   Mở `index.html` (dòng `20–39`) để chỉnh sửa các biến màu CSS:
   ```css
   :root {
     --bg-deep: #06060e;
     --pink: #ff2a85;
     --purple: #9d4edd;
     --cyan: #00f5d4;
     --gold: #ffbe0b;
     --blue: #3a86ff;
     --card-bg: rgba(14, 14, 28, 0.78);
   }
   ```
2. **Cấu hình Danh sách Chức danh Gõ tự động (Typewriter Roles):**
   Chỉnh sửa mảng `roles` trong thẻ `<script>` ở cuối file `index.html` (dòng `812–816`):
   ```javascript
   const roles = [
     "Frontend Developer & UI Enthusiast",
     "Creative Coder & Gamer (@HùngKanji)",
     "Responsive Web & Cyber UI Designer"
   ];
   ```
3. **Cấu hình Đường dẫn Hình ảnh:**
   Đảm bảo toàn bộ ảnh đặt trong `./assets/img/` trùng khớp tên file và phần mở rộng (`.jpg`, `.png`, `.jfif`) với thuộc tính `src` trong `index.html`.

---

## 8. Chạy thử

### 8.1. Chạy thử trên Windows

- **Cách 1: Dùng VS Code Live Server (Khuyên dùng)**
  1. Mở thư mục `KT20A2.1` trong **Visual Studio Code**.
  2. Nhấp chuột phải vào file `index.html` → Chọn **Open with Live Server**.
  3. Trình duyệt sẽ tự động mở tại địa chỉ: `http://127.0.0.1:5500/index.html`.
- **Cách 2: Dùng Python hoặc Node.js trên PowerShell**
  ```powershell
  # Nếu máy đã cài Python 3:
  python -m http.server 8080

  # Hoặc nếu máy đã cài Node.js:
  npx serve -l 8080
  ```
  Sau đó mở trình duyệt truy cập `http://localhost:8080`.
- **Cách 3: Mở trực tiếp**
  Nhấp đúp chuột vào file `index.html` trong File Explorer để mở trực tiếp bằng trình duyệt.

### 8.2. Chạy thử trên macOS

```bash
# Cách 1: Sử dụng Python 3 tích hợp sẵn trên macOS
python3 -m http.server 8080
# Mở nhanh trình duyệt Safari/Chrome từ Terminal:
open http://localhost:8080

# Cách 2: Mở trực tiếp file index.html không qua server
open index.html
```

### 8.3. Chạy thử trên Linux

```bash
# Cách 1: Khởi chạy máy chủ HTTP bằng Python 3
python3 -m http.server 8080
# Mở trình duyệt mặc định:
xdg-open http://localhost:8080

# Cách 2: Sử dụng gói http-server của Node.js
npx http-server -p 8080 -o
```

### 8.4. Chạy thử với Docker

```bash
# Cách 1: Chạy trực tiếp bằng Nginx Container (Không cần build Dockerfile)
# - Trên Linux / macOS / Git Bash:
docker run --rm -d -p 8080:80 --name cyber-portfolio -v "$(pwd):/usr/share/nginx/html:ro" nginx:alpine

# - Trên Windows PowerShell:
docker run --rm -d -p 8080:80 --name cyber-portfolio -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine

# Cách 2: Chạy từ Image đã build ở Bước 6.2
docker run --rm -d -p 8080:80 --name cyber-portfolio hungkanji-portfolio:v1.0
```
- Truy cập trang web tại: **`http://localhost:8080`**
- Để dừng container sau khi kiểm thử:
  ```bash
  docker stop cyber-portfolio
  ```

### 8.5. Kịch bản trải nghiệm nhanh sau khi chạy
1. Nhấn nút **`Neon·Cyber`** ở góc phải thanh Header để kiểm tra chuyển đổi qua lại giữa 3 chế độ màu (`Neon·Cyber` → `Aincrad·SAO` → `Jett·Radiant`).
2. Di chuyển chuột khắp màn hình để quan sát các hạt năng lượng nối tia laser theo tọa độ chuột.
3. Nhấn phím `F12` (DevTools) → Bật **Device Toolbar (`Ctrl + Shift + M`)** và kiểm tra lần lượt ở các kích thước `360px`, `768px`, `1280px`.

---

## 9. Thông tin liên hệ
Mọi ý kiến đóng góp, cơ hội thực tập hoặc hợp tác dự án Frontend xin vui lòng liên hệ:

- **Họ và tên:** Phạm Quốc Hùng (`@HùngKanji`)
- **Vai trò:** Frontend Developer & UI Enthusiast
- **Email:** [hungkanji01@gmail.com](mailto:hungkanji01@gmail.com)
- **GitHub:** [https://github.com/hungkanji](https://github.com/hungkanji)
- **LinkedIn:** [https://linkedin.com/in/hungkanji](https://linkedin.com/in/hungkanji)