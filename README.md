# PristineEDA Brand System

This repository maintains the Pristine brand system for PristineEDA: logos,
banners, icons, illustrations, templates, design tokens, usage guidance, and
the small tools used to maintain those assets.

It currently contains repository, contribution, licensing, and trademark
guidance. No visual assets, approved colors, typography, logo geometry, or
design tokens are published here yet. Product source code, hardware design
files, and unrelated project content do not belong here.

## Documentation index

| Document | Purpose |
| --- | --- |
| [Repository guide](AGENTS.md) | Scope, directory contract, naming, workflow, and validation |
| [Contributing assets](docs/contributing-assets.md) | Rights, provenance, editable masters, exports, and review |
| [Licensing](LICENSE.md) | License scope, attribution, and exclusions |
| [Trademark policy](TRADEMARKS.md) | Use of the Pristine and PristineEDA names and official marks |
| [Third-party register](third-party/README.md) | Upstream provenance, notices, and documentation adaptation |

## Repository layout

- `docs/` contains asset-contribution guidance. Add `brand-guidelines.md` and
  `logo-usage.md` only when approved visual decisions are available.
- `tokens/`, when introduced, contains canonical machine-readable design
  tokens and synchronized derived distribution formats.
- `assets/source/`, when introduced, contains editable masters.
- `assets/export/`, when introduced, contains synchronized, ready-to-use exports.
- `examples/`, when introduced, demonstrates approved usage.
- `third-party/` records provenance and upstream terms for redistributed
  material, including the adapted documentation in this repository.
- `scripts/`, when introduced, contains maintenance and asset-generation code.
- `LICENSES/` contains the CC BY 4.0 legal text and an MIT license template.

Directories are added only when they contain real material. Do not add
placeholder files to reproduce an empty directory tree. The complete future
directory contract is in [`AGENTS.md`](AGENTS.md).

## Contributing assets

Read [`docs/contributing-assets.md`](docs/contributing-assets.md) before adding
or changing an asset. Preserve an editable master, update every affected
export in the same change, and record sufficient provenance to demonstrate
that the material may be redistributed. Submit changes on a separate branch
through a pull request.

Do not invent missing brand colors, typography, logo geometry, or usage rules.
The applicable brand guidelines, logo rules, tokens, and editable masters are
authoritative once approved and added.

## Licensing

This is a multi-license repository:

| Material | Terms |
| --- | --- |
| Original documentation, design tokens, banners, illustrations, and templates | [CC-BY-4.0](LICENSES/CC-BY-4.0.txt) |
| Original maintenance and generation code under `scripts/`, when added | [MIT](LICENSES/MIT.txt), with verified copyright notices as explained in [Licensing](LICENSE.md) |
| Pristine and PristineEDA names, wordmarks, logos, logo marks, and official brand marks | [Trademark policy](TRADEMARKS.md), excluded from the open licenses above |
| Third-party material | Its upstream terms, recorded in the [third-party register](third-party/README.md) |
| Future icons | The explicit terms recorded for each icon; no blanket license applies |

See [`LICENSE.md`](LICENSE.md) for the scope and attribution requirements.
This documentation adapts the
[retroSoC brand repository](https://github.com/retroSoC/brand/tree/92eef243de832fedbab4977e04a27aa410c2dc88).
Upstream attribution and the changes made are recorded in
[`third-party/README.md`](third-party/README.md#retrosoc-documentation).
