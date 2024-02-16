Rotatie is niet de enige manier waarop we afbeeldingen kunnen genereren uit eenvoudige vormen. In dit voorbeeld definiëren we een boomvorm en plaatsen deze vervolgens op verschillende posities in verschillende groottes om een bos te tekenen.

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
    <g id="boom">
      <polygon points="-10,0 10,0 0 -50" fill="#38755b" />
      <line x1="0" y1="0" x2="0" y2="10" stroke="#778074" stroke-width="2" />
    </g>
  </defs>

  <rect x="-100" y="-100" width="200" height="200" fill="#F1DBC3" />
  <circle cx="0" cy="380" r="350" fill="#F8F4E8" />

  <use href="#boom" x="-30" y="25" transform="scale(2)" />
  <use href="#boom" x="-20" y="40" transform="scale(1.2)" />
  <use href="#boom" x="40" y="40" />
  <use href="#boom" x="50" y="30" transform="scale(1.5)" />
</svg>
</figure>

Eerst maken we een achtergrond van een rechthoek en een cirkel.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F1DBC3" />
  <circle cx="0" cy="380" r="350" fill="#F8F4E8" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F1DBC3" />
  <circle cx="0" cy="380" r="350" fill="#F8F4E8" />
</svg>
</figure>

Dan definiëren we een boomvorm uit een eenvoudige veelhoek en een lijn.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <polygon points="-10,0 10,0 0 -50" fill="#38755b" />
  <line x1="0" y1="0" x2="0" y2="10" stroke="#778074" stroke-width="2" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <polygon points="-10,0 10,0 0 -50" fill="#38755b" />
  <line x1="0" y1="0" x2="0" y2="10" stroke="#778074" stroke-width="2" />
</svg>
</figure>

Dan kunnen we de boomvorm op dezelfde manier hergebruiken als in het voorbeeld met het sneeuwvlokje. We verplaatsen de boomvorm naar de `defs` sectie, nemen het op in een groepselement, stellen er een ID voor in en hergebruiken het met het `use` element.

Hier positioneren we ook de hergebruikte elementen door een `x` en `y` coördinaat in te stellen en om wat perspectief aan de afbeelding toe te voegen gebruiken we de `scale` transformatie.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
    <g id="boom">
      <polygon points="-10,0 10,0 0 -50" fill="#38755b" />
      <line x1="0" y1="0" x2="0" y2="10" stroke="#778074" stroke-width="2" />
    </g>
  </defs>

  <rect x="-100" y="-100" width="200" height="200" fill="#F1DBC3" />
  <circle cx="0" cy="380" r="350" fill="#F8F4E8" />

  <use href="#boom" x="-30" y="25" transform="scale(2)" />
  <use href="#boom" x="-20" y="40" transform="scale(1.2)" />
  <use href="#boom" x="40" y="40" />
  <use href="#boom" x="50" y="30" transform="scale(1.5)" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
    <g id="boom">
      <polygon points="-10,0 10,0 0 -50" fill="#38755b" />
      <line x1="0" y1="0" x2="0" y2="10" stroke="#778074" stroke-width="2" />
    </g>
  </defs>

  <rect x="-100" y="-100" width="200" height="200" fill="#F1DBC3" />
  <circle cx="0" cy="380" r="350" fill="#F8F4E8" />

  <use href="#boom" x="-30" y="25" transform="scale(2)" />
  <use href="#boom" x="-20" y="40" transform="scale(1.2)" />
  <use href="#boom" x="40" y="40" />
  <use href="#boom" x="50" y="30" transform="scale(1.5)" />
</svg>
</figure>
