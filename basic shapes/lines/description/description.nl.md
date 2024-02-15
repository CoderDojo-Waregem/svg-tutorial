## Moving styling properties to CSS

We can assign CSS classes to each element and move some attributes to CSS. We can only move the presentation attributes though. Position attributes and attributes that define the shapes have to stay in the SVG-tags. But colors, stroke, and font attributes can be moved to CSS.

```html
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .head {
      fill: #cd803d;
    }
  </style>
  <circle class="head" cx="0" cy="-50" r="30" />
</svg>
```

<figure>
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .head1 {
      fill: #cd803d;
    }
  </style>
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle class="head1" cx="0" cy="-50" r="30" />
</svg>
</figure>

## Rounded lines

We already saw the `fill` and some `stroke` properties, but here’s another styling property. The `stroke-linecap`. This can make our line cap rounded. Note that the legs and the arms are simple lines here.

To give you a comparison if we remove the line cap and set a smaller `stroke-width`, then this is how it would look like.

```html
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .limb {
      stroke: #cd803d;
    }
  </style>
  <line class="limb" x1="-40" y1="-10" x2="40" y2="-10" />
  <line class="limb" x1="-25" y1="50" x2="0" y2="-15" />
  <line class="limb" x1="25" y1="50" x2="0" y2="-15" />
</svg>
```

<figure>
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .limb2 {
      stroke: #cd803d;
    }
  </style>
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <line class="limb2" x1="-40" y1="-10" x2="40" y2="-10" />
  <line class="limb2" x1="-25" y1="50" x2="0" y2="-15" />
  <line class="limb2" x1="25" y1="50" x2="0" y2="-15" />
</svg>
</figure>

But by setting a thick stroke width and a round line cap we can shape legs and arms for our figure.

```html
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .limb {
      stroke: #cd803d;
      stroke-width: 35px;
      stroke-linecap: round;
    }
  </style>
  <line class="limb" x1="-40" y1="-10" x2="40" y2="-10" />
  <line class="limb" x1="-25" y1="50" x2="0" y2="-15" />
  <line class="limb" x1="25" y1="50" x2="0" y2="-15" />
</svg>
```

<figure>
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .limb3 {
      stroke: #cd803d;
      stroke-width: 35px;
      stroke-linecap: round;
    }
  </style>
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <line class="limb3" x1="-40" y1="-10" x2="40" y2="-10" />
  <line class="limb3" x1="-25" y1="50" x2="0" y2="-15" />
  <line class="limb3" x1="25" y1="50" x2="0" y2="-15" />
</svg>
</figure>

## Rounded rectangles

Also, note the `rx` property at the rectangle defining the mouth. This will make the edges rounded. It is similar to the `border-radius` property for regular HTML elements.

```html
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .head {
      fill: #cd803d;
    }
    .mouth {
      fill: none;
      stroke: white;
      stroke-width: 2px;
    }
  </style>
  <circle class="head" cx="0" cy="-50" r="30" />
  <rect class="mouth" x="-10" y="-40" width="20" height="5" rx="2" />
</svg>
```

<figure>
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .head4 {
      fill: #cd803d;
    }
    .mouth4 {
      fill: none;
      stroke: white;
      stroke-width: 2px;
    }
  </style>
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle class="head4" cx="0" cy="-50" r="30" />
  <rect class="mouth4" x="-10" y="-40" width="20" height="5" rx="2" />
</svg>
</figure>

## Gingerbread figure

Once we put it all together, and add eyes and buttons, this is how the final code looks like:

```html
<svg class="gingerbread" width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .head {
      fill: #cd803d;
    }
    .eye {
      fill: white;
    }
    .mouth {
      fill: none;
      stroke: white;
      stroke-width: 2px;
    }
    .limb {
      stroke: #cd803d;
      stroke-width: 35px;
      stroke-linecap: round;
    }
  </style>
  <circle class="head" cx="0" cy="-50" r="30" />
  <circle class="eye" cx="-12" cy="-55" r="3" />
  <circle class="eye" cx="12" cy="-55" r="3" />
  <rect class="mouth" x="-10" y="-40" width="20" height="5" rx="2" />
  <line class="limb" x1="-40" y1="-10" x2="40" y2="-10" />
  <line class="limb" x1="-25" y1="50" x2="0" y2="-15" />
  <line class="limb" x1="25" y1="50" x2="0" y2="-15" />
  <circle class="button" cx="0" cy="-10" r="5" />
  <circle class="button" cx="0" cy="10" r="5" />
</svg>
```

<figure>
<svg width="200" height="200" viewBox="-100 -100 200 200">
  <style>
    .head {
      fill: #cd803d;
    }
    .eye {
      fill: white;
    }
    .mouth {
      fill: none;
      stroke: white;
      stroke-width: 2px;
    }
    .limb {
      stroke: #cd803d;
      stroke-width: 35px;
      stroke-linecap: round;
    }
  </style>
  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <circle class="head" cx="0" cy="-50" r="30" />
  <circle class="eye" cx="-12" cy="-55" r="3" />
  <circle class="eye" cx="12" cy="-55" r="3" />
  <rect class="mouth" x="-10" y="-40" width="20" height="5" rx="2" />
  <line class="limb" x1="-40" y1="-10" x2="40" y2="-10" />
  <line class="limb" x1="-25" y1="50" x2="0" y2="-15" />
  <line class="limb" x1="25" y1="50" x2="0" y2="-15" />
  <circle class="button" cx="0" cy="-10" r="5" />
  <circle class="button" cx="0" cy="10" r="5" />
</svg>
</figure>
