# Governance Working Group Governance

The Governance Working Group operates under a lightweight, consensus-driven governance model aligned with the broader MCP community and the [Working and Interest Groups](https://github.com/modelcontextprotocol/modelcontextprotocol/blob/main/docs/community/working-interest-groups.mdx) documentation.

## Principles

1. **Open Participation** — Anyone can participate regardless of affiliation
2. **Transparency** — All decisions are documented and publicly accessible
3. **Consensus-Driven** — The group seeks agreement; objections prompt discussion
4. **Antitrust Compliance** — All activities follow the [MCP Antitrust Policy](https://github.com/modelcontextprotocol/modelcontextprotocol/blob/main/ANTITRUST.md)
5. **Ecosystem Alignment** — Work aligns with broader MCP goals, values, and specifications

## Roles

### Lead

The current Lead serves an interim term of no more than one year from the charter approval date. The Lead is responsible for:

- Coordinating working sessions and setting agendas
- Representing the working group at the monthly Core Maintainer plus WG/IG leads meeting
- Surfacing community concerns to Core Maintainers in an advisory capacity
- Prioritising proposals and managing the group's review queue
- Landing editorial revisions to governance docs with documented rationale
- Proposing roadmap items and charter amendments
- Managing repository and community health

**Current Lead:**

| Name | Organization | GitHub | Term |
|------|--------------|--------|------|
| Sarah Novotny | Independent (contract Anthropic) | [@sarahnovotny](https://github.com/sarahnovotny) | Interim, NTE 1-year |

Sponsored by David Soria Parra ([@dsp-ant](https://github.com/dsp-ant)).

### WG Members

WG Members are the voting body of the group. To become a WG Member:

1. Participate consistently for at least 3 months
2. Make meaningful contributions (governance doc drafting, reviews, or discussion facilitation)
3. Be nominated by an existing WG Member or the Lead
4. Receive no objections from Leads, Core Maintainers, or Lead Maintainers within 7 days

**Current WG Members:**

| Name | Organization | GitHub | Discord | Level |
|------|--------------|--------|---------|-------|
| Sarah Novotny | Independent (contract Anthropic) | [@sarahnovotny](https://github.com/sarahnovotny) | @sarahnovotny | Lead |
| Andreas Schlapbach | TBD | [@schlpbch](https://github.com/schlpbch) | | WG Member |
| Lin Sun | Solo.io | [@linsun](https://github.com/linsun) | | WG Member |
| Peder Holdgaard Pedersen | Saxo Bank / MCP Maintainer & Community Moderator | [@PederHP](https://github.com/PederHP) | @pederhp | WG Member |
| Kryspin Ziemski | QCOMPUTE | [@kziemski](https://github.com/kziemski) | | WG Member |

No more than 2 Leads may come from any single organisation. This invariant is maintained throughout each term.

### Active Contributors

Active contributors regularly participate in discussions, sessions, or documentation work. They:

- Have demonstrated sustained engagement
- May receive triage permissions
- Are recognized in this document

**Current Active Contributors:**

_None yet — get involved!_

### Contributors

Anyone who participates in any way:

- Joining Discord discussions
- Attending working sessions
- Opening or commenting on issues
- Submitting pull requests
- Reviewing proposals

No formal approval is needed to become a contributor.

## Decision Making

The group uses **lazy consensus** as its default decision mechanism, falling back to a formal vote when consensus cannot be reached:

1. **Proposal** — Ideas are raised via GitHub issues, PRs, or working sessions
2. **Discussion** — Open discussion in Discord and GitHub
3. **Consensus** — The group seeks agreement; silence implies consent
4. **Objection Resolution** — Objections trigger further discussion until resolved
5. **Documentation** — All decisions are recorded in meeting notes or GitHub

### Authority & Decision Rights

| Decision Type | Authority Level |
|---------------|-----------------|
| Meeting logistics & scheduling | Lead (autonomous) |
| WG roadmap and review-queue submissions | Lead (autonomous) |
| Proposal prioritisation within WG | Lead (autonomous) |
| Editorial revisions to existing governance docs (typos, clarifications, link fixes) | Lead (autonomous, with documented rationale) |
| Substantive revisions to existing governance docs | WG consensus → Core Maintainer approval |
| New governance policy or new doc under `docs/community/` | WG consensus → Core Maintainer approval |
| Changes to a page owned outside this WG | Proposed to that owner; owner decides |
| Code of Conduct content revision | WG consensus → Core Maintainer approval |
| Code of Conduct individual incident handling | Out of scope (handled elsewhere) |
| Contributor ladder structural changes | WG consensus → Core Maintainer approval + community comment period |
| Onboarding & mentorship culture and practice docs | WG consensus (autonomous) |
| Surfacing community concerns to Core Maintainers | WG consensus (advisory; non-binding) |
| Scope expansion | Core Maintainer approval required |
| Amendments to the charter | WG consensus → Core Maintainer approval |
| WG Member approval | WG Member sponsors (subject to org-diversity cap) |

The "editorial vs. substantive" line is intentionally narrow: typos, clarifications, broken-link fixes, and rewordings that do not change meaning are editorial. Anything that changes the meaning, scope, or applicability of an existing rule is substantive.

Pull request creation on the specification repository is limited to maintainers. WG Members who are not maintainers draft governance doc changes from a fork or a WG-owned repository; a maintainer in the WG opens the pull request and names the author.

## Leadership Succession

When a Lead seat opens — the interim term ends, a Lead steps down, or the WG agrees to add a seat — the WG selects future Leads as follows:

1. Any WG Member may self-nominate or be nominated by another WG Member
2. Candidates must meet the Lead requirements in the working and interest groups documentation, and the group's leadership must retain sponsorship from at least two Core Maintainers or one Lead Maintainer
3. Selection is by WG consensus using the standard decision-making process, then ratified by Core Maintainers as a charter amendment
4. The org-diversity invariant is enforced at selection time

## Meeting Requirements

All working sessions must include:

- Published agenda in `#governance-wg` at least 48 hours in advance when items are known
- Open attendance for all participants
- Notes posted to the `Meeting Notes - Governance WG` Discussions category

The monthly working session is a standing slot and is not cancelled for lack of an agenda. If three consecutive sessions draw neither attendance nor agenda items, the Lead proposes a reduced cadence or retirement to the Core Maintainers.

## Amendments

Governance changes require:

1. Proposal via GitHub issue, PR, or working session
2. WG consensus
3. Core Maintainer approval
4. Documented rationale for the change, recorded in the charter's changelog

## Contact

Questions about governance can be directed to:

- The `#governance-wg` Discord channel
- GitHub Issues in this repository
- Current Leads and WG Members directly
