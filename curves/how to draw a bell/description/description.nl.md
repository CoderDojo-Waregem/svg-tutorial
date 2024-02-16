Laten we nog een voorbeeld tekenen met kubische en kwadratische Bézierkrommen.

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <g stroke="black" stroke-width="2">
    <circle cx="0" cy="-45" r="7" fill="#4F6D7A" />
    <circle cx="0" cy="50" r="10" fill="#F79257" />
    <path fill="#FDEA96" d="
        M-50,40
        L-50,50
        L50,50
        L50,40
        Q40,40,40,10
        C40,-60,-40,-60,-40,10
        Q-40,40,-50,40"
    />
  </g>
</svg>
</figure>

De onderkant van deze klok wordt gedefinieerd met rechte lijnen.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path fill="#FDEA96" stroke="black" stroke-width="2" d="
      M-50,40
      L-50,50
      L50,50
      L50,40"
  />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path fill="#FDEA96" stroke="black" stroke-width="2" d="
      M-50,40
      L-50,50
      L50,50
      L50,40"
  />
</svg>
</figure>

Dan begint een kwadratische Bézier de klokmantel.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path fill="#FDEA96" stroke="black" stroke-width="2" d="
      M-50,40
      L-50,50
      L50,50
      L50,40
      Q40,40,40,10"
  />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path fill="#FDEA96" stroke="black" stroke-width="2" d="
      M-50,40
      L-50,50
      L50,50
      L50,40
      Q40,40,40,10"
  />
  <circle cx="40" cy="40" r="2" stroke="none" fill="red"></circle>
</svg>
</figure>

Daarna wordt de lijn voortgezet met een kubische Bézier om de top van de bel te vormen.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path fill="#FDEA96" stroke="black" stroke-width="2" d="
      M-50,40
      L-50,50
      L50,50
      L50,40
      Q40,40,40,10
      C40,-60,-40,-60,-40,10"
  />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path fill="#FDEA96" stroke="black" stroke-width="2" d="
      M-50,40
      L-50,50
      L50,50
      L50,40
      Q40,40,40,10
      C40,-60,-40,-60,-40,10"
  />
  <circle cx="-40" cy="-60" r="2" stroke="none" fill="red"></circle>
  <circle cx="40" cy="-60" r="2" stroke="none" fill="red"></circle>
</svg>
</figure>

Dan bereiken we het onderste deel met nog een kwadratische Bézier die het spiegelbeeld vormt van de vorige.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path fill="#FDEA96" stroke="black" stroke-width="2" d="
      M-50,40
      L-50,50
      L50,50
      L50,40
      Q40,40,40,10
      C40,-60,-40,-60,-40,10
      Q-40,40,-50,40"
  />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path fill="#FDEA96" stroke="black" stroke-width="2" d="
      M-50,40
      L-50,50
      L50,50
      L50,40
      Q40,40,40,10
      C40,-60,-40,-60,-40,10
      Q-40,40,-50,40"
  />
  <circle cx="-40" cy="40" r="2" stroke="none" fill="red"></circle>
</svg>
</figure>


We maken de klok af door twee cirkels toe te voegen voor de klepel en de hanger.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <g stroke="black" stroke-width="2">
    <circle cx="0" cy="-45" r="7" fill="#4F6D7A" />
    <circle cx="0" cy="50" r="10" fill="#F79257" />
    <path fill="#FDEA96" d="
        M-50,40
        L-50,50
        L50,50
        L50,40
        Q40,40,40,10
        C40,-60,-40,-60,-40,10
        Q-40,40,-50,40"
    />
  </g>
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <g stroke="black" stroke-width="2">
    <circle cx="0" cy="-45" r="7" fill="#4F6D7A" />
    <circle cx="0" cy="50" r="10" fill="#F79257" />
    <path fill="#FDEA96" d="
        M-50,40
        L-50,50
        L50,50
        L50,40
        Q40,40,40,10
        C40,-60,-40,-60,-40,10
        Q-40,40,-50,40"
    />
  </g>
</svg>
</figure>
