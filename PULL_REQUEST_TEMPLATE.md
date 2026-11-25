<!--
Draft. One logical change per pull request (CONTRIBUTING §1).
Exploitable vulnerabilities and unsafe guidance go to private reporting (SECURITY.md), not here.
-->

## What and why

<!-- One or two sentences. What changes, for whom, and why. -->

Closes #<issue>  ·  RFC: <guide/rfcs/NNNN-title.md, or "not needed: two-way door">

Area: <!-- guide | framework | role-profiles/<family> | tools | site | community -->

## Linked evidence

<!-- A contribution closes only on an identifiable commit with all mandatory checks passed (GOVERNANCE §1). Link what proves it. -->

- [ ] Issue or RFC linked above
- [ ] Sources cited with precise references (clause, section, page), or marked "profile convention" / "to be calibrated" / "unknown, evidence needed"
- [ ] **Role Profiles:** validator output attached, Section 10 catalogue regenerated, qualification suite results attached for every enabled engine
- [ ] **Tools:** tests added or updated, including a negative case
- [ ] **Evidence from real projects:** anonymised per CASE-STUDY-TEMPLATE, Privacy reviewer requested
- [ ] Not applicable items explained below

Evidence links (CI run, suite results, data):

-

## AI assistance declaration (mandatory)

<!-- CONTRIBUTING §3. AI use is not a reason for rejection; an unaccountable contribution is. -->

```
AI-Use: none | review | partial | substantial
Assisted-by: <tool or model name>
Accountable-Human: <name> <email>
```

<!-- One Assisted-by line per tool; omit it only when AI-Use is none. -->

<!-- Commit trailers for an AI-assisted commit (CONTRIBUTING §2.2): the human signs off, the tool is declared
     with Assisted-by. Never use Co-authored-by for an AI tool or model.

     Signed-off-by: Jane Maintainer <jane@example.org>
     Assisted-by: coding agent, model X
-->

- [ ] I am the accountable human: I have read the whole change, I can explain it, and I have checked every source citation and factual claim
- [ ] For `partial` or `substantial`, the commits concerned also carry the `Assisted-by:` trailers, and no `Co-authored-by:` trailer names an AI tool

## DCO sign-off

- [ ] Every commit carries `Signed-off-by:` with the real name and email of the human who certifies the right to submit it under the project licences (`git commit -s`). No AI system or bot signs off
- [ ] If I contribute as part of my job, I am entitled to do so under my employment terms

## Four-eyes review

<!-- The author is never the reviewer. AI review tools may comment but never count as a reviewer. -->

- Requested reviewer (not the author): @<handle>
- For Role Profiles, templates or the gate checklist, publishing domain reviewer (WORKING-GROUPS §3): @<handle>
- Additional reviewers required by the area (Security for signing, secrets or CI permissions; Privacy for project classes or personal data; two native speakers for translations): @<handle>

If a required reviewer or check is unavailable, this pull request stays open and the reason is recorded here:

## Conflict of interest

<!-- GOVERNANCE §8. Employer, vendor relationships, consulting, training or certification interests related to this change. -->

none / <declaration>

## States

<!-- Maintainers set these labels. Passing one never implies the others. -->

- Technical: checks and review on the final commit
- Acceptance: recorded by the owner of the artifact (lazy consensus or RFC decision)
- Publication: included in a signed release with manifest
