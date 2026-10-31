# Mẫu slide Base 2.0

Mẫu gốc: https://claude.ai/artifact/MqB8HPPQoEbCn51Vr4CgqL (deck "Vietravel Airlines × Base 2.0").
Ảnh xem nhanh các kiểu slide: [preview.png](preview.png).

Khi làm deck cho khách hàng mới: giữ nguyên hệ màu, font và bố cục bên dưới, chỉ thay logo, tên khách hàng và nội dung.

## Khung trang

- Canvas 1920 × 1080, nền tối.
- Lề trái/phải 96px. Khối tiêu đề bắt đầu ở top 136px.
- Góc trên trái: logo khách hàng + logo Base.vn (cỡ nhỏ, cùng hàng).
- Góc trên phải: nhãn mục đang trình bày, chữ hoa nhỏ màu xanh nhạt (ví dụ `TỔ CHỨC VÀ PHÂN CÔNG · WORKFORCE`).
- Lớp nhiễu hạt mờ phủ toàn trang: chấm `rgba(157,179,218,.07)` lưới 6px, độ mờ 0.5.

## Màu

| Token | Mã | Dùng cho |
|---|---|---|
| `bg` | `#061235` | Nền chính |
| `bg2` | `#0A1B4A` | Nền phụ, vùng gradient |
| `ink` | `#F4F8FF` | Tiêu đề, chữ chính |
| `ink2` | `#D6E4FF` | Chữ thân nổi bật |
| `mute` | `#9DB3DA` | Chữ mô tả |
| `dim` | `#6C84B2` | Ghi chú, nguồn |
| `sky` | `#6FB2FF` | Nhãn (eyebrow), đường kẻ |
| `blue` | `#2F7BFF` | Nhấn chính |
| `cyan` | `#5EE7FF` | Nhấn phụ, số thứ tự |
| `violet` | `#A78BFA` | Riêng cho AI / Agent |
| vàng | `#F7C51E` | Điểm nhấn rất ít (vạch ngắn ở bìa, ghi chú quan trọng) |
| `card` | `rgba(255,255,255,.045)` | Nền thẻ |
| `cardb` | `rgba(157,179,218,.20)` | Viền thẻ |
| `line` | `rgba(157,179,218,.18)` | Đường kẻ phân cách |

Gradient chữ nhấn (phần `<em>` trong tiêu đề): `linear-gradient(90deg, #6FB2FF, #5EE7FF)`.

## Font

- **Be Vietnam Pro**: tiêu đề và tên mục. Tiêu đề trang 56px, weight 700, letter-spacing −0.025em, line-height 1.12. Tên thẻ 22–34px, weight 700.
- **Inter**: chữ thân 16–22px; nhãn (eyebrow) 13–15px, weight 600, chữ hoa, letter-spacing 0.16–0.22em, màu `sky`; số lớn ở trang phân mục weight 200.
- **Caveat**: chữ viết tay, chỉ dùng cho một dòng nhấn khi thật cần.

## Các kiểu slide

1. **Bìa**: nửa trái là chữ, nửa phải là ảnh lớn hòa vào nền. Nhãn `KHÁCH HÀNG × BASE`; tiêu đề 2 dòng, dòng 1 đậm trắng, dòng 2 nhẹ hơn màu xanh nhạt; vạch ngắn màu vàng; 2 dòng mô tả. Chân trang: tên buổi trình bày bên trái, tháng/năm bên phải. Góc trên phải: `BASE 2.0`.
2. **Nội dung trao đổi**: nhãn `KHÁCH HÀNG × BASE.VN · THÁNG/NĂM`, tiêu đề có một từ nhấn gradient ("Nội dung **trao đổi**"), danh sách đánh số `01…04` màu xanh, mỗi dòng có đường kẻ mảnh.
3. **Trang phân mục**: số rất lớn (`01`, Inter 200, 360px, gradient xanh) bên trái, đường dọc mờ, bên phải nhãn `PHẦN 01` + tiêu đề 120px + mô tả. Đáy trang là thanh điều hướng các phần, phần đang trình bày được tô sáng.
4. **Nội dung chữ + dữ liệu**: tiêu đề có phần nhấn gradient, danh sách đánh số nhỏ, thẻ số liệu (số lớn màu vàng/xanh + mô tả), nền bản đồ/hình mờ phía sau.
5. **Sơ đồ / dòng thời gian**: đường nối mảnh, mốc hình thoi, mỗi mốc có số, tiêu đề và mô tả ngắn.
6. **Bản đồ ứng dụng**: các nhóm (AI Layer, Work OS, People OS, Collaboration, Foundation) trong thẻ bo góc; mỗi nhóm có hàng icon ứng dụng kèm tên.
7. **Chữ + ảnh màn hình**: cột trái rộng khoảng 430px (icon + tên ứng dụng, tiêu đề, 3 ý đánh số, ghi chú vàng), cột phải là khung ảnh màn hình lớn nền sáng, bo góc.
8. **Bảng so sánh luồng**: các hàng (BPM, Task, Project…) với ba cột vai trò, mũi tên mảnh giữa các cột.
9. **Hành trình**: một đường ngang có các mốc (Tuyển dụng → Tiếp nhận → Hồ sơ → Phát triển), dưới mỗi mốc là icon ứng dụng; khối "lặp lại trong suốt thời gian làm việc"; dải chú thích dưới cùng.
10. **Kết**: logo khách hàng + Base ở giữa, nhãn nhỏ `BASE SẼ` có vạch hai bên, khẩu hiệu lớn chữ mảnh ("Học hỏi · Cải tiến · Đồng hành"), dòng tên khách hàng màu xanh đậm, một dòng mô tả.

## Nguyên tắc

- Mỗi trang một thông điệp; tiêu đề là câu có ý, phần then chốt nhấn gradient.
- Màu nhấn chủ yếu là xanh dương và cyan. Vàng chỉ dùng rất ít. Tím chỉ dùng cho AI/Agent.
- Thẻ dùng nền `card`, viền `cardb`, bo góc 18–22px, không đổ bóng đậm.
- Ảnh màn hình đặt trong khung nền sáng, bo góc, che hoặc cắt thông tin của khách hàng khác trước khi đưa vào.
