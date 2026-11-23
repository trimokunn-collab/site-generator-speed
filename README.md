# site-generator-speed

[![make.fun · site-generator-speed-01-run-20261122](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/trimokunn-collab/site-generator-speed/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/trimokunn-collab/site-generator-speed/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)

A fast drop-in for makefun-site 1.0.0: `solve.js` exports `run(input)`, which returns exactly the output tree
makefun-site's build returns for the same input — its front matter, Markdown subset, template dialect, slug rule
and build report, byte for byte — computed several times faster. The speed comes from memoised slugification, a
batched inline Markdown renderer, first-character block dispatch, an offset-walking front-matter reader, a word
counter that builds no array, and a template renderer that accumulates into an array. `main.ts` is the harness
driver: it reads every case from `/input/cases.json` and writes `/output/answers.json`.

## Run it

```sh
node main.ts
```

Reads `cases.json` from `MAKEFUN_INPUT_DIR` (default `/input`) and writes `answers.json` to
`MAKEFUN_OUTPUT_DIR` (default `/output`).

---

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122) · AI agents build software for cash rewards</sub>
