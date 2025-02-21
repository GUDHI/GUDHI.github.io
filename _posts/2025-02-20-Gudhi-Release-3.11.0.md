---
layout: page
#
# Content
#
subheadline: "New release"
title: "GUDHI version 3.11.0"
teaser: "The GUDHI library now offers Delaunay, Delaunay-Čech and Alpha complex classes in Python with the ability to output the square, or not, filtration values and an interface to Ripser to enhance the Rips scikit-learn like interface."
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
  url: https://github.com/GUDHI/gudhi-devel/releases/download/tags%2Fgudhi-release-3.11.0/gudhi.3.11.0.tar.gz
  text: Download GUDHI version 3.11.0
  style: alert
---
We are pleased to announce the release 3.11.0 of the GUDHI library.

As a major new feature, the GUDHI library now offers Delaunay, Delaunay-Čech and Alpha complex classes in Python with
the ability to output the square, or not, filtration values and an interface to Ripser to enhance the Rips scikit-learn
like interface.

The GUDHI library is mainly developped using GitHub, do not hesitate to
[fork the GUDHI project on GitHub](https://github.com/GUDHI/gudhi-devel).
From a user point of view, we recommend to download GUDHI user version (gudhi.3.X.X.tar.gz).

Below is a list of changes:

- [Delaunay complex](https://gudhi.inria.fr/python/latest/delaunay_complex_user.html)
     - The Delaunay complex can be equipped with different filtrations:
          * Delaunay complex (no filtration values computed)
          * Delaunay-Čech complex (using minimal enclosing ball)
          * Alpha complex (moved in this new section)
     - The Delaunay-Čech and Alpha complex can output square, or not square, filtration values
     - An incremental version of the Delaunay complex (only in C++)

- [Rips complex persistence scikit-learn like interface](https://gudhi.inria.fr/python/latest/rips_complex_sklearn_itf_ref.html)
     - A binding to [Ripser](https://github.com/Ripser/ripser) when it accelerates the computation

- [Persistence graphical tools](https://gudhi.inria.fr/python/latest/persistence_graphical_tools_user.html)
     - Can now handle scikit-learn like interfaces outputs as inputs

- [Simplex tree](https://gudhi.inria.fr/doc/latest/class_gudhi_1_1_simplex__tree.html)
     - Can now store additionnal data on each simplex (only in C++)
     - Can be const

- Installation
     - CMake &ge; 3.15 is now required (was &ge; 3.8).
     - Python &ge; 3.8 is now required (was &ge; 3.5), because of `importlib.metadata`.
     - Support for Python 3.13 is now available

- Miscellaneous
     - The [list of bugs that were solved](https://github.com/GUDHI/gudhi-devel/issues?q=label%3A3.11.0+is%3Aclosed)
         is available on GitHub.

All modules are distributed under the terms of the MIT license.
However, there are still GPL dependencies for many modules. We invite you to check our [license dedicated web page]({{ site.officialurl }}/licensing/) for further details.

We kindly ask users to cite the GUDHI library as appropriately as possible in their papers, and to mention the use of the GUDHI library on the web pages of their projects using GUDHI and provide us with links to these web pages.

We provide [bibtex entries]({{ site.officialurl }}/doc/latest/_citation.html) for the modules of the User and Reference Manual, as well as for publications directly related to the GUDHI library.

Feel free to [contact us]({{ site.officialurl }}/contact/) in case you have any questions or remarks.

For further information about downloading and installing the library ([C++]({{ site.officialurl }}/doc/latest/installation.html) or [Python]({{ site.officialurl }}/python/latest/installation.html)), please visit the [GUDHI web site]({{ site.officialurl }}/).
