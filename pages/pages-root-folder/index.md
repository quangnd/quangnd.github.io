---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage
header:
  image_fullwidth: header_frontpage1.jpg
widget1:
  title: "Blog của người tự học"
  url: 'http://quangnd.com/blog/'
  image: widget1.png
  text: 'Tôi đã dành bảy năm để lập trình. Tôi yêu lập trình. Bạn có thể tìm thấy nhiều những dự án, ứng dụng nhỏ trên website. Hoặc nếu muốn, hãy dành chút thời gian đọc CV của tôi.'
widget2:
  title: "Có gì tại blog này?"
  url: 'http://quangnd.com/info/'
  image: widget2.png
  text: '<em>Rất nhiều thứ hay ho.</em><br/>1. Bài viết hướng dẫn học lập trình :)<br/>2. Phương pháp học tập, làm việc hiệu quả<br/>4. Giới thiệu và đánh giá sách.<br/>5. Thảo luận & sẻ chia.'
  
widget3:
  title: "Tài nguyên đã lựa chọn"
  url: 'https://github.com/quangnd/'
  image: humans.png
  text: '<em>Rất nhiều công cụ hỗ trợ lập trình.</em><br/>1. <a href="http://regexone.com" target="_blank">Học regular expression.</a><br/>2. <a href="http://commonmark.org/help/" target="_blank">Học viết với markdown.</a><br/>3. <a href="http://codewars.com/r/YCdOTA" target="_blank">Lập trình cơ bản.</a><br/>4. <a href="http://freecodecamp.com" target="_blank">Fullstack Dev với FreeCodeCamp.</a><br/>'

# Note By Mun
# ===========
# Adding video use code
# video: '<a href="#" data-reveal-id="videoModal"><img src="http://phlow.github.io/feeling-responsive/images/start-video-feeling-responsive-302x182.jpg" width="302" height="182" alt=""/></a>'
# within widget

#<div id="videoModal" class="reveal-modal large" data-reveal="">
#  <div class="flex-video widescreen vimeo" style="display: block;">
#    <iframe width="1280" height="720" src="https://www.youtube.com/embed/3b5zCFSmVvU" frameborder="0" allowfullscreen></iframe>
#  </div>
# <a class="close-reveal-modal">&#215;</a>
#</div>


#
# Use the call for action to show a button on the frontpage
#
# To make internal links, just use a permalink like this
# url: /getting-started/
#
# To style the button in different colors, use no value
# to use the main color or success, alert or secondary.
# To change colors see sass/_01_settings_colors.scss
#
callforaction:
  url: https://tinyletter.com/quangnd
  text: Đăng ký nhận các bài viết cập nhật hàng tuần ›
  style: alert
permalink: /index.html
#
# This is a nasty hack to make the navigation highlight
# this page as active in the topbar navigation
#
homepage: true
---


