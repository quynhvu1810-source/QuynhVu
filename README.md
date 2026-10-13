# QuynhVu — Bộ trợ lý AI cho Business Consultant Base.vn

Repo này biến Claude Code thành **trợ lý, chuyên gia cố vấn và nhà quản trị công việc** cho quy trình tư vấn và bán giải pháp Base.vn.

## Cấu trúc

```
CLAUDE.md                 ← "Bộ não": vai trò, quy ước, sơ đồ chuỗi skill (Claude tự đọc mỗi phiên)
.claude/skills/<tên>/     ← Mỗi skill là một bước trong quy trình, gọi bằng /<tên>
knowledge/                ← Kiến thức BẠN cung cấp: sản phẩm, ICP, case study, từ chối, chỉ tiêu, pipeline
deals/<khach>/            ← Hồ sơ từng khách, các skill đọc và ghi nối tiếp nhau
```

## Chuỗi skill

```
/daily-planner  (mỗi sáng: hôm nay làm gì?)
      │
/lead-triage → /account-research → /discovery-call → /qualify-solution → /pitch-deck + /demo-builder → /follow-up
                                          ▲                                                                   │
                                          └────────────── /sales-coach (review, roleplay bất kỳ lúc nào) ─────┘
```

| Vai | Skill |
|---|---|
| Trợ lý | `/lead-triage`, `/account-research`, `/discovery-call`, `/qualify-solution`, `/pitch-deck`, `/demo-builder`, `/follow-up` |
| Chuyên gia cố vấn | `/sales-coach` |
| Nhà quản trị công việc | `/daily-planner` |

## Hướng dẫn bắt đầu (3 bước)

### Bước 1 — Nạp kiến thức (quan trọng nhất)
Chất lượng đầu ra phụ thuộc vào `knowledge/`. Hãy điền theo thứ tự ưu tiên:
1. `base-products.md`: module, tính năng, điểm khác biệt, điểm "wow" khi demo.
2. `icp.md`: khách hàng lý tưởng và cách chấm điểm lead.
3. `case-studies.md`, `objections.md`: case thật và câu trả lời từ chối hiệu quả.
4. `goals.md`: chỉ tiêu của bạn.
5. `templates/`: đặt file slide mẫu (.pptx) của công ty vào đây.

> Mẹo: gửi tài liệu sản phẩm (PDF, slide, link) rồi nói *"đọc tài liệu này và điền vào knowledge/base-products.md"*.

### Bước 2 — Chạy thử với một khách thật
```
/account-research Công ty ABC
/discovery-call            ← trước cuộc gọi: lấy kịch bản
(gọi điện, rồi dán ghi chú vào)
/discovery-call            ← sau cuộc gọi: chuẩn hóa biên bản
/qualify-solution
/pitch-deck
/demo-builder
/follow-up
```
Bạn cũng có thể nói tự nhiên, ví dụ *"vừa gọi xong cho ABC, đây là ghi chú…"*, Claude sẽ tự chọn đúng skill.

### Bước 3 — Tinh chỉnh liên tục
- Đầu ra chưa đúng ý? Sửa trực tiếp file `SKILL.md` tương ứng, hoặc nói *"sửa skill pitch-deck: luôn thêm slide so sánh đối thủ"*.
- Bài học sau mỗi deal sẽ được lưu vào `knowledge/lessons.md`, giúp trợ lý ngày càng hiểu cách bạn làm việc.
- Muốn thêm skill mới (ví dụ `/competitor-battlecard`)? Tạo thư mục `.claude/skills/<tên>/SKILL.md` theo mẫu có sẵn, hoặc nhờ Claude tạo.

## Cấu trúc một skill
```markdown
---
name: ten-skill
description: Skill làm gì + KHI NÀO dùng (các câu nói kích hoạt). Claude dựa vào dòng này để tự chọn skill.
---
# Hướng dẫn chi tiết: đầu vào, các bước, định dạng đầu ra, bước tiếp theo
```

## ⚠️ Bảo mật
- Giữ repo ở chế độ **Private** vì `deals/` và `pipeline.csv` chứa thông tin khách hàng.
- Tuân thủ chính sách dữ liệu của Base.vn. Ẩn danh thông tin nhạy cảm khi cần.
