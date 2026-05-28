Now that we've learned how to draw arcs, we're ready to tackle the CoderDojo logo.

<figure>
<svg width="400px" height="400px" viewBox="-310 -310 620 620">
  <style>
    text {
      text-anchor: middle;
      dominant-baseline: middle;
      font-family: OCR A, consolas, monospace;
    }
  </style>
  <rect x="-310" y="-310" width="620" height="620" fill="#F5F1EB"/>
  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" />
  <path fill="black" d="
    M0,-300
    A150,150,0,0,1,0,0
    A150,150,0,0,0,0,300
    A300,300,0,0,0,0,-300" 
  />
  <text x="0" y="-128" fill="black" font-size="240">0</text>
  <text x="0" y="172" fill="white" font-size="240">1</text>
</svg>
</figure>

We are using a viewport with a width and height of 620 pixels, with the origin of the coordinate system positioned at the center. We set the width and height of the image itself to 400 pixels.

```html
<svg width="400px" height="400px" viewBox="-310 -310 620 620">
  ...
</svg>
```

<figure>
<svg id="logo1" width="650px" height="640px" viewBox="-330 -320 650 640">

  <style>
    #logo1 text {
      font-family: consolas,monospace;
      text-anchor: middle;
      dominant-baseline: middle;
    }
    #logo1 .coords { 
      display: initial; 
    }
    #logo1 .coords .y-label {
      text-anchor: end;
    }
    #logo1 .coords .grid {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
  </style>
    
  <rect x="-330" y="-320" width="650" height="640" fill="#F5F1EB"/>

  <g class="coords">
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="1,98,1,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="1,98,1,0" />
    <text class="x-label" x="-300" y="-310" fill="black" font-size="10">-300</text>
    <text class="x-label" x="-200" y="-310" fill="black" font-size="10">-200</text>
    <text class="x-label" x="-100" y="-310" fill="black" font-size="10">-100</text>
    <text class="x-label" x="0" y="-310" fill="black" font-size="10">0</text>
    <text class="x-label" x="100" y="-310" fill="black" font-size="10">100</text>
    <text class="x-label" x="200" y="-310" fill="black" font-size="10">200</text>
    <text class="x-label" x="300" y="-310" fill="black" font-size="10">300</text>
    <text class="y-label" x="-308" y="-300" fill="black" font-size="10">-300</text>
    <text class="y-label" x="-308" y="-200" fill="black" font-size="10">-200</text>
    <text class="y-label" x="-308" y="-100" fill="black" font-size="10">-100</text>
    <text class="y-label" x="-308" y="0" fill="black" font-size="10">0</text>
    <text class="y-label" x="-308" y="100" fill="black" font-size="10">100</text>
    <text class="y-label" x="-308" y="200" fill="black" font-size="10">200</text>
    <text class="y-label" x="-308" y="300" fill="black" font-size="10">300</text>
    <path d="M-305,0 L310,0 L305,-2 L305,2 L310,0" stroke="black" stroke-width="1" fill="black" />
    <text x="307" y="8" font-size="10">x</text>
    <path d="M0,-305 L0,310 L-2,305 L2,305 L0,310" stroke="black" stroke-width="1" fill="black" />
    <text x="8" y="307" font-size="10">y</text>
  </g>

</svg>
</figure>

First, we draw a circle with its center at the origin and a radius of 300.

```html
<svg width="400px" height="400px" viewBox="-310 -310 620 620">
  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" />
</svg>
```

<figure>
<svg id="logo2" width="650px" height="640px" viewBox="-330 -320 650 640">

  <style>
    #logo2 text {
      font-family: consolas,monospace;
      text-anchor: middle;
      dominant-baseline: middle;
    }
    #logo2 .coords { 
      display: initial; 
    }
    #logo2 .coords .y-label {
      text-anchor: end;
    }
    #logo2 .coords .grid {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    #logo2 text.element {
      fill: green;
    }
  </style>
    
  <rect x="-330" y="-320" width="650" height="640" fill="#F5F1EB"/>

  <g class="coords">
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="1,98,1,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="1,98,1,0" />
    <text class="x-label" x="-300" y="-310" fill="black" font-size="10">-300</text>
    <text class="x-label" x="-200" y="-310" fill="black" font-size="10">-200</text>
    <text class="x-label" x="-100" y="-310" fill="black" font-size="10">-100</text>
    <text class="x-label" x="0" y="-310" fill="black" font-size="10">0</text>
    <text class="x-label" x="100" y="-310" fill="black" font-size="10">100</text>
    <text class="x-label" x="200" y="-310" fill="black" font-size="10">200</text>
    <text class="x-label" x="300" y="-310" fill="black" font-size="10">300</text>
    <text class="y-label" x="-308" y="-300" fill="black" font-size="10">-300</text>
    <text class="y-label" x="-308" y="-200" fill="black" font-size="10">-200</text>
    <text class="y-label" x="-308" y="-100" fill="black" font-size="10">-100</text>
    <text class="y-label" x="-308" y="0" fill="black" font-size="10">0</text>
    <text class="y-label" x="-308" y="100" fill="black" font-size="10">100</text>
    <text class="y-label" x="-308" y="200" fill="black" font-size="10">200</text>
    <text class="y-label" x="-308" y="300" fill="black" font-size="10">300</text>
    <path d="M-305,0 L310,0 L305,-2 L305,2 L310,0" stroke="black" stroke-width="1" fill="black" />
    <text x="307" y="8" font-size="10">x</text>
    <path d="M0,-305 L0,310 L-2,305 L2,305 L0,310" stroke="black" stroke-width="1" fill="black" />
    <text x="8" y="307" font-size="10">y</text>
  </g>

  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" />
  <line x1="0" y1="0" x2="0" y2="20" stroke="black" stroke-width="1" stroke-dasharray="2,2"/>
  <line x1="300" y1="0" x2="300" y2="20" stroke="black" stroke-width="1" stroke-dasharray="2,2"/>
  <circle cx="0" cy="0" r="5" fill="green" stroke="none" />
  <text class="element" x="-36" y="0" font-size="20">(0,0)</text>
  <path d="M0,20 l5,2 v-4 l-5,2 h300 l-5,-2 v4 l5,-2" stroke="green" stroke-width="1" fill="green" />
  <text class="element" x="150" y="34" font-size="20">300</text>

</svg>
</figure>

Now comes the hardest part: the black teardrop shape. If you analyze it carefully, you’ll see that it consists of three semicircles. We’ll use a `<path>` to draw those three arcs. We’ll start by drawing them with a black outline and no fill. The first semicircle starts at the point $$(0, -300)$$ and ends at the origin. That circle has a radius of 150.

```html
<svg width="400px" height="400px" viewBox="-310 -310 620 620">
  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" />
  <path fill="none" stroke="black" stroke-width="6" d="
    M0,-300
    A150,150,0,0,1,0,0"
  />
</svg>
```

<figure>
<svg id="logo3" width="650px" height="640px" viewBox="-330 -320 650 640">

  <style>
    #logo3 text {
      font-family: consolas,monospace;
      text-anchor: middle;
      dominant-baseline: middle;
    }
    #logo3 .coords { 
      display: initial; 
    }
    #logo3 .coords .y-label {
      text-anchor: end;
    }
    #logo3 .coords .grid {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    #logo3 text.element {
      fill: green;
    }
  </style>
    
  <rect x="-330" y="-320" width="650" height="640" fill="#F5F1EB"/>

  <g class="coords">
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="1,98,1,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="1,98,1,0" />
    <text class="x-label" x="-300" y="-310" fill="black" font-size="10">-300</text>
    <text class="x-label" x="-200" y="-310" fill="black" font-size="10">-200</text>
    <text class="x-label" x="-100" y="-310" fill="black" font-size="10">-100</text>
    <text class="x-label" x="0" y="-310" fill="black" font-size="10">0</text>
    <text class="x-label" x="100" y="-310" fill="black" font-size="10">100</text>
    <text class="x-label" x="200" y="-310" fill="black" font-size="10">200</text>
    <text class="x-label" x="300" y="-310" fill="black" font-size="10">300</text>
    <text class="y-label" x="-308" y="-300" fill="black" font-size="10">-300</text>
    <text class="y-label" x="-308" y="-200" fill="black" font-size="10">-200</text>
    <text class="y-label" x="-308" y="-100" fill="black" font-size="10">-100</text>
    <text class="y-label" x="-308" y="0" fill="black" font-size="10">0</text>
    <text class="y-label" x="-308" y="100" fill="black" font-size="10">100</text>
    <text class="y-label" x="-308" y="200" fill="black" font-size="10">200</text>
    <text class="y-label" x="-308" y="300" fill="black" font-size="10">300</text>
    <path d="M-305,0 L310,0 L305,-2 L305,2 L310,0" stroke="black" stroke-width="1" fill="black" />
    <text x="307" y="8" font-size="10">x</text>
    <path d="M0,-305 L0,310 L-2,305 L2,305 L0,310" stroke="black" stroke-width="1" fill="black" />
    <text x="8" y="307" font-size="10">y</text>
  </g>

  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" stroke-opacity="25%" fill-opacity="50%" />
  <path fill="none" stroke="black" stroke-width="6" d="
    M0,-300
    A150,150,0,0,1,0,0"
  />

  <circle cx="0" cy="-300" r="5" fill="green" stroke="none" />
  <text class="element" x="0" y="-275">(0,-300)</text>
  <circle cx="0" cy="0" r="5" fill="green" stroke="none" />
  <text class="element" x="0" y="-25" font-size="20">(0,0)</text>
  <path d="M0,-150 l5,2 v-4 l-5,2 h150 l-5,-2 v4 l5,-2" stroke="green" stroke-width="1" fill="green" />
  <text class="element" x="75" y="-130" font-size="20">150</text>

</svg>
</figure>

We extend the path with a second semicircle of radius 150 that starts at the origin and ends at the point $$(0, 300)$$.

```html
<svg width="400px" height="400px" viewBox="-310 -310 620 620">
  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" />
  <path fill="none" stroke="black" stroke-width="6" d="
    M0,-300
    A150,150,0,0,1,0,0
    A150,150,0,0,0,0,300"
  />
</svg>
```

<figure>
<svg id="logo4" width="650px" height="640px" viewBox="-330 -320 650 640">

  <style>
    #logo4 text {
      font-family: consolas,monospace;
      text-anchor: middle;
      dominant-baseline: middle;
    }
    #logo4 .coords { 
      display: initial; 
    }
    #logo4 .coords .y-label {
      text-anchor: end;
    }
    #logo4 .coords .grid {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    #logo4 text.element {
      fill: green;
    }
  </style>
    
  <rect x="-330" y="-320" width="650" height="640" fill="#F5F1EB"/>

  <g class="coords">
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="1,98,1,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="1,98,1,0" />
    <text class="x-label" x="-300" y="-310" fill="black" font-size="10">-300</text>
    <text class="x-label" x="-200" y="-310" fill="black" font-size="10">-200</text>
    <text class="x-label" x="-100" y="-310" fill="black" font-size="10">-100</text>
    <text class="x-label" x="0" y="-310" fill="black" font-size="10">0</text>
    <text class="x-label" x="100" y="-310" fill="black" font-size="10">100</text>
    <text class="x-label" x="200" y="-310" fill="black" font-size="10">200</text>
    <text class="x-label" x="300" y="-310" fill="black" font-size="10">300</text>
    <text class="y-label" x="-308" y="-300" fill="black" font-size="10">-300</text>
    <text class="y-label" x="-308" y="-200" fill="black" font-size="10">-200</text>
    <text class="y-label" x="-308" y="-100" fill="black" font-size="10">-100</text>
    <text class="y-label" x="-308" y="0" fill="black" font-size="10">0</text>
    <text class="y-label" x="-308" y="100" fill="black" font-size="10">100</text>
    <text class="y-label" x="-308" y="200" fill="black" font-size="10">200</text>
    <text class="y-label" x="-308" y="300" fill="black" font-size="10">300</text>
    <path d="M-305,0 L310,0 L305,-2 L305,2 L310,0" stroke="black" stroke-width="1" fill="black" />
    <text x="307" y="8" font-size="10">x</text>
    <path d="M0,-305 L0,310 L-2,305 L2,305 L0,310" stroke="black" stroke-width="1" fill="black" />
    <text x="8" y="307" font-size="10">y</text>
  </g>

  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" stroke-opacity="25%" fill-opacity="50%" />
  <path fill="none" stroke="black" stroke-width="6" d="
    M0,-300
    A150,150,0,0,1,0,0
    A150,150,0,0,0,0,300"
  />

  <circle cx="0" cy="300" r="5" fill="green" stroke="none" />
  <text class="element" x="0" y="275">(0,300)</text>
  <circle cx="0" cy="0" r="5" fill="green" stroke="none" />
  <text class="element" x="0" y="-25" font-size="20">(0,0)</text>
  <path d="M-150,150 l5,2 v-4 l-5,2 h150 l-5,-2 v4 l5,-2" stroke="green" stroke-width="1" fill="green" />
  <text class="element" x="-75" y="130" font-size="20">150</text>

</svg>
</figure>

The teardrop shape is closed by connecting the point $$(0, 300)$$ back to the point $$(0, -300)$$ via a semicircle with a radius of 300.

```html
<svg width="400px" height="400px" viewBox="-310 -310 620 620">
  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" />
  <path fill="none" stroke="black" stroke-width="6" d="
    M0,-300
    A150,150,0,0,1,0,0
    A150,150,0,0,0,0,300
    A300,300,0,0,0,0,-300" 
  />
</svg>
```

<figure>
<svg id="logo5" width="650px" height="640px" viewBox="-330 -320 650 640">

  <style>
    #logo5 text {
      font-family: consolas,monospace;
      text-anchor: middle;
      dominant-baseline: middle;
    }
    #logo5 .coords { 
      display: initial; 
    }
    #logo5 .coords .y-label {
      text-anchor: end;
    }
    #logo5 .coords .grid {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    #logo5 text.element {
      fill: green;
    }
  </style>
    
  <rect x="-330" y="-320" width="650" height="640" fill="#F5F1EB"/>

  <g class="coords">
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="1,98,1,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="1,98,1,0" />
    <text class="x-label" x="-300" y="-310" fill="black" font-size="10">-300</text>
    <text class="x-label" x="-200" y="-310" fill="black" font-size="10">-200</text>
    <text class="x-label" x="-100" y="-310" fill="black" font-size="10">-100</text>
    <text class="x-label" x="0" y="-310" fill="black" font-size="10">0</text>
    <text class="x-label" x="100" y="-310" fill="black" font-size="10">100</text>
    <text class="x-label" x="200" y="-310" fill="black" font-size="10">200</text>
    <text class="x-label" x="300" y="-310" fill="black" font-size="10">300</text>
    <text class="y-label" x="-308" y="-300" fill="black" font-size="10">-300</text>
    <text class="y-label" x="-308" y="-200" fill="black" font-size="10">-200</text>
    <text class="y-label" x="-308" y="-100" fill="black" font-size="10">-100</text>
    <text class="y-label" x="-308" y="0" fill="black" font-size="10">0</text>
    <text class="y-label" x="-308" y="100" fill="black" font-size="10">100</text>
    <text class="y-label" x="-308" y="200" fill="black" font-size="10">200</text>
    <text class="y-label" x="-308" y="300" fill="black" font-size="10">300</text>
    <path d="M-305,0 L310,0 L305,-2 L305,2 L310,0" stroke="black" stroke-width="1" fill="black" />
    <text x="307" y="8" font-size="10">x</text>
    <path d="M0,-305 L0,310 L-2,305 L2,305 L0,310" stroke="black" stroke-width="1" fill="black" />
    <text x="8" y="307" font-size="10">y</text>
  </g>

  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" stroke-opacity="25%" fill-opacity="50%" />
  <path fill="none" stroke="black" stroke-width="6" d="
    M0,-300
    A150,150,0,0,1,0,0
    A150,150,0,0,0,0,300
    A300,300,0,0,0,0,-300" 
  />

  <circle cx="0" cy="300" r="5" fill="green" stroke="none" />
  <text class="element" x="0" y="275">(0,300)</text>
  <circle cx="0" cy="-300" r="5" fill="green" stroke="none" />
  <text class="element" x="0" y="-275" font-size="20">(0,-300)</text>
  <path d="M0,20 l5,2 v-4 l-5,2 h300 l-5,-2 v4 l5,-2" stroke="green" stroke-width="1" fill="green" />
  <text class="element" x="150" y="34" font-size="20">300</text>

</svg>
</figure>

Instead of adding a black border to the teardrop shape, we can now fill it with black.

```html
<svg width="400px" height="400px" viewBox="-310 -310 620 620">
  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" />
  <path fill="black" stroke="none" d="
    M0,-300
    A150,150,0,0,1,0,0
    A150,150,0,0,0,0,300
    A300,300,0,0,0,0,-300" 
  />
</svg>
```

<figure>
<svg id="logo6" width="650px" height="640px" viewBox="-330 -320 650 640">

  <style>
    #logo6 text {
      font-family: consolas,monospace;
      text-anchor: middle;
      dominant-baseline: middle;
    }
    #logo6 .coords { 
      display: initial; 
    }
    #logo6 .coords .y-label {
      text-anchor: end;
    }
    #logo6 .coords .grid {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    #logo6 text.element {
      fill: green;
    }
  </style>
    
  <rect x="-330" y="-320" width="650" height="640" fill="#F5F1EB"/>

  <g class="coords">
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="1,98,1,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="1,98,1,0" />
    <text class="x-label" x="-300" y="-310" fill="black" font-size="10">-300</text>
    <text class="x-label" x="-200" y="-310" fill="black" font-size="10">-200</text>
    <text class="x-label" x="-100" y="-310" fill="black" font-size="10">-100</text>
    <text class="x-label" x="0" y="-310" fill="black" font-size="10">0</text>
    <text class="x-label" x="100" y="-310" fill="black" font-size="10">100</text>
    <text class="x-label" x="200" y="-310" fill="black" font-size="10">200</text>
    <text class="x-label" x="300" y="-310" fill="black" font-size="10">300</text>
    <text class="y-label" x="-308" y="-300" fill="black" font-size="10">-300</text>
    <text class="y-label" x="-308" y="-200" fill="black" font-size="10">-200</text>
    <text class="y-label" x="-308" y="-100" fill="black" font-size="10">-100</text>
    <text class="y-label" x="-308" y="0" fill="black" font-size="10">0</text>
    <text class="y-label" x="-308" y="100" fill="black" font-size="10">100</text>
    <text class="y-label" x="-308" y="200" fill="black" font-size="10">200</text>
    <text class="y-label" x="-308" y="300" fill="black" font-size="10">300</text>
    <path d="M-305,0 L310,0 L305,-2 L305,2 L310,0" stroke="black" stroke-width="1" fill="black" />
    <text x="307" y="8" font-size="10">x</text>
    <path d="M0,-305 L0,310 L-2,305 L2,305 L0,310" stroke="black" stroke-width="1" fill="black" />
    <text x="8" y="307" font-size="10">y</text>
  </g>

  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" stroke-opacity="25%" fill-opacity="50%" />
  <path fill="black" stroke="none" d="
    M0,-300
    A150,150,0,0,1,0,0
    A150,150,0,0,0,0,300
    A300,300,0,0,0,0,-300" 
  />

</svg>
</figure>

The last thing we need to do is place the digits `0` and `1` in the correct positions. To do this, we can use the `text` element to place a black-filled digit `0` at position $$(0, -150)$$ and a white-filled digit `1` at position $$(0, 150)$$. We also set the text size (`font-size`) to 240.

```html
<svg width="400px" height="400px" viewBox="-310 -310 620 620">
  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" />
  <path fill="black" stroke="none" d="
    M0,-300
    A150,150,0,0,0,0,300
    A300,300,0,0,0,0,-300" 
  />
  <text x="0" y="-150" fill="black" font-size="240">0</text>
  <text x="0" y="150" fill="white" font-size="240">1</text>
</svg>
```

<figure>
<svg id="logo7" width="650px" height="640px" viewBox="-330 -320 650 640">

  <style>
    #logo7 text {
      text-anchor: middle;
      dominant-baseline: middle;
      font-family: OCR A, consolas, monospace;
    }
    #logo7 .coords text {
      font-family: consolas,monospace;
      text-anchor: middle;
      dominant-baseline: middle;
    }
    #logo7 .coords { 
      display: initial; 
    }
    #logo7 .coords .y-label {
      text-anchor: end;
    }
    #logo7 .coords .grid {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    #logo7 text.element {
      font-family: consolas,monospace;
      fill: green;
    }
  </style>
    
  <rect x="-330" y="-320" width="650" height="640" fill="#F5F1EB"/>

  <g class="coords">
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="1,98,1,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="1,98,1,0" />
    <text class="x-label" x="-300" y="-310" fill="black" font-size="10">-300</text>
    <text class="x-label" x="-200" y="-310" fill="black" font-size="10">-200</text>
    <text class="x-label" x="-100" y="-310" fill="black" font-size="10">-100</text>
    <text class="x-label" x="0" y="-310" fill="black" font-size="10">0</text>
    <text class="x-label" x="100" y="-310" fill="black" font-size="10">100</text>
    <text class="x-label" x="200" y="-310" fill="black" font-size="10">200</text>
    <text class="x-label" x="300" y="-310" fill="black" font-size="10">300</text>
    <text class="y-label" x="-308" y="-300" fill="black" font-size="10">-300</text>
    <text class="y-label" x="-308" y="-200" fill="black" font-size="10">-200</text>
    <text class="y-label" x="-308" y="-100" fill="black" font-size="10">-100</text>
    <text class="y-label" x="-308" y="0" fill="black" font-size="10">0</text>
    <text class="y-label" x="-308" y="100" fill="black" font-size="10">100</text>
    <text class="y-label" x="-308" y="200" fill="black" font-size="10">200</text>
    <text class="y-label" x="-308" y="300" fill="black" font-size="10">300</text>
    <path d="M-305,0 L310,0 L305,-2 L305,2 L310,0" stroke="black" stroke-width="1" fill="black" />
    <text class="element" x="307" y="8" font-size="10">x</text>
    <path d="M0,-305 L0,310 L-2,305 L2,305 L0,310" stroke="black" stroke-width="1" fill="black" />
    <text class="element" x="8" y="307" font-size="10">y</text>
  </g>

  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" stroke-opacity="25%" fill-opacity="50%" />
  <path fill="black" stroke="none" fill-opacity="25%" d="
    M0,-300
    A150,150,0,0,1,0,0
    A150,150,0,0,0,0,300
    A300,300,0,0,0,0,-300" 
  />
  <text x="0" y="-128" fill="black" font-size="240">0</text>
  <text x="0" y="172" fill="white" font-size="240">1</text>

  <circle cx="0" cy="-150" r="5" fill="green" stroke="none" />
  <circle cx="0" cy="150" r="5" fill="green" stroke="none" />
  <text class="element" x="-55" y="-150" font-size="20">(0,-150)</text>
  <text class="element" x="-55" y="150" font-size="20">(0,150)</text>

</svg>
</figure>

However, you will notice that the code above does not yet produce the desired result. After all, we still need to set a few properties for the text. Since these are the same for both numbers, we will use a `style` element to set the CSS properties for all text in the figure at once. We set the font family (`font-family`) and font size (`font-size`) of the text to `OCR A`. For computers on which this font is not installed, we fall back to the `consolas` font and then to the standard `monospace` font.

```html
<style>
  text {
    text-anchor: middle;
    dominant-baseline: middle;
    font-family: OCR A, consolas, monospace;
  }
</style>
```

Normally, the anchor point where the text is positioned is in the top-left corner. With `text-anchor: middle;`, we ensure that the text is horizontally centered around the anchor point. With `dominant-baseline: middle;`, we ensure that the text is vertically centered around the anchor point. However, the latter is not entirely the case, so we move both numbers down another 22 positions along the $$y$$-axis to get them in their desired positions. This is the final result:

```html
<svg width="400px" height="400px" viewBox="-310 -310 620 620">
  <style>
    text {
      text-anchor: middle;
      dominant-baseline: middle;
      font-family: OCR A, consolas, monospace;
    }
  </style>
  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" />
  <path fill="black" stroke="none" d="
    M0,-300
    A150,150,0,0,1,0,0
    A150,150,0,0,0,0,300
    A300,300,0,0,0,0,-300" 
  />
  <text x="0" y="-128" fill="black" font-size="240">0</text>
  <text x="0" y="172" fill="white" font-size="240">1</text>
</svg>
```

<figure>
<svg id="logo8" width="400px" height="400px" viewBox="-310 -310 620 620">
  <style>
    #logo8 text {
      text-anchor: middle;
      dominant-baseline: middle;
      font-family: OCR A, consolas, monospace;
    }
  </style>
  <rect x="-310" y="-310" width="620" height="620" fill="#F5F1EB"/>
  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" />
  <path fill="black" stroke="none" d="
    M0,-300
    A150,150,0,0,1,0,0
    A150,150,0,0,0,0,300
    A300,300,0,0,0,0,-300" 
  />
  <text x="0" y="-128" fill="black" font-size="240">0</text>
  <text x="0" y="172" fill="white" font-size="240">1</text>
</svg>
</figure>
