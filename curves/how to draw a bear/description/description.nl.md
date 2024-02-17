As the ultimate drawing challenge let’s draw a bear.

<figure>
<svg class="bear" width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .bear {
      background-color: #f5eed7;
    }
    .bear .ear {
      fill: #e5c39c;
      stroke: white;
      stroke-width: 5;
    }    
    .bear .face {
      fill: white;
    }
    .bear .mouth {
      fill: none;
      stroke: black;
      stroke-width: 2;
    }
  </style>
  <circle class="ear" cx="-40" cy="-50" r="18" />
  <circle class="ear" cx="40" cy="-50" r="18" />
  <rect class="face" x="-55" y="-60" width="110" height="120" rx="50" ry="30" />
  <circle cx="20" cy="-30" r="3" />
  <circle cx="-20" cy="-30" r="3" />
  <path class="snout" fill="#E5C39C" d="
    M-30,0 C-30,-25,30,-25,30,0 
    L30,30 Q30,40,20,40 
    L-20,40 Q-30,40,-30,30" 
  />
  <path class="nose" d="M-10,0 L10,0 C10,20,-10,20,-10,0" />
  <path class="mouth" d="M0,10 Q0,25,10,25 M0,10 Q0,25,-10,25" />
</svg>
</figure>

We start with the ears. These are two circles that both have the `fill` and the `stroke` attributes set. We also defined a class on the SVG element to set the background color. Note, that here we set the regular `background-color` CSS property and not the `fill` attribute. Fill works with shapes, but the SVG element itself is not a shape.

```html
<svg class="bear" width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .bear {
      background-color: #f5eed7;
    }
    .bear .ear {
      fill: #e5c39c;
      stroke: white;
      stroke-width: 5;
    }    
  </style>
  <circle class="ear" cx="-40" cy="-50" r="18" />
  <circle class="ear" cx="40" cy="-50" r="18" />
</svg>
```

<figure>
<svg class="bear1" width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .bear1 {
      background-color: #f5eed7;
    }
    .bear1 .ear {
      fill: #e5c39c;
      stroke: white;
      stroke-width: 5;
    }    
  </style>
  <circle class="ear" cx="-40" cy="-50" r="18" />
  <circle class="ear" cx="40" cy="-50" r="18" />
</svg>
</figure>

Then let’s add the face and the eyes. Here’s another thing we haven’t covered before. Earlier we saw that we can round rectangles with the `rx` property. We can be even more specific and set a different radius on the $$y$$-axis with the `ry` property. If the latter is not set, it falls back to the other one.

```html
<svg class="bear" width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .bear {
      background-color: #f5eed7;
    }
    .bear .face {
      fill: white;
    }
  </style>
  <rect class="face" x="-55" y="-60" width="110" height="120" rx="50" ry="30" />
  <circle cx="20" cy="-30" r="3" />
  <circle cx="-20" cy="-30" r="3" />
</svg>
```

<figure>
<svg class="bear2" width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .bear2 {
      background-color: #f5eed7;
    }
    .bear2 .face {
      fill: white;
    }
  </style>
  <rect class="face" x="-55" y="-60" width="110" height="120" rx="50" ry="30" />
  <circle cx="20" cy="-30" r="3" />
  <circle cx="-20" cy="-30" r="3" />
</svg>
</figure>

Finally, we can add the nose and the mouth as a few paths as follows.

```html
<svg class="bear" width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .bear {
      background-color: #f5eed7;
    }
    .bear .mouth {
      fill: none;
      stroke: black;
      stroke-width: 2;
    }
  </style>
  <path class="snout" fill="#E5C39C" d="
    M-30,0 C-30,-25,30,-25,30,0 
    L30,30 Q30,40,20,40 
    L-20,40 Q-30,40,-30,30" 
  />
  <path class="nose" d="M-10,0 L10,0 C10,20,-10,20,-10,0" />
  <path class="mouth" d="M0,10 Q0,25,10,25 M0,10 Q0,25,-10,25" />
</svg>
```

<figure>
<svg class="bear3" width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .bear3 {
      background-color: #f5eed7;
    }
    .bear3 .mouth {
      fill: none;
      stroke: black;
      stroke-width: 2;
    }
  </style>
  <path class="snout" fill="#E5C39C" d="
    M-30,0 C-30,-25,30,-25,30,0 
    L30,30 Q30,40,20,40 
    L-20,40 Q-30,40,-30,30" 
  />
  <path class="nose" d="M-10,0 L10,0 C10,20,-10,20,-10,0" />
  <path class="mouth" d="M0,10 Q0,25,10,25 M0,10 Q0,25,-10,25" />
</svg>
</figure>

Once we put it all together we end up with the image on the bear.

```html
<svg class="bear" width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .bear {
      background-color: #f5eed7;
    }
    .bear .ear {
      fill: #e5c39c;
      stroke: white;
      stroke-width: 5;
    }    
    .bear .face {
      fill: white;
    }
    .bear .mouth {
      fill: none;
      stroke: black;
      stroke-width: 2;
    }
  </style>
  <circle class="ear" cx="-40" cy="-50" r="18" />
  <circle class="ear" cx="40" cy="-50" r="18" />
  <rect class="face" x="-55" y="-60" width="110" height="120" rx="50" ry="30" />
  <circle cx="20" cy="-30" r="3" />
  <circle cx="-20" cy="-30" r="3" />
  <path class="snout" fill="#E5C39C" d="
    M-30,0 C-30,-25,30,-25,30,0 
    L30,30 Q30,40,20,40 
    L-20,40 Q-30,40,-30,30" 
  />
  <path class="nose" d="M-10,0 L10,0 C10,20,-10,20,-10,0" />
  <path class="mouth" d="M0,10 Q0,25,10,25 M0,10 Q0,25,-10,25" />
</svg>
```

<figure>
<svg class="bear4" width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .bear4 {
      background-color: #f5eed7;
    }
    .bear4 .ear {
      fill: #e5c39c;
      stroke: white;
      stroke-width: 5;
    }    
    .bear4 .face {
      fill: white;
    }
    .bear4 .mouth {
      fill: none;
      stroke: black;
      stroke-width: 2;
    }
  </style>
  <circle class="ear" cx="-40" cy="-50" r="18" />
  <circle class="ear" cx="40" cy="-50" r="18" />
  <rect class="face" x="-55" y="-60" width="110" height="120" rx="50" ry="30" />
  <circle cx="20" cy="-30" r="3" />
  <circle cx="-20" cy="-30" r="3" />
  <path class="snout" fill="#E5C39C" d="
    M-30,0 C-30,-25,30,-25,30,0 
    L30,30 Q30,40,20,40 
    L-20,40 Q-30,40,-30,30" 
  />
  <path class="nose" d="M-10,0 L10,0 C10,20,-10,20,-10,0" />
  <path class="mouth" d="M0,10 Q0,25,10,25 M0,10 Q0,25,-10,25" />
</svg>
</figure>
