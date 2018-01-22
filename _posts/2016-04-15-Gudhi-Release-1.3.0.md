---
layout: page
#
# Content
#
subheadline: "New release"
title: "GUDHI version 1.3.0"
teaser: "We are pleased to announce the release 1.3.0 of the GUDHI library."
author: vrouvreau
categories:
  - Release
tags:
  - GUDHI release
---




Below is a list of changes made since Gudhi 1.2.0:

- GudhUI (new package)
This package provides a User Interface to have a quick overview of GUDHI features.
GudhUI allows to load OFF points or meshes files that can be visualized on a 3D viewer.
A tool suite is available to perform edge contraction, point cloud persistence, and so on.

- Alpha complex (new package)

     - Alpha_complex is a simplicial complex data structure constructed from the
     finite cells of a Delaunay Triangulation.

- Cubical complex (new package)

     - The cubical complex is an example of a structured complex useful in
     computational mathematics (specially rigorous numerics) and image
     analysis.

- Witness complex (new package)

     - Witness complex Wit(W,L) is a simplicial complex defined on two sets of
     points in Rd. The data structure is described in the paper "Jean-Daniel
     Boissonnat and Clément Maria. The Simplex Tree: An Efficient Data
     Structure for General Simplicial Complexes. Algorithmica, pages 1–22,
     2014."

- Persistent cohomology (new examples)

     - alpha_complex_persistence: How to compute persistent homology from an
       alpha complex.
     - periodic_alpha_complex_3d_persistence.cpp: How to compute persistent
       homology on a periodic alpha complex in 3D.
     - Bitmap_cubical_complex.cpp: How to compute persistent homology from an
       cubical complex.
     - Bitmap_cubical_complex_periodic_boundary_conditions.cpp: How to compute
       persistent homology from a periodic cubical complex.

- Documentation

     - a section on examples.

     - a summary of modules on the main page.

- Data sets

     - tore3D_300.off: 300 random points on a 3D torus.

     - grid_10_10_10_in_0_1.off: Points every 0.1 in each 3 dimensions in
       [0, 1].

     - in data/bitmaps : examples of Perseus style file for Cubical complex

All modules are distributed under the terms of the GPL Open Source license (GNU General Public License v3 or later versions).

We kindly ask users to cite the GUDHI library as appropriately as possible in their papers, and to mention the use of the GUDHI library on the web pages of
their projects using GUDHI and provide us with links to these web pages.
Feel free to [contact us][1] in case you have any question or remark on this topic.

We provide [bibtex entries][2] for the modules of the User and Reference Manual, as well as for publications directly related to the GUDHI library. 

For further information and for [downloading the library][3] and its documentation, please visit the [GUDHI documentation web site][4].


 [1]: {{ site.url }}/contact
 [2]: {{ site.url }}/doc/latest/_citation.html
 [3]: https://gforge.inria.fr/frs/?group_id=3865
 [4]: {{ site.url }}/doc/latest/



