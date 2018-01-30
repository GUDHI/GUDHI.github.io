---
layout: page
title: "Utilities"
meta_title: "utils"
subheadline: ""
teaser: ""
permalink: "/utils/"
---
{::comment}
These flags above are here for web site generation, please let them.
cf. https://gitlab.inria.fr/GUDHI/website
Must be in conformity with _data/navigation.yml
{:/comment}



# Alpha complex #


## alpha_complex_persistence ##

This program computes the persistent homology with coefficient field Z/pZ of the dD alpha complex built from a dD point cloud.
The output diagram contains one bar per line, written with the convention:

```
   p dim birth death
```

where `dim` is the dimension of the homological feature, `birth` and `death` are respectively the birth and death of the feature,
and `p` is the characteristic of the field *Z/pZ* used for homology coefficients (`p` must be a prime number).

**Usage**

```
   alpha_complex_persistence [options] <input OFF file>
```

where
`<input OFF file>` is the path to the input point cloud in [nOFF ASCII format](http://www.geomview.org/docs/html/OFF.html).

**Allowed options**

* `-h [ --help ]` Produce help message
* `-o [ --output-file ]` Name of file in which the persistence diagram is written. Default print in standard output.
* `-r [ --max-alpha-square-value ]` (default = inf) Maximal alpha square value for the Alpha complex construction.
* `-p [ --field-charac ]` (default = 11)     Characteristic p of the coefficient field Z/pZ for computing homology.
* `-m [ --min-persistence ]` (default = 0) Minimal lifetime of homology feature to be recorded. Enter a negative value to see zero length intervals.

**Example**

```
   alpha_complex_persistence -r 32 -p 2 -m 0.45 ../../data/points/tore3D_300.off
```

N.B.:

* Filtration values are alpha square values.


## alpha_complex_3d_persistence ##
This program computes the persistent homology with coefficient field Z/pZ of the 3D alpha complex built from a 3D point cloud. The output diagram contains one bar per line, written with the convention:

```
p dim birth death
```

where `dim` is the dimension of the homological feature, `birth` and `death` are respectively the birth and death of the feature, and `p` is the characteristic of the field *Z/pZ* used for homology coefficients (`p` must be a prime number).

**Usage**

```
   alpha_complex_3d_persistence [options] <input OFF file>
```

where `<input OFF file>` is the path to the input point cloud in [nOFF ASCII format](http://www.geomview.org/docs/html/OFF.html).

**Allowed options**

* `-h [ --help ]` Produce help message
* `-o [ --output-file ]` Name of file in which the persistence diagram is written. Default print in standard output.
* `-p [ --field-charac ]` (default=11) Characteristic p of the coefficient field Z/pZ for computing homology.
* `-m [ --min-persistence ]` (default = 0) Minimal lifetime of homology feature to be recorded. Enter a negative value to see zero length intervals.

**Example**

```
alpha_complex_3d_persistence ../../data/points/tore3D_300.off -p 2 -m 0.45
```

N.B.:

* `alpha_complex_3d_persistence` only accepts OFF files in dimension 3.
* Filtration values are alpha square values.


## exact_alpha_complex_3d_persistence ##

Same as `alpha_complex_3d_persistence`, but using exact computation.
It is slower, but it is necessary when points are on a grid for instance.



## weighted_alpha_complex_3d_persistence ##

Same as `alpha_complex_3d_persistence`, but using weighted points.

**Usage**

```
   weighted_alpha_complex_3d_persistence [options] <input OFF file> <weights input file>
```

where

* `<input OFF file>` is the path to the input point cloud in [nOFF ASCII format](http://www.geomview.org/docs/html/OFF.html).
* `<input weights file>` is the path to the file containing the weights of the points (one value per line).

**Allowed options**

* `-h [ --help ]` Produce help message
* `-o [ --output-file ]` Name of file in which the persistence diagram is written. Default print in standard output.
* `-p [ --field-charac ]` (default=11) Characteristic p of the coefficient field Z/pZ for computing homology.
* `-m [ --min-persistence ]` (default = 0) Minimal lifetime of homology feature to be recorded. Enter a negative value to see zero length intervals.

**Example**

```
   weighted_alpha_complex_3d_persistence ../../data/points/tore3D_300.off ../../data/points/tore3D_300.weights -p 2 -m 0.45
```


N.B.:

* Weights values are explained on CGAL [Alpha shape](https://doc.cgal.org/latest/Alpha_shapes_3/index.html#title0)
and [Regular triangulation](https://doc.cgal.org/latest/Triangulation_3/index.html#Triangulation3secclassRegulartriangulation) documentation.
* Filtration values are alpha square values.


## periodic_alpha_complex_3d_persistence ##
Same as `alpha_complex_3d_persistence`, but using periodic alpha shape 3d.
Refer to the [CGAL's 3D Periodic Triangulations User Manual](https://doc.cgal.org/latest/Periodic_3_triangulation_3/index.html) for more details.

**Usage**

```
   periodic_alpha_complex_3d_persistence [options] <input OFF file> <cuboid file>
```

where

* `<input OFF file>` is the path to the input point cloud in [nOFF ASCII format](http://www.geomview.org/docs/html/OFF.html).
* `<cuboid file>` is the path to the file describing the periodic domain. It must be in the format described [here](/doc/latest/fileformats.html#FileFormatsIsoCuboid).

**Allowed options**

* `-h [ --help ]` Produce help message
* `-o [ --output-file ]` Name of file in which the persistence diagram is written. Default print in standard output.
* `-p [ --field-charac ]` (default=11) Characteristic p of the coefficient field Z/pZ for computing homology.
* `-m [ --min-persistence ]` (default = 0) Minimal lifetime of homology feature to be recorded. Enter a negative value to see zero length intervals


**Example**

```
periodic_alpha_complex_3d_persistence ../../data/points/grid_10_10_10_in_0_1.off ../../data/points/iso_cuboid_3_in_0_1.txt -p 3 -m 1.0
```

N.B.: 

* Cuboid file must be in the format described [here](/doc/latest/fileformats.html#FileFormatsIsoCuboid).
* Filtration values are alpha square values.


# Bottleneck distance #

## bottleneck_read_file_example ##

This program computes the Bottleneck distance between two persistence diagram files.

**Usage**

```
   bottleneck_read_file_example <file_1.pers> <file_2.pers> [<tolerance>]
```

where

* `<file_1.pers>` and `<file_2.pers>` must be in the format described [here](/doc/latest/fileformats.html#FileFormatsPers).
* `<tolerance>` is an error bound on the bottleneck distance (set by default to the smallest positive double value).


# Cover complex #

## Nerve ##
This program builds the Nerve of a point cloud sampled on an OFF file.
The cover C comes from the preimages of intervals covering a coordinate function,
which are then refined into their connected components using the triangulation of the .OFF file.

The program also writes a file SC.txt.
The first three lines in this file are the location of the input point cloud and the function used to compute the cover.
The fourth line contains the number of vertices nv and edges ne of the Nerve. The next nv lines represent the vertices.
Each line contains the vertex ID, the number of data points it contains, and their average color function value.
Finally, the next ne lines represent the edges, characterized by the ID of their vertices.

**Usage**

`Nerve <OFF input file> coordinate resolution gain [--v]`

where

* `coordinate` is the coordinate function to cover
* `resolution` is the number of the intervals
* `gain` is the gain for each interval
* `--v` is optional, it activates verbose mode.

**Example**

`Nerve ../../data/points/human.off 2 10 0.3`

* Builds the Nerve of a point cloud sampled on a 3D human shape (human.off).
The cover C comes from the preimages of intervals (10 intervals with gain 0.3) covering the height function (coordinate 2).

`python KeplerMapperVisuFromTxtFile.py -f ../../data/points/human.off_sc.txt`

* Constructs `human.off_sc.html` file. You can now use your favorite web browser to visualize it.

## VoronoiGIC ##

This util builds the Graph Induced Complex (GIC) of a point cloud.
It subsamples *N* points in the point cloud, which act as seeds of a geodesic Voronoï diagram.
Each cell of the diagram is then an element of C.

The program also writes a file `*_sc.off`, that is an OFF file that can be visualized with GeomView.

**Usage**

`VoroniGIC <OFF input file> samples_number [--v]`

where

* `samples_number` is the number of samples to take from the point cloud
* `--v` is optional, it activates verbose mode.

**Example**

`VoroniGIC ../../data/points/human.off 700`

* Builds the Voronoi Graph Induced Complex with 700 subsamples from `human.off` file.
`../../data/points/human_sc.off` can be visualized with GeomView.


# Cubical Complex #

## cubical_complex_persistence ##
This program computes persistent homology, by using the Bitmap_cubical_complex class, of cubical complexes provided in text files in Perseus style.
See [here](/doc/latest/fileformats.html#FileFormatsPerseus) for a description of the file format.

**Example**

```
   cubical_complex_persistence data/bitmap/CubicalTwoSphere.txt
```

* Creates a Cubical Complex from the Perseus style file `CubicalTwoSphere.txt`,
computes Persistence cohomology from it and writes the results in a persistence file `CubicalTwoSphere.txt_persistence`.

## periodic_cubical_complex_persistence ##

Same as above, but with periodic boundary conditions.

**Example**

```
   periodic_cubical_complex_persistence data/bitmap/3d_torus.txt
```

* Creates a Periodical Cubical Complex from the Perseus style file `3d_torus.txt`,
computes Persistence cohomology from it and writes the results in a persistence file `3d_torus.txt_persistence`.


# Rips Complex #

## rips_persistence ##
This program computes the persistent homology with coefficient field *Z/pZ* of a Rips complex defined on a set of input points. The output diagram contains one bar per line, written with the convention:

`p dim birth death`

where `dim` is the dimension of the homological feature, `birth` and `death` are respectively the birth and death of the feature, and `p` is the characteristic of the field *Z/pZ* used for homology coefficients (`p` must be a prime number).

**Usage**

`rips_persistence [options] <OFF input file>`

**Allowed options**

* `-h [ --help ]` Produce help message
* `-o [ --output-file ]` Name of file in which the persistence diagram is written. Default print in standard output.
* `-r [ --max-edge-length ]` (default = inf) Maximal length of an edge for the Rips complex construction.
* `-d [ --cpx-dimension ]` (default = 1) Maximal dimension of the Rips complex we want to compute.
* `-p [ --field-charac ]` (default = 11)     Characteristic p of the coefficient field Z/pZ for computing homology.
* `-m [ --min-persistence ]` (default = 0) Minimal lifetime of homology feature to be recorded. Enter a negative value to see zero length intervals.

Beware: this program may use a lot of RAM and take a lot of time if `max-edge-length` is set to a large value.

**Example 1 with Z/2Z coefficients**

`rips_persistence ../../data/points/tore3D_1307.off -r 0.25 -m 0.5 -d 3 -p 2`

**Example 2 with Z/3Z coefficients**

`rips_persistence ../../data/points/tore3D_1307.off -r 0.25 -m 0.5 -d 3 -p 3`


## rips_distance_matrix_persistence ##

Same as `rips_persistence` but taking a distance matrix as input. 

**Usage**

`rips_persistence [options] <CSV input file>`

where
`<CSV input file>` is the path to the file containing a distance matrix. Can be square or lower triangular matrix. Separator is ';'.

**Example**

`rips_distance_matrix_persistence data/distance_matrix/full_square_distance_matrix.csv -r 15 -d 3 -p 3 -m 0`


# Witness complex #

For more details about the witness complex, please read the [user manual of the package](/doc/latest/group__witness__complex.html).

## weak_witness_persistence ##
This program computes the persistent homology with coefficient field *Z/pZ* of a Weak witness complex defined on a set of input points.
The output diagram contains one bar per line, written with the convention:

`p dim birth death`

where `dim` is the dimension of the homological feature, `birth` and `death` are respectively the birth and death of the feature,
and `p` is the characteristic of the field *Z/pZ* used for homology coefficients.

**Usage**

`weak_witness_persistence [options] <OFF input file>`

**Allowed options**

* `-h [ --help ]` Produce help message
* `-l [ --landmarks ]` Number of landmarks to choose from the point cloud.
* `-o [ --output-file ]` Name of file in which the persistence diagram is written. By default, print in std::cout.
* `-a [ --max-sq-alpha ]` (default = inf) Maximal squared relaxation parameter.
* `-p [ --field-charac ]` (default = 11) Characteristic p of the coefficient field Z/pZ for computing homology.
* `-m [ --min-persistence ]` (default = 0) Minimal lifetime of homology feature to be recorded. Enter a negative value to see zero length intervals.
* `-d [ --cpx-dimension ]` (default = 2147483647) Maximal dimension of the weak witness complex we want to compute.

**Example**

`weak_witness_persistence data/points/tore3D_1307.off -l 20 -a 0.5 -m 0.006`

N.B.: output is random as the 20 landmarks are chosen randomly.


## strong_witness_persistence ##

This program computes the persistent homology with coefficient field *Z/pZ* of a Strong witness complex defined on a set of input points.
The output diagram contains one bar per line, written with the convention:

`p dim birth death`

where `dim` is the dimension of the homological feature, `birth` and `death` are respectively the birth and death of the feature,
and `p` is the characteristic of the field *Z/pZ* used for homology coefficients.

**Usage**

`strong_witness_persistence [options] <OFF input file>`

**Allowed options**

* `-h [ --help ]` Produce help message
* `-l [ --landmarks ]` Number of landmarks to choose from the point cloud.
* `-o [ --output-file ]` Name of file in which the persistence diagram is written. By default, print in std::cout.
* `-a [ --max-sq-alpha ]` (default = inf) Maximal squared relaxation parameter.
* `-p [ --field-charac ]` (default = 11) Characteristic p of the coefficient field Z/pZ for computing homology.
* `-m [ --min-persistence ]` (default = 0) Minimal lifetime of homology feature to be recorded. Enter a negative value to see zero length intervals.
* `-d [ --cpx-dimension ]` (default = 2147483647) Maximal dimension of the weak witness complex we want to compute.

**Example**

`strong_witness_persistence data/points/tore3D_1307.off -l 20 -a 0.5 -m 0.06`

N.B.: output is random as the 20 landmarks are chosen randomly.


# common #

## off_file_from_shape_generator ##

Generates a pointset and save it in an OFF file. Command-line is:

```
off_file_from_shape_generator on|in sphere|cube|curve|torus|klein <filename> <num_points> <dimension> <parameter1> <parameter2>...
```

Warning: "on cube" generator is not available!

**Examples**

```
off_file_from_shape_generator on sphere onSphere.off 1000 3 15.2
```

* Generates an onSphere.off file with 1000 points randomized on a sphere of dimension 3 and radius 15.2.
 
```
off_file_from_shape_generator in sphere inSphere.off 100 2
```

* Generates an inSphere.off file with 100 points randomized in a sphere of dimension 2 (circle) and radius 1.0 (default).

```
off_file_from_shape_generator in cube inCube.off 10000 3 5.8
```

* Generates a inCube.off file with 10000 points randomized in a cube of dimension 3 and side 5.8.


