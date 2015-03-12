# What is this library for? #
This Javascript library implements the three methods to draw text on **HTML5 `<canvas>` tags** ([strokeText](http://www.whatwg.org/specs/web-apps/current-work/multipage/the-canvas-element.html#dom-context-2d-stroketext), [fillText](http://www.whatwg.org/specs/web-apps/current-work/multipage/the-canvas-element.html#dom-context-2d-filltext) and [measureText](http://www.whatwg.org/specs/web-apps/current-work/multipage/the-canvas-element.html#dom-context-2d-measuretext)) to the browsers which don't already have it (Firefox 2/3.0, Internet Explorer 6+, Opera 9+, Safari 3.x, Chrome 1.0).

The main goal of this implementation is to respect the specs given by the W3C and WHATWG for the HTML5 `<canvas>` tag.

It doesn't change the already implemented functions in Firefox 3.5+, Safari 4 and Chrome 2+ and doesn't require any other library except [ExCanvas](http://code.google.com/p/explorercanvas/) for Internet Explorer.

This project is partially based on the work of David Chester in his project [typeface.js](http://typeface.neocracy.org/).

# Can I see it in action ? #
You can see the **[live DEMO here](http://canvas-text.googlecode.com/svn/trunk/examples/index.html)**.

# How to use it ? #
Simply include the `canvas.text.js` in the head tag and place the font face files on your server, in the folder `faces/` in the directory of `canvas.text.js`. They must be named `family-weight-style.js`, you can find such files [here](http://typeface.neocracy.org/fonts.html) or [here](http://www.madasplayground.com/fonts/). For example, a correct file name for the _Times New Roman Bold Italic_ font would be `times_new_roman-bold-italic.js`.

You can also include them in the head, after `canvas.text.js`, but in this case they will be downloaded even if the browser already supports text methods. The browsers that have built-in text functions won't use the font face files, they will use the client's fonts.

If you want more options, go to the QuickStart guide.

<table width='100%'><tr>
<td align='center'><a href='http://canvas-text.googlecode.com/svn/trunk/examples/index.html'><img src='http://canvas-text.googlecode.com/svn/images/transformations.png' /></a></td>
<td width='280'></td>
</tr></table>