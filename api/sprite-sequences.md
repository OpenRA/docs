# Sprite sequences

This documentation is aimed at modders and has been automatically generated for version `bleed` of OpenRA. Please do not edit it directly, but instead add new `[Desc("String")]` tags to the source code.

Listed below are all sprite sequence types with their properties and their default values plus developer commentary.
Related types with their possible values are listed [at the bottom](#related-value-types-enums).

## OpenRA.Mods.Cnc.Graphics

### ClassicSpriteSequence
**A sprite sequence that has the oddities that come with first-generation Westwood titles. [GitHub](https://github.com/OpenRA/OpenRA/blob/bleed/OpenRA.Mods.Cnc/Graphics/ClassicSpriteSequence.cs)**

> Inherits from: [`DefaultSpriteSequence`](#defaultspritesequence).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| None |  | Boolean | Incorporate a compensation factor for the rotational distortion present in the first-generation Westwood games. |

### ClassicTilesetSpecificSpriteSequence
**A sprite sequence that can have tileset-specific variants and has the oddities that come with first-generation Westwood titles. [GitHub](https://github.com/OpenRA/OpenRA/blob/bleed/OpenRA.Mods.Cnc/Graphics/ClassicTilesetSpecificSpriteSequence.cs)**

> Inherits from: [`ClassicSpriteSequence`](#classicspritesequence), [`DefaultSpriteSequence`](#defaultspritesequence).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| None |  | Dictionary with Key: String, Value: String | Dictionary of <tileset name>: filename to override the Filename key. |
| None |  | Dictionary with Key: String, Value: String | Dictionary of <tileset name>: <filename pattern> to override the FilenamePattern key. |

## OpenRA.Mods.Common.Graphics

### DefaultSpriteSequence
**Generic sprite sequence implementation, mostly unencumbered with game- or artwork-specific logic. [GitHub](https://github.com/OpenRA/OpenRA/blob/bleed/OpenRA.Mods.Common/Graphics/DefaultSpriteSequence.cs)**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| None |  | String | File name of the sprite to use for this sequence. |
| None |  | String | File name pattern to build the sprite to use for this sequence. |
| None |  | Integer | Frame index to start from. |
| None |  | Integer | Number of frames to use. Does not have to be the total amount the sprite sheet has. |
| None |  | Integer | Overrides Length if a different number of frames is defined between facings. |
| None |  | Integer | The number of facings that are provided by sprite frames. Use negative values to rotate counter-clockwise. |
| None |  | Integer (optional) | The total number of facings for the sequence. If >Facings, the closest facing sprite will be rotated to match. Use negative values to rotate counter-clockwise. |
| None |  | Integer | Time (in milliseconds at default game speed) to wait until playing the next frame in the animation. |
| None |  | 1D World Distance | Value controlling the Z-order. A higher values means rendering on top of other sprites at the same position. Use power of 2 values to avoid glitches. |
| None |  | Integer | Additional sprite depth Z offset to apply as a function of sprite Y (0: vertical, 1: flat on terrain) |
| None |  | Integer | If the shadow is not part of the sprite, but baked into the same sprite sheet at a fixed offset, set this to the frame index where it starts. |
| None |  | 1D World Distance | Set Z-Offset for the separate shadow. Used by the later Westwood 2.5D titles. |
| None |  | Collection of Integer | The individual frames to play instead of going through them sequentially from the `Start`. |
| None |  | Boolean | Don't apply terrain lighting or colored overlays. |
| None |  | Real Number | Adjusts the rendered size of the sprite |
| None |  | Boolean | Play the sprite sequence back and forth. |
| None |  | Boolean | Support a frame order where each animation step is split per each direction. |
| None |  | Boolean | Mirror on the X axis. |
| None |  | Boolean | Mirror on the Y axis. |
| None |  | float3 | Change the position in-game on X, Y, Z. |
| None |  | BlendMode (enum) | Apply an OpenGL/Photoshop inspired blend mode. |
| None |  | MiniYaml | Create a virtual sprite file by concatenating one or more frames from multiple files, with optional transformations applied. All defined frames will be loaded into memory, even if unused, so use this property with care. |
| None |  | Collection of Real Number | Sets transparency - use one value to set for all frames or provide a value for each frame. |
| None |  | Boolean | Fade the animation from fully opaque on the first frame to fully transparent after the last frame. |
| None |  | String | Name of the file containing the depth data sprite. |
| None |  | Integer | Frame index containing the depth data. |
| None |  | 2D Real Number | X, Y offset to apply to the depth sprite. |

### TilesetSpecificSpriteSequence
**A sprite sequence that can have tileset-specific variants. [GitHub](https://github.com/OpenRA/OpenRA/blob/bleed/OpenRA.Mods.Common/Graphics/TilesetSpecificSpriteSequence.cs)**

> Inherits from: [`DefaultSpriteSequence`](#defaultspritesequence).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| None |  | Dictionary with Key: String, Value: String | Dictionary of <tileset name>: filename to override the Filename key. |
| None |  | Dictionary with Key: String, Value: String | Dictionary of <tileset name>: <filename pattern> to override the FilenamePattern key. |

## OpenRA.Mods.D2k.Graphics

### D2kSpriteSequence
**A sprite sequence that understands how to apply colour remapping to D2k sprites. [GitHub](https://github.com/OpenRA/OpenRA/blob/bleed/OpenRA.Mods.D2k/Graphics/D2kSpriteSequence.cs)**

> Inherits from: [`DefaultSpriteSequence`](#defaultspritesequence).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| None |  | Color (RRGGBB[AA] notation) | Sets the player remap reference colour. |
| None |  | Boolean | Remap embedded palette index 1 to shadow. |
| None |  | Boolean | Indicates that this is a fog sprite definition. |
