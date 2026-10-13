---
name: demo-builder
description: Soạn kịch bản demo theo câu chuyện của khách và sinh dữ liệu demo sát thực tế để nhập vào Base. Dùng khi người dùng nói "dựng demo", "kịch bản demo", "dữ liệu demo", "chuẩn bị showcase".
---

# Demo builder — Kịch bản và dữ liệu demo

## Đầu vào
`04-qualification.md` (bắt buộc), `01-brief.md`, `knowledge/base-products.md`.

## Đầu ra 1: `06-demo-script.md`
- **Câu chuyện xuyên suốt** (storyline): một ngày làm việc của 2–3 nhân vật trong công ty khách (ví dụ: nhân viên tạo đề xuất → trưởng phòng duyệt → CEO xem báo cáo).
- **Bảng kịch bản** theo thời gian (tổng 30–45 phút):
  | Phút | Màn hình / Module | Thao tác | Lời dẫn | Pain point được giải quyết |
- **3 khoảnh khắc "wow"** gắn với pain lớn nhất.
- Câu hỏi khách có thể hỏi và cách trả lời.
- Checklist chuẩn bị trước buổi demo: tài khoản, dữ liệu, thông báo, thiết bị.

## Đầu ra 2: `06-demo-data.xlsx`
Mỗi sheet là một loại dữ liệu cần nhập vào Base, tên và nội dung theo ngành của khách:
- Sơ đồ tổ chức: phòng ban, chức danh, 15–30 nhân viên (tên tiếng Việt giả lập).
- Dự án và công việc mẫu, có hạn, người phụ trách, trạng thái đa dạng.
- Mẫu đề xuất / phê duyệt: trường thông tin, các bước duyệt, điều kiện rẽ nhánh.
- Quy trình (workflow): các giai đoạn, người phụ trách, SLA.
- Dữ liệu HR (nếu có trong giải pháp): ca làm việc, loại nghỉ phép, KPI/OKR mẫu.

## Lưu ý
- Chỉ dùng dữ liệu giả lập, không dùng dữ liệu thật của khách.
- Nếu người dùng có bật Claude in Chrome hoặc Computer Use, có thể đề nghị nhập trực tiếp vào tài khoản demo Base, nhưng phải hỏi trước khi thao tác.

## Bước tiếp theo
Sau buổi demo, gợi ý `/follow-up`.
