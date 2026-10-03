---
name: makeables
description: Make cards, personalized badges, die-cut stickers, sticker sheets, kits and brand pages with the Makeables CLI. Use for a card, badge or sticker design, a kit or merch pack for an event (including a Luma or Eventbrite link), a brand or company, a print-ready sticker sheet, a brand page at makeables.dev/brands, gallery submissions, and requested iPhone Wallet artwork changes.
---

# Makeables

This is a short entry point. The real instructions ship inside the Makeables CLI.
Load them from the installed version.

## Set up the CLI

You need Node.js 22+ and `makeables` 0.11.0 or newer. Check both:

```sh
node --version
makeables --version
```

If Makeables is missing or older, run `npm view makeables version`. If 0.11.0 or
newer is available, ask once (unless the user already allowed installs), then run:

```sh
npm install --global makeables@latest
```

Check the version again. If npm still gives you a version below 0.11.0, tell the
user, and offer the studio at https://makeables.dev in a built-in browser if one
is available. Do not say the setup worked when it did not.

If a working Makeables MCP connection is available, you can skip the CLI. Load
the same guides with `makeables_inspect` (`section: "guide"`, `guide: "core"`).

## Load the guides

Always start with:

```sh
makeables skills get core
```

Then load the one guide for the job:

| Job | Guide |
| --- | --- |
| A card, from a prompt, image or SVG | `makeables skills get cards` |
| A personalized badge (asks for a photo and name) | `makeables skills get badges` |
| A sticker | `makeables skills get stickers` |
| A kit, brand or event pack (a Luma or brand URL counts) | `makeables skills get kits` |
| A print sheet or PDF | `makeables skills get sheets` |
| Image tools or image generation | `makeables skills get images` |
| Put artwork on an existing iPhone Wallet card | `makeables skills get wallet` |

For a kit, brand or event, the `kits` guide starts with `makeables preflight`. It
checks image generation and asks the user about the art source before any piece.

Run `makeables skills list` to see every guide.

## Build with commands

Make every piece with CLI commands: `new`, `layer add`, `layer set`,
`material set`, `badge package`, `kit`, `brand` and `sheet`. Do not write scripts
that generate design files, do not build packages by hand, and do not read the
CLI's installed source. `makeables schema` lists every field. If a command you
need does not exist, tell the user.

## Show the preview

Use the simplest preview you have:

1. **MCP Apps widget**, if the host can show Makeables tools.
2. **Built-in browser panel**: run `makeables studio start --no-open --json` and
   open the returned URL there. Keep one session and one tab.
3. **Image in the chat**: render a PNG with the CLI, look at it, and show it.

Check what is really available; the client's name does not tell you. Do not open
an external browser or install anything just to get a preview.

## Publish

Making, editing, saving and exporting need no account. Publishing needs the
user's approval for the exact design. Cards, badges, stickers, kits and brands
all use `makeables submit`, and an admin reviews each one. Pending means waiting
for review; approved means public. Say which one it is.

## Wallet

For an iPhone Wallet request, load `makeables skills get wallet` directly and
follow it. Only change the phone when the user asks, on a card they confirmed,
and keep the original-artwork backup private. Never guess which card is which
from artwork, numbers or tap order; ask.
