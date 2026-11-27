<!--
SPDX-FileCopyrightText: 2026 Paolo Ungari and contributors
SPDX-License-Identifier: CC-BY-4.0
-->

# Changelog

All notable changes to the default community health files of the Eiraman organisation are documented in
this file. The format is based on [Keep a Changelog 1.1](https://keepachangelog.com/en/1.1.0/), and versions
follow [community/VERSIONING.md](https://github.com/eiraman/community/blob/main/VERSIONING.md).

## [Unreleased]

## [0.3.0] - 2026-11-27

Scope: Change Request CR-030 of the method project, work package WP-30D (organisation defaults), after
decision D-IT-1 of the Human Manager (CR-029). **Breaking:** a rule of `CONTRIBUTING.md` changes and an
obligation is removed (VERSIONING §2.1): the Italian translation of the Guide is curated and approved by the
Author and no longer needs two native-speaker reviewers. While the artifact is at `0.y.z`, a change that would
be MAJOR bumps MINOR (VERSIONING §2.6), hence the version bump: MINOR. The reviewer rule for translations into
other languages is unchanged.

### Changed

- `CONTRIBUTING.md` §5, "Translations and training": English is canonical and prevails; the Italian
  translation of the Guide is curated and approved by the Author (D-IT-1); translations into other
  languages need two native-speaker reviewers and are informative until the Author approves them as faithful.
- `PULL_REQUEST_TEMPLATE.md`: the two native speakers are required for translations into languages other
  than Italian; for the Italian translation of the Guide the reviewer is the Author.
- `ISSUE_TEMPLATE/5-adopter-case.yml`: the placeholder of the field "Eiraman version used" reads "Guide
  1.0.0-rc.6, Role Profiles release v0.11.0". Placeholder text only; the field is unchanged. The release is
  aligned to the Guide 1.0.0-rc.6 (decision D-031 of the Human Manager), not rc.5; the version of this release does
  not change, because it is still an unreleased candidate.

## [0.2.1] - 2026-11-26

Scope: Change Requests CR-005 and CR-006 of the method project. Version bump: PATCH, workflow only;
no organisation default changes.

### Fixed

- CI, `compliance.yml`: the local-path check removes http(s) URLs from the matched lines and matches
  again, so a path segment inside a URL (such as `/home/` in an official ISO URL) is no longer flagged.
  The block is the one of `role-profiles` v0.4.1 (the whole workflow file is now identical to that one). Change Requests CR-005 and CR-006 of the
  method project.

## [0.2.0] - 2026-11-26

### Added

- `CONTRIBUTING.md` §1 links the release checklist and the versioning rules in `community`, and describes
  the `changelog` CI check. No contribution rule changes.
- This changelog, and the CI workflow `changelog.yml`.

## [0.1.0] - 2026-11-25

First public release, published as commit `0d4ea5f` of `github.com/eiraman/.github` during the restricted
launch of 25 November 2026. It was not tagged; the version number was assigned afterwards. The tag `v0.1.0` will be applied retroactively to that commit.
All files are drafts, not yet in force.

### Added

- `CONTRIBUTING.md`: workflow with the three states of a contribution, the Developer Certificate of Origin
  and the sign-off rule, the mandatory AI assistance declaration (`AI-Use:`, `Accountable-Human:`,
  `Assisted-by:`), the Role Profile path and profile states, other contributions and recognition.
- `CODE_OF_CONDUCT.md` and `SECURITY.md`.
- Issue templates (new Role Profile, profile change, RFC proposal, security guidance, adopter case, tool
  bug) and the pull request template.
- `profile/README.md`, the organisation landing page.
- CI: compliance checks (DCO and AI declaration, REUSE, secrets and deny-list) and the Markdown link check.

[Unreleased]: https://github.com/eiraman/.github/compare/v0.3.0...main
[0.3.0]: https://github.com/eiraman/.github/compare/v0.2.1...v0.3.0
[0.2.1]: https://github.com/eiraman/.github/compare/v0.2.0...v0.2.1
[0.2.0]: https://github.com/eiraman/.github/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/eiraman/.github/releases/tag/v0.1.0
