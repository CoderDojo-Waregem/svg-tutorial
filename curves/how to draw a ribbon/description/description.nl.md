After we learned about quadratic Bézier curves and cubic Bézier curves, let's do another practice round where we use both to draw this ribbon.

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
      <path fill="#B73A3B" id="ribbon" d="
        M0,-20 Q28,-40,56,-45 C96,-48,96,48,56,45 Q28,40,0,20" 
      />
  </defs>

  <rect x="-100" y="-200" width="200" height="400" fill="#F5F1EB"/>
  <use href="#ribbon" />
  <use href="#ribbon" transform="scale(-1)" />
  <ellipse cx="0" cy="0" rx="20" ry="24" fill="#9C2D2A" />
  <path fill="none" stroke="#B73A3B" stroke-width="3" d="
    M0,20 Q40,40,30,60 Q20,80,40,90 
    M0,20 Q-30,30,-20,60 Q-10,90,-50,100"
  />
</svg>
</figure>

We start with the right side of the ribbon with a quadratic Bézier curve. The dot represents the control point again.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path fill="#B73A3B" d="
    M0,-20
    Q28,-40,56,-45"
  />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-200" width="200" height="400" fill="#F5F1EB"/>
  <circle cx="28" cy="-40" r="2"></circle>
  <path fill="#B73A3B" d="
    M0,-20
    Q28,-40,56,-45"
  />
</svg>
</figure>

Then we continue with a cubic Bézier.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path fill="#B73A3B" d="
    M0,-20
    Q28,-40,56,-45
    C96,-48,96,48,56,45"
  />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-200" width="200" height="400" fill="#F5F1EB"/>
  <circle cx="96" cy="-48" r="2"></circle>
  <circle cx="96" cy="48" r="2"></circle>
  <path fill="#B73A3B" d="
    M0,-20
    Q28,-40,56,-45
    C96,-48,96,48,56,45"
  />
</svg>
</figure>

And finish up with another quadratic cubic Bézier that mirrors the first one.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path fill="#B73A3B" d="
    M0,-20
    Q28,-40,56,-45
    C96,-48,96,48,56,45
    Q28,40,0,20"
  />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-200" width="200" height="400" fill="#F5F1EB"/>
  <circle cx="28" cy="40" r="2"></circle>
  <path fill="#B73A3B" d="
    M0,-20
    Q28,-40,56,-45
    C96,-48,96,48,56,45
    Q28,40,0,20"
  />
</svg>
</figure>

Then we can move the whole shape into a reusable component and use it for both sizes. Note that to mirror it to the left side we use negative scaling.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
      <path fill="#B73A3B" id="ribbon" d="
        M0,-20 Q28,-40,56,-45 C96,-48,96,48,56,45 Q28,40,0,20" 
      />
  </defs>

  <use href="#ribbon" />
  <use href="#ribbon" transform="scale(-1)" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
      <path fill="#B73A3B" id="ribbon" d="
        M0,-20 Q28,-40,56,-45 C96,-48,96,48,56,45 Q28,40,0,20" 
      />
  </defs>

  <rect x="-100" y="-200" width="200" height="400" fill="#F5F1EB"/>
  <use href="#ribbon" />
  <use href="#ribbon" transform="scale(-1)" />
</svg>
</figure>

We finish up the image by adding an `ellipse` element in the middle and a stroke for the rest.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
      <path fill="#B73A3B" id="ribbon" d="
        M0,-20 Q28,-40,56,-45 C96,-48,96,48,56,45 Q28,40,0,20" 
      />
  </defs>

  <use href="#ribbon" />
  <use href="#ribbon" transform="scale(-1)" />
  <ellipse cx="0" cy="0" rx="20" ry="24" fill="#9C2D2A" />
  <path fill="none" stroke="#B73A3B" stroke-width="3" d="
    M0,20 Q40,40,30,60 Q20,80,40,90 
    M0,20 Q-30,30,-20,60 Q-10,90,-50,100"
  />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
      <path fill="#B73A3B" id="ribbon" d="
        M0,-20 Q28,-40,56,-45 C96,-48,96,48,56,45 Q28,40,0,20" 
      />
  </defs>

  <rect x="-100" y="-200" width="200" height="400" fill="#F5F1EB"/>
  <use href="#ribbon" />
  <use href="#ribbon" transform="scale(-1)" />
  <ellipse cx="0" cy="0" rx="20" ry="24" fill="#9C2D2A" />
  <path fill="none" stroke="#B73A3B" stroke-width="3" d="
    M0,20 Q40,40,30,60 Q20,80,40,90 
    M0,20 Q-30,30,-20,60 Q-10,90,-50,100"
  />
</svg>
</figure>
