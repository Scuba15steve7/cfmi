# Methodology  
## Constitutional Free Markets Institute (CFMI)

This document explains how CFMI uses research-funded, rules-bound AI to score current legislation; publish conflicts with Charter goals; provide open fix and alignment language; and circulate sample legislation for bipartisan review and comment. It implements [CHARTER.md](CHARTER.md).

Public products are educational and research outputs. They are not legal advice, voting instructions, or counsel to any person.

---

## 1. How Problems Are Ranked

Problems—especially those that distort free markets or stretch constitutional limits—are ranked by a published score. Higher priority work comes first.

| Criterion | Weight | Question |
|-----------|--------|----------|
| **Constitutional stakes** | 25% | Does the status quo stretch enumerated powers, federalism, separation of powers, or property/contract protections? |
| **Market distortion** | 25% | How large and durable are artificial barriers, subsidies, or opaque discretion? |
| **Corruption / rent surface** | 20% | How easy is political allocation or capture relative to open competition? |
| **Tractability** | 15% | Can a least-coercive, rules-based fix or alignment language be drafted and audited? |
| **Spillover & precedent** | 10% | Would a good fix or sample act travel to other states or domains? |
| **Evidence quality** | 5% | Are harms documented with public data, not anecdotes alone? |

**Disqualifiers (do not take the project):**

- Primary goal is to obtain a subsidy, barrier, or privilege for a private interest.
- Solution requires federal commandeering of states.
- Solution depends on open-ended agency discretion without objective criteria.
- CFMI cannot publish methods and drafts openly.

Rankings for active pipelines will be logged in-repo when the pipeline has more than one active track.

---

## 2. Scoring Current Legislation and Publishing Conflicts

### 2.1 Purpose

AI-assisted review scores proposed or enacted legislation against Charter principles. It flags language that expands discretion, creates barriers, enables rents, or otherwise conflicts with free markets and constitutional limits. Reviews publish those conflicts with section hooks and offer open fix or alignment language where salvageable. They do **not** replace legal counsel or constitute advice to any individual on how to vote.

### 2.2 Rubric (0–5 each; higher = more aligned with Charter)

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

### 2.3 Review output format

Each review must include:

1. Bill identification (title, Congress/session or state, sponsors if known)  
2. One-paragraph summary  
3. Dimension scores + short justification with **quoted or paraphrased section hooks**  
4. **Conflicts with Charter goals** — explicit list of where the bill conflicts with free markets, constitutional limits, or anti-capture filters  
5. Hard Flags list  
6. **Open fix / alignment language** — amendment sketches or substitute clauses that would reduce Hard Flags without creating new rents (not legal advice)  
7. Disclosure: model/provider (if known), rubric version, date, human editor  

See [`ai-reviews/sample-bill-review-template.md`](ai-reviews/sample-bill-review-template.md).

### 2.4 Human control

A named human editor accepts, revises, or rejects AI draft reviews before publication. Disagreements with AI scores are noted in the review.

---

## 3. Open Fix and Alignment Language

When a scored bill has salvageable sections or clear Hard Flags:

1. **State the conflict** — Quote or paraphrase the offending hook; cite the Charter principle.  
2. **Offer open language** — Publish redline-style or substitute clauses that align the text with free markets and constitutional limits.  
3. **Least-coercive first** — Prefer clarifying rights, narrowing discretion, sunsets, and publication duties over new programs.  
4. **No rent packages** — Fix language must not introduce subsidies, entry barriers, opaque discretion, or named privileges.  
5. **Public by default** — Fix packs live in-repo with the review version that produced them.

---

## 4. Sample Legislation and Bipartisan Comment

### 4.1 Drafting sequence

1. **Problem statement** — One page: who is harmed, by what rule or practice, with sources.
2. **Constitutional basis** — Enumerated power (if federal) or state authority; federalism constraints; non-preemption defaults.
3. **Free-market impact** — What competition, entry, and property rights change; what rents are removed or risk being created.
4. **Least-coercive options** — Rank: clarify rights → lower barriers to voluntary exchange → narrow, rules-based incentives → only then limited new authority.
5. **Operative text** — Definitions, rights, procedures, transparency, severability, non-preemption / anti-commandeering.
6. **Safeguards** — Unintended consequences section; farmer/consumer/rural protections where relevant; anti-capture clauses.

### 4.2 Pressure tests (mandatory before “v1 public”)

| Test | Pass condition |
|------|----------------|
| **Rent test** | No section creates a transferable privilege available only to named classes without objective, open criteria. |
| **Discretion test** | Approval standards are published and objective; “public interest” alone is insufficient. |
| **Capture test** | Donors/allies gain no unique benefit from the bill’s structure. |
| **Federalism test** | No commandeering; preemption is express, narrow, and justified—or absent. |
| **Transparency test** | Key decisions, transfers, and waivers are public and machine-readable where feasible. |
| **Exit test** | Parties can decline voluntary programs without punishment beyond loss of the optional benefit. |

Failed tests require revision or an explicit, published rationale for residual risk.

### 4.3 Required front matter on sample bills

Every sample bill ships with:

1. Free-Market Impact Statement  
2. Constitutional Basis Statement  
3. Unintended Consequences & Safeguards  

Templates live in [`docs/`](docs/).

### 4.4 Bipartisan circulation and open comment

Sample legislation is published for **bipartisan review and comment**—education and research, not a closed caucus draft.

1. **Publish** a dated draft in-repo (version tag).  
2. **Circulate openly** to stakeholders across the aisle, practitioners, and analysts with a clear ask: Charter-tied redlines + interest disclosure.  
3. **AI-assisted research loop** — Use disclosed feedback and public bill text to refine prompts, checklists, and drafts (clarity, technical workability, fewer side effects). Log material prompt/rubric changes.  
4. **Comment quality over vote-counting** — Edits may improve readability, narrow scope, add sunsets, or reduce unintended consequences. CFMI does not treat “more likely to pass” as a reason to abandon Charter filters.  
5. **Hard limit** — Feedback that requests subsidies, entry barriers, opaque discretion, or named privileges is **rejected**, even if bipartisan. Comment fitness never outranks the Charter.  
6. **Conflict exposure** — Where feedback or research reveals conflicts that block honest fixes, publish them (with sources) as research—not as personal attack content.

### 4.5 Minimizing unintended consequences

Before “circulate v1” and before “comment-ready”:

- Complete the Unintended Consequences template with likelihood/severity/mitigation.  
- Prefer narrower operative text, objective criteria, sunsets, and reporting over broad grants of power.  
- Recheck after each major comment round; bump PATCH/MINOR accordingly.

---

## 5. Stakeholder Feedback Rules

1. **Interest disclosure is mandatory.** Commenters state employment, client relationships, subsidies received, or other material interests related to the subject within the prior 24 months.
2. **Score against principles.** Feedback is evaluated by whether it advances Charter principles—not by volume, status, party, or donation size.
3. **No pay-for-play.** Financial support does not entitle a donor to undisclosed edits.
4. **Public by default.** Substantive feedback on public drafts may be summarized in-repo; private lobbying for rents is declined.
5. **Reject rent-seeking asks.** Requests for subsidies, barriers, or exclusive privileges are recorded as declined when a public log exists.
6. **Bipartisan welcome.** Comment from any party or none is welcome under the same disclosure and Charter filters.

---

## 6. Version Control and Public Audit

1. All charter-level docs, methodology, sample bills, and published reviews live in git (or equivalent public VCS).  
2. Semantic versions on sample bills: `MAJOR.MINOR.PATCH` (breaking policy / additive / typo-clarification).  
3. Tagged releases for donor-facing “frozen” snapshots.  
4. AI rubric changes bump the rubric version string cited in reviews.  
5. Deletions of published analysis require a tombstone note explaining why (legal risk, factual error)—not silent erasure of history; use git history.  
6. When financially able, CFMI will mirror releases to an independent archive.

---

## 7. Bootstrap Constraints

Until funded:

- Tools are free-tier only (git hosting, static markdown, free AI tiers as available).  
- Cadence may be irregular; quality and Charter compliance beat volume.  
- Legal formation, tax status, and formal board governance are tracked as open milestones—not implied by this repository alone. **CFMI does not claim any IRS tax-exempt status.**

---

*Methodology version: 0.3.0 (bootstrap) — scoring + conflict publish + open fix language + bipartisan sample-act comment.*
