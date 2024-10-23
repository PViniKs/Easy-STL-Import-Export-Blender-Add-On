# Easy STL Import/Export Blender Add-On
Modified version of native "Import-Export STL files" blender add-on, with keyboard shortcuts for import and export operators

> [!NOTE]
> This Add-On is a modified version of the original STL Import/Export Add-On that comes with Blender. It was modified to add keyboard shortcuts for the import and export operators, making it easier to use, as you don't need to go through all the menu.

> [!IMPORTANT]
> The original Add-On documentation is found at:
https://docs.blender.org/manual/en/3.5/addons/import_export/mesh_stl.html

> [!TIP]
> The only changes made to the original Add-On were at "register" and "unregister" functions, where keyboard shortcuts (Ctrl + I for import / Ctrl + E for export) were added.


## [Original Reference](https://docs.blender.org/manual/en/3.5/addons/import_export/mesh_stl)

**Category: Import-Export**

**Menu: File > Import/Export > Stl (.stl)**

> This format is useful if you intend to import/export the files for CAD software. It is also commonly used for loading into 3D printing software.

> [!WARNING]
> Currently the script does not handle importing or exporting of normals and does not handle endian-ness, there is nothing in the STL specification about it.

## Importing

### Properties

### Transform

**Scale**
- Value by which to scale the imported objects in relation to the world’s origin.

**Scene Unit**
- Apply current scene’s unit (as defined by unit scale) to imported data.

**Forward / Up Axis**
- Since many applications use a different axis for pointing upwards, these are axis conversion for these settings, Forward and up axes – By mapping these to different axes you can convert rotations between applications default up and forward axes.
- Blender uses Y forward, Z up (since the front view looks along the +Y direction). For example, it is common for applications to use Y as the up axis, in that case -Z forward, Y up is needed.

### Geometry

**Facet Normals**
- Use (import) facet normals (note that this will still give flat shading).

## Exporting

### Properties

### ASCII
- TODO.

### Batch Mode
- TODO.

### Include

**Selection Only**
- When checked, only selected objects are exported. Instanced objects, for example collections that are instanced in the scene, are considered ‘selected’ when their instancer is selected.

### Transform

**Scale**
- Value by which to scale the exported objects in relation to the world’s origin.

**Scene Unit**
- Apply current scene’s unit (as defined by unit scale) to exported data.

**Forward / Up Axis**
- Since many applications use a different axis for ‘Up’, these are axis conversion for these settings, Forward and Up axes – By mapping these to different axes you can convert rotations between applications default up and forward axes.
- Blender uses Y Forward, Z Up (since the front view looks along the +Y direction). For example, it’s common for applications to use Y as the up axis, in that case -Z Forward, Y Up is needed.

**Geometry**
**Apply Modifiers**
- Export objects using the evaluated mesh, meaning the resulting mesh after all Modifiers have been calculated.

## Usage
Use the operator to import ASCII or binary STL-files, you can select multiple files at once. For exporting you can select multiple objects and they will be exported as a single STL-file. You can select between ASCII/binary file format (binary is more compact). You can also choose to enable or disable the modifiers during the export. When on "Object Mode", you can use `Ctrl + I` to easily import STL-files and `Ctrl + E` to export them.
