Laten we beginnen met een eenvoudige kerstbal te tekenen. 

<figure>
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="20" r="70" fill="#D1495B" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257" />
  <circle cx="0" cy="-75" r="12" fill="none" stroke="#F79257" stroke-width="2" />
</svg>
</figure>

Hiervoor gebruiken we alleen eenvoudige vormen: een rechthoek en twee cirkels. Merk op dat de oorsprong van het coördinatenstelsel in het midden van de afbeelding ligt.

Eerst definiëren we het belangrijkste deel van de kerstbal door een `circle` te tekenen. Om een cirkel te tekenen stellen we het middelpunt in (`cx` en `cy`) en de straal met de `r` eigenschap.

We hebben ook presentatie-attributen die onze vormen een stijl geven. Vergelijkbaar met de `background-color` eigenschap in CSS, stellen we de kleur voor de vorm in met het `fill` attribuut.

```html
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <circle cx="0" cy="20" r="70" fill="#D1495B" />
</svg>
```

<figure>
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="20" r="70" fill="#D1495B" />
</svg>
</figure>

Vervolgens tekenen we een rechthoek als een klein kapje bovenop de kerstbal met het `rect` element. In dit geval moeten we de positie linksboven van de rechthoek en de grootte instellen. We gebruiken het `fill` attribuut op dezelfde manier als bij de cirkel.

```html
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <circle cx="0" cy="20" r="70" fill="#D1495B" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257" />
</svg>
```

<figure>
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="20" r="70" fill="#D1495B" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257" />
</svg>
</figure>

Tot slot voegen we nog een cirkel toe als hanger bovenop deze elementen. Merk op dat we hetzelfde `circle` element gebruiken, maar met verschillende attributen. We stellen de eigenschap `fill` in op `"none"` en stellen een rand in voor de vorm met de eigenschappen `stroke` en `stroke-width`.

Dit is dan de uiteindelijke code van de afbeelding:

```html
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <circle cx="0" cy="20" r="70" fill="#D1495B" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257" />
  <circle cx="0" cy="-75" r="12" fill="none" stroke="#F79257" stroke-width="2" />
</svg>
```

<figure>
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle cx="0" cy="20" r="70" fill="#D1495B" />
  <rect x="-17.5" y="-65" width="35" height="20" fill="#F79257" />
  <circle cx="0" cy="-75" r="12" fill="none" stroke="#F79257" stroke-width="2" />
</svg>
</figure>

