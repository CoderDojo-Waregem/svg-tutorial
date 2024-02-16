Nadat we de basisvormen hebben behandeld, is het tijd om verder te gaan met het `path` element. Het pad is het krachtigste SVG-element. We kunnen bijna alles definiëren met paden en als je een SVG-bestand opent, zie je meestal paden. Laten we deze pijl tekenen met één enkel pad.

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-70,0 L70,0 L30,-50 M70,0 L30,50" 
    fill="none" stroke="#D1495B" stroke-width="25" stroke-linecap="round" stroke-linejoin="round" />
</svg>
</figure>

De vorm van een pad wordt gedefinieerd door het `d` attribuut. Daarin definiëren we verschillende tekencommando's. Een commando begint altijd met een letter die het type commando definieert en eindigt met een coördinaat.

Hier hebben we alleen de twee meest eenvoudige commando's nodig: ga-naar (*move-to*) en lijn-naar (*line-to*). Het ga-naar commando verplaatst de cursor naar een punt zonder een lijn te tekenen en het lijn-naar commando tekent een rechte lijn vanaf het vorige punt. Een commando gaat altijd verder met het vorige commando. Als we een lijn tekenen, bepalen we alleen het eindpunt. Het beginpunt is het eindpunt van het vorige commando.

### Pictogram voor een hamburger-menu

Voor we naar het voorbeeld van de pijl gaan, laat ons eerst een eenvoudig pictogram voor een hamburger-menu tekenen. We tekenen drie lijnen binnen hetzelfde pad met de commando's ga-naar (`M`) en lijn-naar (`L`). Eerst gaan we naar het begin van de bovenste lijn (`M40,-40`) en tekenen we een lijn naar het einde (`L40,-40`).

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-40,-40 L40,-40" stroke="#333333" stroke-width="25" stroke-linecap="round" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-40,-40 L40,-40" stroke="#333333" stroke-width="25" stroke-linecap="round" />
</svg>
</figure>

Daarna gaan we verder en tekenen we nog meer lijnen op dezelfde manier. Het coole aan paden is dat ze niet doorlopend hoeven te zijn. We kunnen verschillende ga-naar commando's hebben binnen hetzelfde pad. De komma's tussen de $$x$$- en $$y$$-coördinaten zijn optioneel en kunnen ook vervangen worden door spaties. Ook de spatie tussen het commando en de eerste coördinaat mag weggelaten worden.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-40,-40 L40,-40 M-40,0 L40,0 M-40,40 L40,40" 
    stroke="#333333" stroke-width="25" stroke-linecap="round" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-40,-40 L40,-40 M-40,0 L40,0 M-40,40 L40,40" 
    stroke="#333333" stroke-width="25" stroke-linecap="round" />
</svg>
</figure>

### Hartvormig pictogram

Hier is nog een voorbeeld gemaakt met een ga-naar commando en twee lijn-naar commando's.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-30,-20  L0,10 L30,-20" 
    fill="none" stroke="black" stroke-width="80" stroke-linecap="round" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-30,-20  L0,10 L30,-20" 
    fill="none" stroke="black" stroke-width="80" stroke-linecap="round" />
</svg>
</figure>

Als we in bovenstaand voorbeeld de waarde van de `stroke-width` eigenschap verlagen, dan zien we dat deze code eigenlijk een eenvoudige V-vorm is.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-30,-20  L0,10 L30,-20" 
    fill="none" stroke="black" stroke-width="10" stroke-linecap="round" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-30,-20  L0,10 L30,-20" 
    fill="none" stroke="black" stroke-width="10" stroke-linecap="round" />
</svg>
</figure>

### Pijlvormig pictogram

We kunnen op een vergelijkbare manier een pijl tekenen. We beginnen met een lijn in het midden en vervolgen de lijn om de bovenste vleugel te tekenen.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-70,0 L70,0 L30,-50" 
    fill="none" stroke="#D1495B" stroke-width="25" stroke-linecap="round" stroke-linejoin="round" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-70,0 L70,0 L30,-50" 
    fill="none" stroke="#D1495B" stroke-width="25" stroke-linecap="round" />
</svg>
</figure>

Je zou kunnen opmerken dat we in het vorige voorbeeld ook een `stroke-linejoin` eigenschap hadden om de samenvoeging af te ronden. Het werkt op een vergelijkbare manier als `stroke-linecap` maar dat heeft alleen invloed op het einde van de lijnen. Zonder die eigenschap zou dezelfde lijn er als volgt uitzien.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-70,0 L70,0 L30,-50" 
    fill="none" stroke="#D1495B" stroke-width="25" stroke-linecap="round" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-70,0 L70,0 L30,-50" 
    fill="none" stroke="#D1495B" stroke-width="25" stroke-linecap="round" />
</svg>
</figure>

Dan kunnen we de lijn afmaken door weer naar het einde van de horizontale lijn te gaan en een rechte lijn naar beneden te trekken om de onderste vleugel van de pijl te tekenen.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-70,0 L70,0 L30,-50 M70,0 L30,50" 
    fill="none" stroke="#D1495B" stroke-width="25" stroke-linecap="round" stroke-linejoin="round" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-70,0 L70,0 L30,-50 M70,0 L30,50" 
    fill="none" stroke="#D1495B" stroke-width="25" stroke-linecap="round" stroke-linejoin="round" />
</svg>
</figure>