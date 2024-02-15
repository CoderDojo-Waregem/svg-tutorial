In dit voorbeeld combineren we alles wat we tot nu toe hebben geleerd. We gebruiken hier cirkels, rechthoeken, lijnen, `polyline` en veelhoeken.

We beginnen met de voorkant zelf. Merk op dat we niet alleen een klasse hebben voor het gevel-element, maar ook voor de hele SVG.

```html
<svg class="huis" width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .huis {
      stroke: black;
      stroke-width: 2px;
      fill: white;
    }
  </style>
  <polygon class="gevel" points="-65,80 -65,-10 0,-70 65,-10 65,80" />
</svg>
```

<figure>
<svg class="huis1" width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .huis1 {
      stroke: black;
      stroke-width: 2px;
      fill: white;
    }
    .huis1 .achtergrond {
      stroke: none;
      fill: #F5F1EB;
    }
  </style>
  <rect class="achtergrond" x="-100" y="-100" width="200" height="200" />
  <polygon class="gevel" points="-65,80 -65,-10 0,-70 65,-10 65,80" />
</svg>
</figure>

Daarna voegen we er een dak bovenop. Dit is het enige dat hier nieuw is. We gebruiken een `polyline`. Het verschil tussen een `polyline` en een `polygon` is dat een `polygon` zichzelf altijd sluit, en de `polyline` open blijft. Merk op dat we de `stroke-linecap` eigenschap weer gebruiken zoals we deden met het voorbeeld van de peperkoekfiguur.

```html
<svg class="huis" width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .huis {
      stroke: black;
      stroke-width: 2px;
      fill: white;
    }
  </style>
  <polygon class="gevel" points="-65,80 -65,-10 0,-70 65,-10 65,80" />
</svg>
```
<figure>
<svg class="huis2" width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .huis2 .dak {
      fill: none;
      stroke: #d1495b;
      stroke-width: 10px;
      stroke-linecap: round;
    }
    .huis2 .achtergrond {
      stroke: none;
      fill: #F5F1EB;
    }
  </style>
  <rect class="achtergrond" x="-100" y="-100" width="200" height="200" />
  <polyline class="dak" points="-75,-8 0,-78 75,-8" />
</svg>
</figure>

Daarna blijven we eenvoudige elementen toevoegen voor de deur, de ramen en de trap. De uiteindelijke code voor de afbeelding ziet er als volgt uit:

```html
<svg class="huis" width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .huis {
      stroke: black;
      stroke-width: 2px;
      fill: white;
    } 
    .huis .dak {
      fill: none;
      stroke: #d1495b;
      stroke-width: 10px;
      stroke-linecap: round;
    }
    .huis .deur {
      fill: #d1495b;
    }
    .huis .trap {
      fill: gray;
    }
    .huis .venster {
      fill: #fdea96;
    }
    .huis .vensterbank {
      fill: #d1495b;
      stroke-linecap: round;
    }
    .huis .achtergrond {
      stroke: none;
      fill: #F5F1EB;
    }
  </style>
  <polygon class="gevel" points="-65,80 -65,-10 0,-70 65,-10 65,80" />
  <polyline class="dak" points="-75,-8 0,-78 75,-8" />
  <rect class="deur" x="-45" y="10" width="30" height="60" rx="2" />
  <circle class="deurknop" cx="-35" cy="40" r="2" />
  <rect class="trap" x="-47" y="70" width="34" height="5" />
  <rect class="trap" x="-49" y="75" width="38" height="5" />
  <rect class="venster" x="5" y="15" width="40" height="35" rx="5" />
  <line x1="5" y1="32.5" x2="45" y2="32.5" />
  <line x1="25" y1="15" x2="25" y2="50" />
  <rect class="vensterbank" x="2" y="48" width="46" height="5" rx="5" />
  <circle class="venster" cx="0" cy="-25" r="15" />
  <line x1="-15" y1="-25" x2="15" y2="-25" />
  <line x1="0" y1="-40" x2="0" y2="-10" />
</svg>
```
<figure>
<svg class="huis" width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .huis {
      stroke: black;
      stroke-width: 2px;
      fill: white;
    } 
    .huis .dak {
      fill: none;
      stroke: #d1495b;
      stroke-width: 10px;
      stroke-linecap: round;
    }
    .huis .deur {
      fill: #d1495b;
    }
    .huis .trap {
      fill: gray;
    }
    .huis .venster {
      fill: #fdea96;
    }
    .huis .vensterbank {
      fill: #d1495b;
      stroke-linecap: round;
    }
    .huis .achtergrond {
      stroke: none;
      fill: #F5F1EB;
    }
  </style>
  <rect class="achtergrond" x="-100" y="-100" width="200" height="200" />
  <polygon class="gevel" points="-65,80 -65,-10 0,-70 65,-10 65,80" />
  <polyline class="dak" points="-75,-8 0,-78 75,-8" />
  <rect class="deur" x="-45" y="10" width="30" height="60" rx="2" />
  <circle class="deurknop" cx="-35" cy="40" r="2" />
  <rect class="trap" x="-47" y="70" width="34" height="5" />
  <rect class="trap" x="-49" y="75" width="38" height="5" />
  <rect class="venster" x="5" y="15" width="40" height="35" rx="5" />
  <line x1="5" y1="32.5" x2="45" y2="32.5" />
  <line x1="25" y1="15" x2="25" y2="50" />
  <rect class="vensterbank" x="2" y="48" width="46" height="5" rx="5" />
  <circle class="venster" cx="0" cy="-25" r="15" />
  <line x1="-15" y1="-25" x2="15" y2="-25" />
  <line x1="0" y1="-40" x2="0" y2="-10" />
</svg>
</figure>
