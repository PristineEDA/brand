# Pristine Brand System Repository Guide

## Scope

This file applies to the entire repository. This repository exists only for
the Pristine brand system maintained in PristineEDA/brand: logos, banners,
icons, illustrations, templates, design tokens, usage guidance, and the small
tools needed to maintain those assets.

Do not use this repository for product source code, hardware design files,
general project documentation, or unrelated marketing content. Preserve the
PristineEDA identity and existing assets when extending the repository.

## Repository Contract

Use the following structure as approved content and assets are added. This
tree is a directory contract, not an inventory of existing deliverables.
Git does not track empty directories; do not add placeholder files merely to
reproduce the tree.

```text
.
|-- AGENTS.md
|-- README.md
|-- LICENSE.md
|-- TRADEMARKS.md
|-- LICENSES/
|   |-- CC-BY-4.0.txt
|   `-- MIT.txt
|-- docs/
|   |-- brand-guidelines.md
|   |-- logo-usage.md
|   `-- contributing-assets.md
|-- tokens/
|   |-- brand.tokens.json
|   `-- brand.css
|-- assets/
|   |-- source/
|   |   |-- logo/
|   |   |-- banners/
|   |   |-- icons/
|   |   |-- illustrations/
|   |   `-- templates/
|   `-- export/
|       |-- logo/
|       |-- banners/
|       |-- icons/
|       |-- illustrations/
|       `-- templates/
|-- examples/
|-- third-party/
|   |-- README.md
|   |-- fonts/
|   `-- licenses/
`-- scripts/
```

Once introduced, the repository has four complementary sources of truth:

- `docs/brand-guidelines.md` defines the approved visual language and usage intent.
- `docs/logo-usage.md` defines approved logo variants and restrictions.
- `tokens/brand.tokens.json` contains canonical machine-readable values;
  `tokens/brand.css` is a derived distribution format and must remain in sync.
- `assets/source/` contains editable masters. Files in `assets/export/` are
  derived, ready-to-use deliverables and are never the only editable copy.

These visual definitions and assets are not present yet. Do not invent missing
brand colors, typography, logo geometry, positioning, or usage rules. Limit
the change to what the request explicitly establishes.

## Change Workflow

Work on a separate branch and submit a pull request; do not write directly to
or merge the default branch as part of preparing a contribution.

Before changing an asset:

1. Read the applicable brand guidelines, logo rules, tokens, and editable master.
2. Inspect every existing export of the asset so that variants remain consistent.
3. Confirm that all source material can be redistributed and that required
   attribution is recorded.

When changing an asset:

- Do not alter the brand position, logo geometry, approved colors, or
  typography unless the request explicitly calls for a brand-system change.
- Edit the master under `assets/source/`, then update every affected file under
  `assets/export/` in the same change. Do not patch a generated export as if it
  were the master.
- Preserve aspect ratios, clear space, alignment, and variant relationships.
  Do not stretch, rotate, recolor, crop, outline, or add effects to an official
  mark unless an approved guideline explicitly permits it.
- Preserve an editable master before outlining text, flattening layers,
  rasterizing artwork, optimizing paths, or removing metadata.
- Prefer SVG for logos and icons. Public SVG exports must have an appropriate
  `viewBox`, must be self-contained, and must not depend on remote resources or
  fonts that recipients may not have.
- Include pixel dimensions in raster export names. Generate print-only formats
  such as PDF only for a concrete use case.
- Do not add a build tool, perform a repository-wide regeneration, or redesign
  an official logo unless the request explicitly requires it.

## Naming and Versioning

Use lowercase ASCII kebab-case with this general form:

```text
pristine-{asset}-{variant}-{theme}-{dimensions}.{ext}
```

These are naming examples, not existing assets or approved variants:

```text
pristine-logo-horizontal-color.svg
pristine-logo-mark-mono-light.svg
pristine-banner-github-dark-1280x640.png
```

- Do not use spaces, dates, personal names, `final-final`, or hand-maintained
  version suffixes such as `v2`. Git history and release tags provide versions.
- Omit components that do not apply, but keep equivalent source and export
  names easy to correlate.
- Use platform subdirectories only after the repository has more than one
  platform-specific asset in that category.

## Licensing, Trademarks, and Provenance

`AGENTS.md` is contributor guidance, not a grant of rights.
[`LICENSE.md`](LICENSE.md) and [`TRADEMARKS.md`](TRADEMARKS.md) define the
applicable terms:

- Original Pristine banners, illustrations, templates, documentation, and
  design tokens use Creative Commons Attribution 4.0 International
  (`CC-BY-4.0`). Identify the project and credited creators, link to the license
  and source, preserve supplied notices, and indicate modifications.
- Official logos, logo marks, wordmarks, and the Pristine and PristineEDA
  names are excluded from that CC license. Their permitted uses are defined
  by `TRADEMARKS.md`; do not imply sponsorship or official status.
- Original maintenance and generation code under `scripts/` uses MIT.
  The current MIT text is a template: record verified copyright notices when
  code is first added.
- Icons require explicit per-icon terms; official marks also follow the
  trademark policy.
- Third-party material retains its upstream licenses. Record the creator,
  original URL, license identifier, required notices, and modifications in
  [`third-party/README.md`](third-party/README.md); include full license text
  when redistribution requires it. Preserve the upstream attribution for
  adapted documentation as well as for artwork.

Never scrape or import artwork merely because it is publicly visible. Do not
remove attribution, overwrite the only editable master, or add fonts, stock
material, or AI-generated material whose redistribution rights or provenance
are unclear. AI-generated visual assets may be added only when explicitly
requested and approved, with the model/provider, prompt and input provenance,
applicable terms, and human modifications documented.

## Validation

For every documentation change, verify relative links, path spelling and
case, the documentation index, licensing consistency, and the distinction
between existing files and future directory conventions. Do not link to
nonexistent future files as if they were available.

For every asset change:

1. Open or render each changed file and inspect it visually; a successful
   export command alone is not sufficient.
2. Verify dimensions, aspect ratio, transparency, color mode, legibility, and
   the intended light/dark background behavior.
3. For SVG files, verify the `viewBox`, bounds, embedded resources, and absence
   of broken external references.
4. Confirm that source and export variants are synchronized and that no
   unrelated assets were regenerated.

For every change, run any validation scripts documented by the repository,
then run `git diff --check` (or `git diff --cached --check` for staged changes)
and inspect `git status --short`. Check PR CI results if any checks are configured.

Report which files and variants were checked. If a required format cannot be
rendered with the available tools, state that limitation instead of claiming
visual verification. For documentation-only changes, state that asset checks
are not applicable.

Adapted from retroSoC guidance under CC BY 4.0; see the
[attribution and modification record](third-party/README.md#retrosoc-documentation).
