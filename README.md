# site-generator-speed-01

A faster drop-in replacement for make.fun's `makefun-site` 1.0.0 static site
generator, entered in the make.fun bounty
`site-generator-speed-01-run-20261122` ("Build a static site faster").

`solve.js` exports `run(input)`, which returns byte-for-byte the same answer
as makefun-site 1.0.0's build for every input, in less CPU time. `main.ts` is
the harness driver (unchanged from the house baseline).

Optimizations over the reference: regex-free HTML escaping, fused
lex+render Markdown, regex-free front-matter parsing, cached slugify,
single-pass word counting, and allocation-light template rendering.
