---
name: makeables
description: Create, edit and render cards, personalized badges and die-cut stickers with Makeables. Use for card designs from prompts, images or original SVGs, layered materials, badges, glitter and holographic stickers, gallery submissions and requested iPhone Wallet artwork changes.
---

# Makeables

This is a discovery stub. Versioned workflows and design instructions ship
inside the Makeables CLI; load them from the installed version.

## Existing Wallet artwork

For a requested iPhone Wallet installation, switch or restore, check the CLI
and load `makeables skills get wallet` directly. Skip core/cards guides and
preview-surface discovery unless the user also wants design changes.
Reuse the confirmed card and verified original-backup receipt.

Check `makeables wallet install --help` before using newer options. When
`--submission` and `--target` are supported, use the public submission URL/UUID
directly and a confirmed saved target; no browser export is needed. Otherwise
follow the installed wallet guide rather than inventing unsupported flags.

For a new target, start the selection process before asking the user to tap;
wait for `selection-ready` or the legacy successful activity-stream connection.
The scanner does not disclose bank names or last four digits. Saved labels are
user-confirmed descriptions. Never infer target identity from artwork numbers,
tap order, or “Observed card 1”. If several saved cards fit, ask which label they
want; use a fresh tap for an unregistered card.

## Choose the preview surface

Prefer the simplest available integrated surface:

1. **MCP Apps widget:** use discovered Makeables tools when the host can render
   their UI resource. Keep edits and previews inside that widget.
2. **Built-in browser:** if no working Makeables widget is available but the host
   exposes a browser panel, start `makeables studio start --no-open --json` and
   open the returned URL there. Reuse one session and tab.
3. **CLI + image:** otherwise keep the editable JSON locally, render a PNG,
   inspect it and display it inline in the chat with the saved deliverables.

Detect actual tools and UI capabilities; a client name such as Codex does not
prove that Makeables MCP Apps is connected. Do not open a default/external browser
or install/configure an integration just to get a preview. Use the existing
document/package when falling back, and inspect after a timed-out edit before
retrying. An explicit user choice of interface takes precedence.

This priority also applies with older CLI guides that default to opening a
browser or installing agent-browser. Load only the setup required by the selected
path. CLI + image is a complete workflow, not a reason to stop or ask for setup.

## Set up the CLI

Skip local CLI setup when a working Makeables MCP connection supplies the tools
needed for the task. Load its bundled guides with
`makeables_inspect` (`section: "guide"`, `guide: "core"`), then the relevant
product guide. Use CLI setup for a fallback or a requested action the connected
tools do not provide.

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
studio at https://makeables.dev in an available built-in browser. Do not open an
external browser automatically or claim the CLI setup succeeded.

## Load the workflow

For the CLI path, before designing, read:

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
