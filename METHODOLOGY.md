# Methodology  
## Constitutional Free Markets Institute (CFMI)

This document explains how CFMI chooses problems, drafts legislation, pressure-tests bills, runs AI reviews, and accepts feedback. It implements [CHARTER.md](CHARTER.md).

---

## 1. How Problems Are Ranked

Problems are ranked by a published score. Higher priority work comes first.

| Criterion | Weight | Question |
|-----------|--------|----------|
| **Constitutional stakes** | 25% | Does the status quo stretch enumerated powers, federalism, separation of powers, or property/contract protections? |
| **Market distortion** | 25% | How large and durable are artificial barriers, subsidies, or opaque discretion? |
| **Corruption / rent surface** | 20% | How easy is political allocation or capture relative to open competition? |
| **Tractability** | 15% | Can a least-coercive, rules-based fix be drafted and audited? |
| **Spillover & precedent** | 10% | Would a good fix travel to other states or domains? |
| **Evidence quality** | 5% | Are harms documented with public data, not anecdotes alone? |

**Disqualifiers (do not take the project):**

- Primary goal is to obtain a subsidy, barrier, or privilege for a private interest.
- Solution requires federal commandeering of states.
- Solution depends on open-ended agency discretion without objective criteria.
- CFMI cannot publish methods and drafts openly.

Rankings for active pipelines will be logged in-repo when the pipeline has more than one active track.

---

## 2. How Legislation Is Drafted and Pressure-Tested

### 2.1 Drafting sequence

1. **Problem statement** — One page: who is harmed, by what rule or practice, with sources.
2. **Constitutional basis** — Enumerated power (if federal) or state authority; federalism constraints; non-preemption defaults.
3. **Free-market impact** — What competition, entry, and property rights change; what rents are removed or risk being created.
4. **Least-coercive options** — Rank: clarify rights → lower barriers to voluntary exchange → narrow, rules-based incentives → only then limited new authority.
5. **Operative text** — Definitions, rights, procedures, transparency, severability, non-preemption / anti-commandeering.
6. **Safeguards** — Unintended consequences section; farmer/consumer/rural protections where relevant; anti-capture clauses.

### 2.2 Pressure tests (mandatory before “v1 public”)

| Test | Pass condition |
|------|----------------|
| **Rent test** | No section creates a transferable privilege available only to named classes without objective, open criteria. |
| **Discretion test** | Approval standards are published and objective; “public interest” alone is insufficient. |
| **Capture test** | Donors/allies gain no unique benefit from the bill’s structure. |
| **Federalism test** | No commandeering; preemption is express, narrow, and justified—or absent. |
| **Transparency test** | Key decisions, transfers, and waivers are public and machine-readable where feasible. |
| **Exit test** | Parties can decline voluntary programs without punishment beyond loss of the optional benefit. |

Failed tests require revision or an explicit, published rationale for residual risk.

### 2.3 Required front matter on model bills

Every model bill ships with:

1. Free-Market Impact Statement  
2. Constitutional Basis Statement  
3. Unintended Consequences & Safeguards  

Templates live in [`docs/`](docs/).

### 2.4 Circulation, feedback, and passage fitness

Sample legislation is meant to be **sent to interested parties** for critique and iteration.

1. **Publish** a dated draft in-repo (version tag).  
2. **Circulate** to stakeholders, legislators’ offices, practitioners, and aligned analysts with a clear ask: Charter-tied redlines + interest disclosure.  
3. **AI-assisted training loop** — Use disclosed feedback and public bill text to refine prompts, checklists, and drafts (improve clarity, coalition fit, and technical workability). Log material prompt/rubric changes.  
4. **Passage fitness** — Edits may improve readability, narrow scope, add sunsets, or reduce unintended consequences to raise honest adoption odds.  
5. **Hard limit** — Feedback that requests subsidies, entry barriers, opaque discretion, or named privileges is **rejected**, even if it would increase votes. Passage fitness never outranks the Charter.  
6. **Corruption / conflict exposure** — Where feedback or research reveals conflicts that block solutions, publish them (with sources) as part of removing barriers—not as personal attack content.

### 2.5 Minimizing unintended consequences

Before “circulate v1” and before “adoption-ready”:

- Complete the Unintended Consequences template with likelihood/severity/mitigation.  
- Prefer narrower operative text, objective criteria, sunsets, and reporting over broad grants of power.  
- Recheck after each major feedback round; bump PATCH/MINOR accordingly.

---

## 3. How AI Reviews Existing Bills (change or defeat)

### 3.1 Purpose

AI-assisted review scores proposed or enacted legislation against Charter principles. It flags language that expands discretion, creates barriers, enables rents, or otherwise works **against** CFMI’s goals. Reviews support **amendment, narrowing, or defeat** of bad legislation and identification of salvageable sections. They do **not** replace legal counsel or constitute advice to any individual on how to vote.

### 3.2 Rubric (0–5 each; higher = more aligned with Charter)

| Dimension | 0 | 3 | 5 |
|-----------|---|---|---|
| **A. Enumerated / limited power** | Open-ended national police power | Debatable but bounded claim | Clear textual hook + limits |
| **B. Federalism** | Commandeering or blunt preemption | Conditional spending / partial preemption | Respects states; competition preserved |
| **C. Property & contract** | Weakens titles/contracts without compensation path | Mixed | Strengthens clear rights + remedies |
| **D. Free entry & competition** | New barriers or incumbent shelter | Neutral | Lowers artificial barriers |
| **E. Discretion & opacity** | Broad waiver / “as appropriate” governance | Some standards | Objective criteria + publication |
| **F. Rent / privilege** | Creates or expands transferable political rents | Ambiguous | Removes or blocks rents |
| **G. Least coercion** | New bureaucracy first | Mixed toolkit | Prefer rights, markets, sunsets |

**Composite:** Average of A–G.  
**Flags:** Any dimension ≤ 1 is a **Hard Flag**. Any “artificial manipulation” match (see Charter definition) is a **Hard Flag**.

### 3.3 Review output format

Each review must include:

1. Bill identification (title, Congress/session or state, sponsors if known)  
2. One-paragraph summary  
3. Dimension scores + short justification with **quoted or paraphrased section hooks**  
4. Hard Flags list  
5. Least-coercive alternative sketch (not a full substitute bill unless commissioned)  
6. Disclosure: model/provider (if known), rubric version, date, human editor  

See [`ai-reviews/sample-bill-review-template.md`](ai-reviews/sample-bill-review-template.md).

### 3.4 Human control

A named human editor accepts, revises, or rejects AI draft reviews before publication. Disagreements with AI scores are noted in the review.

---

## 4. Stakeholder Feedback Rules

1. **Interest disclosure is mandatory.** Commenters state employment, client relationships, subsidies received, or other material interests related to the subject within the prior 24 months.
2. **Score against principles.** Feedback is evaluated by whether it advances Charter principles—not by volume, status, or donation size.
3. **No pay-for-play.** Financial support does not entitle a donor to undisclosed edits.
4. **Public by default.** Substantive feedback on public drafts may be summarized in-repo; private lobbying for rents is declined.
5. **Reject rent-seeking asks.** Requests for subsidies, barriers, or exclusive privileges are recorded as declined when a public log exists.

---

## 5. Version Control and Public Audit

1. All charter-level docs, methodology, model bills, and published reviews live in git (or equivalent public VCS).  
2. Semantic versions on model bills: `MAJOR.MINOR.PATCH` (breaking policy / additive / typo-clarification).  
3. Tagged releases for donor-facing “frozen” snapshots.  
4. AI rubric changes bump the rubric version string cited in reviews.  
5. Deletions of published analysis require a tombstone note explaining why (legal risk, factual error)—not silent erasure of history; use git history.  
6. When financially able, CFMI will mirror releases to an independent archive.

---

## 6. Bootstrap Constraints

Until funded:

- Tools are free-tier only (git hosting, static markdown, free AI tiers as available).  
- Cadence may be irregular; quality and Charter compliance beat volume.  
- Legal formation, tax status, and formal board governance are tracked as open milestones—not implied by this repository alone.

---

*Methodology version: 0.2.0 (bootstrap) — circulation / passage-fitness limits / live-bill defense clarified.*
