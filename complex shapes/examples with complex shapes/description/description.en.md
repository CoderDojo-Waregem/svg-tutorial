Now that you have mastered the basic shapes, it is time to make your own drawing. Find a drawing that can be composed of basic shapes. Below we give a few possibilities.

### Poké ball

<figure>
<svg id="pokemon" xmlns="http://www.w3.org/2000/svg" version="1.1" width="400px" height="400px" viewBox="-100 -100 200 200">

  <defs>
    <radialGradient id="licht" cx="0.25" cy="0.20" r="0.35">
      <stop offset="0%" stop-color="rgb(255,255,255,0.75)" />
      <stop offset="100%" stop-color="rgb(255,0,0,0.0)" />
    </radialGradient>
    <radialGradient id="donker" cx="0.25" cy="0.25" r="1">
      <stop offset="0%" stop-color="white" />
      <stop offset="50%" stop-color="white" />
      <stop offset="100%" stop-color="#d6d6d6" />
    </radialGradient>
  </defs>

  <style>
    #pokemon .rooster {
      display: none;
    }
    #pokemon .rooster path {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
  </style>

  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB" />

  <g class="rooster">
    <path d="M-90,0 L180,0" stroke-dasharray="0.2,9.6,0.2,0"></path>
    <path d="M0,-90 L0,180" stroke-dasharray="0.2,9.6,0.2,0"></path>
    <path d="M-90,0 L180,0" stroke-dasharray="1,98,1,0"></path>
    <path d="M0,-90 L0,180" stroke-dasharray="1,98,1,0"></path>
  </g>

  <path stroke="none" fill="rgb(255,0,0,0.6)" d="
    M -90,0
    L 90,0
    A 90,90,0,0,0,-90,0"
  />
  <path stroke="none" fill="url(#donker)" d="
    M -90,0
    L 90,0
    A 90,90,0,0,1,-90,0"
  />

  <line x1="-90" y1="0" x2="90" y2="0" stroke="black" stroke-width="6" />
  <circle cx="0" cy="0" r="30" fill="white" stroke="black" stroke-width="6" />
  <circle cx="0" cy="0" r="20" fill="white" stroke="black" stroke-width="6" />
  <circle cx="0" cy="0" r="90" fill="url(#licht)"/>
  <circle cx="0" cy="0" r="90" fill="none" stroke="black" stroke-width="6" />

</svg>
</figure>

### Sport field

What does the field of your favourite sport look like? Search online for the elements of the sports field and their dimensions.

<figure>
<svg id="soccer" xmlns="http://www.w3.org/2000/svg" version="1.1" width="560px" height="360px" viewBox="-70 -45 140 90">

  <style>
    #soccer .chalk {
      fill: none;
      stroke: white;
      stroke-width: 0.5;
    }
  </style>

  <defs>
    <clipPath id="speelveld">
      <rect x="-43.5" y="-10" width="10" height="20"  />
    </clipPath>
    <g id="half">
      <rect class="chalk" x="-60" y="-20.16" width="16.5" height="40.32" />
      <rect class="chalk" x="-60" y="-9.16" width="5.5" height="18.32" />
      <circle cx="-49" cy="0" r=".5" fill="white" stroke="none" />
      <circle class="chalk" cx="-49" cy="0" r="9.15" fill="none" clip-path="url(#speelveld)" />
      <path class="chalk" d="M-60,39 A1,1,0,0,1,-59,40" />
      <path class="chalk" d="M-60,-39 A1,1,0,0,0,-59,-40" />
      <rect class="chalk" x="-64" y="-3.66" width="4" height="7.32" />
      <line x1="-64" y1="0" x2="-60" y2="0" fill="none" stroke="white" stroke-width="7.32" stroke-dasharray="0.1 0.4" />
      <line x1="-62" y1="-3.66" x2="-62" y2="3.66" fill="none" stroke="white" stroke-width="4" stroke-dasharray="0.1 0.4" />
    </g>
  </defs>

  <rect x="-70" y="-50" width="140" height="100" fill="#3fb55d" stroke="none" />
  <line x1="-70" y1="0" x2="70" y2="0" stroke="#32ac57" stroke-width="100" stroke-dasharray="2.5 5 2.5 0" />

  <rect class="chalk" x="-60" y="-40" width="120" height="80" />
  <line class="chalk" x1="0" y1="-40" x2="0" y2="40" />
  <use href="#half" x="0" y="0" />
  <use href="#half" x="0" y="0" transform="scale(-1.0)" />

  <circle cx="0" cy="0" r=".5" fill="white" stroke="none" />
  <circle class="chalk" cx="0" cy="0" r="9.15" />

</svg>
</figure>
