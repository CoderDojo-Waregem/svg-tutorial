We can also set more traditional animations with CSS. Here we animate the `transform` property with keyframes. We can even trigger this effect on mouse hover.

<figure>
<svg class="bell" width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .bell:hover {
      transform-origin: center 30%;
    }
    
    .bell:hover,
    .bell:hover .bell-tongue {
      animation-duration: 0.5s;
      animation-delay: -0.25s;
      animation-iteration-count: infinite;
      animation-direction: alternate;
      animation-timing-function: ease-in-out;
      animation-name: ring;
    }
    
    @keyframes ring {
      from { transform: rotate(-20deg); }
      to { transform: rotate(20deg); }
    }
  </style>
  
  <g stroke="#001514" stroke-width="2">
    <circle cx="0" cy="-45" r="7" fill="#4F6D7A" />
    <circle class="bell-tongue" cx="0" cy="50" r="10" fill="#F79257" />
    <path fill="#FDEA96"
      d="M-50,40 L-50,50 L50,50 L50,40 Q40,40,40,10
        C40,-60,-40,-60,-40,10 Q-40,40,-50,40"
    />
  </g>
</svg>
</figure>

Here we are reusing the bell example we went through earlier. We add a keyframe animation on hover on both the whole bell itself and the bell tongue.

```html
<svg class="bell" width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .bell:hover {
      transform-origin: center 30%;
    }
    
    .bell:hover,
    .bell:hover .bell-tongue {
      animation-duration: 0.5s;
      animation-delay: -0.25s;
      animation-iteration-count: infinite;
      animation-direction: alternate;
      animation-timing-function: ease-in-out;
      animation-name: ring;
    }
    
    @keyframes ring {
      from { transform: rotate(-20deg); }
      to { transform: rotate(20deg); }
    }
  </style>
  
  <g stroke="#001514" stroke-width="2">
    <circle cx="0" cy="-45" r="7" fill="#4F6D7A" />
    <circle class="bell-tongue" cx="0" cy="50" r="10" fill="#F79257" />
    <path fill="#FDEA96"
      d="M-50,40 L-50,50 L50,50 L50,40 Q40,40,40,10
        C40,-60,-40,-60,-40,10 Q-40,40,-50,40"
    />
  </g>
</svg>
```

<figure>
<svg class="bell1" width="200px" height="200px" viewBox="-100 -100 200 200">
  <style>
    .bell1:hover {
      transform-origin: center 30%;
    }
    
    .bell1:hover,
    .bell1:hover .bell-tongue1 {
      animation-duration: 0.5s;
      animation-delay: -0.25s;
      animation-iteration-count: infinite;
      animation-direction: alternate;
      animation-timing-function: ease-in-out;
      animation-name: ring1;
    }
    
    @keyframes ring1 {
      from { transform: rotate(-20deg); }
      to { transform: rotate(20deg); }
    }
  </style>
  
  <g stroke="#001514" stroke-width="2">
    <circle cx="0" cy="-45" r="7" fill="#4F6D7A" />
    <circle class="bell-tongue1" cx="0" cy="50" r="10" fill="#F79257" />
    <path fill="#FDEA96"
      d="M-50,40 L-50,50 L50,50 L50,40 Q40,40,40,10
        C40,-60,-40,-60,-40,10 Q-40,40,-50,40"
    />
  </g>
</svg>
</figure>
