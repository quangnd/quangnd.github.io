---
layout: page
published: true
title:  "Tại sao sử dụng Redux?"
teaser: "Bài viết này giới thiệu về những lý do bạn nên (ko nên) sử dụng Redux framework với React"
breadcrumb: true
tags:
    - react 
    - javascript
    - redux
categories:
    - programming
header: no
image:
    title: article-image-1.jpg
    caption: ...
    caption_url: https://unsplash.com/
---

Có vẻ như mọi người mới bắt đầu React đều hoang mang vãi chưởng tại sao dân tình cứ dùng Redux kèm theo để làm quái gì. Trước khi bắt đầu loạt giải thích theo hiểu biết cá nhân và những gì mình HỌC được, xin trích lời của Pete Hunt (https://github.com/petehunt/react-howto)

"If you aren't sure if you need it, you don't need it" 

Ok, Let's start! Lưu ý là mình chủ yếu đưa ra những gạch đầu dòng thôi nhé, còn với từng ý bạn không hiểu thì hãy ngồi xuống, kiếm 1 tách cafe và make friends with Google.

=== Trước tiên, bạn cần biết Redux là gì? 
Cơ bản là một state framework, còn chi tiết vui lòng xem document (http://redux.js.org/)

=== Thứ hai, why Redux:
1. One store, store là immutable (không thay đổi trạng thái, không chứa logic ứng dụng).
2. Giảm boilerplate (từ này ko biết dịch như nào, đại loại là giảm các thành phần code cần có để dùng framework, giảm so với gì? So với flux pattern mà FB đề nghị. Cái này lại phải tìm hiểu Flux là gì :D)
3. Thích hợp cho các ứng dụng isomorphic/universal (https://www.lullabot.com/.../what-is-an-isomorphic...)
4. Hot reloading (Giữ ứng dụng đang chạy và tự inject phiên bản mới của file khi bạn edit tại thời điểm runtime, với khả năng này ứng dụng của bạn sẽ ko bị mất trạng thái). (https://facebook.github.io/.../introducing-hot-reloading...)
5. Time travel debugging (hình dung ứng dụng bạn chạy từ bước A -> B -> C -> D, giả dụ bạn đang đứng ở D, bạn muốn quay lại B xem trạng thái của ứng dụng như nào để debug, Redux cho phép làm điều này dễ dàng. Cool, huh?)
6. Siêu bé với 1 framework (chỉ có dung lượng 2K sau khi đã minifined và gzipped)

===Thứ ba, bạn cần Redux khi: (hãy luôn xem Facebook hay Twitter là một ví dụ điển hình cho những ý bên dưới)
1. Ứng dụng của bạn có data flow phức tạp.
2. Các component trong ứng dụng không có quan hệ cha con mà có quan hệ qua lại với nhau. (inter-component)
3. Các dữ liệu không có tính phân cấp (non-heirachical)
4. Ứng dụng có nhiều actions.
5. Dữ liệu được sử dụng ở nhiều nơi.
...

Lời khuyên dành cho beginner:
1. Đọc kỹ hướng dẫn sử dụng trước khi dùng. Redux có một tài liệu được đầu tư kỹ và viết rất tốt. Tất cả những gì bạn cần làm khả năng đọc hiểu tiếng anh và 1 tinh thần ham học hỏi.
2. Nắm vững React cơ bản trước khi bắt đầu với 1 framework đi kèm (cụ thể là Redux, Flux, hay Mobx, hay Alt....)
3. Tìm các tutorial trên mạng, đọc cách họ làm, làm theo họ. Sau khi mọi thứ xong thì xoá đi làm lại bằng trí nhớ của bạn. Lưu ý là bắt đầu bằng những ví dụ đơn giản.
4. Kiểm soát tâm trí của bạn. Thậm chí 1 lập trình viên lâu năm cũng thấy khó hiểu và lạ lẫm với Redux khi tiếp xúc với nó. (What's the hell? Reducer là cái khỉ gì, Store là gì, Actions làm gì, dispatch, middleware, thunk or promise? ....). Nếu vấn đề quá phức tạp, chia nhỏ nó ra và tìm hiểu chứng năng từng thứ 1. Giống như bạn chơi lego vậy.
5. Lắng nghe lời khuyên của những người có kinh nghiệm và luôn giữ tinh thần học hỏi. Kiên trì và nhẫn nại!
6. Chọn 1 con đường và đi theo nó. Đừng đang học React lại nhảy sang Angular, Javascript lại nhảy sang PHP, cũng như đừng dùng Flux rồi lại nhảy sang Redux khi chưa có 1 hiểu biết cơ bản.
7. Dài quá nói không nổi nữa :D

Mình cũng là dev và cũng là người tự học, nếu như lời nói có gì ko phải hoặc múa rìu qua mắt thợ vui lòng anh em bỏ qua. hehe. Quan điểm của mình đơn giản là biết gì thì nói nấy. Hi vọng giúp được anh em.

^^