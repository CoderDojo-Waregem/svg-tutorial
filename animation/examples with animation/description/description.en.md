Use animation to make your image come alive. Here are a few examples.

### USS Enterprise

<figure>
<svg class="space" width="400px" height="800px" viewBox="-200 -400 400 800">
    <defs>
        <path id="text-arc" d="M-60,-200 A60,60,0,0,1,60,-200" />
        <rect id="big" x="30" y="-100" width="4" height="60" />
        <rect id="medium" x="30" y="-100" width="2" height="30" />
        <rect id="small" x="30" y="-100" width="1" height="10" />
    </defs>
    <!--classes-->
    <style>
        .space {
            background: black;
        }

        .star {
            animation-duration: inherit;
            animation-name: warpspeed;
            animation-iteration-count: infinite;
            animation-timing-function: linear;
        }

        @keyframes warpspeed {
            from {
                transform: translate(0, -200px);
            }

            to {
                transform: translate(0, 400px);
            }
        }

        .star.slow {
            animation-duration: 5s;
            fill: lightyellow;
            stroke-width: 1;
            rx: 5;
        }

        .star.medium {
            animation-duration: 1500ms;
            fill: white;
            stroke-width: 1;
            rx: 5;
        }

        .star.fast {
            animation-duration: 500ms;
            fill: lightblue;
            stroke-width: 2;
            rx: 5;
        }

        .hull {
            fill: lightgrey;
            stroke: darkgrey;
            stroke-width: 2;
        }

        .landingbay {
            fill: #625f5f;
        }

        .sign {
            fill: black;
            font-family: Tahoma;
            font-size: 11;
            font-weight: bold;
            stroke: orange;
            stroke-width: 0.5;
            text-anchor: middle;
            dominant-baseline: central;
        }

        .base {
            fill: darkgray;
        }

        .engine {
            fill: lightgrey;
            stroke: darkgrey;
            stroke-width: 2;
            rx: 5;
        }

        .intake {
            fill: blue;
            stroke: darkblue;
        }

        .exhaust {
            fill: orange;
            stroke: darkorange;
        }

        .line {
            fill: #ffb300;
            rx: 50;
            opacity: 40%;
        }
    </style>
    <!-- stars in back -->
    <use href="#big" x="0" y="0" class="star fast" />
    <use href="#big" x="-150" y="-50" class="star fast" />
    <use href="#big" x="30" y="-100" class="star fast" />
    <use href="#big" x="150" y="250" class="star fast" />
    <use href="#medium" x="30" y="-30" class="star medium" />
    <use href="#medium" x="-120" y="-80" class="star medium" />
    <use href="#medium" x="30" y="50" class="star medium" />
    <use href="#medium" x="90" y="-80" class="star medium" />
    <use href="#small" x="10" y="-200" class="star slow" />
    <use href="#small" x="-50" y="-60" class="star slow" />
    <use href="#small" x="30" y="70" class="star slow" />
    <use href="#small" x="10" y="-80" class="star slow" />
    <use href="#small" x="100" y="-50" class="star slow" />
    <use href="#small" x="-50" y="-150" class="star slow" />
    <use href="#small" x="50" y="150" class="star slow" />
    <use href="#small" x="10" y="2000" class="star slow" />

    <!--base-->
    <path d="M-10,-140 L10,-140 L0,-60 L-10,-140" fill="darkgray" stroke="darkgray" stroke-width="30"
        stroke-linecap="round" stroke-linejoin="round" />
    <path d="M-30,-80 L-10,-110 L-10,-95 L-30,-50 L-30,-80 " class="hull" stroke-width="5" stroke-linecap="round"
        stroke-linejoin="round" />
    <path d="M30,-80 L10,-110 L10,-95 L30,-50 L30,-80 " class="hull" stroke-linecap="round" stroke-linejoin="round" />
    <!--schotel-->
    <circle cx="0" cy="-200" r="70" class="hull" />
    <circle cx="0" cy="-200" r="30" class="hull" />
    <polygon points="0,-170 10,-130 -10,-130" class="landingbay" />
    <text class="sign">
        <textPath href="#text-arc" startOffset="50%">
            NCC-1701-A
        </textPath>
    </text>
    <!--motoren-->
    <circle cx="-40" cy="-100" r="10" class="engine intake" />
    <circle cx="-40" cy="-30" r="10" class="engine exhaust" />
    <rect x="-50" y="-100" width="20" height="70" class="engine" />
    <circle cx="40" cy="-100" r="10" class="engine intake" />
    <circle cx="40" cy="-30" r="10" class="engine exhaust" />
    <rect x="30" y="-100" width="20" height="70" class="engine" />

    <!-- lines -->
    <rect x="-50" y="00" width="20" height="4000" class="line" />
    <rect x="30" y="00" width="20" height="4000" class="line" />

    <!-- stars in front -->
    <use href="#big" x="0" y="0" class="star fast" />
    <use href="#big" x="-150" y="-50" class="star fast" />
</svg>
</figure>
