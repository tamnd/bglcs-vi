# Giải quyết vấn đề

[i[Problem solving]<]

Đây là ý tưởng được "đánh cắp" hoàn toàn từ cuốn sách [i[How to Solve It
book]] [flw[_How to Solve It_|How_to_Solve_It]] của George Pólya. Đó là
cuốn sách về cách tiếp cận các bài toán toán học. Và vì khoa học máy
tính về bản chất cũng là toán học, nó hoàn toàn áp dụng được!

Thực ra không hoàn toàn áp dụng được, và tôi chỉ nói vậy vì nghe hay.
Nhưng có thể uốn nắn cho phù hợp khá dễ. Và tôi khuyên bạn nên đọc cuốn
sách này.

Vậy nó là gì? Ngắn gọn và khá dễ thuộc:

[i[Problem solving-->Steps]]

1. **Hiểu** vấn đề
2. **Lên kế hoạch** giải quyết nó
3. **Viết code** cho giải pháp
4. **Nhìn lại** những gì có thể làm tốt hơn

Chỉ vậy thôi.

Và nếu bạn nghĩ về nó, đó thực chất chỉ là quy trình bốn bước để giải
quyết hầu như bất kỳ vấn đề nào. Đèn phòng khách không sáng à? Bạn có
thể giải quyết nó bằng các bước này.

> _"Toán học không phải là về con số. Nếu bạn nghĩ toán học là về con
> số, bạn có thể nghĩ rằng Shakespeare chỉ là về các từ ngữ. Bạn có thể
> nghĩ rằng khiêu vũ chỉ là về giày. Bạn có thể nghĩ rằng âm nhạc chỉ
> là về nốt nhạc. Toán học không phải là về con số. Toán học là về logic,
> về vẻ đẹp, về các kết nối, về cách bạn đi từ nơi này đến nơi khác."_
>
> —Cliff Stoll

Lập trình không phải là về viết code. **Bước 1, 2, và 4 không liên quan
đến việc viết code**[^3cfe]. Những bước này đều diễn ra trong đầu bạn và
trên giấy. Tôi sẽ lập luận rằng ***giải quyết các bài toán lập trình
không liên quan đến máy tính***. Nghe có vẻ vô lý rõ ràng, nhưng đó
chính là nơi hành động thực sự xảy ra! Đặc biệt ở bước 2, đưa ra
_Kế hoạch_. Đó là phần khó. Đó là lý do bạn được trả lương cao. Ai
cũng có thể gõ một chương trình vào sau khi vấn đề đã được giải quyết.

[^3cfe]: Đôi khi thực ra có thể, nhưng chỉ để viết các chương trình
    nhỏ, dùng một lần, khám phá mang tính bằng chứng khái niệm.

Bước 3, _Viết code_, đơn giản chỉ là ghi lại giải pháp. Công việc khó
không phải là ghi lại giải pháp; công việc khó là đưa ra nó ngay từ đầu!

Ngoài ra, bạn khó có thể tiến hành tuyến tính qua các bước này. Bạn có
thể phải quay lại và xem xét lại các bước trước từ thời gian này sang
thời gian khác, nhưng hy vọng tiến trình tổng thể của bạn là theo hướng
về phía trước.

Cuối cùng, với tư cách là sinh viên, bạn phải cưỡng lại sự thôi thúc
tra cứu câu trả lời. Mục tiêu ở đây là để bạn tập luyện cơ giải quyết
vấn đề (vì không ai sẽ thuê bạn làm lập trình viên mà không có những kỹ
năng đó). Hầu như mọi bài toán mà giảng viên nào cũng có thể nghĩ ra đều
đã được đề cập rộng rãi trên Internet hoặc có thể được giải bởi AI. Hãy
nhớ rằng nhận được câu trả lời đúng không phải là điểm mấu chốt; điểm
mấu chốt là luyện tập giải quyết vấn đề để bạn có thể đưa ra câu trả lời
cho bất kỳ bài toán nào được đặt ra cho bạn.[^b374]

[^b374]: Tôi không nghĩ AI có thể giải quyết *tất cả* các vấn đề được
    đặt ra cho nó, nghĩa là bạn vẫn sẽ có việc làm, nhưng chúng có thể
    giải quyết các bài toán tương đối cơ bản thường được dùng trong
    chương trình khoa học máy tính. Đây là năm 2025 và chúng ta sẽ xem
    ghi chú chú thích này "già" đến mức nào.

Hãy cùng khám phá các bước.

## Hiểu vấn đề

[i[Problem solving-->Understanding phase]<]

Tất cả mọi người, kể cả sinh viên, đều thích bỏ qua bước _Hiểu_. Các
giảng viên khôn ngoan sẽ thêm một bài kiểm tra cần nộp trước khi bắt
đầu viết code để xác minh bạn hiểu vấn đề[^873c]. Nhưng bạn cần tự ép
buộc mình thực hiện bước này trước, bất kể thế nào.

[^873c]: Tôi cũng cần phải khôn ngoan hơn.

Về mặt logic, nếu bạn không hiểu đầy đủ vấn đề, không có bước nào còn
lại quan trọng. Bạn có thể đưa ra kế hoạch tốt nhất và viết code hoàn
hảo cho nó, nhưng nếu bạn không hiểu vấn đề ngay từ đầu, bạn vừa viết
code cho giải pháp hoàn hảo của sai vấn đề![^8050]

[^8050]: Một lần trên một trang web thử thách lập trình tôi đã viết code
    cho giải pháp hoàn hảo của *hai* bài toán không phải bài tôi cần
    giải. Tôi đã hiểu sai đến hai lần. Mất gấp ba lần thời gian cần
    thiết để đưa ra giải pháp thực sự.

Và đó là lãng phí thời gian và tiền bạc của người thuê bạn, trong
trường hợp tốt nhất. Hoặc, nếu bạn vẫn còn là sinh viên, là lãng phí
thời gian bạn lẽ ra có thể dùng để học cho bài kiểm tra toán rời rạc
sắp tới. Hay gì đó.

Vậy đừng cắt xén bước này — nó cực kỳ quan trọng về mặt nền tảng.

Bạn nên làm gì? Dưới đây là một số ý tưởng.

* Đọc vấn đề chậm và có phương pháp. Các mô tả này có xu hướng ngắn gọn
  và dễ gây nhầm lẫn. Chúng không dễ đọc, vì vậy đừng cố lướt qua. Đọc
  lại các câu nhiều lần đến khi hiểu ý nghĩa của chúng.
* Ghi chú. Đặc biệt ghi lại những điểm không nhất quán, bỏ sót, lỗi, và
  các câu hỏi còn tồn đọng.
* Viết lại vấn đề bằng lời của bạn. Đây là kỹ thuật rất hiệu quả giúp
  bạn tìm ra các khoảng trống trong sự hiểu biết của mình.
* Nghiên cứu khi cần thiết.
* Đặt câu hỏi làm rõ[^99ca].

[^99ca]: Đây thực ra là một phần trong mô tả công việc của bạn với tư
    cách là lập trình viên. Mọi người sẽ mong đợi và dựa vào bạn làm
    điều này tại nơi làm việc. Vì vậy đừng ngại làm; hãy ngại *không*
    làm.

***Bạn đã hoàn thành bước này khi bạn có thể dạy người khác vấn đề là
gì.*** (Bạn không cần dạy giải pháp — chỉ cần vấn đề.)

Thật rất, *rất* khó để viết một mô tả đầy đủ về một vấn đề, và những
cái bạn nhận được ở nơi làm việc hay ngay cả trong trường học chắc chắn
sẽ còn thiếu sót. Không tin tôi? Hãy viết xuống các quy tắc của trò
tic-tac-toe ("noughts and crosses" nếu bạn gọi như vậy) và tôi đảm bảo
tôi sẽ tìm thấy điều gì đó bạn chưa viết xuống[^5b26].

[^5b26]: Bạn chưa nói cách chọn ai đi trước, liệu có thể chơi với ba
    người không, hay là "X" của tôi không thể chiếm nhiều hơn một ô.
    Ví dụ vậy.

Do đó, bạn rất có thể sẽ phải hỏi các câu hỏi làm rõ.

> **Đến phần giai thoại!** Tôi đã tham gia một dự án viết phần
> front-end của một hệ thống và người khác viết back-end. Có một tài
> liệu rất cụ thể mô tả chính xác sự tương tác giữa hai phần.
>
> Một trong các tương tác liên quan đến việc truyền kết quả của một phép
> tính. Có một ví dụ trong tài liệu cho câu trả lời, ở dạng hex, của
> phép tính toán. Nó đại loại như:
>
> > Với đầu vào `"abc"` và `"xyz"`, kết quả sẽ là số `f319c2c6dcfb`.
>
> Tôi đã viết code (dễ vì pseudocode của thuật toán đã được cung cấp),
> và nó tính ra câu trả lời đúng. Tôi thêm code để truyền số 6 byte đó
> đến server và xong.
>
> Nhưng người viết server nhắn cho tôi nói tôi đang gửi rác.
>
> Chúng tôi trao đổi qua lại, và hóa ra họ nghĩ spec có nghĩa tôi sẽ
> gửi một chuỗi chứa những chữ số hex đó, còn tôi nghĩ spec có nghĩa
> tôi sẽ gửi các byte thô của kết quả. Spec không giúp ích gì — nó mơ
> hồ và cả hai chúng tôi đều không nhận ra điều đó.
>
> Cách dễ nhất là tôi chuyển số sang chuỗi và gửi đi, vì vậy tôi thêm
> dòng code đó và vấn đề biến mất. Nhưng chúng tôi có thể đã phát hiện
> ra sớm hơn nếu xem xét spec kỹ hơn.

[i[Problem solving-->Understanding phase]>]

## Đưa ra kế hoạch

[i[Problem solving-->Planning phase]<]

> _"Lập trình là nghệ thuật nói với một người khác điều mình muốn máy
> tính thực hiện."_
>
> —Donald Knuth

Đã đến lúc bắt đầu viết code? **KHÔNG!** Chưa phải lúc, bạn ơi![^77b5]

[^77b5]: Tính đến năm 2025, tôi làm việc tại Đại học Bang Oregon. Hãy
tiến lên, Beavs!

Bước này, đưa ra kế hoạch, là nơi lập trình thực sự diễn ra. Như tôi đã
nói trước đó, đây là điều làm cho công việc trở nên khó khăn, và là lý
do nó được trả lương tốt. Để trở thành một lập trình viên tàm tạm, bạn
cần xuất sắc trong việc đưa ra kế hoạch vững chắc.

Trước tiên bạn phải _Hiểu_ vấn đề đủ để có thể giải thích cho người
khác. Hoặc ít nhất bạn *nghĩ* bạn hiểu. Bạn có thể học thêm sau. Nhưng
hiểu vấn đề không giống như biết cách giải quyết nó.

Nếu vấn đề thực sự đơn giản và quen thuộc, bạn có thể nghĩ ra kế hoạch
gần như ngay lập tức. [i[Experts]] Các lập trình viên có kinh nghiệm đối
mặt với các nhiệm vụ quen thuộc không cần bỏ nhiều thời gian lập kế
hoạch khi đã hiểu đầy đủ vấn đề.

Nhưng [i[Experts]] các lập trình viên có kinh nghiệm đối mặt với các
nhiệm vụ không quen thuộc *cần* bỏ thời gian vào đó. Dù bạn giỏi đến
đâu — nếu bạn chưa gặp vấn đề này, bạn sẽ cần phải lập kế hoạch cho
giải pháp.

Bút chì và giấy thực sự có thể hữu ích cho bước này. Dưới đây là một số
điều cần suy nghĩ.

* Dữ liệu sẽ chạy qua hệ thống và được biến đổi như thế nào, từ đầu vào
  đã biết đến đầu ra mong muốn?

* Trong những phép biến đổi đó, các hệ thống con nào sẽ thực hiện mỗi
  bước?

* Bạn cần những công nghệ nào để thực hiện các bước này?

* Những điều không biết đã biết là gì?

Một điều lớn cần lưu ý là chúng ta đang nói về việc phân tách vấn đề
thành các thành phần con của nó. Cách làm điều này không phải lúc nào
cũng rõ ràng, mặc dù bạn càng có nhiều kinh nghiệm thì nó càng dễ hơn.

Một mẹo bạn có thể dùng là nghĩ, "Dự án này sẽ dễ nếu chỉ cần dữ liệu
đầu vào ở *dạng này*." Sau đó xem liệu bạn có thể nghĩ ra đoạn code nào
chuyển đổi dữ liệu sang dạng đó không. Chúng ta sẽ đi sâu hơn ở chương
sau.

Một lợi ích khác của việc chia dự án thành các phần nhỏ hơn là nó có
thể tự nhiên gợi ý cách chia code thành các hàm hoặc lớp nhỏ hơn. Điều
này làm cho code dễ bảo trì và đọc hơn.

Bạn sẽ phải thực hiện một số nghiên cứu trong giai đoạn này để tìm hiểu
những công cụ nào bạn có trong tay. Hãy mong đợi điều đó.

*Thực sự* phổ biến trong giai đoạn lập kế hoạch khi nhận ra rằng bạn đã
không hiểu đầy đủ vấn đề. Khi điều này xảy ra, hãy quay lại giai đoạn
_Hiểu_ để làm rõ, rồi quay trở lại lập kế hoạch.

***Bạn biết mình đã xong lập kế hoạch khi bạn có thể mô phỏng việc chạy
trên giấy và trong đầu và bạn tự tin là nó hoạt động. Và bạn có thể
viết pseudocode cấp cao.*** Chia sẻ kế hoạch của bạn với vài con [i[Rubber ducking]]
vịt cao su[^c2a3] để xem nó có vững chắc không.

[^c2a3]: _Rubber ducking_ là việc chia sẻ ý tưởng với một con vịt cao su
    thực sự hoặc đại diện thay thế, có thể thực ra là một người. Nó
    giúp bạn làm rõ suy nghĩ và đạt được đột phá trong giải quyết vấn
    đề. Ngoài ra, Ducks là đội bóng bầu dục của Đại học Oregon, đối thủ
    lâu năm của Bang Oregon. Boo Ducks!

[i[Problem solving-->Planning phase]>]

## Viết code cho giải pháp

[i[Problem solving-->Coding phase]<]

Đây là phần dễ! Bạn phải dịch các kế hoạch pseudocode thành code.

Nếu bạn đã hiểu vấn đề và đưa ra kế hoạch vững chắc, code sẽ hoạt động.
Thậm chí có thể ngay từ lần đầu, nếu bạn rất may mắn[^b1f5].

[^b1f5]: Điều này rất hiếm khi xảy ra với tôi. Khi xảy ra, tôi nhanh
    chóng nhìn ra cửa sổ để đảm bảo bầu trời trong xanh và tôi sắp không
    bị sét đánh. Và tôi mua vé số. Đó chắc chắn là lúc vận may của tôi
    cạn kiệt.

Nếu bạn _không_ hiểu vấn đề và không đưa ra kế hoạch, thì đây không
phải là phần dễ. Bạn sẽ thấy vô số rắc rối, và có thể không hoàn thành
dự án. _Đó_ là mức độ quan trọng của việc hiểu và lập kế hoạch!

Tất nhiên, chúng ta chỉ là người và sẽ gõ sai và mắc lỗi ngớ ngẩn,
nhưng điều đó *dễ* debug hơn nhiều so với việc bạn có kế hoạch tồi, hoặc
tệ hơn, hiểu vấn đề sai. Ôi thôi!

Những phần khó của việc viết code là:

* Biết cú pháp ngôn ngữ.
* Biết những thư viện nào có sẵn.
* Không mắc lỗi vặt.
* Theo sát kế hoạch.

Chúng ta sẽ nói về cách học ngôn ngữ sau, và hai điểm bullet cuối có
thể được giải quyết bằng cách cẩn thận hơn, sử dụng thứ gì đó như
[flw[lập trình theo cặp|Pair_programming]], hoặc nhờ AI hỗ trợ.

Trong khi viết code, bạn có thể tìm thấy chỗ mà kế hoạch của mình không
hoạt động. Điều này xảy ra khá thường xuyên. Khi xảy ra, hãy quay lại
giai đoạn lập kế hoạch, sửa kế hoạch, rồi quay lại giai đoạn viết code
để thực hiện nó.

Một lần nữa, giai đoạn này được cho là tương đối dễ. Nếu bạn đang gặp
khó khăn khi cố làm cho nó hoạt động ngoài việc chỉ sửa lỗi cú pháp
(tức là có gì đó sai về cấu trúc hơn), sự hiểu biết hoặc kế hoạch của
bạn có thể có lỗi. Bạn nên quay lại giai đoạn lập kế hoạch để sửa, và
có thể quay lại giai đoạn hiểu, nếu cần.

***Bạn đã xong giai đoạn này khi code hoạt động và vượt qua tất cả các
bài kiểm tra.***

[i[Problem solving-->Coding phase]>]

## Nhìn lại để cải thiện

[i[Problem solving-->Reflection phase]<]

> "Lập trình là một nghề thủ công. Hãy tự hào về công việc của bạn."
>
> —Chính tác giả

Cuối cùng nhưng chắc chắn không kém quan trọng, hãy nhìn lại và nhìn
với con mắt phê phán vào những gì bạn đã làm. Vâng, nó hoạt động và
vượt qua tất cả các bài kiểm tra. Nhưng nó có thanh lịch như có thể
không? Nó có dễ đọc và dễ bảo trì như có thể không? Có những chỗ nào
code mong manh và có thể thất bại với đầu vào không mong đợi không?

Dù kỹ năng của bạn ở mức nào, luôn còn chỗ để cải thiện. Và một trong
những cách hàng đầu chúng ta học là nhìn lại code tệ hại mình đã viết và
xem mình có thể làm tốt hơn như thế nào.

Code review thật tuyệt vời nếu bạn có thể thuyết phục ai đó bỏ thời
gian làm điều đó cho bạn. Họ sẽ đưa ra gợi ý về những thứ bạn có thể
cải thiện, và bạn có thể sửa chúng ngay bây giờ và ghi nhớ cho lần sau.
Và bạn có thể không đồng ý và không thực hiện những sửa chữa đó; điều
đó cũng ổn.

Một lần nữa, chúng ta có thể tận dụng AI để hỗ trợ điều này. Khi bạn
đã giải quyết được vấn đề và có nó hoạt động, hãy hỏi AI về các gợi ý
cải thiện[^08dd] và xem có điều gì đáng theo không. Kỹ thuật này hiệu
quả với các đoạn code nhỏ, không phải các dự án lớn, nhưng điều đó làm
cho nó trở thành một trợ lý tuyệt vời cho công việc đại học.

[^08dd]: Đảm bảo giảng viên và/hoặc người sử dụng lao động của bạn cho
phép điều này.

> **Nhưng, rất quan trọng đối với sinh viên đại học, bạn cần giải quyết
> vấn đề trước**, và chỉ sau đó mới nhờ AI giúp bạn cải thiện nó. Mục
> tiêu của bạn trong luyện tập ở trường (giống như luyện tập ở phòng
> gym) là được luyện tập với phản hồi, không phải để người khác làm việc
> cho bạn.

Code có thể tệ theo nhiều cách. Nó có thể có lỗi. Nó có thể không hiệu
quả. Nó có thể có định dạng kém. Và nó đơn giản là không thể đọc được.
Hãy nhớ rằng để code của bạn có thể bảo trì được, nó cần phải dễ hiểu
đối với những người khác. Hãy làm nó trông gọn gàng. Trình biên dịch có
thể hài lòng với code không thể đọc được, nhưng con người không nên chấp
nhận điều đó.

***Bạn không bao giờ hoàn thành giai đoạn này.*** Thực tế, bạn xong khi
bạn bỏ cuộc và quyết định đã học đủ về việc cải thiện code. Nhưng bạn
có thể sẽ không tìm ra _Giải Pháp Tối Thượng Cho Vấn Đề Mãi Mãi_ vì
bạn vẫn đang xây dựng kỹ năng của mình suốt đời.

Dù vậy, đây là giai đoạn nơi **rất nhiều** việc học xảy ra. Đây là nơi
bạn có thể xây dựng hiệu quả kỹ năng của mình với nỗ lực tương đối
thấp. Và bạn sẽ thiệt thòi nếu không dành chỉ vài phút sau một dự án
để tận dụng điều đó.

Ở nơi làm việc, điều này có dạng là một [i[Post-mortem]] _post-mortem_,
nơi những người tham gia dự án đã hoàn thành nhìn lại và nghiên cứu
những gì đã đúng và sai.

[i[Problem solving-->Reflection phase]>]

## Suy nghĩ như kẻ phản diện

[i[Villains]<]

Khi giải quyết vấn đề, tôi muốn bạn suy nghĩ như một kẻ phản diện; đó
là, nghĩ như một người sẽ lạm dụng hệ thống mà bạn đang thiết kế và
xây dựng.

Ví dụ, một hàm căn bậc hai thực tế có thể được kiểm tra kỹ lưỡng. Cho
nó một số bình phương hoàn hảo, một số bình phương không hoàn hảo, một
số phân số, v.v. Hoạt động hoàn hảo. Bạn sẽ không truyền số âm vào, đúng
không? Điều đó thật ngớ ngẩn. Nhưng bạn biết ai sẽ làm vậy không? Một
kẻ phản diện!

> **Tôi từng ghé thăm một cửa hàng trực tuyến cho phép bạn đặt số lượng
> âm.** Trang thanh toán nói họ sẽ ghi có vào tài khoản của tôi hàng
> chục nghìn đô la.
>
> Tuy nhiên tôi không bao giờ đủ can đảm để thanh toán, vì tôi không
> muốn chịu trách nhiệm vận chuyển tất cả sản phẩm đó cho họ.
>
> Hơn nữa, tôi không phải kẻ phản diện thực sự... tôi chỉ đang nghĩ
> như vậy thôi!

Hãy chuẩn bị cho những điều bất ngờ về dữ liệu mà code của bạn sẽ nhận.
Hãy chuẩn bị cho các tác nhân độc hại cung cấp dữ liệu nhằm cố gắng
truy cập trái phép hoặc thao túng hệ thống theo những cách không mong
muốn. Hãy kiểm tra những thứ đó trong code của bạn.

Điều này áp dụng cho tất cả các giai đoạn từ hiểu đến nhìn lại.

> **Một người quen của tôi ở đại học đã làm việc cho quân đội** xem xét
> kế hoạch cho những thứ như xe tăng chưa đi vào sản xuất. Công việc của
> anh ấy là suy nghĩ như kẻ phản diện và đặt câu hỏi như, "Làm thế nào
> bạn sẽ đưa cờ lê vào giữa những ống đó để vặn chặt bu lông đó?"

Suy nghĩ như kẻ phản diện không chỉ có thể phát hiện ra những vấn đề
bạn có thể không xem xét đến, mà còn dẫn bạn đến sự hiểu biết sâu sắc
hơn về dự án, tạo ra code bền vững và dễ bảo trì hơn.

[i[Villains]>]

## Áp dụng trong phỏng vấn

[i[Interviewing]<]

Quy trình bốn bước từ chương này chính xác là những gì bạn nên sử dụng
trong các thử thách code khi phỏng vấn.

Thấy đấy, những bài toán phỏng vấn này khá hiểm. Chúng hoàn toàn không
có câu trả lời rõ ràng.

Và tại sao lại như vậy? Có phải vì bạn chưa học đủ không? **Không.** Hoàn
toàn không phải vậy. Dù bạn học bao nhiêu, người phỏng vấn vẫn sẽ nghĩ
ra một câu hỏi không có câu trả lời rõ ràng với bạn, những kẻ tàn ác đó.

Và tại sao họ làm vậy? Họ muốn bạn thất bại? Không hề. *Họ muốn thấy
bạn áp dụng kỹ năng giải quyết vấn đề*.

> **Điều này không phải là phổ quát, nhân tiện.** Có hàng triệu phong
> cách phỏng vấn, và một số trong đó thực sự chỉ muốn xem bạn nhận được
> bao nhiêu câu trả lời đúng. Nhưng tôi sẽ lập luận rằng họ không phỏng
> vấn tối ưu. Và hơn nữa, tôi sẽ lập luận rằng cách duy nhất để có câu
> trả lời đúng là áp dụng các bước giải quyết vấn đề, vì vậy bạn cũng
> có thể làm như vậy trong mọi trường hợp.

Thật tự nhiên khi bạn đang căng thẳng trong buổi phỏng vấn và đối mặt
với một bài toán ban đầu có vẻ không thể, bạn đóng băng như con nai
trước đèn pha xe. Tất cả kiến thức của bạn đột nhiên biến mất trong đám
sương mù và bạn biết mình sẽ không bao giờ có được công việc này và—

***ĐỪNG HOẢNG LOẠN.*** Hãy tự nhắc mình những từ này: "Điều duy nhất
quan trọng bây giờ là *hiểu vấn đề*." Quên giải pháp đi. Điều đó không
quan trọng. Viết code? Không quan trọng. Chỉ cần tập trung vào bước một:
hiểu vấn đề.

Có hai lý do chính cho điều này. Một là người phỏng vấn hy vọng bạn sẽ
bắt đầu từ đó. (Và điều đó nên là lý do đủ.) Nhưng còn một lý do khác
là bằng cách bắt đầu với việc hiểu vấn đề, não bạn sẽ khởi động lại và
tự động bắt đầu nghĩ ra các chiến lược để giải quyết vấn đề... và đó là
bước hai của framework giải quyết vấn đề! Bạn đã đi đúng hướng rồi.

Hãy cố nghĩ (bạn, [i[Villains]] kẻ phản diện ơi) về bất cứ điều gì mơ
hồ trong mô tả vấn đề. Hãy hỏi câu hỏi để làm rõ những điều đó. Giới
hạn của đầu vào là gì? Giới hạn của đầu ra là gì? Bạn làm gì trong điều
kiện lỗi? Có thể gợi ý một ví dụ đầu vào và đầu ra và xác minh với người
phỏng vấn rằng bạn hiểu đúng.

Điều này cho người phỏng vấn thấy bạn chú ý đến chi tiết, một đặc điểm
quan trọng cần có. Và nó cũng cho họ thấy bạn bắt đầu dự án bằng cách
đưa ra những lựa chọn có cân nhắc, chủ ý.

Và nghe này: đối với nhiều người phỏng vấn, việc thấy bạn tiếp cận vấn
đề một cách có hệ thống thực sự quan trọng hơn việc bạn đưa ra câu trả
lời đúng. Và ở chiều ngược lại, không thể hiện kỹ năng giải quyết vấn
đề khi đưa ra câu trả lời có thể khiến bạn thất bại, dù câu trả lời có
đúng!

> **Khi tôi phỏng vấn tại Activision**, có hai câu hỏi tôi đã không
> trả lời đúng. Nhưng tôi đã cố gắng hết sức để giải quyết chúng thành
> tiếng, thể hiện cách tôi tiếp cận vấn đề. Tôi được nhận.
>
> (Những câu hỏi mà tôi đã hỏng là: "Cách nhanh nhất để đảo ngược các
> bit trong một byte là gì?" và "Tối ưu hóa phép tính này xây dựng lưới
> khoảng cách giữa tất cả các cầu thủ bóng đá trên sân.")

Vì vậy hãy đi qua toàn bộ quy trình với người phỏng vấn. Và đừng quên
bước phản ánh cuối cùng! Bạn sẽ làm gì tốt hơn? Giải pháp có thể được
cải thiện như thế nào? Những tính năng nào có thể được thêm vào trong
tương lai? Người phỏng vấn thích những thứ đó, và bạn thích làm người
phỏng vấn vui lòng, đúng không?

[i[Interviewing]>]

## Chi phí theo giai đoạn

[i[Problem solving-->Costs]<]

Một lưu ý liên quan đến framework giải quyết vấn đề là *chi phí thay đổi
phần mềm tăng theo cấp số nhân khi bạn càng tiến xa trong quá trình phát
triển*.

Khi bạn đang ở giai đoạn _Hiểu_, các thay đổi thực sự rẻ. Chúng miễn
phí. Bạn thậm chí chưa nghĩ ra kế hoạch, và bạn chỉ đang phác thảo
ý tưởng.

Khi đến giai đoạn _Kế hoạch_, các thay đổi vẫn khá rẻ. Không miễn phí
— nếu bạn cần thực hiện thay đổi, nó có thể ảnh hưởng đến các phần khác
của kế hoạch, và những phần đó sẽ cần được lập kế hoạch lại, hoặc có
thể cần hiểu thêm.

Tiếp theo, khi đến giai đoạn _Viết code_, bây giờ các thay đổi bắt đầu
gây đau. Có thể một thay đổi đòi hỏi phải bỏ đi và làm lại code trị giá
hàng nghìn hoặc hàng triệu đô la chi phí lập trình viên. Các công ty
thực hiện các thay đổi như thế này liên tục, dù vậy. Họ chỉ phân tích
chi phí-lợi ích và quyết định xem có đáng không.

Cuối cùng, sau khi code được triển khai, bây giờ các thay đổi *thực sự*
tốn kém. Không chỉ chúng ta phải lập kế hoạch lại, lập trình lại, xây
dựng lại, kiểm tra lại và triển khai lại một loạt code, mà còn khách hàng
ghét thực tế là chúng ta yêu cầu cập nhật, vì vậy chúng ta có tất cả các
loại chi phí phụ ẩn liên quan đến thay đổi.

Từ góc độ sinh viên, bạn không lo nhiều về số tiền dự án phần mềm của
bạn sẽ tốn cho công ty. Bạn lo lắng hơn rằng bạn sẽ có đủ thời gian
để hoàn thành nó (cùng với mọi thứ khác — giảng viên của bạn có biết
bạn có nhiều hơn một lớp học không?) với điểm số tử tế.

Vì vậy, những gì bạn cần làm là tập trung sự chú ý vào _Hiểu_ và _Kế
hoạch_ nơi các thay đổi rẻ *về mặt thời gian*. Điều này sẽ cho bạn kết
quả tốt nhất một cách nhanh chóng và hiệu quả (và hy vọng trước hạn
chót) với ít đau đớn lập trình nhất.

## Suy ngẫm về chương

* Bốn giai đoạn của giải quyết vấn đề là gì?

* Giai đoạn nào liên quan đến việc ngồi ở bàn phím viết code?

* Làm thế nào bạn có thể làm cho giai đoạn _Viết code_ khó hơn mức cần
  thiết?

* Hậu quả của một sai lầm không bị phát hiện trong giai đoạn _Hiểu_ là
  gì?

* Đối với mỗi giai đoạn, làm thế nào bạn biết khi nào mình đã hoàn
  thành nó?

* Điều gì xảy ra nếu bạn bỏ qua giai đoạn _Nhìn lại_?

* Beej có ý gì khi nói "suy nghĩ như kẻ phản diện"?

[i[Problem solving-->Costs]>]

[i[Problem solving]>]
