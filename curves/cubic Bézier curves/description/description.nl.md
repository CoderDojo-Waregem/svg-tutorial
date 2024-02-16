Laten we proberen een tekening te maken van deze geschenkdoos.

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .doos {
      fill: #d1495b;
      stroke: black;
      stroke-width: 2px;
    }
    .streep {
      fill: white;
      stroke: black;
      stroke-width: 2px;
    }
    .lint {
      stroke: #b73a3b;
      stroke-width: 4px;
      fill: none;
    }    
  </style>

  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="-50" r="10" fill="#a9172a" />
  <rect class="doos" x="-60" y="-40" width="120" height="100" />
  <rect class="doos" x="-70" y="-47" width="140" height="20" />
  <rect class="streep" x="-20" y="-40" width="40" height="100" />
  <rect class="streep" x="-25" y="-47" width="50" height="20" />
  <path class="lint" d="M0,-50 L30,-50 C50,-50,50,-70,30,-65 L0,-50" />
  <path class="lint" d="M0,-50 L-30,-50 C-50,-50,-50,-70,-30,-65 L0,-50" />
</svg>
</figure>

Hoewel de kwadratische Bézier fantastisch is als we een lijn willen buigen, is ze vaak niet flexibel genoeg. Met kubische Bézierkrommen hebben we niet slechts één controlepunt, maar twee. Het eerste controlepunt bepaalt de beginrichting van de kromme en het tweede bepaalt vanuit welke richting de kromme bij het eindpunt moet komen.

Laten we opnieuw een voorbeeld bekijken, waarbij de cirkels de controlepunten voorstellen.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-50,50 C-60,-50 60,-50 50,50" fill="none" stroke="red" />
  <circle cx="-60" cy="-50" r="5" />
  <circle cx="60" cy="-50" r="5" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-50,50 C-60,-50 60,-50 50,50" fill="none" stroke="red" />
  <circle cx="-60" cy="-50" r="5" />
  <circle cx="60" cy="-50" r="5" />
</svg>
</figure>

Klik hier voor [een interactieve demo](https://hunormarton.github.io/svg-curves){: target="_blank"} van kubische Bézierkrommen (selecteer **Cubic Bézier** bovenaan de pagina).

Kubische Béziers zijn geweldig wanneer we de kromming van een lijn willen voortzetten. Als de richting van de controlepunten overeenkomt met de richtingen van de lijn voor en de lijn na de kromme, dan hebben we een vloeiende overgang tussen de padsegmenten.

In dit voorbeeld gebruikt het lint van de geschenkdoos een kubische Bézier die de vorige rechte lijn vloeiend voortzet en dan terugdraait in de richting van de komende lijn.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M0,0 L30,0 C50,0,50,-25,30,-15 L0,0" fill="none" stroke="red" />
  <circle cx="50" cy="0" r="2" />
  <circle cx="50" cy="-20" r="2" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M0,0 L30,0 C50,0,50,-25,30,-15 L0,0" fill="none" stroke="red" />
  <circle cx="50" cy="0" r="2" />
  <circle cx="50" cy="-20" r="2" />
</svg>
</figure>

Afgezien van het kubische Béziers bestaat de rest van deze afbeelding voornamelijk uit een paar rechthoeken en een cirkel.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .doos {
      fill: #d1495b;
      stroke: black;
      stroke-width: 2px;
    }
    .streep {
      fill: white;
      stroke: black;
      stroke-width: 2px;
    }
    .lint {
      stroke: #b73a3b;
      stroke-width: 4px;
      fill: none;
    }    
  </style>

  <circle cx="0" cy="-50" r="10" fill="#a9172a" />
  <rect class="doos" x="-60" y="-40" width="120" height="100" />
  <rect class="doos" x="-70" y="-47" width="140" height="20" />
  <rect class="streep" x="-20" y="-40" width="40" height="100" />
  <rect class="streep" x="-25" y="-47" width="50" height="20" />
  <path class="lint" d="M0,-50 L30,-50 C50,-50,50,-70,30,-65 L0,-50" />
  <path class="lint" d="M0,-50 L-30,-50 C-50,-50,-50,-70,-30,-65 L0,-50" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .doos {
      fill: #d1495b;
      stroke: black;
      stroke-width: 2px;
    }
    .streep {
      fill: white;
      stroke: black;
      stroke-width: 2px;
    }
    .lint {
      stroke: #b73a3b;
      stroke-width: 4px;
      fill: none;
    }    
  </style>

  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="-50" r="10" fill="#a9172a" />
  <rect class="doos" x="-60" y="-40" width="120" height="100" />
  <rect class="doos" x="-70" y="-47" width="140" height="20" />
  <rect class="streep" x="-20" y="-40" width="40" height="100" />
  <rect class="streep" x="-25" y="-47" width="50" height="20" />
  <path class="lint" d="M0,-50 L30,-50 C50,-50,50,-70,30,-65 L0,-50" />
  <path class="lint" d="M0,-50 L-30,-50 C-50,-50,-50,-70,-30,-65 L0,-50" />
</svg>
</figure>
