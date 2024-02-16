We kunnen niet altijd basisvormen zoals cirkels of rechthoeken gebruiken om onze afbeeldingen samen te stellen. Dit is bijvoorbeeld het geval als we deze kerstboom willen tekenen.

<figure>
<svg width="200px" height="270px" viewBox="-100 -100 200 270">
  <rect x="-100" y="-100" width="270" height="270" fill="#F5F1EB"/>
  <polygon points="0,0 80,120 -80,120" fill="#234236" />
  <polygon points="0,-40 60,60 -60,60" fill="#0C5C4C" />
  <polygon points="0,-80 40,0 -40,0" fill="#38755B" />
  <rect x="-20" y="120" width="40" height="30" fill="brown" />
</svg>
</figure>

Een veelhoek (`polygon`) is de eenvoudigste manier om een vrije vorm te tekenen. Veelhoeken hebben een `points` eigenschap die een lijst van coördinaten bepaalt die verbonden zijn met rechte lijnen.

We kunnen de kroon van de boom maken van drie driehoeken. We beginnen met de onderste en voegen die laag voor laag toe.

```html
<svg width="200px" height="270px" viewBox="-100 -100 200 270">
  <polygon points="0,0 80,120 -80,120" fill="#234236" />
</svg>
```

<figure>
<svg width="200px" height="270px" viewBox="-100 -100 200 270">
  <rect x="-100" y="-100" width="270" height="270" fill="#F5F1EB"/>
  <polygon points="0,0 80,120 -80,120" fill="#234236" />
</svg>
</figure>

```html
<svg width="200px" height="270px" viewBox="-100 -100 200 270">
  <polygon points="0,0 80,120 -80,120" fill="#234236" />
  <polygon points="0,-40 60,60 -60,60" fill="#0C5C4C" />
</svg>
```

<figure>
<svg width="200px" height="270px" viewBox="-100 -100 200 270">
  <rect x="-100" y="-100" width="270" height="270" fill="#F5F1EB"/>
  <polygon points="0,0 80,120 -80,120" fill="#234236" />
  <polygon points="0,-40 60,60 -60,60" fill="#0C5C4C" />
</svg>
</figure>

```html
<svg width="200px" height="270px" viewBox="-100 -100 200 270">
  <polygon points="0,0 80,120 -80,120" fill="#234236" />
  <polygon points="0,-40 60,60 -60,60" fill="#0C5C4C" />
  <polygon points="0,-80 40,0 -40,0" fill="#38755B" />
</svg>
```

<figure>
<svg width="200px" height="270px" viewBox="-100 -100 200 270">
  <rect x="-100" y="-100" width="270" height="270" fill="#F5F1EB"/>
  <polygon points="0,0 80,120 -80,120" fill="#234236" />
  <polygon points="0,-40 60,60 -60,60" fill="#0C5C4C" />
  <polygon points="0,-80 40,0 -40,0" fill="#38755B" />
</svg>
</figure>

Ten slotte voegen we de stam van de boom toe als een rechthoek.

```html
<svg width="200px" height="270px" viewBox="-100 -100 200 270">
  <polygon points="0,0 80,120 -80,120" fill="#234236" />
  <polygon points="0,-40 60,60 -60,60" fill="#0C5C4C" />
  <polygon points="0,-80 40,0 -40,0" fill="#38755B" />
  <rect x="-20" y="120" width="40" height="30" fill="brown" />
</svg>
```

<figure>
<svg width="200px" height="270px" viewBox="-100 -100 200 270">
  <rect x="-100" y="-100" width="270" height="270" fill="#F5F1EB"/>
  <polygon points="0,0 80,120 -80,120" fill="#234236" />
  <polygon points="0,-40 60,60 -60,60" fill="#0C5C4C" />
  <polygon points="0,-80 40,0 -40,0" fill="#38755B" />
  <rect x="-20" y="120" width="40" height="30" fill="brown" />
</svg>
</figure>
