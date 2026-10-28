# Hồ sơ khách hàng: Công ty CP Dệt và May Hồng Hải

> Cập nhật: 28/10/2026 · Người phụ trách: Quỳnh Vũ (Base Enterprise)
> Buổi làm việc: **14:30 – 15:30, 28/10/2026 · Online qua Google Meet**

## 0. Cập nhật sau buổi làm việc 28/10/2026

Khách đã xác nhận mô hình kinh doanh. **Hồng Hải may màn, tự sản xuất và làm thương mại, bán cho các nhà phân phối trên cả nước.** Mô hình này thuộc nhóm *thiết kế lưu kho* (sản xuất để tồn kho, có bổ sung theo đơn), không phải gia công hay FOB như giả thuyết ban đầu. Từ mục 1 trở đi là phân tích trước buổi họp; khi hai phần khác nhau, lấy theo mục 0.

### 0.1. Nhu cầu khách nêu

| Bộ phận | Nhu cầu | Ý nghĩa |
| --- | --- | --- |
| Sản xuất | Theo dõi sản phẩm đang ở khâu nào | Cần thấy tiến độ theo công đoạn của từng lệnh sản xuất |
| Kinh doanh | Kiểm tra kho có hàng không. Có thì giữ hàng cho khách (bên A); không có thì làm lệnh đặt hàng cho sản xuất | Cần xem tồn kho tức thời, giữ hàng theo đơn, tự sinh lệnh sản xuất cho phần thiếu |
| Kinh doanh | Dự tính tháng sau bán bao nhiêu thì tháng trước phải sản xuất để tồn | Cần lập kế hoạch sản xuất theo dự báo bán |
| Kho | Biết mỗi mặt hàng tốn bao nhiêu nguyên vật liệu (định mức) và kho còn đủ NVL không | Cần định mức NVL (BOM) cho từng mã và đối chiếu với tồn NVL |
| Công lương | Giao việc cho công nhân may; kiểm soát họ nhận hàng gì, sau khi nhận xong thì chuyển… | Cần phiếu giao nhận bán thành phẩm và tính lương theo sản phẩm. *Ghi chú gốc bị cắt ở đây, cần bổ sung* |

### 0.2. Chuỗi giá trị đã xác nhận

Dự báo bán (Kinh doanh) → Kế hoạch sản xuất tồn kho → Kiểm tra NVL theo định mức → Mua NVL nếu thiếu → **Giao bán thành phẩm cho công nhân may (công lương)** → Theo dõi công đoạn → QC → **Nhập kho thành phẩm** → Nhà phân phối đặt hàng → Kiểm tồn, giữ hàng hoặc tự sinh lệnh sản xuất → Giao hàng, công nợ

Có hai khâu trọng tâm:
- **Tồn kho thành phẩm:** đúng như mô hình thiết kế lưu kho.
- **Công lương:** kiểm soát hàng phát cho công nhân may và tính lương theo sản phẩm.

### 0.3. Giải pháp điều chỉnh

| Nhu cầu | Giải pháp Base | Cách chạy |
| --- | --- | --- |
| Kiểm tồn, giữ hàng cho nhà phân phối | Base Inventory + CRM/Sales | Kinh doanh tạo đơn → hệ thống hiện tồn khả dụng → đủ thì giữ hàng cho đơn; thiếu thì tự tạo lệnh sản xuất cho phần thiếu |
| Kế hoạch sản xuất tồn kho | BPM (quy trình lập kế hoạch tháng) + báo cáo | Số cần sản xuất = dự báo bán tháng sau + tồn an toàn − tồn hiện có − hàng đang sản xuất |
| Định mức NVL, kiểm NVL | Inventory (định mức theo mã) + Request (đề nghị mua) | Khi tạo lệnh, hệ thống tính NVL cần theo định mức, so với tồn; thiếu thì sinh đề nghị mua |
| Theo dõi công đoạn | BPM (lệnh sản xuất theo công đoạn) | Mỗi lệnh có các bước, ai đang giữ, còn bao nhiêu |
| Công lương | BPM (phiếu giao nhận cho công nhân) + Payroll | Phát bán thành phẩm theo phiếu → công nhân trả hàng → QC đạt → tự cộng sản lượng vào lương sản phẩm |

### 0.4. Cần hỏi tiếp

1. Hoàn thiện ý về công lương: "sau khi nhận xong chuyển…" sang đâu? Trả lại xưởng, chuyển công đoạn khác hay QC?
2. Công nhân may làm tại xưởng hay nhận hàng về nhà (gia công ngoài)? Bao nhiêu người?
3. Đơn giá công tính theo sản phẩm hay theo công đoạn? Hàng lỗi có bị trừ không?
4. Có bao nhiêu mã màn (kích thước, chất liệu, màu)? Đã có định mức NVL cho từng mã chưa?
5. Có bao nhiêu nhà phân phối? Dự báo bán hiện làm thế nào, ai làm?
6. Giữ hàng cho nhà phân phối tối đa bao lâu? Hai đơn cùng cần một mã thì ưu tiên thế nào?
7. NVL chính là những gì (vải màn, viền, chỉ, bao bì)? Mua từ ai, thời gian giao bao lâu?
8. Có mấy kho (NVL, bán thành phẩm, thành phẩm)? Có kho ở chi nhánh hay tỉnh khác không?

### 0.5. Cần chỉnh lại trong deck và tài liệu
- Demo hiện dùng đơn FOB áo polo (PL-M2630), cần đổi sang kịch bản màn sản xuất tồn kho, bán cho nhà phân phối.
- Slide bài toán, chuỗi giá trị, giải pháp, luồng 3 quy trình: chuyển trọng tâm sang tồn kho thành phẩm, kế hoạch sản xuất, định mức NVL, công lương.

## 1. Tóm tắt

Hồng Hải là xưởng dệt may hoạt động khoảng 20 năm, quy mô 30–40 người, hiện điều hành bằng Zalo và Excel. Năm nay doanh thu dự kiến tăng 30%, mục tiêu năm sau tăng 80%. Với cách vận hành hiện tại, CEO trở thành nút thắt thông tin.

- **Vấn đề gốc:** mọi thông tin dồn về CEO qua Zalo; quy trình chưa viết thành văn bản; không có số liệu theo thời gian thực.
- **Đề xuất:** số hóa theo luồng Đơn hàng → Mua NPL → Kho → Sản xuất → Giao hàng, đi kèm HRM và CRM. Triển khai 3 giai đoạn trong khoảng 6 tháng.
- **Định vị so với MISA:** Base lo phần vận hành, MISA giữ phần kế toán. Hai bên bổ trợ, không đối đầu về giá.

## 2. Thông tin doanh nghiệp

| Hạng mục | Thông tin |
| --- | --- |
| Tên pháp lý | Công ty Cổ phần Dệt và May Hồng Hải |
| Mã số thuế | 0104567234. Đầu số 01 là đăng ký tại Hà Nội. **Chưa xác minh được** trên nguồn công khai |
| Ngành | Sản xuất dệt may |
| Thời gian hoạt động | Khoảng 20 năm |
| Quy mô | 30–40 nhân sự, trong đó khoảng 10 người văn phòng |
| Phòng ban | Hành chính nhân sự, Kế toán, Kinh doanh (2 người), Kho, Sản xuất |
| Công cụ hiện tại | Zalo để trao đổi, Excel để quản lý. Chưa có quy trình viết thành văn bản |
| Bán hàng | Chủ yếu khách quen, chưa chạy quảng cáo, sắp mở rộng lĩnh vực kinh doanh |
| Tăng trưởng | +30% doanh thu năm nay, mục tiêu +80% năm sau. Đang tuyển thêm người |
| Người liên hệ, người quyết định | Anh Hải, CEO. Tự tìm hiểu và so sánh Base với MISA |
| Đối thủ trong deal | MISA, báo giá khoảng 140 triệu đồng/năm cho gói 2 năm, năm đầu cao hơn |
| Phân hệ quan tâm | Sản xuất, Bán hàng, Kho, HRM, Mua hàng. BDR đã trao đổi phần kho |

CEO quan tâm nhất tới ba điều: chi phí triển khai, Base khác MISA ở đâu, và hệ thống có theo kịp khi công ty lớn lên không.

> Ghi chú BDR bị cắt ở câu "Khách hàng đang so sánh Base và MISA, đặc biệt quan tâm đến sự…". Cần hỏi lại BDR.

## 3. Nỗi đau (pain point)

| # | Nỗi đau | Khâu |
| --- | --- | --- |
| A | Giao việc, theo dõi tiến độ qua Zalo, mất nhiều thời gian của CEO | Quản trị chung |
| B | Quy trình sản xuất, bán hàng chưa chuẩn hóa | Toàn chuỗi |
| C | Không thấy tiến độ chuyền và sản lượng theo ngày | Sản xuất |
| D | Tồn kho NPL, thành phẩm không cập nhật tức thì | Kho |
| E | Mua NPL, duyệt chi chưa có luồng phê duyệt | Mua hàng |
| F | Tăng trưởng 80%: phải tuyển thêm người và tìm khách mới, trong khi đội kinh doanh chỉ có 2 người | Nhân sự, Bán hàng |

## 4. Bối cảnh ngành và mô hình kinh doanh

Chưa biết Hồng Hải làm theo mô hình nào. Với quy mô và cách bán hàng hiện tại, nhiều khả năng đây là xưởng gia công hoặc sản xuất theo đơn B2B. Đây là giả thuyết, cần xác nhận trong buổi gặp.

**FOB là gì?** FOB (Free On Board) là một điều kiện Incoterms: người bán chịu trách nhiệm tới khi hàng lên tàu ở cảng xuất. Trong ngành may, FOB còn chỉ hình thức "mua nguyên liệu, bán thành phẩm": xưởng tự mua NPL, sản xuất rồi bán trọn sản phẩm cho khách.

| Tiêu chí | Gia công (CMT) | FOB | Thiết kế lưu kho |
| --- | --- | --- | --- |
| Ai mua NPL | Khách | Xưởng, theo đơn | Xưởng, theo dự báo |
| Sản xuất khi nào | Khi có đơn | Khi có đơn | Trước khi có khách |
| Vốn lưu động cần | Thấp | Trung bình đến cao | Cao nhất |
| Rủi ro chính | Năng suất thấp, trễ hạn, lệch NPL khi quyết toán | Mua sai, giá thành vượt giá báo | Tồn kho, lỗi mốt, chết vốn |
| KPI cốt lõi | Sản phẩm/người/ngày, tỷ lệ giao đúng hạn | Giá thành thực tế so với giá báo, công nợ | Vòng quay tồn kho, tỷ lệ bán hết |
| Khâu trọng tâm | Sản xuất | Mua NPL | Kho thành phẩm |
| Phân hệ ưu tiên | Sản xuất, HRM (lương sản phẩm), kho NPL khách gửi | Mua hàng, Kho NPL, Sản xuất (giá thành) | Kho thành phẩm, CRM và bán hàng, kế hoạch sản xuất |
| Thông điệp với CEO | Biết mỗi chuyền làm được bao nhiêu mỗi ngày, lương tính tự động | Biết mỗi mã lãi thật bao nhiêu trước khi giao | Biết mẫu nào bán chạy, tránh hàng tồn chết vốn |

Đặc thù ngành cần lưu ý khi thiết kế giải pháp:
- Mỗi mã hàng có ma trận màu × size và định mức NPL riêng, nên Excel rất dễ sai khi nhiều đơn chạy cùng lúc.
- Trễ giao hàng có thể bị phạt hoặc mất khách, nên cần thấy tiến độ cắt → may → hoàn thiện → đóng gói theo ngày.
- Công nhân thường hưởng lương sản phẩm, nên HRM phải lấy số liệu từ sản xuất.
- Khách lớn và khách xuất khẩu thường đòi truy xuất NPL và hồ sơ tuân thủ.

## 5. Chuỗi giá trị

### 5.1. Chuỗi giá trị hiện tại (giả thuyết từ ghi chú BDR)

| Khâu | Cách làm hiện tại | Điểm nghẽn |
| --- | --- | --- |
| Bán hàng | 2 người, khách quen, chưa quảng cáo | Chưa có CRM, báo giá rời rạc |
| Mua NPL | Đặt qua Zalo, theo thói quen | Chưa có định mức, khó kiểm soát chi |
| Kho NPL | Sổ sách Excel, nhập tay | Tồn kho không cập nhật tức thì |
| Sản xuất | Cắt, may, hoàn thiện, QC | Không thấy tiến độ theo công đoạn |
| Giao hàng | Theo dõi qua Zalo và Excel | Rủi ro trễ hạn khi đơn tăng 80% |

Các hoạt động hỗ trợ:
- **Quản trị chung:** CEO nhận và điều phối mọi việc qua Zalo. Đây là nút thắt chính.
- **Nhân sự:** đang tuyển thêm người; chấm công và tính lương làm thủ công.
- **Kế toán:** tách rời vận hành, số liệu nhập lại từ Excel.
- **Công nghệ, quy trình:** chỉ có Zalo và Excel, chưa có quy trình viết thành văn bản.

### 5.2. Chuỗi giá trị theo 3 mô hình (★ là khâu nên số hóa trước)

**Gia công (CMT), khách gửi NPL**
Nhận đơn (báo đơn giá công) → Nhận NPL (đối chiếu NPL khách gửi) → Kho NPL (tách kho theo khách, theo đơn) → **★ Sản xuất** (năng suất chuyền, lương sản phẩm) → Giao hàng (đúng hạn, đúng số lượng) → Quyết toán (đối chiếu NPL thừa, thiếu)

**FOB, xưởng tự mua NPL**
Báo giá (tính giá FOB theo định mức) → Định mức (duyệt mẫu, chốt định mức) → **★ Mua NPL** (ứng vốn, mua đúng hạn, đúng giá) → Kho NPL (nhập, xuất theo lệnh sản xuất) → Sản xuất (tiến độ, giá thành từng mã) → Giao hàng (giao, thu tiền, công nợ)

**Thiết kế lưu kho, sản xuất trước bán sau**
Thiết kế (mẫu theo mùa) → Kế hoạch (dự báo bán, số lượng sản xuất) → Mua NPL (theo kế hoạch) → Sản xuất (theo lô, giá thành lô) → **★ Tồn kho thành phẩm** (theo mẫu, màu, size) → Bán hàng (đa kênh, xả hàng tồn)

## 6. Giải pháp đề xuất

| Nỗi đau | Nhu cầu số hóa | Giải pháp Base | Ưu tiên |
| --- | --- | --- | --- |
| CEO mất thời gian với Zalo, Excel | Giao việc, theo dõi, báo cáo tập trung | Base Project, Request, Meeting, Message; màn hình điều hành cho CEO | Cao |
| Không có số liệu tức thời | Sản lượng theo công đoạn, tồn kho NPL và thành phẩm | Base BPM (lệnh sản xuất), Base Inventory | Cao |
| Quy trình chưa chuẩn hóa | Luồng có bước, người phụ trách, hạn xử lý | Base BPM: nhận đơn → duyệt mẫu → mua NPL → sản xuất → QC → giao | Cao |
| Kinh doanh 2 người, chỉ có khách quen | Quản lý khách, cơ hội, báo giá, lịch sử đơn | Base CRM, Sales | Trung bình; lên Cao nếu mở lĩnh vực mới |
| Mua NPL khó kiểm soát | Đề nghị mua theo định mức, phê duyệt | Base Request, quy trình mua hàng trên BPM | Trung bình |
| Tuyển thêm người, lương tính tay | Tuyển dụng, chấm công, lương sản phẩm | Base E-Hiring, Timesheet, Payroll | Trung bình |
| Kế toán tách rời vận hành | Đồng bộ dữ liệu sang sổ sách | Giữ phần mềm kế toán hiện có, kết nối dữ liệu | Thấp (giai đoạn sau) |

**Màn hình điều hành của CEO:** đơn hàng trễ tiến độ, đề nghị mua NPL chờ duyệt, NPL sắp hết và tồn thành phẩm, sản lượng từng chuyền trong ngày.

**Ba quy trình nối nhau theo một đơn hàng (mỗi đơn giữ một mã xuyên suốt):**
- **QT1 – Nhận đơn, mua NPL:** Kinh doanh nhận đơn → Duyệt mẫu, chốt định mức → Đề nghị mua NPL → CEO duyệt theo hạn mức → Đặt hàng nhà cung cấp → NPL về kho
- **QT2 – Sản xuất:** Lệnh sản xuất → Cắt → May → Hoàn thiện → QC → Đạt thì nhập kho thành phẩm, không đạt thì sửa hàng
- **QT3 – Giao hàng, thanh toán:** Đóng gói → Xuất kho → Giao khách → Đối chiếu NPL, công nợ → Kế toán ghi nhận → Thu tiền → Đóng đơn

**Luồng duyệt đề nghị mua NPL, thanh toán:** Người đề nghị (kho, sản xuất; tạo phiếu theo định mức) → Trưởng bộ phận → Kế toán (kiểm tra chứng từ, ngân sách) → CEO (trên hạn mức [__] triệu).
Quy tắc: chỉ mua NPL khi có đơn hàng và định mức được duyệt; mua ngoài định mức phải ghi lý do, CEO duyệt riêng.

### Danh mục 16 quy trình đề xuất (★ là ưu tiên giai đoạn 1–2)

1. ★ Tiếp nhận đơn hàng, báo giá
2. ★ Duyệt mẫu, chốt định mức NPL
3. ★ Đề nghị mua NPL theo đơn hàng
4. ★ Nhập kho NPL, đối chiếu NPL khách gửi
5. ★ Lệnh sản xuất, kế hoạch chuyền
6. ★ Báo cáo sản lượng theo công đoạn
7. Kiểm tra chất lượng (QC) công đoạn, thành phẩm
8. Xuất kho, giao hàng
9. Quyết toán NPL với khách gia công
10. ★ Đề nghị thanh toán nhà cung cấp
11. Đề nghị tạm ứng, hoàn ứng
12. Báo hỏng, sửa chữa máy may
13. Tuyển dụng công nhân
14. Chấm công, tính lương sản phẩm
15. Thu hồi công nợ khách hàng
16. Phát triển mẫu mới, hàng thiết kế

## 7. So sánh Base và MISA

| Tiêu chí | MISA | Base.vn |
| --- | --- | --- |
| Thế mạnh gốc | Kế toán, thuế, hóa đơn | Điều hành: công việc, quy trình, nhân sự, bán hàng |
| Thay Zalo trong điều hành | Cần xác nhận phạm vi gói được báo giá | Project, BPM, Request, Message là lõi sản phẩm |
| Quy trình riêng của xưởng | Cần hỏi khả năng tùy biến | Tự cấu hình luồng trên BPM, không cần lập trình |
| Chi phí 2 năm | ~140 triệu đồng/năm (gói 2 năm), năm đầu cao hơn | Tạm tính 114.720.000 đ cho 2 năm, 20 tài khoản |
| Dùng cùng nhau | Giữ cho kế toán | Vận hành trên Base, kết nối dữ liệu sang kế toán |

Thông điệp chốt: *"Anh có thể giữ MISA cho kế toán. Base giúp anh ra khỏi Zalo và nắm được xưởng mỗi ngày."*

## 8. Lộ trình triển khai (tạm tính)

| Giai đoạn | Thời gian | Nội dung | Cổng kiểm soát |
| --- | --- | --- | --- |
| 1 · Điều hành | Tháng 1–2 | Project (giao việc theo đơn hàng, phòng ban), Request (đề nghị mua, tạm ứng, thanh toán), BPM (luồng nhận đơn đến giao hàng), Message và Meeting thay nhóm Zalo | CEO giao việc và duyệt trên Base, không còn qua Zalo |
| 2 · Xưởng và kho | Tháng 3–4 | Kho NPL và thành phẩm, lệnh sản xuất và sản lượng theo công đoạn, mua NPL theo định mức, chấm công khối sản xuất | Tồn kho và tiến độ chuyền xem được theo ngày |
| 3 · Tăng trưởng | Tháng 5–6 | CRM cho đội kinh doanh, E-Hiring và Payroll (lương sản phẩm), kết nối phần mềm kế toán, báo cáo tổng cho CEO | Sẵn sàng cho mức tăng 80% doanh thu năm sau |

Quy trình triển khai 5 bước: Khảo sát → Thiết lập → Kiểm thử (UAT) → Truyền thông nội bộ → Đào tạo và cấp chứng chỉ.

### KPI đo hiệu quả

| KPI | Cách đo | Giai đoạn |
| --- | --- | --- |
| Giờ/tuần CEO xử lý Zalo và Excel | CEO tự ước tính trước và sau | 1 |
| Tỷ lệ đơn hàng chạy trên hệ thống | Số đơn trên BPM / tổng số đơn | 1 |
| Thời gian duyệt một đề nghị | Từ lúc tạo tới lúc duyệt, lấy từ Request | 1 |
| Độ lệch tồn kho NPL | Kiểm kê thực tế so với số trên hệ thống | 2 |
| Tỷ lệ đơn giao đúng hạn | Số đơn đúng hạn / tổng số đơn | 2 |
| Thời gian chốt lương hàng tháng | Số ngày từ cuối kỳ tới lúc có bảng lương | 3 |
| Số khách, cơ hội mới mỗi tháng | Lấy từ CRM | 3 |

Cam kết đề xuất cho buổi gặp: 100% đơn hàng theo dõi tiến độ trên Base; 100% đề nghị mua NPL và thanh toán đi qua Base; số liệu sản lượng và tồn kho trễ tối đa 1 ngày.

## 9. Báo giá tạm tính (20 tài khoản)

Đơn giá 149.000 đ/tài khoản/tháng; phí triển khai 43.200.000 đ, trả một lần năm đầu; mở rộng thêm 10 tài khoản/lần với giá 17.880.000 đ/năm.

| Phương án | Bản quyền | Phí triển khai | Tổng | Ưu đãi |
| --- | --- | --- | --- | --- |
| 1 năm | 35.760.000 | 43.200.000 | **78.960.000 đ** | Không |
| 2 năm (đối tác gắn bó) | 71.520.000 | 43.200.000 | **114.720.000 đ** | Tặng 3 tháng (8.940.000 đ), 10.000 credits AI, bộ quy trình mẫu ngành dệt may, tư vấn chuẩn hóa quy trình |
| 3 năm (đối tác chiến lược) | 107.280.000 | 43.200.000 | **150.480.000 đ** | Tặng 6 tháng (17.880.000 đ), 10.000 credits AI, bộ quy trình mẫu ngành dệt may, tư vấn chuẩn hóa quy trình |

> Số tài khoản (giả định khoảng 10 người văn phòng cộng tổ trưởng, quản đốc) và phí triển khai cần chốt sau khảo sát.

## 10. Chiến lược pitching khi chưa rõ mô hình

**Nguyên tắc:** nói chắc phần mô hình nào cũng cần (điều hành, giao việc, quy trình, phê duyệt, nhân sự); để mở phần riêng (sản xuất, mua hàng, kho, CRM) và cấu hình sau khảo sát.

1. **Mở đầu bằng nỗi đau khách đã nói:** "Anh chia sẻ là đang mất nhiều thời gian xử lý qua Zalo và Excel, và năm sau muốn tăng 80%…"
2. **Đưa ba sơ đồ chuỗi giá trị để khách tự nhận mình thuộc loại nào:** "Bên anh gần với kiểu nào nhất, hay đang pha cả ba? Khâu nào làm anh đau đầu nhất?"
3. **Demo phần chung,** tức một đơn hàng chạy trên Workflow từ nhận đơn tới giao, **rồi nối sang khâu khách vừa chỉ:**
   - Chủ yếu gia công: sản lượng từng chuyền theo ngày, lương sản phẩm tự động
   - Tự mua vải: đề nghị mua theo định mức, xem mã nào lãi thật
   - Có hàng riêng để bán: tồn kho theo mẫu, màu, size; CRM
   - Pha nhiều loại: lấy loại chiếm tỷ trọng lớn nhất làm chính
4. **Chốt bằng buổi khảo sát, chưa chốt bằng báo giá:** "Phần điều hành em triển khai được ngay. Phần xưởng và kho em cần xuống khảo sát 2–3 tiếng để cấu hình đúng cách bên anh đang làm."

**Những điều nên tránh:** demo sâu một phân hệ riêng khi chưa biết mô hình; báo giá trọn gói 5 phân hệ ngay buổi đầu; hỏi liền một mạch 10 câu discovery.

## 11. Câu hỏi discovery và mục đích

| # | Câu hỏi | Mục đích |
| --- | --- | --- |
| 1 | Gia công, FOB hay hàng tự thiết kế? Tỷ lệ mỗi loại? | Xác định khâu trọng tâm và phân hệ triển khai trước |
| 2 | Mỗi tháng bao nhiêu đơn, bao nhiêu mã chạy cùng lúc? Quy mô đơn trung bình? | Đo mức phức tạp: dùng dự án (Project) hay quy trình chuẩn (BPM); ước số tài khoản; có số liệu để thuyết phục CEO |
| 3 | Khách nội địa, xuất khẩu hay bán lẻ? Có đòi báo cáo tiến độ, truy xuất không? | Biết áp lực bên ngoài: khách xuất khẩu đòi truy xuất là lý lẽ bán hàng mạnh |
| 4 | "Mở rộng lĩnh vực kinh doanh" là sản phẩm, kênh hay thị trường mới? | Quyết định CRM làm ngay hay để sau; gắn lộ trình với mục tiêu +80% |
| 5 | Có mấy chuyền, mấy công đoạn? Sản lượng ghi bằng gì, ai tổng hợp? | Thiết kế cách thu số liệu xưởng; tìm người ủng hộ dự án trong nội bộ |
| 6 | Đã có định mức NPL cho từng mã chưa? Hao hụt vải theo dõi thế nào? | Kiểm tra dữ liệu nền; nếu chưa có định mức phải chuẩn hóa trước; hao hụt là chỗ chứng minh ROI |
| 7 | BDR đã xử lý phần kho tới đâu, khách đã đồng ý gì? | Tránh nói ngược với cam kết của BDR |
| 8 | Công nhân hưởng lương thời gian hay lương sản phẩm? Chấm công bằng gì? | Cấu hình Payroll và Timesheet; có cần kết nối máy chấm công không |
| 9 | Kế toán đang dùng phần mềm nào? Có muốn thay không? | Chọn cách định vị so với MISA |
| 10 | Ngân sách, ai duyệt ngoài CEO, mốc thời gian muốn chạy? | Chốt deal (ngân sách, người quyết định, nhu cầu, thời điểm); chọn gói phù hợp |

Thứ tự hỏi gợi ý: câu 1–4 trước để sắp lại ưu tiên phân hệ ngay tại chỗ; câu 5–9 dùng cho demo và báo giá; câu 10 hỏi cuối, khi CEO đã thấy giá trị.

## 12. Bước tiếp theo

**Thống nhất trong buổi họp 28/10**
- [ ] Tỷ lệ gia công, FOB và hàng thiết kế hiện nay
- [ ] Phản hồi về phương án 1, 2 hay 3 năm
- [ ] Ngày khảo sát xưởng: [__/__/2026]

**Hồng Hải chuẩn bị**
- [ ] Cơ cấu phòng ban và người phụ trách từng khâu
- [ ] File Excel đơn hàng, kho, lương đang dùng
- [ ] Định mức NPL mẫu của 1–2 mã hàng

**Base thực hiện**
- [ ] Xác minh mã số thuế 0104567234 tại [tracuunnt.gdt.gov.vn](https://tracuunnt.gdt.gov.vn)
- [ ] Hỏi BDR phần ghi chú bị cắt và nội dung đã trao đổi về kho
- [ ] Xin chi tiết báo giá MISA (phân hệ, số tài khoản) để so sánh chi phí 3 năm
- [ ] Khảo sát xưởng 2–3 giờ cùng CEO, kế toán, kho, quản đốc
- [ ] Demo theo một đơn hàng thật của Hồng Hải
- [ ] Gửi đề xuất triển khai và báo giá chính thức

## 13. Tài liệu liên quan

- Tài liệu phân tích: [Hồng Hải – Chuỗi giá trị & đề xuất số hóa](https://claude.ai/artifact/GA9Vw573Xc1sC26xeeZjCD)
- Deck trình bày: [Hồng Hải x Base](https://claude.ai/artifact/SFzYaquu7Gt8auqoipAb9D) (27 slide, dựng theo form deck Wealphar x Base)

## 14. Lưu ý về độ tin cậy

- Thông tin doanh nghiệp lấy từ ghi chú của BDR; mã số thuế chưa tra được trên nguồn công khai.
- Mô hình kinh doanh, chuỗi giá trị hiện tại và nhận định về MISA là giả thuyết định tính, cần kiểm lại khi khảo sát.
- Báo giá và lộ trình là tạm tính, chốt sau khảo sát.
