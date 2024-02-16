Once we covered basic shapes, it's time to move on to the `path` element. The path is the most powerful SVG element. We can define pretty much anything with paths and if you open any SVG file, you will mostly see paths. Let's draw this arrow using a single path.

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-70,0 L70,0 L30,-50 M70,0 L30,50" 
    fill="none" stroke="#D1495B" stroke-width="25" stroke-linecap="round" />
</svg>
</figure>

The shape of a path is defined by the `d` attribute. Here we define several drawing commands. A command always starts with a letter defining the command type and ends with a coordinate.

Here we only have the two most basic commands, move-to and line-to. The move-to command moves the cursor to a point without drawing a line and the line-to command draws a straight line from the previous point. A command always continues the previous command. When we draw a line we only define the endpoint. The starting point will be the previous command’s endpoint.

### Hamburger menu icon

Before we get to the arrow example, let’s draw a simple hamburger menu icon. We draw three lines within the same path with the move-to (`M`) and line-to (`L`) commands. First, we move to the start of the top line (`M -40, -40`) and draw a line to its end (`L 40, -40`).

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-40,-40 L40,-40" stroke="#333333" stroke-width="25" stroke-linecap="round" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-40,-40 L40,-40" stroke="#333333" stroke-width="25" stroke-linecap="round" />
</svg>
</figure>

Then we continue and draw to more lines the same way. What is cool about paths, is that they don't have to be continuous. We can have several move-to commands within the same path. The commas between the X and Y coordinates are optional. We skip them this time.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-40,-40 L40,-40 M-40,0 L40,0 M-40,40 L40,40" 
    stroke="#333333" stroke-width="25" stroke-linecap="round" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-40,-40 L40,-40 M-40,0 L40,0 M-40,40 L40,40" 
    stroke="#333333" stroke-width="25" stroke-linecap="round" />
</svg>
</figure>

### Heart shape icon

Here's another example made with a move to command and two line to commands.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-30,-20  L0,10 L30,-20" 
    fill="none" stroke="black" stroke-width="80" stroke-linecap="round" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-30,-20  L0,10 L30,-20" 
    fill="none" stroke="black" stroke-width="80" stroke-linecap="round" />
</svg>
</figure>

In the example above if we reduce the value of the `stroke-width` property, then we realize that the code above is actually a simple V shape.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-30,-20  L0,10 L30,-20" 
    fill="none" stroke="black" stroke-width="10" stroke-linecap="round" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-30,-20  L0,10 L30,-20" 
    fill="none" stroke="black" stroke-width="10" stroke-linecap="round" />
</svg>
</figure>

### Heart shape icon

We can draw an arrow in a very similar way. We start with a line in the middle, then we continue the line to draw the upper wing.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-70,0 L70,0 L30,-50" 
    fill="none" stroke="#D1495B" stroke-width="25" stroke-linecap="round" stroke-linejoin="round" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-70,0 L70,0 L30,-50" 
    fill="none" stroke="#D1495B" stroke-width="25" stroke-linecap="round" />
</svg>
</figure>

You might note that with the previous example, we also had a `stroke-linejoin` property to make the join rounded. It works in a similar way to `stroke-linecap` but that only affects the end of the lines. Without that property, the same line would look as follows.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-70,0 L70,0 L30,-50" 
    fill="none" stroke="#D1495B" stroke-width="25" stroke-linecap="round" stroke-linejoin="round" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-70,0 L70,0 L30,-50" 
    fill="none" stroke="#D1495B" stroke-width="25" stroke-linecap="round" />
</svg>
</figure>

Then we can finish the line with moving to the end of the horizontal line again, and drawing a straight line downwards to draw the lower wing of the arrow. You might notice that at the bottom of this and other pages in the navigation button we include a similar SVG.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-70,0 L70,0 L30,-50" 
    fill="none" stroke="#D1495B" stroke-width="25" stroke-linecap="round" stroke-linejoin="round" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-70,0 L70,0 L30,-50 M70,0 L30,50" 
    fill="none" stroke="#D1495B" stroke-width="25" stroke-linecap="round" />
</svg>
</figure>