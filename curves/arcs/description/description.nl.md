Een boog is een deel van een cirkel of ellips. Laten we eens kijken hoe we bogen kunnen gebruiken om dit snoepje te tekenen.

<figure>
<svg width="200px" height="400px" viewBox="-100 -200 200 400">
  <style>
    .body {
      stroke-linecap: round;
      fill: none;
    }    
    .red-mark {
      stroke: #d1495b;
      stroke-width: 2.5px;
    }
    .green-mark {
      stroke: #234236;
      stroke-width: 2.5px;
    }
  </style>

  <rect x="-100" y="-200" width="200" height="400" fill="#F5F1EB"/>
  <path class="body" d="M50,120 L50,-80 A50,50,0,0,0,-50,-80" stroke="#cd803d" stroke-width="45" />
  <path class="body" d="M50,120 L50,-80 A50,50,0,0,0,-50,-80" stroke="white" stroke-width="40" />
  <line class="green-mark" x1="-35" y1="-90" x2="-60" y2="-100" />
  <line class="red-mark" x1="-15" y1="-115" x2="-25" y2="-135" />
  <line class="green-mark" x1="20" y1="-110" x2="35" y2="-130" />
  <line class="red-mark" x1="40" y1="-60" x2="60" y2="-80" />
  <line class="green-mark" x1="40" y1="-10" x2="60" y2="-30" />
  <line class="red-mark" x1="40" y1="40" x2="60" y2="20" />
  <line class="green-mark" x1="40" y1="90" x2="60" y2="70" />
</svg>
</figure>

Als je dacht dat kubische Béziers de meest ingewikkelde onderdelen van een SVG zijn, dan hebben we slecht nieuws voor je. Bogen zijn veel ingewikkelder. Het goede nieuws is echter dat ze zelden worden gebruikt, en we zullen ze in de komende voorbeelden ook niet veel gebruiken.

### De verschillende parameters van een boog

Het boog-naar (*arc-to*; `A`) commando heeft 7 parameters.

<pre>
A rx ry rotatie grote-boog-vlag veeg-vlag x y
</pre>

De laatste twee parameters `(40, 40)` zijn nog steeds het eindpunt van de boog. De eerste twee definiëren een horizontale en een verticale straal `(70, 70)`. Als we een cirkel tekenen, dan zijn deze twee waarden hetzelfde.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-40,-40 A70,70,0,0,0,40,40" fill="none" stroke="red" stroke-width="2" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-40,-40 A70,70,0,0,0,40,40" fill="none" stroke="red" stroke-width="2" />
</svg>
</figure>

Je realiseert je misschien dat zelfs met hetzelfde begin- en eindpunt en dezelfde stralen er vier verschillende variaties kunnen zijn. Het 5e argument is een booleaanse vlag die we kunnen gebruiken om de boog de andere kant op te draaien (nu aangepast naar `1`).

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-40,-40 A70,70,0,0,1,40,40" fill="none" stroke="red" stroke-width="2" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-40,-40 A70,70,0,0,1,40,40" fill="none" stroke="red" stroke-width="2" />
</svg>
</figure>

Het zal je opvallen dat in beide gevallen de boog de kortst mogelijke weg aflegt met deze parameters. Het is ook mogelijk om de lange weg te nemen en toch dezelfde begin- en eindpunten en dezelfde stralen te behouden. Dan is het 4e argument nog een booleaanse vlag die aangeeft of we de lange weg willen nemen (nu hebben we die parameter aangepast naar `1`). Dit heeft ook twee variaties. Je kunt de boog spiegelen door het 5e argument om te keren naar de andere waarde.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-40,-40 A70,70,0,1,1,40,40" fill="none" stroke="red" stroke-width="2" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-40,-40 A70,70,0,1,1,40,40" fill="none" stroke="red" stroke-width="2" />
</svg>
</figure>

Om het nog ingewikkelder te maken, als we de horizontale en verticale stralen op twee verschillende waarden instellen, dan krijgen we een ellipsboog `(70, 40)`. Opnieuw dezelfde begin- en eindpunten, en ook deze heeft 4 verschillende variaties.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-40,-40 A70,40,0,1,1,40,40" fill="none" stroke="red" stroke-width="2" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-40,-40 A70,40,0,1,1,40,40" fill="none" stroke="red" stroke-width="2" />
</svg>
</figure>

Ten slotte kunnen we, als we een ellips tekenen, deze ook draaien over een bepaalde een hoek. We kunnen dit instellen met de 3e parameter (`30`). Wat de dingen nog verdraaider maakt, is dat onze denkbeeldige ellips niet om zijn middelpunt wordt gedraaid, omdat deze boog nog steeds dezelfde begin- en eindpunten moet behouden. Als we een cirkel tekenen, heeft de rotatie geen invloed op de boog.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path d="M-40,-40 A70,40,30,1,1,40,40" fill="none" stroke="red" stroke-width="2" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path d="M-40,-40 A70,40,30,1,1,40,40" fill="none" stroke="red" stroke-width="2" />
</svg>
</figure>

Klik hier voor [een interactieve demo](https://hunormarton.github.io/svg-curves){: target="_blank"} van bogen.

### Een snoepje tekenen

Na al deze inleidingen zijn we eindelijk aangekomen bij het voorbeeld dat we wilden uitwerken. In dit voorbeeld gaan we alleen een eenvoudige boog tekenen.

```html
<svg width="200px" height="400px" viewBox="-100 -200 200 400">
  <style>
    .body {
      stroke-linecap: round;
      fill: none;
    }    
  </style>

  <path class="body" d="M50,120 L50,-80 A50,50,0,0,0,-50,-80" stroke="#cd803d" stroke-width="45" />
</svg>
```

<figure>
<svg width="200px" height="400px" viewBox="-100 -200 200 400">
  <style>
    .body {
      stroke-linecap: round;
      fill: none;
    }    
  </style>

  <rect x="-100" y="-200" width="200" height="400" fill="#F5F1EB"/>
  <path class="body" d="M50,120 L50,-80 A50,50,0,0,0,-50,-80" stroke="#cd803d" stroke-width="45" />
</svg>
</figure>

Om een snoepje te tekenen, trekken we een dikke lijn die bestaat uit een rechte lijn en een halve cirkel. Daarna tekenen we dezelfde lijn opnieuw, met een iets dunnere lijndikte. Door er twee verschillende kleuren voor in te stellen, lijkt het alsof de ene de rand van de andere is.

Voor de afwerking voegen we een paar rechte lijnen toe binnen deze vorm als markeringen.

```html
<svg width="200px" height="400px" viewBox="-100 -200 200 400">
  <style>
    .body {
      stroke-linecap: round;
      fill: none;
    }    
    .red-mark {
      stroke: #d1495b;
      stroke-width: 2.5px;
    }
    .green-mark {
      stroke: #234236;
      stroke-width: 2.5px;
    }
  </style>

  <path class="body" d="M50,120 L50,-80 A50,50,0,0,0,-50,-80" stroke="#cd803d" stroke-width="45" />
  <path class="body" d="M50,120 L50,-80 A50,50,0,0,0,-50,-80" stroke="white" stroke-width="40" />
  <line class="green-mark" x1="-35" y1="-90" x2="-60" y2="-100" />
  <line class="red-mark" x1="-15" y1="-115" x2="-25" y2="-135" />
  <line class="green-mark" x1="20" y1="-110" x2="35" y2="-130" />
  <line class="red-mark" x1="40" y1="-60" x2="60" y2="-80" />
  <line class="green-mark" x1="40" y1="-10" x2="60" y2="-30" />
  <line class="red-mark" x1="40" y1="40" x2="60" y2="20" />
  <line class="green-mark" x1="40" y1="90" x2="60" y2="70" />
</svg>
```

<figure>
<svg width="200px" height="400px" viewBox="-100 -200 200 400">
  <style>
    .body {
      stroke-linecap: round;
      fill: none;
    }    
    .red-mark {
      stroke: #d1495b;
      stroke-width: 2.5px;
    }
    .green-mark {
      stroke: #234236;
      stroke-width: 2.5px;
    }
  </style>

  <rect x="-100" y="-200" width="200" height="400" fill="#F5F1EB"/>
  <path class="body" d="M50,120 L50,-80 A50,50,0,0,0,-50,-80" stroke="#cd803d" stroke-width="45" />
  <path class="body" d="M50,120 L50,-80 A50,50,0,0,0,-50,-80" stroke="white" stroke-width="40" />
  <line class="green-mark" x1="-35" y1="-90" x2="-60" y2="-100" />
  <line class="red-mark" x1="-15" y1="-115" x2="-25" y2="-135" />
  <line class="green-mark" x1="20" y1="-110" x2="35" y2="-130" />
  <line class="red-mark" x1="40" y1="-60" x2="60" y2="-80" />
  <line class="green-mark" x1="40" y1="-10" x2="60" y2="-30" />
  <line class="red-mark" x1="40" y1="40" x2="60" y2="20" />
  <line class="green-mark" x1="40" y1="90" x2="60" y2="70" />
</svg>
</figure>
