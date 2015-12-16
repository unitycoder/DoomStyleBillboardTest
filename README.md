# DoomStyleBillboardTest
Shader to display camera facing billboard, with different texture based on player position angle

*Nothing to do with actual Doom game, havent checked how the sprites are drawn there

## Website
http://unitycoder.com/blog/2015/04/06/doom-style-billboard-shader/

## Whats new

Optimized original DoomSprite1.shader into DoomSprite2.shader.
Moved all the code into vertex shader and into precalculated defines.

```
BEFORE (v1)
 // Stats for Vertex shader:
 //       d3d11 : 25 math
 //    d3d11_9x : 25 math
 //        d3d9 : 47 math
 // Stats for Fragment shader:
 //       d3d11 : 38 math, 1 texture
 //    d3d11_9x : 38 math, 1 texture
 //        d3d9 : 49 math, 1 texture
 
 AFTER (v2)
  // Stats for Vertex shader:
 //       d3d11 : 52 math
 //    d3d11_9x : 52 math
 //        d3d9 : 82 math
 // Stats for Fragment shader:
 //       d3d11 : 0 math, 1 texture
 //    d3d11_9x : 0 math, 1 texture
 //        d3d9 : 1 math, 1 texture
 
 AFTER (v3)
  // Stats for Vertex shader:
 //       d3d11 : 44 math
 //    d3d11_9x : 44 math
 //        d3d9 : 71 math
 // Stats for Fragment shader:
 //       d3d11 : 0 math, 1 texture
 //    d3d11_9x : 0 math, 1 texture
 //        d3d9 : 1 math, 1 texture
```

## Preview
![gif](https://raw.githubusercontent.com/unitycoder/GitImageDump/master/gifs/doom_billboard_sprites.gif)

