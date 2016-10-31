---
layout: page
published: true
title:  "Làm thế nào để cài đặt redux devtools?"
teaser: "Redux devtool là một công cụ rất mạnh và cần phải có với mỗi Redux-react dev. Bài viết sau hướng dẫn cách thức cài đặt đơn giản cho ứng dụng của bạn."
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

## Cài đặt

Chạy lệnh `npm install --save-dev redux-devtools`

## Cấu hình

Nếu bạn có một basic [store](http://redux.js.org/docs/api/createStore.html) được mô tả trong [document chính thức của redux](http://redux.js.org/index.html), bạn chỉ cần thay:

`const store = createStore(reducer);`

với đoạn code sau

`const store = createStore(reducer, window.__REDUX_DEVTOOLS_EXTENSION__ && window.__REDUX_DEVTOOLS_EXTENSION__());`

Lưu ý: nếu bạn dùng eslint và eslint được cấu hình với rule *no-underscore-dangle* bạn cần wrap đoạn code như sau

`
/* eslint-disable no-underscore-dangle */
  const store = createStore(reducer, preloadedState, 
    window.__REDUX_DEVTOOLS_EXTENSION__ && window.__REDUX_DEVTOOLS_EXTENSION__()
  );
  /* eslint-enable */
`

Nếu bạn cần cấu hình ở những trường hợp phức tạp hơn, tham khảo tại:

[https://github.com/zalmoxisus/redux-devtools-extension#usage](https://github.com/zalmoxisus/redux-devtools-extension#usage)

## Sử dụng

1. Chạy ứng dụng của bạn
2. Bật Chrome Develop ToolsTools
3. Chọn Redux tab
4. Enjoy it!

