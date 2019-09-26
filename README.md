three.js
========

<br/>

## Changes from regular version

### WebGLRenderer

_WebGLRenderer.render()_  
Removed `WebVRManager.submitFrame()` call at the end of `WebGLRenderer.render()`. This change allows rendering multiple scenes from multiple cameras in VR (but don't forget to call `WebVRManager.submitFrame()` after all your scenes are rendered).

_WebGLRenderer.renderStates_ exposed


  
### WebVRManager

_WebVRManager.minRenderWidth_  
Added `minRenderWidth` property to WebVRManager. It allows to specify minimum render buffer width. When `eyeParameters.renderWidth` is less than `minRenderWidth`, `minRenderWidth` will be used instead. Render buffer height will change accordingly, keeping aspect ratio the same.


### WebGLState

_buffers.depth_
Added `overrideDepthFunc`, `overrideDepthMask` and `overrideDepthTest` properties. These values have higher priority that material's `depthFunc`, `depthWrite` and `depthTest`.

```js
renderer.state.buffers.depth.overrideDepthTest = false; // all objects will be rendered as if their material.depthTest === false
renderer.state.buffers.depth.overrideDepthTest = null; // all objects will be rendered by default (based on material settings)
```

### Object3D

`onFrameEnter` callback added
