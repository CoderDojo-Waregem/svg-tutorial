Before we start drawing, we have to talk about 

- the coordinate system of SVG images
- the dimensions and the viewport of the `svg` element itself 

### The coordinate system of SVG

The image elements are drawn in a plane with a coordinate system where the $$x$$-axis runs from left to right, and the $$y$$-axis from top to bottom. The latter in particular might take some special attention, because in maths lessons, the $$y$$ axis usually runs from bottom to top.

<figure>
<svg class="coordinates1" width="600px" viewBox="-335 -320 655 640">

  <style>
    .coordinates1 text {
      font-family:consolas,monospace;
      font-size:10px;
      text-anchor:middle;
      dominant-baseline:middle;
    }
    .coordinates1 .grid { 
      display: initial; 
    }
    .coordinates1 .grid text.left {
      text-anchor:end;
    }
    .coordinates1 .grid path {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    .coordinates1 .background {
      stroke: none;
      fill: #F5F1EB;
    }
  </style>

  <rect class="background" x="-335" y="-320" width="655" height="640" />

  <g class="grid">
    <path d="M-300,0 L300,0" stroke-dasharray="0.2,9.6,0.2,0" />
    <path d="M0,-300 L0,300" stroke-dasharray="0.2,9.6,0.2,0" />
    <path d="M-300,0 L300,0" stroke-dasharray="1,98,1,0" />
    <path d="M0,-300 L0,300" stroke-dasharray="1,98,1,0" />
    <text x="-300" y="-310" fill="black" font-size="5">-300</text>
    <text x="-200" y="-310" fill="black" font-size="5">-200</text>
    <text x="-100" y="-310" fill="black" font-size="5">-100</text>
    <text x="0" y="-310" fill="black" font-size="5">0</text>
    <text x="100" y="-310" fill="black" font-size="5">100</text>
    <text x="200" y="-310" fill="black" font-size="5">200</text>
    <text x="300" y="-310" fill="black" font-size="5">300</text>
    <text class="left" x="-308" y="-300" fill="black" font-size="5">-300</text>
    <text class="left" x="-308" y="-200" fill="black" font-size="5">-200</text>
    <text class="left" x="-308" y="-100" fill="black" font-size="5">-100</text>
    <text class="left" x="-308" y="0" fill="black" font-size="5">0</text>
    <text class="left" x="-308" y="100" fill="black" font-size="5">100</text>
    <text class="left" x="-308" y="200" fill="black" font-size="5">200</text>
    <text class="left" x="-308" y="300" fill="black" font-size="5">300</text>
  </g>

  <path d="M-305,0 L310,0 L305,-2 L305,2 L310,0" stroke="black" stroke-width="1" fill="black" />
  <text x="307" y="8" >x</text>
  <path d="M0,-305 L0,310 L-2,305 L2,305 L0,310" stroke="black" stroke-width="1" fill="black" />
  <text x="8" y="307" >y</text>

  <circle cx="100" cy="100" r="50" fill="none" stroke="black" stroke-width="5" />

</svg>
</figure>

The coordinates themselves have no specific dimension: they are simply numbers with no unit of length (such as pixels or metres). To draw a circle, we need to specify for the `circle` element the $$(x, y)$$-coordinates of the **center** of the circle (via the `x` and `y` properties) and the **radius** of the circle (via the `r` property).

```html
<circle cx="100" cy="100" r="50" />
```

This draws a circle (shown below with a thick black border) with center at position $$(100, 100)$$ and radius 50.

<figure>
<svg class="coordinates2" width="600px" viewBox="-335 -320 655 640">

  <style>
    .coordinates2 text {
      font-family:consolas,monospace;
      font-size:10px;
      text-anchor:middle;
      dominant-baseline:middle;
    }
    .coordinates2 text.coord {
      font-size:8px;
    }
    .coordinates2 .grid { 
      display: initial; 
    }
    .coordinates2 .grid text.left {
      text-anchor:end;
    }
    .coordinates2 .grid path {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    .coordinates2 .background {
      stroke: none;
      fill: #F5F1EB;
    }
  </style>
    
  <rect class="background" x="-335" y="-320" width="655" height="640" />

  <g class="grid">
    <path d="M-300,0 L300,0" stroke-dasharray="0.2,9.6,0.2,0" />
    <path d="M0,-300 L0,300" stroke-dasharray="0.2,9.6,0.2,0" />
    <path d="M-300,0 L300,0" stroke-dasharray="1,98,1,0" />
    <path d="M0,-300 L0,300" stroke-dasharray="1,98,1,0" />
    <text x="-300" y="-310" fill="black" font-size="5">-300</text>
    <text x="-200" y="-310" fill="black" font-size="5">-200</text>
    <text x="-100" y="-310" fill="black" font-size="5">-100</text>
    <text x="0" y="-310" fill="black" font-size="5">0</text>
    <text x="100" y="-310" fill="black" font-size="5">100</text>
    <text x="200" y="-310" fill="black" font-size="5">200</text>
    <text x="300" y="-310" fill="black" font-size="5">300</text>
    <text class="left" x="-308" y="-300" fill="black" font-size="5">-300</text>
    <text class="left" x="-308" y="-200" fill="black" font-size="5">-200</text>
    <text class="left" x="-308" y="-100" fill="black" font-size="5">-100</text>
    <text class="left" x="-308" y="0" fill="black" font-size="5">0</text>
    <text class="left" x="-308" y="100" fill="black" font-size="5">100</text>
    <text class="left" x="-308" y="200" fill="black" font-size="5">200</text>
    <text class="left" x="-308" y="300" fill="black" font-size="5">300</text>
  </g>

  <path d="M-305,0 L310,0 L305,-2 L305,2 L310,0" stroke="black" stroke-width="1" fill="black" />
  <text x="307" y="8" >x</text>
  <path d="M0,-305 L0,310 L-2,305 L2,305 L0,310" stroke="black" stroke-width="1" fill="black" />
  <text x="8" y="307" >y</text>

  <circle cx="100" cy="100" r="50" fill="none" stroke="black" stroke-width="5" />
  <circle cx="100" cy="100" r="4" fill="black" stroke="none" />
  <text class="coord" x="80" y="94" fill="green">(100,100)</text>
  <path d="M103,103 L134,134" stroke="green" stroke-width="1" fill="black" />
  <text class="coord" x="125" y="115.5" fill="green">50</text>

</svg>
</figure>

### Dimensions and viewport of an SVG image

The SVG element contains all image elements, but it also defines the dimensions and the viewport of the image. It sets the external and internal dimensions of the image.

The `width` and `height` properties define how much space the image takes up in the browser. These are the external sizes. The size defined by `width` and `height` is how the rest of the HTML thinks of the image and how big it appears in the browser.

There is also a `viewBox` property that defines the viewport for the image on the coordinate system. Only those parts of the image elements that fall within the viewport are visible in the SVG image. The viewport is defined by four internal measures that refer to the coordinate system of the SVG image. The first two values of the `viewBox` property define the position of the top-left corner of the viewport and the last two values define the width and height of the viewport from the perspective of the image elements. The dimensions defined by `viewBox` is how the image elements think about the image when they position themselves within the SVG coordinate system.

In the following three examples, the three SVG images have exactly the same content: the circle centered at position $$(100, 100)$$ and radius 50 that we have already encountered above. However, the three images differ in terms of viewport, so the circle is positioned differently within the image each time. Or they differ in terms of dimensions, causing the image to be displayed larger or smaller in the browser. If the size defined by `viewBox` does not match the `width` and `height` properties, the image is made larger or smaller.

```html
<svg width="100px" height="100px" viewBox="0 0 200 200">
  <circle cx="100" cy="100" r="50" />
</svg>
```

<figure>
<svg width="100px" height="100px" viewBox="0 0 200 200">
  <rect x="0" y="0" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="100" cy="100" r="50" />
</svg>
</figure>

This SVG image has a viewport with top-left corner at position $$(0, 0)$$ and a width and height of 200.

<figure>
<svg class="coordinates3" width="600px" viewBox="-335 -320 655 640">

  <style>
    .coordinates3 text {
      font-family:consolas,monospace;
      font-size:10px;
      text-anchor:middle;
      dominant-baseline:middle;
    }
    .coordinates3 text.coord {
      font-size:8px;
    }
    .coordinates3 .grid { 
      display: initial; 
    }
    .coordinates3 .grid text.left {
      text-anchor:end;
    }
    .coordinates3 .grid path {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    .coordinates3 .background {
      stroke: none;
      fill: #F5F1EB;
    }
  </style>
    
  <rect class="background" x="-335" y="-320" width="655" height="640" />

  <g class="grid">
    <path d="M-300,0 L300,0" stroke-dasharray="0.2,9.6,0.2,0" />
    <path d="M0,-300 L0,300" stroke-dasharray="0.2,9.6,0.2,0" />
    <path d="M-300,0 L300,0" stroke-dasharray="1,98,1,0" />
    <path d="M0,-300 L0,300" stroke-dasharray="1,98,1,0" />
    <text x="-300" y="-310" fill="black" font-size="5">-300</text>
    <text x="-200" y="-310" fill="black" font-size="5">-200</text>
    <text x="-100" y="-310" fill="black" font-size="5">-100</text>
    <text x="0" y="-310" fill="black" font-size="5">0</text>
    <text x="100" y="-310" fill="black" font-size="5">100</text>
    <text x="200" y="-310" fill="black" font-size="5">200</text>
    <text x="300" y="-310" fill="black" font-size="5">300</text>
    <text class="left" x="-308" y="-300" fill="black" font-size="5">-300</text>
    <text class="left" x="-308" y="-200" fill="black" font-size="5">-200</text>
    <text class="left" x="-308" y="-100" fill="black" font-size="5">-100</text>
    <text class="left" x="-308" y="0" fill="black" font-size="5">0</text>
    <text class="left" x="-308" y="100" fill="black" font-size="5">100</text>
    <text class="left" x="-308" y="200" fill="black" font-size="5">200</text>
    <text class="left" x="-308" y="300" fill="black" font-size="5">300</text>
  </g>

  <path d="M-305,0 L310,0 L305,-2 L305,2 L310,0" stroke="black" stroke-width="1" fill="black" />
  <text x="307" y="8" >x</text>
  <path d="M0,-305 L0,310 L-2,305 L2,305 L0,310" stroke="black" stroke-width="1" fill="black" />
  <text x="8" y="307" >y</text>

  <circle cx="100" cy="100" r="50" fill="black" stroke="none" />

  <rect x="-307" y="-307" width="620" height="307" fill="rgb(245,241,235,0.8)" />
  <rect x="-307" y="200" width="620" height="117" fill="rgb(245,241,235,0.8)" />
  <rect x="-307" y="0" width="307" height="200" fill="rgb(245,241,235,0.8)" />
  <rect x="200" y="0" width="117" height="200" fill="rgb(245,241,235,0.8)" />
  <rect x="0" y="0" width="200" height="200" fill="none" stroke="black" stroke-width="1" stroke-dasharray="5,5" />
  <circle cx="0" cy="0" r="4" fill="green" stroke="none" />
  <text class="coord" x="-14" y="-6" fill="green">(0,0)</text>
  <path d="M0,210 L5,212 L5,208 L0,210 L200,210 L195,212 L195,208 L200,210" stroke="green" stroke-width="1" fill="green" />
  <text class="coord" x="100" y="220" fill="green">200</text>
  <path d="M210,0 L212,5 L208,5 L210,0 L210,200 L212,195 L208,195 L210,200" stroke="green" stroke-width="1" fill="green" />
  <text class="coord" x="220" y="100" fill="green">200</text>
  
</svg>
</figure>

This is the same viewport as the SVG image below, but that image is displayed twice as large in the browser. Where the image above is displayed in the browser with a width and height of 100 pixels, the image below displays with a width and height of 200 pixels.

```html
<svg width="200px" height="200px" viewBox="0 0 200 200">
  <circle cx="100" cy="100" r="50" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="0 0 200 200">
  <rect x="0" y="0" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="100" cy="100" r="50" />
</svg>
</figure>

The figure below is display with the same size in the browser.

```html
<svg width="200px" height="200px" viewBox="0 0 100 100">
  <circle cx="100" cy="100" r="50" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="0 0 100 100">
  <rect x="0" y="0" width="100" height="100" fill="#F5F1EB"/>
  <circle cx="100" cy="100" r="50" />
</svg>
</figure>

But its viewport only has half the size: the viewport has width 100 and height 100.

<figure>
<svg class="coordinates4" width="600px" viewBox="-335 -320 655 640">

  <style>
    .coordinates4 text {
      font-family:consolas,monospace;
      font-size:10px;
      text-anchor:middle;
      dominant-baseline:middle;
    }
    .coordinates4 text.coord {
      font-size:8px;
    }
    .coordinates4 .grid { 
      display: initial; 
    }
    .coordinates4 .grid text.left {
      text-anchor:end;
    }
    .coordinates4 .grid path {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    .coordinates4 .background {
      stroke: none;
      fill: #F5F1EB;
    }
  </style>
    
  <rect class="background" x="-335" y="-320" width="655" height="640" />

  <g class="grid">
    <path d="M-300,0 L300,0" stroke-dasharray="0.2,9.6,0.2,0" />
    <path d="M0,-300 L0,300" stroke-dasharray="0.2,9.6,0.2,0" />
    <path d="M-300,0 L300,0" stroke-dasharray="1,98,1,0" />
    <path d="M0,-300 L0,300" stroke-dasharray="1,98,1,0" />
    <text x="-300" y="-310" fill="black" font-size="5">-300</text>
    <text x="-200" y="-310" fill="black" font-size="5">-200</text>
    <text x="-100" y="-310" fill="black" font-size="5">-100</text>
    <text x="0" y="-310" fill="black" font-size="5">0</text>
    <text x="100" y="-310" fill="black" font-size="5">100</text>
    <text x="200" y="-310" fill="black" font-size="5">200</text>
    <text x="300" y="-310" fill="black" font-size="5">300</text>
    <text class="left" x="-308" y="-300" fill="black" font-size="5">-300</text>
    <text class="left" x="-308" y="-200" fill="black" font-size="5">-200</text>
    <text class="left" x="-308" y="-100" fill="black" font-size="5">-100</text>
    <text class="left" x="-308" y="0" fill="black" font-size="5">0</text>
    <text class="left" x="-308" y="100" fill="black" font-size="5">100</text>
    <text class="left" x="-308" y="200" fill="black" font-size="5">200</text>
    <text class="left" x="-308" y="300" fill="black" font-size="5">300</text>
  </g>

  <path d="M-305,0 L310,0 L305,-2 L305,2 L310,0" stroke="black" stroke-width="1" fill="black" />
  <text x="307" y="8" >x</text>
  <path d="M0,-305 L0,310 L-2,305 L2,305 L0,310" stroke="black" stroke-width="1" fill="black" />
  <text x="8" y="307" >y</text>

  <circle cx="100" cy="100" r="50" fill="black" stroke="none" />

  <rect x="-307" y="-307" width="620" height="307" fill="rgb(245,241,235,0.8)" />
  <rect x="-307" y="100" width="620" height="217" fill="rgb(245,241,235,0.8)" />
  <rect x="-307" y="0" width="307" height="100" fill="rgb(245,241,235,0.8)" />
  <rect x="100" y="0" width="217" height="100" fill="rgb(245,241,235,0.8)" />
  <rect x="0" y="0" width="100" height="100" fill="none" stroke="black" stroke-width="1" stroke-dasharray="5,5" />

  <circle cx="0" cy="0" r="4" fill="green" stroke="none" />
  <text class="coord" x="-14" y="-6" fill="green">(0,0)</text>
  <path d="M0,110 L5,112 L5,108 L0,110 L100,110 L95,112 L95,108 L100,110" stroke="green" stroke-width="1" fill="green" />
  <text class="coord" x="50" y="120" fill="green">100</text>
  <path d="M110,0 L112,5 L108,5 L110,0 L110,100 L112,95 L108,95 L110,100" stroke="green" stroke-width="1" fill="green" />
  <text class="coord" x="120" y="50" fill="green">100</text>
  
</svg>
</figure>

We can also set at which coordinate the upper left corner of the viewport should be. In the following example, we move the origin of the coordinate system to the center of the image. To do this, we set the top left corner to `-100,-100`, which is half the image size in negative.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <circle cx="0" cy="0" r="50" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="0" r="50" />
</svg>
</figure>

Note that position of the center of the circle is now `0,0`.

<figure>
<svg class="coordinates5" width="600px" viewBox="-335 -320 655 640">

  <style>
    .coordinates5 text {
      font-family:consolas,monospace;
      font-size:10px;
      text-anchor:middle;
      dominant-baseline:middle;
    }
    .coordinates5 text.coord {
      font-size:8px;
    }
    .coordinates5 .grid { 
      display: initial; 
    }
    .coordinates5 .grid text.left {
      text-anchor:end;
    }
    .coordinates5 .grid path {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    .coordinates5 .background {
      stroke: none;
      fill: #F5F1EB;
    }
  </style>
    
  <rect class="background" x="-335" y="-320" width="655" height="640" />

  <g class="grid">
    <path d="M-300,0 L300,0" stroke-dasharray="0.2,9.6,0.2,0" />
    <path d="M0,-300 L0,300" stroke-dasharray="0.2,9.6,0.2,0" />
    <path d="M-300,0 L300,0" stroke-dasharray="1,98,1,0" />
    <path d="M0,-300 L0,300" stroke-dasharray="1,98,1,0" />
    <text x="-300" y="-310" fill="black" font-size="5">-300</text>
    <text x="-200" y="-310" fill="black" font-size="5">-200</text>
    <text x="-100" y="-310" fill="black" font-size="5">-100</text>
    <text x="0" y="-310" fill="black" font-size="5">0</text>
    <text x="100" y="-310" fill="black" font-size="5">100</text>
    <text x="200" y="-310" fill="black" font-size="5">200</text>
    <text x="300" y="-310" fill="black" font-size="5">300</text>
    <text class="left" x="-308" y="-300" fill="black" font-size="5">-300</text>
    <text class="left" x="-308" y="-200" fill="black" font-size="5">-200</text>
    <text class="left" x="-308" y="-100" fill="black" font-size="5">-100</text>
    <text class="left" x="-308" y="0" fill="black" font-size="5">0</text>
    <text class="left" x="-308" y="100" fill="black" font-size="5">100</text>
    <text class="left" x="-308" y="200" fill="black" font-size="5">200</text>
    <text class="left" x="-308" y="300" fill="black" font-size="5">300</text>
  </g>

  <path d="M-305,0 L310,0 L305,-2 L305,2 L310,0" stroke="black" stroke-width="1" fill="black" />
  <text x="307" y="8" >x</text>
  <path d="M0,-305 L0,310 L-2,305 L2,305 L0,310" stroke="black" stroke-width="1" fill="black" />
  <text x="8" y="307" >y</text>

  <circle cx="0" cy="0" r="50" fill="black" stroke="none" />

  <rect x="-307" y="-307" width="620" height="207" fill="rgb(245,241,235,0.8)" />
  <rect x="-307" y="100" width="620" height="217" fill="rgb(245,241,235,0.8)" />
  <rect x="-307" y="-100" width="207" height="200" fill="rgb(245,241,235,0.8)" />
  <rect x="100" y="-100" width="217" height="200" fill="rgb(245,241,235,0.8)" />
  <rect x="-100" y="-100" width="200" height="200" fill="none" stroke="black" stroke-width="1" stroke-dasharray="5,5" />

  <circle cx="0" cy="0" r="4" fill="white" stroke="none" />
  <text class="coord" x="-14" y="-6" fill="white">(0,0)</text>

  <circle cx="-100" cy="-100" r="4" fill="green" stroke="none" />
  <text class="coord" x="-128" y="-106" fill="green">(-100,-100)</text>

  <path d="M-100,110 L-95,112 L-95,108 L-100,110 L100,110 L95,112 L95,108 L100,110" stroke="green" stroke-width="1" fill="green" />
  <text class="coord" x="0" y="120" fill="green">200</text>
  <path d="M110,-100 L112,-95 L108,-95 L110,-100 L110,100 L112,95 L108,95 L110,100" stroke="green" stroke-width="1" fill="green" />
  <text class="coord" x="120" y="0" fill="green">200</text>
  
</svg>
</figure>

SVGs often have an `xmlns` property as well. This, however – if the image is inlined in HTML – can be omitted.

