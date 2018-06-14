---
layout: page
#
# Content
#
subheadline: "New release"
title: "GUDHI version 2.2.0"
teaser: "As a major new feature, the GUDHI library now offers a Čech complex module, a sparse version of the Rips complex and
a utility to build the Rips complex from a correlation matrix (no Python interface yet)."
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
  url: https://gforge.inria.fr/frs/download.php/file/37564/2018-06-13-10-51-40_GUDHI_2.2.0.tar.gz
  text: Download GUDHI version 2.2.0
  style: alert
---


Below is a list of changes made since Gudhi 2.1.0:

- [Čech complex][8] (new package)
     - The Čech complex is a simplicial complex where the set of all simplices is filtered by the radius of their minimal enclosing ball.

- [Rips complex][9] (new functions and interfaces)
     - A sparse version of the Rips complex
     - Rips complex from a correlation matrix utility

- [Dockerfile][10] (new installation process)
     A Dockerfile example is now provided to compile, test and install GUDHI in a container

- CGAL 4.12 compilation issue (bug fix)

- CMake minimal version is now 3.1
     - To take advantage of the latest features and simplify CMakeLists.txt files


All modules are distributed under the terms of the GPL Open Source license (GNU General Public License v3 or later versions), but a commercial license is also possible.

We kindly ask users to cite the GUDHI library as appropriately as possible in their papers, and to mention the use of the GUDHI library on the web pages of
their projects using GUDHI and provide us with links to these web pages.

Feel free to [contact us][1] in case you have any question or remark on this topic.

We provide [bibtex entries][2] for the modules of the User and Reference Manual, as well as for publications directly related to the GUDHI library. 

For further information about [downloading][3] and installing the library ([C++][6] or [Python][7]), please visit the [GUDHI web site][4].


 [1]: {{ site.url }}/contact
 [2]: {{ site.url }}/doc/latest/_citation.html
 [3]: https://gforge.inria.fr/frs/?group_id=3865
 [4]: {{ site.url }}/
 [5]: http://doc.cgal.org/latest/Spatial_searching/index.html
 [6]: {{ site.url }}/doc/latest/installation.html
 [7]: {{ site.url }}/python/latest/installation.html
 [8]: {{ site.url }}/doc/latest/group__cech__complex.html
 [9]: {{ site.url }}/doc/latest/group__rips__complex.html
 [10]: {{ site.url }}/dockerfile/


