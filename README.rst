jQuery SVG with svgweb support
==============================

This is a fork of Keith Wood's excellent jQuery SVG plugin, originally here:

http://keith-wood.name/svg.html

It now checks for the presence of Google's svgweb Flash SVG emulator, found here:

http://code.google.com/p/svgweb/

and uses it in browsers that don't have native SVG support. It doesn't depend
strictly on svgweb, and will continue to behave as before if it's not present;
it will just use it if it's available. A few specifics:

* It honors svgweb's mechanisms for forcing Flash rendering on all browsers via
  GET parameter or "meta" tag; see the corresponding svgweb documentation.
* If you do use svgweb and want scripts to work in IE, you have to use the
  window.onsvgload event instead of the usually DOM load event, as specified in
  the svgweb docs.
* I haven't heavily tested this, yet. It may break.