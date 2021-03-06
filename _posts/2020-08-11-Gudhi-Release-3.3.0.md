---
layout: page
#
# Content
#
subheadline: "New release"
title: "GUDHI version 3.3.0"
teaser: "As a major new feature, the GUDHI library now offers a persistence-based clustering algorithm, weighted Rips complex using DTM
and edge collapse."
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
  url: https://github.com/GUDHI/gudhi-devel/releases/download/tags%2Fgudhi-release-3.3.0/gudhi.3.3.0.tar.gz
  text: Download GUDHI version 3.3.0
  style: alert
---
We are pleased to announce the release 3.3.0 of the GUDHI library.

The GUDHI library is hosted on GitHub, do not hesitate to [fork the GUDHI project on GitHub](https://github.com/GUDHI/gudhi-devel).
From a user point of view, we recommend to download GUDHI user version (gudhi.3.3.0.tar.gz).

Below is a list of changes made since GUDHI 3.2.0:

- [DTM density estimator]({{ site.officialurl }}/python/latest/point_cloud.html#module-gudhi.point_cloud.dtm)
     - Python implementation of a density estimator based on the distance to the empirical measure defined by a point set.

- [DTM Rips complex]({{ site.officialurl }}/python/latest/rips_complex_user.html#dtm-rips-complex)
     - This Python implementation constructs a weighted Rips complex giving larger weights to outliers, which reduces their impact on the persistence diagram

- [Alpha complex]({{ site.officialurl }}/python/latest/alpha_complex_user.html) - Python interface improvements
     - 'fast' and 'exact' computations
     - Delaunay complex construction by not setting filtration values
     - Use the specific 3d alpha complex automatically to make the computations faster

- [Clustering]({{ site.officialurl }}/python/latest/clustering.html)
     - Python implementation of [ToMATo](https://doi.org/10.1145/2535927), a persistence-based clustering algorithm

- [Edge Collapse]({{ site.officialurl }}/doc/latest/group__edge__collapse.html) of a filtered flag complex
     - This C++ implementation reduces a filtration of Vietoris-Rips complex from its graph to another smaller flag filtration with the same persistence.

- [Bottleneck distance]({{ site.officialurl }}/python/latest/bottleneck_distance_user.html)
     - Python interface to [hera](https://github.com/grey-narn/hera)'s bottleneck distance

- Persistence representations
     - [Atol]({{ site.officialurl }}/python/latest/representations.html#gudhi.representations.vector_methods.Atol) is integrated in finite vectorisation methods. This [article](https://www.fujitsu.com/global/about/resources/news/press-releases/2020/0316-01.html) talks about applications using Atol. This module was originally available at [https://github.com/martinroyer/atol](https://github.com/martinroyer/atol)
     - Python interface change: [Wasserstein metrics]({{ site.officialurl }}/python/latest/representations.html#gudhi.representations.metrics.WassersteinDistance) is now [hera](https://github.com/grey-narn/hera) by default

- Miscellaneous
     - The [list of bugs that were solved since GUDHI-3.2.0](https://github.com/GUDHI/gudhi-devel/issues?q=label%3A3.3.0+is%3Aclosed) is available on GitHub.

All modules are distributed under the terms of the MIT license.
However, there are still GPL dependencies for many modules. We invite you to check our [license dedicated web page]({{ site.officialurl }}/licensing/) for further details.

We kindly ask users to cite the GUDHI library as appropriately as possible in their papers, and to mention the use of the GUDHI library on the web pages of their projects using GUDHI and provide us with links to these web pages.

We provide [bibtex entries]({{ site.officialurl }}/doc/latest/_citation.html) for the modules of the User and Reference Manual, as well as for publications directly related to the GUDHI library. 

Feel free to [contact us]({{ site.officialurl }}/contact/) in case you have any questions or remarks.

For further information about downloading and installing the library ([C++]({{ site.officialurl }}/doc/latest/installation.html) or [Python]({{ site.officialurl }}/python/latest/installation.html)), please visit the [GUDHI web site]({{ site.officialurl }}/).
