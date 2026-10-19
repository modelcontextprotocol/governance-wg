# Epic records for multi-SEP efforts

**Proposal:** [`proposals/epic-records-for-multi-sep-efforts.md`](../proposals/epic-records-for-multi-sep-efforts.md) · **Author:** Kryspin Ziemski ([@kziemski](https://github.com/kziemski))

_Citations of `docs/…`, `seps/…`, and `.github/…` refer to `modelcontextprotocol/modelcontextprotocol`, not to this repository._

**Problem.** MCP tells authors to split large proposals — "Consider whether your change might be too large - could it be split into smaller SEPs?" (`docs/community/contributing.mdx:564`) — and offers no artifact to hold the pieces, so the coupling between sibling SEPs lives in meeting notes and Discord. The roadmap's composition review asks three WGs to make Tasks and Triggers "compose cleanly with each other" (`docs/development/roadmap.mdx:35`), yet nothing records those efforts' membership, coordination, or done criteria.

**The gap, stated so you can call it wrong.** For a bounded, cross-cutting effort spanning more than one SEP — especially more than one Working Group — no artifact carries all seven of: the single outcome, the non-goals, the member SEPs, the dependencies between them, a coordinator, done criteria, and durability past a roadmap rewrite. I am *not* claiming early alignment is missing: pre-SEP direction requests already use the existing queue with a written artifact ([#3407](https://github.com/modelcontextprotocol/modelcontextprotocol/discussions/3407), 2026-09-30). I claim only that the post-direction record does not exist. `seps/1302-formalize-working-groups-and-interest-groups-in-mc.md:84` already names the unit — "a specific SEP, themed series of SEPs". If a WG charter or a `tracking` issue can already hold these seven items across WGs, tell me and I will withdraw this.

**The capability, plainly.** An Epic would be a durable, citable record of one outcome:

- **Outcome** — the single outcome the member SEPs together deliver.
- **Scope** — explicit non-goals, not only goals.
- **Membership** — the member SEPs, declared; a declaration, never a gate.
- **Dependencies** — which members constrain which, and the consequence of withdrawal or rejection.
- **Coordinator** — an existing authority (WG Lead or Maintainer); no new role.
- **Done criteria** — the observable condition for completion, on which the record closes.
- **Lifecycle** — proposed, active, complete, abandoned; abandonment carries a recorded reason.
- **Non-authority** — it must not gate, rank, delay or block any individual SEP. Precedence: roadmap > WG roadmap > epic > individual SEP.
- **Boundedness** — two or more SEPs; if it reduces to one, it is withdrawn and that SEP proceeds alone.
- **Discoverability** — a stable identifier and a location reachable from each member SEP.

**Staged, not standardizing ahead of use.** This proposes the capability, not a carrier. First use is the Tasks effort (SEP-1686 + SEP-2663), recorded from material that already exists, plus one in-flight effort; if that shows no use, the idea is dropped and no carrier SEP gets filed. That sequencing is deliberate — it is the stance the Core Maintainers took on SEP-2084 rather than an argument against it.

**What this is not.** Not a new SEP status — the status table stays untouched. Not a new approval gate. Not a merge or dissolution of any working group. Not roadmap authority. Not a re-litigation of primitive grouping or of SEP-2084.

**Questions where your input changes the draft:**

1. Mechanism: a `Type: Epic` preamble value, a `tracking`-labelled issue form, a `seps/epics/` index, or a column in the generated SEP index — which is least costly, if any?
2. Must the coordinator be an existing authority, or may any sponsor hold it?
3. Should an already-merged multi-SEP effort (e.g. Tasks, SEP-1686 + SEP-2663) be recordable retroactively, or forward only?
4. What should the abandonment record contain beyond a reason?

**Prior art we are aware of.** `seps/1302-formalize-working-groups-and-interest-groups-in-mc.md:84` names "themed series of SEPs". The `tracking` label tracks agreed work but is explicitly "not a new proposal" (`.github/ISSUE_TEMPLATE/work_tracking.yml:2-4`). A2A has eight `[Epic]`-titled issues (#1986–#1992, #1995, created 2026-06-25, all still open) — an uncodified convention, not a model to copy. And `#993 → #1300 → #2084` are three attempts at one problem with no shared record.
