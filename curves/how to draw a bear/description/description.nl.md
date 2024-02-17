Laten we als ultieme uitdaging een beer tekenen.

<figure>
<svg class="beer" width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .beer {
      background-color: #f5eed7;
    }
    .beer .oor {
      fill: #e5c39c;
      stroke: white;
      stroke-width: 5;
    }    
    .beer .gezicht {
      fill: white;
    }
    .beer .mond {
      fill: none;
      stroke: black;
      stroke-width: 2;
    }
  </style>
  <circle class="oor" cx="-40" cy="-50" r="18" />
  <circle class="oor" cx="40" cy="-50" r="18" />
  <rect class="gezicht" x="-55" y="-60" width="110" height="120" rx="50" ry="30" />
  <circle cx="20" cy="-30" r="3" />
  <circle cx="-20" cy="-30" r="3" />
  <path class="snuit" fill="#E5C39C" d="
    M-30,0 C-30,-25,30,-25,30,0 
    L30,30 Q30,40,20,40 
    L-20,40 Q-30,40,-30,30" 
  />
  <path class="neus" d="M-10,0 L10,0 C10,20,-10,20,-10,0" />
  <path class="mond" d="M0,10 Q0,25,10,25 M0,10 Q0,25,-10,25" />
</svg>
</figure>

We beginnen met de oren. Dit zijn twee cirkels die beide de attributen `fill` en `stroke` hebben. We hebben ook een klasse gedefinieerd op het SVG-element om de achtergrondkleur in te stellen. Merk op dat we hier de gewone CSS-eigenschap  `background-color` instellen en niet het attribuut `fill`. Opvullen werkt met vormen, maar het SVG-element zelf is geen vorm.


```html
<svg class="beer" width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .beer {
      background-color: #f5eed7;
    }
    .beer .oor {
      fill: #e5c39c;
      stroke: white;
      stroke-width: 5;
    }    
  </style>
  <circle class="oor" cx="-40" cy="-50" r="18" />
  <circle class="oor" cx="40" cy="-50" r="18" />
</svg>
```

<figure>
<svg class="beer1" width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .beer1 {
      background-color: #f5eed7;
    }
    .beer1 .oor {
      fill: #e5c39c;
      stroke: white;
      stroke-width: 5;
    }    
  </style>
  <circle class="oor" cx="-40" cy="-50" r="18" />
  <circle class="oor" cx="40" cy="-50" r="18" />
</svg>
</figure>

Laten we dan het gezicht en de ogen toevoegen. Hier is nog iets wat we nog niet eerder hebben behandeld. Eerder zagen we dat we rechthoeken kunnen afronden met de `rx` eigenschap. We kunnen nog specifieker zijn en een andere straal instellen op de $$y$$-as met de `ry` eigenschap. Als de laatste niet is ingesteld, dan wordt hiervoor ook de waarde van de `rx` eigenschap gebruikt.

```html
<svg class="beer" width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .beer {
      background-color: #f5eed7;
    }
    .beer .gezicht {
      fill: white;
    }
  </style>
  <rect class="gezicht" x="-55" y="-60" width="110" height="120" rx="50" ry="30" />
  <circle cx="20" cy="-30" r="3" />
  <circle cx="-20" cy="-30" r="3" />
</svg>
```

<figure>
<svg class="beer2" width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .beer2 {
      background-color: #f5eed7;
    }
    .beer2 .gezicht {
      fill: white;
    }
  </style>
  <rect class="gezicht" x="-55" y="-60" width="110" height="120" rx="50" ry="30" />
  <circle cx="20" cy="-30" r="3" />
  <circle cx="-20" cy="-30" r="3" />
</svg>
</figure>

Ten slotte kunnen we nog een paar paden toevoegen voor de neus en de mond.

```html
<svg class="beer" width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .beer {
      background-color: #f5eed7;
    }
    .beer .mond {
      fill: none;
      stroke: black;
      stroke-width: 2;
    }
  </style>
  <path class="snuit" fill="#E5C39C" d="
    M-30,0 C-30,-25,30,-25,30,0 
    L30,30 Q30,40,20,40 
    L-20,40 Q-30,40,-30,30" 
  />
  <path class="neus" d="M-10,0 L10,0 C10,20,-10,20,-10,0" />
  <path class="mond" d="M0,10 Q0,25,10,25 M0,10 Q0,25,-10,25" />
</svg>
```

<figure>
<svg class="beer3" width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .beer3 {
      background-color: #f5eed7;
    }
    .beer3 .mond {
      fill: none;
      stroke: black;
      stroke-width: 2;
    }
  </style>
  <path class="snuit" fill="#E5C39C" d="
    M-30,0 C-30,-25,30,-25,30,0 
    L30,30 Q30,40,20,40 
    L-20,40 Q-30,40,-30,30" 
  />
  <path class="neus" d="M-10,0 L10,0 C10,20,-10,20,-10,0" />
  <path class="mond" d="M0,10 Q0,25,10,25 M0,10 Q0,25,-10,25" />
</svg>
</figure>

Als we alles samenvoegen, dan krijgen we de tekening van de beer.

```html
<svg class="beer" width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .beer {
      background-color: #f5eed7;
    }
    .beer .oor {
      fill: #e5c39c;
      stroke: white;
      stroke-width: 5;
    }    
    .beer .gezicht {
      fill: white;
    }
    .beer .mond {
      fill: none;
      stroke: black;
      stroke-width: 2;
    }
  </style>
  <circle class="oor" cx="-40" cy="-50" r="18" />
  <circle class="oor" cx="40" cy="-50" r="18" />
  <rect class="gezicht" x="-55" y="-60" width="110" height="120" rx="50" ry="30" />
  <circle cx="20" cy="-30" r="3" />
  <circle cx="-20" cy="-30" r="3" />
  <path class="snuit" fill="#E5C39C" d="
    M-30,0 C-30,-25,30,-25,30,0 
    L30,30 Q30,40,20,40 
    L-20,40 Q-30,40,-30,30" 
  />
  <path class="neus" d="M-10,0 L10,0 C10,20,-10,20,-10,0" />
  <path class="mond" d="M0,10 Q0,25,10,25 M0,10 Q0,25,-10,25" />
</svg>
```

<figure>
<svg class="beer4" width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .beer4 {
      background-color: #f5eed7;
    }
    .beer4 .oor {
      fill: #e5c39c;
      stroke: white;
      stroke-width: 5;
    }    
    .beer4 .gezicht {
      fill: white;
    }
    .beer4 .mond {
      fill: none;
      stroke: black;
      stroke-width: 2;
    }
  </style>
  <circle class="oor" cx="-40" cy="-50" r="18" />
  <circle class="oor" cx="40" cy="-50" r="18" />
  <rect class="gezicht" x="-55" y="-60" width="110" height="120" rx="50" ry="30" />
  <circle cx="20" cy="-30" r="3" />
  <circle cx="-20" cy="-30" r="3" />
  <path class="snuit" fill="#E5C39C" d="
    M-30,0 C-30,-25,30,-25,30,0 
    L30,30 Q30,40,20,40 
    L-20,40 Q-30,40,-30,30" 
  />
  <path class="neus" d="M-10,0 L10,0 C10,20,-10,20,-10,0" />
  <path class="mond" d="M0,10 Q0,25,10,25 M0,10 Q0,25,-10,25" />
</svg>
</figure>
