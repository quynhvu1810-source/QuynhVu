---
name: daily-planner
description: Quản trị công việc hằng ngày và hằng tuần của Business Consultant - lập kế hoạch ngày, rà soát pipeline, nhắc follow-up quá hạn, đánh giá cuối tuần. Dùng khi người dùng nói "hôm nay làm gì", "kế hoạch ngày", "rà soát pipeline", "tổng kết tuần".
---

# Daily planner — Nhà quản trị công việc

## Nguồn dữ liệu
`knowledge/pipeline.csv`, `knowledge/goals.md` (chỉ tiêu tháng/quý), các thư mục `deals/`, cùng việc phát sinh người dùng kể thêm.

## Chế độ "Kế hoạch ngày" (mặc định vào buổi sáng)
1. Đọc pipeline và lọc: follow-up đến hạn hoặc quá hạn, lịch demo/hẹn hôm nay, lead hạng A chưa gọi.
2. Xếp việc theo khung giờ:
   - **Khung vàng gọi điện** (9h–11h, 14h–16h): lead A, follow-up nóng.
   - **Khung chuẩn bị**: slide, demo cho các buổi sắp tới (ưu tiên buổi gần nhất).
   - **Khung hành chính**: cập nhật CRM, email.
3. Đầu ra ngắn gọn:
   - **Top 3 việc quan trọng nhất hôm nay** và lý do.
   - Lịch theo giờ.
   - ⚠️ Cảnh báo: deal đứng yên quá 7 ngày, follow-up quá hạn.

## Chế độ "Rà soát pipeline"
Bảng theo giai đoạn: số deal, giá trị, xác suất. So với chỉ tiêu trong `goals.md`, tính khoảng thiếu (gap) và đề xuất hành động để lấp gap.

## Chế độ "Tổng kết tuần" (thứ Sáu)
- Số liệu: số cuộc gọi, số demo, deal chuyển giai đoạn, deal chốt hoặc mất.
- Bài học: điều gì hiệu quả, điều gì không (tham khảo nhận xét từ `/sales-coach`).
- Ưu tiên tuần tới.
- Lưu vào `deals/_tong-ket/<YYYY>-W<tuần>.md`.

## Tự động hóa (tùy chọn)
Người dùng có thể dùng `/loop` hoặc tạo Routine để chạy skill này mỗi sáng ngày làm việc.
