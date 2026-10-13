# Qualification & Solution mapping — Lilama, Bộ phận Thi công

> ⚠️ `knowledge/base-products.md` chưa được điền. Mọi tính năng Base dưới đây dựa trên hiểu biết chung và đều cần bạn đối chiếu `[CẦN XÁC NHẬN]` trước khi nói với khách.

## 1. Fit score: **48/100 → TIẾP TỤC CÓ ĐIỀU KIỆN**

| Tiêu chí | Trọng số | Điểm | Ghi chú |
|---|---|---|---|
| Pain rõ ràng và cấp bách | 30 | 20 | Pain rõ (Fastcons lỗi, hỗ trợ kém), nhưng chưa rõ mức cấp bách |
| Tiếp cận được người quyết định | 25 | 10 | Anh Vinh có thể chỉ là người đề xuất. Doanh nghiệp nhà nước thường có nhiều cấp duyệt |
| Ngân sách phù hợp | 20 | 8 | Chưa có thông tin. Quy mô 10–12 user nên giá trị deal ban đầu nhỏ |
| Timeline ≤ 3 tháng | 15 | 5 | Chưa có thông tin |
| Phù hợp ICP | 10 | 5 | Base mạnh về vận hành và phê duyệt; khách lại đang tìm **phần mềm chuyên ngành xây dựng** |

**Kết luận:** Chưa nên làm slide và demo ngay. Cần một cuộc gọi qualify thứ hai trước, vì 2 rủi ro có thể làm mất deal muộn:
1. **Lệch kỳ vọng sản phẩm.** Nếu anh Vinh muốn một phần mềm thay thế Fastcons trọn gói (dự toán, kho, giá vật tư), nhu cầu #3 và một phần #5 không phải thế mạnh của nền tảng vận hành như Base.
2. **Người quyết định và thủ tục mua sắm** của doanh nghiệp nhà nước.

## 2. Mapping nhu cầu → Base

| # | Nhu cầu | Giải pháp Base (đề xuất) | Mức phù hợp |
|---|---|---|---|
| 1 | Dữ liệu thời gian thực từ công trường | App di động Base: cập nhật công việc, bình luận, gửi ảnh từ hiện trường, thông báo tức thì cho văn phòng `[CẦN XÁC NHẬN]` | 🟢 Mạnh |
| 2 | Tiến độ bằng Gantt | **Base Wework**: dự án, đầu việc theo hạng mục, giao việc, deadline, góc nhìn Gantt `[CẦN XÁC NHẬN có Gantt, phụ thuộc giữa các công việc, baseline]` | 🟡 Khá, nếu khách không đòi lập tiến độ chuyên sâu kiểu MS Project |
| 3 | Vật tư, kho công trình | **Base Request**: đề xuất cấp vật tư có phê duyệt. **Base Workflow**: quy trình nhập/xuất. Sổ tồn kho chi tiết theo công trình `[CẦN XÁC NHẬN Base có module kho hay không]` | 🔴 Yếu, nhiều khả năng cần giữ hoặc tích hợp phần mềm kho/kế toán |
| 4 | Nhật ký thi công, báo cáo | **Base Workflow / Request**: mẫu nhật ký ngày (khối lượng, nhân lực, thiết bị, thời tiết, ảnh), luồng duyệt Giám sát → Chỉ huy trưởng → Quản lý, báo cáo tổng hợp `[CẦN XÁC NHẬN trường dữ liệu, báo cáo]` | 🟢 Mạnh |
| 5 | Chi phí, tài chính | **Base Request**: tạm ứng, đề nghị thanh toán, phê duyệt nhiều cấp, theo dõi theo công trình. Dòng tiền thu/chi và cảnh báo vượt định mức `[CẦN XÁC NHẬN module tài chính của Base]` | 🟡 Mạnh ở khâu phê duyệt; hạch toán và định mức cần xác nhận |

### Định vị đề xuất
Không nên đối đầu Fastcons trên mặt trận "phần mềm xây dựng trọn gói", vì đó là sân nhà của phần mềm chuyên ngành. Nên định vị Base là **nền tảng điều hành công trường**, mạnh nhất ở các nhu cầu #1, #2, #4 và khâu phê duyệt của #5:
> "Anh Vinh đang mất kiểm soát vì thông tin từ công trường về chậm và phê duyệt bị nghẽn. Base giải quyết phần điều hành đó. Phần sổ kho và hạch toán có thể giữ ở hệ thống kế toán, hoặc tích hợp."

Nếu ở cuộc gọi 2, khách khẳng định **bắt buộc** phải có kho và dự toán trong cùng một phần mềm, hãy cân nhắc qualify out (dừng deal) sớm, hoặc hỏi đội sản phẩm Base trước khi demo.

## 3. Lộ trình triển khai (nếu tiếp tục)
| Giai đoạn | Phạm vi | Người dùng | Quick win |
|---|---|---|---|
| 1 (tháng 1) | Nhật ký thi công + tiến độ công trình (Wework) | 10–12 người đội thi công | Báo cáo ngày có ảnh, văn phòng nắm tình hình không cần gọi điện |
| 2 (tháng 2–3) | Đề xuất vật tư, tạm ứng, thanh toán (Request/Workflow) | + kế toán, mua hàng | Rút ngắn thời gian duyệt tạm ứng |
| 3 (mở rộng) | Khối văn phòng 60 người: công việc, quy trình, HRM | Văn phòng | **Land & expand** sang tổng công ty |

## 4. Ước tính ROI (chỉ phần tiết kiệm thời gian)
**Giả định** (cần khách xác nhận): 12 người dùng; lương bình quân 20 triệu đồng/tháng ≈ 113.600 đ/giờ (176 giờ/tháng); 4,33 tuần/tháng.

| Hạng mục | Thận trọng | Kỳ vọng |
|---|---|---|
| Lập và gửi nhật ký, báo cáo (giờ/tuần/người × 12 người) | 2 × 12 = 24 giờ | 3 × 12 = 36 giờ |
| Văn phòng tổng hợp báo cáo, đi hỏi tiến độ (giờ/tuần) | 4 giờ | 6 giờ |
| **Tổng giờ/tháng** | 28 × 4,33 ≈ **121 giờ** | 42 × 4,33 ≈ **182 giờ** |
| **Giá trị/tháng** | ≈ **13,8 triệu đồng** | ≈ **20,7 triệu đồng** |

Chưa tính: giảm thất thoát và vượt định mức vật tư, giảm chậm tiến độ. Đây thường là khoản lớn hơn nhiều; hãy hỏi khách một công trình tiêu biểu bị vượt chi phí bao nhiêu để định lượng.
Chi phí Base: `[CẦN XÁC NHẬN bảng giá]`.

## 5. Rủi ro deal và cách xử lý
| Rủi ro | Xử lý |
|---|---|
| Lệch kỳ vọng: khách cần phần mềm xây dựng chuyên sâu | Hỏi thẳng ở cuộc gọi 2 (câu Q3–Q5 trong script); định vị Base là nền tảng điều hành |
| Anh Vinh không phải người quyết định | Xin anh Vinh giới thiệu, hoặc mời người duyệt vào buổi demo |
| Thủ tục mua sắm doanh nghiệp nhà nước (chào giá, nhiều cấp) | Hỏi sớm quy trình; chuẩn bị hồ sơ năng lực và báo giá chuẩn |
| Hợp đồng Fastcons còn hiệu lực | Hỏi thời điểm hết hạn; đề xuất chạy thử song song |
| Công trường sóng yếu, người dùng ngại công nghệ | Xác nhận khả năng dùng offline `[CẦN XÁC NHẬN]`; demo trên điện thoại, thao tác dưới 1 phút |
| Giá trị deal nhỏ (12 user) | Thiết kế lộ trình mở rộng sang văn phòng 60 người |
