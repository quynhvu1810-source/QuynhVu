---
name: follow-up
description: Soạn email follow-up, tóm tắt buổi demo, proposal và FAQ gửi khách sau cuộc gọi hoặc buổi demo. Dùng khi người dùng nói "viết email", "follow-up", "gửi proposal", "khách im lặng".
---

# Follow-up — Sau cuộc gọi và demo

## Đầu vào
Ghi chú của người dùng về buổi demo (khách phản hồi gì, hỏi gì, ai tham dự) và các file trong `deals/<khach>/`.

## Đầu ra: `07-follow-up.md`
1. **Email tóm tắt** gửi trong 24 giờ: cảm ơn, nhắc lại 3 pain point và cách Base giải quyết, trả lời câu hỏi còn mở, bước tiếp theo có ngày cụ thể. Viết 2 phiên bản: trang trọng và thân thiện.
2. **Proposal ngắn** (khi khách yêu cầu): phạm vi, lộ trình, đầu tư, điều khoản `[CẦN XÁC NHẬN]`.
3. **FAQ** cho người ảnh hưởng nội bộ của khách (IT, HR, kế toán).
4. **Chuỗi nhắc nhở** khi khách im lặng: ngày 3, 7, 14. Mỗi email đưa thêm một giá trị mới (case study, bài viết, ROI), không chỉ hỏi "anh/chị đã cân nhắc chưa".

Cập nhật trạng thái và ngày follow-up kế tiếp trong `knowledge/pipeline.csv`.
