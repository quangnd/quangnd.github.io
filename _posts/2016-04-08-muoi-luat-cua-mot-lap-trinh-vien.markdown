---
layout: post
title: 10 luật để trở thành một lập trình viên tốt
date: "2016-04-08 01:47:54 +0700"
published: true
---


Bài viết này được lấy ý tưởng từ [một cuốn sách nổi tiếng][pragmatic-programmer]. Rất nổi tiếng ở thế hệ tôi, nhưng có thể bạn chưa từng nghe nói tới. Nó xứng đáng được đọc, đọc lại và nhắc lại.

Dưới đây là 10 luật thú vị rút ra từ cuốn sách, nếu một lập trình viên hiểu và thực hiện những điều này trong công việc hàng ngày, tôi khẳng định chẳng bao lâu anh ta sẽ trở thành một lập trình viên giỏi, viết code rõ ràng, đẹp và có tính tái sử dụng!

**Luật #1: Do not repeat yourself - Đừng lặp lại bản thân bạn**

[Nguyên tắc DRY][DRY] được phát biểu như sau:

> Every piece of knowledge must have a single, unambiguous, authoritative representation within a system.

This will increase your maintenance capabilities and lower bugs proliferation.

**Rule #2: Fix broken windows - Sửa những ô cửa vỡ**

Khái niệm "Những ô cửa sổ vỡ" được rút ra từ lĩnh vực tội phạm học:

> Hãy xem một tòa nhà với một vài cánh cửa sổ vỡ. Nếu những cánh cửa sổ không được sửa, xu hướng tất yếu là càng ngày càng có nhiều cửa sổ bị phá hoại hơn. Cuối cùng, một số người có thể đột nhập vào tòa nhà, nếu nó còn trống, tòa nhà sẽ trở thành một nơi bị xâm chiếm.

Trong việc phát triển phần mềm, những ô cửa vỡ là những thiết kệ ko tốt, những quyết định sai và cả những dòng code tệ hại. Nếu bạn không fix những lỗi này ngay khi nhận thấy chúng, bạn sẽ nhanh chóng rơi vào trạng thái gọi là [software rot][software-rot].

**Rule #3: Crash Early - Đổ vỡ sớm**

Luôn là tốt hơn khi để cho code đổ vỡ sớm. Sử dụng những giá trị trả về (mã lỗi) để notify cho một component đang được gọi về một lỗi là một ý tưởng tồi. Bởi vì, một component sẽ bỏ qua giá trị này, điều đó có nghĩa là lỗi có thể xảy ra và bị bỏ qua trong im lặng mà ko được xử lý. 

**Rule #4: Use tracer bullets**

Ý tưởng của luật này là triển khai ứng dụng của bạn lên môi trường production (môi trường chạy thật) sớm nhất có thể.

Chúng ta cũng nói chuyện về những đoạn code "phát sáng trong bóng tối". Khi bạn có một dự án mới, cố gắng thực hiện ở mức độ nhất định để có thể triển khai trên môi trường production. Làm nó đơn giản ở mức tối thiểu, đừng cố gắng hình dung mọi thứ trong giai đoạn đầu tiên. Mục tiêu trước nhất là có một gói phần mềm đơn giản, chắc chắn có thể hoạt động, trong môi trường prodction. Sau đó, bạn có thể cập nhật gói phần mềm này một cách thường xuyên.  

Tracer bullet là gói đầu tiên của bạn, bằng cách giảm bớt các chức năng, bạn sẽ tập trung vào vấn đề thực hiện tại môi trường thật/đóng gói/triển khai. Các đặc điểm và tính năng khác sẽ đến sau. Chiến lược này cũng có lợi trong việc giảm các rủi ro của vấn đề tối ưu hóa sớm (thường được gọi là [root of all evil][the-root-of-all-evil])

**Rule #5: Write Shy Code**

Shy code đước biết đến với thuật ngữ the [Law of Demeter][law-of-demeter]. Nó có thể được miêu tả như là một nguyên tắc của tri thức tối thiểu, Wikipedia giải thích như sau:

Hướng dẫn […] được tổng quát ngắn gọn theo những cách sau:

- Each unit should have only limited knowledge about other units: only units “closely” related to the current unit.
- Each unit should only talk to its friends; don’t talk to strangers.
- Only talk to your immediate friends.
 
Respecting the Law of Demeter when writing code enhance maintainability and reduce code duplication (so yes, that helps you repsect rule #1).

**Rule #6: Configure, don’t integrate - Cấu hình, không tích hợp**

Chi tiết sẽ làm lộn xộn code của bạn, chúng thay đổi thường xuyên (như các hằng số, chuỗi...). Mỗi thay đổi trong code tiềm ẩn nguy cơ phá vỡ hệ thống. Để loại trừ điều này, bạn nên đưa các chi tiết ra khỏi code, đặt chúng trong các file cấu hình. Code cấu hình còn được gọi là "soft code", nó  Every change to the code is a risk to break the system. To avoid that, you should get the details out of the code, in configuration files. Configurable code is called Â« soft code Â», nó thích nghi với sự thay đổi.

Bát cứ khi nào bạn phải sử dụng chi tiết trong code của mình, dừng lại và đặt chúng ra ngoài. Một chút thời gian lúc này sẽ đem lại thời gian hữu ích gấp 10 lần trong tương lai.

**Rule #7: Refactor Early, refactor often- Cải tiến code sớm, cải tiến thường xuyên**

Bạn nên cải tiến code, nhưng khi nào? Sau đây là một vài gợi ý: 

- Bạn tìm thấy một vài đoạn code trùng lặp có thể xóa (theo luật #1!)
- Bạn muốn dưa code chi tiết ra bên ngoài (luật #6)
- Bạn nhìn thấy cách thức để khái quát hóa (generalize) một vài thứ trong code.

Tuy nhiên, đừng refactor một cách mù quáng, bạn cần phải tỉnh táo và cẩn thận khi thực hiện những cải thiện, nếu sơ suất, việc này sẽ gây ra hậu quả trái ngược với mong muốn của bạn:

- Không nên thực hiện thêm chức năng và cải thiện cùng thời điểm.
- Chắc chắn rằng bạn phải test lại để tránh chức năng hoạt động ko như mong muốn.
- Thực hiện những phần nhỏ, có chủ ý. Một phần tại một thời điểm.

**Rule #8: Design to test - Thiết kế khả test**

Nếu bạn là một người ưa sự hoàn hảo, có lẽ bạn sẽ viết test trước khi code (phương hướng tiếp cận này còn được gọi là Test-Driven Development), nhưng điều này là không đơn giản. Điều quan trọng nhất tôi muốn đề cập là bạn cần phải luôn hướng code của mình tới mục tiêu là khả test - nói cách khác là viết code sao cho dễ test nhất. Dựa theo luật 5 - Law of Demeter sẽ giúp bạn luôn viết code có tính đóng gói tốt, từ đó dẫn tới việc test thuận lợi hơn.

Nếu một phần của code là khó (hoặc không thể) test, bạn cần cải thiện code (refactor) tới những thành phần nhỏ hơn.

**Rule #9: if you’ve found a bug, write a test - Nếu bạn tìm thấy một bug, viết test**

This is a very sane approach: whenever a bug is found in production, first thing to do is to write a test that reproduces the issue. That way you’ll be sure to understand the bug correctly before thinking at the fix and you’ll have a non-regression test that will make sure the bug won’t happen again.

**Rule #10: Know when to stop - Biết khi nào nên dừng lại**

Những lập trình viên giống những người hoạ sỹ, họ vẽ nên những bức tranh ở bên ngoài tâm trí của họ. Điểm cốt yếu ở dây là họ không biết khi nào, hay tại đâu họ nên dừng lại. Hãy nhớ là phần mềm hoàn hảo không tồn tại (Chính xác là bạn không thể viết được một phần mềm hoàn hảo, cho dù bạn có cố gắng thế nào chăng nữa)

Khi nào một bức tranh được hoàn thiện? Chỉ người hoạ sỹ có câu trả lời. Bạn là nghệ sĩ tạo nên những dòng code, và bạn biết khi nào nên dừng lại!


Source: http://blog.sukria.net/2012/01/06/the-10-rules-of-the-pragmatic-programmer/

[the-root-of-all-evil]: http://c2.com/cgi/wiki?PrematureOptimization
[law-of-demeter]: https://en.wikipedia.org/wiki/Law_of_Demeter
[refactor]: https://en.wikipedia.org/wiki/Code_refactoring
[generalization]: https://en.wikipedia.org/wiki/Generalization
[test-driven-development]: https://en.wikipedia.org/wiki/Test-driven_development
[software-rot]: https://en.wikipedia.org/wiki/Software_rot
[pragmatic-programmer]: https://pragprog.com/book/tpp/the-pragmatic-programmer
[DRY]: https://en.wikipedia.org/wiki/Don%27t_repeat_yourself
