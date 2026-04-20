# Phân tách vấn đề

[i[Breaking down problems]<]

> _"Có những trò chơi bên ngoài trò chơi."_
>
> —Stringer Bell, _The Wire_

Nếu các bước giải quyết vấn đề (_Hiểu_, _Kế hoạch_, _Viết code_,
_Nhìn lại_) có phần tiếp theo, chương này sẽ là nó.

Những bước đó thực sự giúp bạn vượt qua mọi vấn đề, nhưng hóa ra những
vấn đề đó tồn tại như các vấn đề fractal bên trong vấn đề bên trong
vấn đề.

Ví dụ, có thể bạn muốn đóng một cái bàn. Đó là toàn bộ vấn đề:

* Đóng một cái bàn

Thế nhưng có thể chưa đủ nếu bạn chưa đóng nhiều bàn. Vì vậy bạn phân
tách vấn đề thành các bài toán con phụ thuộc nhau.

* Đóng một cái bàn
  * Gắn chân vào mặt bàn
    * Làm mặt bàn
    * Làm chân bàn

Và có thể vẫn chưa đủ. Làm thế nào để làm chân bàn? Làm thế nào để làm
mặt bàn?

* Đóng một cái bàn
  * Gắn chân vào mặt bàn
    * Làm mặt bàn
      * Đánh nhám bề mặt
        * Dán viền vào mặt bàn
          * Cắt mặt bàn chính
            * Học sử dụng cưa bàn
          * Cắt viền
    * Làm chân bàn
      * Cắt chân bàn
      * Tiện chân bàn trên máy tiện
        * Học sử dụng máy tiện

Và cứ tiếp tục như vậy. *Chúng ta tiếp tục phân tách vấn đề cho đến khi
chúng ta thu được bước đủ nhỏ để biết mình có thể thực hiện được.*

Khi bạn mới bắt đầu, bạn có thể phải rút gọn vấn đề xuống từng dòng
code đơn lẻ. [i[Experts]] Các lập trình viên có kinh nghiệm thường không
cần phân tách đến tận mức đó vì họ đã thành thục trong các bước con.

Ví dụ, một thợ mộc với kinh nghiệm vừa phải có thể chỉ cần phân tách
việc đóng bàn thành bộ bước thứ hai của chúng ta ở trên, và không cần
đi vào chi tiết như vậy.

Như mọi thứ khác, phân tách vấn đề là một kỹ năng, và bạn sẽ giỏi hơn
khi luyện tập.

Khi phân tách vấn đề, hãy nhớ lại cân nhắc trước đó của chúng ta: "Bài
toán này sẽ dễ nếu dữ liệu đầu vào ở _dạng này_." Đó là gợi ý rằng bạn
nên tách ra một bài toán con chuyển đổi dữ liệu đầu vào sang dạng đó,
từ đó làm cho bài toán trở nên dễ.

Và khi bạn có một bài toán con, hãy giả vờ đó là toàn bộ vấn đề, chỉ
trong một chút. Tập trung chặt vào nó và xem liệu bạn có thể giải quyết
nó một cách độc lập không. Nếu không, hãy tự hỏi điều gì sẽ làm cho nó
dễ giải quyết, và tách ra thành một bài toán con.

Lặp lại.

Bạn càng luyện tập phân tách vấn đề và viết code cho giải pháp, bạn sẽ
càng giỏi hơn. Sớm thôi bạn sẽ không cần phân tách vấn đề xa đến mức
bạn cần trước đây, và, giống như một [i[Experts]] chuyên gia, bạn sẽ
bắt đầu nhận ra các mẫu mà bạn có thể tái sử dụng.

Tuy nhiên, không phải lúc nào cũng rõ ràng _cách_ phân tách một vấn đề.

Một kỹ thuật là tưởng tượng một hiện thân vật lý của thứ bạn đang cố
code. (Ví dụ, bạn đang viết một thuật toán sắp xếp? Hãy tưởng tượng một
đống khối chữ cái trên bàn và bạn phải sắp xếp chúng.)

Và sau đó, để đẩy xa hơn, hãy tưởng tượng bạn đang dạy một người bạn
không có kiến thức kỹ thuật cách giải quyết nó. Bạn sẽ mô tả các bước
như thế nào? Các điều kiện? Khi nào họ xong?

Nếu bạn có thể sắp xếp vật lý các cuốn sách trên kệ (dù "sách" là gì),
bạn có thể viết một thuật toán để làm chính xác điều tương tự. Bạn chỉ
cần phân tách các bước.

## Pseudocode

[i[Pseudocode]<]

Một trong những công cụ lớn mà các lập trình viên dùng để khám phá ý
tưởng là viết pseudocode. Đây là "code dành cho con người". Máy tính
không thể đọc được nó. (Mặc dù một số người có thể lập luận rằng Python
khá gần với pseudocode.)

Nhưng bạn có thể dùng nó để phác thảo các bước của một thuật toán hoặc
quy trình để kiểm tra độ hợp lý hoặc chỉ khám phá cách bạn có thể làm
điều gì đó.

Bạn có thể viết một số pseudocode để chèn một giá trị vào một danh sách
đã được sắp xếp.

``` {.default}
find correct spot in list
insert the value there
```

Nhưng điều đó không thực sự mô tả đủ. Chúng ta có thể phải phân tách
tiếp.

``` {.default}
find correct spot in list
    → find first entry larger than the new one
    
insert the value there
    → shift all the higher values to the right
    → insert the new value in the newly-opened spot
```

Đang tiến triển.


``` {.default}
find correct spot in list
    find first entry larger than the new one
        → loop through items, stop when you find a larger one
    
insert the value there
    shift all the higher values to the right
    insert the new value in the newly-opened spot
```

Và bây giờ nó đang trở nên rõ ràng hơn một chút.


``` {.default}
find correct spot in list
    find first entry larger than the new one
        loop through items, stop when you find a larger one
        → record the index before it
    
insert the value there
    shift all the higher values to the right
    insert the new value in the newly-opened spot
        → set the list item at the index to the new value
```

Và chúng ta đang đến rất gần mức có thể dịch pseudocode sang code thực
tế. Có thể vẫn chưa rõ ràng cách chúng ta sẽ dịch chuyển tất cả các giá
trị sang phải, và chúng ta nên phân tách điều đó thêm một chút.

Đôi khi các lập trình viên thêm pseudocode vào code thực của họ dưới
dạng comment và triển khai code thực bên dưới chúng.

Đây là công cụ mạnh mẽ để sử dụng trong giai đoạn _Kế hoạch_. Nó thực
sự có thể giúp củng cố suy nghĩ của bạn về quy trình tổng thể.

[i[Pseudocode]>]

## Bằng chứng khái niệm

[i[Proof of concept]<]

Điều gì sẽ xảy ra nếu bạn đã phân tách bài toán lớn hơn thành các bài
toán con nhỏ hơn, nhưng đơn giản bạn không biết liệu một trong những
thứ đó có khả thi để thực hiện không.

Ví dụ, "Bạn có thể render một hình ảnh vào HTML canvas và sau đó lưu
hình ảnh đó trực tiếp vào thư viện ảnh trên điện thoại di động không?"
Có thể bạn chưa bao giờ làm điều đó, và bạn không biết liệu điện thoại
và công nghệ web có khả năng đó không.

Một cách chắc chắn để tìm hiểu là viết code bằng chứng khái niệm.

Vì vậy bạn tạo một trang web, thêm canvas, vẽ thứ gì đó đặc trưng lên
đó, như một hình chữ nhật, và sau đó thêm code để tải xuống khi nhấn nút.

Điều này trước đây đòi hỏi rất nhiều đọc sách và, sau đó, tìm kiếm
trên web. Và thường vẫn còn như vậy. Nhưng phổ biến hơn bây giờ chúng
ta dựa vào AI[^4914] để trả lời các câu hỏi "nó có thể và làm thế nào",
và thậm chí đưa ra một số code bằng chứng khái niệm.

[^4914]: Một lần nữa, nếu được phép trong môi trường làm việc hoặc
trường học của bạn.

Khi bạn có code hoạt động, bạn biết hai điều:

1. Nó hoạt động!
2. Cách viết code để thực hiện điều đó.

Thường thì code bằng chứng khái niệm chưa sẵn sàng cho môi trường sản
xuất, nhưng tạo thành cốt lõi của những gì bạn sẽ cuối cùng bàn giao.

Một cách sử dụng khác của code bằng chứng khái niệm là để trình bày
cho mọi người thấy sản phẩm hoàn thiện sẽ trông như thế nào hoặc hoạt
động như thế nào. Đôi khi người ta viết code một triển khai giả, nơi
chỉ một phần nhỏ của giao diện người dùng hoạt động nhưng người xem có
thể nắm được ý tưởng về cách phần mềm cuối cùng sẽ hoạt động.

Thường thì phần lớn code bạn đã viết cho bằng chứng khái niệm sẽ bị bỏ
đi, và bạn có thể cảm thấy kháng cự khi loại bỏ công việc đó. Nhưng
đừng lo lắng về nó. Phần quan trọng của bằng chứng khái niệm là kiến
thức thu được trong khi làm việc, không phải bản thân công việc.

[i[Proof of concept]>]

> _"Hãy lên kế hoạch vứt bỏ một cái; dù sao bạn cũng sẽ làm vậy."_
>
> —Fred Brooks, _The Mythical Man-Month_

## Suy ngẫm về chương

* Tại sao việc phân tách một vấn đề lại quan trọng?

* Bạn phải phân tách vấn đề đến đâu trước khi có thể bắt đầu viết code?

* Pseudocode là gì và tại sao chúng ta viết nó?

* Bằng chứng khái niệm là gì và tại sao nó hữu ích?

[i[Breaking down problems]>]
