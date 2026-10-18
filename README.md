# AIM//LAB

A local-first, responsive browser aim trainer for controller, mouse and touch input. Built as a static site with no framework, tracking, account or API key.

## Run locally

Open `index.html` in a modern browser, or serve this directory with any static HTTP server. The project can be deployed as a static site to Vercel.

## Current features

- Flick, tracking, switching and reaction/acquisition drills.
- Sensitivity multiplier and controller stick deadzone controls.
- Controller input via the browser Gamepad API, mouse aiming and touch drag aiming.
- Accuracy, acquisition-time, movement-stability proxy and target-rate metrics.
- A heuristic sensitivity candidate based on comparable trial scores.
- Responsive desktop/mobile layout.
- Trial history kept in `sessionStorage` for the current browser tab.

## Honest limitations

- The optimiser is a transparent heuristic, not a trained AI model. It needs repeated comparable trials; it does not infer a game's actual sensitivity automatically.
- The trainer multiplier is an internal scale, not a universal conversion to a game's sensitivity units or cm/360.
- Browser Gamepad API support depends on browser, operating system, controller connection and user interaction. On some mobile browsers, controller support is absent or inconsistent.
- This cannot read or change Fortnite or other game settings, inject input into games, reproduce a game's aim assist, or calibrate game-specific acceleration/FOV.
- The current build is a first playable prototype. Metrics such as stability are rough proxies; tracking drill scoring and controller response need further validation before treating results as authoritative.

## Suggested calibration protocol

1. Use the same device, browser, frame rate, input mode and drill for every comparison.
2. Warm up, then run at least 3 trials at each sensitivity candidate.
3. Alternate candidates instead of testing all slow settings before all fast settings, to reduce fatigue/order effects.
4. Compare accuracy, median acquisition time and consistency together. Don't select a sensitivity from one high score.
5. Confirm the chosen setting in the actual game, because game-specific mechanics can materially change the result.

## Roadmap

- Better controller identification and configurable stick-axis mapping.
- Export/import session data and longer-term local persistence.
- More robust repeated-trial optimisation with confidence intervals.
- Game-specific calibration guides and measured conversion profiles where reliable data exists.
- Automated tests for input handling and score calculations.

## Licence

Personal project. Add a licence before redistributing if you want to define reuse terms.
