---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage
header:
  image_fullwidth: gudhi_banner.jpg
widget1:
  title: "Project"
  url: 'http://domain.de/must-be-absolut-url-like-this-one/'
  image: 'http://localhost:4000/images/simplicial_complex.png' # 302x183
  text: 'The GUDHI open source library provides the central data structures and algorithms that underly applications in geometry understanding in higher dimensions.'
widget2:
  title: "Download"
  url: 'http://domain.de/must-be-absolut-url-like-this-one/'
  image: 'http://localhost:4000/images/simplicial_complex.png' # 302x183
  text: 'GUDHI is header-only. Download the source code and use it right away!'
widget3:
  title: "Documentation"
  url: 'http://domain.de/must-be-absolut-url-like-this-one/'
  image: 'http://localhost:4000/images/simplicial_complex.png' # 302x183
  text: 'User & reference manuals of all the GUDHI modules.'
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
  url: https://tinyletter.com/feeling-responsive
  text: Inform me about new updates and features ›
  style: alert
permalink: /index.html
---
<div id="videoModal" class="reveal-modal large" data-reveal="">
  <div class="flex-video widescreen vimeo" style="display: block;">
    <iframe width="1280" height="720" src="https://www.youtube.com/embed/3b5zCFSmVvU" frameborder="0" allowfullscreen></iframe>
  </div>
  <a class="close-reveal-modal">&#215;</a>
</div>
