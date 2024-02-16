Voor we beginnen met tekenen, moeten we het eerst hebben over het coördinatenstelsel van SVG-afbeeldingen, en over de afmetingen en het kijkvenster die vastgelegd worden in het `svg` element zelf.

### Het coördinatensysteem van SVG

SVG-afbeeldingen worden getekend in een vlak met een coördinatenstelsel waarbij de $$x$$-as van links naar rechts loopt, en de $$y$$-as van boven naar onder. Vooral dat laatste is misschien wel wat wennen, want in de wiskundelessen loopt de $$y$$-as meestal van onder naar boven.

<figure>
<svg class="coordinaten1" width="600px" viewBox="-335 -320 655 640">

  <style>
    .coordinaten1 text {
      font-family:consolas,monospace;
      font-size:10px;
      text-anchor:middle;
      dominant-baseline:middle;
    }
    .coordinaten1 .grid { 
      display: initial; 
    }
    .coordinaten1 .grid text.left {
      text-anchor:end;
    }
    .coordinaten1 .grid path {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    .coordinaten1 .achtergrond {
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

De coördinaten zelf hebben geen specifieke dimensie: het zijn gewoon getallen zonder lengte-eenheid (zoals pixels of meter). Om een cirkel te tekenen moeten we voor het `circle`-element de $$(x, y)$$-coördinaten van het **middelpunt** van de cirkel vastleggen (via de eigenschappen `x` en `y`) en de **straal** van de cirkel (via de eigenschap `r`).

```html
<circle cx="100" cy="100" r="50" />
```

Dit tekent een cirkel (hieronder weergegeven met een dikke zwarte rand) met middelpunt op positie $$(100, 100)$$ en straal 50.

<figure>
<svg class="coordinaten2" width="600px" viewBox="-335 -320 655 640">

  <style>
    .coordinaten2 text {
      font-family:consolas,monospace;
      font-size:10px;
      text-anchor:middle;
      dominant-baseline:middle;
    }
    .coordinaten2 text.coord {
      font-size:8px;
    }
    .coordinaten2 .grid { 
      display: initial; 
    }
    .coordinaten2 .grid text.left {
      text-anchor:end;
    }
    .coordinaten2 .grid path {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    .coordinaten2 .achtergrond {
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

Het SVG-element bevat alle afbeeldingselementen, maar het definieert ook de afmetingen en het kijkvenster van de afbeelding. Het stelt de interne en de externe maten van de afbeelding in.

De eigenschappen `width` (breedte) en `height` (hoogte) bepalen hoeveel ruimte de afbeelding inneemt in de browser. Dit zijn de externe maten. De grootte die wordt gedefinieerd door `width` en `height` is hoe de rest van HTML denkt over de SVG-afbeelding en hoe groot deze wordt weergegeven in de browser.

Er is ook een eigenschap `viewBox` die het kijkvenster op het coördinatensysteem definieert voor de afbeelding. Enkel die delen van de afbeeldingselementen die binnen het kijkvenster vallen, zijn zichtbaar in de SVG-afbeelding. Het kijkvenster wordt gedefinieerd op basis van vier interne maten die refereren aan het coördinatensysteem van de SVG-afbeelding. De eerste twee waarden van de eigenschap `viewBox` bepalen de positie van de linkerbovenhoek van het kijkvenster en de laatste twee waarden bepalen de breedte en de hoogte van het kijkvenster vanuit het perspectief van de afbeeldingselementen. De grootte gedefinieerd door `viewBox` is hoe de afbeeldingselementen denken over de afbeelding wanneer ze zichzelf positioneren binnen het coördinatenstelsel van SVG.

In de volgende drie voorbeelden hebben de drie SVG-afbeeldingen precies dezelfde inhoud: de cirkel met middelpunt op positie $$(100, 100)$$ en straal 50 die we hierboven al zijn tegengekomen. De drie afbeelden verschillen echter qua kijkvenster, waardoor de cirkel telkens anders gepositioneerd is binnen de afbeelding. Of ze verschillen qua afmetingen waardoor de afbeelding groter of kleiner weergegeven wordt in de browser. Als de grootte die door `viewBox` gedefinieerde wordt, niet overeenkomt met de eigenschappen `width` en `height`, dan wordt de afbeelding groter of kleiner gemaakt.

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
<svg class="coordinaten3" width="600px" viewBox="-335 -320 655 640">

  <style>
    .coordinaten3 text {
      font-family:consolas,monospace;
      font-size:10px;
      text-anchor:middle;
      dominant-baseline:middle;
    }
    .coordinaten3 text.coord {
      font-size:8px;
    }
    .coordinaten3 .grid { 
      display: initial; 
    }
    .coordinaten3 .grid text.left {
      text-anchor:end;
    }
    .coordinaten3 .grid path {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    .coordinaten3 .achtergrond {
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
<svg class="coordinaten4" width="600px" viewBox="-335 -320 655 640">

  <style>
    .coordinaten4 text {
      font-family:consolas,monospace;
      font-size:10px;
      text-anchor:middle;
      dominant-baseline:middle;
    }
    .coordinaten4 text.coord {
      font-size:8px;
    }
    .coordinaten4 .grid { 
      display: initial; 
    }
    .coordinaten4 .grid text.left {
      text-anchor:end;
    }
    .coordinaten4 .grid path {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    .coordinaten4 .achtergrond {
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

We kunnen ook instellen op welke coördinaat de linkerbovenhoek van het kijkvenster moet staan. In het volgende voorbeeld verplaatsen we de oorsprong van het coördinatensysteem naar het midden van de afbeelding. Hiervoor stellen we de linkerbovenhoek in op `-100,-100`, wat de helft is van de afbeeldingsgrootte in negatief.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <circle cx="0" cy="0" r="50" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="0" r="50" />
</svg>
</figure>

Merk op dat positie van het middelpunt van de cirkel nu `0,0` is.

<figure>
<svg class="coordinaten5" width="600px" viewBox="-335 -320 655 640">

  <style>
    .coordinaten5 text {
      font-family:consolas,monospace;
      font-size:10px;
      text-anchor:middle;
      dominant-baseline:middle;
    }
    .coordinaten5 text.coord {
      font-size:8px;
    }
    .coordinaten5 .grid { 
      display: initial; 
    }
    .coordinaten5 .grid text.left {
      text-anchor:end;
    }
    .coordinaten5 .grid path {
      fill: none;
      stroke: royalblue;
      stroke-width: 600;
    }
    .coordinaten5 .achtergrond {
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

  <circle cx="0" cy="0" r="50" fill="black" stroke="none" />

  <rect x="-307" y="-307" width="620" height="207" fill="rgb(245,241,235,0.8)" />
  <rect x="-307" y="100" width="620" height="217" fill="rgb(245,241,235,0.8)" />
  <rect x="-307" y="-100" width="207" height="200" fill="rgb(245,241,235,0.8)" />
  <rect x="100" y="-100" width="217" height="200" fill="rgb(245,241,235,0.8)" />
  <rect x="-100" y="-100" width="200" height="200" fill="none" stroke="black" stroke-width="1" stroke-dasharray="5,5" />

  <circle cx="0" cy="0" r="4" fill="white" stroke="none" />
  <text class="coord" x="-14" y="-6" fill="white">(0,0)</text>

  <circle cx="-100" cy="-100" r="4" fill="green" stroke="none" />
  <text class="coord" x="-128" y="-106" fill="green">(-100,-100)</text>

  <path d="M-100,110 L-95,112 L-95,108 L-100,110 L100,110 L95,112 L95,108 L100,110" stroke="green" stroke-width="1" fill="green" />
  <text class="coord" x="0" y="120" fill="green">200</text>
  <path d="M110,-100 L112,-95 L108,-95 L110,-100 L110,100 L112,95 L108,95 L110,100" stroke="green" stroke-width="1" fill="green" />
  <text class="coord" x="120" y="0" fill="green">200</text>
  
</svg>
</figure>

SVG-afbeeldingen hebben vaak ook een eigenschap `xmlns`. Deze eigenschap kan echter weggelaten worden als de afbeelding in een HTML-document vervat zit.
