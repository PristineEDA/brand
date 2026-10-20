# Third-Party Material

This directory is the provenance and licensing register for third-party
material redistributed by the Pristine brand-system repository.

The repository includes adapted retroSoC documentation, recorded below. No
third-party artwork, fonts, icons, or maintenance software are currently
included.

## Material covered by this register

Record any redistributed material not created for Pristine by its contributors,
including documentation, fonts, icons, stock material, copied themes, binaries,
templates, and source artwork. Public visibility or free download access is
not evidence of a right to redistribute a work.

Development-only tools do not belong in this register unless their code or
assets are actually redistributed with a repository deliverable.

## Required record

Add a record before adding the corresponding material. Include every field
below; use `None` only when the upstream terms make the field inapplicable.

```text
Repository path:
Creator or copyright owner:
Original source URL:
License identifier or exact license name:
Required notices:
Modifications made:
Local full-text license path:
```

- Prefer an SPDX identifier when the upstream license has one.
- Describe modifications precisely enough to distinguish the redistributed
  copy from the upstream work.
- Preserve upstream copyright and attribution notices verbatim when required.
- Put complete license texts under `third-party/licenses/` when redistribution
  requires them, or link to an identical full text already in `LICENSES/`.
  Create new directories only when real material is added.
- If one work is offered under multiple licenses, record the option actually
  used for redistribution and preserve all notices required by that option.

Do not copy a third-party work into the repository until its record is complete
and its terms permit the intended redistribution and modification. Third-party
material is never relicensed under the repository's CC-BY-4.0 or MIT defaults.

## retroSoC documentation

- **Repository paths:** [`AGENTS.md`](../AGENTS.md), [`README.md`](../README.md),
  [`LICENSE.md`](../LICENSE.md), [`TRADEMARKS.md`](../TRADEMARKS.md),
  [`docs/contributing-assets.md`](../docs/contributing-assets.md), and this
  `third-party/README.md`.
- **Creator or copyright owner:** retroSoC contributors, as credited upstream.
- **Original source URL:**
  <https://github.com/retroSoC/brand/tree/92eef243de832fedbab4977e04a27aa410c2dc88>,
  using the corresponding paths at that commit. The license scope is stated
  in the [upstream LICENSE.md](https://github.com/retroSoC/brand/blob/92eef243de832fedbab4977e04a27aa410c2dc88/LICENSE.md).
- **License identifier:** `CC-BY-4.0`,
  <https://creativecommons.org/licenses/by/4.0/>.
- **Required notices:** Copyright (c) 2026 retroSoC contributors.
  Retain upstream attribution, source and license links, the applicable
  disclaimer of warranties, and an indication of modifications. CC BY 4.0
  section 5 contains the disclaimer. No retroSoC endorsement is implied.
- **Modifications made:** Adapted for the Pristine brand system in
  PristineEDA/brand; retained the existing PristineEDA Brand System identity;
  changed project references, asset naming examples, and the permission-request
  URL; added a documentation index and explicit current-versus-future content
  status; specified a PR workflow and documentation validation; clarified
  per-icon licensing, attribution, AI visual-asset provenance, and the MIT
  template's notice requirements; added this provenance record. No retroSoC
  visual assets, brand values, software, or trademark permissions were imported.
- **Local full-text license path:**
  [`LICENSES/CC-BY-4.0.txt`](../LICENSES/CC-BY-4.0.txt).

These adapted documents remain under CC-BY-4.0. When redistributing one
separately, include this record or an accessible link to it so that its
upstream attribution and modification history remain available.

## Standard license texts

- [`LICENSES/CC-BY-4.0.txt`](../LICENSES/CC-BY-4.0.txt) reproduces the unmodified
  CC BY 4.0 legal text supplied in the pinned reference repository, with only
  the extra trailing blank line removed. Its canonical source is <https://creativecommons.org/licenses/by/4.0/legalcode.en>.
  The license text's closing notice identifies Creative Commons and dedicates
  the text of its public licenses to the public domain under CC0. It is not
  Pristine-authored material.
- [`LICENSES/MIT.txt`](../LICENSES/MIT.txt) contains the standard MIT terms,
  also available at <https://opensource.org/license/mit>. Compared with the
  reference repository, only its project-specific copyright line has been
  replaced by template fields. No retroSoC software is copied; that notice is
  not transferred to future Pristine software. See
  [`LICENSE.md`](../LICENSE.md#mit-licensed-maintenance-code) for how to complete
  the template using verified notices when code is added.
