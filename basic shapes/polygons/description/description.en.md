We can't always use basic shapes like circles or rectangles to assemble our images. This is the case if we want to draw this Christmas tree.

<figure>
<svg width="200" height="400" viewBox="-100 -200 200 400">
  <rect x="-100" y="-200" width="200" height="400" fill="#F5F1EB"/>
  <polygon points="0,0 80,120 -80,120" fill="#234236" />
  <polygon points="0,-40 60,60 -60,60" fill="#0C5C4C" />
  <polygon points="0,-80 40,0 -40,0" fill="#38755B" />
  <rect x="-20" y="120" width="40" height="30" fill="brown" />
</svg>
</figure>

A `polygon` is the easiest way to draw a freeform shape. Polygons have a `points` property that sets a list of coordinates that are connected with straight lines.

We can make the crown of the tree from three triangles. We start with the one at the bottom, and we add it layer by layer.

```html
<svg width="200" height="400" viewBox="-100 -200 200 400">
  <polygon points="0,0 80,120 -80,120" fill="#234236" />
</svg>
```

<figure>
<svg width="200" height="400" viewBox="-100 -200 200 400">
  <rect x="-100" y="-200" width="200" height="400" fill="#F5F1EB"/>
  <polygon points="0,0 80,120 -80,120" fill="#234236" />
</svg>
</figure>

```html
<svg width="200" height="400" viewBox="-100 -200 200 400">
  <polygon points="0,0 80,120 -80,120" fill="#234236" />
  <polygon points="0,-40 60,60 -60,60" fill="#0C5C4C" />
</svg>
```

<figure>
<svg width="200" height="400" viewBox="-100 -200 200 400">
  <rect x="-100" y="-200" width="200" height="400" fill="#F5F1EB"/>
  <polygon points="0,0 80,120 -80,120" fill="#234236" />
  <polygon points="0,-40 60,60 -60,60" fill="#0C5C4C" />
</svg>
</figure>

```html
<svg width="200" height="400" viewBox="-100 -200 200 400">
  <polygon points="0,0 80,120 -80,120" fill="#234236" />
  <polygon points="0,-40 60,60 -60,60" fill="#0C5C4C" />
  <polygon points="0,-80 40,0 -40,0" fill="#38755B" />
</svg>
```

<figure>
<svg width="200" height="400" viewBox="-100 -200 200 400">
  <rect x="-100" y="-200" width="200" height="400" fill="#F5F1EB"/>
  <polygon points="0,0 80,120 -80,120" fill="#234236" />
  <polygon points="0,-40 60,60 -60,60" fill="#0C5C4C" />
  <polygon points="0,-80 40,0 -40,0" fill="#38755B" />
</svg>
</figure>

Finally, we add the trunk of the tree as a rectangle.

```html
<svg width="200" height="400" viewBox="-100 -200 200 400">
  <polygon points="0,0 80,120 -80,120" fill="#234236" />
  <polygon points="0,-40 60,60 -60,60" fill="#0C5C4C" />
  <polygon points="0,-80 40,0 -40,0" fill="#38755B" />
  <rect x="-20" y="120" width="40" height="30" fill="brown" />
</svg>
```

<figure>
<svg width="200" height="400" viewBox="-100 -200 200 400">
  <rect x="-100" y="-200" width="200" height="400" fill="#F5F1EB"/>
  <polygon points="0,0 80,120 -80,120" fill="#234236" />
  <polygon points="0,-40 60,60 -60,60" fill="#0C5C4C" />
  <polygon points="0,-80 40,0 -40,0" fill="#38755B" />
  <rect x="-20" y="120" width="40" height="30" fill="brown" />
</svg>
</figure>
