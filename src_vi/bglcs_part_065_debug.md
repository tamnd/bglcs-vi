# Debug

[i[Debugging]<]

Trước khi bắt đầu, cách tốt nhất để debug một chương trình là ngay từ
đầu không có bug. Dù chúng ta chỉ là con người và chắc chắn <!-- the
following two words are deliberately misspelled --> mak mstakes, <!--
sic --> cách tốt nhất để tránh bug là tuân theo khung giải quyết vấn đề.
Hãy nhớ rằng trận chiến lập trình nằm ở các giai đoạn _Hiểu_ và _Lên
kế hoạch_. Bạn hoàn thành những giai đoạn đó càng đầy đủ và chính xác,
bạn sẽ càng có ít bug khi viết code.

Như vậy, hãy nói về những việc cần làm khi điều không tránh khỏi xảy
ra.

## Mô Hình Tư Duy

[i[Mental model of computation]<]

Đây là một trong những điều quan trọng nhất để trở thành lập trình viên:
*có mô hình tư duy về quá trình tính toán*.

Tức là, bạn phải có khả năng đọc code và biết điều gì sẽ xảy ra.

``` {.python}
def foo(n):
    i = 0

    while i < n:
        i = i + 1 + (i % 2)

    print(i)

foo(5)
```

Hãy đọc đoạn code Python vô nghĩa ở trên. Tính toán kết quả đầu ra trong
đầu. Rồi xem bạn có đúng không. (Tôi viết code đó, và vẫn mất tôi một
phút tốt đẹp để mô phỏng câu trả lời trong đầu. Nhưng tôi đã đúng!)

***Nếu bạn không thể "chạy" code trong đầu, bạn không thể debug.*** Vâng,
tôi nói thẳng thế. Tôi chắc một số người không đồng ý với tôi, nhưng tôi
muốn nhấn mạnh tầm quan trọng của điều này.

*Debug là nghệ thuật tìm ra phần code nơi mô hình tư duy của bạn về quá
trình tính toán và thực tế của quá trình tính toán không khớp nhau.* Và
sau đó sửa nó.

Nếu bạn không có mô hình tư duy, bạn không có gì để so sánh và sẽ tiến
triển rất ít.

Làm thế nào để cải thiện mô hình tư duy về tính toán của bạn?

* **Nghiên cứu code**. Trace qua nó. Có rất nhiều code ngoài kia để
  luyện tập, ví dụ trên GitHub, trên HackerRank, codebase của bạn học,
  code của chính bạn viết bốn tháng trước mà bạn đã quên nó hoạt động
  thế nào, v.v.

* **Dự đoán kết quả đầu ra**. Khi bạn học code, hãy cố đoán xem nó sẽ
  hoạt động thế nào khi chạy.

* **Trace thủ công một lần chạy**. Dùng bảng trắng để theo dõi thủ công
  các biến nhận giá trị gì, hàm nào được gọi, và đang thực thi dòng code
  nào.

* **Viết đặc tả**. Nghiên cứu một đoạn code và "reverse engineer" nó.
  Tìm hiểu nó làm gì, rồi viết một đặc tả dễ đọc cho người mô tả hoàn
  hảo thuật toán hoặc codebase ở mức độ mà người đọc có thể tái triển
  khai từ đầu.

* **Chạy từng bước với debugger**. Để máy tính chỉ cho bạn thấy chương
  trình đang chạy như thế nào. Chúng ta sẽ nói thêm về điều đó bên dưới.

Bạn chắc chắn sẽ cải thiện kỹ năng này qua thực hành.

[i[Mental model of computation]>]

## Tái Hiện Bug

[i[Debugging-->Reproducing bugs]<]

Trước tiên hãy làm điều này: xem bạn có thể khiến bug xảy ra ổn định
không. Có thể tái hiện ("repro") bug là bước đầu tiên để có thể dẹp nó.

Đôi khi đây thực sự là phần khó. Bạn thấy điều gì đó sai một lần (hoặc
ai đó báo cáo họ thấy nó), và bây giờ bạn không thể repro nó.

> **Tại thời điểm này bạn có thể bị cám dỗ sử dụng một kỹ thuật lập
> trình được gọi là "cầu nguyện"** khi bạn đang cầu nguyện rằng hoặc
> bạn không thực sự thấy nó hoặc bug sẽ không bao giờ nhô mặt xấu xí
> của nó lên nữa trên đời này. Nhưng đây là sự thật đáng buồn: nếu ai
> đó thấy bug hiếm gặp này _chỉ một lần_ khi kiểm thử, hàng nghìn hay
> hàng triệu người sẽ thấy bug khi nó đưa vào production. Định luật
> Murphy _và_ thống kê? Bạn không có cơ hội chống lại điều đó.

Nếu bạn không thể repro nó, bạn chỉ đang bắn vào bóng tối khi cố sửa
nó. Mục tiêu của bạn lúc này là chỉ cần khiến nó xảy ra. Làm việc ngược
lại một cách logic. Điều gì _nhất định_ đã xảy ra trong luồng chương
trình để thấy những gì người báo bug thấy? Tìm ở đó trước. Ngay cả khi
bạn chắc chắn điều kiện nào đó _không thể_ đúng, nếu nó nhất định phải
đúng để thấy bug, thì nó _nhất định_ đã đúng! Tiếp tục trace ngược lại,
tìm nơi mô hình tư duy của bạn và code không khớp và dùng điều đó để
tự repro.

Nếu bạn chỉ có thể repro nó lẻ tẻ, bạn có cơ hội, nhưng sẽ khó. Mục
tiêu của bạn là khiến nó repro ổn định. Điều này giúp bạn không phải
mãi mãi cố gắng repro hiếm gặp. Nếu bạn có thể khiến nó xảy ra ổn định,
đó là tiết kiệm thời gian lớn và giúp bạn thu hẹp nơi bug có thể nằm.

Khi bạn tìm ra cách repro ổn định, bây giờ bạn có thể xử lý có hệ thống
hơn. Bạn muốn tìm số bước tối thiểu có thể khiến bug xuất hiện. Ví dụ,
bạn đang chơi game và thấy bug khi bạn hoàn thành 20 vòng đường đua rồi
lái vào cây. Có thể thử chỉ lái vào cây trước. Nếu may mắn, bạn đã tiết
kiệm được 20 vòng và thu hẹp bug xuống còn cái cây. Nếu không có gì xảy
ra, bạn biết 20 vòng là phần không thể thiếu của bug. Có thể thử một
vòng rồi đến cây. Có repro không?

Tìm số bước tối thiểu không chỉ giúp bạn thu hẹp hơn nữa vị trí bug
trong code, mà còn giúp kiểm thử các bản sửa dễ hơn vì bạn không phải
mất nhiều thời gian để repro vấn đề.

[i[Debugging-->Reproducing bugs]>]

## Tìm Bug

[i[Debugging-->Locating bugs]<]

Có một bug ở đâu đó. Bạn biết điều đó vì khi bạn cung cấp đầu vào cho
code, nó xử lý, và cuối cùng cho ra kết quả bất ngờ.

Ở đâu đó trong quá trình lớn đó, thực tế của tính toán không khớp với
mô hình tư duy của bạn về tính toán.

Ban đầu, tất cả những gì bạn có thể biết là ở đâu đó trong 10.000 dòng
code có điều gì đó sai. Vậy là bạn đã thu hẹp xuống mức đó. Mô hình tư
duy của bạn nói rằng nếu đầu vào là `2`, đầu ra sẽ là `3490`. Nhưng
thay vào đó đầu ra là `299792458`.

Do đó bạn biết bug nằm ở đâu đó giữa đầu vào và đầu ra.

Bạn _có thể_ chỉ bắt đầu thay đổi ngẫu nhiên trong code để xem nó có
được sửa không. Đôi khi được gọi là _shotgun debugging_ hoặc _prayer
debugging_, và nó rất, rất, rất, rất, *rất* hiếm khi hiệu quả. Thường
xuyên hơn nhiều bạn chỉ làm rối tung mọi thứ và khiến vấn đề khó tìm
hơn. Nó giống như cố sửa vấn đề điện của xe bằng cách ngẫu nhiên thêm
và cắt dây. Không đáng để debug theo cách này.

Dù vậy, đây là kỹ thuật rất phổ biến được thực hành, uổng công, bởi
sinh viên trên khắp thế giới. Tuy nhiên bạn không nên dùng nó.

Thay vào đó, đã đến lúc xử lý có hệ thống. Ở đâu đó trong đường ống
tính toán đó, các giá trị trung gian được tính toán không khớp với mô
hình tư duy của bạn. Nhiệm vụ của bạn là tìm ra nơi đó.

Vì vậy bạn bắt đầu thăm dò _bên trong_ chương trình ở các điểm khác
nhau để xem nơi nào mọi thứ đi lệch. Binary search rất hay — nhảy đến
giữa quá trình và kiểm tra các giá trị trong một lần chạy (xem bên
dưới). Nếu chúng như mong đợi, bug vì vậy phải nằm giữa giữa chương
trình và phần cuối! Bạn vừa giảm một nửa không gian tìm kiếm. Bây giờ
làm lại cho đến khi bạn thu hẹp đủ để thấy bug.

Tôi muốn tranh luận, dù một số người có thể không đồng ý, *bug chưa được
tìm thấy cho đến khi bạn hiểu nó*. Tức là, bạn **phải** hiểu chính xác
chương trình của bạn cho ra kết quả `299792458` thay vì kết quả mong
đợi `3490` như thế nào. Hiểu đầy đủ điều đó có nhiều lợi ích:

* Bạn có thể tự tin hơn rằng bạn đã sửa bug thực sự.
* Bạn sẽ học cách nhận ra các mẫu dẫn đến bug này, giúp bạn tránh tốt
  hơn trong tương lai.
* Bạn đang rèn luyện kỹ năng giải quyết vấn đề trong khi làm điều này.

Khi bạn hiểu đầu ra sai được tạo ra như thế nào, hãy sửa vấn đề một
cách dứt khoát và chính xác, và biết tại sao cách sửa sẽ hoạt động.

Cuối cùng, nếu bạn chỉ đang nộp báo cáo bug (tức là người khác sẽ sửa),
có khả năng cung cấp cho họ các bước tối thiểu cần thiết để repro sẽ làm
bạn trở thành anh hùng của họ trong ngày đó. Hãy xem xét từ góc độ
ngược lại; bạn thích sửa bug với chuỗi bước dài dòng mơ hồ để repro,
hay một bug với vài bước khiến nó repro mỗi lần? Càng cụ thể, người sửa
bug càng vui, dù đó là bạn hay người khác.

[i[Debugging-->Locating bugs]>]

## Debug Bằng Print

[i[Debugging-->By printing]<]

Cách thăm dò phần mềm truyền thống tốt bụng khi đang chạy được gọi là
_print debugging_, hoặc nếu bạn là lập trình viên C, _printf debugging_
(đọc là "print eff").

Về cơ bản đây chỉ là việc đặt các câu lệnh in một cách chiến thuật bên
trong code để xem chương trình của bạn đang ở trạng thái nào.

Có một số cách dùng phổ biến:

* In bất cứ thứ gì để xem liệu một phần code có thực sự thực thi không.

  ``` {.python}
  print("A")

  x = foo()

  print("B")

  if x == 3:
      print("C")
      x *= 2
  else:
      print("D")
      bar()

  print("E")
  ```

  Chú ý rằng khi tôi chạy code, tôi có thể thấy nó chạy đến đâu trước
  khi crash, và tôi có thể xác định `x` có bằng `3` không.

* In một số giá trị cụ thể để xem chúng là gì.

  Đây là ví dụ nơi chúng ta lấy dữ liệu từ một cảm biến nào đó trong
  vòng lặp để xử lý. Chúng ta nghi ngờ một số dữ liệu bị lỗi (có thể
  cảm biến bị hỏng) nên đang in ra để xem chúng ta nhận được gì.

  ``` {.python}
  while not done:
      data = get_sensor_data()

      print(f"Got sensor data: {data}")

      process_sensor_data(data)

      done = data < 0
  ```


> **Đừng dùng tục ngữ trong các câu lệnh debug của bạn.**
> Định luật Murphy nói rằng nếu bạn dùng tục ngữ, bạn sẽ quên xóa nó,
> và dù nó ở trong phần code bạn chắc chắn sẽ không bao giờ chạy, nó
> sẽ không tránh khỏi hiện lên màn hình trong khi bạn đang demo cho
> khách hàng trước mặt sếp vào ngày sếp đang đánh giá bạn để tăng
> lương.
>
> Tôi biết rõ hơn ai hết lập trình có thể bực bội đến mức nào. Và khi
> tôi cảm thấy như vậy và quên thở sâu và lấy lại bình tĩnh, tôi in
> cái này:
>
> ``` {.python}
> print("AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA");
> ```
>
> <!-- ` --> Không chỉ nó nổi bật rõ ràng trên màn hình, mà nó còn rất
> dễ gõ khi bực bội và giúp giải tỏa năng lượng tiêu cực của tôi. Và
> nếu khách hàng thấy nó, đó chỉ là lỗi nhỏ.
>
> Một người bạn khác của tôi đề xuất in các emoji không gây phản cảm,
> cũng là cách thú vị để xả stress.

Bây giờ, print debugging bị coi là phương tiện debug kém hơn so với
dùng debugger thật sự (như trong phần sau). Nhưng ai cũng làm vậy vào
một lúc nào đó, và một số người còn thề bằng nó.

Nơi tôi nghĩ nó thực sự tỏa sáng là khi bạn cần thu thập nhiều dữ liệu
về lần chạy để thấy mẫu lớn hơn nổi lên, hoặc khi bạn cần bắt một sự
kiện hiếm gặp. Nếu có gì đó xảy ra một lần trong 10.000 lần chạy, việc
chạy từng bước với debugger tiêu chuẩn sẽ mất mãi. Bạn có thể thêm một
số câu lệnh in và script chạy 10.000 lần và xem kết quả đầu ra để thấy
khi nào nó xuất hiện.

Một điều cần chú ý là nếu bạn đang in nhiều, có thể khó phân tích kết
quả bằng mắt, và thông báo lỗi có thể bị mất trong đó. Tôi khuyên nên
chuyển hướng kết quả vào file rồi mở nó trong editor để tìm kiếm.

Và cuối cùng, đừng quên xóa tất cả các câu lệnh in trước khi bạn giao
nộp công việc!

[i[Debugging-->By printing]>]

## Debugger

[i[Debuggers]<]

Debugger là các công cụ giúp bạn tìm bug. Có nhiều debugger khác nhau,
nhưng hầu hết tất cả đều có chung một tập tính năng. Các tính năng
chính là:

* Thêm _breakpoint_ nơi chương trình sẽ dừng chạy và bạn sẽ có quyền
  kiểm soát trong debugger
* "Single step" qua chương trình từng dòng một
* Kiểm tra giá trị của các biến

Các tính năng bổ sung phổ biến là:

* Bước vào một hàm
* Tiếp tục ra khỏi một hàm
* Bước qua một hàm
* Đặt giá trị của các biến
* Kiểm tra call stack
* Đặt breakpoint kích hoạt theo điều kiện

Hiếm gặp hơn là _time-travel debugger_. Ngoài việc cho phép bạn bước
tiến qua chương trình, chúng còn cho phép bạn bước lùi! Điều này rất
hay nếu bạn bước qua bug vô tình và muốn bước lại để xem nó.

Tất cả các [flw[IDE|Integrated_development_environment]] lớn đều có chức
năng debugger. (Đó là một phần của "tích hợp", chữ "I" trong "IDE".)
Cũng có các debugger độc lập mà bạn có thể chạy. Và tất cả các ngôn ngữ
chính thống đều có hỗ trợ debugger nào đó.

Như bạn có thể tưởng tượng, với những tính năng đó, debugger thực sự
mạnh mẽ.

Nếu bạn nghi ngờ có bug trong hàm `foo()`, bạn có thể đặt breakpoint ở
đó, chạy code, rồi có quyền kiểm soát debugger khi `foo()` thực thi.
Sau đó bạn có thể bước qua từng dòng, xem cách các giá trị của biến
thay đổi. Và không cần thêm bất kỳ câu lệnh in nào.

Chú ý rằng trong VS Code, việc thiết lập debugger có thể là chuyện đơn
giản, hoặc bạn có thể phải chỉnh sửa một số file JSON khó hiểu để nó
hoạt động.

Dù sao đi nữa, học cách dùng debugger là kỹ năng quý giá có thể giúp
bạn tiết kiệm rất nhiều thời gian trong khi cố tìm con quỷ nhỏ đó trong
code.

[i[Debuggers]>]

## Suy Ngẫm Về Chương

* _Mô hình tư duy về tính toán_ là gì và nó quan trọng như thế nào cho
  việc debug?

* Tại sao việc tìm trường hợp tái hiện tối thiểu của bug lại là bước
  quan trọng trong việc sửa bug đó?

* Bạn thu hẹp vị trí bug trong code như thế nào?

* So sánh print debugging với dùng debugger. Bạn nghĩ điểm mạnh và điểm
  yếu tương đối của chúng là gì?

[i[Debugging]>]
