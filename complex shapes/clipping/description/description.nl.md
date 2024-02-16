This ornament is the same as we drew on the first day, except it has a motif on its side defined as a `polyline`.

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
    <clipPath id="ball1">
      <circle cx="0" cy="20" r="70" />
    </clipPath>
  </defs>

  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="20" r="70" fill="#D1495B" />
  <polyline clip-path="url(#ball1)" fill="none" stroke="#9C2D2A" stroke-width="20"
    points="-120 40 -80 0 -40 40 0 0 40 40 80 0 120 40" />
  <circle cx="0" cy="-75" r="12" fill="none" stroke="#F79257" stroke-width="2" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257" />
</svg>
</figure>

By default, the `polyline` wouldn't match the edge of the `circle` shape. Without **clipping** this motif would look like this:

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="20" r="70" fill="#D1495B" />
  <polyline fill="none" stroke="#9C2D2A" stroke-width="20"
    points="-120 40 -80 0 -40 40 0 0 40 40 80 0 120 40" />
  <circle cx="0" cy="-75" r="12" fill="none" stroke="#F79257" stroke-width="2" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257" />
</svg>
</figure>

We use `clip-path` here to make sure that the motif fits perfectly on the ornament. The `clip-path` is defined in the definitions section.

Here we define a `clipPath` with an ID. The content of this `clip-path` is a `circle` that matches the size of our ornament. Then we use it to clip the `polyline`, by setting its `clip-path` property.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
    <clipPath id="ball">
      <circle cx="0" cy="20" r="70" />
    </clipPath>
  </defs>

  <circle cx="0" cy="20" r="70" fill="#D1495B" />
  <polyline clip-path="url(#ball)" fill="none" stroke="#9C2D2A" stroke-width="20"
    points="-120 40 -80 0 -40 40 0 0 40 40 80 0 120 40" />
  <circle cx="0" cy="-75" r="12" fill="none" stroke="#F79257" stroke-width="2" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
    <clipPath id="ball">
      <circle cx="0" cy="20" r="70" />
    </clipPath>
  </defs>

  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="20" r="70" fill="#D1495B" />
  <polyline clip-path="url(#ball)"  fill="none" stroke="#9C2D2A" stroke-width="20"
    points="-120 40 -80 0 -40 40 0 0 40 40 80 0 120 40" />
  <circle cx="0" cy="-75" r="12" fill="none" stroke="#F79257" stroke-width="2" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257" />
</svg>
</figure>
