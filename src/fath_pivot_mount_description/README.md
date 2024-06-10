fath_pivot_mount_description
=======================

This package contains a single URDF macro used to add a manually-adjustable, Fath pivot mount used for cameras and other
sensors.

![Fath Pivot Mount](doc/fath_pivot_mount_urdf.png "The Fath pivot mount model, with an angle of pi/8")

To add the mount to your URDF, add e.g.

```xml
<xacro:include filename="$(find fath_pivot_mount_description)/urdf/lockmount.urdf.xacro" />
<xacro:fath_pivot_mount prefix="front_camera" parent_link="front_mount" angle="${pi/8}">
  <origin xyz="0 0 0" rpy="0 0 0" />
</xacro:fath_pivot_mount>

<xacro:sensor_d435 parent="front_camera_mount" name="front_realsense">
  <origin xyz="0 0 0" rpy="0 0 0" />
</xacro:sensor_d435>
```

The `prefix` parameter is prepended to all the joints and links inside the macro to ensure uniqueness.

The `parent_link` parameter defines the parent of the fath_pivot_mount.  The macro automatically creates a fixed
joint between `parent_link` and `${prefix}_base_link`.

The `angle` parameter is the pitch angle of the mount.  This angle is assumed to be fixed, as the fath_pivot_mount
is manually adjusted.

The mounting surface of the mount is `${prefix}_mount`, which may be used as the parent link for other URDF joints,
as shown in the example above.
