Alle paden die we tot nu toe getekend hebben, bestonden uit rechte lijnen. Laat ons eens deze gebogen kerstboom tekenen.

<figure>
<svg width="200px" height="250px" viewBox="-100 -100 200 250">
  <rect x="-100" y="-100" width="200" height="250" fill="#F5F1EB"/>
  <path fill="none" stroke="black" stroke-width="1" d="
      M0,-80
      L5,-75      L0,-70
      L-10,-65    L0,-60
      L15,-55     L0,-50
      L-20,-45    L0,-40
      L25,-35     L0,-30
      L-30,-25    L0,-20
      L35,-15     L0,-10
      L-40,-5     L0,0
      L45,5       L0,10
      L-50,15     L0,20
      L55,25      L0,30
      L-60,35     L0,40
      L65,45      L0,50
      L-70,55     L0,60
      L75,65      L0,70
      L-80,75     L0,80
      L85,85      L0,90
      L-90,95     L0,100
      L95,105     L0,110
      L-100,115   L0,120
      L0,140 L20,140 L-20,140" />
</svg>
</figure>

Het `path`-element wordt echt krachtig als we krommen gaan gebruiken. Een daarvan is de **kwadratische Bezierkromme**. Daarvoor moeten we niet alleen een eindpunt instellen, maar we moeten ook een controlepunt instellen.

Het controlepunt is een onzichtbare coördinaat waar de lijn naartoe buigt, maar niet raakt. Kijk naar dit blije gezicht! Hier is het onzichtbare controlepunt in het midden van de onderkant van de afbeelding (op coördinaat `0,100`).

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <circle cx="-50" cy="-50" r="20" />
  <circle cx="50" cy="-50" r="20" />
  <path d="M-70,50 Q0,100,70,50" fill="none" stroke="black" stroke-width="10" stroke-linecap="round" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="-50" cy="-50" r="20" />
  <circle cx="50" cy="-50" r="20" />
  <path d="M-70,50 Q0,100,70,50" fill="none" stroke="black" stroke-width="10" stroke-linecap="round" />
</svg>
</figure>

In dit voorbeeld ligt het controlepunt op dezelfde afstand van de twee eindpunten. Dit is niet noodzakelijk. In onderstaand voorbeeld markeren we het controlepunt met een cirkel. Merk op dat het controlepunt en de cirkel dezelfde coördinaten hebben.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-50,50 Q50,-50,50,50" fill="none" stroke="black" stroke-width="5" />
  <circle cx="50" cy="-50" r="5" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-50,50 Q50,-50,50,50" fill="none" stroke="black" stroke-width="5" />
  <circle cx="50" cy="-50" r="5" />
</svg>
</figure>

Klik hier voor [een interactieve demo](https://hunormarton.github.io/svg-curves){: target="_blank"} van kwadratische Bézierkrommen (selecteer **Quadratic Bézier** bovenaan de pagina).

Om onze gebogen kerstboom te tekenen, hebben we een reeks kwadratische Béziers waarbij de controlepunten steeds verder weg komen te liggen van het middelpunt van de boom naarmate het pad naar beneden gaat.

```html
<svg width="200px" height="250px" viewBox="-100 -100 200 250">
  <path fill="none" stroke="#0C5C4C" stroke-width="5" d="
      M0,-80
      Q5,-75,0,-70
      Q-10,-65,0,-60
      Q15,-55,0,-50
      Q-20,-45,0,-40
      Q25,-35,0,-30
      Q-30,-25,0,-20
      Q35,-15,0,-10
      Q-40,-5,0,0
      Q45,5,0,10
      Q-50,15,0,20
      Q55,25,0,30
      Q-60,35,0,40
      Q65,45,0,50
      Q-70,55,0,60
      Q75,65,0,70
      Q-80,75,0,80
      Q85,85,0,90
      Q-90,95,0,100
      Q95,105,0,110
      Q-100,115,0,120
      L0,140 L20,140 L-20,140" />
</svg>
```

<figure>
<svg width="200px" height="250px" viewBox="-100 -100 200 250">
  <rect x="-100" y="-100" width="200" height="250" fill="#F5F1EB"/>
  <path fill="none" stroke="#0C5C4C" stroke-width="5" d="
      M0,-80
      Q5,-75,0,-70
      Q-10,-65,0,-60
      Q15,-55,0,-50
      Q-20,-45,0,-40
      Q25,-35,0,-30
      Q-30,-25,0,-20
      Q35,-15,0,-10
      Q-40,-5,0,0
      Q45,5,0,10
      Q-50,15,0,20
      Q55,25,0,30
      Q-60,35,0,40
      Q65,45,0,50
      Q-70,55,0,60
      Q75,65,0,70
      Q-80,75,0,80
      Q85,85,0,90
      Q-90,95,0,100
      Q95,105,0,110
      Q-100,115,0,120
      L0,140 L20,140 L-20,140" />
</svg>
</figure>

Als we elke kwadratische Bézierkromme hierboven opsplitsen in twee lijnstukken met dezelfde coördinaten, dan zou dat er zo uitzien:

```html
<svg width="200px" height="250px" viewBox="-100 -100 200 250">
  <path fill="none" stroke="black" stroke-width="1" d="
      M0,-80
      L5,-75      L0,-70
      L-10,-65    L0,-60
      L15,-55     L0,-50
      L-20,-45    L0,-40
      L25,-35     L0,-30
      L-30,-25    L0,-20
      L35,-15     L0,-10
      L-40,-5     L0,0
      L45,5       L0,10
      L-50,15     L0,20
      L55,25      L0,30
      L-60,35     L0,40
      L65,45      L0,50
      L-70,55     L0,60
      L75,65      L0,70
      L-80,75     L0,80
      L85,85      L0,90
      L-90,95     L0,100
      L95,105     L0,110
      L-100,115   L0,120
      L0,140 L20,140 L-20,140" />
</svg>
```

<figure>
<svg width="200px" height="250px" viewBox="-100 -100 200 250">
  <rect x="-100" y="-100" width="200" height="250" fill="#F5F1EB"/>
  <path fill="none" stroke="black" stroke-width="1" d="
      M0,-80
      L5,-75      L0,-70
      L-10,-65    L0,-60
      L15,-55     L0,-50
      L-20,-45    L0,-40
      L25,-35     L0,-30
      L-30,-25    L0,-20
      L35,-15     L0,-10
      L-40,-5     L0,0
      L45,5       L0,10
      L-50,15     L0,20
      L55,25      L0,30
      L-60,35     L0,40
      L65,45      L0,50
      L-70,55     L0,60
      L75,65      L0,70
      L-80,75     L0,80
      L85,85      L0,90
      L-90,95     L0,100
      L95,105     L0,110
      L-100,115   L0,120
      L0,140 L20,140 L-20,140" />
</svg>
</figure>