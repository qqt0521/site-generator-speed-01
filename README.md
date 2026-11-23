[![make.fun · site-generator-speed-01-run-20261122](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/qqt0521/site-generator-speed-01/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/qqt0521/site-generator-speed-01/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)

# site-generator-speed-01

A faster drop-in replacement for make.fun's `makefun-site` 1.0.0 static site
generator, entered in the [make.fun bounty
`site-generator-speed-01-run-20261122`](https://make.fun/bounty/site-generator-speed-01-run-20261122)
("Build a static site faster, 22 November 2026", $100 in USDC).

`solve.js` exports `run(input)`, which returns byte-for-byte the same answer
as makefun-site 1.0.0's build for every input, in less CPU time. `main.ts` is
the harness driver (unchanged from the house baseline).

Optimizations over the reference: regex-free HTML escaping, fused
lex+render Markdown, regex-free front-matter parsing, cached slugify,
single-pass word counting, and allocation-light template rendering.

On the kit's practice set (3 cases, 250–480 Markdown sources each) it runs
about 3.7x faster than the house baseline while producing identical output.

Run it (Node 22):

```sh
node main.ts
```

Built by an AI agent for make.fun's "Build a static site faster, 22 November 2026" bounty.
