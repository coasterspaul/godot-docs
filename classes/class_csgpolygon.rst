.. Generated automatically by doc/tools/makerst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the CSGPolygon.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_CSGPolygon:

CSGPolygon
==========

**Inherits:** :ref:`CSGPrimitive<class_CSGPrimitive>` **<** :ref:`CSGShape<class_CSGShape>` **<** :ref:`VisualInstance<class_VisualInstance>` **<** :ref:`Spatial<class_Spatial>` **<** :ref:`Node<class_Node>` **<** :ref:`Object<class_Object>`

**Category:** Core

Brief Description
-----------------

Extrudes a 2D polygon shape to create a 3D mesh.

Properties
----------

+---------------------------------------------------+--------------------------------------------------------------+
| :ref:`float<class_float>`                         | :ref:`depth<class_CSGPolygon_depth>`                         |
+---------------------------------------------------+--------------------------------------------------------------+
| :ref:`Material<class_Material>`                   | :ref:`material<class_CSGPolygon_material>`                   |
+---------------------------------------------------+--------------------------------------------------------------+
| :ref:`Mode<enum_CSGPolygon_Mode>`                 | :ref:`mode<class_CSGPolygon_mode>`                           |
+---------------------------------------------------+--------------------------------------------------------------+
| :ref:`bool<class_bool>`                           | :ref:`path_continuous_u<class_CSGPolygon_path_continuous_u>` |
+---------------------------------------------------+--------------------------------------------------------------+
| :ref:`float<class_float>`                         | :ref:`path_interval<class_CSGPolygon_path_interval>`         |
+---------------------------------------------------+--------------------------------------------------------------+
| :ref:`bool<class_bool>`                           | :ref:`path_joined<class_CSGPolygon_path_joined>`             |
+---------------------------------------------------+--------------------------------------------------------------+
| :ref:`bool<class_bool>`                           | :ref:`path_local<class_CSGPolygon_path_local>`               |
+---------------------------------------------------+--------------------------------------------------------------+
| :ref:`NodePath<class_NodePath>`                   | :ref:`path_node<class_CSGPolygon_path_node>`                 |
+---------------------------------------------------+--------------------------------------------------------------+
| :ref:`PathRotation<enum_CSGPolygon_PathRotation>` | :ref:`path_rotation<class_CSGPolygon_path_rotation>`         |
+---------------------------------------------------+--------------------------------------------------------------+
| :ref:`PoolVector2Array<class_PoolVector2Array>`   | :ref:`polygon<class_CSGPolygon_polygon>`                     |
+---------------------------------------------------+--------------------------------------------------------------+
| :ref:`bool<class_bool>`                           | :ref:`smooth_faces<class_CSGPolygon_smooth_faces>`           |
+---------------------------------------------------+--------------------------------------------------------------+
| :ref:`float<class_float>`                         | :ref:`spin_degrees<class_CSGPolygon_spin_degrees>`           |
+---------------------------------------------------+--------------------------------------------------------------+
| :ref:`int<class_int>`                             | :ref:`spin_sides<class_CSGPolygon_spin_sides>`               |
+---------------------------------------------------+--------------------------------------------------------------+

Enumerations
------------

  .. _enum_CSGPolygon_Mode:

enum **Mode**:

- **MODE_DEPTH** = **0** --- Shape is extruded to :ref:`depth<class_CSGPolygon_depth>`.
- **MODE_SPIN** = **1** --- Shape is extruded by rotating it around an axis.
- **MODE_PATH** = **2** --- Shape is extruded along a path set by a :ref:`Shape<class_Shape>` set in :ref:`path_node<class_CSGPolygon_path_node>`.

  .. _enum_CSGPolygon_PathRotation:

enum **PathRotation**:

- **PATH_ROTATION_POLYGON** = **0** --- Slice is not rotated.
- **PATH_ROTATION_PATH** = **1** --- Slice is rotated around the up vector of the path.
- **PATH_ROTATION_PATH_FOLLOW** = **2** --- Slice is rotate to match the path exactly.

Description
-----------

This node takes a 2D polygon shape and extrudes it to create a 3D mesh.

Property Descriptions
---------------------

  .. _class_CSGPolygon_depth:

- :ref:`float<class_float>` **depth**

+----------+------------------+
| *Setter* | set_depth(value) |
+----------+------------------+
| *Getter* | get_depth()      |
+----------+------------------+

Extrusion depth when :ref:`mode<class_CSGPolygon_mode>` is constant MODE_DEPTH.

  .. _class_CSGPolygon_material:

- :ref:`Material<class_Material>` **material**

+----------+---------------------+
| *Setter* | set_material(value) |
+----------+---------------------+
| *Getter* | get_material()      |
+----------+---------------------+

Material to use for the resulting mesh.

  .. _class_CSGPolygon_mode:

- :ref:`Mode<enum_CSGPolygon_Mode>` **mode**

+----------+-----------------+
| *Setter* | set_mode(value) |
+----------+-----------------+
| *Getter* | get_mode()      |
+----------+-----------------+

Extrusion mode.

  .. _class_CSGPolygon_path_continuous_u:

- :ref:`bool<class_bool>` **path_continuous_u**

+----------+------------------------------+
| *Setter* | set_path_continuous_u(value) |
+----------+------------------------------+
| *Getter* | is_path_continuous_u()       |
+----------+------------------------------+

If true the u component of our uv will continuously increase in unison with the distance traveled along our path when :ref:`mode<class_CSGPolygon_mode>` is constant MODE_PATH.

  .. _class_CSGPolygon_path_interval:

- :ref:`float<class_float>` **path_interval**

+----------+--------------------------+
| *Setter* | set_path_interval(value) |
+----------+--------------------------+
| *Getter* | get_path_interval()      |
+----------+--------------------------+

Interval at which a new extrusion slice is added along the path when :ref:`mode<class_CSGPolygon_mode>` is constant MODE_PATH.

  .. _class_CSGPolygon_path_joined:

- :ref:`bool<class_bool>` **path_joined**

+----------+------------------------+
| *Setter* | set_path_joined(value) |
+----------+------------------------+
| *Getter* | is_path_joined()       |
+----------+------------------------+

If true the start and end of our path are joined together ensuring there is no seam when :ref:`mode<class_CSGPolygon_mode>` is constant MODE_PATH.

  .. _class_CSGPolygon_path_local:

- :ref:`bool<class_bool>` **path_local**

+----------+-----------------------+
| *Setter* | set_path_local(value) |
+----------+-----------------------+
| *Getter* | is_path_local()       |
+----------+-----------------------+

If false we extrude centered on our path, if true we extrude in relation to the position of our CSGPolygon when :ref:`mode<class_CSGPolygon_mode>` is constant MODE_PATH.

  .. _class_CSGPolygon_path_node:

- :ref:`NodePath<class_NodePath>` **path_node**

+----------+----------------------+
| *Setter* | set_path_node(value) |
+----------+----------------------+
| *Getter* | get_path_node()      |
+----------+----------------------+

The :ref:`Shape<class_Shape>` object containing the path along which we extrude when :ref:`mode<class_CSGPolygon_mode>` is constant MODE_PATH.

  .. _class_CSGPolygon_path_rotation:

- :ref:`PathRotation<enum_CSGPolygon_PathRotation>` **path_rotation**

+----------+--------------------------+
| *Setter* | set_path_rotation(value) |
+----------+--------------------------+
| *Getter* | get_path_rotation()      |
+----------+--------------------------+

The method by which each slice is rotated along the path when :ref:`mode<class_CSGPolygon_mode>` is constant MODE_PATH.

  .. _class_CSGPolygon_polygon:

- :ref:`PoolVector2Array<class_PoolVector2Array>` **polygon**

+----------+--------------------+
| *Setter* | set_polygon(value) |
+----------+--------------------+
| *Getter* | get_polygon()      |
+----------+--------------------+

Point array that defines the shape that we'll extrude.

  .. _class_CSGPolygon_smooth_faces:

- :ref:`bool<class_bool>` **smooth_faces**

+----------+-------------------------+
| *Setter* | set_smooth_faces(value) |
+----------+-------------------------+
| *Getter* | get_smooth_faces()      |
+----------+-------------------------+

Generates smooth normals so smooth shading is applied to our mesh.

  .. _class_CSGPolygon_spin_degrees:

- :ref:`float<class_float>` **spin_degrees**

+----------+-------------------------+
| *Setter* | set_spin_degrees(value) |
+----------+-------------------------+
| *Getter* | get_spin_degrees()      |
+----------+-------------------------+

Degrees to rotate our extrusion for each slice when :ref:`mode<class_CSGPolygon_mode>` is constant MODE_SPIN.

  .. _class_CSGPolygon_spin_sides:

- :ref:`int<class_int>` **spin_sides**

+----------+-----------------------+
| *Setter* | set_spin_sides(value) |
+----------+-----------------------+
| *Getter* | get_spin_sides()      |
+----------+-----------------------+

Number of extrusion when :ref:`mode<class_CSGPolygon_mode>` is constant MODE_SPIN.

