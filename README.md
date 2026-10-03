# Makeables Community

The public home for the Makeables agent skill, Wallet companion downloads, bug reports and feature requests.

[Makeables](https://makeables.dev) is a design studio for cards, personalized
badges and die-cut stickers, with editable layers, original SVG artwork and live WebGPU materials.

## Install the skill

```sh
npx skills add crafter-station/makeables-community --skill makeables --global
```

Select your coding agent when prompted. Omit `--global` for a project-only install. Then ask it to
use the `makeables` skill.

The skill checks for Node.js 22+ and Makeables 0.11.0 or newer. When installation
is authorized, it installs or updates the CLI if needed, then reads
`makeables skills get core`. Product workflows and creative guidance are
bundled with the CLI rather than copied into this repository.

If npm does not yet offer a compatible CLI version, the skill explains the
release requirement. You can use the [browser studio](https://makeables.dev)
in the meantime; installing the skill and installing the CLI are separate steps.

## Make something

**Card:** “Use Makeables to design a credit card for a fictional bank inspired
by the solstice. Coordinate both faces, the chip, contactless symbol, payment
network and materials. Keep everything editable.”

**Badge:** “Use Makeables to create a badge from my photo. My display name is
Alex. Use expressive typography and a chrome finish, then show me both sides.”

**Sticker:** “Use Makeables to create an original die-cut sticker with a holographic
finish. Keep its layers editable and show it in the shared Design Studio.”

The agent loads one focused guide per job with `makeables skills get cards`,
`badges`, `stickers`, `kits`, `sheets`, `images` or `wallet`. `makeables skills list` lists the available
guides. Creation and local export require no account; public sharing is a
separate, approved action.

Cards, badges and stickers share `/submit` in the browser and the same CLI submission flow:

```sh
makeables submit --file design.json --dry-run
makeables submit --file design.json --yes
makeables submit status --file design.json
```

Editable JSON, original card SVGs and portable packages are supported. Designs
stay private while awaiting review; gallery publication follows admin approval.

## From a card preview to your phone

After showing a card, the agent offers to iterate, submit it to the gallery, or
install the artwork on your phone. If you choose installation, it loads
`makeables skills get wallet`. `makeables wallet setup` downloads the matching
Mac companion and verifies the checksum pinned in your CLI version. No source
checkout, Python installation or Xcode is needed.

The companion applies artwork to an existing Wallet card over USB and preserves
verified original-artwork backups for restoration. It does not add or remove
payment cards. This uses experimental, unofficial device services: artwork
apply has been tested on a Wallet card; restoration on an actual Wallet card
remains unverified. The website itself never writes to your phone.

## Bugs and ideas

- [Report a bug](https://github.com/crafter-station/makeables-community/issues/new?template=bug_report.yml)
- [Request a feature](https://github.com/crafter-station/makeables-community/issues/new?template=feature_request.yml)
- [Browse existing issues](https://github.com/crafter-station/makeables-community/issues)

Include your CLI version when relevant and remove credentials or private studio
session URLs from logs. Do not attach Wallet backups, raw device logs or card resource IDs.

## What lives here

- `skills/makeables/SKILL.md`: the canonical installable discovery stub.
- `.github/ISSUE_TEMPLATE/`: bug-report and feature-request forms.
- Releases: versioned macOS Wallet companion archives, with checksums.

The application source and full CLI guides are maintained separately. Update
this stub when bootstrap or guide discovery changes; design instructions belong
to the versioned CLI.

Made by [Crafter Station](https://crafter.run). See [LICENSE](LICENSE) for
permission to use the skill and documentation.
