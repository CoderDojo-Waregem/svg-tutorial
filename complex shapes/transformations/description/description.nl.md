Een ster is een eenvoudige vorm.

<figure>
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
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
</svg>
</figure>

We zouden het kunnen definiëren als een hoop veelhoeken en elk punt afzonderlijk kunnen instellen. Maar dan zouden we elke coördinaat afzonderlijk moeten bepalen. In plaats daarvan kunnen we slechts één arm definiëren en deze dan vijf keer herhalen met een rotatie om dezelfde vorm te krijgen. We zullen het `transform` attribuut gebruiken om een rotatie in te stellen.

Laten we eerst een arm definiëren. In dit voorbeeld bestaat elke arm uit twee veelhoeken.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <polygon points="0,0 36,-50 0,-100" fill="#EDD8B7" />
  <polygon points="0,0 -36,-50 0,-100" fill="#E5C39C" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <polygon points="0,0 36,-50 0,-100" fill="#EDD8B7" />
  <polygon points="0,0 -36,-50 0,-100" fill="#E5C39C" />
</svg>
</figure>

We kunnen ze groeperen met een `g` element en samen roteren. Het `g` element kan andere elementen bevatten en attributen gedefinieerd op het groepselement zijn van toepassing op zijn kinderen.

Vervolgens roteren we elke arm in de juiste positie met een `rotate` transformatie.

```html
<svg width="200" height="200" viewBox="-100 -100 200 200">
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
</svg>
```

<figure>
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
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
</svg>
</figure>

Je hebt misschien opgemerkt dat we onze veelhoeken definiëren om te starten vanuit de oorsprong van het coördinatenstelsel (dat is het middelpunt van de afbeelding). Standaard is de rotatie ook rond de oorsprong van het coördinatenstelsel.

Omdat we vijf armen hebben, is de onderkant van de afbeelding iets korter dan de bovenkant van de afbeelding. Om de afbeelding te centreren, kunnen we de hele ster groeperen en de `translate` transformatie gebruiken om alles 5 eenheden naar beneden te verplaatsen langs de $$y$$ coordinaat.

In dit voorbeeld moesten we de code voor elke arm steeds opnieuw kopiëren en plakken. In het volgende voorbeeld zullen we zien hoe we vormen kunnen hergebruiken.
