---
layout: page
#
# Content
#
subheadline: "New release"
title: "GUDHI version 1.3.1"
teaser: "We are pleased to announce the release 1.3.1 of the GUDHI library."
author: vrouvreau
categories:
  - Release
tags:
  - GUDHI release
---




Below is a list of changes made since Gudhi 1.3.0:

- Bug fix

As Simplex_handle default type was an 'int' in the simplex tree data structure, persistence cohomology computation was segmentation faulting
when the number of simplices was going further to the 'int' maximum value (2.7 billions of simplices on a classical modern machine and OS).
Simplex_handle default type is now an 'std::uint32_t' and can go up to about 4 billions of simplices.

- CMake

     - The messages from CMake has been rewritten to be more consistent.

- Coding conventions

     - CMake projects names and C++ namespaces have been homogenized.

- Documentation

     - Mandatory and optional third party libraries have been separated in the documentation.

- Data sets

     - in data/points/generator : thanks to [Aurélien Alvarez][5], aurelien_alvarez_surfaces_in_R8.py is a script to generate
     points on a surface in R8.

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
 [5]: http://www.aurelienalvarez.org/

