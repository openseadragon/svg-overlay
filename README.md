# SVG Overlay for OpenSeadragon

An OpenSeadragon plugin that adds SVG overlay capability.

Compatible only with the new "Collections" branch of OpenSeadragon.

## Documentation

To use, include the `openseadragon-svg-overlay.js` file after `openseadragon.js` on your web page.

To add SVG overlay capability to your OpenSeadragon Viewer, call `svgOverlay()` on it. This will return the SVG `g` element that you should add all of your SVG elements to. As the user zooms and pans, the `g` element will transform to match. Add your elements according to the OpenSeadragon Viewport coordinate system.

Note that if you want to be able to receive events on any of the SVG elements you add, you'll need to set their `pointer-events` property accordingly. Using a value of `'fill'` seems to work nicely.

If your viewer changes size, you'll need to resize the SVG overlay by calling `svgOverlay('resize')` on your Viewer.

See demo.html for an example of it in use.
