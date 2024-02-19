Drawing shapes is not the only use case for paths. We can also use them to render text along an invisible path. We can define a path in the definitions section and use it in a `textPath` element to make the text go around the circle. Here we use arc again, but you can use any other path and the text will follow the stroke.

```html
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
    <path id="text-arc" d="M0,50 A50,50,0,1,1,1,50" />
  </defs>

  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <text fill="#0c5c4c" font-family="Tahoma" font-size="11" font-weight="bold">
    <textPath href="#text-arc">
      CoderDojo is cool! CoderDojo is cool! CoderDojo is cool!
    </textPath>
  </text>
</svg>
```

<figure>
<svg width="200px" height="200px" viewBox="-100 -100 200 200">
  <defs>
    <path id="text-arc" d="M0,50 A50,50,0,1,1,1,50" />
  </defs>

  <rect x="-100" y="-100" width="200" height="200" fill="#F5F1EB"/>
  <text fill="#0c5c4c" font-family="Tahoma" font-size="11" font-weight="bold">
    <textPath href="#text-arc">
      CoderDojo is cool! CoderDojo is cool! CoderDojo is cool!
    </textPath>
  </text>
</svg>
</figure>
