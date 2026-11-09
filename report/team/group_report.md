# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm: 001
- Thành viên: xem `TEAM.md`
- Candidate problem được chọn (1 câu):
- Quyết định cuối: Go / Not Yet / No-Go

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

| # | Người đưa ra | Candidate (Job Story ngắn) | Actor | Bottleneck | Câu hỏi phản biện nhận được (ai hỏi) |
|---:|---|---|---|---|---|
| 1 | Dương Mạnh Hùng | Khi bắt đầu buổi lab và nhận tài liệu Git, tôi muốn hiểu mục tiêu và hướng dẫn ngay ở lần đọc đầu, để bắt đầu làm bài đúng hướng. | Sinh viên tham gia buổi lab | Đọc mục tiêu và phân chia công việc chưa rõ, phải đọc lại hướng dẫn; khoảng 30–60 phút/buổi. | Nguyễn Tuấn Bách hỏi: Vấn đề chỉ xảy ra trong 1–2 buổi lab đầu hay xuyên suốt các buổi? Nếu vòng đời ngắn, người dùng có sẵn sàng sử dụng công cụ riêng không? |
| 2 | Dương Mạnh Hùng | Khi phát hiện lỗi hoặc thấy sản phẩm có vấn đề, tôi muốn xác định và sửa nguyên nhân trong thời gian ngắn, để duy trì hiệu năng công việc và chất lượng sản phẩm. | Lập trình viên backend | Debug và xác định nguyên nhân sau khi xem log; tổng thời gian khoảng 30–90 phút/ngày. | Nguyễn Đức Trọng hỏi: Người dùng tự phát hiện lỗi rồi dùng AI hỗ trợ sửa, hay AI tự tìm và sửa toàn bộ từ đầu đến cuối? |
| 3 | Dương Mạnh Hùng | Khi bắt đầu làm bài và cần đọc file Markdown hoặc slide có cấu trúc nhiều phần, tôi muốn tìm và hiểu đúng thông tin, để không bỏ sót hoặc hiểu sai yêu cầu. | Sinh viên | Đọc hiểu và kiểm tra lại nội dung; 2–5 tài liệu/ngày, mỗi tài liệu 20–30 phút. | Nguyễn Đức Trọng hỏi: Nếu file Markdown đã có mục lục, bottleneck còn nằm ở việc tìm mục hay ở việc đọc hiểu yêu cầu và ngữ cảnh? |
| 4 | Nguyễn Tuấn Bách | Khi cần tài liệu trong nhóm Discord, tôi muốn tìm và xác định đúng tài liệu cần dùng, để phục vụ việc học tập và làm việc. | Học viên | Tìm và xác định đúng tài liệu trong Discord; khoảng 30 phút/lần. | Chưa pitch |
| 5 | Nguyễn Tuấn Bách | Khi bắt đầu tuần học, tôi muốn biết các thông báo và lịch học nào cần chú ý, để không bỏ lỡ hoạt động hoặc thời hạn quan trọng. | Bản thân — học viên | Chưa xác định; cần đo thời gian đọc/đối chiếu và kiểm tra có phải xem lại thông báo hay không. | Chưa pitch |
| 6 | Nguyễn Tuấn Bách | Khi chuẩn bị làm bài lab có hạn nộp trong ngày, tôi muốn hiểu rõ yêu cầu và các mục cần hoàn thành, để nộp bài đúng yêu cầu trước 23:59. | Bản thân — học viên | Chưa xác định; cần đo thời gian đọc/làm rõ yêu cầu và số lần phải hỏi lại hoặc phát hiện thiếu mục. | Chưa pitch |
| 7 | Lê Quang Vinh | Khi khách hàng gửi yêu cầu bảo hành xe, tôi muốn yêu cầu được phân loại và chuyển đến đúng bộ phận, để quá trình kiểm tra và xử lý bảo hành diễn ra nhanh chóng. | Nhân viên tiếp nhận yêu cầu bảo hành / chăm sóc khách hàng | Đọc mô tả, xác định loại sự cố và tìm đúng bộ phận phụ trách (bước 3–4); thời gian chưa xác định. | Chưa pitch |
| 8 | Lê Quang Vinh | Khi cư dân gửi phản ánh về sự cố tại khu đô thị, tôi muốn phản ánh được ghi nhận, chuyển đến đúng bộ phận và cập nhật trạng thái xử lý, để vấn đề được giải quyết kịp thời mà không phải liên hệ nhiều lần. | Nhân viên chăm sóc khách hàng / ban quản lý khu đô thị | Xác định mức độ ưu tiên và chuyển phản ánh đến đúng bộ phận (bước 3–4); thời gian chưa xác định. | Lê Đoàn Dương hỏi: Cư dân hiện gửi phản ánh qua những kênh nào? Ai là người chịu ảnh hưởng chính: cư dân hay nhân viên? |
| 9 | Lê Quang Vinh | Khi nhu cầu đặt xe tăng cao vào giờ cao điểm, tôi muốn biết khu vực có nhu cầu lớn và điều phối xe phù hợp, để giảm thời gian chờ và hạn chế thiếu xe cục bộ. | Nhân viên điều phối vận hành / tài xế Xanh SM | Tìm kiếm và phân bổ xe phù hợp khi nhu cầu tập trung tại một khu vực (bước 3–5); thời gian chưa xác định. | Lê Đoàn Dương hỏi: Làm thế nào để đo lường hiệu quả điều phối xe? |
| 10 | Nguyễn Đức Trọng | Khi tôi cần chọn linh kiện điện tử cho mạch thiết kế, tôi muốn tổng hợp và so sánh thông số kỹ thuật từ nhiều datasheet, để biết linh kiện nào dùng được và linh kiện nào sẽ gây hỏng mạch. | Kỹ sư / sinh viên điện tử đang thiết kế mạch (mình và nhóm thực chiến) | Đọc và so sánh thủ công nhiều datasheet ở bước 4–5; mất khoảng 60–120 phút/lần. | Chưa pitch |
| 11 | Nguyễn Đức Trọng | Khi nộp bài assignment cuối tuần, tôi muốn biết bài đã đáp ứng đủ tiêu chí trong rubric chưa, để không bị trừ điểm vì thiếu mục rubric. | Học viên khóa AI Thực chiến Khóa 5 | Đọc rubric và đối chiếu thủ công với bài; mất 15–20 phút/lần và dễ bỏ sót tiêu chí nhỏ. | Chưa pitch |
| 12 | Lê Đoàn Dương | Khi thực hiện một dự án nhóm, tôi muốn theo dõi tập trung nhiệm vụ, người phụ trách và deadline, để đảm bảo các thành viên phối hợp hiệu quả và hoàn thành công việc đúng hạn. | Nhóm trưởng và các thành viên trong nhóm sinh viên | Thông tin tiến độ phân tán, phải tìm kiếm và hỏi lại thành viên chưa cập nhật; khoảng 2–3 lần hỏi lại/tuần, thời gian cần đo thêm. | Dương Mạnh Hùng hỏi: Lần gần nhất phải hỏi lại nhiệm vụ hoặc deadline là khi nào, mất bao lâu và có ảnh hưởng đến tiến độ không? |
| 13 | Lê Đoàn Dương | Khi phải nghiên cứu một chủ đề để thực hiện đồ án hoặc bài thuyết trình, tôi muốn tìm kiếm, đánh giá và hệ thống hóa các tài liệu liên quan, để tiết kiệm thời gian và đảm bảo nội dung có cơ sở đáng tin cậy. | Sinh viên, thành viên nhóm thực hiện đồ án hoặc người nghiên cứu | Truy cập nhiều nguồn, đọc tài liệu dài và đánh giá thủ công; khoảng 5–8 tài liệu, mất 2–3 giờ/bài. | Dương Mạnh Hùng hỏi: Trong 2–3 giờ xử lý 5–8 tài liệu, bước nào là bottleneck chính: tìm kiếm, đánh giá nguồn, đọc hiểu hay tổng hợp? |
| 14 | Lê Đoàn Dương | Khi thực hiện nhiều thí nghiệm Machine Learning với các dataset, model và hyperparameter khác nhau, tôi muốn quản lý tập trung cấu hình, kết quả và checkpoint của từng lần chạy, để có thể so sánh, tái lập và lựa chọn model phù hợp nhất. | Sinh viên AI/Data Science, người nghiên cứu Machine Learning và ML Engineer | Kết quả, cấu hình và checkpoint nằm ở nhiều file/thư mục; phải tìm lại thủ công khi so sánh hoặc tái lập, thời gian chưa đo. | Dương Mạnh Hùng hỏi: Lần gần nhất không tìm lại được dataset, cấu hình hoặc checkpoint là khi nào; việc đó làm mất bao lâu hoặc ảnh hưởng kết quả ra sao? |

### 2.2. Cluster

| Cluster | Các candidate | Pattern chung | Candidate đại diện |
|---|---|---|---|
| 1. Tìm kiếm và hiểu thông tin học tập | #1, #3, #4, #5, #6 | Tài liệu và thông báo nằm ở nhiều nơi, người học mất thời gian tìm kiếm, đọc hiểu và xác định đúng yêu cầu. | #6 |
| 2. Nghiên cứu và so sánh tài liệu kỹ thuật | #10, #13 | Phải đọc nhiều nguồn hoặc datasheet, đánh giá độ phù hợp và tổng hợp thông tin thủ công. | #10 |
| 3. Phân loại và xử lý yêu cầu hoặc sự cố | #2, #7, #8 | Phải xác định nguyên nhân, mức độ hoặc bộ phận phụ trách trước khi xử lý, dễ mất thời gian ở bước phân loại. | #8 |
| 4. Điều phối công việc và nguồn lực | #9, #12 | Thông tin phân tán, khó phân bổ nguồn lực hoặc theo dõi người phụ trách, trạng thái và thời hạn. | #12 |
| 5. Kiểm tra và quản lý kết quả | #11, #14 | Khó đối chiếu kết quả với tiêu chí hoặc tìm lại cấu hình, dữ liệu và kết quả cũ để kiểm tra, so sánh và tái lập. | #11 |

### 2.3. Opportunity Solution Tree rút gọn

Gốc là **1 outcome**. Nhánh là **opportunity** (nhu cầu, pain), không phải tính năng hay công cụ.

```text
OUTCOME: Giảm ít nhất 30% thời gian và số lần làm lại khi tìm, hiểu và xử lý thông tin
├── Opportunity A: Người học mất nhiều thời gian tìm và xác định đúng tài liệu, thông báo hoặc yêu cầu cần thực hiện
├── Opportunity B: Người dùng phải đọc nhiều nguồn và tổng hợp thủ công để so sánh, đánh giá thông tin kỹ thuật
├── Opportunity C: Người tiếp nhận khó xác định nguyên nhân, mức độ ưu tiên hoặc bộ phận phù hợp để xử lý yêu cầu
├── Opportunity D: Nhóm khó theo dõi người phụ trách, trạng thái và deadline vì thông tin tiến độ bị phân tán
└── Opportunity E: Người dùng khó đối chiếu kết quả với tiêu chí hoặc tìm lại dữ liệu, cấu hình và kết quả cũ
```

Những ý đã gạch bỏ vì là solution đội lốt opportunity:

- Tạo chatbot hoặc trợ lý AI để hỏi đáp tài liệu.
- Tự động phân loại yêu cầu và chuyển đến đúng bộ phận.
- Tạo dashboard quản lý task, deadline và trạng thái.
- Tạo công cụ quản lý tập trung dataset, model và checkpoint.

### 2.4. Chấm điểm shortlist (1–5)

| Candidate | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được No AI/Rule/Workflow/Agent | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| #6 — Hiểu yêu cầu lab | 5 | 4 | 2 | 4 | 5 | 5 | 5 | 30 |
| #11 — Kiểm tra bài theo rubric | 5 | 5 | 4 | 5 | 5 | 5 | 5 | 34 |
| #12 — Theo dõi task và deadline | 5 | 4 | 4 | 4 | 4 | 5 | 5 | 31 |

**Candidate được chọn:** #11 — Kiểm tra bài assignment theo rubric

**Vì sao chọn:** Có actor, quy trình và bottleneck rõ; pain có thể đo bằng thời gian đối chiếu và số tiêu chí bị bỏ sót. Phạm vi vừa sức để kiểm chứng và xây dựng prototype trong lab.

**Vì sao loại các candidate còn lại:**

- #6: Pain còn chưa đủ bằng chứng và chưa xác định rõ thời gian xử lý.
- #12: Vấn đề thực tế nhưng cần thu thập dữ liệu từ nhiều thành viên, khó kiểm chứng nhanh.

**Xử lý bất đồng (nếu có):**

---

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map

| # | Giả định | Loại (Value / Usability / Feasibility / Viability) | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
|---:|---|---|---:|---:|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |
| 6 | | | | | |

*Điền 4–6 giả định; xóa dòng thừa.*

Giả định nhóm kiểm chứng trong buổi này:

### 3.2. Kiểm chứng

Cách đã dùng: Phỏng vấn / Survey / Log, ticket, review

Interview snapshot (mỗi buổi phỏng vấn một bảng, hoặc đặt file trong `report/assets/cp4-interview-snapshot-N.md`):

| Trường | Nội dung |
|---|---|
| Người được hỏi (vai trò, không ghi tên thật) | |
| Câu nói đáng nhớ nhất (nguyên văn) | |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | |
| Hiện đang xử lý bằng cách nào (workaround)? | |
| Mất bao lâu, bao lần? | |
| Insight / opportunity rút ra | |

Tổng hợp:

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---:|---|---|
| | | | |

**Nhóm đã sửa problem thế nào sau kiểm chứng:**

### 3.3. Research giải pháp đã có

| Công cụ / case / pattern | Link | Giải bước nào trong quy trình? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| **CoGrader – AI-powered Rubric Grading** | https://cograder.com/ | Hỗ trợ đọc bài assignment, đối chiếu nội dung với từng tiêu chí trong rubric, đề xuất điểm số và tạo feedback cho sinh viên. | Tự động đánh giá từng tiêu chí; hỗ trợ rubric tùy chỉnh; tạo feedback cụ thể; xử lý nhiều bài cùng lúc; giảng viên có thể chỉnh sửa kết quả trước khi trả bài. | Tập trung chủ yếu vào bài viết; kết quả AI vẫn cần giảng viên kiểm duyệt; có rủi ro đánh giá sai khi tiêu chí rubric phức tạp hoặc mang tính định tính. | Có thể ứng dụng AI để giảm thời gian đọc và đối chiếu bài làm. Cần hiển thị điểm số kèm giải thích theo từng tiêu chí và cho phép người dùng chỉnh sửa kết quả. |
| **Gradescope – AI-assisted Grading & Answer Groups** | https://www.gradescope.com/ | Hỗ trợ phân loại các câu trả lời tương tự, nhóm bài làm và áp dụng rubric để chấm điểm hàng loạt thay vì đánh giá từng câu trả lời riêng lẻ. | Giảm thao tác chấm lặp lại; hỗ trợ rubric linh hoạt; có thể thay đổi rubric và áp dụng cập nhật cho các bài liên quan; hỗ trợ thống kê kết quả theo câu hỏi. | AI grouping chỉ hỗ trợ một số dạng câu hỏi nhất định; giảng viên vẫn phải xem xét các nhóm câu trả lời và quyết định điểm; không tự động đánh giá toàn bộ assignment theo ngữ nghĩa. | Có thể tối ưu quy trình bằng cách tự động phân loại và nhóm các bài có nội dung tương tự. Cần có bước xác nhận của con người trước khi áp dụng kết quả hàng loạt. |
| **Turnitin Feedback Studio – Rubric & Feedback Management** | https://www.turnitin.com/products/feedback-studio/ | Hỗ trợ giảng viên đánh giá bài viết theo rubric, ghi nhận điểm số và phản hồi theo từng tiêu chí; đồng thời kiểm tra mức độ tương đồng nội dung. | Có rubric và grading forms; hỗ trợ nhận xét trực tiếp trên bài; tái sử dụng nhận xét thông qua QuickMarks; giúp sinh viên hiểu rõ điểm mạnh và điểm cần cải thiện. | Tập trung vào đánh giá bài viết và phản hồi học thuật; không phải giải pháp tự động chấm toàn bộ assignment theo rubric; giảng viên vẫn cần thực hiện việc đánh giá và nhập điểm. | Cần kết hợp điểm số với nhận xét cụ thể theo từng tiêu chí. Ngoài kết quả tổng thể, hệ thống nên giúp người học hiểu tại sao bài làm đạt hoặc chưa đạt yêu cầu. |

---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

Sơ đồ (ASCII, Mermaid hoặc link ảnh trong `report/assets/`):

```text

```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú |
|---:|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |

**Bottleneck chính:**

### 4.2. Quy trình tương lai

Ghi rõ bước nào **Rule**, bước nào **AI**, bước nào **con người**, **boundary** ở đâu, **phương án quay về** khi AI sai.

```text

```

### 4.3. Before / after

| Chỉ số | Trước | Sau (kỳ vọng) | Ghi chú |
|---|---:|---:|---|
| Số bước | | | |
| Tổng thời gian | | | |
| Số bước thủ công | | | |
| Bottleneck chính | | | |
| Rủi ro mới phát sinh | | | |

---

## 5. Problem Statement v0 (CP5)

| Trường | Nội dung |
|---|---|
| **Actor** | |
| **Quy trình** | |
| **Bottleneck** | |
| **Impact** | |
| **Success Metric** (baseline → target, cách đo) | |
| **Boundary** (AI không được làm gì; khi nào cần con người kiểm tra — HITL) | |

Phản biện nhận được (từ AI hoặc nhóm khác) và nhóm có đồng ý không:

-

---

## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

Bài của nhóm nằm ở ô:

Vì sao:

### 6.2. So sánh 4 mức

| Mức | Phương án cho bài của nhóm | Đủ khi nào | Rủi ro | Chọn? |
|---|---|---|---|---|
| **No AI** (sửa quy trình) | | | | |
| **Rule** | | | | |
| **Workflow** | | | | |
| **Agent** | | | | |

**Mức chọn:**

**Vì sao không chọn mức đơn giản hơn:**

### 6.3. AI Canvas rút gọn

| Thành phần | Nội dung |
|---|---|
| **Prediction** — AI dự đoán / tạo ra gì? | |
| **Judgment** — con người cân nhắc, quyết định gì? | |
| **Action** — hành động cuối cùng là gì, ai làm? | |
| **Outcome** — đo kết quả bằng gì? | |
| **Input** — AI cần dữ liệu đầu vào gì mỗi lần chạy? Có sẵn không? | |
| **Feedback** — lấy phản hồi ở đâu để cải thiện? | |

### 6.4. Hai câu hỏi của Google PAIR

- Người dùng muốn **được hỗ trợ (augment)** hay **giao hẳn việc (automate)**? Bằng chứng:
- AI sai kiểu nào tệ hơn, **báo nhầm** hay **bỏ sót**? Vì sao, và thiết kế đã xử lý thế nào:

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường | Nội dung |
|---|---|
| **Actor** | |
| **Quy trình** | |
| **Bottleneck** | |
| **Impact** | |
| **Success Metric** (baseline → target, cách đo) | |
| **Boundary** | |
| **AI intervention point** | |
| **Mức chọn** | No AI / Rule / Workflow / Agent |
| **Rủi ro & người kiểm tra** | |

**Thay đổi so với v0 và lý do:**

| Trường | v0 | v1 | Vì sao đổi |
|---|---|---|---|
| | | | |

**Tiêu chí đánh giá đầu ra của AI (3–5 tiêu chí):**

| # | Tiêu chí | Đạt khi | Không đạt khi |
|---:|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |

---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro

| Rủi ro | Câu hỏi | Mức độ rủi ro (Thấp = an toàn / TB / Cao = nguy hiểm) | Lý do / bằng chứng |
|---|---|---|---|
| **Value** | Người dùng có thật sự cần và sẽ dùng không? | | |
| **Usability** | Người dùng có dùng được, có hiểu và sửa được đầu ra của AI không? | | |
| **Feasibility** | Có đủ dữ liệu, công cụ, kỹ năng để làm không? | | |
| **Viability** | Có hợp chi phí, pháp lý, quy định tổ chức không? Ai vận hành? | | |

### 8.2. Kết luận

**Quyết định:** Go / Not Yet / No-Go

**Lý do:**

**Nếu Go — pilot nhỏ nhất:**

**Nếu Not Yet — cần kiểm chứng gì trước:**

**Nếu No-Go — nên làm gì thay AI:**

**Ngưỡng dừng** (nếu sau … mà … thì quay về …):

---

## 9. Hạn chế và hướng tiếp theo

-

## 10. Tài liệu tham khảo

-
