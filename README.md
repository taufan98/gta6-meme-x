# gta6-meme-x — GTA 6 meme entry for make.fun

Entry for the make.fun bounty [gta6-meme-x-01](https://make.fun/bounty/gta6-meme-x-01)
("Post a GTA 6 meme on X"): an AI judge compares the posts two at a time, and the
top 50 share $500.

## The meme

![GTA 6 meme: waited 13 years, now waiting for the download](gta6-meme.png)

> **WAITED 13 YEARS FOR GTA 6**
> **NOW I'M WAITING FOR THE DOWNLOAD**

The joke: after 13 years since GTA V, the game is finally out — and the download
screen says "Time remaining: 13 years". The make.fun ghost sits on the couch next
to him, holding its magenta star coin, waiting along with him.

make.fun is a site where people and their AI agents build things, enter them in
paid competitions (bounties) and earn real money when they win.

## The post is the entry

The post goes out on X from a public account with the meme as its first picture,
its text carrying make.fun (a link or written out) and/or a tag of `@makefunai`,
and the entrant's play code. `POST.json` at this repository's root names the
post's address:

    {"url": "https://x.com/<handle>/status/<id>"}

Posted on X at https://x.com/sadewa0981/status/2123450918117294269 with play code
`makefun-emerald-portrait-brook`.

`main.ts` (Node 22, standard library only) copies `POST.json` from this
repository to `/output/POST.json`. That is all the program has to do — the house
reads the post itself from X and the judge sees the post's first picture and
its text.

## Run it locally

    mkdir -p out && MAKEFUN_BOT_DIR=. MAKEFUN_OUTPUT_DIR=out node main.ts

`out/POST.json` is then byte for byte this directory's `POST.json`.
