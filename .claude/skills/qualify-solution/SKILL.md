---
name: qualify-solution
description: Đánh giá mức độ phù hợp của deal và ánh xạ pain point của khách sang giải pháp Base, kèm lộ trình triển khai và ước tính ROI. Dùng khi người dùng nói "qualify", "chọn giải pháp", "khách này nên dùng module gì", "tính ROI".
---

# Qualify & Solution mapping

## Đầu vào
`03-discovery-notes.md` (bắt buộc), `01-brief.md` (nếu có), `knowledge/base-products.md`.

## Đầu ra: `04-qualification.md`
1. **Fit score 0–100** kèm bảng chấm điểm:
   | Tiêu chí | Trọng số | Điểm | Ghi chú |
   |---|---|---|---|
   | Pain rõ ràng và cấp bách | 30% | | |
   | Tiếp cận được người quyết định | 25% | | |
   | Ngân sách phù hợp | 20% | | |
   | Timeline ≤ 3 tháng | 15% | | |
   | Phù hợp ICP | 10% | | |
   Kết luận: **Tiếp tục / Nurture / Loại**, kèm lý do.
2. **Bảng mapping** Pain point → Module Base → Tính năng cụ thể → Kết quả kỳ vọng. Chỉ dùng tính năng có trong `knowledge/`. Tính năng chưa chắc chắn thì ghi `[CẦN XÁC NHẬN]`.
3. **Lộ trình triển khai theo giai đoạn**: Giai đoạn 1 giải quyết pain lớn nhất, nhanh thấy kết quả (quick win). Giai đoạn 2–3 mở rộng.
4. **Ước tính ROI**: liệt kê rõ giả định (số người, số giờ/tuần, lương bình quân), công thức và kết quả. Đưa ra 2 kịch bản: thận trọng và kỳ vọng.
5. **Rủi ro deal** và cách xử lý: đối thủ, người phản đối nội bộ, ngân sách…

Cập nhật trạng thái và fit score trong `knowledge/pipeline.csv`.

## Bước tiếp theo
Gợi ý `/pitch-deck` và `/demo-builder`.
