Om ons voorbeeld van het bos nog wat te pimpen, kunnen we een sneeuweffect toevoegen met een vergelijkbare animatie. We animeren opnieuw `transform`, maar deze keer verplaatsen we veel meer elementen.

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .vlok {
      animation-duration: inherit;
      animation-name: sneeuwen;
      animation-iteration-count: infinite;
      animation-timing-function: linear;
    }
    @keyframes sneeuwen {
      from { transform: translate(0, -100px); }
      to { transform: translate(0, 100px); }
    }
    .vlok.doorzichtig {
      opacity: 0.7;
    }
    .vlok.traag {
      animation-duration: 5s;
    }
    .vlok.snel {
      animation-duration: 3s;
    }
  </style>
  <defs>
    <g id="tree">
      <polygon points="-10,0 10,0 0,-50" fill="#38755b" />
      <line x2="0" y2="10" stroke="#778074" stroke-width="2" />
    </g>
    <circle id="big" cx="0" cy="0" r="5" fill="white" />
    <circle id="small" cx="0" cy="0" r="3" fill="white" />
  </defs>

  <rect x="-100" y="-100" width="200" height="200" fill="#F1DBC3" />
  <circle cx="0" cy="380" r="350" fill="#F8F4E8" />

  <use href="#tree" x="-30" y="25" transform="scale(2)" />
  <use href="#tree" x="-20" y="40" transform="scale(1.2)" />
  <use href="#tree" x="40" y="40" />
  <use href="#tree" x="50" y="30" transform="scale(1.5)" />

  <use href="#big" x="0" y="0" class="vlok snel" />
  <use href="#big" x="-50" y="-20" class="vlok snel doorzichtig" />
  <use href="#big" x="30" y="-40" class="vlok snel" />
  <use href="#big" x="50" y="-20" class="vlok snel doorzichtig" />
  <use href="#big" x="30" y="50" class="vlok traag" />
  <use href="#big" x="-70" y="-80" class="vlok traag doorzichtig" />
  <use href="#big" x="30" y="50" class="vlok traag" />
  <use href="#big" x="90" y="-80" class="vlok traag doorzichtig" />
  <use href="#small" x="10" y="-50" class="vlok traag" />
  <use href="#small" x="-50" y="-60" class="vlok traag doorzichtig" />
  <use href="#small" x="30" y="70" class="vlok traag" />
  <use href="#small" x="10" y="-80" class="vlok traag doorzichtig" />
</svg>
</figure>

We breiden het voorbeeld van het bos uit met eenvoudige herbruikbare sneeuwvlokken en voegen er een heleboel toe aan de scène met verschillende CSS-klassen om wat variatie in snelheid en uiterlijk in te stellen. Daarna voegen we animatie toe in CSS om te doen alsof het aan het sneeuwen is. Het is een beetje glitchy en niet de meest geavanceerde animatie, maar je snapt het idee.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .vlok {
      animation-duration: inherit;
      animation-name: sneeuwen;
      animation-iteration-count: infinite;
      animation-timing-function: linear;
    }
    @keyframes sneeuwen {
      from { transform: translate(0, -100px); }
      to { transform: translate(0, 100px); }
    }
    .vlok.doorzichtig {
      opacity: 0.7;
    }
    .vlok.traag {
      animation-duration: 5s;
    }
    .vlok.snel {
      animation-duration: 3s;
    }
  </style>
  <defs>
    <g id="tree">
      <polygon points="-10,0 10,0 0,-50" fill="#38755b" />
      <line x2="0" y2="10" stroke="#778074" stroke-width="2" />
    </g>
    <circle id="big" cx="0" cy="0" r="5" fill="white" />
    <circle id="small" cx="0" cy="0" r="3" fill="white" />
  </defs>

  <rect x="-100" y="-100" width="200" height="200" fill="#F1DBC3" />
  <circle cx="0" cy="380" r="350" fill="#F8F4E8" />

  <use href="#tree" x="-30" y="25" transform="scale(2)" />
  <use href="#tree" x="-20" y="40" transform="scale(1.2)" />
  <use href="#tree" x="40" y="40" />
  <use href="#tree" x="50" y="30" transform="scale(1.5)" />

  <use href="#big" x="0" y="0" class="vlok snel" />
  <use href="#big" x="-50" y="-20" class="vlok snel doorzichtig" />
  <use href="#big" x="30" y="-40" class="vlok snel" />
  <use href="#big" x="50" y="-20" class="vlok snel doorzichtig" />
  <use href="#big" x="30" y="50" class="vlok traag" />
  <use href="#big" x="-70" y="-80" class="vlok traag doorzichtig" />
  <use href="#big" x="30" y="50" class="vlok traag" />
  <use href="#big" x="90" y="-80" class="vlok traag doorzichtig" />
  <use href="#small" x="10" y="-50" class="vlok traag" />
  <use href="#small" x="-50" y="-60" class="vlok traag doorzichtig" />
  <use href="#small" x="30" y="70" class="vlok traag" />
  <use href="#small" x="10" y="-80" class="vlok traag doorzichtig" />
</svg>
```
