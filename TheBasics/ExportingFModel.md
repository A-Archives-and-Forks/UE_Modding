# FModel
FModel is one of the best tools to browse, view and export all of the file types within the `.pak` file.
<br>
If your game has AES: [Adding AES](#adding-aes-key-optional).<br>
If your game has usmapping: [Adding mappings](#adding-usmapping-optional) _(mostly UE5+)_.

# Creating Game Preset
Launch the tool, Directory -> Selector.

FModel has presets for different games, so it will remember the PAK file and its settings.

To add a new one, simply expand the "Add Undetected Game".

![FModel Directory Selector window with 'Add Undetected Game' section expanded to create a new game preset](/Media/fmodel_1.png)

Next, give it a name and specify the path to the Paks folder of the game. For example:<br>
![FModel adding a new game preset: name field filled and Paks folder path selected via file browser](/Media/fmodel_2.png)<br>
And click the `+` button on the right to create a game preset.

Now you can pick the newly created profile and choose the correct UE4 version.
Once ready, click OK to begin.

And the next time you launch FModel, you just pick the game and click OK.
![FModel game preset selection dropdown showing the newly created game profile selected, ready to load with UE version chosen](/Media/fmodel_3.png)

## Adding AES key (optional)
If your game has AES encryption, navigate to Directory -> AES and input the AES to be able to read the PAK file.

![FModel AES key input dialog open under Directory menu, with AES key field ready for pasting the encryption key](/Media/fmodel_4.png)

## Adding USMapping (optional)
If your game has mapping (mostly UE5+), navigate to Settings, enable the "Local Mapping File", and provide the .usmap file for the game.

![FModel Settings window with 'Local Mapping File' enabled and path to .usmap file selected for UE5+ mapping support](/Media/fmodel_usmapping.png)

_Where can you get that `.usmap`? usually provided by modders_

# Browsing Game Files
That's the part where you have to start to explore and look around to find what you're looking for.

### Navigation Basics
![FModel main interface overview: Archives tab listing .pak files, Folders tab showing directory tree, and Packages tab displaying selected folder contents](/Media/fmodel_5.png) <br>

- Archives Tab: All available `.pak` files within the Paks folder.
- Folders Tab: The hierarchical structure of the `.pak`.
- Packages Tab: Files of the current selected folder.


### Exporting 
Exporting is simple, just right-click on the file(s) you want, and pick the right export type.
![FModel right-click context menu on a selected asset file, showing export options including .png for textures, .psk for meshes, .psa for animations, and Json](/Media/fmodel_6.png)<br>

<br>
Different asset types can be exported differently.<br>

- Zen `.uasset` such as blueprints, DataTables, Structs - export directly or Json **(Zen assets are incompatible with UAssetGUI, you can only edit with [hex editing](../BasicModding/HexEditing.md))**.
- Textures - as `.png`.
- Models such as StaticMesh or SkeletalMesh (characters) - `.psk`
- Animations - `.psa`


It doesn't have to be as exact, it really depends on the case and mod.
<br>
For example: exporting a skeletal mesh as `.uasset` to edit the used textures by changing the paths.

To repack a Zen uasset exported by FModel, you can use [UnrealReZen](../BasicModding/IoStorePacking.md).