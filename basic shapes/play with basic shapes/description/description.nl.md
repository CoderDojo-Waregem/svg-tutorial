Nu je de basisvormen onder de knie hebt, wordt het tijd om je eigen tekening. Zoek een tekening die kan samengesteld worden uit basisvormen. Hieronder geven we alvast een paar mogelijkheden.

### Vlaggen

De meeste landen hebben vlaggen die bestaan uit rechthoeken, driehoeken, lijnen en cirkels. Hieronder zie je alvast enkele mogelijkheden. Weet je van welke landen die de vlaggen zijn? Zoek zelf ook nog enkele vlaggen die je kunt tekenen.

<figure>
<svg id="vlaggen" width="550px" height="400px" viewBox="0 0 1100 800">

  <rect x="0" y="0" width="1100" height="800" fill="#F5F1EB" />

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

### Pokébal

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

### Lieveheersbeestje

<figure>
<svg id="ladybug" xmlns="http://www.w3.org/2000/svg" version="1.1" width="400px" height="400px" viewBox="-100 -100 200 200">

  <defs>
    <clipPath id="lichaam-contour">
      <circle cx="0" cy="40" r="60" />
    </clipPath>
    <radialGradient id="ladybug-light" cx="0.35" cy="0.70" r="0.35">
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
  <circle cx="0" cy="40" r="60" fill="url(#ladybug-light)"/>
  </g>
  </g>

</svg>
</figure>

### Sport field

Hoe ziet het veld eruit van je favoriete sport? Zoek online naar de elementen van het sportveld en hun afmetingen.

<figure>
<svg id="soccer" xmlns="http://www.w3.org/2000/svg" width="560px" version="1.1" height="360px" viewBox="-70 -45 140 90">

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

### Ster

```python
import math

# straal van buitenste en binnenste cirkels instellen
straal_1 = 1.0
straal_2 = 0.39

# hoeken berekenen
hoeken_1 = [18 + index * 72 for index in range(5)]
hoeken_2 = [54 + index * 72 for index in range(5)]

# punten van veelhoek berekenen
punten = []
for angle_1, angle_2 in zip(hoeken_1, hoeken_2):
    punten.append((
        straal_1 * math.cos(math.radians(angle_1)),
        straal_1 * math.sin(math.radians(angle_1)),
    ))
    punten.append((
        straal_2 * math.cos(math.radians(angle_2)),
        straal_2 * math.sin(math.radians(angle_2)),
    ))

# punten van veelhoek uitschrijven
print(' '.join(f'{punt[0]:.3f},{-punt[1]:.3f}' for punt in punten))
```

<figure>
<svg width="200px" height="200px" viewBox="-1 -1.1 2 2">
  <rect x="-1" y="-1.1" width="2" height="2" fill="#F5F1EB" />
  <polygon points="0.951,-0.309 0.229,-0.316 0.000,-1.000 -0.229,-0.316 -0.951,-0.309 -0.371,0.121 -0.588,0.809 -0.000,0.390 0.588,0.809 0.371,0.121" stroke="black" stroke-width="0.01" fill="yellow" />
</svg>
</figure>
