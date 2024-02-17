Als zelf tekeningen maakt, dan kan handig zijn om het **kijkvenster** zichtbaar te maken, of zelfs om het assenstelsel zichtbaar te maken. We leggen kort uit hoe je dat kan doen voor een kijkvenster met breedte 200 en hoogte 200 waarbij de oorsprong (het punt $$(0,0)$$) in het midden van het kijkvenster ligt. De linkerbovenhoek van het kijkvenster ligt dus in het punt $$(-100, -100)$$.

```html
<svg viewBox="-100 -100 200 200">
    ...
</svg> 
```

We tekenen ook een doorzichtige groene cirkel met middelpunt $$(30, 50)$$ en straal 40. We tekenen een kleine zwarte cirkel om de positie van het middelpunt zichtbaar te maken

```html
<circle cx="30" cy="50" r="40" fill="rgb(0,255,0,0.5)" />
<circle cx="30" cy="50" r="2" fill="black" />
```

### Kijkvenster zichtbaar maken

Het kijkvenster kan je zichtbaar maken door het `style` attribuut van het `svg` element te gebruiken om de rand (`border`) in te stellen op een dunne (`1px`) zwarte (`black`) gestreepte (`dashed`) lijn. We kunnen ook de achtergrondkleur (`background-color`) instellen op de kleur `#F5F1EB`.

```html
<svg width="400px" height="400px" viewBox="-100 -100 200 200" 
  style="border:dashed black 1px; background-color:#F5F1EB;"
>
    <circle cx="30" cy="50" r="40" fill="rgb(0,255,0,0.5)" />
    <circle cx="30" cy="50" r="2" fill="black" />
</svg>
```

<figure>
<svg width="400px" height="400px" viewBox="-100 -100 200 200" 
  style="border:dashed black 1px; background-color:#F5F1EB;"
>
    <circle cx="30" cy="50" r="40" fill="rgb(0,255,0,0.5)" />
    <circle cx="30" cy="50" r="2" fill="black" />
</svg>
</figure>

### Assenstelsel tekenen

Om afbeeldingselementen te plaatsen, is het handig om ook het assenstelsel bij de hand te hebben. Hieronder tekenen we bij de tientallen langs de assen een dunne blauwe lijn (zowel horizontaal als verticaal) en bij de hondertallen tekenen we iets dikkere lijnen. De oorsprong $$(0,0)$$ ligt in het midden van de tekening, waar de twee dikkere lijnen elkaar kruisen.

```html
<svg width="400px" height="400px" viewBox="-100 -100 200 200">

    <style>
      .rooster { 
        display: initial;
      }
      .rooster path {
        fill: none;
        stroke: royalblue;
        stroke-width: 200;
      }
    </style>
      
    <g class="rooster">
      <path d="M-100,0 L200,0" stroke-dasharray="0.2,9.6,0.2,0"></path>
      <path d="M0,-100 L0,200" stroke-dasharray="0.2,9.6,0.2,0"></path>
      <path d="M-100,0 L200,0" stroke-dasharray="1,98,1,0"></path>
      <path d="M0,-100 L0,200" stroke-dasharray="1,98,1,0"></path>
    </g>

    <circle cx="30" cy="50" r="40" fill="rgb(0,255,0,0.5)" />
    <circle cx="30" cy="50" r="2" fill="black" />
  
</svg>
```

<figure>
<svg width="400px" height="400px" viewBox="-100 -100 200 200">

    <style>
      .rooster { 
        display: initial;
      }
      .rooster path {
        fill: none;
        stroke: royalblue;
        stroke-width: 200;
      }
    </style>
      
    <g class="rooster">
      <path d="M-100,0 L200,0" stroke-dasharray="0.2,9.6,0.2,0"></path>
      <path d="M0,-100 L0,200" stroke-dasharray="0.2,9.6,0.2,0"></path>
      <path d="M-100,0 L200,0" stroke-dasharray="1,98,1,0"></path>
      <path d="M0,-100 L0,200" stroke-dasharray="1,98,1,0"></path>
    </g>

    <circle cx="30" cy="50" r="40" fill="rgb(0,255,0,0.5)" />
    <circle cx="30" cy="50" r="2" fill="black" />
  
</svg>
</figure>

Als je bij de weergave-instelling van het rooster `display: initial;` vervangt door `display: none;` dan wordt het rooster verborgen. Op die manier kan je het rooster snel weergeven en verbergen.