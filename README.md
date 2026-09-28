# Makeables Community

The public home for the Makeables agent skill, bug reports and feature requests.

[Makeables](https://makeables.dev) is a design studio for cards and personalized
badges, with editable layers, original SVG artwork and live WebGPU materials.

## Install the skill

```sh
npx skills add crafter-station/makeables-community --skill makeables
```

Select your coding agent and installation scope when prompted. Then ask it to
use the `makeables` skill.

The skill checks for Node.js 22+ and Makeables 0.1.0 or newer. When installation
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

The agent loads focused instructions with `makeables skills get cards` or
`makeables skills get badges`. `makeables skills list` lists the available
guides. Creation and local export require no account; public sharing is a
separate, approved action.

## Bugs and ideas

- [Report a bug](https://github.com/crafter-station/makeables-community/issues/new?template=bug_report.yml)
- [Request a feature](https://github.com/crafter-station/makeables-community/issues/new?template=feature_request.yml)
- [Browse existing issues](https://github.com/crafter-station/makeables-community/issues)

Include your CLI version when relevant and remove credentials or private studio
session URLs from logs.

## What lives here

- `skills/makeables/SKILL.md`: the canonical installable discovery stub.
- `.github/ISSUE_TEMPLATE/`: bug-report and feature-request forms.

The application source and full CLI guides are maintained separately. Update
this stub when bootstrap or guide discovery changes; design instructions belong
to the versioned CLI.

Made by [Crafter Station](https://crafter.run). See [LICENSE](LICENSE) for
permission to use the skill and documentation.
