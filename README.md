# 🎓 Website IT4Teacher - Câu lạc bộ Sư phạm Tin học (Góc JavaScript căn bản)

> **Bài tập lớn học phần:** ICT0023 - Thiết kế Web  
> **Đơn vị:** Khoa Khoa học Tự nhiên - Công nghệ, Trường Đại học Tây Bắc  
> **Nhóm thực hiện:** Nhóm 10 (Lớp K66 ĐHSP Tin học)  
> **Giảng viên hướng dẫn:** Nguyễn Duy Hiếu  
> **Thư mục mã nguồn:** `ICT0023-K66-IT4Teacher/`

---

## 🎯 1. Mục tiêu và người dùng

- **Mục tiêu:** Xây dựng kênh truyền thông chính thức cho CLB Sư phạm Tin học IT4Teacher; cung cấp thông tin bộ máy tổ chức, hoạt động sinh hoạt, sản phẩm ứng dụng công nghệ (AI/Game) và cổng tuyển thành viên năm 2026.
- **Người dùng chính:** Sinh viên quan tâm đến CNTT/lập trình, Ban chủ nhiệm & thành viên CLB, sinh viên có nguyện vọng ứng tuyển.
- **Đặc điểm kỹ thuật:** Website tĩnh phía máy khách (Client-side Static Website) xây dựng bằng HTML5, CSS3 và JavaScript thuần (Vanilla JS). Không sử dụng Backend hay Cơ sở dữ liệu; Form đăng nhập ở Footer là giao diện tĩnh UI-only và Nút ứng tuyển điều hướng sang Google Forms.

---

## 👥 2. Thành viên nhóm & Phân công nhiệm vụ

| Họ và tên | Vai trò / Ban | Nhiệm vụ chính |
| :--- | :--- | :--- |
| **Giàng Tuấn Anh** | Chủ nhiệm CLB (Nhóm trưởng) | Cấu trúc HTML chính, kịch bản điều hướng, trang `1TrangChu.html` & `2GioiThieu.html` |
| **Tòng Thị Thanh Thúy** | Phó chủ nhiệm | Thiết kế CSS toàn hệ thống, hệ màu Dark Mode (`DoiMau.css`), trang `3HoatDong.html` |
| **Cầm Huy Tường** | Ban Kỹ thuật | Kịch bản JS (`hoidap.js`, `script.js`, `dieuhuong.js`), trang `4SanPham.html` & `6HoiDap.html` |
| **Bùi Việt Hà** | Ban Truyền thông | Biên tập nội dung, xử lý ảnh/video, trang `5TuyenThanhVien.html` & `Xemthem.html` |

---

## 🌐 3. Cấu trúc Website (7 Trang)

| Trang | Tệp HTML | Nội dung chính |
| :--- | :--- | :--- |
| **Trang chủ** | `1TrangChu.html` | Giới thiệu tổng quan CLB, sứ mệnh, video MP4 giới thiệu, danh sách công cụ phần mềm |
| **Giới thiệu** | `2GioiThieu.html` | Thông tin bộ máy Ban chủ nhiệm và các Ban chuyên môn |
| **Hoạt động** | `3HoatDong.html` | Bài viết về hoạt động, thành tựu NCKH, cuộc thi (Hue-ICT Challenge, Giải B Sáng tạo TTN Nhi đồng) |
| **Sản phẩm** | `4SanPham.html` | Trưng bày dự án AI & Game Canvas (Cyber Caro 15x15, Cozy Kitchen, Saiyan Clash) kèm video demo MP4 |
| **Tuyển thành viên** | `5TuyenThanhVien.html` | Cổng thông tin đợt tuyển thành viên 2026, nút dẫn đơn Google Forms và liên kết trang chi tiết |
| **Hỏi đáp** | `6HoiDap.html` | Bảng giải đáp thắc mắc FAQ dạng Accordion tự động đóng/mở |
| **Trang chi tiết** | `Xemthem.html` | Chi tiết đối tượng, quyền lợi và quy trình 3 bước ứng tuyển thành viên năm 2026[cite: 7] |

---

## ⚙️ 4. Chức năng tương tác (JavaScript thuần)

| Tên chức năng | Mô tả thực hiện | Tệp kịch bản xử lý |
| :--- | :--- | :--- |
| **Điều hướng Responsive** | Navbar dạng menu ngang trên máy tính, chuyển sang menu trượt Mobile Drawer (`#mobileMenu`) khi bấm Hamburger[cite: 7] | `JAVASCRIPT/script.js` (`toggleMenu()`)[cite: 7] |
| **Tìm kiếm phía Client** | Ô tìm kiếm `#searchMember` lọc danh sách thành viên/nội dung trực tiếp tại trình duyệt và cuộn đến kết quả[cite: 7] | `JAVASCRIPT/DoiDaoDienVaTimKiemThanhVien.js`[cite: 7] |
| **Giao diện Sáng/Tối** | Nút `#themeToggle` bật/tắt chế độ Dark/Light Mode bằng cách nhúng tệp CSS đổi màu[cite: 7] | `CSS/DoiMau.css`, `JAVASCRIPT/DoiDaoDienVaTimKiemThanhVien.js`[cite: 7] |
| **FAQ Accordion** | Nhấp vào câu hỏi để mở câu trả lời, tự động đóng câu trả lời của các câu khác[cite: 7] | `JAVASCRIPT/hoidap.js`[cite: 7] |
| **Nút Back-to-top** | Tự động xuất hiện khi cuộn trang xuống quá 400px và cuộn mượt về đầu trang khi nhấp[cite: 7] | `JAVASCRIPT/dieuhuong.js`[cite: 7] |
| **Form Validation UI** | Kiểm tra thuộc tính `required` ở Form Đăng nhập Footer (chỉ xử lý giao diện tĩnh phía Client)[cite: 7] | `1TrangChu.html`, `CSS/foot.css`[cite: 7] |

---

## 🛠️ 5. Công nghệ sử dụng

- **Core:** HTML5 ngữ nghĩa (`<header>`, `<nav>`, `<article>`, `<footer>`), CSS3 (Box Model, Flexbox, Media Queries), JavaScript thuần (Vanilla JS thao tác DOM)[cite: 7].
- **Thư viện biểu tượng:** Font Awesome v6.4.0 (kết nối qua CDN)[cite: 7].
- **Lưu ý:** Dự án **không** sử dụng Bootstrap hay jQuery[cite: 7].

---

## 🎨 6. Thiết kế & Bảng màu

- **Chế độ giao diện:** Hỗ trợ chuyển đổi linh hoạt chế độ Sáng (Light Mode) và Tối (Dark Mode) qua nút bấm chọn giao diện[cite: 7].
- **Bố cục:** Thiết kế thích ứng (Responsive Layout) bằng Flexbox và Media Queries, hiển thị tối ưu trên Desktop, Tablet và Smartphone[cite: 7].

---

## 📂 7. Cấu trúc thư mục dự án

```text
ICT0023-K66-IT4Teacher/
├── 1TrangChu.html                  # Trang chủ
├── 2GioiThieu.html                 # Trang giới thiệu nhân sự
├── 3HoatDong.html                  # Trang hoạt động & giải thưởng
├── 4SanPham.html                   # Trang sản phẩm Game & AI
├── 5TuyenThanhVien.html            # Trang cổng thông tin tuyển thành viên
├── 6HoiDap.html                    # Trang hỏi đáp FAQ Accordion
├── Xemthem.html                    # Trang chi tiết đợt tuyển thành viên 2026
├── CSS/
│   ├── styles.css                  # Reset CSS, biến hệ màu & khung chung
│   ├── 1TrangChu.css, 2GioiThieu.css, 3HoatDong.css...
│   ├── foot.css, search.css
│   └── DoiMau.css                  # Chuyển đổi hệ màu Dark/Light Mode
├── JAVASCRIPT/
│   ├── script.js                   # Bật/tắt Mobile Drawer Menu
│   ├── dieuhuong.js                # Hiệu ứng cuộn & Nút Back-to-top
│   ├── DoiDaoDienVaTimKiemThanhVien.js # Dark Mode & Tìm kiếm Client
│   ├── hoidap.js                   # Xử lý FAQ Accordion
│   └── gioithieu.js, hoatdong.js, footer.js...
└── images/                         # Ảnh logo, hoạt động, tệp video MP4 (VDN.mp4, caroo.mp4)
