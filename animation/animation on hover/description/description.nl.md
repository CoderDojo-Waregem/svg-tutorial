We kunnen ook meer traditionele animaties instellen met CSS. Hier animeren we de `transform` eigenschap met keyframes. We kunnen dit effect bijvoorbeeld activeren als de muisaanwijzer boven de klok geplaatst wordt.

<figure>
<svg class="klok" width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .klok:hover {
      transform-origin: center 30%;
    }
    
    .klok:hover,
    .klok:hover .klepel {
      animation-duration: 0.5s;
      animation-delay: -0.25s;
      animation-iteration-count: infinite;
      animation-direction: alternate;
      animation-timing-function: ease-in-out;
      animation-name: rinkelen;
    }
    
    @keyframes rinkelen {
      from { transform: rotate(-20deg); }
      to { transform: rotate(20deg); }
    }
  </style>
  
  <g stroke="#001514" stroke-width="2">
    <circle cx="0" cy="-45" r="7" fill="#4F6D7A" />
    <circle class="klepel" cx="0" cy="50" r="10" fill="#F79257" />
    <path fill="#FDEA96"
      d="M-50,40 L-50,50 L50,50 L50,40 Q40,40,40,10
        C40,-60,-40,-60,-40,10 Q-40,40,-50,40"
    />
  </g>
</svg>
</figure>

Hiervoor hergebruiken we het voorbeeld van de klok dat we eerder besproken hebben. We voegen aan het zweven een keyframe-animatie toe op zowel de volledige klok als de klepel.

```html
<svg class="klok" width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .klok:hover {
      transform-origin: center 30%;
    }
    
    .klok:hover,
    .klok:hover .klepel {
      animation-duration: 0.5s;
      animation-delay: -0.25s;
      animation-iteration-count: infinite;
      animation-direction: alternate;
      animation-timing-function: ease-in-out;
      animation-name: rinkelen;
    }
    
    @keyframes rinkelen {
      from { transform: rotate(-20deg); }
      to { transform: rotate(20deg); }
    }
  </style>
  
  <g stroke="#001514" stroke-width="2">
    <circle cx="0" cy="-45" r="7" fill="#4F6D7A" />
    <circle class="klepel" cx="0" cy="50" r="10" fill="#F79257" />
    <path fill="#FDEA96"
      d="M-50,40 L-50,50 L50,50 L50,40 Q40,40,40,10
        C40,-60,-40,-60,-40,10 Q-40,40,-50,40"
    />
  </g>
</svg>
```

<figure>
<svg class="klok1" width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .klok1:hover {
      transform-origin: center 30%;
    }
    
    .klok1:hover,
    .klok1:hover .klepel1 {
      animation-duration: 0.5s;
      animation-delay: -0.25s;
      animation-iteration-count: infinite;
      animation-direction: alternate;
      animation-timing-function: ease-in-out;
      animation-name: rinkelen1;
    }
    
    @keyframes rinkelen1 {
      from { transform: rotate(-20deg); }
      to { transform: rotate(20deg); }
    }
  </style>
  
  <g stroke="#001514" stroke-width="2">
    <circle cx="0" cy="-45" r="7" fill="#4F6D7A" />
    <circle class="klepel1" cx="0" cy="50" r="10" fill="#F79257" />
    <path fill="#FDEA96"
      d="M-50,40 L-50,50 L50,50 L50,40 Q40,40,40,10
        C40,-60,-40,-60,-40,10 Q-40,40,-50,40"
    />
  </g>
</svg>
</figure>
