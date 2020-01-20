---
layout: page
#
# Content
#
subheadline: "New release"
title: "GUDHI version 3.1.0"
teaser: "As a major new feature, the GUDHI library now offers 2 new Python modules: Persistence representations and Wasserstein distance."
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
  url: https://github.com/GUDHI/gudhi-devel/releases/download/tags%2Fgudhi-release-3.1.0/gudhi.3.1.0.tar.gz
  text: Download GUDHI version 3.1.0
  style: alert
---

We are now using GitHub to develop the GUDHI library, do not hesitate to [fork the GUDHI project on GitHub](https://github.com/GUDHI/gudhi-devel). From a user point of view, we recommend to download GUDHI user version (gudhi.3.1.0.tar.gz).

Below is a list of changes made since Gudhi 3.0.0:

- [Persistence representations]({{ site.officialurl }}/python/latest/representations.html) (new Python module)
     - Vectorizations, distances and kernels that work on persistence diagrams, compatible with scikit-learn. This module was originally available at https://github.com/MathieuCarriere/sklearn-tda and named sklearn_tda.

- [Wasserstein distance]({{ site.officialurl }}/python/latest/wasserstein_distance_user.html) (new Python module)
     - The q-Wasserstein distance measures the similarity between two persistence diagrams.

- [Alpha complex]({{ site.officialurl }}/doc/latest/group__alpha__complex.html) (new C++ interface)
     - Thanks to [CGAL 5.0 Epeck_d](https://doc.cgal.org/latest/Kernel_d/structCGAL_1_1Epeck__d.html) kernel, an exact computation version of Alpha complex dD is available and the default one (even in Python).

- [Persistence graphical tools]({{ site.officialurl }}/python/latest/persistence_graphical_tools_user.html) (new Python interface)
     - Axes as a parameter allows the user to subplot graphics.
     - Use matplotlib default palette (can be user defined).

- Miscellaneous
     - Python `read_off` function has been renamed `read_points_from_off_file` as it only reads points from OFF files.
     - See the list of [bug fixes](https://github.com/GUDHI/gudhi-devel/issues?utf8=%E2%9C%93&q=is%3Aissue+label%3A3.1.0+).


All modules are distributed under the terms of the MIT license.
However, there are still GPL dependencies for many modules. We invite you to check our [license dedicated web page]({{ site.officialurl }}/licensing/) for further details.

We kindly ask users to cite the GUDHI library as appropriately as possible in their papers, and to mention the use of the GUDHI library on the web pages of their projects using GUDHI and provide us with links to these web pages.

We provide [bibtex entries]({{ site.officialurl }}/doc/latest/_citation.html) for the modules of the User and Reference Manual, as well as for publications directly related to the GUDHI library. 

Feel free to [contact us]({{ site.officialurl }}/contact/) in case you have any questions or remarks.

For further information about downloading and installing the library ([C++]({{ site.officialurl }}/doc/latest/installation.html) or [Python]({{ site.officialurl }}/python/latest/installation.html)), please visit the [GUDHI web site]({{ site.officialurl }}).

