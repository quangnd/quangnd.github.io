---
layout: page
published: true
# subheadline: Đây là subheadline
title:  "React là gì và tại bao bạn nên học React ngay bây giờ"
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
    caption_url: https://unsplash.com/
---

Trong quá trình nghiên cứu và học hỏi các kỹ thuật lập trình với hệ sinh thái của Javascript và NodeJS, mình bắt gặp React - một công nghệ được phát triển và sử dụng bởi Facebook.

Suốt nhiều năm làm lập trình mình chưa thấy sự xuất hiện nào đẹp và tuyệt vời như React. Nó buộc chúng ta phải mở rộng tư duy về lập trình, thiết kế chương trình cũng như cách tiếp cận vấn đề.

Hãy xem thử một ví dụ về React 

[Mardown previewer](http://codepen.io/quangnd/full/vGOpQK/)

Hi vọng các bạn sẽ tìm được những điều lý thú và tìm được vài lý do để học React cho bản thân mình qua blog chia sẻ này.

# React là gì?

React là một thư viện Javascript giúp bạn xây dựng tầng Views (thường được xem như là chữ V trong mô hình MVC). React có thể xây dựng website hoàn toàn sử dụng Javascript (để thao tác với HTML), được tăng cường bởi VirtualDOM - thứ mà chúng ta sẽ tìm hiểu ngay sau đây.

React nhỏ, nhưng có võ, hơn nữa thư viện này còn được một trong những ứng dụng mạng xã hội phức tạp nhất hiện nay là Facebook sử dụng. Bạn có nghĩ nó đáng để tìm hiểu không?

Dưới đây là những yếu tố cơ bản của React

1. Reusable, composable, and stateful components

In React, we build views using smaller components. We can reuse a single component in multiple places, with different states and properties, and components can contain other components. Every component in a React application has a private state that may change over time, and React will take care of updating the component's view when its state changes.

2. The nature of reactive updates

React's name is the simple explanation for this concept. When the state of a component changes, those changes need to be reflected somewhere. For example, we need to regenerate the HTML views for the browser's Document Object Model (DOM) whenever their state changes. With React, we do not need to worry about how to reflect the state changes; React will simply react to the changes and automatically update the views when needed.

3.  The virtual representation of views in memory

With React, we write HTML using JavaScript. We rely on the power of JavaScript to generate HTML that depends on some data, rather than enhancing HTML to make it work with that data. Enhancing HTML is what other JavaScript frameworks usually do. For example, Angular extends HTML with features like loops, conditionals, and others.
If we are receiving just the data from the server (with AJAX), we need something more than HTML to work with it, so it's either using an enhanced HTML, or using the power of JavaScript itself to generate the HTML. Both approaches have advantages and disadvantages, and React embraces the latter one, with the argument that the advantages are stronger than the disadvantages.
Using JavaScript to render HTML allows React to have a virtual representation of HTML in memory (which is aptly named the virtual DOM), and React uses that to render the views virtually first. Every time a state changes and we have a new HTML tree that needs to be written back to the browser's DOM, instead of writing the whole tree, React will only write the difference between the new tree and the previous tree since it has both trees in memory. This process is known as tree reconciliation, and I think it’s the best thing that’s happened in web development since AJAX!

...coming soon...
![This is demo image]({{site.baseurl}}/images/homepage_typography.jpg)



[the-root-of-all-evil]: http://c2.com/cgi/wiki?PrematureOptimization
[law-of-demeter]: https://en.wikipedia.org/wiki/Law_of_Demeter
[refactor]: https://en.wikipedia.org/wiki/Code_refactoring
[generalization]: https://en.wikipedia.org/wiki/Generalization
[test-driven-development]: https://en.wikipedia.org/wiki/Test-driven_development
[software-rot]: https://en.wikipedia.org/wiki/Software_rot
[pragmatic-programmer]: https://pragprog.com/book/tpp/the-pragmatic-programmer
[DRY]: https://en.wikipedia.org/wiki/Don%27t_repeat_yourself