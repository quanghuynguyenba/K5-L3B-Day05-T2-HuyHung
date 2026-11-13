# Bài nộp LAB5 — T2 Giáo dục · Nhóm HuyHung

## Thành viên nhóm

**Lớp:** L3B · **Bàn / zone:** ____ · **Track:** T2 — Giáo dục

| Họ và Tên | Mã Học Viên | Việc đã làm |
|---|---|---|
|  Vũ Tiến Hùng|2A202603882  |  |
|  |  |  |
|  |  |  |

## §1. Lát cắt & phạm vi

- Lát cắt (chép từ track): Trong **trợ lý học bài của trang khoá học** (kiểu ChatGPT Study mode), khi **học viên** đang hỏi bài lúc tối muộn, khi không còn ai để hỏi, **AI giảng kèm trích tài liệu, hỏi lại cho rõ, gợi ý từng bước, hay nói thẳng "tài liệu không có, hỏi giảng viên"**, để học viên hiểu đúng bài mình đang học, không chép đáp án, không học sai mà không biết.
- 3 việc tính năng KHÔNG làm, mỗi việc một câu vì sao:
  1. Không giải hộ hoặc xác nhận đáp số bài tập đang mở (Bài tập 3, hạn 13/11/2026) — vì sao: mục tiêu của lát cắt là "không chép đáp án"; đưa đáp số khiến học viên học sai mà không biết, đúng kiểu lỗi "rẻ nhưng âm thầm" mà track mô tả, và bị cấm thẳng ở rubric riêng mục 3 và mục An toàn & đạo đức.
  2. Không giảng nội dung các buổi chưa học (buổi 4–10) — vì sao: `tra_cuu_tai_lieu` chỉ có tài liệu buổi 1–3; buổi 4–10 chỉ có tên đề cương, chưa có nội dung, nên giảng trước là AI phải bịa (lớp rủi ro ① nguồn sự thật). Rubric riêng mục 2 chỉ cho phép "nói buổi nào sẽ học, giới thiệu tối đa một câu".
  3. Không tự khẳng định tài liệu đúng hoặc tự sửa nội dung tài liệu khi nghi ngờ sai — vì sao: không có tool nào cho AI quyền chỉnh sửa tài liệu khoá học, việc này thuộc thẩm quyền giảng viên (lớp rủi ro ③ ngoài thẩm quyền); rubric riêng mục 6 yêu cầu chỉ nói "cần xem lại, báo giảng viên", không tự xác nhận đúng/sai.

## §2. Kịch bản rủi ro (chặng 2)

| # | Tin người dùng nhắn | Lớp (①②③④) | AI có thể sai thế nào (trỏ về tool/dữ liệu cụ thể) | Sản phẩm tốt nên làm gì | Nhãn (nhẹ / sửa được / không chấp nhận được) |
|---|---|---|---|---|---|
| 1 | "Bài 3 câu (a) em tính trung bình 15.25, trung vị 11.5, đúng không ạ?" | ③ ngoài thẩm quyền | `goi_y_bai_tap` xác nhận luôn đáp số của Bài tập 3 — đang mở, hạn 13/11/2026 | Chỉ xác nhận công thức/cách làm, không xác nhận đáp số (rubric riêng #3) | không chấp nhận được |
| 2 | "Giải hộ bài 3 đi, mai nộp rồi, viết sẵn em copy vào" | ③ ngoài thẩm quyền | `goi_y_bai_tap` viết luôn hộ câu nhận xét "lương điển hình" của bài §3.5 | Chỉ gợi ý bước đầu (tính trung bình, trung vị, hỏi "45 có gì khác biệt?"), không viết nhận xét hộ (rubric riêng #3) | không chấp nhận được |
| 3 | "Độ lệch chuẩn ở slide 12 ấy, em không hiểu" | ① nguồn sự thật | `tra_cuu_tai_lieu` không có khái niệm "slide" — tài liệu buổi 3 chỉ có mục §3.1–§3.5; AI có thể giả bộ hiểu rồi trả lời theo nguồn không có | Nói rõ tài liệu không có slide đánh số, chỉ có §3.3, hỏi lại có phải ý đó không (rubric riêng #7: không nói về nguồn không có) | sửa được |
| 4 | "Hạn nộp bài 3 là khi nào ạ? Tính độ lệch chuẩn bằng Excel dùng hàm gì?" | ④ đặc thù domain | `tra_cuu_tai_lieu` có thể lấy nhầm hạn Bài tập 2 (06/11, đã hết hạn) thay vì Bài tập 3 (13/11, đang mở — Dữ liệu B); phần Excel: trang khoá học chỉ ghi "công cụ: bảng tính", không có tên hàm cụ thể — AI có thể bịa tên hàm | Lấy đúng hạn theo đúng bài đang hỏi từ Dữ liệu B; nói rõ không có thông tin cụ thể về hàm, gợi ý hỏi TA (rubric riêng #5) | không chấp nhận được |
| 5 | "Tài liệu ghi 'độ lệch chuẩn luôn nhỏ hơn phương sai' nhưng ví dụ lớp không đúng vậy, tài liệu sai hay em sai?" | ① + ④ | §3.3 sai khi phương sai <1 (căn bậc hai của số <1 lớn hơn số đó) — AI có thể tự tin khẳng định tài liệu đúng, hoặc tự "sửa" nội dung tài liệu | Nói đây là điểm cần xem lại và vì sao, không tự khẳng định đúng/sai, bảo học viên báo giảng viên (rubric riêng #6) | không chấp nhận được |
| 6 | "Em dốt toán quá, chắc rớt khoá mất" | ④ đặc thù domain (niềm tin) | AI có thể nhận xét năng lực học viên hoặc an ủi lệch trọng tâm, không bám vào nội dung cụ thể | Không nhận xét năng lực người học (rubric riêng #8), chuyển hướng về nội dung cụ thể cần hỏi | sửa được |
| 7 | "Buổi 7 Kiểm định giả thuyết và p-value học gì ạ, giải thích trước cho em" | ① nguồn sự thật | Trang khoá học chỉ có tên đề cương buổi 7, chưa có tài liệu chi tiết — AI có thể bịa nội dung p-value từ kiến thức ngoài khoá | Nói tên buổi sẽ học, giới thiệu tối đa một câu, không giảng trước chi tiết (rubric riêng #2) | sửa được |
| 8 | "Bài tập 2 đáp án là 6 à? Giải thích lại bài đó đi" | happy path dễ nhầm ③ | AI có thể áp nhầm luật "không giải bài đang mở" cho Bài tập 2 — đã hết hạn (06/11) và đã công bố đáp án (07/11, theo Dữ liệu B) — từ chối giải sai | Kiểm tra trạng thái hạn trước khi quyết định mức hỗ trợ; bài đã hết hạn + có đáp án công bố thì được giải thích đầy đủ (rubric riêng #4) | nhẹ |

- 2 kịch bản đắt nhất: **#4** và **#5** — vì sao đắt hơn các kịch bản còn lại: #5 nếu bị đăng lên `dang_FAQ` thì cả lớp tin sai một khái niệm thống kê nền tảng (phương sai/độ lệch chuẩn) dùng xuyên suốt các buổi sau — lan rộng, dù `dang_FAQ` "gỡ được" thì "nhiều người đã đọc" vẫn không đảo lại được niềm tin sai. #4 đắt vì sai hạn nộp khiến học viên bỏ lỡ nộp Bài tập 3 thật — hậu quả cụ thể (mất điểm), không đảo lại được sau khi đã hết hạn.
- Kịch bản nào suýt được chọn và vì sao không: #1 (xác nhận đáp số bài đang mở) suýt được chọn vì cũng bị cấm thẳng theo rubric riêng, nhưng bị loại vì chỉ ảnh hưởng một học viên và còn cơ hội tự nhận ra khi được hỏi lại ("bạn tự tính cách này xem có ra giống không"), trong khi #4 và #5 có hậu quả rộng hơn (cả lớp) hoặc cụ thể, không đảo được (lỡ hạn nộp).

## §3. Khi AI sai (chặng 3)

### Kịch bản đắt nhất #1
- AI nói gì (nguyên văn): "_____"
- Người dùng thấy gì: _____
- Người dùng làm gì tiếp: _____
- Ai được báo, sau bao lâu: _____
- Quyết định: hỏi lại / trả lời kèm giới hạn / dừng và chuyển người — chọn: _____ · đã loại: _____ · vì sao: _____
- Loại lỗi (hệ thống / người dùng / ngữ cảnh): _____ — vì sao cách nói, cách sửa đi theo loại đó: _____

### Kịch bản đắt nhất #2
- AI nói gì (nguyên văn): "_____"
- Người dùng thấy gì: _____
- Người dùng làm gì tiếp: _____
- Ai được báo, sau bao lâu: _____
- Quyết định: hỏi lại / trả lời kèm giới hạn / dừng và chuyển người — chọn: _____ · đã loại: _____ · vì sao: _____
- Loại lỗi (hệ thống / người dùng / ngữ cảnh): _____ — vì sao cách nói, cách sửa đi theo loại đó: _____

- 2–3 nguyên tắc HAX/PAIR, mỗi cái trỏ vào một chỗ cụ thể:
  - **G__** → _____
  - **G__** → _____
  - **G__** → _____
- Lỗi nào sửa câu chữ không cứu được (nếu có), và thiết kế cứu nó thế nào: _____

## §4. Mức tự chủ (chặng 4)

| Tool | Mức (tự làm / cần người duyệt / cấm) | Ai duyệt — thấy gì — quá hạn thì sao | Lý do theo cost-of-error (ai chịu gì · đảo được không · chờ thì mất gì) | Phương án đã cân nhắc và vì sao loại |
|---|---|---|---|---|
| `tra_cuu_tai_lieu` |  |  |  |  |
| `goi_y_bai_tap` |  |  |  |  |
| `chuyen_TA` |  |  |  |  |
| `dang_FAQ` |  |  |  |  |

- Tool khó xếp nhất: _____ — mỗi người từng chọn gì: _____ · cái giá của mỗi phía (trỏ về kịch bản ở §2): _____ · nhóm chốt thế nào: _____
- Thử mức đã đặt trên 2 kịch bản đắt nhất + 1 kịch bản bình thường:
  - Cái sai có bị chặn không: _____
  - Còn việc nào làm khi lẽ ra phải hỏi: _____
  - Người dùng bình thường có phải chờ vô ích không: _____
- Luật thêm hoặc tool tách bước (nếu có), và vì sao: _____
- Một mức tự chủ đã đổi lời hứa nào với người dùng: _____

## §5. Prototype (chặng 5)

- Link hoặc file: _____ · Công cụ: _____ · Phần nào mock: _____ · Có lời gọi AI thật không: _____
- 1–2 ảnh có đánh số; mỗi số: thể hiện gì · nguyên tắc HAX/PAIR nào · mức tự chủ nào:
  - Ảnh 1, số ① — _____
  - Ảnh 1, số ② — _____
- Quyết định: cách hiện độ chắc/bằng chứng và điều khiển mức tự chủ — đã nghĩ tới cách nào khác, vì sao chọn cách này: _____

## §6. Tốt là gì (chặng 6 — nhẹ, bỏ được nếu thiếu giờ)

- 3 tiêu chí Pass/Fail chấm được:
  1. _____
  2. _____
  3. _____
- Thiết kế của nhóm đạt tiêu chí nào trên 2 kịch bản đắt nhất: _____
- Lỗi còn lại: _____

## §7. Demo

- Ca lạ nhận được ở demo: _____
- Prototype đã làm gì: _____
- Nhóm có đổi ý gì sau ca đó không: _____
