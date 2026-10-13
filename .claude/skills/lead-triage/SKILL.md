---
name: lead-triage
description: Làm sạch, phân loại và xếp ưu tiên danh sách lead do Marketing cấp. Dùng khi người dùng gửi file lead (Excel/CSV/danh sách dán vào) hoặc nói "lọc lead", "ưu tiên gọi ai", "phân loại khách".
---

# Lead triage — Làm sạch và ưu tiên lead

## Đầu vào
File Excel/CSV hoặc danh sách dán trực tiếp. Hỏi lại nếu thiếu cột tên công ty.

## Các bước
1. **Làm sạch**: bỏ dòng trùng (theo SĐT, email, tên công ty), chuẩn hóa SĐT về dạng `0xxxxxxxxx`, viết hoa tên công ty đúng chuẩn, đánh dấu dòng thiếu thông tin.
2. **Bổ sung**: suy luận ngành nghề và quy mô từ tên công ty, chức danh hoặc email domain nếu có. Ghi `[ƯỚC ĐOÁN]` cho mọi giá trị suy luận.
3. **Chấm điểm 0–100** theo tiêu chí trong `knowledge/icp.md`. Nếu file đó chưa có thì dùng mặc định:
   - Quy mô nhân sự (30%): 50–1000 người điểm cao nhất.
   - Chức danh người liên hệ (25%): CEO/COO/HR Director/Trưởng phòng > nhân viên.
   - Ngành ưu tiên (20%).
   - Nguồn lead và mức quan tâm (25%): đăng ký demo > tải tài liệu > sự kiện.
4. **Phân hạng**: A (≥70, gọi hôm nay), B (40–69, gọi trong tuần), C (<40, nurture).

## Đầu ra
- File `deals/_lead-triage-<YYYY-MM-DD>.xlsx` có thêm các cột: `Điểm`, `Hạng`, `Lý do`, `Gợi ý góc tiếp cận` (1 câu).
- Thêm lead hạng A và B vào `knowledge/pipeline.csv` với trạng thái `Mới`.
- Tóm tắt trong chat: số lead, số trùng đã bỏ, top 5 lead nên gọi đầu tiên kèm lý do.

## Bước tiếp theo
Gợi ý chạy `/account-research <tên công ty>` cho các lead hạng A.
