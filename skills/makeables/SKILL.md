---
name: makeables
description: Create, edit and render cards, personalized badges and die-cut stickers with Makeables. Use for card designs from prompts, images or original SVGs, layered materials, badges, glitter and holographic stickers, gallery submissions and requested iPhone Wallet artwork changes.
---

# Makeables

This is a discovery stub. Versioned workflows and design instructions ship
inside the Makeables CLI; load them from the installed version.

## Set up the CLI

Requires Node.js 22+ and `makeables` 0.4.0 or newer. Check `node --version`
and `makeables --version`.

If Makeables is missing, too old or does not support `skills get`, check
`npm view makeables version`. If a compatible release is available, install
or update it with:

```sh
npm install --global makeables@latest
```

Reuse existing installation authorization; otherwise ask once before installing.
Check the version again after installation. If npm still offers a version below
0.4.0, explain that the usable CLI release is not yet available and offer the
browser studio at https://makeables.dev. Do not claim the CLI setup succeeded.

## Load the workflow

Before designing, read:

```sh
makeables skills get core
```

Then load only the relevant guide:

- Cards, references and original SVG edits: `makeables skills get cards`.
- Apply, switch or restore an existing Wallet card design: `makeables skills get wallet`.
  Load it when the user chooses phone installation after a card preview, too.
- Badges: `makeables skills get badges`; follow the core guide's portrait and
  display-name intake when a personalized badge needs them.
- Stickers: `makeables skills get stickers`; use the shared Design Studio, sidebar
  gallery and glitter, holographic or vinyl materials. No portrait is needed.
- Full design vocabulary: `makeables skills get design`.
- Local reference tools, tracing or optional image generation: `makeables skills get images`, only
  when the requested work needs them.

Use `makeables skills list` for discovery, or `makeables skills get core --full`
when all guides are useful. Cards and stickers do not require a portrait or badge intake.
Follow the loaded guide for editable documents, rendering, live materials and
revisions. Preserve the user's artwork and requested scope.

Creating, editing, local saving and export need no account. Publishing is a
separate action: follow the CLI guide and the user's approval for the exact
design being shared. Cards, badges and stickers use `makeables submit` or the same `/submit`
form, with admin review. Keep the complete editable document or portable package;
report pending review separately from public approval.


Follow the cards guide's ready-preview handoff: offer to keep iterating,
submit to the gallery, or install the design on the phone. Respect a choice
already made for the displayed version. Wallet operations need the user's
request and an established target; creating a design alone does not authorize
publication or device changes. Keep original-artwork backups private.
