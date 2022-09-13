This documentation is aimed at modders and has been automatically generated for version `dev-20220913` of OpenRA. Please do not edit it directly, but instead add new `[Desc("String")]` tags to the source code.

Listed below are all sprite sequence types with their properties and their default values plus developer commentary.
Related types with their possible values are listed [at the bottom](#related-value-types-enums).

# Sprite sequences:

## OpenRA.Mods.Cnc.Graphics

### ClassicSpriteSequence
**A sprite sequence that has the oddities that come with first-generation Westwood titles.**
###### Inherits from: [`DefaultSpriteSequence`](#defaultspritesequence).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| UseClassicFacings | False | Boolean | Incorporate a compensation factor for the rotational distortion present in the first-generation Westwood games. |

### ClassicTilesetSpecificSpriteSequence
**A sprite sequence that can have tileset-specific variants and has the oddities that come with first-generation Westwood titles.**
###### Inherits from: [`ClassicSpriteSequence`](#classicspritesequence), [`DefaultSpriteSequence`](#defaultspritesequence).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| TilesetOverrides |  | Dictionary with Key: String, Value: String | Dictionary of <string: string> with tileset name to override -> tileset name to use instead. |
| UseTilesetCode | False | Boolean | Use `TilesetCodes` as defined in `mod.yaml` to add a letter as a second character into the sprite filename like the Westwood 2.5D titles did for tileset-specific variants. |
| AddExtension | True | Boolean | Append a tileset-specific extension to the file name - either as defined in `mod.yaml`'s `TilesetExtensions` (if `UseTilesetExtension` is used) or the default hardcoded one for this sequence type (.shp). |
| UseTilesetExtension | False | Boolean | Whether `mod.yaml`'s `TilesetExtensions` should be used with the sequence's file name. |

## OpenRA.Mods.Common.Graphics

### DefaultSpriteSequence
**Generic sprite sequence implementation, mostly unencumbered with game- or artwork-specific logic.**

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| Start | 0 | Integer | Frame index to start from. |
| Length | 1 | Integer | Number of frames to use. Does not have to be the total amount the sprite sheet has. |
| Stride | -1 | Integer | Overrides Length if a different number of frames is defined between facings. |
| Facings | 1 | Integer | The amount of directions the unit faces. Use negative values to rotate counter-clockwise. |
| InterpolatedFacings | 1 | Integer | The amount of directions the unit faces. Use negative values to rotate counter-clockwise. |
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
| Combine |  | MiniYaml | Allows to append multiple sequence definitions which are indented below this node like when offsets differ per frame or a sequence is spread across individual files. |
| Alpha |  | Collection of Real Number | Sets transparency - use one value to set for all frames or provide a value for each frame. |
| AlphaFade | False | Boolean | Fade the animation from fully opaque on the first frame to fully transparent after the last frame. |
| DepthSprite |  | String | Name of the file containing the depth data sprite. |
| DepthSpriteFrame | 0 | Integer | Frame index containing the depth data. |
| DepthSpriteOffset | 0,0 | 2D Real Number | X, Y offset to apply to the depth sprite. |
| HasEmbeddedPalette | False | Boolean | Make a custom palette embedded in the sprite available to the PaletteFromEmbeddedSpritePalette trait. |

### TilesetSpecificSpriteSequence
**A sprite sequence that can have tileset-specific variants.**
###### Inherits from: [`DefaultSpriteSequence`](#defaultspritesequence).

| Property | Default Value | Type | Description |
| -------- | ------------- | ---- | ----------- |
| TilesetOverrides |  | Dictionary with Key: String, Value: String | Dictionary of <string: string> with tileset name to override -> tileset name to use instead. |
| UseTilesetCode | False | Boolean | Use `TilesetCodes` as defined in `mod.yaml` to add a letter as a second character into the sprite filename like the Westwood 2.5D titles did for tileset-specific variants. |
| AddExtension | True | Boolean | Append a tileset-specific extension to the file name - either as defined in `mod.yaml`'s `TilesetExtensions` (if `UseTilesetExtension` is used) or the default hardcoded one for this sequence type (.shp). |
| UseTilesetExtension | False | Boolean | Whether `mod.yaml`'s `TilesetExtensions` should be used with the sequence's file name. |

# Related value types (enums):

### BlendMode
Possible values: `None`, `Alpha`, `Additive`, `Subtractive`, `Multiply`, `Multiplicative`, `DoubleMultiplicative`, `LowAdditive`, `Screen`, `Translucent`

Referenced by: [`DefaultSpriteSequence`](#defaultspritesequence)

