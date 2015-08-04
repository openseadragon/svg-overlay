# SVG Overlay for OpenSeadragon

An OpenSeadragon plugin that adds SVG overlay capability.

Compatible only with the new "Collections" branch of OpenSeadragon.

## Documentation

To use, include the `openseadragon-svg-overlay.js` file after `openseadragon.js` on your web page.

To add SVG overlay capability to your OpenSeadragon Viewer, call `svgOverlay()` on it. This will return a new object with the following methods:

* node(): Returns the SVG `g` element that you should add all of your SVG elements to. As the user zooms and pans, the `g` element will transform to match. Add your elements according to the OpenSeadragon Viewport coordinate system.
* resize(): If your viewer changes size, you'll need to resize the SVG overlay by calling this method.
* onClick(node, handler): If you want to accept click events on a sub-node, use this method. It takes care of making sure the click isn't also handled by the Viewer. The handler you provide is called when the click occurs and given a single argument, an [OpenSeadragon.MouseTracker click event](http://openseadragon.github.io/docs/OpenSeadragon.MouseTracker.html#clickHandler).

See demo.html for an example of it in use. You can see it in action at http://openseadragon.github.io/svg-overlay/demo.html.
