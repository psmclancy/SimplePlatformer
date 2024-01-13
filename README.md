# SimplePlatformer
A minimal platformer showing basic Godot use

*Current version Godot 4.2.1*

## Setup

* [Download Godot 4.2.1-stable](https://godotengine.org/download/archive/) (App is portable, no install)
* Clone this repo to wherever you want to work out of
* Launch Godot, in project manager select "scan" and navigate to the repository you cloned in the last step
* If everything worked properly you should now be able to double click the project and launch the editor
  * In the editor you should be able to hit `f5` and have the game launch the `level_01` scene which is set to default
 
# Repository Structure

**_NOTE:_** In Godot, `res://` refers to the 'home' directory, in the case the `SimplePlatformer` directory.\

### res://Content/
  * For most non text-based assets ie. images, 3d models, audio files etc.
  * Separating assets into this folder hurts modularity, but is important long term in case binaries are stored/version controlled with a different method than text/"Source" files. At some point binaries may be included that can't be handled by standard git.
  * Intended just for assets used in game, not DCC files like Photoshop .PSDs, .blend etc. just their outputs like .pngs, .gltf
  * As the project is currently only using git/github **do not put files larger than 100mb here**. Use a lower resolution, more compression etc. If it's absolutely essential to use a file over the size limit, the project needs a restructuring.
### res://Documentation
  * For plain-text files documenting the project (default to markdown). Only use images already used in-game or linked, externally hosted images rather than including new image files just for documentation, to avoid bloating project size. Avoid images where possible to avoid dependancies.
### res://Source
  * For most text based files ie. scene files (.tscn), gdscript (.gd), resources (.tres) etc.
  * Source is dependant on assets from content, so where possible - structure it in a way that's laid out and named the same as its related Content directories/files
    * ie. `res://Content/Player/player_sprite.png` and `res://Source/Player/player_sprite.png` 
