# Báo cáo cá nhân — 2A202603431_DuongManhHung

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Dương Mạnh Hùng
- MSSV: 2A202603431
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: 001
- Link repo nhóm: https://github.com/Hungztv/K5-L3A-Day02-001-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Tốn thời gian / cần đọc, tổng hợp nhiều thông tin | Khi bắt đầu buổi lab và nhận tài liệu Git, tôi muốn hiểu mục tiêu và hướng dẫn ngay ở lần đọc đầu, để bắt đầu làm bài đúng hướng. | Sinh viên tham gia buổi lab | Mất khoảng 30–60 phút mỗi buổi; xảy ra khoảng 5 buổi/tuần, tương đương khoảng 150–300 phút/tuần. |
| 2 | Cần đọc, tổng hợp nhiều thông tin | Khi bắt đầu làm bài và cần đọc file Markdown hoặc slide có cấu trúc nhiều phần, tôi muốn tìm đúng thông tin và ngữ cảnh liên quan, để không bỏ sót hoặc hiểu sai yêu cầu. | Sinh viên | Xử lý 2–5 tài liệu/ngày, mỗi tài liệu mất khoảng 20–30 phút; khi gặp lỗi thường phải kiểm tra lại 1–2 lần. |
| 3 | Lặp lại / tốn thời gian | Khi phát hiện lỗi hoặc thấy sản phẩm có vấn đề, tôi muốn xác định và sửa nguyên nhân trong thời gian ngắn, để duy trì hiệu năng công việc và chất lượng sản phẩm. | Lập trình viên backend | Tổng thời gian tự kiểm tra và debug khoảng 30–90 phút/ngày trong các ngày làm việc; thời gian từng lần lỗi chưa được tách riêng ở bước scan. |
| 4 | Cần đọc, tổng hợp nhiều thông tin | Khi muốn chia sẻ một chủ đề kỹ thuật, tôi muốn cô đọng kiến thức thành nội dung ngắn gọn, dễ hiểu, để người khác có thể tiếp nhận và áp dụng. | Người làm nội dung kỹ thuật / cộng đồng công nghệ | Đã thực hiện 4 bài; mỗi bài mất khoảng 30–60 phút để đọc, cô đọng và biên tập. |
| 5 | Tốn thời gian / lặp lại | Khi thiết kế cơ sở dữ liệu và API cho hệ thống nhiều cửa hàng, tôi muốn giữ mô hình dữ liệu và các endpoint nhất quán, để hệ thống mở rộng mà không phát sinh xung đột hoặc suy giảm hiệu năng. | Lập trình viên backend / nhóm phát triển | Công việc xuất hiện khoảng 4 lần/tuần; mỗi lần mất từ 30 phút đến một buổi; đã gặp vấn đề xung đột dữ liệu và truy vấn cần tối ưu. |


**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

- Tôi đã dùng AI để phản biện và chuẩn hóa cách diễn đạt các ý tưởng ban đầu thành Job Story. Tôi giữ lại các vấn đề có trải nghiệm và số liệu cụ thể; tôi bỏ cách viết solution-first như “dùng RAG”, “AI làm Code Reviewer” hoặc “xây Chatbot”, vì đó là giải pháp chứ chưa phải problem. Tôi tự kiểm tra và bổ sung lại thời gian, tần suất, số tài liệu và số bài thực tế dựa trên trải nghiệm của mình.

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Khó hiểu tài liệu Git trước mỗi buổi lab | Xảy ra khoảng 5 buổi/tuần, mất 30–60 phút mỗi buổi; actor và bottleneck dễ xác định. | Chưa biết nguyên nhân chính là mục tiêu, phân chia công việc hay hướng dẫn chưa rõ. |
| 2 | Mất nhiều thời gian xác định và sửa lỗi backend | Xảy ra hầu hết các ngày làm việc, tổng thời gian debug 30–90 phút/ngày; impact rõ và có thể đo theo từng lần lỗi ở bước tiếp theo. | Chưa biết lỗi logic, bảo mật hay truy vấn là nhóm lỗi chiếm nhiều thời gian nhất. |
| 3 | Khó tìm và hiểu thông tin trong file Markdown hoặc slide có cấu trúc nhiều phần | Xử lý 2–5 tài liệu/ngày, mỗi tài liệu mất 20–30 phút và có lúc phải kiểm tra lại 1–2 lần. | Chưa biết lỗi thường đến từ cấu trúc tài liệu, cách đọc hay thiếu bước kiểm chứng. |

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi bắt đầu buổi lab và nhận tài liệu Git, tôi muốn hiểu mục tiêu và hướng dẫn ngay ở lần đọc đầu, để bắt đầu làm bài đúng hướng. |
| Actor | Sinh viên tham gia buổi lab |
| Thời điểm / bối cảnh | Bắt đầu buổi lab, khi nhận tài liệu Git và hướng dẫn bài tập |
| Quy trình hiện tại (3–7 bước) | Mở tài liệu (5 phút) → đọc mục tiêu (5 phút) → đọc hướng dẫn (15–20 phút) → đọc lại phần chưa hiểu (10 phút) |
| Bottleneck (bước nào, mất bao nhiêu phút) | Đọc mục tiêu và phần phân chia công việc chưa rõ, khiến phải đọc lại hướng dẫn; tổng thời gian là khoảng 30–60 phút. |
| Impact (nếu không giải thì sao) | Có thể làm sai yêu cầu, mất nhiều thời gian hơn các bạn khác và phải hỏi lại. |
| Success metric (baseline → target) | Thời gian hiểu tài liệu từ 30–60 phút xuống dưới 30 phút/buổi; đo bằng thời gian từ lúc mở tài liệu đến khi bắt đầu làm đúng task đầu tiên. |
| Phương án không dùng AI | Dùng checklist, ghi chú cá nhân và tìm ví dụ minh họa trước khi bắt đầu làm bài. |
| Giả thuyết về AI (nếu có) | Có thể hỗ trợ làm rõ mục tiêu, phân chia công việc và chỉ ra phần cần đọc trước; sinh viên vẫn tự kiểm tra lại với tài liệu gốc. |
| Cảm nhận nhanh | Chưa biết |

Quy trình nháp hiện tại:

```text
[Mở tài liệu: 5'] → [Đọc mục tiêu: 5']
→ [Đọc hướng dẫn: 15–20'] → [Đọc lại phần chưa hiểu: 10'] ← BOTTLENECK
→ [Bắt đầu làm bài]
```

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story | Khi phát hiện lỗi hoặc thấy sản phẩm có vấn đề, tôi muốn xác định và sửa nguyên nhân trong thời gian ngắn, để duy trì hiệu năng công việc và chất lượng sản phẩm. |
| Actor | Lập trình viên backend |
| Thời điểm / bối cảnh | Khi phát hiện lỗi trong quá trình phát triển hoặc khi sản phẩm có hành vi không đúng |
| Quy trình hiện tại (3–7 bước) | Khoanh vùng phần kiến trúc bị ảnh hưởng (5–10 phút) → trích xuất log (10 phút) → phân tích và sửa mã nguồn (10–20 phút hoặc lâu hơn) → kiểm tra, thử nghiệm lại toàn bộ luồng (20–30 phút) |
| Bottleneck (bước nào, mất bao nhiêu phút) | Debug và xác định nguyên nhân sau khi xem log; bước sửa lỗi có thể kéo dài hơn 20 phút khi nguyên nhân chưa rõ. |
| Impact (nếu không giải thì sao) | Tạo vòng lặp debug, làm giảm hiệu năng công việc và kéo dài thời gian hoàn thiện sản phẩm. |
| Success metric (baseline → target) | Baseline hiện có: tổng thời gian debug khoảng 30–90 phút/ngày; ở bước kiểm chứng sẽ đo riêng từng lần lỗi và mục tiêu là dưới 45 phút/lần lỗi. |
| Phương án không dùng AI | Thiết lập test tự động và logging đầy đủ để phát hiện, tái hiện và khoanh vùng lỗi nhanh hơn. |
| Giả thuyết về AI (nếu có) | Có thể dùng AI để hỗ trợ phân tích log và gợi ý nguyên nhân, nhưng lập trình viên phải kiểm tra mã nguồn và chạy test trước khi chấp nhận sửa đổi. |
| Cảm nhận nhanh | Chưa biết |

Quy trình nháp hiện tại:

```text
[Khoanh vùng kiến trúc: 5–10'] → [Trích xuất log: 10']
→ [Phân tích và sửa mã: 10–20'+] → [Kiểm tra toàn bộ luồng: 20–30'] ← BOTTLENECK
```

### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | Khi bắt đầu làm bài và cần đọc file Markdown hoặc slide có cấu trúc nhiều phần, tôi muốn tìm và hiểu đúng thông tin cần thiết, để hoàn thành bài mà không bỏ sót hoặc hiểu sai yêu cầu. |
| Actor | Sinh viên |
| Thời điểm / bối cảnh | Khi bắt đầu làm bài từ tài liệu Markdown hoặc slide có cấu trúc nhiều phần |
| Quy trình hiện tại (3–7 bước) | Mở tài liệu (5 phút) → đọc nội dung (10–20 phút) → ghi chú và kiểm tra lại thông tin (15 phút) |
| Bottleneck (bước nào, mất bao nhiêu phút) | Đọc hiểu nội dung, đặc biệt khi tài liệu có nhiều phần cần đối chiếu; bước này chiếm khoảng 10–20 phút và có thể phải kiểm tra lại. |
| Impact (nếu không giải thì sao) | Hiểu sai hoặc bỏ sót thông tin, dẫn đến làm sai tài liệu, mất thêm thời gian và giảm lượng kiến thức tiếp thu được. |
| Success metric (baseline → target) | Thời gian xử lý hiện tại khoảng 20–30 phút/tài liệu; mục tiêu giảm còn 15–20 phút/tài liệu và giảm lỗi nhầm hoặc bỏ sót thông tin. |
| Phương án không dùng AI | Kiểm tra chéo các thông tin quan trọng giữa tài liệu và ghi chú trước khi bắt đầu làm bài. |
| Giả thuyết về AI (nếu có) | Có thể hỗ trợ tìm và đối chiếu thông tin trong tài liệu, nhưng sinh viên vẫn phải kiểm tra lại nội dung gốc trước khi sử dụng. |
| Cảm nhận nhanh | Chưa biết |

Quy trình nháp hiện tại:

```text
[Mở tài liệu: 5'] → [Đọc nội dung: 10–20']
→ [Ghi chú và kiểm tra lại: 15'] ← BOTTLENECK
```

### Card muốn pitch nhất

- Card số: 1
- Vì sao: Đây là vấn đề xảy ra khoảng 5 buổi/tuần, mất 30–60 phút mỗi buổi, có quy trình và bottleneck rõ, đồng thời dễ kiểm chứng với các sinh viên khác.
- Câu hỏi muốn nhóm phản biện: Nguyên nhân chính khiến sinh viên phải đọc lại tài liệu là mục tiêu chưa rõ, cách phân chia công việc hay thiếu ví dụ minh họa?

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Một số ý tưởng ban đầu viết theo hướng solution-first như RAG, AI Code Reviewer hoặc Chatbot thay vì mô tả problem. | Có | Viết lại thành Job Story tập trung vào bối cảnh, nhu cầu và kết quả mong muốn; đưa giải pháp vào phần giả thuyết riêng. |
| Metric ban đầu còn chung chung, ví dụ “tối ưu nhanh nhất có thể”. | Có | Đổi thành metric đo được: debug có tổng thời gian 30–90 phút/ngày ở bước scan và mục tiêu chi tiết dưới 45 phút/lần lỗi ở CP2. |
| Bottleneck cần là một bước cụ thể trong quy trình, không chỉ là “quy trình chậm”. | Có | Bổ sung bước nghẽn và thời lượng: đọc lại phần chưa hiểu, debug/xác định nguyên nhân, và đọc hiểu/kiểm tra lại tài liệu. |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Trình bày Problem Card #1 về việc khó hiểu tài liệu Git trước buổi lab, với quy trình 30–60 phút và bottleneck ở việc đọc mục tiêu, phân chia công việc và đọc lại phần chưa hiểu. | Đưa một problem học tập cụ thể vào danh sách candidate để nhóm có thể so sánh với các problem về tài liệu, debug và quản lý công việc. |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt cho Lê Đoàn Dương: (1) Với quản lý công việc nhóm, lần gần nhất bạn phải hỏi lại nhiệm vụ hoặc deadline là khi nào, mất bao lâu và có gây trễ việc không? (2) Trong 2–3 giờ xử lý 5–8 tài liệu, bước nào là bottleneck chính: tìm kiếm, đánh giá nguồn, đọc hiểu hay tổng hợp? (3) Với quản lý thí nghiệm Machine Learning, lần gần nhất bạn không tìm lại được dataset, cấu hình hoặc checkpoint là khi nào; việc đó làm mất bao lâu hoặc ảnh hưởng kết quả ra sao? | Làm rõ bằng chứng hành vi, bước nghẽn và mức độ ảnh hưởng của ba candidate trước khi nhóm chấm điểm và chọn problem chung. |
| Nhận phản biện | Câu hỏi tôi nhận được: Nguyễn Đức Trọng hỏi liệu problem debug backend là để người dùng tự phát hiện rồi AI hỗ trợ sửa, hay AI tự phát hiện và sửa toàn bộ; nếu file Markdown đã có mục lục thì bottleneck của problem đọc tài liệu còn là gì; Nguyễn Tuấn Bách hỏi vấn đề này chỉ xảy ra trong 1–2 buổi lab đầu hay xuyên suốt các buổi, và người dùng có sử dụng công cụ riêng nếu vòng đời vấn đề ngắn không. | Tôi xác định phạm vi debug là người dùng/lập trình viên phát hiện lỗi trước, sau đó AI chỉ hỗ trợ phân tích và gợi ý sửa; con người phải kiểm tra và chạy test. Với file Markdown, problem không phải thiếu mục lục mà là đọc hiểu mục tiêu, phân chia công việc, chọn phần liên quan và đối chiếu ngữ cảnh. Một số người có thể chỉ gặp vấn đề trong 1–2 buổi lab đầu, nhưng công cụ hỗ trợ đọc hiểu vẫn có thể giúp đọc tài liệu nhanh hơn và giúp nhiều người tiếp thu dễ hơn; nhóm cần kiểm chứng thêm tần suất và nhu cầu sử dụng công cụ riêng. |
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
