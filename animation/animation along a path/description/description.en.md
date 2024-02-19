Another fun use of paths is to create animation paths.

<figure>
<svg id="animation" width="400px" height="200px" viewBox="-200 -100 400 200">
  <style>
    #animation .sleigh {
      offset-path: path(
        "M-220,80 L-90,80 Q60,80,60,-10 A50,50,0,0,0,-60,-10 Q-60,80,90,80 L220,80"
      );
      animation: roller-coaster 6000ms infinite linear;
    }
    
    @keyframes roller-coaster {
      0% { offset-distance: 0%; }
      100% { offset-distance: 100%; }
    }    
  </style>
  <rect x="-200" y="-100" width="400" height="200" fill="#F5F1EB"/>
  <path stroke="#E0CEB9" stroke-width="4" fill="none"
    d="M-200,80 L-80,80 Q80,80,70,-10 A70,70,0,0,0,-70,-10 Q-80,80,80,80 L200,80"
  />
  <g class="sleigh" fill="none">
    <path stroke="#AF6455" stroke-width="5"
      d="M-30,-2 L30,-2 A10,10,0,0,0,30,-22 M-20,-2 L-20,-17 M20,-2 L20,-17"
    />
    <path d="M-27,-17 L27,-17" stroke="#7A504F" stroke-width="6" />
  </g>
</svg>
</figure>

This method is not SVG only. We are using the `offset-path` CSS property here that works for any other HTML element as well. But if you check the value of this attribute, you see that we define a path the same way as we do for an SVG.

To break this down into two parts, first, we have the track. We define this as a single path.

<figure>
<svg id="animation1" width="400px" height="200px" viewBox="-200 -100 400 200">
  <rect x="-200" y="-100" width="400" height="200" fill="#F5F1EB"/>
  <path stroke="#E0CEB9" stroke-width="4" fill="none"
    d="M-200,80 L-80,80 Q80,80,70,-10 A70,70,0,0,0,-70,-10 Q-80,80,80,80 L200,80"
  />
</svg>
</figure>

And then we have a sled, that is made out of two different paths grouped together.

<figure>
<svg id="animation2" width="400px" height="200px" viewBox="-200 -100 400 200">
  <rect x="-200" y="-100" width="400" height="200" fill="#F5F1EB"/>
  <g class="sleigh" fill="none">
    <path stroke="#AF6455" stroke-width="5"
      d="M-30,-2 L30,-2 A10,10,0,0,0,30,-22 M-20,-2 L-20,-17 M20,-2 L20,-17"
    />
    <path d="M-27,-17 L27,-17" stroke="#7A504F" stroke-width="6" />
  </g>
</svg>
</figure>

Neither of these are very interesting on their own. What is new, is that we can add an animation where the animation path is essentially the same as the path of the track. The animation path is only slightly different to make the sledge fit the path even better. By default, the bottom-middle part of the sled would move along the path and the beginning and end of it would slightly sink into the path. Instead of that alter the path to raise the sled slightly at some tight turns.

```html
<svg width="400px" height="200px" viewBox="-200 -100 400 200">
  <style>
    .sleigh {
      offset-path: path(
        "M-220,80 L-90,80 Q60,80,60,-10 A50,50,0,0,0,-60,-10 Q-60,80,90,80 L220,80"
      );
      animation: roller-coaster 6000ms infinite linear;
    }
    
    @keyframes roller-coaster {
      0% { offset-distance: 0%; }
      100% { offset-distance: 100%; }
    }    
  </style>
  <rect x="-200" y="-100" width="400" height="200" fill="#F5F1EB"/>
  <path stroke="#E0CEB9" stroke-width="4" fill="none"
    d="M-200,80 L-80,80 Q80,80,70,-10 A70,70,0,0,0,-70,-10 Q-80,80,80,80 L200,80"
  />
  <g class="sleigh" fill="none">
    <path stroke="#AF6455" stroke-width="5"
      d="M-30,-2 L30,-2 A10,10,0,0,0,30,-22 M-20,-2 L-20,-17 M20,-2 L20,-17"
    />
    <path d="M-27,-17 L27,-17" stroke="#7A504F" stroke-width="6" />
  </g>
</svg>
```

<figure>
<svg id="animation3" width="400px" height="200px" viewBox="-200 -100 400 200">
  <style>
    #animation3 .sleigh {
      offset-path: path(
        "M-220,80 L-90,80 Q60,80,60,-10 A50,50,0,0,0,-60,-10 Q-60,80,90,80 L220,80"
      );
      animation: roller-coaster 6000ms infinite linear;
    }
    
    @keyframes roller-coaster {
      0% { offset-distance: 0%; }
      100% { offset-distance: 100%; }
    }    
  </style>
  <rect x="-200" y="-100" width="400" height="200" fill="#F5F1EB"/>
  <path stroke="#E0CEB9" stroke-width="4" fill="none"
    d="M-200,80 L-80,80 Q80,80,70,-10 A70,70,0,0,0,-70,-10 Q-80,80,80,80 L200,80"
  />
  <g class="sleigh" fill="none">
    <path stroke="#AF6455" stroke-width="5"
      d="M-30,-2 L30,-2 A10,10,0,0,0,30,-22 M-20,-2 L-20,-17 M20,-2 L20,-17"
    />
    <path d="M-27,-17 L27,-17" stroke="#7A504F" stroke-width="6" />
  </g>
</svg>
</figure>
