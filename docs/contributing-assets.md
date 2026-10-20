# Contributing Assets

This guide supplements the repository-wide rules in [`AGENTS.md`](../AGENTS.md).
It covers the rights, provenance, source files, and exports required for a
Pristine brand-system contribution. Submit changes on a separate branch
through a pull request.

## Rights and contribution terms

Before submitting material, confirm that you created it or have permission to
redistribute it in this repository and in the intended exported formats. Do
not scrape or import artwork merely because it is publicly visible.

Contributors retain copyright in their original contributions. By submitting
original documentation, design tokens, banners, illustrations, or templates,
you agree to make that contribution available under CC-BY-4.0 as described in
[`LICENSE.md`](../LICENSE.md). By submitting original maintenance or generation
code under `scripts/`, you agree to make it available under MIT and provide
the verified copyright notices required by that policy.

This guide introduces no copyright assignment, Contributor License Agreement,
or Developer Certificate of Origin requirement. A proposed
official name, logo, logo mark, or other brand mark requires an explicit rights
statement agreed with the maintainers before it can be accepted; do not assume
that the open licenses apply to it. Each icon needs its own explicit terms.

## Source and export requirements

- Read all applicable approved guidelines, logo rules, and tokens before
  editing. Do not invent missing brand decisions or import another project's
  visual identity.
- Add the editable master under the appropriate `assets/source/` directory.
- Add every required ready-to-use form under the corresponding
  `assets/export/` directory in the same change.
- Keep source and export names easy to correlate and follow the lowercase
  ASCII kebab-case `pristine-` naming convention in `AGENTS.md`.
- Preserve an editable master before outlining text, flattening layers,
  rasterizing artwork, optimizing paths, or removing metadata.
- Do not stretch, rotate, recolor, crop, outline, or add effects to an official
  mark unless an approved rule expressly permits it.

## Provenance information

For an original contribution, include the creator, creation method, applicable
repository license, and any source inputs. For a third-party contribution,
including adapted documentation, complete the record required by
[`third-party/README.md`](../third-party/README.md) and include any full license
text required for redistribution. Do not remove supplied copyright notices or
replace them with unsupported Pristine copyright claims.

Add AI-generated visual material only when explicitly requested and approved
by a maintainer. Record:

- the model and provider;
- the prompt and any image, font, text, or other input provenance;
- the provider terms applicable when the output was generated; and
- a description of human modifications.

Do not submit fonts, stock material, third-party artwork, or AI-generated
visual material when its redistribution rights or provenance are unclear.

## Review checklist

Before requesting review:

1. Inspect every changed asset source and export visually.
2. Verify dimensions, aspect ratio, transparency, color mode, legibility, and
   light/dark-background behavior as applicable.
3. For SVG, verify the `viewBox`, bounds, embedded resources, and absence of
   remote dependencies.
4. Confirm that all affected variants are synchronized and no unrelated assets
   were regenerated.
5. Verify documentation links, case-sensitive paths, the index, licensing
   consistency, and whether described files actually exist.
6. Run any documented validation, `git diff --check` (or
   `git diff --cached --check` for staged changes), and `git status --short`.
7. Describe the changes and validation in the PR. Check any CI results and
   resolve failures caused by the contribution.

For documentation-only contributions, steps 1-4 do not apply. State any
validation limitations instead of claiming checks that were not performed.

Adapted from retroSoC guidance under CC BY 4.0; see the
[attribution and modification record](../third-party/README.md#retrosoc-documentation).
