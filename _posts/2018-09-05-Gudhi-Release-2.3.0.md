---
layout: page
#
# Content
#
subheadline: "New release"
title: "GUDHI version 2.3.0"
teaser: "As a major new feature, the GUDHI library now offers a Python interface
to the Nerve and Graph Induced Complex. The GUDHI conda package is now available through conda-forge channel."
author: GUDHI Editorial Board
categories:
  - Release
tags:
  - GUDHI release
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
  url: https://gforge.inria.fr/frs/download.php/file/37696/2018-09-04-14-25-00_GUDHI_2.3.0.tar.gz
  text: Download GUDHI version 2.3.0
  style: alert
---


Below is a list of changes made since Gudhi 2.2.0:
- [Nerve and Graph Induced Complex][7] (new Python interface)
     - Cover complexes, that provably contain topological information about the input data.

- Compilation issue (bug fix)
     - CMake warning with ninja generator.
     - thread_local management on old XCode versions.
     - Boost dependency for Windows Python module.

- [GUDHI conda package][8]
     - The GUDHI conda package is now available through conda-forge channel.

All modules are distributed under the terms of the GPL Open Source license (GNU General Public License v3 or later versions), but a commercial license is also possible.

We kindly ask users to cite the GUDHI library as appropriately as possible in their papers, and to mention the use of the GUDHI library on the web pages of
their projects using GUDHI and provide us with links to these web pages.

Feel free to [contact us][1] in case you have any question or remark on this topic.

We provide [bibtex entries][2] for the modules of the User and Reference Manual, as well as for publications directly related to the GUDHI library. 

For further information about [downloading][3] and installing the library ([C++][5] or [Python][6]), please visit the [GUDHI web site][4].


 [1]: {{ site.url }}/contact
 [2]: {{ site.officialurl }}/doc/latest/_citation.html
 [3]: https://gforge.inria.fr/frs/?group_id=3865
 [4]: {{ site.url }}/
 [5]: {{ site.officialurl }}/doc/latest/installation.html
 [6]: {{ site.officialurl }}/python/latest/installation.html
 [7]: {{ site.officialurl }}/python/latest/nerve_gic_complex_user.html
 [8]: {{ site.url }}/conda/


