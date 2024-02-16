Let’s have another example with cubic and quadratic beziers.

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <g stroke="black" stroke-width="2">
    <circle cx="0" cy="-45" r="7" fill="#4F6D7A" />
    <circle cx="0" cy="50" r="10" fill="#F79257" />
    <path fill="#FDEA96" d="
        M-50,40
        L-50,50
        L50,50
        L50,40
        Q40,40,40,10
        C40,-60,-40,-60,-40,10
        Q-40,40,-50,40"
    />
  </g>
</svg>
</figure>

Here the bottom of this bell is defined with straight lines.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path fill="#FDEA96" stroke="black" stroke-width="2" d="
      M-50,40
      L-50,50
      L50,50
      L50,40"
  />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path fill="#FDEA96" stroke="black" stroke-width="2" d="
      M-50,40
      L-50,50
      L50,50
      L50,40"
  />
</svg>
</figure>

Then a quadratic Béziers starts the bell cloak.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path fill="#FDEA96" stroke="black" stroke-width="2" d="
      M-50,40
      L-50,50
      L50,50
      L50,40
      Q40,40,40,10"
  />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path fill="#FDEA96" stroke="black" stroke-width="2" d="
      M-50,40
      L-50,50
      L50,50
      L50,40
      Q40,40,40,10"
  />
  <circle cx="40" cy="40" r="2" stroke="none" fill="red"></circle>
</svg>
</figure>

Then the line is continued with a cubic Bézier to form the top of the bell.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path fill="#FDEA96" stroke="black" stroke-width="2" d="
      M-50,40
      L-50,50
      L50,50
      L50,40
      Q40,40,40,10
      C40,-60,-40,-60,-40,10"
  />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path fill="#FDEA96" stroke="black" stroke-width="2" d="
      M-50,40
      L-50,50
      L50,50
      L50,40
      Q40,40,40,10
      C40,-60,-40,-60,-40,10"
  />
  <circle cx="-40" cy="-60" r="2" stroke="none" fill="red"></circle>
  <circle cx="40" cy="-60" r="2" stroke="none" fill="red"></circle>
</svg>
</figure>

Then we reach the bottom part with another quadratic bezier that mirrors the previous one.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path fill="#FDEA96" stroke="black" stroke-width="2" d="
      M-50,40
      L-50,50
      L50,50
      L50,40
      Q40,40,40,10
      C40,-60,-40,-60,-40,10
      Q-40,40,-50,40"
  />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path fill="#FDEA96" stroke="black" stroke-width="2" d="
      M-50,40
      L-50,50
      L50,50
      L50,40
      Q40,40,40,10
      C40,-60,-40,-60,-40,10
      Q-40,40,-50,40"
  />
  <circle cx="-40" cy="40" r="2" stroke="none" fill="red"></circle>
</svg>
</figure>


We finish the bell, by adding two circles for the bell-clapper, and the hanger.


```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <g stroke="black" stroke-width="2">
    <circle cx="0" cy="-45" r="7" fill="#4F6D7A" />
    <circle cx="0" cy="50" r="10" fill="#F79257" />
    <path fill="#FDEA96" d="
        M-50,40
        L-50,50
        L50,50
        L50,40
        Q40,40,40,10
        C40,-60,-40,-60,-40,10
        Q-40,40,-50,40"
    />
  </g>
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <g stroke="black" stroke-width="2">
    <circle cx="0" cy="-45" r="7" fill="#4F6D7A" />
    <circle cx="0" cy="50" r="10" fill="#F79257" />
    <path fill="#FDEA96" d="
        M-50,40
        L-50,50
        L50,50
        L50,40
        Q40,40,40,10
        C40,-60,-40,-60,-40,10
        Q-40,40,-50,40"
    />
  </g>
</svg>
</figure>
