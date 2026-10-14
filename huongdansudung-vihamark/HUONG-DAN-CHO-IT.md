# Đưa hướng dẫn Vihamark lên base.vn/huongdansudung-vihamark

Mục tiêu: mở được trang hướng dẫn tại **https://base.vn/huongdansudung-vihamark**

## Trang này gồm gì
- Chỉ một file tĩnh: `index.html`. Không cần backend, cơ sở dữ liệu hay bước build.
- Tài nguyên ngoài duy nhất là phông chữ Google Fonts (fonts.googleapis.com, fonts.gstatic.com).
  Nếu website có Content-Security-Policy, cần cho phép hai tên miền này.

## Cách đưa lên
1. Tải cả thư mục `huongdansudung-vihamark/` vào thư mục gốc (web root) của base.vn,
   sao cho đường dẫn là `<web-root>/huongdansudung-vihamark/index.html`.
2. Kiểm tra máy chủ trả về `index.html` khi mở `/huongdansudung-vihamark`
   và `/huongdansudung-vihamark/` (đây là cấu hình mặc định của Nginx, Apache và hầu hết CDN).
3. Nếu base.vn chạy trên CMS hoặc framework (WordPress, Next.js…), dùng cách tương đương:
   tạo route tĩnh `/huongdansudung-vihamark` trả về nội dung file `index.html`.

## Kiểm tra sau khi đưa lên
- Mở link trên máy tính: slide hiển thị ngang, phím ← → để chuyển slide.
- Mở link trên điện thoại cầm dọc: slide tự chuyển sang bố cục dọc, vuốt để chuyển slide.
- Mở trong tab ẩn danh, không cần đăng nhập.

File `HUONG-DAN-CHO-IT.md` này không cần tải lên máy chủ.
