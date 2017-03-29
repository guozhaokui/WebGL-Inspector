*   check TEXTURE_2D (need to add all new types)
    *   Texture.js:388
    *   background-image: url(assets/texture-3d.png);
    *   background-image: url(assets/texture-2d-array.png);
*   check SAMPLER_2D (need to check all new types)
*   handle more texImage functions
    *   texStorage2D
    *   texStorage3D
    *   texImage3D
    *   texSubImage3D
*   check
*   check binds
    *   vao
    *   sync
    *   fence
    *   transform feedback
*   check creates
    *   vao
    *   sync
    *   fence
    *   transform feedback

*   Handle samplers
*   Handle vertex arrays
*   Handle texture formats
*   Handle int attributes
*   Handle uniform block objects
*   Handle pixel store parameters
*   Make GL constants static
*   replay/RedundancyChecker
*   shared/info.js (lots of enums)
*   shared/utilties.js
    *   isWebGLResrouce
    *   getWebGLContext

*   fix style
    *   hightlghts are off
    *   there are gaps in areas

*   ui/Window.js
    *   UIType.Matrix line:406 (handle other types of matrixes)
    *   UIType.Object line:334 (handle new resource types)

*   resource/Texture.js guessSize (handle 3d, texStorage, copyTex)

## When adding a new resource

    *   bottom of core/host/ResourceCache.js
    *   core/host/Statistics.js - must be `lowercaseCount`
    *   ui/shared/TraceLine.js around line 265 and 550
    *   note that parts of the code assume names match as in
        `Buffer` -> `WebGLBuffer` -> `createBuffer` -> `deleteBuffer`
        but vertexArrays don't match as it's `WebGLVertexArrayObject`
        but it's `createVertexArray` and `deleteVertexArray`

## Need to fix

*   When I capture a long frame the list formatting gets out of sync.
    (http://webgl2fundamentals.org)

*   Figure out why inspector gets error on `generateMipmap`

## Things that might be nice to refactor

*   Switch Ids to per resource

    As it is resource ids are across all resources. Personally I'd
    find it much more useful to know this is the 3rd shader
    that was created rather than say the 79th if 78 non shader
    related resources were created first. When I see 79 I have
    no way to know which shader that is in my own code.

*   Merge VertexArray and vertexArrayObjectOES


