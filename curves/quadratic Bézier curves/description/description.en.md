All paths we have drawn so far consisted of straight lines. Let's draw this curved Christmas tree.

<figure>
<svg width="200px" height="250px" viewBox="-100 -100 200 250">
  <rect x="-100" y="-100" width="200" height="250" fill="#F5F1EB"/>
  <path fill="none" stroke="#0C5C4C" stroke-width="5" d="
      M0,-80
      Q5,-75,0,-70
      Q-10,-65,0,-60
      Q15,-55,0,-50
      Q-20,-45,0,-40
      Q25,-35,0,-30
      Q-30,-25,0,-20
      Q35,-15,0,-10
      Q-40,-5,0,0
      Q45,5,0,10
      Q-50,15,0,20
      Q55,25,0,30
      Q-60,35,0,40
      Q65,45,0,50
      Q-70,55,0,60
      Q75,65,0,70
      Q-80,75,0,80
      Q85,85,0,90
      Q-90,95,0,100
      Q95,105,0,110
      Q-100,115,0,120
      L0,140 L20,140 L-20,140" />
</svg>
</figure>

The path element becomes really powerful when we start using curves. One of them is the **quadratic Bezier curve**. We not only set the endpoint, but we also have to set a control point.

The control point is an invisible coordinate to which the line is bending to, but not touching it. Look at this happy face! Here the invisible control point is at the middle of the bottom of the image (at coordinate `0,100`).

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <circle cx="-50" cy="-50" r="20" />
  <circle cx="50" cy="-50" r="20" />
  <path d="M-70,50 Q0,100,70,50" fill="none" stroke="black" stroke-width="10" stroke-linecap="round" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="-50" cy="-50" r="20" />
  <circle cx="50" cy="-50" r="20" />
  <path d="M-70,50 Q0,100,70,50" fill="none" stroke="black" stroke-width="10" stroke-linecap="round" />
</svg>
</figure>

In the example above the control point is at the same distance of the two endpoints. This is not necessary. In the example below we mark the control point with a circle. Note, that the control point and the circle have the same coordinates.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-50,50 Q50,-50,50,50" fill="none" stroke="black" stroke-width="5" />
  <circle cx="50" cy="-50" r="5" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-50,50 Q50,-50,50,50" fill="none" stroke="black" stroke-width="5" />
  <circle cx="50" cy="-50" r="5" />
</svg>
</figure>

Click here for [an interactive demo](https://hunormarton.github.io/svg-curves){: target="_blank"} of quadratic Bézier curves (select **Quadratic Bézier** at the top of the page).

To draw our curved Christmas tree, we have a series of quadratic Béziers where the control points get further and further away from the center of the tree as the path goes down.

```html
<svg width="200px" height="250px" viewBox="-100 -100 200 250">
  <path fill="none" stroke="#0C5C4C" stroke-width="5" d="
      M0,-80
      Q5,-75,0,-70
      Q-10,-65,0,-60
      Q15,-55,0,-50
      Q-20,-45,0,-40
      Q25,-35,0,-30
      Q-30,-25,0,-20
      Q35,-15,0,-10
      Q-40,-5,0,0
      Q45,5,0,10
      Q-50,15,0,20
      Q55,25,0,30
      Q-60,35,0,40
      Q65,45,0,50
      Q-70,55,0,60
      Q75,65,0,70
      Q-80,75,0,80
      Q85,85,0,90
      Q-90,95,0,100
      Q95,105,0,110
      Q-100,115,0,120
      L0,140 L20,140 L-20,140" />
</svg>
```

<figure>
<svg width="200px" height="250px" viewBox="-100 -100 200 250">
  <rect x="-100" y="-100" width="200" height="250" fill="#F5F1EB"/>
  <path fill="none" stroke="#0C5C4C" stroke-width="5" d="
      M0,-80
      Q5,-75,0,-70
      Q-10,-65,0,-60
      Q15,-55,0,-50
      Q-20,-45,0,-40
      Q25,-35,0,-30
      Q-30,-25,0,-20
      Q35,-15,0,-10
      Q-40,-5,0,0
      Q45,5,0,10
      Q-50,15,0,20
      Q55,25,0,30
      Q-60,35,0,40
      Q65,45,0,50
      Q-70,55,0,60
      Q75,65,0,70
      Q-80,75,0,80
      Q85,85,0,90
      Q-90,95,0,100
      Q95,105,0,110
      Q-100,115,0,120
      L0,140 L20,140 L-20,140" />
</svg>
</figure>

If we break down each quadratic bézier above into two line segments with the same coordinates, that would look like this:

```html
<svg width="200px" height="250px" viewBox="-100 -100 200 250">
  <path fill="none" stroke="black" stroke-width="1" d="
      M0,-80
      L5,-75      L0,-70
      L-10,-65    L0,-60
      L15,-55     L0,-50
      L-20,-45    L0,-40
      L25,-35     L0,-30
      L-30,-25    L0,-20
      L35,-15     L0,-10
      L-40,-5     L0,0
      L45,5       L0,10
      L-50,15     L0,20
      L55,25      L0,30
      L-60,35     L0,40
      L65,45      L0,50
      L-70,55     L0,60
      L75,65      L0,70
      L-80,75     L0,80
      L85,85      L0,90
      L-90,95     L0,100
      L95,105     L0,110
      L-100,115   L0,120
      L0,140 L20,140 L-20,140" />
</svg>
```

<figure>
<svg width="200px" height="250px" viewBox="-100 -100 200 250">
  <rect x="-100" y="-100" width="200" height="250" fill="#F5F1EB"/>
  <path fill="none" stroke="black" stroke-width="1" d="
      M0,-80
      L5,-75      L0,-70
      L-10,-65    L0,-60
      L15,-55     L0,-50
      L-20,-45    L0,-40
      L25,-35     L0,-30
      L-30,-25    L0,-20
      L35,-15     L0,-10
      L-40,-5     L0,0
      L45,5       L0,10
      L-50,15     L0,20
      L55,25      L0,30
      L-60,35     L0,40
      L65,45      L0,50
      L-70,55     L0,60
      L75,65      L0,70
      L-80,75     L0,80
      L85,85      L0,90
      L-90,95     L0,100
      L95,105     L0,110
      L-100,115   L0,120
      L0,140 L20,140 L-20,140" />
</svg>
</figure>