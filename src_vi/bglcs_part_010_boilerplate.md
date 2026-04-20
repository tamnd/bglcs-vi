# Lời Tựa
<!-- Beej's guide to Learning Computer Science
# vim: ts=4:sw=4:nosi:et:tw=72
-->

<!-- No hyphenation -->
<!-- [nh[scalbn]] -->

<!-- Index see alsos -->
<!--
[is[Git Log==>see Log]]
[is[Recursion==>see Recursion]]
-->

Bạn đang bắt đầu tìm hiểu về Khoa học Máy tính, hay đang cân nhắc về
điều đó? Bạn đang nghĩ đến việc lấy bằng? Hay bạn đã đang theo học rồi.
Cuốn hướng dẫn tổng quan này dành cho bạn!

Tôi sẽ không nói nhiều về cách viết code (cũng ít thôi). Và thật ra,
tôi cũng sẽ không nói về khoa học và toán học đằng sau Khoa học Máy
tính — nghe có vẻ mâu thuẫn. Điều tôi sẽ nói trong khoảng 40 trang này
là _cách học_ khi bạn còn là một lập trình viên mới vào nghề.

Nào, dù tôi rất muốn biết chính xác cách mọi người học (và nhồi nhét
điều đó vào 40 trang), nhưng thành thật mà nói, tôi không biết.

Điều tôi có là hơn 40 năm kinh nghiệm lập trình (tự học trước khi vào
đại học), 20 năm kinh nghiệm trong ngành, và hơn 8 năm kinh nghiệm giảng
dạy. Cùng với bằng Cử nhân và Thạc sĩ Khoa học Máy tính.

Và tôi có những quan điểm về cách tốt nhất để học lập trình!

Nói thẳng ra luôn: bạn có thể hoàn toàn không đồng ý với những gì tôi
viết ở đây. Và tôi không sao với điều đó.

Nhưng tôi đã có cơ hội chứng kiến sinh viên mắc phải đủ loại sai lầm.
Và hy vọng tôi có thể giúp một số bạn đọc tránh được những sai lầm đó
ngay từ đầu.

Sinh viên và giảng viên: nếu bạn thấy điều gì đó không đồng ý hoặc điều
quan trọng còn thiếu, xin đừng ngần ngại [fl[cho tôi
biết|mailto:beej@beej.us]] để tôi có thể cải thiện hướng dẫn này.

Khuyến cáo: như với tất cả các hướng dẫn tôi viết, tôi không phải bậc
thầy về chủ đề này. Với một chủ đề mơ hồ như cách con người học, tôi
càng không phải bậc thầy hơn.

Nhưng hãy đọc và lấy những gì hữu ích, phần còn lại thì để lại cho
[flw[boids|Boids]].

## Đối tượng độc giả

[i[Audience]]

Sinh viên đại học mới bắt đầu học lập trình là những người tôi nhắm đến
khi viết cuốn này. Vậy nên độc giả mục tiêu xấp xỉ trong phạm vi đó.
Những người đang học trung học hoặc chỉ muốn học lập trình cũng có thể
là một phần trong số đó.

### Về thuật ngữ "Khoa học Máy tính"

Cuốn hướng dẫn này, ở một mức độ nào đó, được đặt tên chưa thật chuẩn.
Nó không thực sự nói về những gì hầu hết mọi người coi là "khoa học máy
tính". Nó nói nhiều hơn về lập trình — thứ mà các nhà khoa học máy tính,
kỹ sư phần mềm, lập trình viên đều làm rất nhiều.

Tôi đặt tên nó là _Hướng dẫn về Khoa học Máy tính_ vì một vài lý do:

* Ít nhất ở Mỹ, chương trình học mà các nhà phát triển phần mềm theo
  đuổi được gọi là "Khoa học Máy tính" và những người bắt đầu học
  chương trình đó chính là đối tượng mục tiêu.
* Khi bạn bắt đầu học Khoa học Máy tính (bằng cấp), bạn sẽ làm những
  thứ trong hướng dẫn này. Sau đó, khi bạn đến phần Khoa học Máy tính
  (khoa học thực sự) của chương trình, bạn sẽ đã vượt qua nó rồi.

Vậy nên Hướng dẫn này phù hợp để bắt đầu (hy vọng vậy), nhưng hãy hiểu
rằng bạn chỉ đang chập chững bước vào một đại dương bao la chờ được
khám phá.

## Trang chủ chính thức

[i[Home page]]

Địa chỉ chính thức của tài liệu này là:

[fl[`https://beej.us/guide/bglcs/`|https://beej.us/guide/bglcs/]].

## Sửa lỗi

[i[Corrections to the Guide]]

Tôi cung cấp các hướng dẫn này miễn phí với hy vọng chân thành rằng
mọi người sẽ thấy chúng thực sự hữu ích. Nếu có gì đó chưa thực sự hữu
ích (hoặc, bạn biết đấy, "sai"), tôi rất muốn được nghe để có thể sửa
chữa nhằm thực hiện sứ mệnh của mình.

* [fl[Gửi email cho tôi|mailto:beej@beej.us]]
* [fl[Báo cáo sự cố|https://github.com/beejjorgensen/bglcs/issues]]
* [fl[Gửi pull request|https://github.com/beejjorgensen/bglcs]]

Cảm ơn!

## Chính sách Email

[i[Emailing Beej]]

Nhìn chung tôi sẵn sàng hỗ trợ qua email, hãy cứ viết, nhưng tôi không
thể đảm bảo sẽ trả lời. Tôi có cuộc sống khá bận rộn và đôi khi không
thể trả lời câu hỏi của bạn. Khi đó, tôi thường chỉ xóa tin nhắn đi.
Không có gì cá nhân cả; chỉ là tôi sẽ không bao giờ có thời gian để
đưa ra câu trả lời chi tiết mà bạn cần.

Về nguyên tắc, câu hỏi càng phức tạp thì khả năng tôi trả lời càng
thấp. Nếu bạn có thể thu hẹp câu hỏi trước khi gửi cho tôi, và đảm bảo
đính kèm mọi thông tin liên quan (như nền tảng, trình biên dịch, thông
báo lỗi, và bất cứ thứ gì bạn nghĩ có thể giúp tôi gỡ lỗi), bạn sẽ có
nhiều khả năng nhận được phản hồi hơn.

Nếu không nhận được phản hồi, hãy tiếp tục mày mò, cố tìm câu trả lời,
và nếu vẫn bế tắc, hãy viết lại cho tôi cùng với những thông tin bạn đã
tìm được — hy vọng đủ để tôi có thể giúp được.

Sau khi đã dặn dò bạn về cách viết và không viết cho tôi, tôi chỉ muốn
nói rằng tôi _thực sự_ trân trọng mọi lời khen mà cuốn hướng dẫn này
đã nhận được qua nhiều năm. Đó là nguồn động lực thực sự, và tôi rất
vui khi biết nó đang được sử dụng tốt! `:-)` Cảm ơn!

## Nhân bản

[i[Mirroring]]

Bạn hoàn toàn được chào đón khi nhân bản trang này, dù công khai hay
riêng tư. Nếu bạn nhân bản trang này công khai và muốn tôi liên kết đến
từ trang chính, hãy gửi cho tôi một dòng tại
[`beej@beej.us`](mailto:beej@beej.us).

## Lưu ý dành cho người dịch

[i[Translations]]

Nếu bạn muốn dịch hướng dẫn này sang ngôn ngữ khác, hãy viết cho tôi
tại [`beej@beej.us`](mailto:beej@beej.us) và tôi sẽ liên kết đến bản
dịch của bạn từ trang chính. Hãy tự do thêm tên và thông tin liên lạc
của bạn vào bản dịch.

Xin lưu ý các hạn chế về giấy phép trong phần Bản quyền và Phân phối
bên dưới.

## Bản quyền và Phân phối

[i[Distributing the Guide]]

Hướng dẫn học Khoa học Máy tính của Beej là Bản quyền © 2025 Brian
"Beej Jorgensen" Hall.

Với các ngoại lệ cụ thể cho mã nguồn và bản dịch dưới đây, tác phẩm
này được cấp phép theo Giấy phép Creative Commons
Attribution-Noncommercial-No Derivative Works 3.0. Để xem bản sao của
giấy phép này, hãy truy cập:

[`https://creativecommons.org/licenses/by-nc-nd/3.0/`](https://creativecommons.org/licenses/by-nc-nd/3.0/)

hoặc gửi thư đến Creative Commons, 171 Second Street, Suite 300, San
Francisco, California, 94105, USA.

Một ngoại lệ cụ thể đối với phần "Không Có Sản Phẩm Phái Sinh" của giấy
phép là như sau: hướng dẫn này có thể được dịch tự do sang bất kỳ ngôn
ngữ nào ngoài tiếng Anh, với điều kiện bản dịch phải chính xác và toàn
bộ hướng dẫn được in lại đầy đủ. Các hạn chế giấy phép tương tự áp dụng
cho bản dịch cũng như bản gốc. Bản dịch cũng có thể bao gồm tên và
thông tin liên lạc của người dịch.

Mã nguồn lập trình được trình bày trong tài liệu này được cấp cho vùng
công cộng (public domain), hoàn toàn tự do khỏi bất kỳ hạn chế giấy
phép nào.

Các nhà giáo dục được khuyến khích tự do giới thiệu hoặc cung cấp bản
sao của hướng dẫn này cho học sinh của mình.

Liên hệ [`beej@beej.us`](mailto:beej@beej.us) để biết thêm thông tin.

## Lời cảm ơn

Những điều khó khăn nhất khi viết các hướng dẫn này là:

* Tìm hiểu tài liệu đủ chi tiết để có thể giải thích được
* Tìm ra cách giải thích rõ ràng nhất — một quá trình lặp đi lặp lại
  dường như vô tận
* Tự đặt mình vào vị trí một _chuyên gia_ được gọi là, trong khi thực
  ra tôi chỉ là một con người bình thường đang cố hiểu tất cả, giống
  như tất cả mọi người
* Kiên trì tiếp tục khi quá nhiều thứ khác thu hút sự chú ý của tôi

Nhiều người đã giúp tôi trong quá trình này, và tôi muốn ghi nhận những
ai đã làm cho cuốn sách này trở thành hiện thực.

* Tất cả mọi người trên Internet đã quyết định chia sẻ kiến thức của họ
  dưới hình thức này hay hình thức khác. Việc chia sẻ tự do thông tin
  hướng dẫn là điều làm cho Internet trở thành nơi tuyệt vời như vậy.
* Tất cả những ai đã gửi sửa lỗi và pull request về mọi thứ từ hướng
  dẫn dễ gây nhầm lẫn đến lỗi chính tả.

Cảm ơn! ♥
