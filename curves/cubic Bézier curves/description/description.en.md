Let's try to make a drawing of this gift box.

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .box {
      fill: #d1495b;
      stroke: black;
      stroke-width: 2px;
    }
    .stripe {
      fill: white;
      stroke: black;
      stroke-width: 2px;
    }
    .ribbon {
      stroke: #b73a3b;
      stroke-width: 4px;
      fill: none;
    }    
  </style>

  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="-50" r="10" fill="#a9172a" />
  <rect class="box" x="-60" y="-40" width="120" height="100" />
  <rect class="box" x="-70" y="-47" width="140" height="20" />
  <rect class="stripe" x="-20" y="-40" width="40" height="100" />
  <rect class="stripe" x="-25" y="-47" width="50" height="20" />
  <path class="ribbon" d="M0,-50 L30,-50 C50,-50,50,-70,30,-65 L0,-50" />
  <path class="ribbon" d="M0,-50 L-30,-50 C-50,-50,-50,-70,-30,-65 L0,-50" />
</svg>
</figure>

While the quadratic Bézier is great when we want to bend a line, often it’s not flexible enough. With cubic Bézier, we not only have one control point but two. The first control point sets the initial direction of the curve and the second one defines from which direction should the curve arrive at its endpoint.

Again, let’s see an example, where the circles represent the control points.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-50,50 C-60,-50 60,-50 50,50" fill="none" stroke="red" />
  <circle cx="-60" cy="-50" r="5" />
  <circle cx="60" cy="-50" r="5" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-50,50 C-60,-50 60,-50 50,50" fill="none" stroke="red" />
  <circle cx="-60" cy="-50" r="5" />
  <circle cx="60" cy="-50" r="5" />
</svg>
</figure>

Click here for [an interactive demo](https://hunormarton.github.io/svg-curves){: target="_blank"} of cubic Béziers (select **Cubic Bézier** at the top of the page).

Cubic Béziers are great when we want to continue the flow of a line. If the direction of the control points matches the directions of the line before and the line after the curve, then we have a smooth transition between the path segments.

In this example, the ribbon of the gift box uses a cubic Bézier that smoothly continues the previous straight line and then turns back to the direction of the upcoming line.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M0,0 L30,0 C50,0,50,-25,30,-15 L0,0" fill="none" stroke="red" />
  <circle cx="50" cy="0" r="2" />
  <circle cx="50" cy="-20" r="2" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M0,0 L30,0 C50,0,50,-25,30,-15 L0,0" fill="none" stroke="red" />
  <circle cx="50" cy="0" r="2" />
  <circle cx="50" cy="-20" r="2" />
</svg>
</figure>

Apart from the cubic Béziers the rest of this image is mainly just a few rectangles and a circle.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .box {
      fill: #d1495b;
      stroke: black;
      stroke-width: 2px;
    }
    .stripe {
      fill: white;
      stroke: black;
      stroke-width: 2px;
    }
    .ribbon {
      stroke: #b73a3b;
      stroke-width: 4px;
      fill: none;
    }    
  </style>

  <circle cx="0" cy="-50" r="10" fill="#a9172a" />
  <rect class="box" x="-60" y="-40" width="120" height="100" />
  <rect class="box" x="-70" y="-47" width="140" height="20" />
  <rect class="stripe" x="-20" y="-40" width="40" height="100" />
  <rect class="stripe" x="-25" y="-47" width="50" height="20" />
  <path class="ribbon" d="M0,-50 L30,-50 C50,-50,50,-70,30,-65 L0,-50" />
  <path class="ribbon" d="M0,-50 L-30,-50 C-50,-50,-50,-70,-30,-65 L0,-50" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .box {
      fill: #d1495b;
      stroke: black;
      stroke-width: 2px;
    }
    .stripe {
      fill: white;
      stroke: black;
      stroke-width: 2px;
    }
    .ribbon {
      stroke: #b73a3b;
      stroke-width: 4px;
      fill: none;
    }    
  </style>

  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="-50" r="10" fill="#a9172a" />
  <rect class="box" x="-60" y="-40" width="120" height="100" />
  <rect class="box" x="-70" y="-47" width="140" height="20" />
  <rect class="stripe" x="-20" y="-40" width="40" height="100" />
  <rect class="stripe" x="-25" y="-47" width="50" height="20" />
  <path class="ribbon" d="M0,-50 L30,-50 C50,-50,50,-70,30,-65 L0,-50" />
  <path class="ribbon" d="M0,-50 L-30,-50 C-50,-50,-50,-70,-30,-65 L0,-50" />
</svg>
</figure>