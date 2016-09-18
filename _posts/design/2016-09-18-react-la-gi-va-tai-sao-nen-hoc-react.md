---
layout: page
published: true
# subheadline: Đây là subheadline
title:  "React là gì?"
teaser: "Sơ lược về ReactJS"
breadcrumb: true
tags:
    - react 
    - javascript
categories:
    - programming
header: no
image:
    title: article-image-1.jpg
    caption: ...
    caption_url: https://unsplash.com/
---

Trong quá trình nghiên cứu và học hỏi các kỹ thuật lập trình với hệ sinh thái của Javascript và NodeJS, mình bắt gặp React - một công nghệ được phát triển và sử dụng bởi Facebook.

Suốt nhiều năm làm lập trình mình chưa thấy sự xuất hiện nào đẹp và tuyệt vời như React. Nó buộc chúng ta phải mở rộng tư duy về lập trình, thiết kế chương trình cũng như cách tiếp cận vấn đề. Và như lời giới thiệu của Facebook, React sinh ra là để giải quyết những bài toán lớn và phức tạp.

Hãy xem thử một ví dụ về React mình đã viết. KHi bạn nhập nội dung tại khung bên trái, ngay lập tức nội dung này được render dựa trên [Markdown] tại khung thứ hai

[Mardown previewer](http://codepen.io/quangnd/full/vGOpQK/)

Hi vọng các bạn sẽ tìm được những điều lý thú và tìm được vài lý do để học React cho bản thân mình qua blog chia sẻ này.

# React là gì?

React là một thư viện Javascript giúp bạn xây dựng tầng Views (thường được xem như là chữ V trong mô hình MVC). React có thể xây dựng website hoàn toàn sử dụng Javascript (để thao tác với HTML), được tăng cường bởi VirtualDOM - thứ mà chúng ta sẽ tìm hiểu sau trong bài viết.

React nhỏ, nhưng có võ, hơn nữa thư viện này còn được một trong những ứng dụng mạng xã hội phức tạp nhất hiện nay là Facebook sử dụng. Bạn có nghĩ nó đáng để tìm hiểu không?

Dưới đây là những yếu tố cơ bản của React

### 1. Các component lưu trạng thái, có thể tái sử dụng

Trong React, chúng ta xây dựng trang web sử dụng những thành phần (component) nhỏ. Chúng ta có thể tái sử dụng một component ở nhiều nơi, với các trạng thái hoặc các thuộc tính khác nhau, trong một component lại có thể chứa thành phần khác. Mỗi component trong React có một trạng thái riêng, có thể thay đổi, và React sẽ thực hiện cập nhật component dựa trên những thay đổi của trạng thái.

Một đoạn code tạo ra component CommentBox 

{% highlight javascript %}
var CommentBox = React.createClass({
  render: function() {
    return (
      <div className="commentBox">
        Hello, world! I am a CommentBox.
      </div>
    );
  }
});
{% endhighlight %}

### 2. Phản ứng (React) khi có thay đổi

Khi trạng thái của một component thay đổi, những thay đổi này cần được thực hiện theo cách thức nào đó. Trong mô hình web truyền thống với DOM, chúng ta cần tạo lại mã HTML để thể hiện các đối tượng mới trên trang web, nói cách khác chúng ta cần tạo ra view mới khi trạng thái của component thay đổi. Với React, chúng ta không cần lo lắng về cách thức tạo ra view mới, React sẽ kiểm soát những thay đổi này và tự động update views khi cần thiết.

[Todo MVC Example]

Bạn có thể thấy cách view thay đổi trong ví dụ todomvc ở đường link trên, khi người dùng chọn complete một nhiệm vụ, view đã được lập tức thay đổi.

### 3. DOM ảo (VirtualDOM)

Với React, chúng ta viết HTML sử dụng JavaScript. Chúng ta mượn khả năng linh hoạt của Javascript để tạo ra mã HTML phụ thuộc trên dữ liệu, đây là cách tiếp cận khác với kiểu mở rộng HTML (Enhancing HTML). Phương thức mở rộng HTML được một vài framework sử dụng, điển hình là Angular. Angular đã mở rộng HTML với các đặc điểm như vòng lặp, các câu lệnh điều kiện và một vài tiện ích khác.

Hãy nghĩ về việc bạn lấy dữ liệu từ server với AJAX, để xử lý dữ liệu này chúng ta không chỉ cần HTML mà còn cần một phương thức tốt hơn để thao tác với dữ liệu. Nếu bạn đã làm Angular hay ASP.NET MVC, bạn sẽ không xa lạ gì với đặc điểm mở rộng HTML như ngRepeat. React có một cách tiếp cận khác với thứ gọi là VirtualDOM. Việc sử dụng Javascript để tạo ra mã HTML cho phép React có một cây đối tượng HTML ảo - VirtualDOM. Khi bạn load trang web sử dụng React, một VirtualDOM được tạo ra và lưu trong bộ nhớ. Mỗi khi có một trạng thái thay đổi, chúng ta sẽ có một cây đối tượng HTML mới và cần được tạo lại để hiển thị lên trình duyệt. Thay vì tạo lại toàn bộ cây, React dùng một thuật toán thông minh để tạo lại chỉ các thành phần khác biệt giữa cây mới và cây cũ. Và bởi vì cả hai cây cũ và mới đều được lưu trong bộ nhớ, xử lý này diễn ra siêu nhanh. 

Qui trình xử lý này được gọi với thuật ngữ **tree reconciliation**, và rất nhiều lập trình viên bày tỏ rằng đây là một trong những phát kiến tuyệt vời nhất trong lĩnh vực phát triển web kể từ ngày AJAX ra đời.

Các tài nguyên tham khảo

- [React offical page]
- ReactJS succinctly book

*Mình đang viết tiếp phần 2: Tại sao sử dụng React? Mời bạn nào quan tâm đón xem.*

[Markdown]: http://commonmark.org/help/
[React offical page]: https://facebook.github.io
[Todo MVC Example]: http://todomvc.com/examples/react/#/
