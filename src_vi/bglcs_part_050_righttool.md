# Công Cụ Phù Hợp Cho Công Việc

[i[Right tool for the job]<]

[i[Programming languages-->Best]]

"Ngôn ngữ lập trình nào là tốt nhất?"

Đây là câu hỏi phổ biến của những người mới bắt đầu học lập trình. Và
thường thì mọi người đều có ý kiến riêng, đặc biệt khi họ mới vào
nghề.

Nhưng bất kỳ ai đã hoạt động trong lĩnh vực này một thời gian sẽ nói
với bạn rằng không có ngôn ngữ lập trình "tốt nhất" nếu không biết bối
cảnh của vấn đề bạn đang giải quyết.

Tôi không biết ai lại tuyên bố rằng [flw[lập trình Bash|Shell_script]]
là ngôn ngữ lập trình tốt nhất. Nhưng chắc chắn có những bài toán mà
thực sự nó lại là giải pháp tốt nhất!

Hãy thử dùng phép so sánh xem! Cái gì tốt hơn: tua vít hay búa? Đây là
câu hỏi đánh lừa! Cả hai đều là công cụ tốt nhất, nhưng chỉ trong bối
cảnh công việc mà chúng được thiết kế cho.

Các ngôn ngữ lập trình khác nhau có điểm mạnh và điểm yếu khác nhau.
Nhiệm vụ của bạn với tư cách là một lập trình viên là chọn búa cho đinh
và tua vít cho vít, và phải thành thạo cả hai công cụ đó. "Tôi không
quen với máy cưa bàn và không thực sự thích nó, nên tôi sẽ dùng cái búa
này để cắt tấm ván ép" không phải là giải pháp mà sếp của bạn đang tìm
kiếm.

> [i[Scuba diving]] **Người hướng dẫn lặn biển của tôi đã cho tôi một
> lời khuyên.** Tôi đang xem xét mua một số thiết bị và đang phân vân
> giữa đồ tiêu chuẩn và thiết bị kiểu
> [flw[DIR|Doing_It_Right_(scuba_diving)]].
>
> Ông nói, "Hãy trở thành người thợ lặn giỏi nhất trong bất kỳ thiết bị
> nào. Tôi không quan tâm nếu anh đang lặn với bộ collar ngựa từ những
> năm 1960 và bình J-valve."

Những lập trình viên giỏi nhất có rất nhiều công cụ trong tay, và họ
biết cách sử dụng chúng.

Vì vậy, khi bạn thấy mình nói, "Ngôn ngữ này tệ và tôi ghét nó so với
ngôn ngữ kia mà tôi yêu thích!" hãy nghĩ đến những trường hợp sử dụng
của ngôn ngữ mà bạn ghét đó. Bởi vì nó được tạo ra với một lý do, và
việc xác định lý do đó có thể giúp bạn biết khi nào bạn _nên_ dùng nó.

Và vì bạn đang nóng lòng muốn biết, ngôn ngữ yêu thích của tôi là Rust.

Hay Python. Hay C. Hay JavaScript. Hay SQL. Hay AWK. Hay Bash. Hay...
thật ra còn tùy thuộc vào vấn đề tôi đang giải quyết!

## Hãy Có Chính Kiến {#be-opinionated}

[i[Being opinionated]<]

Tôi vừa nói xong rằng bạn nên đối xử công bằng với tất cả các ngôn ngữ
và không thiên vị phải không?

Đúng vậy. Nhưng tôi thề điều này không mâu thuẫn với điều đó.

Tại sao cần có chính kiến? Đó là vì bạn nên cân nhắc kỹ lưỡng và có đủ
thông tin khi đưa ra lựa chọn. Và một cách tốt để làm điều đó là có
chính kiến cùng với lý do cụ thể. Nó buộc bạn phải đào sâu vào điểm
mạnh và điểm yếu của các công nghệ khác nhau, và điều đó giúp bạn chọn
ra công cụ tốt nhất trong bộ công cụ của mình cho một công việc cụ thể.

Điều này không có nghĩa là bạn nên cư xử thô lỗ. Đây không phải là
chuyện ai đúng hay ai sai — không có gì trong số này được khắc vào đá
bất biến. Mọi người đều vừa đúng vừa sai cùng lúc. Rất kiểu Schrödinger
của chúng ta.

**Bạn nên có chính kiến về những công cụ mình chọn.** Từ tất cả mọi
thứ trong tay, bạn chọn ngôn ngữ *này* và hệ thống build *này* để sử
dụng. Bạn chọn editor *này* hoặc thư viện *kia*. Bạn nên có lý do giải
thích *tại sao* chúng là tốt nhất, dù có nhiều ngôn ngữ hay công cụ
khác cũng sẽ đáp ứng được yêu cầu.

**Bạn nên có chính kiến về những cấu trúc dữ liệu mình chọn.** Lập
trình là một công việc sáng tạo — bạn có thể biến tất cả mọi thứ thành
[flw[máy Turing|Turing_machine]] nếu muốn và giải quyết vấn đề theo
cách đó, nhưng có rất nhiều lựa chọn khác. Hãy chọn những lựa chọn tốt
nhất và có lý do giải thích *tại sao* bạn chọn chúng trong số tất cả
các lựa chọn khác có sẵn.

**Bạn nên có chính kiến về những thuật toán mình chọn.**
Mergesort chẳng hạn? Cứ dùng đi. Nhưng thực ra có những lúc insertion
sort tầm thường lại tốt hơn! Binary search? Tại sao dùng nó nếu linear
search là đủ tốt cho công việc? Hãy có lý do giải thích *tại sao* bạn
chọn thuật toán đó khi bạn có thể đã dùng một thuật toán khác.

Khi quyết định, bạn có thể đang xem xét những yếu tố như hiệu suất, hay
khả năng đọc của code, hay thời gian phát triển cần thiết, hay chi phí
công cụ, hay công nghệ mà codebase hiện tại đang dùng, hay tất cả các
yếu tố khác.

Bạn luôn phải sẵn sàng học hỏi thêm. Dù bạn chọn gì với lý do của
mình, một nửa Internet sẽ không đồng ý với bạn. Và bạn biết không? Chính
bạn trong tương lai thậm chí cũng có thể không đồng ý với bạn!

Khi học hỏi thêm, bạn sẽ tìm hiểu về những trường hợp cụ thể mà một
công nghệ nào đó là tốt nhất, trong khi trước đây bạn nghĩ nó sẽ không
phù hợp. Hãy cởi mở để học hỏi và thay đổi khi thích hợp. Điều này có
thể là điều gì đó lớn như việc lựa chọn framework cho sản phẩm định nghĩa
toàn bộ công ty của bạn, hoặc điều gì đó nhỏ như việc các biến mảng có
nên đặt tên số nhiều hay không.

Khi trưởng thành, các lựa chọn của bạn sẽ thay đổi. Và, miễn là bạn có
lý do đằng sau đó, đó là điều tốt.

[i[Being opinionated]>]

## Suy Ngẫm Về Chương

* Mô tả quan điểm điển hình của một lập trình viên có kinh nghiệm về
  ngôn ngữ lập trình nào là tốt nhất.

* Tại sao cần có chính kiến về công nghệ?

* Những yếu tố nào cần xem xét khi quyết định công nghệ nào là công cụ
  phù hợp cho công việc?

* Những yếu tố nào cần xem xét khi quyết định công nghệ nào là công cụ
  phù hợp cho công việc mà không được đề cập trong chương này?

* Tại sao việc tiếp tục học hỏi lại quan trọng đến vậy khi lựa chọn
  công nghệ?

[i[Right tool for the job]>]
