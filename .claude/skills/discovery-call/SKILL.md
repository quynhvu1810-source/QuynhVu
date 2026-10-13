---
name: discovery-call
description: Soạn kịch bản và bộ câu hỏi cho cuộc gọi discovery, hoặc chuyển ghi chú/transcript sau cuộc gọi thành biên bản có cấu trúc. Dùng khi người dùng nói "kịch bản gọi", "câu hỏi khai thác", "vừa gọi xong", "tóm tắt cuộc gọi", hoặc dán ghi chú cuộc gọi.
---

# Discovery call — Trước và sau cuộc gọi

Xác định chế độ: **TRƯỚC** cuộc gọi (chưa có ghi chú) hay **SAU** cuộc gọi (người dùng dán ghi chú hoặc transcript).

## Chế độ TRƯỚC → `02-call-script.md`
Đọc `01-brief.md` nếu có. Soạn:
1. **Mở đầu (30 giây)**: giới thiệu, lý do gọi gắn với tín hiệu trong brief, xin phép 10–15 phút.
2. **Câu hỏi khai thác** theo SPIN, mỗi nhóm 3–4 câu, ưu tiên các giả thuyết pain point trong brief:
   - Situation: cách đang quản lý công việc, phê duyệt, nhân sự hiện nay; công cụ đang dùng.
   - Problem: chỗ nào chậm, sai sót, mất kiểm soát.
   - Implication: hậu quả về thời gian, chi phí, rủi ro.
   - Need-payoff: nếu giải quyết được thì giá trị là gì.
3. **Câu hỏi qualify**: ai ra quyết định, ngân sách, timeline, đã thử giải pháp nào.
4. **Xử lý từ chối**: lấy từ `knowledge/objections.md`, bổ sung theo ngành.
5. **Chốt bước tiếp theo**: đề xuất lịch demo cụ thể (2 lựa chọn thời gian).

## Chế độ SAU → `03-discovery-notes.md`
Chuyển ghi chú thô thành:
- Bối cảnh doanh nghiệp, công cụ hiện tại.
- **Pain point** (trích nguyên lời khách nếu có), mức độ ưu tiên do khách tự nói.
- **BANT**: Budget, Authority (người quyết định, người ảnh hưởng), Need, Timeline.
- Thông tin còn thiếu → câu hỏi cho lần gọi sau.
- Bước tiếp theo đã thống nhất, có ngày cụ thể.
- Cập nhật trạng thái trong `knowledge/pipeline.csv`.

## Bước tiếp theo
Gợi ý `/qualify-solution`.
