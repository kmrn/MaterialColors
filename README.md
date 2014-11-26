MaterialColors
==============

**A Sass partial for all of Google's Material color palette.**

##[Here's a working demo.](http://ron953.github.io/MaterialColors/)


Liking the colors encouraged by Google's new design spec? It's pretty tough to remember any of those hex codes though. This Sass partial makes it easy though.

What it does mainly is take all of the colors from http://google.com/design/spec/style/color.html and assigns them all to SCSS variables and classes. Pretty simple stuff.


You can call them in two different ways:
```HTML
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
Or I could easily just add the `blue-grey` class to the element:
```HTML
<div class="foo blue-grey"></div>
```
Then you can go up or down by using `lighten` or `darken`:
```HTML
<div class="foo blue-grey lighten-2"></div>
<div class="bar blue-grey darken-2"></div>
```

The HTML method applies the background-color property to an element. If you're trying to apply the color to text (use sparingly, it doesn't really fit with the Material theme) just add `-text` to the end of the color's name.
```HTML
<div class="foo orange-text"></div>
```

After moving the file into your project, just include it with a quick,
```SCSS
@include "material-colors";
```
==============
Coming up with good color palettes for Material apps is easy!

Just jam together about three different hues from one color palette and pair them with one accent color from a color's secondary palette (A100, A200, A400, A700). That's all there is too it.

Here's a nice example color palette for an app:

```HTML
<!-- Primary Color Palette -->
<div class="foo indigo"></div>
<div class="bar indigo lighten-4"></div>
<div class="baz indigo darken-2"></div>

<!-- Accent Color -->
<div class="accent pink lighten-1"></div>
```
While the above isn't **technically** correct regarding Material, it's easier to implement, is a little more elegant, and is pretty close anyways. If you want to get exact, you can always just use the SCSS variables:

```SCSS
//Primary Color Palette
.foo { background-color: $indigo-500; }
.bar { background-color: $indigo-100; }
.baz { background-color: $indigo-700; }

//Accent Color
.accent { background-color: $pink-A200; }
```

It's really up to you which way you want to go with that.