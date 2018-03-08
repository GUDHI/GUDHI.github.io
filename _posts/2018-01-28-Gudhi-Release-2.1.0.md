---
layout: page
#
# Content
#
subheadline: "New release"
title: "GUDHI version 2.1.0"
teaser: "As a major new feature, the GUDHI library now offers persistence representations and cover complex (no Python interface yet)."
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
  url: https://gforge.inria.fr/frs/download.php/file/37362/2018-01-31-09-25-53_GUDHI_2.1.0.tar.gz
  text: Download GUDHI version 2.1.0
  style: alert
---


Below is a list of changes made since Gudhi 2.0.1:

- [Cover complex][8] (new package)
     - Nerves and Graph Induced Complexes are cover complexes, that provably contain topological information about the input data.

- [Persistence representation][9] (new package)
     - It contains implementation of various representations of persistence
     diagrams. It implements basic functionalities which are neccessary to use
     persistence in statistics and machine learning.

- [Simplex tree][10] (new functions and interfaces)
     - Graph expansion with a blocker oracle.
     - Cech complex implementation example using CGAL mini spheres in fixed dimension.
     - Automatic dimension set mechanism.

- Alpha complex (new function)
     - [Weighted periodic 3D][11] version utility.

- CGAL 4.11 compilation issue (bug fix)

- [Cubical complex][12] (bug fix)
     - Perseus file read function.
     - Computations of incidence indices between cubes.
     - Missing periodic argument for the Python version. 

- Documentation
     - New [file formats][13] section.
     - Bugs fix

- [Utilities][14]
     - Separate examples from utilities.


All modules are distributed under the terms of the GPL Open Source license (GNU General Public License v3 or later versions), but a commercial license is also possible.

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
 [8]: {{ site.url }}/doc/latest/group__cover__complex.html
 [9]: {{ site.url }}/doc/latest/group___persistence__representations.html
 [10]: {{ site.url }}/doc/latest/group__simplex__tree.html
 [11]: {{ site.url }}/doc/latest/_alpha_complex_2weighted_periodic_alpha_complex_3d_persistence_8cpp-example.html
 [12]: {{ site.url }}/doc/latest/group__cubical__complex.html
 [13]: {{ site.url }}/doc/latest/fileformats.html
 [14]: {{ site.url }}/utils/

