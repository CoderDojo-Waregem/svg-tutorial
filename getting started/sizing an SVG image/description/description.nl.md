Voordat we beginnen met tekenen, moeten we het hebben over het coördinatenstelsel van SVG-afbeeldingen en over de afmetingen en het kijkvenster die vastgelegd worden in het `svg` element zelf.

### Het coördinatensysteem van SVG

SVG-afbeeldingen worden getekend in een vlak met een coördinatenstelsel waarbij de $$x$$-as van links naar rechts loopt, en de $$y$$-as van boven naar onder. Vooral dat laatste is misschien wel wat wennen, want in de wiskundelessen loopt de $$y$$-as meestal van onder naar boven.

<figure>
<svg class="coordinates1" width="100%" height="100%" viewBox="-330 -320 640 640">

  <style>
    .coordinates1 text {
      font-family:consolas,monospace;
      font-size:10;
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
  </style>
    
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
<svg class="coordinates2" width="100%" height="100%" viewBox="-330 -320 640 640">

  <style>
    .coordinates2 text {
      font-family:consolas,monospace;
      font-size:10;
      text-anchor:middle;
      dominant-baseline:middle;
    }
    .coordinates2 text.coord {
      font-size:8;
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
  </style>
    
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

### Afmetingen en venster van het SVG-element

Het SVG-element bevat de afbeeldingselementen en definieert het frame van onze afbeelding. Het stelt de binnenmaat en de buitenmaat van de afbeelding in.

De eigenschappen `width` (breedte) en `height` (hoogte) bepalen hoeveel ruimte de afbeelding inneemt in de browser. Er is ook een eigenschap `viewBox` die een coördinatensysteem definieert voor de afbeeldingselementen. De eerste twee waarden in `viewBox` definiëren de coördinaat linksboven in de afbeelding en de laatste twee definiëren de grootte vanuit het perspectief van de afbeeldingselementen.

- De grootte die wordt gedefinieerd door `width` en `height` is hoe de rest van HTML denkt over de afbeelding en hoe groot deze wordt weergegeven in de browser.
- De grootte gedefinieerd door `viewBox` is hoe de afbeeldingselementen denken over de afbeelding wanneer ze zichzelf positioneren.

In de volgende drie voorbeelden hebben we drie SVG-afbeeldingen die precies dezelfde inhoud hebben. Een `circle` element met hetzelfde middelpunt en dezelfde straal. Ze zien er echter heel anders uit. Als de door `viewBox` gedefinieerde grootte niet overeenkomt met de eigenschappen `width` en `height`, dan wordt de afbeelding groter of kleiner gemaakt.

```html
<svg width="100" height="100" viewBox="0 0 200 200">
  <circle cx="100" cy="100" r="50" />
</svg>
```

<figure>
<svg width="100" height="100" viewBox="0 0 200 200">
  <rect x="0" y="0" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="100" cy="100" r="50" />
</svg>
</figure>

```html
<svg width="200" height="200" viewBox="0 0 200 200">
  <circle cx="100" cy="100" r="50" />
</svg>
```

<figure>
<svg width="200" height="200" viewBox="0 0 200 200">
  <rect x="0" y="0" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="100" cy="100" r="50" />
</svg>
</figure>

```html
<svg width="100" height="100" viewBox="0 0 200 200">
  <circle cx="100" cy="100" r="50" />
</svg>
```

<figure>
<svg width="200" height="200" viewBox="0 0 100 100">
  <rect x="0" y="0" width="100" height="100" fill="#F5F1EB"/>
  <circle cx="100" cy="100" r="50" />
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
