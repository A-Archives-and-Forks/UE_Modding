# Previewing Animations
UModel is great at finding all associated animations of a skeleton mesh and playing them.

Once you load your Skeletal Mesh(SK), SkeletalMesh->FindAnimations.

![UModel context menu on Skeletal Mesh with 'FindAnimations' option selected to locate associated animations](/Media/umodel_anim1.png)

After a short search, it will print the number of found animations for this SK.

![UModel preview panel showing number of animations found for the selected skeletal mesh after search](/Media/umodel_anim2.png)


### Basic Navigation
- LMB - Orbit around SK.
- RMB - Zoom in/out.
- `[` - Previous Animation.
- `]` - Next Animation.
- `Space` - Play current animation.

## Exporting Animations (.psa)
Using the FlatView search, type in the name of the animation, then right-click and Export.
![UModel FlatView search results: animation file highlighted, right-click menu open with Export option selected](/Media/umodel_anim3.png) <br>

The exported `.psa` file is a Skeletal Mesh(SK) animation that can be loaded into Blender using a plugin or/and used for modding.