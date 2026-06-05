If you’re creating your own drawings, it can be helpful to display the **viewport**, or even to display the coordinate axes. We’ll briefly explain how to do this for a viewport with a width of 200 and a height of 200, where the origin (the point $$(0,0)$$) is located in the center of the viewport. The top-left corner of the viewport is therefore at the point $$(-100, -100)$$.

```html
<svg viewBox="-100 -100 200 200">
    ...
</svg> 
```

We also draw a transparent green circle with center at $$(30, 50)$$ and radius 40. We draw a small black circle to show the position of the center

```html
<circle cx="30" cy="50" r="40" fill="rgb(0,255,0,0.5)" />
<circle cx="30" cy="50" r="2" fill="black" />
```

### Draw the viewport

You can make the viewport visible by using the `style` attribute of the `svg` element to set the border to a thin (`1px`) black (`black`) dashed (`dashed`) line. We can also set the background color (`background-color`) to `#F5F1EB`.

```html
<svg width="400px" height="400px" viewBox="-100 -100 200 200" 
  style="border:dashed black 1px; background-color:#F5F1EB;"
>
    <circle cx="30" cy="50" r="40" fill="rgb(0,255,0,0.5)" />
    <circle cx="30" cy="50" r="2" fill="black" />
</svg>
```

<figure>
<svg width="400px" height="400px" viewBox="-100 -100 200 200" 
  style="border:dashed black 1px; background-color:#F5F1EB;"
>
    <circle cx="30" cy="50" r="40" fill="rgb(0,255,0,0.5)" />
    <circle cx="30" cy="50" r="2" fill="black" />
</svg>
</figure>

### Drawing the axis system

To place the elements of the diagram, it is helpful to have the coordinate axes handy. Below, we draw a thin blue line (both horizontal and vertical) at the tens along the axes, and slightly thicker lines at the hundreds. The origin $$(0,0)$$ lies at the center of the drawing, where the two thicker lines intersect.
```html
<svg width="400px" height="400px" viewBox="-100 -100 200 200">

    <style>
      .rooster { 
        display: initial;
      }
      .rooster path {
        fill: none;
        stroke: royalblue;
        stroke-width: 200;
      }
    </style>
      
    <g class="rooster">
      <path d="M-100,0 L200,0" stroke-dasharray="0.2,9.6,0.2,0"></path>
      <path d="M0,-100 L0,200" stroke-dasharray="0.2,9.6,0.2,0"></path>
      <path d="M-100,0 L200,0" stroke-dasharray="1,98,1,0"></path>
      <path d="M0,-100 L0,200" stroke-dasharray="1,98,1,0"></path>
    </g>

    <circle cx="30" cy="50" r="40" fill="rgb(0,255,0,0.5)" />
    <circle cx="30" cy="50" r="2" fill="black" />
  
</svg>
```

<figure>
<svg width="400px" height="400px" viewBox="-100 -100 200 200">

    <style>
      .rooster { 
        display: initial;
      }
      .rooster path {
        fill: none;
        stroke: royalblue;
        stroke-width: 200;
      }
    </style>
      
    <g class="rooster">
      <path d="M-100,0 L200,0" stroke-dasharray="0.2,9.6,0.2,0"></path>
      <path d="M0,-100 L0,200" stroke-dasharray="0.2,9.6,0.2,0"></path>
      <path d="M-100,0 L200,0" stroke-dasharray="1,98,1,0"></path>
      <path d="M0,-100 L0,200" stroke-dasharray="1,98,1,0"></path>
    </g>

    <circle cx="30" cy="50" r="40" fill="rgb(0,255,0,0.5)" />
    <circle cx="30" cy="50" r="2" fill="black" />
  
</svg>
</figure>

If you replace `display: initial;` with `display: none;` in the grid's display settings, the grid will be hidden. This allows you to quickly show and hide the grid.