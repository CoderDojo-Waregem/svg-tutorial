Voordat we beginnen met tekenen, moeten we het hebben over het `svg` element zelf. Het SVG-element bevat de afbeeldingselementen en definieert het frame van onze afbeelding. Het stelt de binnenmaat en de buitenmaat van de afbeelding in.

De eigenschappen `width` (breedte) en `height` (hoogte) bepalen hoeveel ruimte de afbeelding inneemt in de browser. Er is ook een eigenschap `viewBox` die een coördinatensysteem definieert voor de afbeeldingselementen. De eerste twee waarden in `viewBox` definiëren de coördinaat linksboven in de afbeelding en de laatste twee definiëren de grootte vanuit het perspectief van de afbeeldingselementen.

- De grootte die wordt gedefinieerd door `width` en `height` is hoe de rest van HTML denkt over de afbeelding en hoe groot deze wordt weergegeven in de browser.
- De grootte gedefinieerd door `viewBox` is hoe de afbeeldingselementen denken over de afbeelding wanneer ze zichzelf positioneren.

In de volgende drie voorbeelden hebben we drie SVG-afbeeldingen die precies dezelfde inhoud hebben. Een `circle` element met hetzelfde middelpunt en dezelfde straal. Ze zien er echter heel anders uit. Als de door `viewBox` gedefinieerde grootte niet overeenkomt met de eigenschappen `width` en `height`, dan wordt de afbeelding groter of kleiner gemaakt.

```html
<svg width="100" height="100" viewBox="0 0 200 200">
  <circle cx="100" cy="100" r="50" />
</svg>
```

<figure>
<svg width="100" height="100" viewBox="0 0 200 200">
  <rect x="0" y="0" width="200" height="200" stroke="gray" stroke-width="4" stroke-dasharray="4,4" fill="none"/>
  <circle cx="100" cy="100" r="50" />
</svg>
</figure>

```html
<svg width="200" height="200" viewBox="0 0 200 200">
  <circle cx="100" cy="100" r="50" />
</svg>
```

<figure>
<svg width="200" height="200" viewBox="0 0 200 200">
  <rect x="0" y="0" width="200" height="200" stroke="gray" stroke-width="2" stroke-dasharray="2,2" fill="none"/>
  <circle cx="100" cy="100" r="50" />
</svg>
</figure>

```html
<svg width="100" height="100" viewBox="0 0 200 200">
  <circle cx="100" cy="100" r="50" />
</svg>
```

<figure>
<svg width="200" height="200" viewBox="0 0 100 100">
  <rect x="0" y="0" width="100" height="100" stroke="gray" stroke-width="1" stroke-dasharray="1,1" fill="none"/>
  <circle cx="100" cy="100" r="50" />
</svg>
</figure>

We kunnen ook instellen welke coördinaat in de linkerbovenhoek van de afbeelding moet staan. In het volgende voorbeeld verplaatsen we de oorsprong van het coördinatensysteem naar het midden van de afbeelding. We stellen de linkerbovenhoek in op `-100,-100`, wat de helft is van de afbeeldingsgrootte in negatief.

Merk op dat positie van het middelpunt van de cirkel nu `0,0` is.

```html
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <circle cx="0" cy="0" r="50" />
</svg>
```

<figure>
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" stroke="gray" stroke-width="2" stroke-dasharray="2,2" fill="none"/>
  <circle cx="0" cy="0" r="50" />
</svg>
</figure>

SVG-afbeeldingen hebben vaak ook een eigenschap `xmlns`. Deze eigenschap kan echter weggelaten worden als de afbeelding in een HTML-document vervat zit.
