Now that you have mastered the basic shapes, it is time to make your own drawing. Find a drawing that can be composed of basic shapes. Below we give a few possibilities.

### Flags

Most countries have flags consisting of rectangles, triangles, lines and circles. Below you can see some possibilities in advance. Do you know which countries those flags belong to? Find some flags of your own that you can draw.

<figure>
<svg id="flags" xmlns="http://www.w3.org/2000/svg" version="1.1" width="550px" height="400px" viewBox="0 0 1100 800">

  <rect x="0" y="0" width="1100" height="800" fill="#F5F1EB" />

  <g id="belgium" transform="translate(50,50)" >
    <rect x="0" y="0" width="100" height="200" fill="black" />
    <rect x="100" y="0" width="100" height="200" fill="#fedd02" />
    <rect x="200" y="0" width="100" height="200" fill="#ee1b2a" />
  </g>

  <g id="netherlands" transform="translate(400,50)" >
    <rect x="0" y="0" width="300" height="200" fill="white" />
    <rect x="0" y="0" width="300" height="66.66" fill="#a21d22" />
    <rect x="0" y="133.333" width="300" height="66.66" fill="#263e86" />
  </g>

  <g id="norway" transform="translate(750,50)" >
    <rect x="0" y="0" width="300" height="200" fill="#fe0000" />
    <line x1="0" y1="100" x2="300" y2="100" stroke="white" stroke-width="40"/>
    <line x1="100" y1="0" x2="100" y2="200" stroke="white" stroke-width="40"/>
    <line x1="0" y1="100" x2="300" y2="100" stroke="#042568" stroke-width="20"/>
    <line x1="100" y1="0" x2="100" y2="200" stroke="#042568" stroke-width="20"/>
  </g>

  <g id="greece" transform="translate(50,300)" >
    <rect x="0" y="0" width="300" height="200" fill="#3b50a9" />
    <line x1="150" y1="0" x2="150" y2="200" stroke="white" stroke-width="300" stroke-dasharray="22.222 22.222" stroke-dashoffset="22.22" />
    <rect x="0" y="0" width="111.111" height="111.111" fill="#3b50a9" />
    <line x1="0" y1="55.555" x2="111.111" y2="55.555" stroke="white" stroke-width="22.222" />
    <line x1="55.555" y1="0" x2="55.555" y2="112.111" stroke="white" stroke-width="22.222" />
  </g>

  <g id="switzerland" transform="translate(400,300)" >
    <rect x="0" y="0" width="300" height="200" fill="#d82b25" />
    <line x1="100" y1="100" x2="200" y2="100" stroke="white" stroke-width="40"/>
    <line x1="150" y1="50" x2="150" y2="150" stroke="white" stroke-width="40" />
  </g>

  <g id="czechia" transform="translate(750,300)" >
    <rect x="0" y="0" width="300" height="100" fill="white" />
    <rect x="0" y="100" width="300" height="100" fill="#d7141b" />
    <polygon points="0,0, 125,100, 0,200" stroke="none" fill="#11467f" />
  </g>

  <g id="japan" transform="translate(50,550)" >
    <rect x="0" y="0" width="300" height="200" fill="white" />
    <circle cx="150" cy="100" r="50" fill="#d7141b" stroke="none" />
  </g>

  <g id="xxx" transform="translate(400,550)" >
    <rect x="0" y="0" width="300" height="200" fill="none" stroke="black" stroke-width="0.5" stroke-dasharray="10,10" />
  </g>

  <g id="yyy" transform="translate(750,550)" >
    <rect x="0" y="0" width="300" height="200" fill="none" stroke="black" stroke-width="0.5" stroke-dasharray="10,10" />
  </g>

</svg>
</figure>

### Star

<figure>
<svg width="400px" height="400px" viewBox="-1 -1.1 2 2">
  <rect x="-1" y="-1.1" width="2" height="2" fill="#F5F1EB" />
  <polygon stroke="black" stroke-width="0.05" stroke-linejoin="round" fill="yellow"
    points="0.000,-1.000 -0.229,-0.316 -0.951,-0.309 -0.371,0.121 -0.588,0.809 -0.000,0.390 0.588,0.809 0.371,0.121 0.951,-0.309 0.229,-0.316" />
</svg>
</figure>

The vertices of the star were computed using this Python script.

```python
import math

# set properties of star
point_count = 5
starting_angle = 90
outer_radius = 1.0
inner_radius = 0.39

# compute polygon points
points = [
    (
        (inner_radius if index % 2 else outer_radius) * math.cos(math.radians(angle)),
        -(inner_radius if index % 2 else outer_radius) * math.sin(math.radians(angle))
    )
    for index, angle in enumerate(starting_angle + index * 360 / (2 * point_count) for index in range(2 * point_count))
]

# show polygon points
print(' '.join(f'{point[0]:.3f},{point[1]:.3f}' for point in points))
```

### Kürschák's tile

Mattie drew his own version of Kürschák's tile.

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

