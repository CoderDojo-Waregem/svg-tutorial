Paden worden niet enkel gebruikt om vormen te tekenen. We kunnen ze ook gebruiken om tekst langs een onzichtbaar pad te laten lopen. We kunnen een cirkelvormig pad definiëren in de `defs` sectie en het gebruiken in een `textPath`-element om de tekst rond de cirkel te laten gaan. We gebruiken hier weer boog, maar je kunt elk ander pad gebruiken en de tekst zal de lijn volgen.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
    <path id="text-arc" d="M0,50 A50,50,0,1,1,1,50" />
  </defs>

  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <text fill="#0c5c4c" font-family="Tahoma" font-size="11" font-weight="bold">
    <textPath href="#text-arc">
      CoderDojo is cool! CoderDojo is cool! CoderDojo is cool!
    </textPath>
  </text>
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
    <path id="text-arc" d="M0,50 A50,50,0,1,1,1,50" />
  </defs>

  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <text fill="#0c5c4c" font-family="Tahoma" font-size="11" font-weight="bold">
    <textPath href="#text-arc">
      CoderDojo is cool! CoderDojo is cool! CoderDojo is cool!
    </textPath>
  </text>
</svg>
</figure>
