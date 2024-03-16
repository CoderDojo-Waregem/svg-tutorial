Nu je de basisvormen, complexere vormen en gebogen lijnen onder de knie hebt, kun je zo ongeveer alles tekenen. Laat je vaardigheden zien door je eigen tekening uit je toetsenbord te toveren. Hieronder geven we een paar mogelijkheden.

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

### Waterpolobal

Maxime speelt waterpolo. Hij ontwierp deze bal met zijn eigen logo.

<figure>
<svg id="water_polo" xmlns="http://www.w3.org/2000/svg" width="430px" height="430px" viewBox="-215 -215 430 430">

  <defs>
    <clipPath id="bal">
      <circle cx="0" cy="0" r="200" />
    </clipPath>
  </defs>
  
  <style>
    text {
      text-anchor: middle;
      dominant-baseline: middle;
      font-family: consolas, monospace;
      font-weight: bold;
    }
  </style>

  # achtergrond
  <rect x="-215" y="-215" width="430" height="430" fill="#F5F1EB" />
  
  # bal
  <circle cx="0" cy="0" r="200" fill="#fabd12" stroke="black" stroke-width="1"/>

  # rechte verticale naden
  <line clip-path="url(#bal)" x1="-127.28" y1="180" x2="-127.28" y2="-180" stroke="black" stroke-width="5" />
  <line clip-path="url(#bal)" x1="127.28" y1="180" x2="127.28" y2="-180" stroke="black" stroke-width="5" />

  # rechte diagonale naden
  <line clip-path="url(#bal)" x1="-68.40" y1="-187.94" x2="68.40" y2="187.94" stroke="black" stroke-width="5" />
  <line clip-path="url(#bal)" x1="68.40" y1="-187.94" x2="-68.40" y2="187.93" stroke="black" stroke-width="5" />

  # afgeronde rechtehoek naden
  <path stroke="#333333" stroke-width="5" fill="#fabd12" stroke-linecap="round"
    d="M-127.28,-127.28 L127.28,-127.28 A180,180,0,0,1,127.28,127.28 L-127.28,127.28 A180,180,0,0,1,-127.28,-127.28" />

  # kromme horizontale naden
  <path d="M-177.265,-31.256 Q0,-80,177.265,-31.256" fill="none" stroke="black" stroke-width="5" />
  <path d="M-177.265,31.256 Q0,80,177.265,31.256" fill="none" stroke="black" stroke-width="5" />

  # logo
  <text x="0" y="4" fill="black" font-size="75">MAXime</text>
  
</svg>
</figure>

### Collage

Maak een kerstige collage met alle voorbeelden die we in deze handleiding getekend hebben.

<figure>
<svg id="collage" xmlns="http://www.w3.org/2000/svg" version="1.1" width="400px" height="400px" viewBox="-100 -100 200 200">

  <style>
    #geschenk .doos {
      fill: #d1495b;
      stroke: black;
      stroke-width: 2px;
    }
    #geschenk .streep {
      fill: white;
      stroke: black;
      stroke-width: 2px;
    }
    #geschenk .lint {
      stroke: #b73a3b;
      stroke-width: 4px;
      fill: none;
    }

    #peperkoek .hoofd {
      fill: #cd803d;
    }
    #peperkoek .oog {
      fill: white;
    }
    #peperkoek .mond {
      fill: none;
      stroke: white;
      stroke-width: 2px;
    }
    #peperkoek .ledemaat {
      stroke: #cd803d;
      stroke-width: 35px;
      stroke-linecap: round;
    }

  </style>

  <defs>

    <clipPath id="kerstbal-contour">
      <circle cx="0" cy="20" r="70" />
    </clipPath>

    <g id="kerstboom">
      <polygon points="0,0 80,120 -80,120" fill="#234236" />
      <polygon points="0,-40 60,60 -60,60" fill="#0C5C4C" />
      <polygon points="0,-80 40,0 -40,0" fill="#38755B" />
      <rect x="-20" y="120" width="40" height="30" fill="brown" />
    </g>

    <g id="geschenk">
      <circle cx="0" cy="-50" r="10" fill="#a9172a" />
      <rect class="doos" x="-60" y="-40" width="120" height="100" />
      <rect class="doos" x="-70" y="-47" width="140" height="20" />
      <rect class="streep" x="-20" y="-40" width="40" height="100" />
      <rect class="streep" x="-25" y="-47" width="50" height="20" />
      <path class="lint" d="M0,-50 L30,-50 C50,-50,50,-70,30,-65 L0,-50" />
      <path class="lint" d="M0,-50 L-30,-50 C-50,-50,-50,-70,-30,-65 L0,-50" />
    </g>

    <g id="ster" transform="rotate(30)">
      <g transform="translate(0 5)">
        <g>
          <polygon points="0,0 36,-50 0,-100" fill="#EDD8B7" />
          <polygon points="0,0 -36,-50 0,-100" fill="#E5C39C" />
        </g>
        <g transform="rotate(72)">
          <polygon points="0,0 36,-50 0,-100" fill="#EDD8B7" />
          <polygon points="0,0 -36,-50 0,-100" fill="#E5C39C" />
        </g>
        <g transform="rotate(-72)">
          <polygon points="0,0 36,-50 0,-100" fill="#EDD8B7" />
          <polygon points="0,0 -36,-50 0,-100" fill="#E5C39C" />
        </g>
        <g transform="rotate(144)">
          <polygon points="0,0 36,-50 0,-100" fill="#EDD8B7" />
          <polygon points="0,0 -36,-50 0,-100" fill="#E5C39C" />
        </g>
        <g transform="rotate(-144)">
          <polygon points="0,0 36,-50 0,-100" fill="#EDD8B7" />
          <polygon points="0,0 -36,-50 0,-100" fill="#E5C39C" />
        </g>
      </g>
    </g>

    <g id="kerstbal">
      <circle cx="0" cy="20" r="70" fill="#D1495B" />
      <polyline clip-path="url(#kerstbal-contour)" fill="none" stroke="#9C2D2A" stroke-width="20"
        points="-120 40 -80 0 -40 40 0 0 40 40 80 0 120 40" />
      <circle cx="0" cy="-75" r="12" fill="none" stroke="#F79257" stroke-width="2" />
      <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257" />
    </g>

    <g id="klok" stroke="black" stroke-width="2">
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

    <path fill="#B73A3B" id="strikdeel" d="
      M0,-20 Q28,-40,56,-45 C96,-48,96,48,56,45 Q28,40,0,20"
    />

    <g id="strikje">
      <use href="#strikdeel" />
      <use href="#strikdeel" transform="scale(-1)" />
      <ellipse cx="0" cy="0" rx="20" ry="24" fill="#9C2D2A" />
      <path fill="none" stroke="#B73A3B" stroke-width="3" d="
        M0,20 Q40,40,30,60 Q20,80,40,90
        M0,20 Q-30,30,-20,60 Q-10,90,-50,100"
      />
    </g>

    <g id="peperkoek">
      <circle class="hoofd" cx="0" cy="-50" r="30" />
      <circle class="oog" cx="-12" cy="-55" r="3" />
      <circle class="oog" cx="12" cy="-55" r="3" />
      <rect class="mond" x="-10" y="-40" width="20" height="5" rx="2" />
      <line class="ledemaat" x1="-40" y1="-10" x2="40" y2="-10" />
      <line class="ledemaat" x1="-25" y1="50" x2="0" y2="-15" />
      <line class="ledemaat" x1="25" y1="50" x2="0" y2="-15" />
      <circle class="knoop" cx="0" cy="-10" r="5" />
      <circle class="knoop" cx="0" cy="10" r="5" />
    </g>


  </defs>

  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB" />
  <use href="#kerstboom" x="0" y="-30" transform="scale(0.8)" />
  <use href="#geschenk" x="-220" y="365" transform="scale(0.22)" />
  <use href="#geschenk" x="-220" y="535" transform="scale(0.16)" />
  <use href="#ster" x="0" y="-590" transform="scale(0.14)" />
  <use href="#kerstbal" x="60" y="-320" transform="scale(0.12)" />
  <use href="#kerstbal" x="-100" y="-20" transform="scale(0.12)" />
  <use href="#kerstbal" x="-200" y="420" transform="scale(0.12)" />
  <use href="#kerstbal" x="180" y="340" transform="scale(0.12)" />
  <use href="#klok" x="80" y="-100" transform="scale(0.12)" />
  <use href="#klok" x="40" y="500" transform="scale(0.12)" />
  <use href="#strikje" x="180" y="120" transform="scale(0.12)" />
  <use href="#peperkoek" x="130" y="50" transform="rotate(20) scale(0.6)" />
</svg>
</figure>
