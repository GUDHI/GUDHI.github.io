---
layout: page
#
# Content
#
subheadline: "New release"
title: "GUDHI version 3.0.0"
teaser: "As a major new feature, the GUDHI library is now released under a MIT license."
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
  url: https://github.com/GUDHI/gudhi-devel/releases/download/tags%2Fgudhi-release-3.0.0.rc2/2019-09-11-07-52-20_GUDHI_3.0.0.rc2.tar.gz
  text: Download GUDHI version 3.0.0
  style: alert
---

We invite you to check our [license dedicated web page]({{ site.url }}/licensing)
for further details about this change.

We are now using GitHub to develop the GUDHI library, do not hesitate to
[fork the GUDHI project on GitHub](https://github.com/GUDHI/gudhi-devel).
From a user point of view, we recommend to
[download GUDHI user version](https://github.com/GUDHI/gudhi-devel/releases/download/tags%2Fgudhi-release-3.0.0.rc2/2019-09-11-07-52-20_GUDHI_3.0.0.rc2.tar.gz).

Below is a list of changes made since Gudhi 2.3.0:

- [Persistence graphical tools]({{ site.officialurl }}/python/latest/persistence_graphical_tools_user.html) (new functionnality)
     - Add a persistence density graphical tool

- [Rips complex]({{ site.officialurl }}/python/latest/rips_complex_user.html) (new Python interface)
     - Sparse Rips complex is now available in Python.

- [Alpha complex]({{ site.officialurl }}/doc/latest/group__alpha__complex.html) (new C++ interface)
     - Dedicated Alpha complex for 3d cases. Alpha complex 3d can be standard, weighted, periodic or weighted and periodic.

- Third parties (new dependencies)
     - C++14 is the new standard (instead of C++11 on former versions of GUDHI)
     - boost >= 1.56 is now required (instead of 1.48 on former versions of GUDHI)
     - CGAL >= 4.11 is now required (instead of various requirements on former versions of GUDHI)
     - Eigen >= 3.1.0 is now required (version was not checked)

All modules are distributed under the terms of the MIT license.

We kindly ask users to cite the GUDHI library as appropriately as possible in their papers, and to mention the use of the GUDHI library on the web pages of
their projects using GUDHI and provide us with links to these web pages.

Feel free to [contact us]({{ site.officialurl }}/contact/) in case you have any questions or remarks.

We provide [bibtex entries]({{ site.officialurl }}/doc/latest/_citation.html) for the modules of the User and Reference Manual,
as well as for publications directly related to the GUDHI library. 

For further information about downloading and installing the library ([C++]({{ site.officialurl }}/doc/latest/installation.html)
or [Python]({{ site.officialurl }}/python/latest/installation.html)), please visit the [GUDHI web site]({{ site.officialurl }}).


