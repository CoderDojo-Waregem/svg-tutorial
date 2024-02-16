In plaats van steeds dezelfde code te herhalen, kunnen we ook een definitie voor een vorm maken en die hergebruiken. Hier definiëren we een tak van een sneeuwvlok en gebruiken deze vervolgens zes keer met verschillende rotaties.

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <defs>
    <path id="tak1" stroke="#E5C39C" stroke-width="5" d="
      M0,0 L0,-90
      M0,-20 L20,-34
      M0,-20 L-20,-34
      M0,-40 L20,-54
      M0,-40 L-20,-54
      M0,-60 L20-74
      M0,-60 L-20,-74" 
    />
  </defs>
  
  <use href="#tak1" />
  <use href="#tak1" transform="rotate(60)" />
  <use href="#tak1" transform="rotate(120)" />
  <use href="#tak1" transform="rotate(180)" />
  <use href="#tak1" transform="rotate(240)" />
  <use href="#tak1" transform="rotate(300)" />
</svg>
</figure>

### Een tak van de sneeuwvlok tekenen

De tak is gedefinieerd als een `path`. Eerder hebben we al behandeld hoe je basispaden tekent. Hier tekenen we de tak op een vergelijkbare manier. We kunnen een eenvoudige lijn tekenen - de hoofdtak - door gebruik te maken van de ga-naar (`M`) en lijn-naar (`L`) commando's:

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path stroke="#E5C39C" stroke-width="5" d="M0,0 L0,-90" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path stroke="#E5C39C" stroke-width="5" d="M0,0 L0,-90" />
</svg>
</figure>

Dan kunnen we verder gaan met tekenen en een zijtak toevoegen door nog een ga-naar en een lijn-naar commando toe te voegen:

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path stroke="#E5C39C" stroke-width="5" d="M0,0 L0,-90 M0,-20 L20,-34" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path stroke="#E5C39C" stroke-width="5" d="M0,0 L0,-90 M0,-20 L20,-34" />
</svg>
</figure>

De voltooide tak zou er als volgt uitzien:

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path id="tak" stroke="#E5C39C" stroke-width="5" d="
    M0,0 L0,-90
    M0,-20 L20,-34
    M0,-20 L-20,-34
    M0,-40 L20,-54
    M0,-40 L-20,-54
    M0,-60 L20-74
    M0,-60 L-20,-74" 
  />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path id="tak" stroke="#E5C39C" stroke-width="5" d="
    M0,0 L0,-90
    M0,-20 L20,-34
    M0,-20 L-20,-34
    M0,-40 L20,-54
    M0,-40 L-20,-54
    M0,-60 L20-74
    M0,-60 L-20,-74" 
  />
</svg>
</figure>

### Afbeeldingselementen hergebruiken

Dan kunnen we het volledige tak pad verplaatsen naar de `defs` sectie. De `defs` sectie is een verborgen compartiment van onze afbeelding. Dingen hier verschijnen niet op het scherm, maar we kunnen ernaar verwijzen en ze later gebruiken.

Als we eenmaal een tak hebben gedefinieerd, kunnen we deze op de volgende manier meerdere keren gebruiken met het `use` commando.

Vervolgens kunnen we de individuele takken naar hun juiste positie verplaatsen met het `transform` commando, op dezelfde manier als we deden met het voorbeeld van de ster.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
    <path id="tak" stroke="#E5C39C" stroke-width="5" d="
      M0,0 L0,-90
      M0,-20 L20,-34
      M0,-20 L-20,-34
      M0,-40 L20,-54
      M0,-40 L-20,-54
      M0,-60 L20-74
      M0,-60 L-20,-74" 
    />
  </defs>
  
  <use href="#tak" />
  <use href="#tak" transform="rotate(60)" />
  <use href="#tak" transform="rotate(120)" />
  <use href="#tak" transform="rotate(180)" />
  <use href="#tak" transform="rotate(240)" />
  <use href="#tak" transform="rotate(300)" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <defs>
    <path id="tak" stroke="#E5C39C" stroke-width="5" d="
      M0,0 L0,-90
      M0,-20 L20,-34
      M0,-20 L-20,-34
      M0,-40 L20,-54
      M0,-40 L-20,-54
      M0,-60 L20-74
      M0,-60 L-20,-74" 
    />
  </defs>
  
  <use href="#tak" />
  <use href="#tak" transform="rotate(60)" />
  <use href="#tak" transform="rotate(120)" />
  <use href="#tak" transform="rotate(180)" />
  <use href="#tak" transform="rotate(240)" />
  <use href="#tak" transform="rotate(300)" />
</svg>
</figure>
