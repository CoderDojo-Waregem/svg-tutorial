Het is ook cool om paden te gebruiken voor *animatiepaden*.

<figure>
<svg id="animatie" width="400px" height="200px" viewBox="-200 -100 400 200">
  <style>
    #animatie .sleigh {
      offset-path: path(
        "M-220,80 L-90,80 Q60,80,60,-10 A50,50,0,0,0,-60,-10 Q-60,80,90,80 L220,80"
      );
      animation: roller-coaster 6000ms infinite linear;
    }
    
    @keyframes roller-coaster {
      0% { offset-distance: 0%; }
      100% { offset-distance: 100%; }
    }    
  </style>
  <rect x="-200" y="-100" width="400" height="200" fill="#F5F1EB"/>
  <path stroke="#E0CEB9" stroke-width="4" fill="none"
    d="M-200,80 L-80,80 Q80,80,70,-10 A70,70,0,0,0,-70,-10 Q-80,80,80,80 L200,80"
  />
  <g class="sleigh" fill="none">
    <path stroke="#AF6455" stroke-width="5"
      d="M-30,-2 L30,-2 A10,10,0,0,0,30,-22 M-20,-2 L-20,-17 M20,-2 L20,-17"
    />
    <path d="M-27,-17 L27,-17" stroke="#7A504F" stroke-width="6" />
  </g>
</svg>
</figure>

Deze methode kan niet alleen voor SVG gebruikt worden. We gebruiken hier de CSS-eigenschap  `offset-path` die ook voor elk ander HTML-element werkt. Maar als je de waarde van dit attribuut bekijkt, dan zie je dat een pad op dezelfde manier gedefinieerd wordt als bij een SVG.

Om dit in twee delen op te splitsen, tekenen we eerst de baan. We definiëren dit als één enkel pad.

<figure>
<svg id="animatie1" width="400px" height="200px" viewBox="-200 -100 400 200">
  <rect x="-200" y="-100" width="400" height="200" fill="#F5F1EB"/>
  <path stroke="#E0CEB9" stroke-width="4" fill="none"
    d="M-200,80 L-80,80 Q80,80,70,-10 A70,70,0,0,0,-70,-10 Q-80,80,80,80 L200,80"
  />
</svg>
</figure>

Dan tekenen we ook nog een slee, die samengesteld is uit twee verschillende paden die samen één groep vormen.

<figure>
<svg id="animatie2" width="400px" height="200px" viewBox="-200 -100 400 200">
  <rect x="-200" y="-100" width="400" height="200" fill="#F5F1EB"/>
  <g class="sleigh" fill="none">
    <path stroke="#AF6455" stroke-width="5"
      d="M-30,-2 L30,-2 A10,10,0,0,0,30,-22 M-20,-2 L-20,-17 M20,-2 L20,-17"
    />
    <path d="M-27,-17 L27,-17" stroke="#7A504F" stroke-width="6" />
  </g>
</svg>
</figure>

Geen van beide zijn op zichzelf erg interessant. Wat wel nieuw is, is dat we een animatie kunnen toevoegen waarbij het animatiepad in wezen hetzelfde is als het pad van de baan. Het animatiepad is alleen iets anders om de slee nog beter op het pad te laten glijden. Standaard beweegt het onderste en middelste deel van de slee over het pad en zakken het begin en het einde een beetje in het pad. In plaats daarvan hebben we het pad wat aangepast zodat de slee iets omhoog komt bij sommige krappe bochten.

```html
<svg width="400px" height="200px" viewBox="-200 -100 400 200">
  <style>
    .sleigh {
      offset-path: path(
        "M-220,80 L-90,80 Q60,80,60,-10 A50,50,0,0,0,-60,-10 Q-60,80,90,80 L220,80"
      );
      animation: roller-coaster 6000ms infinite linear;
    }
    
    @keyframes roller-coaster {
      0% { offset-distance: 0%; }
      100% { offset-distance: 100%; }
    }    
  </style>
  <rect x="-200" y="-100" width="400" height="200" fill="#F5F1EB"/>
  <path stroke="#E0CEB9" stroke-width="4" fill="none"
    d="M-200,80 L-80,80 Q80,80,70,-10 A70,70,0,0,0,-70,-10 Q-80,80,80,80 L200,80"
  />
  <g class="sleigh" fill="none">
    <path stroke="#AF6455" stroke-width="5"
      d="M-30,-2 L30,-2 A10,10,0,0,0,30,-22 M-20,-2 L-20,-17 M20,-2 L20,-17"
    />
    <path d="M-27,-17 L27,-17" stroke="#7A504F" stroke-width="6" />
  </g>
</svg>
```

<figure>
<svg id="animatie3" width="400px" height="200px" viewBox="-200 -100 400 200">
  <style>
    #animatie3 .sleigh {
      offset-path: path(
        "M-220,80 L-90,80 Q60,80,60,-10 A50,50,0,0,0,-60,-10 Q-60,80,90,80 L220,80"
      );
      animation: roller-coaster 6000ms infinite linear;
    }
    
    @keyframes roller-coaster {
      0% { offset-distance: 0%; }
      100% { offset-distance: 100%; }
    }    
  </style>
  <rect x="-200" y="-100" width="400" height="200" fill="#F5F1EB"/>
  <path stroke="#E0CEB9" stroke-width="4" fill="none"
    d="M-200,80 L-80,80 Q80,80,70,-10 A70,70,0,0,0,-70,-10 Q-80,80,80,80 L200,80"
  />
  <g class="sleigh" fill="none">
    <path stroke="#AF6455" stroke-width="5"
      d="M-30,-2 L30,-2 A10,10,0,0,0,30,-22 M-20,-2 L-20,-17 M20,-2 L20,-17"
    />
    <path d="M-27,-17 L27,-17" stroke="#7A504F" stroke-width="6" />
  </g>
</svg>
</figure>
