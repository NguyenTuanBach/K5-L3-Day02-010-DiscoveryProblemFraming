# Báo cáo cá nhân — MSSV_HoTen

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Nguyễn Đức Trọng
- MSSV: 2A202603367
- Email trường (không bắt buộc, repo có thể để public): 26ai.trongnd3@vinuni.edu.vn
- Tên nhóm: 001
- Link repo nhóm: https://github.com/Hungztv/K5-L3A-Day02-001-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Lặp lại | Khi tôi hay quên các câu lệnh github, docker, sql, tôi muốn ghi nhớ các câu lệnh, để đỡ mất thời gian tra lại và upload tài liệu chia sẻ cho mọi người. | Kỹ sư / học viên dùng CLI hằng ngày | Tra Google/ChatGPT ~3–5 lần/ngày, mỗi lần ~3–5 phút; ước tính 15–25 phút/ngày mất cho việc tra lại câu lệnh đã biết |
| 2 | Cần đọc, tổng hợp nhiều thông tin | Khi tôi cần chọn linh kiện điện tử, tôi muốn tổng hợp thông số từ nhiều datasheet, để biết dùng linh kiện nào được và linh kiện nào sẽ gây hỏng mạch. | Kỹ sư điện tử thiết kế mạch | Mỗi lần chọn linh kiện phải đọc 3–5 datasheet (~20–30 trang/file), mất 1–2 giờ; sai linh kiện gây hỏng mạch, thiệt hại cả tiền lẫn thời gian làm lại |
| 3 | Lặp lại | Khi nộp bài assignment cuối tuần, tôi muốn biết mình đã đáp ứng đủ tiêu chí chấm điểm chưa, để không bị trừ điểm vì thiếu mục mà rubric yêu cầu. | Học viên khóa AI Thực chiến | Rubric thay đổi theo từng bài; mỗi lần tự đối chiếu thủ công mất ~15–20 phút; ước tính 1–2 lần/tuần bị trừ điểm vì thiếu mục nhỏ |
| 4 | Pain từ người khác | Khi thành viên mới vào nhóm thực chiến hỏi lại quy trình git flow, cách đặt tên branch, merge request, tôi muốn có nguồn tham chiếu chung đầy đủ, để không phải giải thích lại từ đầu mỗi lần. | Thành viên cũ (mất thời gian giải thích), thành viên mới (mất thời gian hỏi) | Xảy ra mỗi khi onboard người mới hoặc sau nghỉ dài; ước tính 2–3 câu hỏi lặp/tuần trên Slack nhóm, mỗi lần giải thích ~10–15 phút |
| 5 | | | | |
| 6 | | | | |
| 7 | | | | |
| 8 | | | | |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

- AI gợi ý thêm 8 problem theo 4 lăng kính (problem #5–#14 trong session làm việc). Giữ lại: #8 (kiểm tra rubric trước nộp bài) vì trùng với trải nghiệm thật. Bỏ: #7 (setup project mới), #9 (đọc paper dài), #10 (debug lỗi lặp lại), #13 (git flow onboarding) — sau khi phản biện với PM hoài nghi, #7 và #13 bị loại vì Rule/doc tĩnh đã đủ giải quyết; #9 và #10 chưa có số liệu thật để xác nhận.

---

## 3. Top 2 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 2

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Chọn linh kiện điện tử | Actor rõ (kỹ sư thiết kế mạch); bottleneck đọc nhiều datasheet là bài toán tổng hợp thật; hậu quả sai linh kiện đo được (hỏng mạch, thiệt hại tài chính); rule không giải quyết được so sánh đa thông số | Cần xác nhận tần suất thật (bao nhiêu lần/tháng chọn linh kiện mới?); input datasheet dạng PDF có parse được không? |
| 2 | Kiểm tra rubric bài nộp | Actor rõ (học viên cuối tuần); bottleneck đối chiếu bài với rubric động là thật; metric đo được (số lần bị trừ điểm); rubric thay đổi theo từng bài nên rule tĩnh không đủ | Rubric hiện có dạng file PDF/Google Doc không, hay chỉ nói miệng? |

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi tôi cần chọn linh kiện điện tử cho mạch thiết kế, tôi muốn tổng hợp và so sánh thông số kỹ thuật từ nhiều datasheet, để biết linh kiện nào dùng được và linh kiện nào sẽ gây hỏng mạch. |
| Actor | Kỹ sư / sinh viên điện tử đang thiết kế mạch (mình và nhóm thực chiến) |
| Thời điểm / bối cảnh | Khi bắt đầu thiết kế mạch mới hoặc thay thế linh kiện hết hàng; xảy ra ~2–4 lần/tháng |
| Quy trình hiện tại (3–7 bước) | 1. Xác định yêu cầu mạch (điện áp, dòng, tần số) → 2. Tìm kiếm linh kiện trên LCSC/Mouser/DigiKey → 3. Tải về 3–5 datasheet (PDF, 20–50 trang/file) → 4. Đọc thủ công từng datasheet, ghi chép thông số → 5. So sánh tay trên giấy hoặc spreadsheet → 6. Quyết định chọn linh kiện |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 4–5: Đọc và so sánh thủ công nhiều datasheet — mất 60–120 phút/lần; dễ bỏ sót thông số giới hạn tuyệt đối (absolute maximum ratings) dẫn đến chọn sai |
| Impact (nếu không giải thì sao) | Chọn sai linh kiện → hỏng mạch khi test → mất thêm 1–3 ngày làm lại + chi phí mua linh kiện thay thế |
| Success metric (baseline → target) | Thời gian so sánh và chọn linh kiện: từ 60–120 phút/lần → dưới 15 phút/lần |
| Phương án không dùng AI | Tạo spreadsheet template sẵn các thông số cần check; lưu lại các linh kiện đã dùng thành thư viện cá nhân |
| Giả thuyết về AI (nếu có) | AI đọc nhiều datasheet PDF cùng lúc, trích xuất và so sánh các thông số theo yêu cầu, cảnh báo nếu thông số vượt giới hạn tuyệt đối |
| Cảm nhận nhanh | Workflow / Agent |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — ~90–120 phút/lần chọn linh kiện

[Xác định yêu cầu mạch: 5'] 
  → [Tìm kiếm trên LCSC/Mouser: 10–15'] 
  → [Tải 3–5 datasheet PDF: 5'] 
  → [Đọc thủ công từng datasheet: 30–60'] ← BOTTLENECK
  → [Ghi chép thông số ra giấy/spreadsheet: 15–20'] ← BOTTLENECK
  → [So sánh và quyết định: 10–15'] 
  → [Đặt mua linh kiện: 5']
```

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story | Khi nộp bài assignment cuối tuần, tôi muốn biết bài mình đã đáp ứng đủ tiêu chí chấm điểm trong rubric chưa, để không bị trừ điểm vì thiếu mục mà rubric yêu cầu. |
| Actor | Học viên khóa AI Thực chiến Khóa 5 chuẩn bị nộp bài cuối tuần |
| Thời điểm / bối cảnh | Tối cuối tuần (Chủ nhật), ~1–2 giờ trước deadline nộp bài; rubric thay đổi theo từng assignment |
| Quy trình hiện tại (3–7 bước) | 1. Hoàn thành bài làm → 2. Mở rubric (PDF/Google Doc riêng) → 3. Đọc từng tiêu chí trong rubric → 4. Tự đối chiếu thủ công với bài đã làm → 5. Phát hiện thiếu (hoặc không phát hiện) → 6. Bổ sung (nếu còn thời gian) → 7. Nộp bài |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3–4: Đọc rubric và đối chiếu thủ công với bài — mất 15–20 phút; dễ bỏ sót tiêu chí nhỏ khi mệt cuối ngày |
| Impact (nếu không giải thì sao) | Bị trừ điểm vì thiếu mục nhỏ (format, section bắt buộc); ước tính 1–2 lần/tháng bị trừ điểm vì lý do này |
| Success metric (baseline → target) | Thời gian tự review trước nộp: từ 15–20 phút → dưới 5 phút; số lần bị trừ điểm vì thiếu mục: từ 1–2 lần/tháng → 0 lần/tháng |
| Phương án không dùng AI | Tạo checklist tĩnh từ rubric, tự tick trước khi nộp — nhưng rubric thay đổi theo từng bài nên checklist cũng phải cập nhật tay mỗi lần |
| Giả thuyết về AI (nếu có) | AI nhận bài nộp + rubric, tự đối chiếu và trả về danh sách tiêu chí đã đạt / chưa đạt kèm vị trí cụ thể trong bài |
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — ~15–20 phút tự review trước nộp

[Hoàn thành bài làm] 
  → [Mở rubric (file riêng): 2'] 
  → [Đọc từng tiêu chí rubric: 5–8'] 
  → [Tự đối chiếu thủ công với bài: 8–12'] ← BOTTLENECK
  → [Phát hiện thiếu mục (hoặc không): ???] 
  → [Bổ sung nếu còn thời gian] 
  → [Nộp bài]

Vấn đề: Bước đối chiếu làm thủ công khi đã mệt cuối ngày
→ dễ bỏ sót tiêu chí nhỏ → bị trừ điểm sau khi nộp
```

### Card muốn pitch nhất

- Card số:
- Vì sao:
- Câu hỏi muốn nhóm phản biện:

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| | | |

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
