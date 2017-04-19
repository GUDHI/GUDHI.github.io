---
layout: page
#
# Content
#
subheadline: "New release"
title: "GUDHI version 2.0.0"
teaser: "As a major new feature, the GUDHI library now offers an interface with Python. All the new modules comes with their Python interface and a lot of examples, even in Python."
author: vrouvreau
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
  url: https://gforge.inria.fr/frs/download.php/file/36748/2017-04-19-22-24-25_GUDHI_2.0.0.tar.gz
  text: Download GUDHI version 2.0.0 ›
  style: alert
---


Below is a list of changes made since Gudhi 1.3.1:

- Bottleneck distance (new package)

     - Bottleneck distance measures the similarity between two persistence diagrams.

- cython (new package)

     - A Cython package allows to compile a Python interface with the GUDHI library.

- Spatial searching (new package)

     - Spatial searching is a wrapper around [CGAL dD spatial searching][5] algorithms that provides
     a simplified API to perform (approximate) neighbor searches..

- Subsampling (new package)

     - Subsampling offers methods to subsample a set of points.

- Tangential complex (new package)

     - A Tangential Delaunay complex is a non filtered simplicial complex designed to
     reconstruct a k-dimensional manifold embedded in d-dimensional Euclidean space.

- Witness complex (new relaxed version with a new interface)

     - Witness complex Wit(W,L) is a simplicial complex defined on two sets of
     points in Rd. The new relaxed version is filtrated. The new interface eases the
     simplicial complex construction.

- Alpha complex (new interface)

     - Alpha complex is a simplicial complex data structure constructed from the
     finite cells of a Delaunay Triangulation. The new interface eases the simplicial
     complex construction.

- Rips complex (new interface)

     - The Rips complex is a simplicial complex constructed from an expanded one-skeleton
     graph. The new interface eases the simplicial complex construction and allows the Rips
     complex to be build from a distance matrix.
     

All modules are distributed under the terms of the GPL Open Source license (GNU General Public License v3 or later versions).

We kindly ask users to cite the GUDHI library as appropriately as possible in their papers, and to mention the use of the GUDHI library on the web pages of
their projects using GUDHI and provide us with links to these web pages.

Feel free to [contact us][1] in case you have any question or remark on this topic.

We provide [bibtex entries][2] for the modules of the User and Reference Manual, as well as for publications directly related to the GUDHI library. 

For further information about [downloading][3] and installing the library ([C++][6] or [Python][7]), please visit the [GUDHI web site][4].


 [1]: {{ site.url }}/contact
 [2]: {{ site.url }}/doc/latest/_citation.html
 [3]: https://gforge.inria.fr/frs/?group_id=3865
 [4]: {{ site.url }}
 [5]: http://doc.cgal.org/latest/Spatial_searching/index.html
 [6]: {{ site.url }}/doc/latest/installation.html
 [7]: {{ site.url }}/python/latest/installation.html


