# Disclosure of relationships to works cited in groups and SEPs

> **This is a proposal, not a filed SEP.** It is written in the SEP template's shape so that this review and
> the eventual SEP review cover the same material. It becomes a SEP only after this Working Group's
> consensus and a Core Maintainer sponsor; no PR exists in the specification repository.
>
> Paths of the form `docs/…`, `seps/…`, and `AI_POLICY.md` refer to
> [`modelcontextprotocol/modelcontextprotocol`](https://github.com/modelcontextprotocol/modelcontextprotocol),
> not to files in this repository.

- **Status**: Draft
- **Type**: Process
- **Created**: 2026-11-20
- **Author(s)**: Kryspin Ziemski <krys&#64;qcomp.io> (@kziemski)
- **Sponsor**: None
- **Issue**: [#2](https://github.com/modelcontextprotocol/governance-wg/issues/2)
- **PR**: this pull request (governance-wg proposal)

## Abstract

Working groups, interest groups and SEPs frequently cite work a participant has an interest in: a draft standard, a conformance corpus, a reference implementation, a product, a paper. The citation is often load-bearing — it can define the problem, supply the pass/fail oracle, or become the basis of an interoperability convention — but no MCP rule requires the person citing it to say they maintain it. This proposal adds one disclosure duty to the group operating rules and to the SEP template: when you cite or propose such a work and you have a relationship to it, state the relationship in one line at the point of citation. A SEP gains a required **References and Disclosures** section, which the Sponsor checks for presence before setting `in-review`. The duty is a statement about the work, not about the person. It creates no conflict, no bar to participation, and no investigative obligation, and it does not change how proposals are judged.

## Motivation

MCP groups routinely evaluate artifacts they did not produce. A domain-specific use case may rest on a test corpus someone else publishes; a security proposal may depend on another organization's format; a specification change may cite an IETF draft, an SDK, or a research paper. Groups need that external work. They also need to know what they are looking at.

Today they cannot, from the record alone. The project discloses two things: AI assistance, per PR, issue or comment (`AI_POLICY.md:5-17`, restated in `docs/community/policies.mdx:22`), and the organization a WG Member lists in the group's member table (`docs/community/working-interest-groups.mdx:91`). Neither addresses the relationship between a participant and a work they cite. A member table says who employs someone; it does not say that the corpus proposed as the definition of conformance is maintained by the person proposing it, or that the product recommended as prior art is sold by their employer.

Three costs follow.

1. **Evidence cannot be weighed for what it is.** A conformance corpus, a reference implementation and an independent analysis carry different weight when deciding whether a design works. Reviewers reconstruct which is which from link text, repository owners and domain knowledge, often incorrectly.
2. **Undisclosed promotion costs the group, not only the proposer.** In a forum where competitors sit together, a proposal that reads as neutral evidence while advancing one implementation's format is a trust problem even when the work is good. The Antitrust Policy already assumes organizational interests are visible (`docs/community/antitrust.mdx:26-39`); the operating rules never ask for them at the point where they matter.
3. **The burden is uneven.** Participants who disclose — "I maintain X, happy to map its fields" — do extra work and expose themselves to being discounted, while a participant who says nothing is treated as disinterested. A rule that asks everyone replaces a norm only the conscientious follow.

The gap is textual, not cultural. WG Members must keep their organization current (`docs/community/working-interest-groups.mdx:91`), and a Core Maintainer resolving an escalated dispute must share no organizational affiliation with the parties (`:111`). Both presuppose known affiliations without creating a duty to state a relationship to a cited work. The SEP template captures name, email, GitHub handle and sponsor, and asks authors to "reference related work or prior art", with no provenance field (`seps/TEMPLATE.md:8-10,45`). There is no PR template and no `CITATION.cff`.

This proposal closes that gap in the smallest way that is checkable: one line at the point of citation, and one required section in a SEP. It deliberately does not decide when a relationship is disqualifying. That question is not answerable by rule, and attempting to answer it would convert a documentation duty into a disciplinary one.

## Specification

### 1. Scope and definitions

Applies in every working group and interest group forum: GitHub issues, pull requests and discussions in project repositories, group meetings, agendas and notes, and the text of SEPs.

**Covered work** means any document, draft or published standard, test corpus or conformance suite, reference implementation, software product, repository, or analysis that is not part of the MCP specification or an official MCP repository. Citations of MCP's own specification, schema, SDKs and project repositories are out of scope.

**Relationship** means any of:

- (a) you authored or co-authored the work, or you maintain it;
- (b) an organization you work for, or advise, owns, funds, publishes or sells it;
- (c) you receive payment, equity, or a commission connected to its adoption;
- (d) you hold a named role in the standards body, project or organization that produces it.

Nothing else counts. Unrelated employment, clients, compensation amounts, revenue and organizational history are outside this section and must not be requested.

### 2. The disclosure duty

1. **Trigger.** When you cite, link, quote or propose a covered work in a group forum, and you have a relationship to it, state the relationship.
2. **Placement.** The statement goes in the same comment, document, agenda item or meeting note as the citation, next to it. One line is enough.
3. **Form.** State the relationship, not the biography:
   - `Disclosure: I maintain X, the corpus cited above.`
   - `Disclosure: I work at Y, which publishes the format proposed here.`
   - `Disclosure: I am an editor of the draft cited in §2.`
   - `Disclosure: I advise Z, which sells the implementation this section recommends.`
   A shorter form is acceptable where the relationship is obvious from the link: `Disclosure: I maintain this.`
4. **No statement required otherwise.** If no relationship applies, say nothing. There is no declaration of disinterest, no "none" line, and no obligation to list unrelated work.
5. **Timing.** The statement is made when the citation is made. A later edit that adds a citation takes the duty with it. There is no duty to revisit earlier comments, and no retroactive application.
6. **Responding to a missing disclosure.** Any participant may ask for one in the thread, and the answer belongs there. Asking is not an accusation: an omission is a documentation gap, resolved by adding the line. Leads may remind a participant. A repeated refusal is a behavioral concern under the existing escalation path (`docs/community/working-interest-groups.mdx:109`), not a new process.

### 3. SEP requirements

1. **Required section.** Every SEP gains a section titled **References and Disclosures**, placed after **Rationale** and before **Backward Compatibility**. It lists each covered work cited in the Abstract, Motivation, Specification or Rationale that any listed author has a relationship to, with the relationship; and, for a work the SEP proposes as a normative reference, conformance oracle or required dependency, who controls changes to that work and how its releases are identified. If no author has such a relationship and no work is proposed as normative, the section reads `None.`
2. **Sponsor check.** Before setting `in-review`, the Sponsor confirms the section is present and non-empty. The Sponsor does not verify its accuracy and does not judge the relationship. The check is mechanical, like the existing confirmation that prior discussion is linked (`docs/community/sep-guidelines.mdx:77`).
3. **Reference implementation.** Where the reference implementation, or a corpus linked from that section, is maintained by an author or their organization, say so in one line.
4. **No effect on the decision.** A disclosed relationship is not a ground for rejection, a reason to discount the proposal, or a factor in the Core Maintainer decision criteria (`docs/community/sep-guidelines.mdx:118`). A SEP may be accepted with every cited work maintained by its authors. What changes is that reviewers know it.

### 4. Limits and non-effects

1. **No conflict finding.** No conflicts of interest, recusal duties, or eligibility rules are created. Existing recusal rules (`docs/community/working-interest-groups.mdx:111`) are unchanged.
2. **No bar to participation.** Disclosing does not limit anyone's participation, and a disclosed relationship must not be used to exclude a participant from discussion of their own work.
3. **No investigation.** No participant is required to research another's interests, and no Lead is required to audit disclosures. The duty is self-declaration.
4. **Antitrust boundary.** Nothing here requires disclosing clients, customers, pricing, margins, pipeline or business plans, and a request for such information in a meeting is already barred (`docs/community/antitrust.mdx:26-39`).
5. **Conduct boundary.** A knowingly false disclosure is a Code of Conduct matter under the existing process. An omitted disclosure is not; it is resolved by asking. No reporting channel and no tribunal are created.
6. **Prospective application.** The duty applies to citations and SEPs created after the change takes effect. Existing SEPs are not amended and prior discussions are not re-opened. An author may add the section voluntarily.
7. **Individual membership unchanged.** Membership remains personal, not organizational (`docs/community/governance.mdx:101`). A disclosed relationship describes a work, not a person's standing.

### 5. Roles, responsibilities, timing

| Role | Responsibility |
|---|---|
| Author or commenter | States the relationship at the point of citation (§2); completes the SEP section (§3.1) |
| SEP Sponsor | Confirms the section is present before `in-review` (§3.2); no accuracy check |
| WG Lead / IG Facilitator | Reminds on omission; may add a disclosure reminder to the agenda template |
| Core Maintainers | Decide the SEP; decide disputes about application |
| Governance WG | Stewards the text and any later amendment |

Effective on merge of the implementing PR. No phase-in, no migration window, no label changes.

## Rationale

### Why a relationship to the work, not a profile of the person

The fact a reviewer needs is narrow: does the person citing this artifact control it? A general affiliation registry would answer that too, at the cost of collecting employment, clients and commercial relationships that the Antitrust Policy discourages in meetings, and that fall unevenly on independents and small vendors. A relationship statement is finite, checkable, and stays about the work.

### Why not prohibit self-citation

The people who know an external format best are usually the people who build it. Excluding them removes the expertise the groups need and pushes the same advocacy into private channels. Disclosure keeps the expertise and makes the interest visible.

### Why the SEP check is presence, not truth

A Sponsor cannot verify authorship claims, and asking them to try creates an investigation duty with no capacity behind it. Presence is mechanical, cheap, and enough to force the question into the record. Truth is governed by the Code of Conduct, as with every other statement a contributor makes.

### Alternatives considered

- **Ordinary pull request.** Not available: the WG/IG rules were adopted by SEP-2149 and "changing them requires a Process SEP" (`docs/community/working-interest-groups.mdx:6`), and the SEP process itself can only be changed by a Process SEP (`docs/community/sep-guidelines.mdx:6`).
- **Informational SEP.** Cannot create a duty or a template field, and the documentation change would still need a Process SEP. It produces guidance nobody is asked to follow.
- **Mandatory affiliations field for all participants.** Rejected: conflicts with individual membership (`docs/community/governance.mdx:101`), collects commercial data, and imposes a cost on everyone to answer a question that arises only at a citation.
- **Code of Conduct amendment.** Rejected: the CoC is incident-based and punitive; this is a documentation duty with one mechanical check. Routing it through the CoC would make every omitted line look like misconduct.
- **Extending `AI_POLICY.md`.** Rejected as the vehicle: that policy is about tooling, not commercial relationship, and merging the two blurs a rule that currently works. Its shape is borrowed instead: one line, in the thread, with extent.
- **Charter template `Organization` column only.** Rejected: directory data, updated rarely, and per-group charters cannot override shared rules.
- **A neutrality rule for normative artifacts.** The stronger claim — that the project should not adopt a conformance oracle controlled by one participant without change-control guarantees — is a real problem and is deliberately out of scope. This proposal requires only that the control relationship be stated (§3.1). A separate proposal should address change control, forkability and hosting.

### Anticipated objections

- *"This will be used to discredit vendors."* Answered by §4.1-4.2: no conflict finding, no bar, and an explicit statement that a disclosed relationship does not discount the argument.
- *"It is unenforceable."* Partly true, and accepted: one gate is mechanical, the rest is a norm with a documented way to ask. A rule followed most of the time and pointable-to beats an unwritten norm followed only by the conscientious.
- *"It adds process to a heavy process."* The required section can be the word `None.` No new labels, no new fields, no new review stage.
- *"Why not just ask in the thread?"* Asking works, and the rule keeps asking available. What it adds is that the answer belongs in the record without anyone having to make an accusation first.

### Evidence of consensus

This issue thread and the WG meeting notes where the proposal is discussed are the consensus record. Objections raised there are added here as they are made.

## Backward Compatibility

No existing documentation or SEP is invalidated. Existing SEPs keep their text and status; the required section applies to SEPs created after the change takes effect. No labels, tooling or schema change. `npm run generate:seps` runs after the template edit; `check:seps` is unaffected.

## Security Implications

No protocol surface, no code path, no data handling change.

Two social risks are worth stating. First, a disclosure rule can be turned into a demand for personal information; §1 and §4.4 bound what may be asked to the relationship with a cited work and exclude clients, compensation and business plans. Second, a missing disclosure can be treated as evidence of bad faith; §2.6 and §4.5 make a missing line a documentation gap resolved by asking, and reserve the conduct question for a knowingly false statement. Participants who contribute pseudonymously may satisfy §2 by naming the relationship and the organization that controls the work, without disclosing unrelated employment.

## Reference Implementation

Four edits in the specification repository, in the same PR:

- `docs/community/working-interest-groups.mdx` — new section "Disclosure of relationships to cited works", inserted between Participation levels and Making decisions.
- `docs/community/sep-guidelines.mdx` — the section check in workflow step 6, and one clause in **Review and acceptance** so a disclosure is not a decision criterion.
- `seps/TEMPLATE.md` — the required **References and Disclosures** section, and the one-line note in **Reference Implementation**.
- `docs/community/policies.mdx` — one index entry pointing at the rule.

This follows SEP-1850 and SEP-2149, which implemented their process changes in the same pull request. A worked example — three citations, one self-maintained corpus, one employer product, one with no relationship — goes in the PR description as the reviewable artifact.

No conformance scenario is required: Process SEPs are exempt (`docs/community/sep-guidelines.mdx:128`).

## Open Questions

1. **Binding Core Maintainers.** Doing so moves the text into `docs/community/governance.mdx`, which triggers the SEP-2085 amendment procedure — Lead Maintainer proposal authority and a two-thirds Core Maintainer vote. The draft does not, and relies on the norm applying to everyone. Decide before a SEP is opened.
2. **IG meeting notes.** Should the meeting-notes template carry a standing reminder line? Cheap, but a per-group operational choice under `docs/community/working-interest-groups.mdx:115`; it need not be normative.
3. **Time bound.** Should §2.6 set a deadline for answering a request for disclosure, or leave it to the group's existing discussion norms?
4. **Trigger breadth.** Does "cite, link, quote or propose" cover the cases the WG cares about, or is there a category of reference — for example, a competitor's published benchmark — that needs its own treatment?

## Appendix A — Normative text under review

The two sections the WG is being asked to endorse. Formatting and links are final in the implementing PR; wording is what matters here.

**`docs/community/working-interest-groups.mdx`, new section**

> ## Disclosure of relationships to cited works
>
> Groups evaluate work they did not produce: drafts, conformance corpora, reference implementations, products, analyses. When you cite or propose such a work and you have a relationship to it, say so in the same comment, document, agenda item or meeting note. One line is enough, and it describes the work, not you.
>
> You have a relationship when you authored or co-authored the work, maintain it, work for or advise an organization that owns, funds, publishes or sells it, receive payment or equity connected to its adoption, or hold a named role in the body that produces it. Employment on unrelated matters, clients, compensation and business plans are not covered and must not be asked for; the Antitrust Policy already bars exchanging them in meetings.
>
> Examples: `Disclosure: I maintain X, the corpus cited above.` `Disclosure: I work at Y, which publishes this format.` If no relationship applies, say nothing; there is no declaration of disinterest. The duty applies when the citation is made and is not retroactive.
>
> Anyone may ask for a missing disclosure in the thread, and the answer belongs there. Asking is not an accusation: an omission is a documentation gap, not misconduct. A knowingly false statement is handled under the Code of Conduct; an omission is handled by asking, then by the existing escalation path.
>
> A disclosed relationship is not a conflict of interest, a recusal duty, or a reason to discount a proposal. It does not limit anyone's participation, and no one is required to investigate another participant's interests. Reviewers weigh the argument.

**`seps/TEMPLATE.md`, new section between Rationale and Backward Compatibility**

> ## References and Disclosures
>
> **Required for every SEP.** List each work cited in the Abstract, Motivation, Specification or Rationale that an author has a relationship to, and state the relationship: authored or maintained by an author, owned, funded, published or sold by an organization an author works for or advises, payment or equity connected to its adoption, or a named role in the body that produces it. For a work the SEP proposes as a normative reference, conformance oracle or required dependency, also state who controls changes to it and how its releases are identified.
>
> If no author has a relationship to a cited work and no work is proposed as normative, write `None.` The sponsor confirms this section is present before setting `in-review`; the sponsor does not verify it. A disclosed relationship is not a ground for rejection and does not discount the proposal.

## Appendix B — Files changed by the implementing PR

| File | Change |
|---|---|
| `docs/community/working-interest-groups.mdx` | New section (§2) |
| `docs/community/sep-guidelines.mdx` | Step 6 check; one clause in Review and acceptance |
| `seps/TEMPLATE.md` | Required section; one line in Reference Implementation |
| `docs/community/policies.mdx` | Index entry under standing policies |
