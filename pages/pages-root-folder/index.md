---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage
header:
  image_fullwidth: gudhi_banner_5.jpg
widget1:
  title: "Project"
  url: '/intro/'
  image: '/images/Stereographic_polytope_8cell_.png' # 302x183
  text: 'The GUDHI open source library provides the central data structures and algorithms that underly applications in geometry understanding in higher dimensions.'
widget2:
  title: "Download"
  url: 'https://gforge.inria.fr/frs/?group_id=3865'
  image: '/images/600-cell_graph_H4_302x182.png' # 302x183
  text: 'GUDHI is header-only. Download the source code and use it right away!'
widget3:
  title: "Documentation"
  url: 'http://gudhi.gforge.inria.fr/doc/latest/modules.html'
  image: '/images/Stereographic_polytope_24cell_.png' # 302x183
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
  url: http://lists.gforge.inria.fr/mailman/listinfo/gudhi-users
  text: Subscribe to the GUDHI users mailing-list ›
  style: alert
permalink: /index.html
---
