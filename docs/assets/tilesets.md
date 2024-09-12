# Tilesets

import { Swatch } from '@site/src/components/Swatch';

Tilesets are used to provide additional tiles that can be used by your scenes using the [Replace Tile](/docs/scripting/script-glossary/scene#tiles) events and to allow creating seamless scene transitions by using [Common Tilesets](/docs/project-editor/scenes#common-tilesets).

You can add tilesets to your game by including `.png` files in your project's `assets/tilesets` folder.

Replace Tile event uses GBVM function `VM_REPLACE_TILE_XY` whose variable `START_IDX` is clamped between 0 and 255. As such - don't make your tileset images more than 256 8x8px tiles otherwise it will loop back to 0 when finding your new tile.

## Color Requirements

Tileset PNGs must only contain the following four colors:

<Swatch color="#071821" />
<Swatch color="#306850" />
<Swatch color="#86c06c" />
<Swatch color="#e0f8cf" />

Download the GB Studio Palette Swatches for:  
[Adobe Photoshop](/assets/swatches/gb-studio-photoshop.aco)  
[Aseprite](/assets/swatches/gb-studio-aseprite.aseprite)  
[Piskel](/assets/swatches/gb-studio-piskel-background-palette.gpl)  

Colors that are not one of the above hex codes will be matched to the nearest color. Unlike sprites, the color `#65ff00` can not be used in tilesets.
