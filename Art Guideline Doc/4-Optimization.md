## Optimization

### MESHES/MODELS

Meshes are made up of flat surfaces called polygons. 
Polygons are what is rendered to the screen.

#### Triangulation

Polygon counts in Unity are always measured in tris (triangular faces), and Unity will split any imported model into tris.
Unity may not do this very well, in which case you may have to triangulate the mesh yourself.

**NOTE**: Triangulated models are harder to edit, so save an un-triangulated copy first.

#### Polycount

To avoid performance problems, limit the scene's overall polygon count by making the assets as efficiently as possible. 
The target polycount of an asset will change depending on size, distance, and importance.

##### Recommended Polycounts:
- **Small/Distant/Tertiary Props** \= 100-300 tris
- **Medium/Secondary Props** \= 400-800 tris
- **Large/Close/Hero Props** \= 900-1500 tris

#### LOD (Level Of Detail)

Objects that are close to the camera at times and far away at others should use LODs. 
For example, a hero object with 1200 tris may have a 600 tri version for the middle distance, a 150 tri version for the far distance, and a flat 2D version for extreme distances.

### TEXTURES AND OTHER IMAGES

Images usually represent a game’s largest memory hog. 
For this reason, images must be optimized.

#### Square, Power of 2

All images used in a game need to be **square, with pixel dimensions in powers of 2**. 
In other words, 2x2, 4x4, 8x8, 16x16, 32x32, and so on (doubles each time).

##### Size Recommendations:
- **32x32** - When using a solid color, it’s possible to go very small; 32x32 is fine.
- **64x64** - When using color indexes, 64 pixels is the smallest recommended size.
- **128x128, 256x256, 512x512** - Most textures should be one of these sizes unless they are very detailed.
- **1024x1024, 2048x2048** - These sizes are often referred to as 1K and 2K, respectively. 1K images are helpful for highly detailed textures. Generally, 2K images should only be used with atlases and exceptionally detailed textures.

Additionally, images can be sized relative to each other based on how large they appear on the screen. 
For example, if one image is 1024px in width and spans the screen, and another image spans only halfway across the screen, there is no reason for it to be larger than 512px.

#### Texture Atlases

UI elements and decals are often unusual shapes and rarely fit easily into a square, power of two texture. 
For this reason, Unity’s atlas feature should be used. 
This leads to larger images, but it can significantly reduce draw calls, as many images can be loaded in one atlas file.
