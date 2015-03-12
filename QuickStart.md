This library is intended to be very simple, but you can customize it a little bit if you want so.

## Include the right files ##
For this library to work the best it can, you'll need 3 files :
  * The library itself
  * The ExCanvas library if you want it to be available to Internet Explorer 6+ users
  * At least one font face file: they contain the font glyphs coordinates. They can be found [on the typeface.js website](http://typeface.neocracy.org/) or [here (lots of fonts !)](http://www.madasplayground.com/fonts/).

```
<!--[if IE]><script type="text/javascript" src="excanvas.js"></script><![endif]-->
<script type="text/javascript" src="canvas.text.js"></script>
```
The Canvas text library file **MUST** be named _canvas.text.js_. In the future, that could be changed, but this is very important as of now.

The third dependency is related to the font family/weight/style you'll want to use on the canvas element. The font face files can be included the same way the other files are, but need to be after canvas.text.js.

The needed face files will be downloaded when needed via Ajax and parsed on the fly. For this to work, these files must respect a convention :
  * lower case letters
  * must respect this format : `family-weight-style.js` where _face_ is the font family, like _Arial_ or _Times new roman_, _weight_ is the font weight (bold or normal), _style_ is the font style (italic or normal)
  * the spaces in the font family name must be replaced by underscores (`_`)
  * be placed in the `faces` folder next to the canvas.text.js file.

## Options ##
The implementation can be customized thanks to a few options :
  * "reimplement": override the built-in text functions by the ones provided by the lib.
  * "dontUseMoz": don't use the Mozilla text functions in Firefox 3.0.
  * "fallbackCharacter": the character used when a character is not in the font face file.
  * "debug": used when debugging, it does nothing for now.

These options can be defined by adding HTTP params to the `canvas.text.js` include:
```
<script type="text/javascript" src="canvas.text.js?reimplement=true&debug=true"></script>
```

## Use the text functions ##
Now the libraries are included, the only thing you have to do is to use the text functions, as they are specified on the [WHATWG specification page](http://www.whatwg.org/specs/web-apps/current-work/multipage/the-canvas-element.html#text).