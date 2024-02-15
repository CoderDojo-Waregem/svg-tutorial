Before we start drawing, we have to talk about the `svg` element itself. The SVG element contains the image elements and defines the frame of our image. It sets the inner size and the outer size of the image.

The `width` and `height` properties define how much space the image takes up in the browser. There’s also a `viewBox` property that defines a coordinate system for the image elements. The first two values in viewBox define the top-left coordinate in the image and the last two define the size from the perspective of the image elements.

- The size defined by `width` and `height` is how the rest of the HTML thinks of the image and how big it appears in the browser.
- The size defined by `viewBox` is how the image elements think of the image when they position themselves.

In these next three examples, we have three SVGs that have the very same content. A `circle` element with the same center coordinate and same radius. They appear quite different though. In case the size defined by viewBox does not match the width and the height properties, then the image scales up or scales down.

```svg
<svg width="100" height="100" viewBox="0 0 200 200">
  <circle cx="100" cy="100" r="50" />
</svg>
```

<figure>
<svg width="100" height="100" viewBox="0 0 200 200">
  <rect x="0" y="0" width="200" height="200" stroke="gray" stroke-width="4" stroke-dasharray="4,4" fill="none"/>
  <circle cx="100" cy="100" r="50" />
</svg>
</figure>

```svg
<svg width="200" height="200" viewBox="0 0 200 200">
  <circle cx="100" cy="100" r="50" />
</svg>
```

<figure>
<svg width="200" height="200" viewBox="0 0 200 200">
  <rect x="0" y="0" width="200" height="200" stroke="gray" stroke-width="2" stroke-dasharray="2,2" fill="none"/>
  <circle cx="100" cy="100" r="50" />
</svg>
</figure>

```svg
<svg width="100" height="100" viewBox="0 0 200 200">
  <circle cx="100" cy="100" r="50" />
</svg>
```

<figure>
<svg width="200" height="200" viewBox="0 0 100 100">
  <rect x="0" y="0" width="100" height="100" stroke="gray" stroke-width="1" stroke-dasharray="1,1" fill="none"/>
  <circle cx="100" cy="100" r="50" />
</svg>
</figure>

We can also set what coordinate should be in the top-left corner of the image. In the following example, we move the origin of the coordinate system to the center of the image. We set the top left corner to `-100,-100` which is half of the image size in negative.

Note that now the center position of the circle is `0,0`.

SVGs often have an `xmlns` property as well. This, however – if the image is inlined in HTML – can be omitted.