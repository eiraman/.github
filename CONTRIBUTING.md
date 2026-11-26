<!--
SPDX-FileCopyrightText: 2026 Paolo Ungari and contributors
SPDX-License-Identifier: CC-BY-4.0
-->

# Contributing to Eiraman

Status: **draft**. Values marked **proposal** are to be decided.

Thank you for helping. Eiraman governs AI-assisted work with traditional management practice, and this project applies the same practice to its own contributions: a human is accountable for every change, the author never reviews their own work, and nothing is closed without evidence.

Before contributing, read the [Code of Conduct](CODE_OF_CONDUCT.md) and, for decisions and roles, [GOVERNANCE.md](https://github.com/eiraman/community/blob/main/GOVERNANCE.md). Find the right group in [WORKING-GROUPS.md](https://github.com/eiraman/community/blob/main/WORKING-GROUPS.md).

## 1. Workflow

1. **Issue first.** Open an issue that states the problem, the affected artifact and the evidence. Small fixes (typos, broken links) may skip this step.
2. **RFC if needed.** Changes listed in GOVERNANCE §6.2 (Guide text, levels, new families, breaking format changes, governance) need an RFC first. RFCs live in the `rfcs/` folder of the `guide` repository; see `guide/rfcs/README.md`.
3. **Pull request.** One logical change per pull request. Fill in the template, including the AI assistance declaration (§3) and any conflict of interest (GOVERNANCE §8).
4. **Automated checks (Deny).** CI checks DCO sign-off, the AI assistance declaration, formatting, links and, for Role Profiles, the validator. A failing check blocks the pull request; it is not waived by a reviewer.
5. **Review (four eyes).** At least one reviewer who is not the author. The owning group may require more (see WORKING-GROUPS). AI review tools may comment, but they never count as a reviewer.
6. **Acceptance.** The owner of the artifact records acceptance: lazy consensus of the group, or the RFC decision.
7. **Publication.** Accepted changes enter the next signed release. For Role Profiles, templates and the gate checklist, publication is by a domain reviewer (§4).

A contribution has three separate states, shown as labels on the pull request:

| State | Meaning | Closed when |
|---|---|---|
| Technical | Checks and review | All mandatory checks pass on the final commit, and the review is approved by someone other than the author |
| Acceptance | Decision of the owner | Recorded acceptance on that same commit |
| Publication | In a release | Included in a signed release with manifest |

If a required review or check is not available, the pull request stays open with the reason recorded. It is never merged "pending review".

Releases follow the checklist in [community/RELEASING.md](https://github.com/eiraman/community/blob/main/RELEASING.md), and versions the rules in [community/VERSIONING.md](https://github.com/eiraman/community/blob/main/VERSIONING.md). The `changelog` CI check expects each pull request to change the repository's `CHANGELOG.md`, normally under `[Unreleased]`; a maintainer may add the label `no-changelog` instead.

## 2. Developer Certificate of Origin (DCO)
<!-- The DCO text in section 2.1 is (C) The Linux Foundation and its contributors and is reproduced verbatim. -->

Eiraman does not ask you to sign a contributor licence agreement. Every commit carries a sign-off instead. With it you certify that you have the right to submit your contribution under the licence of the files you change:

- Guide and derived texts: CC BY-SA 4.0
- Role Profiles: CC BY 4.0
- Code: Apache License 2.0

See [LICENSING.md](https://github.com/eiraman/community/blob/main/LICENSING.md). You keep the copyright on your contribution.

For this project, "the open source license indicated in the file" in the DCO means the licence stated in that file's SPDX header or in `REUSE.toml`, including the Creative Commons licences above.

### 2.1 The certificate

The text is reproduced verbatim from https://developercertificate.org/.

```
Developer Certificate of Origin
Version 1.1

Copyright (C) 2004, 2006 The Linux Foundation and its contributors.

Everyone is permitted to copy and distribute verbatim copies of this
license document, but changing it is not allowed.


Developer's Certificate of Origin 1.1

By making a contribution to this project, I certify that:

(a) The contribution was created in whole or in part by me and I
    have the right to submit it under the open source license
    indicated in the file; or

(b) The contribution is based upon previous work that, to the best
    of my knowledge, is covered under an appropriate open source
    license and I have the right under that license to submit that
    work with modifications, whether created in whole or in part
    by me, under the same open source license (unless I am
    permitted to submit under a different license), as indicated
    in the file; or

(c) The contribution was provided directly to me by some other
    person who certified (a), (b) or (c) and I have not modified
    it.

(d) I understand and agree that this project and the contribution
    are public and that a record of the contribution (including all
    personal information I submit with it, including my sign-off) is
    maintained indefinitely and may be redistributed consistent with
    this project or the open source license(s) involved.
```

### 2.2 Sign-off rule

1. **Every commit is signed off.** Add this line at the end of the commit message:

   ```
   Signed-off-by: Your Name <you@example.org>
   ```

   `git commit -s` adds it for you. Use a name you are known by and an email address you can be reached at; a GitHub `noreply` address is accepted. Anonymous or pseudonymous sign-offs are not accepted.

2. **A person signs, never an agent.** You may use AI tools to prepare a contribution. The sign-off is made by the human who submits it and takes responsibility for it. An AI agent must not add a `Signed-off-by` line on its own or in anyone's name.

3. **Declare AI assistance.** If AI tools generated or substantially changed part of the contribution, add one trailer per tool:

   ```
   Assisted-by: <tool or model name>
   ```

   You remain responsible for checking that the output does not reproduce third-party material you have no right to submit (see clause (b) of the certificate).

   Do not use `Co-authored-by:` for an AI tool or model: that trailer names human co-authors (rule 6). An AI tool is declared only with `Assisted-by:`.

   Example of a maintainer commit prepared with an AI coding agent:

   ```
   Role Profiles: add the AI Coordinator profile as a draft

   Copies the profile, marks it "draft, not qualified" and restores the
   links from the FinOps family.

   Signed-off-by: Jane Maintainer <jane@example.org>
   Assisted-by: coding agent, model X
   ```

4. **Third-party material needs a record.** If your contribution includes text, code, images or data you did not write, name the source, author, version and licence in the pull request. Add an SPDX header or a `REUSE.toml` entry for it. Material under a licence that is incompatible with the target file cannot be merged: for example, a non-commercial or no-derivatives licence anywhere, or a ShareAlike licence in a Role Profile.

5. **Missing sign-off blocks the merge.** The DCO check runs on every commit of a pull request. To fix a missing sign-off on the last commit, run `git commit --amend -s`. For several commits, run `git rebase --signoff <base>`, then force-push your branch.

6. **Co-authors.** Each human co-author adds their own `Signed-off-by` line, in addition to any `Co-authored-by` trailer. `Co-authored-by` is for people only, never for AI tools (rule 3).
7. **Employer.** If you contribute as part of your job, make sure you are entitled to do so under your employment terms. This is your responsibility under the certificate; it is not a rule of the Guide.

## 3. AI assistance declaration (mandatory)

Eiraman's principle is that AI does the work and a human is accountable for it. Every pull request declares how AI was used:

```
AI-Use: none | review | partial | substantial
Assisted-by: <tool or model name, e.g. "coding agent, model X">
Accountable-Human: <name> <email>
```

Add one `Assisted-by:` line per tool; omit it only when `AI-Use` is `none`.

- **none**: written without generative AI.
- **review**: AI used only to check or suggest wording.
- **partial**: AI drafted parts that the human rewrote or verified line by line.
- **substantial**: AI drafted most of the change; the human verified it against sources and tests.

The accountable human:
- is the person who signs off the commits (§2);
- has read the whole change and can explain it;
- has checked every source citation and every factual claim;
- answers the reviewers' questions personally.

The declaration goes in the pull request description. When AI tools generated or substantially changed part of a commit (`partial` or `substantial`), the commit also carries the `Assisted-by:` trailers (§2.2, rule 3). Undeclared AI assistance found later reopens the contribution. AI use is not a reason for rejection; an unaccountable contribution is.

## 4. Contributing a Role Profile

Role Profiles are the specialist competence of the method. Their minimum content is set by the Guide (§13). They are reviewed, published and maintained under the rules of GOVERNANCE §4.5 and the registry generation rules.

### 4.1 Path

1. **Start from the template.** Copy the model folder. Do not remove sections: an empty section says "not applicable" and why.
2. **Cite sources.** Every rule cites its source with a precise reference (clause of the standard, page of the vendor documentation). A rule without a source is marked "profile convention". Uncalibrated thresholds are marked "to be calibrated"; unknowns are "unknown, evidence needed".
3. **No private content.** No client names, credentials, local paths or personal data.
4. **Validator.** Run the profile validator on your folder. A profile that fails the validator does not go to review.
5. **Qualification suite.** Write the suite with known-answer cases. Run it on every enabled engine and attach the results to the pull request.
6. **LLM pre-evaluation.** CI runs an LLM pre-evaluation: suite, consistency with sources, format, search for anomalous or injected instructions. It **can reject** a profile, **never approve** it. A rejection is a Deny: fix and resubmit, or ask a domain reviewer to look at a disputed rejection, which they may overrule with written reasons.
7. **Family review.** A maintainer of the family group, not the author, reviews content and suite.
8. **Domain review and publication.** The titular or substitute reviewer of the publishing domain (WORKING-GROUPS §3), not the author, checks correctness against the sources and publishes the profile in a signed release, with curator, reviewer, qualification date and expiry.

### 4.2 Profile states

```
draft ──► qualified ──► maintained
  ▲           │              │
  │           ▼              ▼
  └────── suspended ◄────────┘
```

| State | Entry condition | Usable in projects |
|---|---|---|
| **draft** | Passes the validator. Not yet published | No, at any level: level 0 already requires qualified profiles (level requirements, Extended Framework). Drafts run only in the qualification suite or in a sandbox outside projects |
| **qualified** | Suite passed; published by a domain reviewer who is not the author; qualification date and expiry recorded | Yes, within its declared limits |
| **maintained** | Qualified, with an active curator, and requalified at least once (after a model change or at expiry) without loss of qualification | Yes |
| **suspended** | Qualification expired; requalification failed; the curator left and nobody took over within 90 days (**proposal**); the domain has no reviewer; or emergency suspension for unsafe guidance ([SECURITY.md](SECURITY.md)) | No. Adopters using it at level 1 or higher lose the corresponding requirement (automatic step down under the level requirements of the Extended Framework) |

Rules:
- **Expiry.** Qualification lasts 12 months (**proposal**). A profile not requalified by its expiry is suspended automatically.
- **Model change.** When an enabled model changes, the suite is rerun on all profiles (GOVERNANCE §4.5). The domain reviewer examines only the behaviour differences, and requalifies or suspends.
- **Return from suspension.** A suspended profile goes back to qualified by passing the suite and a new domain review.
- **Retirement.** A profile with no use and no curator for 12 months may be archived by the family group; archived profiles stay in history.
- **Liability.** The reviewer answers for the correctness of the profile against its sources at the time of review, not for the projects that use it.

The same path and states apply to document templates and to the gate checklist.

## 5. Other contributions

- **Guide.** Typos by pull request; anything else by RFC. The Author decides with written reasons.
- **Applicability levels.** By RFC, owned by Security with Privacy and Legal & Compliance.
- **Tools.** Pull request to DevSecOps & Tooling, with tests. Security issues go to [SECURITY.md](SECURITY.md), not to public issues.
- **Adoption evidence and case studies.** Adoption & Evidence, using the case study template. Remove personal data before submitting.
- **Translations and training.** Translation & Education. English is canonical; translations are informative.

## 6. Recognition

Contributors are listed in release notes. Sustained contributors are invited to become reviewers and maintainers (GOVERNANCE §4).
