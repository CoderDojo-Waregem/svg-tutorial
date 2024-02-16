De opvulling van een vorm kan gedefinieerd worden als een kleurovergang. We voegen een subtiel 3D-effect toe aan onze kerstbal en bouwen een sneeuwpop.

<figure>
<svg width="200px" height="250px" viewBox="-100 -100 200 250" style="background-color: lightblue">
  <defs>
    <radialGradient id="sneeuwbal" cx="0.25" cy="0.25" r="1">
      <stop offset="0%" stop-color="white" />
      <stop offset="50%" stop-color="white" />
      <stop offset="100%" stop-color="#d6d6d6" />
    </radialGradient>
  </defs>

  <circle cx="0" cy="60" r="80" fill="url(#sneeuwbal)" />
  <circle cx="0" cy="-40" r="50" fill="url(#sneeuwbal)" />
  <polygon points="10,-46 50,-40 10,-34" fill="#e66465" />

  <circle cx="0" cy="-55" r="5" />
  <circle cx="20" cy="-55" r="5" />

  <line x1="-40" y1="30" x2="-90" y2="-30" stroke="black" stroke-width="5" />
  <line x1="-65" y1="0" x2="-90" y2="-10" stroke="black" stroke-width="5" />
</svg>
</figure>

### Een gepimpte kerstbal

Laat ons de kerstbal die we eerder gemaakt hebben een beetje pimpen.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
    <clipPath id="ball1">
      <circle cx="0" cy="20" r="70" />
    </clipPath>
  </defs>

  <circle cx="0" cy="20" r="70" fill="#D1495B" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257" />
  <circle cx="0" cy="-75" r="12" fill="none" stroke="#F79257" stroke-width="2" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
    <clipPath id="ball1">
      <circle cx="0" cy="20" r="70" />
    </clipPath>
  </defs>

  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="20" r="70" fill="#D1495B" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257" />
  <circle cx="0" cy="-75" r="12" fill="none" stroke="#F79257" stroke-width="2" />
</svg>
</figure>

We kunnen een subtiel 3D-effect toevoegen door de hoofdcirkel op te vullen met een kleurovergang. Hiervoor definiëren we een `radialGradient` in de `defs` sectie. Dit heeft een andere syntax dan bij CSS, maar de mogelijkheden zijn vergelijkbaar.

We definiëren zijn ID, positioneren het middelpunt met `cx` en `cy`, stellen zijn straal in en de stopkleuren. Dan kunnen we het gebruiken als attribuut voor de `fill` eigenschap van een vorm.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
    <radialGradient id="shine" cx="0.25" cy="0.25" r="0.35">
      <stop offset="0%" stop-color="#e3a8b0" />
      <stop offset="100%" stop-color="#D1495B" />
    </radialGradient>
  </defs>

  <circle cx="0" cy="20" r="70" fill="url(#shine)" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257"  />
  <circle cx="0" cy="-75" r="12" fill="none" stroke="#F79257" stroke-width="2" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
    <radialGradient id="shine" cx="0.25" cy="0.25" r="0.35">
      <stop offset="0%" stop-color="#e3a8b0" />
      <stop offset="100%" stop-color="#D1495B" />
    </radialGradient>
  </defs>

  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="20" r="70" fill="url(#shine)" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257"  />
  <circle cx="0" cy="-75" r="12" fill="none" stroke="#F79257" stroke-width="2" />
</svg>
</figure>

### Een sneeuwpop bouwen

Voor de sneeuwpop tekenen we als volgt twee cirkels met een vergelijkbare kleurovergang.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200" style="background-color: lightblue">
  <defs>
    <radialGradient id="sneeuwbal" cx="0.25" cy="0.25" r="1">
      <stop offset="0%" stop-color="white" />
      <stop offset="50%" stop-color="white" />
      <stop offset="100%" stop-color="#d6d6d6" />
    </radialGradient>
  </defs>

  <circle cx="0" cy="0" r="80" fill="url(#sneeuwbal)" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200" style="background-color: lightblue">
  <defs>
    <radialGradient id="sneeuwbal1" cx="0.25" cy="0.25" r="1">
      <stop offset="0%" stop-color="white" />
      <stop offset="50%" stop-color="white" />
      <stop offset="100%" stop-color="#d6d6d6" />
    </radialGradient>
  </defs>

  <circle cx="0" cy="0" r="80" fill="url(#sneeuwbal1)" />
</svg>
</figure>

Dan voegen we een veelhoek toe voor de neus, twee cirkels voor de ogen en twee lijnen voor de arm. Eenvoudig.

```html
<svg width="200px" height="250px" viewBox="-100 -100 200 250" 
  style="background-color: lightblue">
  <defs>
    <radialGradient id="sneeuwbal" cx="0.25" cy="0.25" r="1">
      <stop offset="0%" stop-color="white" />
      <stop offset="50%" stop-color="white" />
      <stop offset="100%" stop-color="#d6d6d6" />
    </radialGradient>
  </defs>

  <circle cx="0" cy="60" r="80" fill="url(#sneeuwbal)" />
  <circle cx="0" cy="-40" r="50" fill="url(#sneeuwbal)" />
  <polygon points="10,-46 50,-40 10,-34" fill="#e66465" />

  <circle cx="0" cy="-55" r="5" />
  <circle cx="20" cy="-55" r="5" />

  <line x1="-40" y1="30" x2="-90" y2="-30" stroke="black" stroke-width="5" />
  <line x1="-65" y1="0" x2="-90" y2="-10" stroke="black" stroke-width="5" />
</svg>
```

<figure>
<svg width="200px" height="250px" viewBox="-100 -100 200 250" 
  style="background-color: lightblue">
  <defs>
    <radialGradient id="sneeuwbal2" cx="0.25" cy="0.25" r="1">
      <stop offset="0%" stop-color="white" />
      <stop offset="50%" stop-color="white" />
      <stop offset="100%" stop-color="#d6d6d6" />
    </radialGradient>
  </defs>

  <circle cx="0" cy="60" r="80" fill="url(#sneeuwbal2)" />
  <circle cx="0" cy="-40" r="50" fill="url(#sneeuwbal2)" />
  <polygon points="10,-46 50,-40 10,-34" fill="#e66465" />

  <circle cx="0" cy="-55" r="5" />
  <circle cx="20" cy="-55" r="5" />

  <line x1="-40" y1="30" x2="-90" y2="-30" stroke="black" stroke-width="5" />
  <line x1="-65" y1="0" x2="-90" y2="-10" stroke="black" stroke-width="5" />
</svg>
</figure>