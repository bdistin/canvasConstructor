# Change Log
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/)
and this project adheres to [Semantic Versioning](http://semver.org/).

## 0.1.7
### Added
- `changeCanvasSize()` to change the canvas' width/height.
- `changeCanvasWidth()` to change the canvas' width.
- `changeCanvasHeigth()` to change the canvas' heigth.

### Removed
- `registerTextFont()` as canvas-constructor relies on Canvas 1.6.6, this method is useless.

## 0.1.6
### Added
- `setStrokeWidth()` to change stroke/line's width.
- `beginPath()` to start making paths.
- `closePath()` to start closing paths.
- `createLinearGradient()` to create linear gradients.
- `createRadialGradient()` to create radial gradients.
- `arc()` and `arcTo()`, to create arcs.
- `quadraticCurveTo()` to create quadratic Bèzier curves.
- `bezierCurveTo()` to create cubic Bèzier curves.
- `lineTo()` to connect lines.
- `moveTo()` to move the starting point of a path to any (x, y) coordinates.

### Changed
- Added default `'#000000'` for the `setStroke()` method.
- `addImage()` removed `this.save()` and `this.restore()` so users can use their own paths.

### Fixed
- Examples for `measureText()`.

## 0.1.5
### Added
- `save()` To save the current state onto a stack.
- `rotate()` To add a rotation to the transformation matrix.
- `scale()` To perform scaling transformations.
- `traslate()` To perform translating transformations.
- `fill()` To fill the current/given path.
- `stroke()` To stroke the current/given path.
- `addStrokeText()` To add stroked text.
- `measureText()` To measure in pixels a text. Be **careful**, if you do not
provide a callback (second argument), this method will return an Integer value
instead of being chainable.
- `setTextBaseline()` To set the text's baseline.
- `setShadowOffsetX()` To set the shadow offset for the axis X.
- `setShadowOffsetY()` To set the shadow offset for the axis Y.
- `setGlobalAlpha()` To set the global alpha value for the next elements.
- `clearCircle()` To clear the pixels with a circle shape.
- `clearPixels()` To clear the pixels with a rectangle shape. (Usage is
identical to `addRect()`).

### Changed
- **Breaking** | `fillRect()` -> `addRect()` | To keep consistency.
- `addText()` now accepts a third argument: `maxWidth`.
- `addImage()` now saves and restores the context.

### Fixed
- `addRoundImage()` now points to `addImage()` with the correct arguments.
- `addBevelImage()` now points to `addImage()` with the correct arguments.

## 0.1.4
### Changed
- Updated `README.md`.

## 0.1.3
### Fixed
- Fix a weird bug with the `in` operator in `addImage()`

## 0.1.0
### Added
- Added `addFont()` method for retrocompatibility with old versions of Canvas.
(Thanks to [York](https://github.com/YorkAARGH) in
[PR#1](https://github.com/kyranet/canvasConstructor/pull/1))

### Changed
- Better `README.md`.

### Fixed
- Bugs in the `options` argument for `addImage()`.
