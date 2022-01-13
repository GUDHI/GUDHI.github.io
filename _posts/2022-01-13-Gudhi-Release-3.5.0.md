---
layout: page
#
# Content
#
subheadline: "New release"
title: "GUDHI version 3.5.0"
teaser: "As a major new feature, the GUDHI library now offers Coxeter triangulations and points generators"
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
  url: https://github.com/GUDHI/gudhi-devel/releases/download/tags%2Fgudhi-release-3.5.0/gudhi.3.5.0.tar.gz
  text: Download GUDHI version 3.5.0
  style: alert
---
We are pleased to announce the release 3.5.0 of the GUDHI library.

As a major new feature, the GUDHI library now offers Coxeter triangulations and points generators.
The support for python 3.10 is available.

We are now using GitHub to develop the GUDHI library, do not hesitate to [fork the GUDHI project on GitHub](https://github.com/GUDHI/gudhi-devel). From a user point of view, we recommend to download GUDHI user version (gudhi.3.X.X.tar.gz).

Below is a list of changes made since GUDHI 3.4.1:

- [Coxeter triangulation]({{ site.officialurl }}/doc/latest/group__coxeter__triangulation.html)
     - constructs a piecewise-linear approximation of an m-dimensional smooth manifold embedded in R^d using an ambient triangulation. 

- [Datasets generators]({{ site.officialurl }}/python/latest/datasets_generators.html)
     - the python module `points` enables the generation of points on a sphere or a flat torus.

- Miscellaneous
     - The [list of bugs that were solved since GUDHI-3.4.1](https://github.com/GUDHI/gudhi-devel/issues?q=label%3A3.5.0+is%3Aclosed) is available on GitHub.

All modules are distributed under the terms of the MIT license.
However, there are still GPL dependencies for many modules. We invite you to check our [license dedicated web page]({{ site.officialurl }}/licensing/) for further details.

We kindly ask users to cite the GUDHI library as appropriately as possible in their papers, and to mention the use of the GUDHI library on the web pages of their projects using GUDHI and provide us with links to these web pages.

We provide [bibtex entries]({{ site.officialurl }}/doc/latest/_citation.html) for the modules of the User and Reference Manual, as well as for publications directly related to the GUDHI library. 

Feel free to [contact us]({{ site.officialurl }}/contact/) in case you have any questions or remarks.

For further information about downloading and installing the library ([C++]({{ site.officialurl }}/doc/latest/installation.html) or [Python]({{ site.officialurl }}/python/latest/installation.html)), please visit the [GUDHI web site]({{ site.officialurl }}/).
