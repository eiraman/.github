<!--
SPDX-FileCopyrightText: 2026 Paolo Ungari and contributors
SPDX-License-Identifier: CC-BY-4.0
-->

# Security Policy

Status: **draft**. Values marked **proposal** are to be decided.

Eiraman has two kinds of security issues: vulnerabilities in the **tools**, and **unsafe guidance** in Role Profiles, templates, the gate checklist or the Guide. Both are reported privately. Do not open public issues for them.

## 1. Reporting

- Private vulnerability reporting on the repository (preferred): `<link PLACEHOLDER>`
- Email: `<security@PLACEHOLDER>` (encryption key: `<PLACEHOLDER>`)

Please include: affected artifact and version (release tag or commit), description, steps or prompts to reproduce, impact, and whether you used AI to find or describe the issue (see CONTRIBUTING §3).

## 2. Vulnerabilities in tools

In scope: the profile validator, the activation tool, the Digital Seniority map, CI workflows, release signing and manifests, the site generator and any other code in the project's repositories.

| Step | Target (proposal) |
|---|---|
| Acknowledgement | 3 working days |
| Triage and severity (CVSS) | 10 working days |
| Fix for critical or high severity | 30 days |
| Coordinated disclosure | at most 90 days after the report, or earlier when a fix is released |

Handled by the DevSecOps & Tooling maintainers with the Security domain reviewer. The fix is reviewed by someone other than its author and published in a signed release with an advisory. A CVE is requested where applicable. Reporters are credited unless they ask otherwise.

## 3. Unsafe guidance in Role Profiles and other content

Report guidance that could cause harm when followed by an agent or an adopter, for example:
- a rule that produces insecure configurations or weakens a control;
- a wrong or outdated source citation that changes a security, privacy or legal requirement;
- anomalous or injected instructions in a profile (prompt injection, hidden text, instructions unrelated to the role);
- a gap in the gate checklist that lets an out-of-scope project through (Guide §14);
- an applicability level requirement that is unsafe for its project class.

Process:
1. **Triage** by the titular reviewer of the affected domain (substitute if unavailable), with the Security reviewer, within 3 working days (**proposal**).
2. **Containment.** If the guidance is confirmed or plausibly unsafe, any domain reviewer or the Security reviewer may **suspend** the profile, template or checklist version immediately. This is a pre-authorised reversible containment action (Guide §5) and needs no prior vote. Suspension is recorded with its reasons and notified to declared adopters.
3. **Correction** through the ordinary path (CONTRIBUTING §4), with four eyes and a new qualification.
4. **Disclosure.** An advisory states the affected versions, the risk and the corrected version. Adopters at level 1 or higher must treat the suspension as a lost requirement (automatic step down under the level requirements of the Extended Framework) until they move to the corrected version.

The reviewer answers for the correctness of a profile against its sources at the time of review, not for the projects that use it (GOVERNANCE §4.5). Adopters remain responsible for their projects.

## 4. Supported versions

Security fixes are made for the latest release of each artifact. Suspended profiles receive no fixes until they are requalified.
