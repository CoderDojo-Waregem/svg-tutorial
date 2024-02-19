Nu we geleerd hebben hoe we bogen kunnen tekenen, zijn we klaar om het CoderDojo-logo aan te pakken.

<figure>
<svg width="400px" height="400px" viewBox="-310 -310 620 620">
  <style>
    text {
      text-anchor: middle;
      dominant-baseline: middle;
      font-family: OCR A, consolas, monospace;
    }
  </style>
  <rect x="-310" y="-310" width="620" height="620" fill="#F5F1EB"/>
  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" />
  <path fill="black" d="
    M0,-300
    A150,150,0,0,1,0,0
    A150,150,0,0,0,0,300
    A300,300,0,0,0,0,-300" 
  />
  <text x="0" y="-128" fill="black" font-size="240">0</text>
  <text x="0" y="172" fill="white" font-size="240">1</text>
</svg>
</figure>

We werken met een kijkvenster met een breedte en hoogte van 620 dat de oorsprong van het cöordinatenstelsel in het centrum plaatst. De afbeelding zelf geven we een breedte en een hoogte van 400 pixels.

```html
<svg width="400px" height="400px" viewBox="-310 -310 620 620">
  ...
</svg>
```

<figure>
<svg id="logo1" width="650px" height="640px" viewBox="-330 -320 650 640">

  <style>
    #logo1 text {
      font-family: consolas,monospace;
      font-size: 10px;
      text-anchor: middle;
      dominant-baseline: middle;
    }
    #logo1 .coords { 
      display: initial; 
    }
    #logo1 .coords .y-label {
      text-anchor: end;
    }
    #logo1 .coords .grid {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
  </style>
    
  <rect x="-330" y="-320" width="650" height="640" fill="#F5F1EB"/>

  <g class="coords">
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="1,98,1,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="1,98,1,0" />
    <text class="x-label" x="-300" y="-310" fill="black" font-size="5">-300</text>
    <text class="x-label" x="-200" y="-310" fill="black" font-size="5">-200</text>
    <text class="x-label" x="-100" y="-310" fill="black" font-size="5">-100</text>
    <text class="x-label" x="0" y="-310" fill="black" font-size="5">0</text>
    <text class="x-label" x="100" y="-310" fill="black" font-size="5">100</text>
    <text class="x-label" x="200" y="-310" fill="black" font-size="5">200</text>
    <text class="x-label" x="300" y="-310" fill="black" font-size="5">300</text>
    <text class="y-label" x="-308" y="-300" fill="black" font-size="5">-300</text>
    <text class="y-label" x="-308" y="-200" fill="black" font-size="5">-200</text>
    <text class="y-label" x="-308" y="-100" fill="black" font-size="5">-100</text>
    <text class="y-label" x="-308" y="0" fill="black" font-size="5">0</text>
    <text class="y-label" x="-308" y="100" fill="black" font-size="5">100</text>
    <text class="y-label" x="-308" y="200" fill="black" font-size="5">200</text>
    <text class="y-label" x="-308" y="300" fill="black" font-size="5">300</text>
    <path d="M-305,0 L310,0 L305,-2 L305,2 L310,0" stroke="black" stroke-width="1" fill="black" />
    <text x="307" y="8" >x</text>
    <path d="M0,-305 L0,310 L-2,305 L2,305 L0,310" stroke="black" stroke-width="1" fill="black" />
    <text x="8" y="307" >y</text>
  </g>

</svg>
</figure>

Eerst tekenen we een cirkel waarvan het middelpunt in de oorsprong ligt en met een straal van 300.

```html
<svg width="400px" height="400px" viewBox="-310 -310 620 620">
  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" />
</svg>
```

<figure>
<svg id="logo2" width="650px" height="640px" viewBox="-330 -320 650 640">

  <style>
    #logo2 text {
      font-family: consolas,monospace;
      font-size: 10px;
      text-anchor: middle;
      dominant-baseline: middle;
    }
    #logo2 .coords { 
      display: initial; 
    }
    #logo2 .coords .y-label {
      text-anchor: end;
    }
    #logo2 .coords .grid {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    #logo2 text.element {
      font-size: 20px;
      fill: green;
    }
  </style>
    
  <rect x="-330" y="-320" width="650" height="640" fill="#F5F1EB"/>

  <g class="coords">
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="1,98,1,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="1,98,1,0" />
    <text class="x-label" x="-300" y="-310" fill="black" font-size="5">-300</text>
    <text class="x-label" x="-200" y="-310" fill="black" font-size="5">-200</text>
    <text class="x-label" x="-100" y="-310" fill="black" font-size="5">-100</text>
    <text class="x-label" x="0" y="-310" fill="black" font-size="5">0</text>
    <text class="x-label" x="100" y="-310" fill="black" font-size="5">100</text>
    <text class="x-label" x="200" y="-310" fill="black" font-size="5">200</text>
    <text class="x-label" x="300" y="-310" fill="black" font-size="5">300</text>
    <text class="y-label" x="-308" y="-300" fill="black" font-size="5">-300</text>
    <text class="y-label" x="-308" y="-200" fill="black" font-size="5">-200</text>
    <text class="y-label" x="-308" y="-100" fill="black" font-size="5">-100</text>
    <text class="y-label" x="-308" y="0" fill="black" font-size="5">0</text>
    <text class="y-label" x="-308" y="100" fill="black" font-size="5">100</text>
    <text class="y-label" x="-308" y="200" fill="black" font-size="5">200</text>
    <text class="y-label" x="-308" y="300" fill="black" font-size="5">300</text>
    <path d="M-305,0 L310,0 L305,-2 L305,2 L310,0" stroke="black" stroke-width="1" fill="black" />
    <text x="307" y="8" >x</text>
    <path d="M0,-305 L0,310 L-2,305 L2,305 L0,310" stroke="black" stroke-width="1" fill="black" />
    <text x="8" y="307" >y</text>
  </g>

  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" />
  <line x1="0" y1="0" x2="0" y2="20" stroke="black" stroke-width="1" stroke-dasharray="2,2"/>
  <line x1="300" y1="0" x2="300" y2="20" stroke="black" stroke-width="1" stroke-dasharray="2,2"/>
  <circle cx="0" cy="0" r="5" fill="green" stroke="none" />
  <text class="element" x="-36" y="0">(0,0)</text>
  <path d="M0,20 l5,2 v-4 l-5,2 h300 l-5,-2 v4 l5,-2" stroke="green" stroke-width="1" fill="green" />
  <text class="element" x="150" y="34">300</text>

</svg>
</figure>

Nu komt het moeilijkste deel: de zwarte druppelvorm. Als je die goed analyseert, dan zie je dat die bestaat uit drie halve cirkels. We gebruiken een `<path>` om die drie cirkelbogen te tekenen. We zullen die eerst tekenen met een zwarte rand zonder opvulling. De eerste halve cirkel start bij het punt $$(0, -300)$$ en eindigt in de oorsprong. Die cirkel heeft een straal van 150.

```html
<svg width="400px" height="400px" viewBox="-310 -310 620 620">
  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" />
  <path fill="none" stroke="black" stroke-width="6" d="
    M0,-300
    A150,150,0,0,1,0,0"
  />
</svg>
```

<figure>
<svg id="logo3" width="650px" height="640px" viewBox="-330 -320 650 640">

  <style>
    #logo3 text {
      font-family: consolas,monospace;
      font-size: 10px;
      text-anchor: middle;
      dominant-baseline: middle;
    }
    #logo3 .coords { 
      display: initial; 
    }
    #logo3 .coords .y-label {
      text-anchor: end;
    }
    #logo3 .coords .grid {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    #logo3 text.element {
      font-size: 20px;
      fill: green;
    }
  </style>
    
  <rect x="-330" y="-320" width="650" height="640" fill="#F5F1EB"/>

  <g class="coords">
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="1,98,1,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="1,98,1,0" />
    <text class="x-label" x="-300" y="-310" fill="black" font-size="5">-300</text>
    <text class="x-label" x="-200" y="-310" fill="black" font-size="5">-200</text>
    <text class="x-label" x="-100" y="-310" fill="black" font-size="5">-100</text>
    <text class="x-label" x="0" y="-310" fill="black" font-size="5">0</text>
    <text class="x-label" x="100" y="-310" fill="black" font-size="5">100</text>
    <text class="x-label" x="200" y="-310" fill="black" font-size="5">200</text>
    <text class="x-label" x="300" y="-310" fill="black" font-size="5">300</text>
    <text class="y-label" x="-308" y="-300" fill="black" font-size="5">-300</text>
    <text class="y-label" x="-308" y="-200" fill="black" font-size="5">-200</text>
    <text class="y-label" x="-308" y="-100" fill="black" font-size="5">-100</text>
    <text class="y-label" x="-308" y="0" fill="black" font-size="5">0</text>
    <text class="y-label" x="-308" y="100" fill="black" font-size="5">100</text>
    <text class="y-label" x="-308" y="200" fill="black" font-size="5">200</text>
    <text class="y-label" x="-308" y="300" fill="black" font-size="5">300</text>
    <path d="M-305,0 L310,0 L305,-2 L305,2 L310,0" stroke="black" stroke-width="1" fill="black" />
    <text x="307" y="8" >x</text>
    <path d="M0,-305 L0,310 L-2,305 L2,305 L0,310" stroke="black" stroke-width="1" fill="black" />
    <text x="8" y="307" >y</text>
  </g>

  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" stroke-opacity="25%" fill-opacity="50%" />
  <path fill="none" stroke="black" stroke-width="6" d="
    M0,-300
    A150,150,0,0,1,0,0"
  />

  <circle cx="0" cy="-300" r="5" fill="green" stroke="none" />
  <text class="element" x="0" y="-275">(0,-300)</text>
  <circle cx="0" cy="0" r="5" fill="green" stroke="none" />
  <text class="element" x="0" y="-25">(0,0)</text>
  <path d="M0,-150 l5,2 v-4 l-5,2 h150 l-5,-2 v4 l5,-2" stroke="green" stroke-width="1" fill="green" />
  <text class="element" x="75" y="-130">150</text>

</svg>
</figure>

We breiden het pad uit met een tweede halve cirkel met een straal van 150 die start bij de oorsprong en eindigt bij het punt $$(0, 300)$$.

```html
<svg width="400px" height="400px" viewBox="-310 -310 620 620">
  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" />
  <path fill="none" stroke="black" stroke-width="6" d="
    M0,-300
    A150,150,0,0,1,0,0
    A150,150,0,0,0,0,300"
  />
</svg>
```

<figure>
<svg id="logo4" width="650px" height="640px" viewBox="-330 -320 650 640">

  <style>
    #logo4 text {
      font-family: consolas,monospace;
      font-size: 10px;
      text-anchor: middle;
      dominant-baseline: middle;
    }
    #logo4 .coords { 
      display: initial; 
    }
    #logo4 .coords .y-label {
      text-anchor: end;
    }
    #logo4 .coords .grid {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    #logo4 text.element {
      font-size: 20px;
      fill: green;
    }
  </style>
    
  <rect x="-330" y="-320" width="650" height="640" fill="#F5F1EB"/>

  <g class="coords">
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="1,98,1,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="1,98,1,0" />
    <text class="x-label" x="-300" y="-310" fill="black" font-size="5">-300</text>
    <text class="x-label" x="-200" y="-310" fill="black" font-size="5">-200</text>
    <text class="x-label" x="-100" y="-310" fill="black" font-size="5">-100</text>
    <text class="x-label" x="0" y="-310" fill="black" font-size="5">0</text>
    <text class="x-label" x="100" y="-310" fill="black" font-size="5">100</text>
    <text class="x-label" x="200" y="-310" fill="black" font-size="5">200</text>
    <text class="x-label" x="300" y="-310" fill="black" font-size="5">300</text>
    <text class="y-label" x="-308" y="-300" fill="black" font-size="5">-300</text>
    <text class="y-label" x="-308" y="-200" fill="black" font-size="5">-200</text>
    <text class="y-label" x="-308" y="-100" fill="black" font-size="5">-100</text>
    <text class="y-label" x="-308" y="0" fill="black" font-size="5">0</text>
    <text class="y-label" x="-308" y="100" fill="black" font-size="5">100</text>
    <text class="y-label" x="-308" y="200" fill="black" font-size="5">200</text>
    <text class="y-label" x="-308" y="300" fill="black" font-size="5">300</text>
    <path d="M-305,0 L310,0 L305,-2 L305,2 L310,0" stroke="black" stroke-width="1" fill="black" />
    <text x="307" y="8" >x</text>
    <path d="M0,-305 L0,310 L-2,305 L2,305 L0,310" stroke="black" stroke-width="1" fill="black" />
    <text x="8" y="307" >y</text>
  </g>

  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" stroke-opacity="25%" fill-opacity="50%" />
  <path fill="none" stroke="black" stroke-width="6" d="
    M0,-300
    A150,150,0,0,1,0,0
    A150,150,0,0,0,0,300"
  />

  <circle cx="0" cy="300" r="5" fill="green" stroke="none" />
  <text class="element" x="0" y="275">(0,300)</text>
  <circle cx="0" cy="0" r="5" fill="green" stroke="none" />
  <text class="element" x="0" y="-25">(0,0)</text>
  <path d="M-150,150 l5,2 v-4 l-5,2 h150 l-5,-2 v4 l5,-2" stroke="green" stroke-width="1" fill="green" />
  <text class="element" x="-75" y="130">150</text>

</svg>
</figure>

De druppelvorm wordt gesloten door het punt $$(0, 300)$$ terug te verbinden met het punt $$(0, -300)$$ via een halve cirkel met straal 300.

```html
<svg width="400px" height="400px" viewBox="-310 -310 620 620">
  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" />
  <path fill="none" stroke="black" stroke-width="6" d="
    M0,-300
    A150,150,0,0,1,0,0
    A150,150,0,0,0,0,300
    A300,300,0,0,0,0,-300" 
  />
</svg>
```

<figure>
<svg id="logo5" width="650px" height="640px" viewBox="-330 -320 650 640">

  <style>
    #logo5 text {
      font-family: consolas,monospace;
      font-size: 10px;
      text-anchor: middle;
      dominant-baseline: middle;
    }
    #logo5 .coords { 
      display: initial; 
    }
    #logo5 .coords .y-label {
      text-anchor: end;
    }
    #logo5 .coords .grid {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    #logo5 text.element {
      font-size: 20px;
      fill: green;
    }
  </style>
    
  <rect x="-330" y="-320" width="650" height="640" fill="#F5F1EB"/>

  <g class="coords">
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="1,98,1,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="1,98,1,0" />
    <text class="x-label" x="-300" y="-310" fill="black" font-size="5">-300</text>
    <text class="x-label" x="-200" y="-310" fill="black" font-size="5">-200</text>
    <text class="x-label" x="-100" y="-310" fill="black" font-size="5">-100</text>
    <text class="x-label" x="0" y="-310" fill="black" font-size="5">0</text>
    <text class="x-label" x="100" y="-310" fill="black" font-size="5">100</text>
    <text class="x-label" x="200" y="-310" fill="black" font-size="5">200</text>
    <text class="x-label" x="300" y="-310" fill="black" font-size="5">300</text>
    <text class="y-label" x="-308" y="-300" fill="black" font-size="5">-300</text>
    <text class="y-label" x="-308" y="-200" fill="black" font-size="5">-200</text>
    <text class="y-label" x="-308" y="-100" fill="black" font-size="5">-100</text>
    <text class="y-label" x="-308" y="0" fill="black" font-size="5">0</text>
    <text class="y-label" x="-308" y="100" fill="black" font-size="5">100</text>
    <text class="y-label" x="-308" y="200" fill="black" font-size="5">200</text>
    <text class="y-label" x="-308" y="300" fill="black" font-size="5">300</text>
    <path d="M-305,0 L310,0 L305,-2 L305,2 L310,0" stroke="black" stroke-width="1" fill="black" />
    <text x="307" y="8" >x</text>
    <path d="M0,-305 L0,310 L-2,305 L2,305 L0,310" stroke="black" stroke-width="1" fill="black" />
    <text x="8" y="307" >y</text>
  </g>

  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" stroke-opacity="25%" fill-opacity="50%" />
  <path fill="none" stroke="black" stroke-width="6" d="
    M0,-300
    A150,150,0,0,1,0,0
    A150,150,0,0,0,0,300
    A300,300,0,0,0,0,-300" 
  />

  <circle cx="0" cy="300" r="5" fill="green" stroke="none" />
  <text class="element" x="0" y="275">(0,300)</text>
  <circle cx="0" cy="-300" r="5" fill="green" stroke="none" />
  <text class="element" x="0" y="-275">(0,-300)</text>
  <path d="M0,20 l5,2 v-4 l-5,2 h300 l-5,-2 v4 l5,-2" stroke="green" stroke-width="1" fill="green" />
  <text class="element" x="150" y="34">300</text>

</svg>
</figure>

In plaats van de druppelvorm een zwarte rand te geven, kunnen we die nu een zwarte opvulling geven.

```html
<svg width="400px" height="400px" viewBox="-310 -310 620 620">
  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" />
  <path fill="black" stroke="none" d="
    M0,-300
    A150,150,0,0,1,0,0
    A150,150,0,0,0,0,300
    A300,300,0,0,0,0,-300" 
  />
</svg>
```

<figure>
<svg id="logo6" width="650px" height="640px" viewBox="-330 -320 650 640">

  <style>
    #logo6 text {
      font-family: consolas,monospace;
      font-size: 10px;
      text-anchor: middle;
      dominant-baseline: middle;
    }
    #logo6 .coords { 
      display: initial; 
    }
    #logo6 .coords .y-label {
      text-anchor: end;
    }
    #logo6 .coords .grid {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    #logo6 text.element {
      font-size: 20px;
      fill: green;
    }
  </style>
    
  <rect x="-330" y="-320" width="650" height="640" fill="#F5F1EB"/>

  <g class="coords">
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="1,98,1,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="1,98,1,0" />
    <text class="x-label" x="-300" y="-310" fill="black" font-size="5">-300</text>
    <text class="x-label" x="-200" y="-310" fill="black" font-size="5">-200</text>
    <text class="x-label" x="-100" y="-310" fill="black" font-size="5">-100</text>
    <text class="x-label" x="0" y="-310" fill="black" font-size="5">0</text>
    <text class="x-label" x="100" y="-310" fill="black" font-size="5">100</text>
    <text class="x-label" x="200" y="-310" fill="black" font-size="5">200</text>
    <text class="x-label" x="300" y="-310" fill="black" font-size="5">300</text>
    <text class="y-label" x="-308" y="-300" fill="black" font-size="5">-300</text>
    <text class="y-label" x="-308" y="-200" fill="black" font-size="5">-200</text>
    <text class="y-label" x="-308" y="-100" fill="black" font-size="5">-100</text>
    <text class="y-label" x="-308" y="0" fill="black" font-size="5">0</text>
    <text class="y-label" x="-308" y="100" fill="black" font-size="5">100</text>
    <text class="y-label" x="-308" y="200" fill="black" font-size="5">200</text>
    <text class="y-label" x="-308" y="300" fill="black" font-size="5">300</text>
    <path d="M-305,0 L310,0 L305,-2 L305,2 L310,0" stroke="black" stroke-width="1" fill="black" />
    <text x="307" y="8" >x</text>
    <path d="M0,-305 L0,310 L-2,305 L2,305 L0,310" stroke="black" stroke-width="1" fill="black" />
    <text x="8" y="307" >y</text>
  </g>

  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" stroke-opacity="25%" fill-opacity="50%" />
  <path fill="black" stroke="none" d="
    M0,-300
    A150,150,0,0,1,0,0
    A150,150,0,0,0,0,300
    A300,300,0,0,0,0,-300" 
  />

</svg>
</figure>

Het laatste dat we nog moeten doen is de cijfers `0` en `1` op de juiste plaats zetten. Hiervoor kunnen we het `text`-element gebruiken om een zwart opgevuld cijfer `0` op positie $$(0, -150)$$ te zetten en een wit opgevuld cijfer `1` op positie $$(0, 150)$$. We stellen de grootte van de tekst (`font-size`) ook in op 240.

```html
<svg width="400px" height="400px" viewBox="-310 -310 620 620">
  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" />
  <path fill="black" stroke="none" d="
    M0,-300
    A150,150,0,0,0,0,300
    A300,300,0,0,0,0,-300" 
  />
  <text x="0" y="-150" fill="black" font-size="240">0</text>
  <text x="0" y="150" fill="white" font-size="240">1</text>
</svg>
```

<figure>
<svg id="logo7" width="650px" height="640px" viewBox="-330 -320 650 640">

  <style>
    #logo7 text {
      text-anchor: middle;
      dominant-baseline: middle;
      font-family: OCR A, consolas, monospace;
    }
    #logo7 .coords text {
      font-family: consolas,monospace;
      text-anchor: middle;
      dominant-baseline: middle;
    }
    #logo7 .coords { 
      display: initial; 
    }
    #logo7 .coords .y-label {
      text-anchor: end;
    }
    #logo7 .coords .grid {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    #logo7 text.element {
      font-family: consolas,monospace;
      fill: green;
    }
  </style>
    
  <rect x="-330" y="-320" width="650" height="640" fill="#F5F1EB"/>

  <g class="coords">
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="0.2,9.6,0.2,0" />
    <path class="grid" d="M-300,0 L300,0" stroke-dasharray="1,98,1,0" />
    <path class="grid" d="M0,-300 L0,300" stroke-dasharray="1,98,1,0" />
    <text class="x-label" x="-300" y="-310" fill="black" font-size="5">-300</text>
    <text class="x-label" x="-200" y="-310" fill="black" font-size="5">-200</text>
    <text class="x-label" x="-100" y="-310" fill="black" font-size="5">-100</text>
    <text class="x-label" x="0" y="-310" fill="black" font-size="5">0</text>
    <text class="x-label" x="100" y="-310" fill="black" font-size="5">100</text>
    <text class="x-label" x="200" y="-310" fill="black" font-size="5">200</text>
    <text class="x-label" x="300" y="-310" fill="black" font-size="5">300</text>
    <text class="y-label" x="-308" y="-300" fill="black" font-size="5">-300</text>
    <text class="y-label" x="-308" y="-200" fill="black" font-size="5">-200</text>
    <text class="y-label" x="-308" y="-100" fill="black" font-size="5">-100</text>
    <text class="y-label" x="-308" y="0" fill="black" font-size="5">0</text>
    <text class="y-label" x="-308" y="100" fill="black" font-size="5">100</text>
    <text class="y-label" x="-308" y="200" fill="black" font-size="5">200</text>
    <text class="y-label" x="-308" y="300" fill="black" font-size="5">300</text>
    <path d="M-305,0 L310,0 L305,-2 L305,2 L310,0" stroke="black" stroke-width="1" fill="black" />
    <text class="element" x="307" y="8" font-size="5">x</text>
    <path d="M0,-305 L0,310 L-2,305 L2,305 L0,310" stroke="black" stroke-width="1" fill="black" />
    <text class="element" x="8" y="307" font-size="5">y</text>
  </g>

  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" stroke-opacity="25%" fill-opacity="50%" />
  <path fill="black" stroke="none" fill-opacity="25%" d="
    M0,-300
    A150,150,0,0,1,0,0
    A150,150,0,0,0,0,300
    A300,300,0,0,0,0,-300" 
  />
  <text x="0" y="-128" fill="black" font-size="240">0</text>
  <text x="0" y="172" fill="white" font-size="240">1</text>

  <circle cx="0" cy="-150" r="5" fill="green" stroke="none" />
  <circle cx="0" cy="150" r="5" fill="green" stroke="none" />
  <text class="element" x="-55" y="-150" font-size="20">(0,-150)</text>
  <text class="element" x="-55" y="150" font-size="20">(0,150)</text>

</svg>
</figure>

Je zult echter merken dat bovenstaande code nog niet het gewenste resultaat geeft. We moeten immers nog enkele eigenschappen van de tekst instellen. Omdat die voor beide cijfers hetzelfde zijn, zullen we een `style`-element gebruiken om de CSS-eigenschappen van alle tekst in de figuur in één keer in te stellen. We stellen het lettertype (`font-family`) van de tekst (`font-size`) in op `OCR A`. Voor computers waarop dit lettertype niet geïnstalleerd is, vallen we achtereenvolgens terug op het lettertype `consolas` en daarna op het standaard `monospace` lettertype.

```html
<style>
  text {
    text-anchor: middle;
    dominant-baseline: middle;
    font-family: OCR A, consolas, monospace;
  }
</style>
```

Normaal gezien ligt het ankerpunt waar de tekst geplaatst wordt in de linkerbovenhoek. Met `text-anchor: middle;` zorgen we ervoor dat de tekst horizontaal gecentreerd wordt rond het ankerpunt. Met `dominant-baseline: middle;` zorgen we ervoor dat de tekst verticaal gecentreerd wordt rond het ankerpunt. Dat laatste is echter niet helemaal het geval, waardoor we beide cijfers nog 22 posities lager zetten langs de $$y$$-as om ze op hun gewenste plaats te krijgen. Dit is het eindresultaat:

```html
<svg width="400px" height="400px" viewBox="-310 -310 620 620">
  <style>
    text {
      text-anchor: middle;
      dominant-baseline: middle;
      font-family: OCR A, consolas, monospace;
    }
  </style>
  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" />
  <path fill="black" stroke="none" d="
    M0,-300
    A150,150,0,0,1,0,0
    A150,150,0,0,0,0,300
    A300,300,0,0,0,0,-300" 
  />
  <text x="0" y="-128" fill="black" font-size="240">0</text>
  <text x="0" y="172" fill="white" font-size="240">1</text>
</svg>
```

<figure>
<svg id="logo8" width="400px" height="400px" viewBox="-310 -310 620 620">
  <style>
    #logo8 text {
      text-anchor: middle;
      dominant-baseline: middle;
      font-family: OCR A, consolas, monospace;
    }
  </style>
  <rect x="-310" y="-310" width="620" height="620" fill="#F5F1EB"/>
  <circle cx="0" cy="0" r="300" fill="white" stroke="black" stroke-width="4" />
  <path fill="black" stroke="none" d="
    M0,-300
    A150,150,0,0,1,0,0
    A150,150,0,0,0,0,300
    A300,300,0,0,0,0,-300" 
  />
  <text x="0" y="-128" fill="black" font-size="240">0</text>
  <text x="0" y="172" fill="white" font-size="240">1</text>
</svg>
</figure>
