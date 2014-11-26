MaterialColors
==============

**A Sass partial for all of Google's Material color palette.**

Liking the colors encouraged by Google's new design spec? It's pretty tough to remember any of those hex codes though. This Sass partial makes it easy though.

What it does mainly is take all of the colors from http://google.com/design/spec/style/colors.html and assigns them all to SCSS variables. Pretty simple stuff.


You can call them in two different ways:
```HTML5
<div class="foo red"></div>
```
or in SCSS
```SCSS
$[color]-[hue]

```

So for example, if I wanted use that neat blue-grey color, all I have to do is say:
```SCSS
$blue-grey-500
```
Or I could easily just add the "blue-grey" class to the element:
```HTML5
<div class="foo blue-grey"></div>
```
Then you can go up or down by using "lighten" or "darken":
```HTML5
<div class="foo blue-grey lighten-2"></div>
<div class="bar blue-grey darken-2"></div>
```

After moving the file into your project, just include it with a quick,
```SCSS
@include "material-colors";
```
==============
Coming up with good color palettes for Material apps is easy!

Just jam together about three different hues from one color palette and pair them with one accent color from a color's secondary palette (A100, A200, A400, A700). That's all there is too it.

