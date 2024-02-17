Nadat we hebben geleerd over kwadratische Bézierkrommen en kubische Bézierkrommen, doen we nog een oefenrondje waarbij we beide soorten krommen gebruiken om dit strikje te tekenen.

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
      <path fill="#B73A3B" id="strikje" d="
        M0,-20 Q28,-40,56,-45 C96,-48,96,48,56,45 Q28,40,0,20" 
      />
  </defs>

  <rect x="-100" y="-200" width="200" height="400" fill="#F5F1EB"/>
  <use href="#strikje" />
  <use href="#strikje" transform="scale(-1)" />
  <ellipse cx="0" cy="0" rx="20" ry="24" fill="#9C2D2A" />
  <path fill="none" stroke="#B73A3B" stroke-width="3" d="
    M0,20 Q40,40,30,60 Q20,80,40,90 
    M0,20 Q-30,30,-20,60 Q-10,90,-50,100"
  />
</svg>
</figure>

We beginnen voor de rechterkant van het strikje met een kwadratische Bézierkromme. De stip stelt opnieuw het controlepunt voor.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path fill="#B73A3B" d="
    M0,-20
    Q28,-40,56,-45"
  />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-200" width="200" height="400" fill="#F5F1EB"/>
  <circle cx="28" cy="-40" r="2"></circle>
  <path fill="#B73A3B" d="
    M0,-20
    Q28,-40,56,-45"
  />
</svg>
</figure>

Daarna gaan we verder met een kubische Bézier.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path fill="#B73A3B" d="
    M0,-20
    Q28,-40,56,-45
    C96,-48,96,48,56,45"
  />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-200" width="200" height="400" fill="#F5F1EB"/>
  <circle cx="96" cy="-48" r="2"></circle>
  <circle cx="96" cy="48" r="2"></circle>
  <path fill="#B73A3B" d="
    M0,-20
    Q28,-40,56,-45
    C96,-48,96,48,56,45"
  />
</svg>
</figure>

En we eindigen met nog een kwadratische kubische Bézierkromme die het spiegelbeeld is van de eerste.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path fill="#B73A3B" d="
    M0,-20
    Q28,-40,56,-45
    C96,-48,96,48,56,45
    Q28,40,0,20"
  />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-200" width="200" height="400" fill="#F5F1EB"/>
  <circle cx="28" cy="40" r="2"></circle>
  <path fill="#B73A3B" d="
    M0,-20
    Q28,-40,56,-45
    C96,-48,96,48,56,45
    Q28,40,0,20"
  />
</svg>
</figure>

Dan kunnen we de volledige vorm verplaatsen naar een herbruikbare component en die voor beide kanten van het strikje gebruiken. Merk op dat we negatieve schaling gebruiken om naar de linkerkant te spiegelen.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
      <path fill="#B73A3B" id="strikje" d="
        M0,-20 Q28,-40,56,-45 C96,-48,96,48,56,45 Q28,40,0,20" 
      />
  </defs>

  <use href="#strikje" />
  <use href="#strikje" transform="scale(-1)" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
      <path fill="#B73A3B" id="strikje" d="
        M0,-20 Q28,-40,56,-45 C96,-48,96,48,56,45 Q28,40,0,20" 
      />
  </defs>

  <rect x="-100" y="-200" width="200" height="400" fill="#F5F1EB"/>
  <use href="#strikje" />
  <use href="#strikje" transform="scale(-1)" />
</svg>
</figure>

We maken de afbeelding af door een `ellipse` element in het midden toe te voegen en een kromme lijn voor het touwtje.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
      <path fill="#B73A3B" id="strikje" d="
        M0,-20 Q28,-40,56,-45 C96,-48,96,48,56,45 Q28,40,0,20" 
      />
  </defs>

  <use href="#strikje" />
  <use href="#strikje" transform="scale(-1)" />
  <ellipse cx="0" cy="0" rx="20" ry="24" fill="#9C2D2A" />
  <path fill="none" stroke="#B73A3B" stroke-width="3" d="
    M0,20 Q40,40,30,60 Q20,80,40,90 
    M0,20 Q-30,30,-20,60 Q-10,90,-50,100"
  />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
      <path fill="#B73A3B" id="strikje1" d="
        M0,-20 Q28,-40,56,-45 C96,-48,96,48,56,45 Q28,40,0,20" 
      />
  </defs>

  <rect x="-100" y="-200" width="200" height="400" fill="#F5F1EB"/>
  <use href="#strikje1" />
  <use href="#strikje1" transform="scale(-1)" />
  <ellipse cx="0" cy="0" rx="20" ry="24" fill="#9C2D2A" />
  <path fill="none" stroke="#B73A3B" stroke-width="3" d="
    M0,20 Q40,40,30,60 Q20,80,40,90 
    M0,20 Q-30,30,-20,60 Q-10,90,-50,100"
  />
</svg>
</figure>
