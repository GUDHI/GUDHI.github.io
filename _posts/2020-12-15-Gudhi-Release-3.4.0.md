---
layout: page
#
# Content
#
subheadline: "New release"
title: "GUDHI version 3.4.0"
teaser: "As a major new feature, the GUDHI library now offers dD weighted alpha complex, pip and conda packages for Python 3.9."
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
  url: https://github.com/GUDHI/gudhi-devel/releases/download/tags%2Fgudhi-release-3.4.0/gudhi.3.4.0.tar.gz
  text: Download GUDHI version 3.4.0
  style: alert
---
We are pleased to announce the release 3.4.0 of the GUDHI library.

As a major new feature, the GUDHI library now offers dD weighted alpha complex, pip and conda packages for Python 3.9.

We are now using GitHub to develop the GUDHI library, do not hesitate to [fork the GUDHI project on GitHub](https://github.com/GUDHI/gudhi-devel). From a user point of view, we recommend to download GUDHI user version (gudhi.3.4.0.tar.gz).

Below is a list of changes made since GUDHI 3.3.0:

- [Alpha complex](https://gudhi.inria.fr/doc/latest/group__alpha__complex.html)
     - the C++ weighted version for alpha complex is now available in any dimension D.

- Simplex tree [C++](https://gudhi.inria.fr/doc/latest/class_gudhi_1_1_simplex__tree.html) [Python](https://gudhi.inria.fr/python/latest/simplex_tree_ref.html)
     - A new method to reset the filtrations
     - A new method to get the boundaries of a simplex

- [Subsampling](https://gudhi.inria.fr/doc/latest/group__subsampling.html)
     - The C++ function `choose_n_farthest_points()` now takes a distance function instead of a kernel as first argument, users can replace `k` with `k.squared_distance_d_object()` in each call in their code.

- Miscellaneous
     - The [list of bugs that were solved since GUDHI-3.3.0](https://github.com/GUDHI/gudhi-devel/issues?q=label%3A3.4.0+is%3Aclosed) is available on GitHub.

All modules are distributed under the terms of the MIT license.
However, there are still GPL dependencies for many modules. We invite you to check our [license dedicated web page]({{ site.officialurl }}/licensing/) for further details.

We kindly ask users to cite the GUDHI library as appropriately as possible in their papers, and to mention the use of the GUDHI library on the web pages of their projects using GUDHI and provide us with links to these web pages.

We provide [bibtex entries]({{ site.officialurl }}/doc/latest/_citation.html) for the modules of the User and Reference Manual, as well as for publications directly related to the GUDHI library. 

Feel free to [contact us]({{ site.officialurl }}/contact/) in case you have any questions or remarks.

For further information about downloading and installing the library ([C++]({{ site.officialurl }}/doc/latest/installation.html) or [Python]({{ site.officialurl }}/python/latest/installation.html)), please visit the [GUDHI web site]({{ site.officialurl }}/).
