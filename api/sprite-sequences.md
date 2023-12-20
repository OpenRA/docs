# Sprite sequences

This documentation is aimed at modders and has been automatically generated for version `bleed` of OpenRA. Please do not edit it directly, but instead add new `[Desc("String")]` tags to the source code.

Listed below are all sprite sequence types with their properties and their default values plus developer commentary.
Related types with their possible values are listed [at the bottom](#related-value-types-enums).

## OpenRA.Mods.Cnc.Graphics

### ClassicSpriteSequence
**A sprite sequence that has the oddities that come with first-generation Westwood titles.**

> Inherits from: [`DefaultSpriteSequence`](#defaultspritesequence).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| UseClassicFacings | False | Boolean | Incorporate a compensation factor for the rotational distortion present in the first-generation Westwood games. |

### ClassicTilesetSpecificSpriteSequence
**A sprite sequence that can have tileset-specific variants and has the oddities that come with first-generation Westwood titles.**

> Inherits from: [`ClassicSpriteSequence`](#classicspritesequence), [`DefaultSpriteSequence`](#defaultspritesequence).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| TilesetFilenames |  | Dictionary with Key: String, Value: String | Dictionary of <tileset name>: filename to override the Filename key. |
| TilesetFilenamesPattern |  | Dictionary with Key: String, Value: String | Dictionary of <tileset name>: <filename pattern> to override the FilenamePattern key. |

### D2kSpriteSequence
**A sprite sequence that understands how to apply colour remapping to D2k sprites.**

> Inherits from: [`DefaultSpriteSequence`](#defaultspritesequence).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Remap | 00000000 | Color (RRGGBB[AA] notation) | Sets the player remap reference colour. |
| UseShadow | True | Boolean | Remap embedded palette index 1 to shadow. |
| ConvertShroudToFog | False | Boolean | Indicates that this is a fog sprite definition. |

## OpenRA.Mods.Common.Graphics

### DefaultSpriteSequence
**Generic sprite sequence implementation, mostly unencumbered with game- or artwork-specific logic.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Filename |  | String | File name of the sprite to use for this sequence. |
| FilenamePattern |  | String | File name pattern to build the sprite to use for this sequence. |
| Start | 0 | Integer | Frame index to start from. |
| Length | 1 | Integer | Number of frames to use. Does not have to be the total amount the sprite sheet has. |
| Stride | -1 | Integer | Overrides Length if a different number of frames is defined between facings. |
| Facings | 1 | Integer | The number of facings that are provided by sprite frames. Use negative values to rotate counter-clockwise. |
| InterpolatedFacings |  | Integer (optional) | The total number of facings for the sequence. If >Facings, the closest facing sprite will be rotated to match. Use negative values to rotate counter-clockwise. |
| Tick | 40 | Integer | Time (in milliseconds at default game speed) to wait until playing the next frame in the animation. |
| ZOffset | 0c0 | 1D World Distance | Value controlling the Z-order. A higher values means rendering on top of other sprites at the same position. Use power of 2 values to avoid glitches. |
| ZRamp | 0 | Integer | Additional sprite depth Z offset to apply as a function of sprite Y (0: vertical, 1: flat on terrain) |
| ShadowStart | -1 | Integer | If the shadow is not part of the sprite, but baked into the same sprite sheet at a fixed offset, set this to the frame index where it starts. |
| ShadowZOffset | -0c5 | 1D World Distance | Set Z-Offset for the separate shadow. Used by the later Westwood 2.5D titles. |
| Frames |  | Collection of Integer | The individual frames to play instead of going through them sequentially from the `Start`. |
| IgnoreWorldTint | False | Boolean | Don't apply terrain lighting or colored overlays. |
| Scale | 1 | Real Number | Adjusts the rendered size of the sprite |
| Reverses | False | Boolean | Play the sprite sequence back and forth. |
| Transpose | False | Boolean | Support a frame order where each animation step is split per each direction. |
| FlipX | False | Boolean | Mirror on the X axis. |
| FlipY | False | Boolean | Mirror on the Y axis. |
| Offset | 0,0,0 | float3 | Change the position in-game on X, Y, Z. |
| BlendMode | Alpha | [`BlendMode`](#blendmode) | Apply an OpenGL/Photoshop inspired blend mode. |
| Combine |  | MiniYaml | Create a virtual sprite file by concatenating one or more frames from multiple files, with optional transformations applied. All defined frames will be loaded into memory, even if unused, so use this property with care. |
| Alpha |  | Collection of Real Number | Sets transparency - use one value to set for all frames or provide a value for each frame. |
| AlphaFade | False | Boolean | Fade the animation from fully opaque on the first frame to fully transparent after the last frame. |
| DepthSprite |  | String | Name of the file containing the depth data sprite. |
| DepthSpriteFrame | 0 | Integer | Frame index containing the depth data. |
| DepthSpriteOffset | 0,0 | 2D Real Number | X, Y offset to apply to the depth sprite. |

### TilesetSpecificSpriteSequence
**A sprite sequence that can have tileset-specific variants.**

> Inherits from: [`DefaultSpriteSequence`](#defaultspritesequence).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| TilesetFilenames |  | Dictionary with Key: String, Value: String | Dictionary of <tileset name>: filename to override the Filename key. |
| TilesetFilenamesPattern |  | Dictionary with Key: String, Value: String | Dictionary of <tileset name>: <filename pattern> to override the FilenamePattern key. |

# Related value types (enums):

### BlendMode
Possible values: `None`, `Alpha`, `Additive`, `Subtractive`, `Multiply`, `Multiplicative`, `DoubleMultiplicative`, `LowAdditive`, `Screen`, `Translucent`

Referenced by: [`DefaultSpriteSequence`](#defaultspritesequence)

