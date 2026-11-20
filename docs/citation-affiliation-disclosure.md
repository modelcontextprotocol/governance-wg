# Citation-affiliation disclosure — one page for discussion

Discussion summary for [issue #2](https://github.com/modelcontextprotocol/governance-wg/issues/2). The full proposal is [`proposals/citation-affiliation-disclosure.md`](../proposals/citation-affiliation-disclosure.md). Not a filed SEP.

## The problem in three sentences

Groups evaluate artifacts they did not produce — corpora, reference implementations, vendor formats, drafts — and the citation is often load-bearing: it can define the problem or become the pass/fail oracle. MCP requires disclosure of AI assistance and of the organization in a WG Member's directory entry, and nothing else. So a reviewer cannot tell from the record whether the person proposing a corpus as the definition of conformance maintains that corpus.

## The rule

1. **In groups:** when you cite or propose a covered work and you have a relationship to it (author/maintainer, employer or advised org controls it, payment or equity tied to adoption, named role in the producing body), say so in one line at the point of citation. Otherwise say nothing.
2. **In SEPs:** a required **References and Disclosures** section after Rationale. It may be the word `None.` For an artifact proposed as a normative or conformance oracle, also state who controls changes to it. The Sponsor checks presence before `in-review`, not accuracy.
3. **Limits:** no conflict finding, no recusal, no bar to participation, no investigation duty, prospective only. A missing line is resolved by asking; only a knowingly false statement is a CoC matter.

## What it does not do

- It does not make an oracle neutral. If a corpus controlled by one participant is proposed as the definition of conformance, disclosure makes the interest visible but does not settle change control, pinning, forkability or hosting. That is a separate proposal and should stay separate.
- It does not characterize any past discussion. It applies to citations made after it takes effect.
- It does not collect affiliations, clients, compensation, or business plans; the Antitrust Policy already bars that in meetings.

## Decisions needed from the WG

| # | Decision | Default in the draft |
|---|---|---|
| 1 | In scope, and a sponsor? | No sponsor yet |
| 2 | Does the duty also belong in the charter template's meeting/notes requirements? | `working-interest-groups.mdx` only |
| 3 | Bind Core Maintainers explicitly? | No — that moves the text to `governance.mdx` and triggers SEP-2085 (Lead Maintainer proposal, 2/3 CM vote) |
| 4 | Is `None.` acceptable as the SEP default? | Yes |
| 5 | Is "cite, link, quote or propose" the right trigger? | Yes, with the four relationship classes |

## Why a Process SEP

The WG/IG rules were adopted by SEP-2149 and change only by Process SEP (`working-interest-groups.mdx:6`); the SEP process likewise (`sep-guidelines.mdx:6`); "a governance or process change" is SEP-worthy (`sep-guidelines.mdx:16`). The Governance WG charter covers it: it stewards those pages and "may sponsor a SEP that changes a governance process".

Implementation is four documentation edits in one PR — no schema, no labels, no new review stage — as SEP-1850 and SEP-2149 did. Process SEPs are exempt from the conformance gate.

## If the WG wants this faster

Two smaller options, both weaker:

- **Guidance only.** Publish the norm on the WG page without a SEP. No duty, no SEP section, no enforcement, and the operating rules are untouched. Cheap, and probably ignored.
- **Template section only.** Add `References and Disclosures` to the SEP template without touching the group rules. Covers SEPs, not the IG/issue discussion where most citations happen.

The draft keeps both surfaces because the citation problem is the same in both places, and because a rule that only binds SEP authors leaves the discussion threads — where evidence is first presented — uncovered.
