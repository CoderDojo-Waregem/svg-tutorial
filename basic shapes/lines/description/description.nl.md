Het zal je misschien verbazen hoe eenvoudig het is om dit peperkoeken mannetje te tekenen op basis van een aantal lijnen. We leren ook hoe je de uiteinden van lijnen en de hoekpunten van rechthoeken kunt afronden.

<figure>
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .hoofd {
      fill: #cd803d;
    }
    .oog {
      fill: white;
    }
    .mond {
      fill: none;
      stroke: white;
      stroke-width: 2px;
    }
    .ledemaat {
      stroke: #cd803d;
      stroke-width: 35px;
      stroke-linecap: round;
    }
  </style>
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle class="hoofd" cx="0" cy="-50" r="30" />
  <circle class="oog" cx="-12" cy="-55" r="3" />
  <circle class="oog" cx="12" cy="-55" r="3" />
  <rect class="mond" x="-10" y="-40" width="20" height="5" rx="2" />
  <line class="ledemaat" x1="-40" y1="-10" x2="40" y2="-10" />
  <line class="ledemaat" x1="-25" y1="50" x2="0" y2="-15" />
  <line class="ledemaat" x1="25" y1="50" x2="0" y2="-15" />
  <circle class="knoop" cx="0" cy="-10" r="5" />
  <circle class="knoop" cx="0" cy="10" r="5" />
</svg>
</figure>

### Stijleigenschappen verplaatsen naar CSS

We kunnen CSS-klassen toewijzen aan elk element en sommige attributen verplaatsen naar CSS. We kunnen echter alleen de presentatie-attributen verplaatsen. Positieattributen en attributen die de vormen definiëren moeten in de SVG-tags blijven. Maar attributen voor kleuren, lijnen en lettertypes kunnen naar CSS verplaatst worden.

```html
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .hoofd {
      fill: #cd803d;
    }
  </style>
  <circle class="hoofd" cx="0" cy="-50" r="30" />
</svg>
```

<figure>
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .hoofd1 {
      fill: #cd803d;
    }
  </style>
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle class="hoofd1" cx="0" cy="-50" r="30" />
</svg>
</figure>

### Afgeronde lijnen

We zagen al de `fill` en enkele `stroke` eigenschappen, maar hier is nog een presentatie-eigenschap. De `stroke-linecap`. Hiermee kunnen we het uiteinde van onze lijnen afronden. Merk op dat de benen en armen gewoon als lijnen getekend worden.

Ter vergelijking, als we de `stroke-linecap` verwijderen en een smallere `stroke-width` instellen, dan zou het er zo uitzien.

```html
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .ledemaat {
      stroke: #cd803d;
    }
  </style>
  <line class="ledemaat" x1="-40" y1="-10" x2="40" y2="-10" />
  <line class="ledemaat" x1="-25" y1="50" x2="0" y2="-15" />
  <line class="ledemaat" x1="25" y1="50" x2="0" y2="-15" />
</svg>
```

<figure>
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .ledemaat2 {
      stroke: #cd803d;
      stroke-width: 1px;
      stroke-linecap: butt;
    }
  </style>
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <line class="ledemaat2" x1="-40" y1="-10" x2="40" y2="-10" />
  <line class="ledemaat2" x1="-25" y1="50" x2="0" y2="-15" />
  <line class="ledemaat2" x1="25" y1="50" x2="0" y2="-15" />
</svg>
</figure>

Maar door een dikke lijnbreedte en een rond uiteinde in te stellen, kunnen we benen en armen vormgeven voor onze figuur.

```html
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .ledemaat {
      stroke: #cd803d;
      stroke-width: 35px;
      stroke-linecap: round;
    }
  </style>
  <line class="ledemaat" x1="-40" y1="-10" x2="40" y2="-10" />
  <line class="ledemaat" x1="-25" y1="50" x2="0" y2="-15" />
  <line class="ledemaat" x1="25" y1="50" x2="0" y2="-15" />
</svg>
```

<figure>
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .ledemaat3 {
      stroke: #cd803d;
      stroke-width: 35px;
      stroke-linecap: round;
    }
  </style>
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <line class="ledemaat3" x1="-40" y1="-10" x2="40" y2="-10" />
  <line class="ledemaat3" x1="-25" y1="50" x2="0" y2="-15" />
  <line class="ledemaat3" x1="25" y1="50" x2="0" y2="-15" />
</svg>
</figure>

### Afgeronde rechthoeken

Let ook op de `rx` eigenschap bij de rechthoek die de mond definieert. Hierdoor worden de randen afgerond. Het is vergelijkbaar met de `border-radius` eigenschap voor gewone HTML-elementen.

```html
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .hoofd {
      fill: #cd803d;
    }
    .mond {
      fill: none;
      stroke: white;
      stroke-width: 2px;
    }
  </style>
  <circle class="hoofd" cx="0" cy="-50" r="30" />
  <rect class="mond" x="-10" y="-40" width="20" height="5" rx="2" />
</svg>
```

<figure>
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .hoofd4 {
      fill: #cd803d;
    }
    .mond4 {
      fill: none;
      stroke: white;
      stroke-width: 2px;
    }
  </style>
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle class="hoofd4" cx="0" cy="-50" r="30" />
  <rect class="mond4" x="-10" y="-40" width="20" height="5" rx="2" />
</svg>
</figure>

### Peperkoeken mannetje

Zodra we alles hebben samengevoegd en ogen en knoppen hebben toegevoegd, ziet de uiteindelijke code er zo uit:

```html
<svg class="gingerbread" width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .hoofd {
      fill: #cd803d;
    }
    .oog {
      fill: white;
    }
    .mond {
      fill: none;
      stroke: white;
      stroke-width: 2px;
    }
    .ledemaat {
      stroke: #cd803d;
      stroke-width: 35px;
      stroke-linecap: round;
    }
  </style>
  <circle class="hoofd" cx="0" cy="-50" r="30" />
  <circle class="oog" cx="-12" cy="-55" r="3" />
  <circle class="oog" cx="12" cy="-55" r="3" />
  <rect class="mond" x="-10" y="-40" width="20" height="5" rx="2" />
  <line class="ledemaat" x1="-40" y1="-10" x2="40" y2="-10" />
  <line class="ledemaat" x1="-25" y1="50" x2="0" y2="-15" />
  <line class="ledemaat" x1="25" y1="50" x2="0" y2="-15" />
  <circle class="knoop" cx="0" cy="-10" r="5" />
  <circle class="knoop" cx="0" cy="10" r="5" />
</svg>
```

<figure>
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .hoofd {
      fill: #cd803d;
    }
    .oog {
      fill: white;
    }
    .mond {
      fill: none;
      stroke: white;
      stroke-width: 2px;
    }
    .ledemaat {
      stroke: #cd803d;
      stroke-width: 35px;
      stroke-linecap: round;
    }
  </style>
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle class="hoofd" cx="0" cy="-50" r="30" />
  <circle class="oog" cx="-12" cy="-55" r="3" />
  <circle class="oog" cx="12" cy="-55" r="3" />
  <rect class="mond" x="-10" y="-40" width="20" height="5" rx="2" />
  <line class="ledemaat" x1="-40" y1="-10" x2="40" y2="-10" />
  <line class="ledemaat" x1="-25" y1="50" x2="0" y2="-15" />
  <line class="ledemaat" x1="25" y1="50" x2="0" y2="-15" />
  <circle class="knoop" cx="0" cy="-10" r="5" />
  <circle class="knoop" cx="0" cy="10" r="5" />
</svg>
</figure>
