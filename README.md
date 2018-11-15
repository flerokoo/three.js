three.js
========

<br/>

## Changes from regular version

### WebGLRenderer

_WebGLRenderer.render()_  
Removed `WebVRManager.submitFrame()` call at the end of `WebGLRenderer.render()`. This change allows rendering multiple scenes from multiple cameras in VR (but don't forget to call `WebVRManager.submitFrame()` after all your scenes are rendered).

  
### WebVRManager

_WebVRManager.minRenderWidth_  
Added `minRenderWidth` property to WebVRManager. It allows to specify minimum render buffer width. When `eyeParameters.renderWidth` is less than `minRenderWidth`, `minRenderWidth` will be used instead. Render buffer height will change accordingly, keeping aspect ratio the same.
