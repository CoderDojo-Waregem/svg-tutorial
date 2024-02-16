Let’s start with a simple Christmas ornament. 

<div class="dodona-centered-group">
<figure>
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="20" r="70" fill="#D1495B" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257" />
  <circle cx="0" cy="-75" r="12" fill="none" stroke="#F79257" stroke-width="2" />
</svg>
</figure>
</div>

Here we only use simple shapes, a rectangle, and two circles. Note, that the origin of the coordinate system is in the center of the image.

First, we define the main part of the Christmas ornament, by drawing a `circle`. To draw a circle we set their center position (`cx` and `cy`) and the radius with the `r` property.

We also have presentational attributes that style our shapes. Similar to the `background-color` property in CSS, we set the color for the shape with the `fill` attribute.

```html
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <circle cx="0" cy="20" r="70" fill="#D1495B" />
</svg>
```

<div class="dodona-centered-group">
<figure>
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="20" r="70" fill="#D1495B" />
</svg>
</figure>
</div>

Then we draw a rectangle as a little cap on top of the Christmas ornament with the `rect` element. In this case, we have to set the top-left position of the rectangle and its size. We use the `fill` attribute the same way as we did with the circle.

```html
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <circle cx="0" cy="20" r="70" fill="#D1495B" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257" />
</svg>
```

<div class="dodona-centered-group">
<figure>
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="20" r="70" fill="#D1495B" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257" />
</svg>
</figure>
</div>

Finally, we add another circle as a hanger on top of these. Note that we use the same `circle` element, but with different attributes. We set the fill property to `"none"` and set a border for the shape with the `stroke` and `stroke-width` properties.

The final code of the image is as follows:

```html
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <circle cx="0" cy="20" r="70" fill="#D1495B" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257" />
  <circle cx="0" cy="-75" r="12" fill="none" stroke="#F79257" stroke-width="2" />
</svg>
```

<div class="dodona-centered-group">
<figure>
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="20" r="70" fill="#D1495B" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257" />
  <circle cx="0" cy="-75" r="12" fill="none" stroke="#F79257" stroke-width="2" />
</svg>
</figure>
</div>
