---
layout: page
#
# Content
#
subheadline: "New release"
title: "GUDHI version 3.2.0"
teaser: "As a major new feature, the GUDHI library now offers Weighted Rips Complex, extended persistence and point cloud utilities new modules."
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
  url: https://github.com/GUDHI/gudhi-devel/releases/download/tags%2Fgudhi-release-3.2.0/gudhi.3.2.0.tar.gz
  text: Download GUDHI version 3.2.0
  style: alert
---

We are now using GitHub to develop the GUDHI library, do not hesitate to [fork the GUDHI project on GitHub](https://github.com/GUDHI/gudhi-devel). From a user point of view, we recommend to download GUDHI user version (gudhi.3.2.0.tar.gz).

Below is a list of changes made since Gudhi 3.1.1:

- Point cloud utilities
     - A new module [Time Delay Embedding]({{ site.officialurl }}/python/latest/point_cloud.html#time-delay-embedding) to embed time-series data in the R^d according to [Takens' Embedding Theorem](https://en.wikipedia.org/wiki/Takens%27s_theorem) and obtain the coordinates of each point.
     - A new module [K Nearest Neighbors]({{ site.officialurl }}/python/latest/point_cloud.html#k-nearest-neighbors) that wraps several implementations for computing the k nearest neighbors in a point set.
     - A new module [Distance To Measure]({{ site.officialurl }}/python/latest/point_cloud.html#distance-to-measure) to compute the distance to the empirical measure defined by a point set

- [Persistence representations]({{ site.officialurl }}/python/latest/representations.html)
     - Interface to Wasserstein distances.

- Rips complex
     - A new module [Weighted Rips Complex]({{ site.officialurl }}/python/latest/rips_complex_user.html#weighted-rips-complex) to construct a simplicial complex from a distance matrix and weights on vertices.

- [Wassertein distance]({{ site.officialurl }}/python/latest/wasserstein_distance_user.html)
     - An [another implementation]({{ site.officialurl }}/python/latest/wasserstein_distance_user.html#hera) comes from Hera (BSD-3-Clause) which is based on [Geometry Helps to Compare Persistence Diagrams](http://doi.acm.org/10.1145/3064175) by Michael Kerber, Dmitriy Morozov, and Arnur Nigmetov.
     - `gudhi.wasserstein.wasserstein_distance` has now an option to return the optimal matching that achieves the distance between the two diagrams.
     - A new module [Barycenters]({{ site.officialurl }}/python/latest/wasserstein_distance_user.html#barycenters) to estimate the Frechet mean (aka Wasserstein barycenter) between persistence diagrams.

- [Simplex tree]({{ site.officialurl }}/python/latest/simplex_tree_ref.html)
     - Extend filtration method to compute extended persistence
     - Flag and lower star persistence pairs generators
     - A new interface to filtration, simplices and skeleton getters to return an iterator

- [Alpha complex]({{ site.officialurl }}/doc/latest/group__alpha__complex.html)
     - Improve computations (cache circumcenters computation and point comparison improvement)

- [Persistence graphical tools]({{ site.officialurl }}/python/latest/persistence_graphical_tools_user.html)
     - New rendering option proposed (use LaTeX style, add grey block, improved positioning of labels, etc.). 
     - Can now handle (N x 2) numpy arrays as input 

- Miscellaneous
     - The [list of bugs that were solved since GUDHI-3.2.0](https://github.com/GUDHI/gudhi-devel/issues?q=label%3A3.2.0+is%3Aclosed) is available on GitHub.

All modules are distributed under the terms of the MIT license.
However, there are still GPL dependencies for many modules. We invite you to check our [license dedicated web page]({{ site.officialurl }}/licensing/) for further details.

We kindly ask users to cite the GUDHI library as appropriately as possible in their papers, and to mention the use of the GUDHI library on the web pages of their projects using GUDHI and provide us with links to these web pages.

We provide [bibtex entries]({{ site.officialurl }}/doc/latest/_citation.html) for the modules of the User and Reference Manual, as well as for publications directly related to the GUDHI library. 

Feel free to [contact us]({{ site.officialurl }}/contact/) in case you have any questions or remarks.

For further information about downloading and installing the library ([C++]({{ site.officialurl }}/doc/latest/installation.html) or [Python]({{ site.officialurl }}/python/latest/installation.html)), please visit the [GUDHI web site]({{ site.officialurl }}).

