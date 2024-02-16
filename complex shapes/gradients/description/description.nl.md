The filling of a shape can be defined as a gradient. We add a subtle 3D effect to our Christmas decoration and build a snowman.

<figure>
<svg width="200px" height="250px" viewBox="-100 -100 200 250" 
  style="background-color: lightblue">
  <defs>
    <radialGradient id="snowball" cx="0.25" cy="0.25" r="1">
      <stop offset="0%" stop-color="white" />
      <stop offset="50%" stop-color="white" />
      <stop offset="100%" stop-color="#d6d6d6" />
    </radialGradient>
  </defs>

  <circle cx="0" cy="60" r="80" fill="url(#snowball)" />
  <circle cx="0" cy="-40" r="50" fill="url(#snowball)" />
  <polygon points="10,-46 50,-40 10,-34" fill="#e66465" />

  <circle cx="0" cy="-55" r="5" />
  <circle cx="20" cy="-55" r="5" />

  <line x1="-40" y1="30" x2="-90" y2="-30" stroke="black" stroke-width="5" />
  <line x1="-65" y1="0" x2="-90" y2="-10" stroke="black" stroke-width="5" />
</svg>
</figure>

### Upgrade the Christmas Ornament

Let’s upgrade the Christmas Ornament we created before.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
    <clipPath id="ball1">
      <circle cx="0" cy="20" r="70" />
    </clipPath>
  </defs>

  <circle cx="0" cy="20" r="70" fill="#D1495B" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257" />
  <circle cx="0" cy="-75" r="12" fill="none" stroke="#F79257" stroke-width="2" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
    <clipPath id="ball1">
      <circle cx="0" cy="20" r="70" />
    </clipPath>
  </defs>

  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="20" r="70" fill="#D1495B" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257" />
  <circle cx="0" cy="-75" r="12" fill="none" stroke="#F79257" stroke-width="2" />
</svg>
</figure>

We can add a subtle 3D effect by filling the main circle with a gradient. Here we define a `radialGradient` in the `defs` section. It has a different syntax than CSS, but the capabilities are rather similar.

We define its ID, center position with `cx` and `cy`, set its radius, and the stop colors. Then we can use it as an attribute for the `fill` property of a shape.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
    <radialGradient id="shine" cx="0.25" cy="0.25" r="0.35">
      <stop offset="0%" stop-color="#e3a8b0" />
      <stop offset="100%" stop-color="#D1495B" />
    </radialGradient>
  </defs>

  <circle cx="0" cy="20" r="70" fill="url(#shine)" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257"  />
  <circle cx="0" cy="-75" r="12" fill="none" stroke="#F79257" stroke-width="2" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
    <radialGradient id="shine" cx="0.25" cy="0.25" r="0.35">
      <stop offset="0%" stop-color="#e3a8b0" />
      <stop offset="100%" stop-color="#D1495B" />
    </radialGradient>
  </defs>

  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="20" r="70" fill="url(#shine)" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257"  />
  <circle cx="0" cy="-75" r="12" fill="none" stroke="#F79257" stroke-width="2" />
</svg>
</figure>

### Building a Snowman

For the snowman we draw two circles with a similar gradient as follows.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200" 
  style="background-color: lightblue">
  <defs>
    <radialGradient id="snowball" cx="0.25" cy="0.25" r="1">
      <stop offset="0%" stop-color="white" />
      <stop offset="50%" stop-color="white" />
      <stop offset="100%" stop-color="#d6d6d6" />
    </radialGradient>
  </defs>

  <circle cx="0" cy="0" r="80" fill="url(#snowball)" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200" 
  style="background-color: lightblue">
  <defs>
    <radialGradient id="snowball1" cx="0.25" cy="0.25" r="1">
      <stop offset="0%" stop-color="white" />
      <stop offset="50%" stop-color="white" />
      <stop offset="100%" stop-color="#d6d6d6" />
    </radialGradient>
  </defs>

  <circle cx="0" cy="0" r="80" fill="url(#snowball1)" />
</svg>
</figure>

Then we add a polygon for the nose, two circles for the eyes, and two lines for the arm. Simple.

```html
<svg width="200px" height="250px" viewBox="-100 -100 200 250" 
  style="background-color: lightblue">
  <defs>
    <radialGradient id="snowball" cx="0.25" cy="0.25" r="1">
      <stop offset="0%" stop-color="white" />
      <stop offset="50%" stop-color="white" />
      <stop offset="100%" stop-color="#d6d6d6" />
    </radialGradient>
  </defs>

  <circle cx="0" cy="60" r="80" fill="url(#snowball)" />
  <circle cx="0" cy="-40" r="50" fill="url(#snowball)" />
  <polygon points="10,-46 50,-40 10,-34" fill="#e66465" />

  <circle cx="0" cy="-55" r="5" />
  <circle cx="20" cy="-55" r="5" />

  <line x1="-40" y1="30" x2="-90" y2="-30" stroke="black" stroke-width="5" />
  <line x1="-65" y1="0" x2="-90" y2="-10" stroke="black" stroke-width="5" />
</svg>
```

<figure>
<svg width="200px" height="250px" viewBox="-100 -100 200 250" 
  style="background-color: lightblue">
  <defs>
    <radialGradient id="snowball2" cx="0.25" cy="0.25" r="1">
      <stop offset="0%" stop-color="white" />
      <stop offset="50%" stop-color="white" />
      <stop offset="100%" stop-color="#d6d6d6" />
    </radialGradient>
  </defs>

  <circle cx="0" cy="60" r="80" fill="url(#snowball2)" />
  <circle cx="0" cy="-40" r="50" fill="url(#snowball2)" />
  <polygon points="10,-46 50,-40 10,-34" fill="#e66465" />

  <circle cx="0" cy="-55" r="5" />
  <circle cx="20" cy="-55" r="5" />

  <line x1="-40" y1="30" x2="-90" y2="-30" stroke="black" stroke-width="5" />
  <line x1="-65" y1="0" x2="-90" y2="-10" stroke="black" stroke-width="5" />
</svg>
</figure>