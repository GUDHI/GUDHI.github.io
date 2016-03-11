---
layout: page
#
# Content
#
subheadline: "New release"
title: "GUDHI version 1.2.0"
teaser: "We are pleased to announce the release 1.2.0 of the GUDHI library."
author: vrouvreau
categories:
  - Release
tags:
  - GUDHI release
#
# Styling
#
#image:
#  header: ""
#  thumb: "Calabi_yau_formatted_thumb.jpg"
#  homepage: "Calabi_yau_formatted.jpg"
#  caption: "Caption?"
---


Below is a list of changes made since GUDHI 1.1.0:

- GudhUI (new package)
This package provides a User Interface to have a quick overview of GUDHI features.
GudhUI allows to load OFF points or meshes files that can be visualized on a 3D viewer.
A tool suite is available to perform edge contraction, point cloud persistence, and so on.

- Persistent cohomology (new examples)

     - persistence_from_simple_simplex_tree: How to compute persistent homology after inserting simplices and their filtration values
     - plain_homology: How to compute (non-persistent) homology on simplices
     - alpha_shapes_persistence.cpp: How to compute persistent homology after constructing a CGAL 3D alpha shape simplices on a point cloud file

- Simplex tree (new example)

     - mini_simplex_tree: How to fill a minimalist (in terms of memory usage) simplex tree

- Skeleton blocker (new examples)

     - Skeleton_blocker_from_simplices: How to fill a skeleton blocker with simplices
     - Skeleton_blocker_link: How to find a link in a skeleton blocker

- Compilation

     - Fix CMake issues.

     - Fix Clang compilation.

     - Fix Visual Studio 2013 compilation.

- Data sets

     - spiral_3d_10k.off: 10000 points on a 3D spiral.

     - spiral_4d_10k.off: 10000 points on a 4D spiral.

     - tore3D_1307.off: 1307 points on a 3D torus.

     - images: pictures taken from a camera rotating around an object (asian mug, little car, lucky cat and money pig) and their off files associated.

All modules are distributed under the terms of the GPL Open Source license (GNU General Public License v3 or later versions).

We kindly ask users to cite the GUDHI library as appropriately as possible in their papers, and to mention the use of the GUDHI library on the web pages of
their projects using GUDHI and provide us with links to these web pages.
Feel free to [contact us][1] in case you have any question or remark on this topic.

We provide [bibtex entries][2] for the modules of the User and Reference Manual, as well as for publications directly related to the GUDHI library. 

For further information and for [downloading the library][3] and its documentation, please visit the [GUDHI documentation web site][4].


 [1]: {{ site.url }}/contact
 [2]: http://gudhi.gforge.inria.fr/doc/latest/_citation.html
 [3]: https://gforge.inria.fr/frs/?group_id=3865
 [4]: http://gudhi.gforge.inria.fr/doc/latest/


