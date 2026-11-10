# derby

browser game that simulates a horse racing day, built with Vue 3 and Vuex
as a take-home assignment.

live at [danylo-morhun.github.io/derby](https://danylo-morhun.github.io/derby/).

## how it plays

the game creates 20 horses, each with a name, a color and a condition from 1 to 100.
Generate Race Schedule picks 10 random horses for each of 6 rounds. Start Race runs
the rounds one after another, with the distance growing each round.

| round | distance |
| :---- | :------- |
| 1     | 1200 m   |
| 2     | 1400 m   |
| 3     | 1600 m   |
| 4     | 1800 m   |
| 5     | 2000 m   |
| 6     | 2200 m   |

a horse's speed depends on its condition and a random factor. the track shows
the horses moving in real time. after each round the results panel shows the winner.
the full results dialog lists every horse's position, time and medal per round, and the stable
dialog shows each horse's condition, status and performance across the day.

## structure

```
src/store/modules  horses, race and game state in Vuex
src/utils          race logic: horse selection, speed and results
src/components     track, horse list, controls and dialogs
```

## run locally

```bash
npm install
npm run dev
```

| command            | what it does                        |
| :----------------- | :---------------------------------- |
| `npm run build`    | production build                    |
| `npm run test`     | Vitest unit tests of the race logic |
| `npm run test:e2e` | Cypress test of the full game flow  |

pushes to main are deployed to GitHub Pages.

## license

MIT
