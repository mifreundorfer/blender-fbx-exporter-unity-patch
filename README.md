# A patched Blender FBX Exporter for Unity

## Modifications

- Changed the node type for Armatures from 'Null' to 'LimbNode' to prevent Unity from optimizing out the Armature Root Node when only a single object is in the file (since that will break animation import).

- Using simplify during animation export currently drops constant curves, this makes it impossible to export a static pose. Modified simplify so that curves that differ from the rest pose are always retained. (Not properly tested with object animation, only bones)


## Installation

Replace the io_scene_fbx folder in your Blender install with the one from this repository, found here:(Blender install folder)/2.76/scripts/addons/io_scene_fbx
