Voordat we beginnen met tekenen, moeten we het hebben over het coördinatenstelsel van SVG-afbeeldingen en over de afmetingen en het kijkvenster die vastgelegd worden in het `svg` element zelf.

### Het coördinatensysteem van SVG

SVG-afbeeldingen worden getekend in een vlak met een coördinatenstelsel waarbij de $$x$$-as van links naar rechts loopt, en de $$y$$-as van boven naar onder. Vooral dat laatste is misschien wel wat wennen, want in de wiskundelessen loopt de $$y$$-as meestal van onder naar boven.

<figure>
<svg class="coordinates1" width="600px" viewBox="-335 -320 655 640">

  <style>
    .coordinates1 text {
      font-family:consolas,monospace;
      font-size:10px;
      text-anchor:middle;
      dominant-baseline:middle;
    }
    .coordinates1 .grid { 
      display: initial; 
    }
    .coordinates1 .grid text.left {
      text-anchor:end;
    }
    .coordinates1 .grid path {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    .coordinates1 .achtergrond {
      stroke: none;
      fill: #F5F1EB;
    }
  </style>

  <rect class="achtergrond" x="-335" y="-320" width="655" height="640" />

  <g class="grid">
    <path d="M-300,0 L300,0" stroke-dasharray="0.2,9.6,0.2,0" />
    <path d="M0,-300 L0,300" stroke-dasharray="0.2,9.6,0.2,0" />
    <path d="M-300,0 L300,0" stroke-dasharray="1,98,1,0" />
    <path d="M0,-300 L0,300" stroke-dasharray="1,98,1,0" />
    <text x="-300" y="-310" fill="black" font-size="5">-300</text>
    <text x="-200" y="-310" fill="black" font-size="5">-200</text>
    <text x="-100" y="-310" fill="black" font-size="5">-100</text>
    <text x="0" y="-310" fill="black" font-size="5">0</text>
    <text x="100" y="-310" fill="black" font-size="5">100</text>
    <text x="200" y="-310" fill="black" font-size="5">200</text>
    <text x="300" y="-310" fill="black" font-size="5">300</text>
    <text class="left" x="-308" y="-300" fill="black" font-size="5">-300</text>
    <text class="left" x="-308" y="-200" fill="black" font-size="5">-200</text>
    <text class="left" x="-308" y="-100" fill="black" font-size="5">-100</text>
    <text class="left" x="-308" y="0" fill="black" font-size="5">0</text>
    <text class="left" x="-308" y="100" fill="black" font-size="5">100</text>
    <text class="left" x="-308" y="200" fill="black" font-size="5">200</text>
    <text class="left" x="-308" y="300" fill="black" font-size="5">300</text>
  </g>

  <path d="M-305,0 L310,0 L305,-2 L305,2 L310,0" stroke="black" stroke-width="1" fill="black" />
  <text x="307" y="8" >x</text>
  <path d="M0,-305 L0,310 L-2,305 L2,305 L0,310" stroke="black" stroke-width="1" fill="black" />
  <text x="8" y="307" >y</text>

  <circle cx="100" cy="100" r="50" fill="none" stroke="black" stroke-width="5" />

</svg>
</figure>

De coördinaten hebben zelf geen specifieke dimensie: het zijn gewoon getallen zonder lengte-eenheid (zoals pixels of meter). Om een cirkel te tekenen moeten we voor het `circle`-element de $$(x, y)$$-coördinaten van het **middelpunt** van de cirkel vastleggen (via de eigenschappen `x` en `y`) en de **straal** van de cirkel (via de eigenschap `r`).

```html
<circle cx="100" cy="100" r="50" />
```

Dit tekent een cirkel (hier met een dikke zwarte rand) met middelpunt op positie $$(100, 100)$$ en straal 50.

<figure>
<svg class="coordinates2" width="600px" viewBox="-335 -320 655 640">

  <style>
    .coordinates2 text {
      font-family:consolas,monospace;
      font-size:10px;
      text-anchor:middle;
      dominant-baseline:middle;
    }
    .coordinates2 text.coord {
      font-size:8px;
    }
    .coordinates2 .grid { 
      display: initial; 
    }
    .coordinates2 .grid text.left {
      text-anchor:end;
    }
    .coordinates2 .grid path {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    .coordinates2 .achtergrond {
      stroke: none;
      fill: #F5F1EB;
    }
  </style>
    
  <rect class="achtergrond" x="-335" y="-320" width="655" height="640" />

  <g class="grid">
    <path d="M-300,0 L300,0" stroke-dasharray="0.2,9.6,0.2,0" />
    <path d="M0,-300 L0,300" stroke-dasharray="0.2,9.6,0.2,0" />
    <path d="M-300,0 L300,0" stroke-dasharray="1,98,1,0" />
    <path d="M0,-300 L0,300" stroke-dasharray="1,98,1,0" />
    <text x="-300" y="-310" fill="black" font-size="5">-300</text>
    <text x="-200" y="-310" fill="black" font-size="5">-200</text>
    <text x="-100" y="-310" fill="black" font-size="5">-100</text>
    <text x="0" y="-310" fill="black" font-size="5">0</text>
    <text x="100" y="-310" fill="black" font-size="5">100</text>
    <text x="200" y="-310" fill="black" font-size="5">200</text>
    <text x="300" y="-310" fill="black" font-size="5">300</text>
    <text class="left" x="-308" y="-300" fill="black" font-size="5">-300</text>
    <text class="left" x="-308" y="-200" fill="black" font-size="5">-200</text>
    <text class="left" x="-308" y="-100" fill="black" font-size="5">-100</text>
    <text class="left" x="-308" y="0" fill="black" font-size="5">0</text>
    <text class="left" x="-308" y="100" fill="black" font-size="5">100</text>
    <text class="left" x="-308" y="200" fill="black" font-size="5">200</text>
    <text class="left" x="-308" y="300" fill="black" font-size="5">300</text>
  </g>

  <path d="M-305,0 L310,0 L305,-2 L305,2 L310,0" stroke="black" stroke-width="1" fill="black" />
  <text x="307" y="8" >x</text>
  <path d="M0,-305 L0,310 L-2,305 L2,305 L0,310" stroke="black" stroke-width="1" fill="black" />
  <text x="8" y="307" >y</text>

  <circle cx="100" cy="100" r="50" fill="none" stroke="black" stroke-width="5" />
  <circle cx="100" cy="100" r="4" fill="black" stroke="none" />
  <text class="coord" x="80" y="94" fill="green">(100,100)</text>
  <path d="M103,103 L134,134" stroke="green" stroke-width="1" fill="black" />
  <text class="coord" x="125" y="115.5" fill="green">50</text>

</svg>
</figure>

### Afmetingen en kijkvenster van het SVG-element

Het SVG-element bevat de afbeeldingselementen en definieert het kijkvenster van onze afbeelding. Het stelt de binnenmaat en de buitenmaat van de afbeelding in.

De eigenschappen `width` (breedte) en `height` (hoogte) bepalen hoeveel ruimte de afbeelding inneemt in de browser. Er is ook een eigenschap `viewBox` die het kijkvenster op het coördinatensysteem definieert voor de afbeelding. De eerste twee waarden in `viewBox` bepalen de coördinaat van de linkerbovenhoek van het kijkvenster en de laatste twee bepalen de breedte en de hoogte van het kijkvenster vanuit het perspectief van de afbeeldingselementen.

- De grootte die wordt gedefinieerd door `width` en `height` is hoe de rest van HTML denkt over de afbeelding en hoe groot deze wordt weergegeven in de browser.
- De grootte gedefinieerd door `viewBox` is hoe de afbeeldingselementen denken over de afbeelding wanneer ze zichzelf positioneren binnen het coördinatenstelsel van SVG.

In de volgende drie voorbeelden hebben we drie SVG-afbeeldingen die precies dezelfde inhoud hebben: de cirkel met middelpunt op positie $$(100, 100)$$ en straal 50 die we hierboven al zijn tegengekomen. De drie afbeelden hebben echter telkens een ander kijkvenster, waardoor de cirkel telkens anders gepositioneerd is binnen de afbeelding. Als de door `viewBox` gedefinieerde grootte niet overeenkomt met de eigenschappen `width` en `height`, dan wordt de afbeelding groter of kleiner gemaakt.

```html
<svg width="100px" height="100px" viewBox="0 0 200 200">
  <circle cx="100" cy="100" r="50" />
</svg>
```

<figure>
<svg width="100px" height="100px" viewBox="0 0 200 200">
  <rect x="0" y="0" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="100" cy="100" r="50" />
</svg>
</figure>

Deze SVG-afbeelding heeft een kijkvenster met linkerbovenhoek op positie $$(0, 0)$$ en een breedte en hoogte van 200.

<figure>
<svg class="coordinates3" width="600px" viewBox="-335 -320 655 640">

  <style>
    .coordinates3 text {
      font-family:consolas,monospace;
      font-size:10px;
      text-anchor:middle;
      dominant-baseline:middle;
    }
    .coordinates3 text.coord {
      font-size:8px;
    }
    .coordinates3 .grid { 
      display: initial; 
    }
    .coordinates3 .grid text.left {
      text-anchor:end;
    }
    .coordinates3 .grid path {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    .coordinates3 .achtergrond {
      stroke: none;
      fill: #F5F1EB;
    }
  </style>
    
  <rect class="achtergrond" x="-335" y="-320" width="655" height="640" />

  <g class="grid">
    <path d="M-300,0 L300,0" stroke-dasharray="0.2,9.6,0.2,0" />
    <path d="M0,-300 L0,300" stroke-dasharray="0.2,9.6,0.2,0" />
    <path d="M-300,0 L300,0" stroke-dasharray="1,98,1,0" />
    <path d="M0,-300 L0,300" stroke-dasharray="1,98,1,0" />
    <text x="-300" y="-310" fill="black" font-size="5">-300</text>
    <text x="-200" y="-310" fill="black" font-size="5">-200</text>
    <text x="-100" y="-310" fill="black" font-size="5">-100</text>
    <text x="0" y="-310" fill="black" font-size="5">0</text>
    <text x="100" y="-310" fill="black" font-size="5">100</text>
    <text x="200" y="-310" fill="black" font-size="5">200</text>
    <text x="300" y="-310" fill="black" font-size="5">300</text>
    <text class="left" x="-308" y="-300" fill="black" font-size="5">-300</text>
    <text class="left" x="-308" y="-200" fill="black" font-size="5">-200</text>
    <text class="left" x="-308" y="-100" fill="black" font-size="5">-100</text>
    <text class="left" x="-308" y="0" fill="black" font-size="5">0</text>
    <text class="left" x="-308" y="100" fill="black" font-size="5">100</text>
    <text class="left" x="-308" y="200" fill="black" font-size="5">200</text>
    <text class="left" x="-308" y="300" fill="black" font-size="5">300</text>
  </g>

  <path d="M-305,0 L310,0 L305,-2 L305,2 L310,0" stroke="black" stroke-width="1" fill="black" />
  <text x="307" y="8" >x</text>
  <path d="M0,-305 L0,310 L-2,305 L2,305 L0,310" stroke="black" stroke-width="1" fill="black" />
  <text x="8" y="307" >y</text>

  <circle cx="100" cy="100" r="50" fill="black" stroke="none" />

  <rect x="-307" y="-307" width="620" height="307" fill="rgb(245,241,235,0.8)" />
  <rect x="-307" y="200" width="620" height="117" fill="rgb(245,241,235,0.8)" />
  <rect x="-307" y="0" width="307" height="200" fill="rgb(245,241,235,0.8)" />
  <rect x="200" y="0" width="117" height="200" fill="rgb(245,241,235,0.8)" />
  <rect x="0" y="0" width="200" height="200" fill="none" stroke="black" stroke-width="1" stroke-dasharray="5,5" />
  <circle cx="0" cy="0" r="4" fill="green" stroke="none" />
  <text class="coord" x="-14" y="-6" fill="green">(0,0)</text>
  <path d="M0,210 L5,212 L5,208 L0,210 L200,210 L195,212 L195,208 L200,210" stroke="green" stroke-width="1" fill="green" />
  <text class="coord" x="100" y="220" fill="green">200</text>
  <path d="M210,0 L212,5 L208,5 L210,0 L210,200 L212,195 L208,195 L210,200" stroke="green" stroke-width="1" fill="green" />
  <text class="coord" x="220" y="100" fill="green">200</text>
  
</svg>
</figure>

Dit is hetzelfde kijkvenster als onderstaande SVG-afbeelding, maar die wordt wel dubbel zo groot weergegeven in de browser. Waar bovenstaande afbeelding in de browser weergegeven wordt met een breedte en hoogte van 100 pixels, wordt onderstaande afbeelding weergegeven met een breedte en hoogte van 200 pixels.

```html
<svg width="200px" height="200px" viewBox="0 0 200 200">
  <circle cx="100" cy="100" r="50" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="0 0 200 200">
  <rect x="0" y="0" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="100" cy="100" r="50" />
</svg>
</figure>

Onderstaande figuur wordt dan weer even groot weergegeven in de browser.

```html
<svg width="200px" height="200px" viewBox="0 0 100 100">
  <circle cx="100" cy="100" r="50" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="0 0 100 100">
  <rect x="0" y="0" width="100" height="100" fill="#F5F1EB"/>
  <circle cx="100" cy="100" r="50" />
</svg>
</figure>

Maar in dit geval is de breedte en de hoogte van het kijkvenster maar half zo groot: het kijkvenster heeft een breedte en een hoogte van 100.

<figure>
<svg class="coordinates4" width="600px" viewBox="-335 -320 655 640">

  <style>
    .coordinates4 text {
      font-family:consolas,monospace;
      font-size:10px;
      text-anchor:middle;
      dominant-baseline:middle;
    }
    .coordinates4 text.coord {
      font-size:8px;
    }
    .coordinates4 .grid { 
      display: initial; 
    }
    .coordinates4 .grid text.left {
      text-anchor:end;
    }
    .coordinates4 .grid path {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    .coordinates4 .achtergrond {
      stroke: none;
      fill: #F5F1EB;
    }
  </style>
    
  <rect class="achtergrond" x="-335" y="-320" width="655" height="640" />

  <g class="grid">
    <path d="M-300,0 L300,0" stroke-dasharray="0.2,9.6,0.2,0" />
    <path d="M0,-300 L0,300" stroke-dasharray="0.2,9.6,0.2,0" />
    <path d="M-300,0 L300,0" stroke-dasharray="1,98,1,0" />
    <path d="M0,-300 L0,300" stroke-dasharray="1,98,1,0" />
    <text x="-300" y="-310" fill="black" font-size="5">-300</text>
    <text x="-200" y="-310" fill="black" font-size="5">-200</text>
    <text x="-100" y="-310" fill="black" font-size="5">-100</text>
    <text x="0" y="-310" fill="black" font-size="5">0</text>
    <text x="100" y="-310" fill="black" font-size="5">100</text>
    <text x="200" y="-310" fill="black" font-size="5">200</text>
    <text x="300" y="-310" fill="black" font-size="5">300</text>
    <text class="left" x="-308" y="-300" fill="black" font-size="5">-300</text>
    <text class="left" x="-308" y="-200" fill="black" font-size="5">-200</text>
    <text class="left" x="-308" y="-100" fill="black" font-size="5">-100</text>
    <text class="left" x="-308" y="0" fill="black" font-size="5">0</text>
    <text class="left" x="-308" y="100" fill="black" font-size="5">100</text>
    <text class="left" x="-308" y="200" fill="black" font-size="5">200</text>
    <text class="left" x="-308" y="300" fill="black" font-size="5">300</text>
  </g>

  <path d="M-305,0 L310,0 L305,-2 L305,2 L310,0" stroke="black" stroke-width="1" fill="black" />
  <text x="307" y="8" >x</text>
  <path d="M0,-305 L0,310 L-2,305 L2,305 L0,310" stroke="black" stroke-width="1" fill="black" />
  <text x="8" y="307" >y</text>

  <circle cx="100" cy="100" r="50" fill="black" stroke="none" />

  <rect x="-307" y="-307" width="620" height="307" fill="rgb(245,241,235,0.8)" />
  <rect x="-307" y="100" width="620" height="217" fill="rgb(245,241,235,0.8)" />
  <rect x="-307" y="0" width="307" height="100" fill="rgb(245,241,235,0.8)" />
  <rect x="100" y="0" width="217" height="100" fill="rgb(245,241,235,0.8)" />
  <rect x="0" y="0" width="100" height="100" fill="none" stroke="black" stroke-width="1" stroke-dasharray="5,5" />

  <circle cx="0" cy="0" r="4" fill="green" stroke="none" />
  <text class="coord" x="-14" y="-6" fill="green">(0,0)</text>
  <path d="M0,110 L5,112 L5,108 L0,110 L100,110 L95,112 L95,108 L100,110" stroke="green" stroke-width="1" fill="green" />
  <text class="coord" x="50" y="120" fill="green">100</text>
  <path d="M110,0 L112,5 L108,5 L110,0 L110,100 L112,95 L108,95 L110,100" stroke="green" stroke-width="1" fill="green" />
  <text class="coord" x="120" y="50" fill="green">100</text>
  
</svg>
</figure>

We kunnen ook instellen welke coördinaat in de linkerbovenhoek van de afbeelding moet staan. In het volgende voorbeeld verplaatsen we de oorsprong van het coördinatensysteem naar het midden van de afbeelding. We stellen de linkerbovenhoek in op `-100,-100`, wat de helft is van de afbeeldingsgrootte in negatief.

Merk op dat positie van het middelpunt van de cirkel nu `0,0` is.

```html
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <circle cx="0" cy="0" r="50" />
</svg>
```

<figure>
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="0" r="50" />
</svg>
</figure>

SVG-afbeeldingen hebben vaak ook een eigenschap `xmlns`. Deze eigenschap kan echter weggelaten worden als de afbeelding in een HTML-document vervat zit.
