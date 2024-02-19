Now that you have mastered the basic shapes, it is time to make your own drawing. Find a drawing that can be composed of basic shapes. Below we give a few possibilities.

### Flags

Most countries have flags consisting of rectangles, triangles, lines and circles. Below you can see some possibilities in advance. Do you know which countries those flags belong to? Find some flags of your own that you can draw.

<figure>
<svg width="550px" height="400px" viewBox="0 0 1100 800">

  <rect x="0" y="0" width="1100" height="800" fill="#F1DBC3" />

  <g id="belgium" transform="translate(50,50)" >
    <rect x="0" y="0" width="100" height="200" fill="black" />
    <rect x="100" y="0" width="100" height="200" fill="#fedd02" />
    <rect x="200" y="0" width="100" height="200" fill="#ee1b2a" />
  </g>

  <g id="netherlands" transform="translate(400,50)" >
    <rect x="0" y="0" width="300" height="200" fill="white" />
    <rect x="0" y="0" width="300" height="66.66" fill="#a21d22" />
    <rect x="0" y="133.333" width="300" height="66.66" fill="#263e86" />
  </g>

  <g id="norway" transform="translate(750,50)" >
    <rect x="0" y="0" width="300" height="200" fill="#fe0000" />
    <line x1="0" y1="100" x2="300" y2="100" stroke="white" stroke-width="40"/>
    <line x1="100" y1="0" x2="100" y2="200" stroke="white" stroke-width="40"/>
    <line x1="0" y1="100" x2="300" y2="100" stroke="#042568" stroke-width="20"/>
    <line x1="100" y1="0" x2="100" y2="200" stroke="#042568" stroke-width="20"/>
  </g>

  <g id="greece" transform="translate(50,300)" >
    <rect x="0" y="0" width="300" height="200" fill="#3b50a9" />
    <line x1="150" y1="0" x2="150" y2="200" stroke="white" stroke-width="300" stroke-dasharray="22.222 22.222" stroke-dashoffset="22.22" />
    <rect x="0" y="0" width="111.111" height="111.111" fill="#3b50a9" />
    <line x1="0" y1="55.555" x2="111.111" y2="55.555" stroke="white" stroke-width="22.222" />
    <line x1="55.555" y1="0" x2="55.555" y2="112.111" stroke="white" stroke-width="22.222" />
  </g>

  <g id="switzerland" transform="translate(400,300)" >
    <rect x="0" y="0" width="300" height="200" fill="#d82b25" />
    <line x1="100" y1="100" x2="200" y2="100" stroke="white" stroke-width="40"/>
    <line x1="150" y1="50" x2="150" y2="150" stroke="white" stroke-width="40" />
  </g>

  <g id="czechia" transform="translate(750,300)" >
    <rect x="0" y="0" width="300" height="100" fill="white" />
    <rect x="0" y="100" width="300" height="100" fill="#d7141b" />
    <polygon points="0,0, 125,100, 0,200" stroke="none" fill="#11467f" />
  </g>

  <g id="japan" transform="translate(50,550)" >
    <rect x="0" y="0" width="300" height="200" fill="white" />
    <circle cx="150" cy="100" r="50" fill="#d7141b" stroke="none" />
  </g>

  <g id="xxx" transform="translate(400,550)" >
    <rect x="0" y="0" width="300" height="200" fill="none" stroke="black" stroke-width="0.5" stroke-dasharray="10,10" />
  </g>

  <g id="yyy" transform="translate(750,550)" >
    <rect x="0" y="0" width="300" height="200" fill="none" stroke="black" stroke-width="0.5" stroke-dasharray="10,10" />
  </g>

</svg>
</figure>

### Poké ball

<figure>
<svg id="pokemon" xmlns="http://www.w3.org/2000/svg" version="1.1" width="200px" height="200px" viewBox="-120 -120 240 240">

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

### Ladybug

<figure>
<svg id="ladybug" xmlns="http://www.w3.org/2000/svg" width="200px" version="1.1" height="200px" viewBox="-100 -100 200 200">

  <defs>
    <clipPath id="lichaam-contour">
      <circle cx="0" cy="40" r="60" />
    </clipPath>
    <radialGradient id="licht" cx="0.35" cy="0.70" r="0.35">
      <stop offset="0%" stop-color="rgb(255,255,255,0.75)" />
      <stop offset="100%" stop-color="rgb(255,0,0,0.0)" />
    </radialGradient>
  </defs>

  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB" />

  <g transform="translate(-10,-15)">
  <g transform="rotate(20,0,40)">
  <circle class="hoofd" cx="0" cy="-12" r="30" fill="black" />
  <circle class="lichaam" cx="0" cy="40" r="60" fill="#ee5564" />
  <polygon fill="black" points="0,-10 6,100 -6,100" clip-path="url(#lichaam-contour)" />
  <circle cx="-20" cy="10" r="6" fill="black" />
  <circle cx="20" cy="10" r="6" fill="black" />
  <circle cx="-40" cy="40" r="6" fill="black" />
  <circle cx="40" cy="40" r="6" fill="black" />
  <circle cx="-25" cy="70" r="6" fill="black" />
  <circle cx="25" cy="70" r="6" fill="black" />
  <circle cx="-40" cy="-60" r="3" fill="black" />
  <circle cx="40" cy="-60" r="3" fill="black" />

  <path stroke="black" stroke-width="3" d="M0,-27 Q0,-50,-40,-60" fill="none" />
  <path stroke="black" stroke-width="3" d="M0,-27 Q0,-50,40,-60" fill="none" />
  <circle cx="0" cy="40" r="60" fill="url(#licht)"/>
  </g>
  </g>

</svg>
</figure>
