# Học Một Ngôn Ngữ Mới

[i[Programming languages-->Learning]<]

Ngôn ngữ đầu tiên bạn học là khó nhất. Không chỉ học ngôn ngữ, bạn còn
đang học các _khái niệm_ được dùng trong ngôn ngữ đó. Ý tôi về khái
niệm là những thứ như cách tổ chức hàm và truyền đối số, cách chạy
vòng lặp, cách làm điều kiện, v.v.

Tất cả các ngôn ngữ đều có chung các khái niệm này (nhiều hay ít — sẽ
nói thêm sau), và vì vậy học ngôn ngữ thứ hai chỉ là học cách áp dụng
những khái niệm bạn đã biết.

Nó giống như nếu bạn đã biết tiếng Tây Ban Nha, học tiếng Ý không phải
bước nhảy lớn.

Chương này nói về việc học thêm ngôn ngữ sau khi bạn đã học ngôn ngữ
đầu tiên. Điều này quan trọng vì bạn sẽ học ngôn ngữ mới trong suốt sự
nghiệp của mình. May mắn thay, học ngôn ngữ mới tự nó là một kỹ năng,
và bạn càng học nhiều ngôn ngữ mới, nó càng trở nên dễ hơn.

[i[Programming paradigms]]

Có hai phần lớn để học ngôn ngữ mới trong mô hình bạn đã biết (thủ tục,
hướng đối tượng, hàm, v.v.)

1. **Học cú pháp**. Như `if` và `while`, và cách khai báo biến và hàm,
   v.v.

2. **Học thư viện chuẩn**. Đây là chức năng tích hợp sẵn mà bạn có thể
   tận dụng, như đọc và ghi file, in ra màn hình, hoặc kết nối với web
   server.

Học cú pháp thường là phần dễ hơn trong hai. Hầu hết các ngôn ngữ có
cú pháp tương đối đơn giản.

Để so sánh, bạn có thể học động từ, danh từ, tính từ là gì và cách
[flw[phân tích câu|Sentence_diagram]]. Nhưng đó chưa đủ để viết một tác
phẩm văn học xuất sắc. Bạn cũng cần biết những từ nào có trong tay.

Và đó là phần phức tạp hơn. Nhiều thư viện chuẩn có *rất nhiều* chức
năng tích hợp sẵn. [fl[Hãy lướt qua thư viện chuẩn Python xem ví dụ|https://docs.python.org/3/library/index.html]].

## Học Cú Pháp

[i[Programming languages-->Syntax]<]

Nhảy thẳng vào! Theo một hướng dẫn và viết các chương trình "toy". Đây
là những chương trình chỉ luyện tập một khía cạnh nào đó của ngôn ngữ.

Chúng ta làm điều kiện trong Rust như thế nào? Hãy viết một chương trình
toy để tìm hiểu.

``` {.rs}
fn main() {
    if (1 == 2) {
        println!("Something is horribly wrong.");
    } else {
        println!("That's correct.");
    }
}
```

Đợi đã — những dấu ngoặc đơn đó có cần thiết quanh `if` không?

``` {.default}
$ rustc foo.c
  warning: unnecessary parentheses around `if` condition
```

Không cần! Đây là chương trình toy; chúng ta chỉ dùng nó để học.

Để học tất cả cú pháp cần thiết, hãy lấy các khái niệm bạn đã biết và
tìm hiểu cách áp dụng chúng trong ngôn ngữ mới.

* Hàm main
* Biến
* Điều kiện
* Vòng lặp
* Class
* v.v.

Lúc đầu sẽ gây bực bội vì bạn phải tra cứu từng. Thứ. Một. Giống như
với một ngôn ngữ người mới, bạn biết về mặt khái niệm rằng bạn muốn đi
đến siêu thị, nhưng bạn phải tra tất cả những từ tiếng Ý đó nếu bạn
không biết tiếng Ý.

Tin tốt là cú pháp của ngôn ngữ máy tính *đơn giản hơn nhiều* so với
ngôn ngữ người. Và bạn có thể nắm vững nó khá nhanh.

[i[Programming languages-->Syntax]>]

## Học Thư Viện

[i[Programming languages-->Libraries]<]

Thư viện chuẩn là chức năng đã được tích hợp sẵn đi kèm với ngôn ngữ.
Điều này tiện lợi vì bạn biết rằng tất cả mọi người đã cài ngôn ngữ đều
có sẵn tất cả các hàm này và không phải tải xuống bất kỳ phụ thuộc bên
thứ ba nào thêm.

Nhưng bạn cần quen thuộc với thư viện chuẩn của ngôn ngữ đó để biết
ngôn ngữ có thể làm gì sẵn có, và để không tái phát minh bánh xe khi
không cần thiết.

Một khuyến nghị là lướt qua thư viện chuẩn của ngôn ngữ bạn đang dùng.
Bạn không phải biết chính xác cách sử dụng chức năng
[flw[IMAP|Internet_Message_Access_Protocol]] của Python, nhưng biết nó
có sẵn trong trường hợp bạn cần là rất có giá trị. Ít nhất, nó cho bạn
biết Python là ứng viên để lựa chọn ngôn ngữ nếu bạn cần làm việc với
IMAP.

Rồi khi bạn thực sự cần một số chức năng đó, bạn có thể đào sâu vào
tài liệu và ví dụ để xem nó hoạt động thế nào.

Tôi có xu hướng học thư viện theo từng mảnh, chỉ học chi tiết những gì
tôi cần để hoàn thành công việc. Tôi biết phần còn lại của những gì nó
_có thể_ làm (vì tôi đã lướt qua tài liệu), nhưng tôi chỉ biết từng
mảnh và miếng đủ để code với chúng.

Và điều đó ổn, vì các thư viện rất đồ sộ, và khó có thể đạt được sự
thành thạo mọi thứ trong đó. Bạn chỉ cần có thể học những gì bạn cần
để hoàn thành công việc.

[i[Programming languages-->Libraries]>]

## Học Một Mô Hình Mới

[i[Programming paradigms-->Learning]<]

Trước tiên, _mô hình lập trình_ là gì? Đó là cách mô hình hóa bài toán
để bạn có thể đưa ra giải pháp. Tôi biết điều đó mơ hồ nhưng hãy kiên
nhẫn với tôi vài đoạn.

Hãy tưởng tượng đang làm khai thuế. (Xin lỗi.) Khi làm, đó là một chuỗi
các bước liên tiếp. Điền tên. Điền thu nhập. Nếu thu nhập lớn hơn một
giá trị nào đó, làm _x_. Còn lại làm _y_. Đó là một thủ tục bạn đang
theo. Bạn có thể mô hình hóa nó như một chuỗi các bước.

Hãy tưởng tượng bạn đang mô phỏng một thế giới fantasy 3D. Trong thế
giới đó, bạn có thể có một loại sinh vật gọi là orc, và có thể có nhiều
sinh vật loại đó chạy xung quanh. Và chúng đều có tọa độ riêng, và
[flw[điểm máu|Health_(game_terminology)#Hit_points]] riêng của chúng,
nhưng chúng đều có cùng hành vi khi bạn tiến lại gần. Bạn có thể mô
hình hóa chúng như một tập hợp các đối tượng độc lập nhưng có hành vi
tương tự.

Đây là hai cách khác nhau để giải quyết bài toán, hoặc bằng cách mô
hình hóa chúng như một chuỗi các bước, hoặc như các đối tượng.

Chúng ta gọi các mô hình khác nhau này là _mô hình lập trình_. Ví dụ
đầu là "lập trình thủ tục" (kiểu vậy; tôi đang lướt qua một chút), và
ví dụ thứ hai là "lập trình hướng đối tượng".

Có [flw[rất nhiều mô hình|Programming_paradigm]], nhưng Bộ Ba Lớn là
thủ tục, hướng đối tượng, và hàm.

Đây là điều đáng lo: học một mô hình mới thì khó. Khó hơn nhiều so với
chỉ học một ngôn ngữ khác trong cùng mô hình.

Nếu bạn biết tiếng Tây Ban Nha, học tiếng Ý tương đối dễ. Nhưng học
tiếng Trung, đó là điều khác! Không dễ như vậy. Tiếp tục phép so sánh,
đó là mô hình khác. Bạn phải học các kỹ thuật và khái niệm mới mà bạn
thậm chí có thể chưa biết đến từ các ngôn ngữ Roman.

> **Tôi đã học [i[Erlang]] Erlang một thời gian trước**.
> [fl[Erlang|https://www.erlang.org/]] là một ngôn ngữ hàm, và tôi còn
> yếu với mô hình hàm.
>
> Ví dụ, trong Erlang, khi bạn đặt một "biến", bạn không bao giờ có thể
> thay đổi nó. Và mọi cách tôi biết để mô hình hóa bài toán đều liên
> quan đến việc thay đổi biến!
>
> Ý tôi là, bạn làm gì _bất cứ thứ gì_ nếu không thể thay đổi biến?!
>
> Nhưng rõ ràng, các hệ thống lớn đã được triển khai thành công trong
> Erlang, vậy nên có cách. Nhưng tôi phải thay đổi cách suy nghĩ về cách
> mô hình hóa bài toán, và việc học cách mới đó là một thách thức đáng
> kể.

Lời khuyên chính của tôi ở đây là dùng _rất nhiều_ ví dụ để thấy ngôn
ngữ đó thực hiện các tác vụ cơ bản thế nào. Tức là, thu thập và nghiên
cứu nhiều chương trình toy.

Rồi đặt ra các thách thức liên quan (hoặc tìm một số trên mạng, hoặc
nhờ AI tạo) cho phép bạn luyện tập để xây dựng kỹ năng và tìm ra các
lỗ hổng trong hiểu biết của mình.

[i[Programming paradigms-->Learning]>]

## Suy Ngẫm Về Chương

* Tại sao học ngôn ngữ lập trình đầu tiên lại khó hơn học ngôn ngữ thứ
  hai?

* Sự khác biệt giữa học cú pháp và học thư viện là gì?

* Sự khác biệt giữa ngôn ngữ lập trình và mô hình lập trình là gì?

* Tại sao học một mô hình mới thường khó hơn học một ngôn ngữ lập trình
  mới trong mô hình bạn đã biết?

[i[Programming languages-->Learning]>]
