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

### Kịch bản #4 (đắt nhất) — nhầm hạn nộp / bịa hàm không có nguồn
- AI nói gì (nguyên văn): "Theo trang khoá học, **Bài tập 3 hạn nộp 23:59 ngày 13/11/2026 và đang mở** (khác Bài tập 2 đã hết hạn 06/11, đã có đáp án). Về hàm tính độ lệch chuẩn trên bảng tính: tài liệu buổi 3 chỉ dạy công thức, không ghi rõ dùng hàm nào hay phần mềm nào — mình không có thông tin đó để nói chắc. Bạn nên hỏi TA (giờ 8:00–22:00) để chọn đúng hàm giảng viên muốn, vì chọn nhầm có thể ra số khác với đáp án mà bạn không biết vì sao."
- Người dùng thấy gì: khung trả lời tách hai phần rõ ràng — phần hạn nộp có nhãn "✓ từ trang khoá học" kèm trạng thái "Đang mở"; phần hàm Excel có nhãn "⚠ không có trong tài liệu" và nút **[Hỏi TA ngay]**.
- Người dùng làm gì tiếp: bấm **[Hỏi TA ngay]** (gọi `chuyen_TA`) nếu vẫn cần hàm cụ thể, hoặc tự tra cách tính theo công thức §3.3 đã học.
- Ai được báo, sau bao lâu: TA được báo ngay khi học viên bấm chuyển, hiển thị trong hàng chờ kèm giờ hỏi; nếu ngoài giờ TA (8:00–22:00), hệ thống báo "TA trả lời trong giờ làm việc, dự kiến sáng mai".
- Quyết định: **trả lời kèm giới hạn** cho cả hai phần (không hỏi lại vì câu hỏi đã rõ ràng, hỏi lại thêm chỉ làm mất thời gian của học viên tối muộn; không dừng toàn bộ chuyển người vì phần hạn nộp AI có đủ dữ liệu để trả lời chắc chắn ngay, chuyển hết sẽ bắt học viên chờ TA cho cả câu dễ) · đã loại: "hỏi lại cho rõ" (không cần vì câu hỏi đã cụ thể), "dừng và chuyển người toàn bộ" (lãng phí phần đã có dữ liệu chắc) · vì sao: cost-of-error hai phần khác nhau nên phải xử lý khác nhau trong cùng một câu trả lời.
- Loại lỗi: **hệ thống** — nếu AI trả lời tên hàm cụ thể, đó là lỗi thiết kế: hệ thống thiếu một bước kiểm tra "câu trả lời có trỏ được về một dòng dữ liệu đã cấp không" trước khi sinh câu trả lời, nên mới lẫn giữa phần có nguồn (hạn nộp) và phần không có nguồn (tên hàm) mà vẫn trả lời như nhau. Sửa đúng là sửa bước kiểm tra nguồn trong thiết kế, không phải sửa riêng câu chữ của một lần trả lời.

### Kịch bản #5 (đắt nhất) — tài liệu khoá học có câu sai (§3.3)
- AI nói gì (nguyên văn): "Mình không đủ thẩm quyền để khẳng định tài liệu đúng hay sai. Về mặt toán: câu 'độ lệch chuẩn luôn nhỏ hơn phương sai' chỉ đúng khi phương sai lớn hơn 1; nếu phương sai nhỏ hơn 1, căn bậc hai của nó lại lớn hơn chính nó. Mình đã gửi câu hỏi này cho giảng viên kiểm tra lại mục §3.3, bạn sẽ được báo khi có xác nhận chính thức."
- Người dùng thấy gì: nhãn trạng thái "⏳ Chưa xác nhận — đã chuyển giảng viên kiểm tra §3.3", chip trích dẫn "§3.3 Phương sai và độ lệch chuẩn", dòng ghi chú nhỏ "Vì sao mình không tự trả lời: đây là nội dung tài liệu khoá học, không thuộc thẩm quyền của trợ lý."
- Người dùng làm gì tiếp: tạm ghi chú "chưa chắc" cạnh mục §3.3 trong vở, tiếp tục học phần khác; nhận thông báo lại khi giảng viên xác nhận.
- Ai được báo, sau bao lâu: giảng viên được báo ngay (không phải TA — lỗi nội dung tài liệu thuộc thẩm quyền giảng viên, khác câu hỏi bài tập thường); **gap đã nhận ra:** track chỉ cấp tool `chuyen_TA`, không có tool chuyển thẳng giảng viên, nên thiết kế cần thêm luật "TA gắn cờ ưu tiên cao và escalate lên giảng viên, TA không tự trả lời thay" — ghi rõ ở §4 là luật thêm.
- Quyết định: **dừng và chuyển người** làm nhánh chính (không tự xác nhận đúng/sai tài liệu), kèm một phần **trả lời có giới hạn** về nguyên lý toán tổng quát để học viên không trống tay trong lúc chờ · đã loại: "hỏi lại cho rõ" (câu hỏi đã rất rõ, hỏi lại chỉ trì hoãn) và "chỉ trả lời kèm giới hạn mà không chuyển người" (không sửa được gốc: tài liệu sai vẫn còn cho các học viên sau) · vì sao: sai tài liệu ảnh hưởng cả lớp, chỉ giảng viên có thẩm quyền sửa nguồn.
- Loại lỗi: **ngữ cảnh** — AI làm đúng thiết kế (trích đúng tài liệu được cấp), nhưng tài liệu nguồn sai nên kết quả sai với thực tế toán học; đây không phải lỗi AI "nói bậy" mà là lỗi của dữ liệu đầu vào trong đúng tình huống này. Vì là lỗi ngữ cảnh, cách sửa không phải "nói khéo hơn" mà phải sửa ở tầng dữ liệu/thiết kế (xem mục cuối).

- 2–3 nguyên tắc HAX/PAIR, mỗi cái trỏ vào một chỗ cụ thể:
  - **G1 — làm rõ hệ thống làm được gì** → kịch bản #4: nhãn "✓ từ trang khoá học" / "⚠ không có trong tài liệu" tách rõ phần AI có nguồn và phần AI không có nguồn, thay vì trả lời đồng nhất.
  - **G10 — thu hẹp phạm vi khi nghi ngờ** → kịch bản #5: AI không tự chọn "tài liệu đúng" hay "tài liệu sai", mà chỉ nêu điều kiện toán học chung rồi dừng ở đó, chuyển quyết định cho giảng viên.
  - **PAIR — Errors + Graceful Failure (mỗi loại lỗi một đường lui)** → cả hai kịch bản có đường lui khác nhau theo đúng loại lỗi: #4 (lỗi hệ thống, thiếu nguồn) → nút [Hỏi TA ngay]; #5 (lỗi ngữ cảnh, nguồn gốc sai) → trạng thái "đã chuyển giảng viên", không phải cùng một nút.
- Lỗi nào sửa câu chữ không cứu được, và thiết kế cứu nó thế nào: kịch bản #5 — nếu chỉ sửa câu AI nói ("nói khéo hơn, thêm cảnh báo") thì tài liệu §3.3 vẫn sai cho mọi học viên khác đọc trực tiếp tài liệu hoặc hỏi lại AI lần sau. Thiết kế cứu: gắn một **cờ "đang chờ giảng viên xác nhận"** vào chính mục §3.3 trong dữ liệu (không chỉ trong một lượt chat), để mọi học viên hỏi tới mục này — không riêng người hỏi đầu tiên — đều thấy cảnh báo, và `dang_FAQ` tạm khoá đăng công khai về mục này cho tới khi giảng viên xác nhận.

## §4. Mức tự chủ (chặng 4)

| Tool | Mức (tự làm / cần người duyệt / cấm) | Ai duyệt — thấy gì — quá hạn thì sao | Lý do theo cost-of-error (ai chịu gì · đảo được không · chờ thì mất gì) | Phương án đã cân nhắc và vì sao loại |
|---|---|---|---|---|
| `tra_cuu_tai_lieu` | tự làm | không áp dụng (chỉ đọc) | Sai thì chỉ trả về sai đoạn hoặc không tìm thấy — rẻ, và luôn kèm mã mục để học viên tự đối chiếu ngay; bắt duyệt mỗi lần tra cứu sẽ phá mất giá trị "tối muộn, không ai hỏi" của sản phẩm trong khi tool không đổi gì cả | Đã cân nhắc "cần duyệt" — loại vì tool chỉ đọc, không có gì để đảo, duyệt chỉ làm chậm vô ích |
| `goi_y_bai_tap` (tách theo trạng thái bài) | **Bài đang mở:** tự làm nhưng giới hạn hành vi — chỉ gợi bước đầu, cấm đưa đáp số/nhận xét hộ. **Bài đã hết hạn + có đáp án công bố:** tự làm đầy đủ | không áp dụng (giới hạn nằm trong luật hành vi của tool, không qua người duyệt) | Bài đang mở mà gợi quá tay = học viên đã chép, không đảo được (đã "hiểu" sai mà không biết); bài đã hết hạn thì giải đầy đủ không còn hại ai, chờ duyệt mỗi lần sẽ vô ích | Đã cân nhắc "cần người duyệt" cho mọi lần gợi ý — loại vì tốn thời gian TA cho câu hỏi học thuật bình thường, trong khi giới hạn hành vi theo trạng thái bài đã chặn được rủi ro chính mà không cần người |
| `chuyen_TA` | tự làm | không áp dụng | Đây là đường lui an toàn mặc định: sai thì chỉ hơi tốn thời gian TA đọc một câu không cần thiết, không gây hại cho học viên; chờ người duyệt trước khi chuyển sẽ làm mất đúng lúc học viên cần (tối muộn) | Đã cân nhắc "cần duyệt trước khi chuyển" — loại vì bản chất hành động là "xin người khác xem", không có gì để duyệt trước |
| `dang_FAQ` | cần người duyệt | Giảng viên hoặc TA duyệt nội dung trước khi đăng công khai cho cả lớp; nếu quá hạn duyệt (ví dụ qua đêm không ai duyệt), câu hỏi vẫn ở trạng thái "chưa đăng", học viên khác hỏi lại thì AI vẫn trả lời riêng theo luật thông thường, không chờ FAQ | Sai thì "nhiều người đã đọc" (theo đúng mô tả đảo-lại-được-không của tool) — đây chính là cơ chế lan rộng ở kịch bản #5; một bước duyệt ngắn chặn được trước khi lan ra cả lớp | Đã cân nhắc "tự làm" (đăng ngay cho nhanh) — loại vì đúng là nguyên nhân của kịch bản #5; đã cân nhắc "cấm" — loại vì mất giá trị chia sẻ câu hỏi hay cho cả lớp đang cùng học buổi 3 |

- Tool khó xếp nhất: **`dang_FAQ`** — mức nào cũng có giá: cấm hoàn toàn thì mất giá trị chia sẻ (nhiều học viên khác tối đó cũng thắc mắc y như vậy); tự làm (đăng ngay) thì đúng là cơ chế khiến kịch bản #5 lan ra cả lớp; cần duyệt thì đúng nhưng chậm, trong khi giá trị FAQ nằm ở tốc độ (giúp được nhiều người ngay buổi tối đó). *Ghi chú trung thực:* nhóm hiện mới có 1/3 thành viên điền — phần "mỗi người từng chọn gì" cần được bổ sung khi đủ nhóm thảo luận thật; nhóm chốt theo cost-of-error: ưu tiên chặn rủi ro lan rộng (kịch bản #5) hơn tốc độ, nên chọn "cần duyệt".
- Thử mức đã đặt trên 2 kịch bản đắt nhất + 1 kịch bản bình thường (#8):
  - **#4:** Cái sai có bị chặn không — *chưa chắc chắn*: mức "tự làm" của `tra_cuu_tai_lieu` chỉ quyết định AI được tự tra cứu, không tự động buộc AI từ chối phần không có nguồn (hàm Excel) — mức tự chủ không đủ, phải kèm luật hành vi "không có nguồn thì phải nói rõ" như đã ghi ở §3, không chỉ dựa vào mức tự chủ của tool. Còn việc nào làm khi lẽ ra phải hỏi — có, nếu thiếu luật hành vi đó AI vẫn có thể tự trả lời hàm Excel. Người dùng bình thường chờ vô ích — không, tool ở mức tự làm nên trả lời ngay.
  - **#5:** Cái sai có bị chặn không — có, phần "tự xác nhận tài liệu đúng/sai" bị chặn vì không tool nào cấp quyền đó cho AI. Còn việc nào làm khi lẽ ra phải hỏi — có một khe hở: nếu TA tự trả lời thay vì escalate giảng viên (vì `chuyen_TA` không phân biệt mức ưu tiên), TA có thể tự tin xác nhận sai thay. Người dùng bình thường chờ vô ích — không, vì luật "dừng và chuyển người" chỉ áp cho câu hỏi nghi vấn lỗi tài liệu, không áp cho mọi câu hỏi.
  - **#8 (bình thường — hỏi lại bài đã hết hạn):** Cái sai có bị chặn không — có, vì mức được tách đúng theo trạng thái bài (đã hết hạn + có đáp án → tự làm đầy đủ). Còn việc nào làm khi lẽ ra phải hỏi — không. Người dùng bình thường chờ vô ích — không, trả lời ngay vì ở mức tự làm.
- Luật thêm hoặc tool tách bước: (1) tách `goi_y_bai_tap` thành hai hành vi theo trạng thái bài (đang mở / đã hết hạn) — nhờ đó kịch bản #2 và #8 được xử lý khác nhau đúng cost-of-error, dù cùng một tool gốc; (2) thêm luật cho `chuyen_TA`: khi câu hỏi được gắn nhãn "nghi vấn lỗi tài liệu" (như kịch bản #5), TA phải escalate giảng viên, không tự trả lời thay — vì đây là khe hở có thật của bộ tool hiện có (không có tool chuyển thẳng giảng viên).
- Một mức tự chủ đã đổi lời hứa nào với người dùng: trước khi tách `goi_y_bai_tap`, lời hứa ngầm (kiểu trợ lý AI thường thấy) là "AI sẽ giúp em làm bài"; sau khi tách theo trạng thái, lời hứa rõ ràng hơn và nhỏ hơn: "AI chỉ đồng hành gợi ý bước đầu khi bài đang mở, giải đầy đủ khi bài đã qua hạn" — người dùng biết trước giới hạn, không kỳ vọng được giải hộ.

## §5. Prototype (chặng 5)

- Link hoặc file: `prototype/index.html` (mở bằng trình duyệt, không cần server) · Công cụ: HTML/CSS/JS thuần, tự viết tay (không dùng Lovable/v0/Figma) · Phần nào mock: toàn bộ — dữ liệu dựng cứng trong trang, không đăng nhập, không backend · Có lời gọi AI thật không: **không** (không nhận bonus "lời gọi AI thật" — ưu tiên đúng giới hạn "dữ liệu giả" hơn gọi thật mà lộ rủi ro).
- 2 màn hình (chuyển bằng tab ở đầu trang):
  - **Màn hình 1 — học viên:** dựng đúng 2 lượt chat của kịch bản #5 và #4 (2 kịch bản đắt nhất ở §2), thể hiện: nhãn nguồn (✓ từ trang khoá học / ⚠ không có trong tài liệu / ⏳ chưa xác nhận), chip trích dẫn mã mục, trạng thái "đã chuyển giảng viên", nút hoàn tác-chuyển-người ("Hỏi TA ngay").
    - Số ① — kịch bản #5: nguyên tắc **G10 — thu hẹp phạm vi khi nghi ngờ**; mức tự chủ: "cấm" (tự xác nhận tài liệu) + "tự làm" (nhánh `chuyen_TA`).
    - Số ② — kịch bản #4: nguyên tắc **G1 — làm rõ hệ thống làm được gì** + **PAIR Errors/Graceful Failure**; mức tự chủ: "tự làm" của `tra_cuu_tai_lieu`, kèm nút chuyển TA cho phần không có nguồn.
  - **Màn hình 2 — giảng viên/TA (hàng chờ):** bảng hàng chờ hai dòng, phân biệt nhãn "nghi vấn lỗi tài liệu — escalate giảng viên" (chỉ giảng viên xác nhận được) với "câu hỏi thường — TA trả lời" — thể hiện đúng luật thêm ở §4 (TA không tự xác nhận thay lỗi tài liệu). Đây là màn hình bonus riêng của track T2.
- Quyết định: chọn hiện độ chắc bằng **nhãn màu + chip trích dẫn** ngay trong bong bóng chat (thấy ngay, không cần bấm thêm) — đã nghĩ tới cách khác là chỉ ghi trong câu chữ AI nói (ví dụ "mình không chắc...") nhưng loại vì câu chữ dễ bị đọc lướt qua lúc tối muộn, còn nhãn màu thấy được ngay cả khi không đọc hết đoạn văn; cũng đã nghĩ tới việc dùng % độ tin cậy (dạng số) nhưng loại vì học viên không biết % đó tính từ đâu, dễ hiểu lầm là "AI chắc 70% nên tin được", trong khi nhãn nguồn (có/không có tài liệu) trung thực hơn về bản chất giới hạn của AI.
- *Hạn chế còn lại (ghi trung thực):* chưa chụp ảnh PNG đánh số riêng để kèm vào `prototype/` như gợi ý cấu trúc repo — các số đánh số đang nằm ngay trong HTML (mở file là thấy luôn ① ②), nhóm nên tự chụp màn hình khi mở file bằng trình duyệt nếu cần ảnh tĩnh để nộp kèm.

## §6. Tốt là gì (chặng 6 — nhẹ, bỏ được nếu thiếu giờ)

- 3 tiêu chí Pass/Fail chấm được:
  1. Không có kịch bản nào bị AI xác nhận hoặc giải hộ đáp số cho bài tập đang mở.
  2. Mọi câu trả lời về nội dung tài liệu đều trỏ được về một mục §x.x cụ thể, hoặc nói rõ "không có trong tài liệu" — không có câu nào bỏ trống nguồn.
  3. Khi nghi ngờ tài liệu sai, AI không tự khẳng định đúng/sai mà luôn có đường chuyển giảng viên ngay trong lượt trả lời đó (không im lặng, không tự quyết).
- Thiết kế của nhóm đạt tiêu chí nào trên 2 kịch bản đắt nhất:
  - **#4:** tiêu chí 1 — Pass (không liên quan xác nhận đáp số). Tiêu chí 2 — **chưa chắc Pass**: thiết kế hiện tại chỉ chặn bằng "luật nói miệng" (yêu cầu AI tự nhận không có nguồn), chưa có cơ chế kỹ thuật thật kiểm tra groundedness trước khi trả lời — đây là lỗi còn lại, không phải đã giải quyết xong. Tiêu chí 3 — không áp dụng (không phải ca tài liệu sai).
  - **#5:** tiêu chí 1 — không áp dụng. Tiêu chí 2 — Pass (trích đúng §3.3, không bỏ trống nguồn). Tiêu chí 3 — Pass về mặt thiết kế (có đường chuyển giảng viên), nhưng còn khe hở: tool `chuyen_TA` không tự phân biệt mức ưu tiên, phải dựa vào nhãn gắn thủ công "nghi vấn lỗi tài liệu" mà bài chưa định nghĩa ai/cái gì gắn nhãn đó.
- Lỗi còn lại: (a) tiêu chí 2 ở #4 mới là luật thiết kế trên giấy, chưa có cơ chế kỹ thuật (groundedness check) thật; (b) cơ chế gắn nhãn "nghi vấn lỗi tài liệu" ở #5 chưa được định nghĩa rõ ai/khi nào gắn, cần một vòng thiết kế nữa nếu làm tiếp.

## §7. Demo

*(Mục này chỉ điền được sau khi demo thật diễn ra — không bịa ca lạ chưa xảy ra, vi phạm liêm chính học thuật của chương trình. Nhóm điền ngay sau buổi demo.)*

- Ca lạ nhận được ở demo: _____ *(điền sau demo)*
- Prototype đã làm gì: _____ *(điền sau demo)*
- Nhóm có đổi ý gì sau ca đó không: _____ *(điền sau demo)*
