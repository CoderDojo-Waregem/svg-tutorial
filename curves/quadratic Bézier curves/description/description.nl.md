Dit is dezelfde kerstbal die we eerder ook al getekend hebben, behalve dat hij nu een motief aan de zijkant heeft dat gedefinieerd wordt als een `polyline`.

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
    <clipPath id="bal1">
      <circle cx="0" cy="20" r="70" />
    </clipPath>
  </defs>

  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="20" r="70" fill="#D1495B" />
  <polyline clip-path="url(#bal1)" fill="none" stroke="#9C2D2A" stroke-width="20"
    points="-120 40 -80 0 -40 40 0 0 40 40 80 0 120 40" />
  <circle cx="0" cy="-75" r="12" fill="none" stroke="#F79257" stroke-width="2" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257" />
</svg>
</figure>

Standaard zou de `polyline` niet samenvallen met de rand van de cirkel. Zonder **bijknippen** zou het motief er zo uitzien:

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="20" r="70" fill="#D1495B" />
  <polyline fill="none" stroke="#9C2D2A" stroke-width="20"
    points="-120 40 -80 0 -40 40 0 0 40 40 80 0 120 40" />
  <circle cx="0" cy="-75" r="12" fill="none" stroke="#F79257" stroke-width="2" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257" />
</svg>
</figure>

We gebruiken hier een `clip-path` om ervoor te zorgen dat het motief perfect op de kerstbal past. Het `clip-path` wordt gedefinieerd in de sectie `defs`.

Daar definiëren we een `clipPath` met een ID. De inhoud van dit `clip-pad` is een cirkel die overeenkomt met de grootte van onze kerstbal. Daarna gebruiken we het `clip-pad` om de `polyline` bij te knippen door de `clip-path` eigenschap ervan in te stellen.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
    <clipPath id="bal">
      <circle cx="0" cy="20" r="70" />
    </clipPath>
  </defs>

  <circle cx="0" cy="20" r="70" fill="#D1495B" />
  <polyline clip-path="url(#bal)" fill="none" stroke="#9C2D2A" stroke-width="20"
    points="-120 40 -80 0 -40 40 0 0 40 40 80 0 120 40" />
  <circle cx="0" cy="-75" r="12" fill="none" stroke="#F79257" stroke-width="2" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
    <clipPath id="bal">
      <circle cx="0" cy="20" r="70" />
    </clipPath>
  </defs>

  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="20" r="70" fill="#D1495B" />
  <polyline clip-path="url(#bal)"  fill="none" stroke="#9C2D2A" stroke-width="20"
    points="-120 40 -80 0 -40 40 0 0 40 40 80 0 120 40" />
  <circle cx="0" cy="-75" r="12" fill="none" stroke="#F79257" stroke-width="2" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257" />
</svg>
</figure>
