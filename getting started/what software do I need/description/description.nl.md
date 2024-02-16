Een SVG-bestand is een tekstbestand. Je hebt enkel een teksteditor nodig om de tekst op te stellen voor de SVG-afbeelding. De afspraak is dat je een tekstbestand met een SVG-afbeelding opslaat met de extensie `.svg`. Wanneer je dubbelklikt op een bestand met een `.svg` extensie, dan krijg je de afbeelding in een browser te zien.

Wij zullen gebruikmaken van de online teksteditor [StackBlitz](https://stackblitz.com/fork/web-platform){: target="_blank"}. Daarmee hoef je helemaal geen editor te installeren op je computer, en krijg je bij elke aanpassing meteen ook het resultaat van de afbeelding te zien.

<div class="dodona-centered-group">
  <img width="80%" src="media/stackblitz.png" data-caption="In de online teksteditor StackBlitz kan je de tekst van een SVG-afbeelding schrijven in het <samp>index.html</samp> bestand, en krijg je meteen het resultaat te zien." />
</div>

Daar kan je de tekst voor de SVG-afbeelding rechtstreeks in het bestand `index.html` plaatsen. Het is ook niet nodig om HTML-code schrijven. Je kunt je enkel tot de SVG-afbeelding beperken.

```html
<svg width="100px" height="100px" viewBox="0 0 100 100">
  <cirkel cx="50" cy="50" r="25" fill="red" />
</svg>
```

Als je een mooie SVG-afbeelding gemaakt hebt, vergeet die dan ook niet  op je computer op te slaan in een tekstbestand met de extensie `.svg`!
