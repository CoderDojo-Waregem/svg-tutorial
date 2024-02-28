De Hongaarse wiskundige József Kürschák gaf dit "bewijs zonder woorden" dat een regelmatige twaalfhoek die ingeschreven is in een eenheidscirkel oppervlakte 3 heeft.

<div class="dodona-centered-group">
<figure>
<svg xmlns="http://www.w3.org/2000/svg" width="400px" height="400px" viewBox="-1 -1 2 2">
<rect x="-1" y="-1" width="2" height="2" stroke="black" stroke-width="0.02" fill="#b6ddc7" />
<line x1="1.000" y1="-1.000" x2="0.866" y2="-0.500" stroke="black" stroke-width="0.01" />
<line x1="1.000" y1="-1.000" x2="0.500" y2="-0.866" stroke="black" stroke-width="0.01" />
<line x1="-1.000" y1="-1.000" x2="-0.500" y2="-0.866" stroke="black" stroke-width="0.01" />
<line x1="-1.000" y1="-1.000" x2="-0.866" y2="-0.500" stroke="black" stroke-width="0.01" />
<line x1="-1.000" y1="1.000" x2="-0.866" y2="0.500" stroke="black" stroke-width="0.01" />
<line x1="-1.000" y1="1.000" x2="-0.500" y2="0.866" stroke="black" stroke-width="0.01" />
<line x1="1.000" y1="1.000" x2="0.500" y2="0.866" stroke="black" stroke-width="0.01" />
<line x1="1.000" y1="1.000" x2="0.866" y2="0.500" stroke="black" stroke-width="0.01" />
<polygon points="0.000,-1.000 -0.500,-0.866 -0.866,-0.500 -1.000,-0.000 -0.866,0.500 -0.500,0.866 -0.000,1.000 0.500,0.866 0.866,0.500 1.000,0.000 0.866,-0.500 0.500,-0.866" stroke="black" stroke-width="0.01" fill="#fce9ea" />
<polygon points="0,0 0.129,-0.483 0.000,-1.000 -0.129,-0.483" stroke="black" stroke-width="0.01" fill="#ef9ba0" />
<polygon points="0,0 -0.129,-0.483 -0.500,-0.866 -0.354,-0.354" stroke="black" stroke-width="0.01" fill="#ef9ba0" />
<polygon points="0,0 -0.354,-0.354 -0.866,-0.500 -0.483,-0.129" stroke="black" stroke-width="0.01" fill="#ef9ba0" />
<polygon points="0,0 -0.483,-0.129 -1.000,-0.000 -0.483,0.129" stroke="black" stroke-width="0.01" fill="#ef9ba0" />
<polygon points="0,0 -0.483,0.129 -0.866,0.500 -0.354,0.354" stroke="black" stroke-width="0.01" fill="#ef9ba0" />
<polygon points="0,0 -0.354,0.354 -0.500,0.866 -0.129,0.483" stroke="black" stroke-width="0.01" fill="#ef9ba0" />
<polygon points="0,0 -0.129,0.483 -0.000,1.000 0.129,0.483" stroke="black" stroke-width="0.01" fill="#ef9ba0" />
<polygon points="0,0 0.129,0.483 0.500,0.866 0.354,0.354" stroke="black" stroke-width="0.01" fill="#ef9ba0" />
<polygon points="0,0 0.354,0.354 0.866,0.500 0.483,0.129" stroke="black" stroke-width="0.01" fill="#ef9ba0" />
<polygon points="0,0 0.483,0.129 1.000,0.000 0.483,-0.129" stroke="black" stroke-width="0.01" fill="#ef9ba0" />
<polygon points="0,0 0.483,-0.129 0.866,-0.500 0.354,-0.354" stroke="black" stroke-width="0.01" fill="#ef9ba0" />
<polygon points="0,0 0.354,-0.354 0.500,-0.866 0.129,-0.483" stroke="black" stroke-width="0.01" fill="#ef9ba0" />
</svg>
</figure>
</div>

Als de cirkel ingeschreven is in een vierkant, dan kan de resulterende figuur betegeld worden door driehoeken van twee families — 16 gelijkzijdige driehoeken waarvan de zijden gelijk zijn aan die van de twaalfhoek en 32 gelijkbenige driehoeken met hoeken 15°-15°-150° en langste zijde 1. De oppervlakte van het grote vierkant is 4 en de driehoeken waaruit de twaalfhoek bestaat kunnen herschikt worden zodat 3 van de kwadranten gevuld worden (zie de video hieronder). De oppervlakte van de twaalfhoek is dus 3/4 van 4, ofwel 3.

<div class="dodona-centered-group">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/7lCJDdD_fHs?si=Nt6_AeQfQ__feRZn" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>

Om te zien dat het vierkant en de twaalfhoek kunnen worden betegeld zoals we hierboven beweerden, zie [Alexander Bogomolny’s discussie](https://www.cut-the-knot.org/Curriculum/Geometry/KurschakTile.shtml){: target="_blank"}.

### Opgave

De bovenstaande figuur is opgebouwd uit lijnen, rechthoeken en veelhoeken. Inmiddels beheers je al deze vormen. De vraag is dus of je de figuur kunt reproduceren?

Je kennis van driehoeksmeetkunde zal hier goed van pas komen. Maar het is al een stuk moeilijker om die met de hand te genereren. Hier is een voorbeeld van een klein Python-script dat je kunt gebruiken om de SVG-afbeelding te genereren.

```python
import math

def point(radius, angle):

    angle = math.radians(angle)
    x = radius * math.cos(angle)
    y = -radius * math.sin(angle)
    return f'{x:.3f},{y:.3f}'

# header line
svg = '<svg xmlns="http://www.w3.org/2000/svg" width="400px" height="400px" viewBox="-1 -1 2 2">\n'

# background square
svg += '<rect x="-1" y="-1" width="2" height="2" stroke="black" stroke-width="0.02" fill="#b6ddc7" />\n'

# lines from corner points to dodecagon
radius1 = 2 ** 0.5
radius2 = 1.0
for index in range(4):
    x1, y1 = point(radius1, 45 + index * 90).split(',')
    x2, y2 = point(radius2, 45 + index * 90 - 360 / 24).split(',')
    svg += f'<line x1="{x1}" y1="{y1}" x2="{x2}" y2="{y2}" stroke="black" stroke-width="0.01" />\n'
    x2, y2 = point(radius2, 45 + index * 90 + 360 / 24).split(',')
    svg += f'<line x1="{x1}" y1="{y1}" x2="{x2}" y2="{y2}" stroke="black" stroke-width="0.01" />\n'

# dodecagon
radius1 = 1.0
points = ' '.join(point(radius1, 90 + index * 360 / 12) for index in range(12))
svg += f'<polygon points="{points}" stroke="black" stroke-width="0.01" fill="#fce9ea" />\n'

# inner star
radius1 = 1.0
radius2 = 0.5
for index in range(12):
    points = ' '.join([
        '0,0',
        point(radius2, 90 + index * 360 / 12 - 360 / 24),
        point(radius1, 90 + index * 360 / 12),
        point(radius2, 90 + index * 360 / 12 + 360 / 24),
    ])
    svg += f'<polygon points="{points}" stroke="black" stroke-width="0.01" fill="#ef9ba0" />\n'

# footer
svg += '</svg>\n'

# generate output
print(svg)
```

Dit is de uitvoer die het script genereert:

```html
<svg xmlns="http://www.w3.org/2000/svg" width="400px" height="400px" viewBox="-1 -1 2 2">
<rect x="-1" y="-1" width="2" height="2" stroke="black" stroke-width="0.02" fill="#b6ddc7" />
<line x1="1.000" y1="-1.000" x2="0.866" y2="-0.500" stroke="black" stroke-width="0.01" />
<line x1="1.000" y1="-1.000" x2="0.500" y2="-0.866" stroke="black" stroke-width="0.01" />
<line x1="-1.000" y1="-1.000" x2="-0.500" y2="-0.866" stroke="black" stroke-width="0.01" />
<line x1="-1.000" y1="-1.000" x2="-0.866" y2="-0.500" stroke="black" stroke-width="0.01" />
<line x1="-1.000" y1="1.000" x2="-0.866" y2="0.500" stroke="black" stroke-width="0.01" />
<line x1="-1.000" y1="1.000" x2="-0.500" y2="0.866" stroke="black" stroke-width="0.01" />
<line x1="1.000" y1="1.000" x2="0.500" y2="0.866" stroke="black" stroke-width="0.01" />
<line x1="1.000" y1="1.000" x2="0.866" y2="0.500" stroke="black" stroke-width="0.01" />
<polygon points="0.000,-1.000 -0.500,-0.866 -0.866,-0.500 -1.000,-0.000 -0.866,0.500 -0.500,0.866 -0.000,1.000 0.500,0.866 0.866,0.500 1.000,0.000 0.866,-0.500 0.500,-0.866" stroke="black" stroke-width="0.01" fill="#fce9ea" />
<polygon points="0,0 0.129,-0.483 0.000,-1.000 -0.129,-0.483" stroke="black" stroke-width="0.01" fill="#ef9ba0" />
<polygon points="0,0 -0.129,-0.483 -0.500,-0.866 -0.354,-0.354" stroke="black" stroke-width="0.01" fill="#ef9ba0" />
<polygon points="0,0 -0.354,-0.354 -0.866,-0.500 -0.483,-0.129" stroke="black" stroke-width="0.01" fill="#ef9ba0" />
<polygon points="0,0 -0.483,-0.129 -1.000,-0.000 -0.483,0.129" stroke="black" stroke-width="0.01" fill="#ef9ba0" />
<polygon points="0,0 -0.483,0.129 -0.866,0.500 -0.354,0.354" stroke="black" stroke-width="0.01" fill="#ef9ba0" />
<polygon points="0,0 -0.354,0.354 -0.500,0.866 -0.129,0.483" stroke="black" stroke-width="0.01" fill="#ef9ba0" />
<polygon points="0,0 -0.129,0.483 -0.000,1.000 0.129,0.483" stroke="black" stroke-width="0.01" fill="#ef9ba0" />
<polygon points="0,0 0.129,0.483 0.500,0.866 0.354,0.354" stroke="black" stroke-width="0.01" fill="#ef9ba0" />
<polygon points="0,0 0.354,0.354 0.866,0.500 0.483,0.129" stroke="black" stroke-width="0.01" fill="#ef9ba0" />
<polygon points="0,0 0.483,0.129 1.000,0.000 0.483,-0.129" stroke="black" stroke-width="0.01" fill="#ef9ba0" />
<polygon points="0,0 0.483,-0.129 0.866,-0.500 0.354,-0.354" stroke="black" stroke-width="0.01" fill="#ef9ba0" />
<polygon points="0,0 0.354,-0.354 0.500,-0.866 0.129,-0.483" stroke="black" stroke-width="0.01" fill="#ef9ba0" />
</svg>
```

### Bronnen

**Alexanderson GL, Seydel K (1978)**. [Kürschak’s Tile](https://www.jstor.org/stable/3616688){: target="_blank"}, *Mathematical Gazette* **62(421)**, 192-196.