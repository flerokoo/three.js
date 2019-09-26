three.js
========

<<<<<<< HEAD
<br/>
=======
[![NPM package][npm]][npm-url]
[![Build Size][build-size]][build-size-url]
[![Build Status][build-status]][build-status-url]
[![Dependencies][dependencies]][dependencies-url]
[![Dev Dependencies][dev-dependencies]][dev-dependencies-url]
[![Language Grade][lgtm]][lgtm-url]
>>>>>>> 7e0a78beb9317e580d7fa4da9b5b12be051c6feb

## Changes from regular version

<<<<<<< HEAD
### WebGLRenderer

_WebGLRenderer.render()_  
Removed `WebVRManager.submitFrame()` call at the end of `WebGLRenderer.render()`. This change allows rendering multiple scenes from multiple cameras in VR (but don't forget to call `WebVRManager.submitFrame()` after all your scenes are rendered).
=======
The aim of the project is to create an easy to use, lightweight, 3D library with a default WebGL renderer. The library also provides Canvas 2D, SVG and CSS3D renderers in the examples.

[Examples](http://threejs.org/examples/) &mdash;
[Documentation](http://threejs.org/docs/) &mdash;
[Wiki](https://github.com/mrdoob/three.js/wiki) &mdash;
[Migrating](https://github.com/mrdoob/three.js/wiki/Migration-Guide) &mdash;
[Questions](http://stackoverflow.com/questions/tagged/three.js) &mdash;
[Forum](https://discourse.threejs.org/) &mdash;
[Gitter](https://gitter.im/mrdoob/three.js) &mdash;
[Slack](https://join.slack.com/t/threejs/shared_invite/enQtMzYxMzczODM2OTgxLTQ1YmY4YTQxOTFjNDAzYmQ4NjU2YzRhNzliY2RiNDEyYjU2MjhhODgyYWQ5Y2MyZTU3MWNkOGVmOGRhOTQzYTk)
>>>>>>> 7e0a78beb9317e580d7fa4da9b5b12be051c6feb

_WebGLRenderer.renderStates_ exposed

<<<<<<< HEAD

  
### WebVRManager
=======
Download the [minified library](http://threejs.org/build/three.min.js) and include it in your HTML, or install and import it as a [module](http://threejs.org/docs/#manual/introduction/Import-via-modules),
Alternatively, see [how to build the library yourself](https://github.com/mrdoob/three.js/wiki/Build-instructions).

```html
<script src="js/three.min.js"></script>
```

This code creates a scene, a camera, and a geometric cube, and it adds the cube to the scene. It then creates a `WebGL` renderer for the scene and camera, and it adds that viewport to the `document.body` element. Finally, it animates the cube within the scene for the camera.

```javascript
var camera, scene, renderer;
var geometry, material, mesh;

init();
animate();

function init() {

	camera = new THREE.PerspectiveCamera( 70, window.innerWidth / window.innerHeight, 0.01, 10 );
	camera.position.z = 1;

	scene = new THREE.Scene();
>>>>>>> 7e0a78beb9317e580d7fa4da9b5b12be051c6feb

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

<<<<<<< HEAD
`onFrameEnter` callback added
=======
[npm]: https://img.shields.io/npm/v/three.svg
[npm-url]: https://www.npmjs.com/package/three
[build-size]: https://badgen.net/bundlephobia/minzip/three
[build-size-url]: https://bundlephobia.com/result?p=three
[build-status]: https://travis-ci.org/mrdoob/three.js.svg?branch=dev
[build-status-url]: https://travis-ci.org/mrdoob/three.js
[dependencies]: https://img.shields.io/david/mrdoob/three.js.svg
[dependencies-url]: https://david-dm.org/mrdoob/three.js
[dev-dependencies]: https://img.shields.io/david/dev/mrdoob/three.js.svg
[dev-dependencies-url]: https://david-dm.org/mrdoob/three.js#info=devDependencies
[lgtm]: https://img.shields.io/lgtm/grade/javascript/g/mrdoob/three.js.svg?label=code%20quality
[lgtm-url]: https://lgtm.com/projects/g/mrdoob/three.js/
>>>>>>> 7e0a78beb9317e580d7fa4da9b5b12be051c6feb
