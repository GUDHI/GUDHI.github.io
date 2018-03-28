---
layout: page
#
# Content
#
subheadline: "New release"
title: "GUDHI version 2.0.1"
teaser: "This minor GUDHI library version is fixing issues and improves persistence graphical tools module. All the new modules comes with their Python interface and a lot of examples, even in Python."
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
  url: https://gforge.inria.fr/frs/download.php/file/37140/2017-10-02-10-19-30_GUDHI_2.0.1.tar.gz
  text: Download GUDHI version 2.0.1 ›
  style: alert
---


Below is a list of changes made since Gudhi 2.0.0:

- Spatial searching (new function)

     - Spatial searching is now offering a radius search method.

- Persistence graphical tools (interfaces improvement)

     - Add a band boot display mechanism on persistence diagram.
     - Number of points and barcode limitation before the display.
     - Interface modification to read persistence from a file.

- Bottleneck distance (bug fix)

     - Read persistence files with infinity values bug is fixed.

- Persistent cohomology (bug fix)

     - Weighted Alpha complex 3d persistence bug is fixed.

- Simplex tree (dead code)

     - Remove useless global filtration attribute, getter and setter.

- cython

     - Plot persistence functions improvement.
     - Rename cythonize_gudhi.py in setup.py to be conform with Python conventions.
     - Windows python module compilation issue fix.
     - Documentation generation bug fix.
     - Reduce CMake interactions.
     - Rips complex memory leak fix.

- Doxygen

     - Using MathJax.js to generate LaTeX instead of png.

- CMake

     - Boost dependencies improvement.
     - Conda compilation issues fix.
     - Modules activation/desactivation mechanism for compilation and test.

- Data points generator

     - Move data/points/generator into src/common/utilities.
     

All modules are distributed under the terms of the GPL Open Source license (GNU General Public License v3 or later versions), but a commercial license is also possible.

We kindly ask users to cite the GUDHI library as appropriately as possible in their papers, and to mention the use of the GUDHI library on the web pages of
their projects using GUDHI and provide us with links to these web pages.

Feel free to [contact us][1] in case you have any question or remark on this topic.

We provide [bibtex entries][2] for the modules of the User and Reference Manual, as well as for publications directly related to the GUDHI library. 

For further information about [downloading][3] and installing the library ([C++][6] or [Python][7]), please visit the [GUDHI web site][4].


 [1]: {{ site.url }}/contact
 [2]: {{ site.url }}/doc/latest/_citation.html
 [3]: https://gforge.inria.fr/frs/?group_id=3865
 [4]: {{ site.url }}/
 [5]: http://doc.cgal.org/latest/Spatial_searching/index.html
 [6]: {{ site.url }}/doc/latest/installation.html
 [7]: {{ site.url }}/python/latest/installation.html


