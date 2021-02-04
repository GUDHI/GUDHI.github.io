---
layout: page
title: "Dockerfile"
meta_title: "Dockerfile"
subheadline: ""
teaser: ""
permalink: "/dockerfile/"
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
  url: https://raw.githubusercontent.com/GUDHI/gudhi-deploy/main/Dockerfile_for_gudhi_installation
  text: Latest Dockerfile version
  style: alert

---

This container includes the installation of the C++ library if you want to build
your own C++ software on top of the GUDHI library.

It also includes all the [utilities][1].

Finally, this will also install the [GUDHI Python][2] package

If you do not want to build the container, it is available on
[GUDHI docker hub repository][3].

Please, find below an example of Dockerfile to install latest GUDHI version in a container.

 [1]: {{ site.url }}/utils/
 [2]: {{ site.officialurl }}/python/latest/
 [3]: https://hub.docker.com/r/gudhi/latest_gudhi_version
