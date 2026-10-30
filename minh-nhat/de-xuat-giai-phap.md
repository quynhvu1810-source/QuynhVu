# Đề xuất giải pháp số hóa – Công ty TNHH Xây dựng Thương mại Dịch vụ Minh Nhật

## 1. Hồ sơ khách hàng

| Hạng mục | Thông tin |
|---|---|
| Tên doanh nghiệp | Công ty TNHH Xây dựng Thương mại Dịch vụ Minh Nhật |
| Địa điểm | Quảng Ninh |
| Quy mô | ~25 nhân sự văn phòng / điều phối; sản xuất bằng máy móc, không có công nhân trực tiếp |
| Lĩnh vực | Thương mại + sản xuất vật liệu xây dựng; kinh doanh máy xúc, máy ủi; vận chuyển vật liệu bằng xe ben |
| Hoạt động chính | Sản xuất gạch không nung, cấu kiện; kinh doanh thiết bị; giao nhận – vận chuyển |
| Công cụ hiện tại | Zalo, trao đổi trực tiếp |
| Nhu cầu | (1) Giao việc, theo dõi tiến độ, mức độ hoàn thành; (2) Quản lý tài sản, thiết bị, chu kỳ bảo dưỡng |

## 2. Vấn đề hiện tại (khi dùng Zalo + trao đổi miệng)

- Việc giao qua tin nhắn bị trôi, không có hạn chót, người chịu trách nhiệm và trạng thái rõ ràng.
- Lãnh đạo không có bức tranh tổng thể: việc nào trễ, ai đang quá tải, đơn giao hàng nào chưa xong.
- Tài sản giá trị lớn (máy xúc, máy ủi, xe ben, dây chuyền ép gạch) không có hồ sơ tập trung; bảo dưỡng dựa vào trí nhớ → dễ quá hạn, hỏng hóc đột xuất, dừng sản xuất/giao hàng.
- Không lưu được lịch sử sửa chữa, chi phí, giờ máy/km để ra quyết định thay thế, thanh lý.

## 3. Mục tiêu

1. 100% công việc được giao trên hệ thống, có người phụ trách – hạn chót – trạng thái.
2. Báo cáo tiến độ theo phòng ban/dự án/cá nhân xem được theo thời gian thực.
3. 100% tài sản, thiết bị có mã, hồ sơ, người quản lý và lịch bảo dưỡng.
4. Nhắc bảo dưỡng tự động trước hạn; không còn thiết bị quá hạn bảo dưỡng.

## 4. Phạm vi giải pháp

### 4.1. Phân hệ Quản lý công việc

**Cấu trúc không gian làm việc (dự án / nhóm việc) đề xuất**

| Nhóm việc | Phụ trách | Ví dụ công việc |
|---|---|---|
| Sản xuất gạch không nung & cấu kiện | Quản đốc / điều phối sản xuất | Lập kế hoạch ca máy, nhập nguyên liệu, kiểm tra chất lượng lô |
| Kinh doanh vật liệu | Phòng kinh doanh | Báo giá, chốt đơn, theo dõi công nợ |
| Kinh doanh máy xúc, máy ủi | Phòng kinh doanh thiết bị | Tư vấn, demo máy, hợp đồng, bàn giao |
| Giao nhận – vận chuyển (xe ben) | Điều phối vận tải | Điều xe, giao hàng đến công trình, xác nhận biên bản giao |
| Hành chính – Kế toán | HCNS, Kế toán | Hồ sơ pháp lý, thanh toán, chứng từ |

**Quy trình mẫu: Đơn giao vật liệu đến công trình**

```
Tiếp nhận đơn → Kiểm tra tồn kho/lịch sản xuất → Điều xe ben & tài xế
→ Xuất kho → Giao hàng tại công trình (ảnh + biên bản) → Đối soát & thu tiền → Hoàn thành
```

**Trường thông tin chuẩn cho mỗi công việc:** người giao, người thực hiện, người theo dõi, hạn chót, mức ưu tiên, % hoàn thành, checklist con, tệp/ảnh đính kèm, bình luận thay cho Zalo.

**Trạng thái:** Mới → Đang làm → Chờ duyệt → Hoàn thành / Quá hạn.

**Báo cáo:** việc quá hạn theo người/phòng ban, tỷ lệ hoàn thành đúng hạn theo tuần/tháng, khối lượng việc từng nhân sự.

### 4.2. Phân hệ Quản lý tài sản – thiết bị – bảo dưỡng

**Danh mục tài sản đề xuất**

| Nhóm | Ví dụ | Chỉ số theo dõi bảo dưỡng |
|---|---|---|
| Xe ben | Xe ben 15 tấn, 25 tấn | Km, ngày đăng kiểm, bảo hiểm |
| Máy công trình | Máy xúc, máy ủi (dùng nội bộ / hàng kinh doanh / cho thuê) | Giờ máy |
| Dây chuyền sản xuất | Máy ép gạch không nung, máy trộn, băng tải, khuôn | Số ca / số sản phẩm, định kỳ theo tháng |
| Thiết bị phụ trợ | Máy phát điện, xe nâng, máy nén khí | Giờ chạy, định kỳ |
| Tài sản văn phòng | Máy tính, máy in | Định kỳ |

**Hồ sơ mỗi tài sản:** mã tài sản (VD `XB-01`, `MX-03`, `DC-EP-01`), tên, nhóm, biển số/số khung/số máy, ngày mua, nguyên giá, vị trí/công trình đang hoạt động, người quản lý/tài xế, tình trạng (Đang hoạt động / Đang bảo dưỡng / Hỏng / Thanh lý), giấy tờ (đăng ký, đăng kiểm, bảo hiểm).

**Kế hoạch bảo dưỡng mẫu**

| Thiết bị | Hạng mục | Chu kỳ | Nhắc trước |
|---|---|---|---|
| Xe ben | Thay dầu động cơ, lọc dầu | 5.000 km hoặc 3 tháng | 7 ngày |
| Xe ben | Đăng kiểm | Theo hạn đăng kiểm | 30 ngày |
| Xe ben | Bảo hiểm TNDS | 12 tháng | 30 ngày |
| Máy xúc / máy ủi | Bảo dưỡng cấp 1 (dầu, lọc, mỡ) | 250 giờ máy | 20 giờ |
| Máy xúc / máy ủi | Bảo dưỡng cấp 2 (thủy lực, gầm) | 1.000 giờ máy | 50 giờ |
| Máy ép gạch | Kiểm tra khuôn, xi lanh thủy lực | Hàng tháng | 3 ngày |
| Máy trộn, băng tải | Vệ sinh, tra dầu mỡ | Hàng tuần | 1 ngày |

**Luồng xử lý:** đến hạn → hệ thống tự tạo công việc bảo dưỡng giao cho người phụ trách → thực hiện, ghi chi phí, vật tư thay thế, ảnh → cập nhật chỉ số (km/giờ máy) và tính lại hạn kế tiếp. Sự cố đột xuất được báo hỏng ngay trên hệ thống (thay cho nhắn Zalo).

**Báo cáo:** thiết bị sắp/đã quá hạn bảo dưỡng, chi phí sửa chữa theo thiết bị/tháng, thời gian dừng máy, tài sản theo vị trí/công trình.

## 5. Phân quyền

| Vai trò | Quyền chính |
|---|---|
| Giám đốc | Xem toàn bộ báo cáo, giao việc mọi phòng ban, duyệt chi phí sửa chữa lớn |
| Trưởng bộ phận | Giao/duyệt việc trong bộ phận, xem báo cáo bộ phận |
| Nhân viên | Nhận việc, cập nhật tiến độ, báo hỏng thiết bị |
| Phụ trách tài sản / kỹ thuật | Quản lý hồ sơ tài sản, lịch và nhật ký bảo dưỡng |
| Kế toán | Xem nguyên giá, chi phí sửa chữa, khấu hao |

## 6. Lộ trình triển khai (~6 tuần)

| Giai đoạn | Thời gian | Nội dung | Kết quả |
|---|---|---|---|
| 1. Khảo sát | Tuần 1 | Phỏng vấn lãnh đạo, trưởng bộ phận; thu thập danh sách nhân sự, tài sản, lịch bảo dưỡng hiện có | Bản chốt yêu cầu |
| 2. Cấu hình | Tuần 2–3 | Tạo tài khoản, phòng ban, nhóm việc, quy trình mẫu; nhập danh mục tài sản và kế hoạch bảo dưỡng | Hệ thống có dữ liệu thật |
| 3. Đào tạo | Tuần 4 | Đào tạo theo vai trò (lãnh đạo, quản lý, nhân viên, kỹ thuật) – ưu tiên dùng trên điện thoại | 25/25 người sử dụng được |
| 4. Vận hành thử | Tuần 5–6 | Chạy song song; quy định "việc không có trên hệ thống coi như chưa giao" | Bỏ giao việc qua Zalo |
| 5. Nghiệm thu | Cuối tuần 6 | Rà soát chỉ số mục tiêu, điều chỉnh | Biên bản nghiệm thu |

## 7. Dữ liệu cần khách hàng cung cấp

- [ ] Danh sách nhân sự: họ tên, chức vụ, bộ phận, số điện thoại/email
- [ ] Sơ đồ tổ chức và người phê duyệt
- [ ] Danh sách tài sản/thiết bị: tên, biển số/số máy, ngày mua, nguyên giá, người quản lý
- [ ] Hạn đăng kiểm, bảo hiểm của xe ben
- [ ] Số km / giờ máy hiện tại của từng xe, máy
- [ ] Lịch bảo dưỡng theo khuyến cáo nhà sản xuất (nếu có)
- [ ] Các nhóm Zalo đang dùng để giao việc (để chuyển đổi tương ứng)

## 8. Chỉ số đo lường hiệu quả (sau 3 tháng)

- Tỷ lệ công việc giao trên hệ thống ≥ 95%
- Tỷ lệ hoàn thành đúng hạn tăng so với tháng đầu vận hành
- 0 thiết bị quá hạn bảo dưỡng / đăng kiểm / bảo hiểm
- Giảm số lần dừng máy đột xuất của dây chuyền và xe ben
