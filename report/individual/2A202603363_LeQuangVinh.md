# Báo cáo cá nhân — 2A202603363_LeQuangVinh

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên:Lê Quang Vinh
- MSSV:2A202603363
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm:001
- Link repo nhóm:https://github.com/Hungztv/K5-L3A-Day02-001-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 |Lặp lại|Khi khách hàng gửi yêu cầu bảo hành xe, tôi muốn tự động phân loại yêu cầu và chuyển đến đúng bộ phận, để giảm thời gian xử lý thủ công |Nhân viên CSKH, kỹ thuật viên, khách hàng VinFast |Cần đo thời gian phân loại mỗi yêu cầu, tỷ lệ chuyển sai bộ phận và số yêu cầu tồn đọng |
| 2 |Tốn thời gian |Khi cần kiểm tra tình trạng phòng và lịch đặt phòng, tôi muốn tổng hợp dữ liệu từ các hệ thống quản lý, để nhanh chóng biết phòng nào còn trống |Nhân viên lễ tân, quản lý khách sạn Vinpearl |Cần đo thời gian kiểm tra tình trạng phòng và số trường hợp dữ liệu không đồng bộ |
| 3 |Cần đọc tổng hợp nhiều thông tin |Khi tiếp nhận hồ sơ bệnh nhân trước buổi khám, tôi muốn nhanh chóng nắm được lịch sử khám và các kết quả xét nghiệm liên quan, để chuẩn bị cho quá trình tư vấn |Bác sĩ, điều dưỡng, nhân viên y tế Vinmec |Cần đo thời gian tổng hợp hồ sơ và số lần phải chuyển đổi giữa các hệ thống |
| 4 |Pain từ người khác |Khi cư dân gửi phản ánh về sự cố tại khu đô thị, tôi muốn biết phản ánh đã được tiếp nhận và xử lý đến đâu, để không phải liên hệ nhiều lần |Cư dân, nhân viên chăm sóc khách hàng, ban quản lý Vinhomes |Cần đo thời gian phản hồi, số lần cư dân phải hỏi lại và tỷ lệ phản ánh quá hạn |
| 5 |Lặp lại |Khi nhu cầu đặt xe tăng cao vào giờ cao điểm, tôi muốn dự báo khu vực có nhu cầu lớn và phân bổ xe phù hợp, để giảm thời gian chờ của khách hàng |Tài xế, nhân viên điều phối, khách hàng Xanh SM |Cần đo thời gian chờ trung bình, tỷ lệ yêu cầu không có xe nhận và mức chênh lệch cung cầu theo khu vực |
| 6 | | | | |
| 7 | | | | |
| 8 | | | | |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

-

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 |VinFast – Phân loại yêu cầu bảo hành |Quy trình rõ, có thể đo thời gian xử lý và tỷ lệ phân loại sai|Khâu phân loại có thực sự là bottleneck lớn nhất?|
| 2 |Vinhomes – Xử lý phản ánh cư dân |Nhiều bên tham gia, có thể đo thời gian phản hồi và tỷ lệ quá hạn |Phản ánh thường bị tắc ở tiếp nhận, phân công hay xử lý? |
| 3 |Xanh SM – Điều phối xe giờ cao điểm |Bài toán vận hành rõ, có metric định lượng và tiềm năng tối ưu bằng AI |Nguyên nhân chính là thiếu xe hay phân bổ xe chưa hợp lý? |

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story |Khi khách hàng gửi yêu cầu bảo hành xe, tôi muốn yêu cầu được phân loại và chuyển đến đúng bộ phận, để quá trình kiểm tra và xử lý bảo hành diễn ra nhanh chóng|
| Actor |Nhân viên tiếp nhận yêu cầu bảo hành / nhân viên chăm sóc khách hàng |
| Thời điểm / bối cảnh |Khi khách hàng gửi yêu cầu bảo hành qua ứng dụng, hotline hoặc trung tâm dịch vụ |
| Quy trình hiện tại (3–7 bước) |1. Tiếp nhận yêu cầu từ khách hàng · 2. Đọc mô tả và kiểm tra thông tin xe · 3. Xác định loại sự cố và phạm vi bảo hành · 4. Chuyển yêu cầu đến bộ phận phụ trách · 5. Bộ phận kỹ thuật tiếp nhận và xử lý |
| Bottleneck (bước nào, mất bao nhiêu phút) |Bước 3–4: Nhân viên phải đọc mô tả, xác định loại sự cố và tìm đúng bộ phận phụ trách. Thời gian: TBD |
| Impact (nếu không giải thì sao) |Có nguy cơ phân loại sai, chuyển nhầm bộ phận hoặc phải yêu cầu khách hàng bổ sung thông tin. Mức độ ảnh hưởng cần khảo sát |
| Success metric (baseline → target) |Giảm thời gian phân loại yêu cầu; giảm tỷ lệ chuyển sai bộ phận; không làm tăng tỷ lệ phân loại sai nghiêm trọng |
| Phương án không dùng AI |Xây dựng biểu mẫu tiếp nhận thống nhất, danh mục lỗi và bộ quy tắc phân loại theo loại sự cố |
| Giả thuyết về AI (nếu có) |AI đọc mô tả sự cố, nhận diện nhóm vấn đề và đề xuất bộ phận phụ trách. Nhân viên xác nhận trước khi chuyển yêu cầu |
| Cảm nhận nhanh |Workflow|

Quy trình nháp hiện tại:

```
HIỆN TẠI — Thời gian tổng: 30P

[1. Tiếp nhận yêu cầu]
          ↓
[2. Kiểm tra thông tin xe]
          ↓
[3. Đọc và phân loại sự cố] ← BOTTLENECK CẦN KIỂM CHỨNG
          ↓
[4. Chuyển đến bộ phận phụ trách]
          ↓
[5. Kỹ thuật tiếp nhận và xử lý]

```

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story |Khi cư dân gửi phản ánh về sự cố tại khu đô thị, tôi muốn phản ánh được ghi nhận, chuyển đến đúng bộ phận và cập nhật trạng thái xử lý, để vấn đề được giải quyết kịp thời mà không phải liên hệ nhiều lần|
| Actor |Nhân viên chăm sóc khách hàng / nhân viên ban quản lý khu đô thị |
| Thời điểm / bối cảnh |Khi cư dân gửi phản ánh về vệ sinh, thang máy, an ninh, kỹ thuật hoặc tiện ích |
| Quy trình hiện tại (3–7 bước) |1. Cư dân gửi phản ánh · 2. Nhân viên tiếp nhận và ghi nhận thông tin · 3. Phân loại sự cố và xác định bộ phận phụ trách · 4. Chuyển yêu cầu đến bộ phận liên quan · 5. Bộ phận phụ trách xử lý · 6. Cập nhật kết quả cho cư dân |
| Bottleneck (bước nào, mất bao nhiêu phút) |Bước 3–4: Xác định mức độ ưu tiên và chuyển phản ánh đến đúng bộ phận. Thời gian: TBD |
| Impact (nếu không giải thì sao) |Phản ánh có thể bị chuyển sai bộ phận, chậm xử lý hoặc cư dân phải liên hệ nhiều lần để hỏi trạng thái |
| Success metric (baseline → target) |Giảm thời gian từ lúc tiếp nhận đến khi phân công; giảm tỷ lệ phản ánh quá hạn và số lần cư dân phải hỏi lại |
| Phương án không dùng AI |Xây dựng biểu mẫu tiếp nhận thống nhất, quy tắc phân loại phản ánh và SLA cho từng loại sự cố |
| Giả thuyết về AI (nếu có) |AI phân tích nội dung phản ánh, xác định nhóm sự cố, mức độ ưu tiên và đề xuất bộ phận xử lý. Nhân viên kiểm tra trước khi phân công |
| Cảm nhận nhanh |Workflow|

Quy trình nháp hiện tại:

```
HIỆN TẠI — Thời gian tổng: 

[1. Cư dân gửi phản ánh]
          ↓
[2. Nhân viên tiếp nhận]
          ↓
[3. Phân loại và xác định ưu tiên] ← BOTTLENECK CẦN KIỂM CHỨNG
          ↓
[4. Chuyển đến bộ phận phụ trách]
          ↓
[5. Bộ phận xử lý sự cố]
          ↓
[6. Cập nhật kết quả cho cư dân]

```

### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story |Khi nhu cầu đặt xe tăng cao vào giờ cao điểm, tôi muốn biết khu vực nào có nhu cầu lớn và điều phối xe phù hợp, để giảm thời gian chờ của khách hàng và hạn chế tình trạng thiếu xe cục bộ|
| Actor |Nhân viên điều phối vận hành / tài xế Xanh SM |
| Thời điểm / bối cảnh |Giờ cao điểm buổi sáng, chiều tối hoặc khi có sự kiện khiến nhu cầu đặt xe tăng |
| Quy trình hiện tại (3–7 bước) |1. Khách hàng tạo yêu cầu đặt xe · 2. Hệ thống ghi nhận vị trí và nhu cầu · 3. Hệ thống tìm kiếm xe phù hợp · 4. Tài xế nhận hoặc từ chối chuyến · 5. Hệ thống tiếp tục tìm xe nếu chưa có tài xế nhận · 6. Tài xế đến đón khách |
| Bottleneck (bước nào, mất bao nhiêu phút) |Bước 3–5: Tìm kiếm và phân bổ xe phù hợp khi nhu cầu tập trung tại một khu vực. Thời gian: TBD |
| Impact (nếu không giải thì sao) |Khách hàng phải chờ lâu, yêu cầu đặt xe có thể không được đáp ứng; tài xế có thể phân bố không đồng đều giữa các khu vực |
| Success metric (baseline → target) |Giảm thời gian chờ trung bình; tăng tỷ lệ yêu cầu được tài xế nhận; giảm tỷ lệ yêu cầu bị hủy do không có xe |
| Phương án không dùng AI |Thiết lập quy tắc điều phối dựa trên khoảng cách, số lượng xe sẵn sàng và ngưỡng nhu cầu theo khu vực |
| Giả thuyết về AI (nếu có) |AI dự báo nhu cầu đặt xe theo khu vực và khung giờ, đề xuất vị trí phân bổ xe phù hợp cho bộ phận điều phối |
| Cảm nhận nhanh |Workflow / Agent|

Quy trình nháp hiện tại:

```
HIỆN TẠI — Thời gian tổng: TBD

[1. Khách hàng đặt xe]
          ↓
[2. Ghi nhận vị trí và nhu cầu]
          ↓
[3. Tìm xe phù hợp]
          ↓
[4. Tài xế nhận chuyến]
          ↓
[5. Tìm xe khác nếu chưa có tài xế nhận]
          ↓
[6. Tài xế đến đón khách]

BOTTLENECK CẦN KIỂM CHỨNG: Bước 3–5

```

### Card muốn pitch nhất

- Card số: 1 
- Vì sao:Đây là vấn đề có đầu vào và đầu ra khá rõ ràng: nhân viên tiếp nhận yêu cầu bảo hành, xác định loại sự cố rồi chuyển đến bộ phận phù hợp. Có thể đo thời gian phân loại, tỷ lệ chuyển sai bộ phận và số lần phải bổ sung thông tin. Ngoài ra, có thể thử giải pháp từ biểu mẫu và bộ quy tắc trước khi cân nhắc AI.
- Câu hỏi muốn nhóm phản biện:Liệu phân loại yêu cầu có thực sự là nút thắt lớn nhất trong quy trình bảo hành, hay thời gian chờ kiểm tra kỹ thuật và xác nhận điều kiện bảo hành mới là nguyên nhân chính gây chậm trễ?

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Chưa phân biệt rõ phân loại lỗi kỹ thuật và xác định lỗi có thuộc phạm vi bảo hành hay không.|Đồng ý|Tách hai hoạt động này thành các bước riêng trong quy trình để tránh nhầm lẫn|

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | | |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: | |
| Nhận phản biện | Câu hỏi tôi nhận được: | Tôi đã sửa gì: |
| Gom cluster / cây OST | | |
| Chọn candidate problem | | |
| Kiểm chứng / research | | |
| Quy trình nhóm | | |
| Problem Statement | | |
| Mức can thiệp AI | | |
| Quyết định | | |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | | | | |
| CP2 Problem Card | | | | |
| CP4 Research | | | | |
| CP5 Quy trình | | | | |
| CP5–6 Problem Statement | | | | |
| CP6 Mức can thiệp / quyết định | | | | |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

---

## 7. Tài liệu tham khảo

-
