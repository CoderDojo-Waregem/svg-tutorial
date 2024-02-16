Instead of repeating the same code over and over again we can also create a definition for a shape and reuse it. Here we define a branch of a snowflake and then use it six times with different rotations.

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <defs>
    <path id="branch1" stroke="#E5C39C" stroke-width="5" d="
      M0,0 L0,-90
      M0,-20 L20,-34
      M0,-20 L-20,-34
      M0,-40 L20,-54
      M0,-40 L-20,-54
      M0,-60 L20-74
      M0,-60 L-20,-74" 
    />
  </defs>
  
  <use href="#branch1" />
  <use href="#branch1" transform="rotate(60)" />
  <use href="#branch1" transform="rotate(120)" />
  <use href="#branch1" transform="rotate(180)" />
  <use href="#branch1" transform="rotate(240)" />
  <use href="#branch1" transform="rotate(300)" />
</svg>
</figure>

### Drawing a branch of the snowflake

The branch is defined as a `path`. Earlier we already covered how to draw basic paths. Here we draw the branch in a similar way. We can draw a simple line – the main branch – by using the move to (`M`) and line to (`L`) commands:

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path stroke="#E5C39C" stroke-width="5" d="M0,0 L0,-90" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path stroke="#E5C39C" stroke-width="5" d="M0,0 L0,-90" />
</svg>
</figure>

Then we can continue drawing, and add a side branch by adding another move to and line to commands:

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path stroke="#E5C39C" stroke-width="5" d="M0,0 L0,-90 M0,-20 L20,-34" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path stroke="#E5C39C" stroke-width="5" d="M0,0 L0,-90 M0,-20 L20,-34" />
</svg>
</figure>

The finished branch would look like this:

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <path id="branch" stroke="#E5C39C" stroke-width="5" d="
    M0,0 L0,-90
    M0,-20 L20,-34
    M0,-20 L-20,-34
    M0,-40 L20,-54
    M0,-40 L-20,-54
    M0,-60 L20-74
    M0,-60 L-20,-74" 
  />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <path id="branch" stroke="#E5C39C" stroke-width="5" d="
    M0,0 L0,-90
    M0,-20 L20,-34
    M0,-20 L-20,-34
    M0,-40 L20,-54
    M0,-40 L-20,-54
    M0,-60 L20-74
    M0,-60 L-20,-74" 
  />
</svg>
</figure>

### Reusing image elements

Then we can move the entire branch path into the `defs` section. The `defs` section is a hidden compartment of our image. Things here don’t show up on the screen, but we can refer to them and use them later.

Once we defined a branch, we can reuse it multiple times with the `use` command the following way.

Then we can move the individual branches to their correct position with the `transform` command in the same way as we did with the star example.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
    <path id="branch" stroke="#E5C39C" stroke-width="5" d="
      M0,0 L0,-90
      M0,-20 L20,-34
      M0,-20 L-20,-34
      M0,-40 L20,-54
      M0,-40 L-20,-54
      M0,-60 L20-74
      M0,-60 L-20,-74" 
    />
  </defs>
  
  <use href="#branch" />
  <use href="#branch" transform="rotate(60)" />
  <use href="#branch" transform="rotate(120)" />
  <use href="#branch" transform="rotate(180)" />
  <use href="#branch" transform="rotate(240)" />
  <use href="#branch" transform="rotate(300)" />
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <defs>
    <path id="branch" stroke="#E5C39C" stroke-width="5" d="
      M0,0 L0,-90
      M0,-20 L20,-34
      M0,-20 L-20,-34
      M0,-40 L20,-54
      M0,-40 L-20,-54
      M0,-60 L20-74
      M0,-60 L-20,-74" 
    />
  </defs>
  
  <use href="#branch" />
  <use href="#branch" transform="rotate(60)" />
  <use href="#branch" transform="rotate(120)" />
  <use href="#branch" transform="rotate(180)" />
  <use href="#branch" transform="rotate(240)" />
  <use href="#branch" transform="rotate(300)" />
</svg>
</figure>
