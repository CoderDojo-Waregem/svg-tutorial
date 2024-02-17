An arc is part of a circle or ellipse. Let's see how we can use arcs to draw this candy.

<figure>
<svg width="200px" height="400px" viewBox="-100 -200 200 400">
  <style>
    .body {
      stroke-linecap: round;
      fill: none;
    }    
    .red-mark {
      stroke: #d1495b;
      stroke-width: 2.5;
    }
    .green-mark {
      stroke: #234236;
      stroke-width: 2.5;
    }
  </style>

  <rect x="-100" y="-200" width="200" height="400" fill="#F5F1EB"/>
  <path class="body" d="M50,120 L50,-80 A50,50,0,0,0,-50,-80" stroke="#cd803d" stroke-width="45" />
  <path class="body" d="M50,120 L50,-80 A50,50,0,0,0,-50,-80" stroke="white" stroke-width="40" />
  <line class="green-mark" x1="-35" y1="-90" x2="-60" y2="-100" />
  <line class="red-mark" x1="-15" y1="-115" x2="-25" y2="-135" />
  <line class="green-mark" x1="20" y1="-110" x2="35" y2="-130" />
  <line class="red-mark" x1="40" y1="-60" x2="60" y2="-80" />
  <line class="green-mark" x1="40" y1="-10" x2="60" y2="-30" />
  <line class="red-mark" x1="40" y1="40" x2="60" y2="20" />
  <line class="green-mark" x1="40" y1="90" x2="60" y2="70" />
</svg>
</figure>

If you thought that cubic Béziers are the most complicated parts of an SVG then we have bad news for you. Arcs are way more complicated. The good news though, is that they are rarely used, and we won’t use them much in the upcoming examples either.

### The different parameters of an arc

The arc to command has 7 parameters.

<pre>
A rx ry rotation large-arc-flag sweep-flag x y
</pre>

The last two parameters `(40, 40)` are still the endpoint of the arc. The first two define a horizontal and a vertical radius `(70, 70)`. If we draw a circle, those two values are the same.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-40,-40 A70,70,0,0,0,40,40" fill="none" stroke="red" stroke-width="2" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-40,-40 A70,70,0,0,0,40,40" fill="none" stroke="red" stroke-width="2" />
</svg>
</figure>

You might realize that even with the same starting point and endpoint, and the same radii, there can be four different variations. The 5th argument is a boolean flag, and we can use it to flip the arc the other way (now it changed to `1`).


```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-40,-40 A70,70,0,0,1,40,40" fill="none" stroke="red" stroke-width="2" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-40,-40 A70,70,0,0,1,40,40" fill="none" stroke="red" stroke-width="2" />
</svg>
</figure>

You might notice that in both cases, the arc ends up the shortest possible way with these parameters. It is also possible to go the long way and still keep the same start and endpoints, and the same radii. Then the 4th argument is another boolean flag that sets if we want to go the long way (now we also changed it to `1`). This also has two variations. You can mirror it, by flipping the 5th argument to the other value.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-40,-40 A70,70,0,1,1,40,40" fill="none" stroke="red" stroke-width="2" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-40,-40 A70,70,0,1,1,40,40" fill="none" stroke="red" stroke-width="2" />
</svg>
</figure>

To complicate things even further, if we set the horizontal and vertical radii to two different values then we end up with an arc of an ellipse `(70, 40)`. Again, the same start and end points, and this also has 4 different variations.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-40,-40 A70,40,0,1,1,40,40" fill="none" stroke="red" stroke-width="2" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-40,-40 A70,40,0,1,1,40,40" fill="none" stroke="red" stroke-width="2" />
</svg>
</figure>

Finally, if we draw an ellipse we can also turn it by an angle. We can set this by the 3rd parameter (`30`). What makes things even more twisted, is that our imaginary ellipse is not rotated around its center, because this arc still has to maintain the same start and end points. In case we draw a circle, the rotation does not affect the arc.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-40,-40 A70,40,30,1,1,40,40" fill="none" stroke="red" stroke-width="2" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-40,-40 A70,40,30,1,1,40,40" fill="none" stroke="red" stroke-width="2" />
</svg>
</figure>

Click here for [an interactive demo](https://hunormarton.github.io/svg-curves){: target="_blank"} of arcs.

### Drawing a candy

Now after all these introductions we finally got to today’s example. We are only going to draw a simple arc in this one.

```html
<svg width="200px" height="400px" viewBox="-100 -200 200 400">
  <style>
    .body {
      stroke-linecap: round;
      fill: none;
    }    
  </style>

  <path class="body" d="M50,120 L50,-80 A50,50,0,0,0,-50,-80" stroke="#cd803d" stroke-width="45" />
</svg>
```

<figure>
<svg width="200px" height="400px" viewBox="-100 -200 200 400">
  <style>
    .body {
      stroke-linecap: round;
      fill: none;
    }    
  </style>

  <rect x="-100" y="-200" width="200" height="400" fill="#F5F1EB"/>
  <path class="body" d="M50,120 L50,-80 A50,50,0,0,0,-50,-80" stroke="#cd803d" stroke-width="45" />
</svg>
</figure>

To draw a candy, we draw a thick line that consists of a straight line and a half circle. Then we draw the same line again, with a slightly thinner stroke width. By setting two different colors for them, they will look as if one is the border of the other.

For the finishing touches, we add a few straight lines inside this shape as markings.

```html
<svg width="200px" height="400px" viewBox="-100 -200 200 400">
  <style>
    .body {
      stroke-linecap: round;
      fill: none;
    }    
    .red-mark {
      stroke: #d1495b;
      stroke-width: 2.5;
    }
    .green-mark {
      stroke: #234236;
      stroke-width: 2.5;
    }
  </style>

  <path class="body" d="M50,120 L50,-80 A50,50,0,0,0,-50,-80" stroke="#cd803d" stroke-width="45" />
  <path class="body" d="M50,120 L50,-80 A50,50,0,0,0,-50,-80" stroke="white" stroke-width="40" />
  <line class="green-mark" x1="-35" y1="-90" x2="-60" y2="-100" />
  <line class="red-mark" x1="-15" y1="-115" x2="-25" y2="-135" />
  <line class="green-mark" x1="20" y1="-110" x2="35" y2="-130" />
  <line class="red-mark" x1="40" y1="-60" x2="60" y2="-80" />
  <line class="green-mark" x1="40" y1="-10" x2="60" y2="-30" />
  <line class="red-mark" x1="40" y1="40" x2="60" y2="20" />
  <line class="green-mark" x1="40" y1="90" x2="60" y2="70" />
</svg>
```

<figure>
<svg width="200px" height="400px" viewBox="-100 -200 200 400">
  <style>
    .body {
      stroke-linecap: round;
      fill: none;
    }    
    .red-mark {
      stroke: #d1495b;
      stroke-width: 2.5;
    }
    .green-mark {
      stroke: #234236;
      stroke-width: 2.5;
    }
  </style>

  <rect x="-100" y="-200" width="200" height="400" fill="#F5F1EB"/>
  <path class="body" d="M50,120 L50,-80 A50,50,0,0,0,-50,-80" stroke="#cd803d" stroke-width="45" />
  <path class="body" d="M50,120 L50,-80 A50,50,0,0,0,-50,-80" stroke="white" stroke-width="40" />
  <line class="green-mark" x1="-35" y1="-90" x2="-60" y2="-100" />
  <line class="red-mark" x1="-15" y1="-115" x2="-25" y2="-135" />
  <line class="green-mark" x1="20" y1="-110" x2="35" y2="-130" />
  <line class="red-mark" x1="40" y1="-60" x2="60" y2="-80" />
  <line class="green-mark" x1="40" y1="-10" x2="60" y2="-30" />
  <line class="red-mark" x1="40" y1="40" x2="60" y2="20" />
  <line class="green-mark" x1="40" y1="90" x2="60" y2="70" />
</svg>
</figure>
