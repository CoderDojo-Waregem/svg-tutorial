[SVG](https://developer.mozilla.org/en-US/docs/Web/SVG){: target="_blank"} (*Scalable Vector Graphics*) heeft een grammatica die heel sterk lijkt op HTML. Ze zijn beide gebaseerd op [XML](https://developer.mozilla.org/en-US/docs/Web/XML){: target="_blank"}. Sinds [HTML5](https://en.wikipedia.org/wiki/HTML5){: target="_blank"} kunnen we de code van een SVG-afbeelding ook gewoon in een HTML-bestand plaatsen:

```html
<html>
  <h1>Dag ninja</h1>
  <svg width="100px" height="100px" viewBox="0 0 100 100">
    <cirkel cx="50" cy="50" r="25" fill="red" />
  </svg>
</html>
```

Hierdoor kunnen we heel wat coole dingen doen. We kunnen delen van een afbeelding aanspreken met JavaScript om iets interactief te maken, of we kunnen kunst genereren met code. We kunnen ook een deel van de vormgeving overlaten aan CSS en zelfs afbeeldingselementen animeren met CSS.

In deze handleiding verkennen we stap voor stap hoe je SVG-afbeeldingen kunt opbouwen, van basis tot meer geavanceerde onderwerpen.
