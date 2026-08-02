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

### 1.1 Public salience + Charter filter

CFMI does **not** set its agenda by poll rank alone. Top issues are chosen in two steps:

1. **Public salience** — What large shares of Americans *say* are the biggest national problems, drawn from recent nonpartisan polling (e.g. Gallup most-important-problem, Pew “very big problem” batteries, AP-NORC open-ended government priorities, CBS/YouGov and related). Polling describes stated concerns; it does not establish causal truth or Charter correctness.
2. **Charter filter** — Each salient public label is scored for fit with [CHARTER.md](CHARTER.md): free-market barriers, government overreach, cronyism/rents, constitutional process, and tractability for CFMI’s AI products (score bills, publish conflicts, open fix / sample acts). High public salience with weak Charter fit (e.g. immigration as a lead topic, or raw “crime” theater) stays off the priority agenda **unless remapped**.

**Public-label remapping.** Poll labels are starting points, not product titles. CFMI remaps slogans to Charter mechanisms before scoring fit. Example: public “crime” / “public safety” → **access to justice, anti-corruption, and justice bureaucracy** (civil forfeiture, UPL barriers to affordable legal help, court fee/fine traps, opaque charging and discovery, defender rationing, careful QI/bail mechanism analysis)—not tough-on-crime or defund campaigns. Free markets remain central where entry, prices, and rents are distorted; the deeper through-line is **giving power back to people over government bureaucracy** (published criteria, property and due process, least-coercive transparency, anti-capture).

**Priority score (agenda selection):** Public salience (0–5) × Charter fit (0–5). Within that shortlist, §1’s weighted criteria still rank *projects and bills*.

The working matrix, source links, public-label → issue-slug map, and legislative/regulatory roadblocks live in [`research/public-priorities-charter-matrix.md`](research/public-priorities-charter-matrix.md). The public explanation is [`docs/priorities.html`](docs/priorities.html). Issue briefs are ordered in [`ai-reviews/issues/README.md`](ai-reviews/issues/README.md).

Refresh the matrix when major national poll releases shift the top tier, or when CFMI adds or retires issue briefs.

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

### 2.5 Multi-agent investigation (operating design)

For deeper issue and bill work, CFMI uses a **bounded hierarchical investigation**: one orchestrator agent, six fixed specialist lanes (text/mechanism, root cause, influence, steelman, safeguards, fix language), and depth-limited digs (max 2–3) when Hard Flags fire—not unconstrained agent trees. Root-cause analysis asks whether the design **shifts power to bureaucracy/privileged interests or to accountable people under clear rules** (see architecture). Pipeline, stop conditions, and copy-paste prompts live in [`ops/ai-investigation-architecture.md`](ops/ai-investigation-architecture.md). Human editor gate still applies (§2.4). Influence work remains bound by §7; hidden-barrier analysis by §4.7.

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

### 4.6 Issue briefs: steelman, evidence links, bipartisan comment

Issue briefs (see [`ai-reviews/issues/_brief-template.md`](ai-reviews/issues/_brief-template.md)) are research products that show where government—not open competition—blocks progress. Before a brief is treated as **adoption-ready** (homepage exemplar, sample-act lead-in, or “circulate for bipartisan comment”):

1. **Steelman counters required.** Publish a Counterarguments / defense of status quo section with linked sources. Strawmen fail the test.  
2. **Both-sides evidence links.** Supporting reform and counterarguments must cite papers, agency reports, association statements, or clearly labeled affected-people sources. No fake or unverified links.  
3. **CFMI response.** Weigh both sides against Charter filters and state the least-coercive path—not a party line.  
4. **Passability without Charter breach.** Address legitimate counterarguments in design (narrow scope, evidence thresholds, sunsets, objective criteria). “More likely to pass” never justifies new rents, barriers, or opaque discretion.  
5. **Bipartisan comment path.** Fix language and sample acts circulate for cross-aisle review under §4.4; interest disclosure applies (§5).  
6. **Feedback loop.** Counterevidence and brief-improvement suggestions use the public [counterevidence](.github/ISSUE_TEMPLATE/counterevidence.yml) template and [ops/suggestion-ranking.md](ops/suggestion-ranking.md) §1b so AI-assisted research can update Voices & evidence tables.

Exemplar: [`ai-reviews/issues/occupational-licensing.md`](ai-reviews/issues/occupational-licensing.md).

### 4.7 Looking past talking points — hidden barrier analysis

Crooked anti-free-market problems are often buried. Public narratives (“safety,” “character,” “affordability,” “environment,” “infrastructure”) can be sincere, manufactured, or both. CFMI research—especially AI-assisted problem finding—must separate **what people say** from **what the rulebook does**, and search for operative legal and economic mechanisms that raise rivals’ costs or freeze supply while sounding like public goods.

**Required separation (every issue brief and sample-act problem statement):**

| Layer | Question |
|-------|----------|
| **Public narrative** | What official rationale and talking points dominate hearings, press, and campaign language? |
| **Operative mechanism** | What statute, code, map, fee schedule, timeline, or discretionary standard actually blocks voluntary exchange? |

Do not treat slogans as evidence. Do not assume the narrative is false—steelman it—then test whether the operative design matches the claimed purpose.

**Checklist of common hiding places** (scan every domain; housing is the prototype):

1. **Discretionary standards** — “character,” “compatibility,” “harmony,” “public interest,” “as appropriate,” without published objective criteria.  
2. **Process delay as veto** — sequential reviews, completeness games, endless resubmittals, no deemed-approved shot clock.  
3. **Fees and exactions** — permit fees, impact fees, in-lieu payments structured to price out marginal projects.  
4. **Parking and quantitative minimums** — unit-count, lot-size, setback, or parking floors that freeze density without naming exclusion.  
5. **HOA / covenant overlays** — private restrictions stacked on local ordinances (map both layers).  
6. **Environmental review misuse as entry barrier** — process and litigation risk used to raise rivals’ costs (state-aware: CEQA-style regimes where relevant; do not treat California as the only case or as dogma).  
7. **Growth moratoria and concurrency traps** — temporary freezes or “adequate facilities” tests that never clear for new supply.  
8. **Impact fees as exclusion** — fees that fail nexus/proportionality or that fund general budgets under a growth label.  
9. **“Inclusionary” / affordability rules that tax supply** — set-asides and in-lieu taxes that raise the cost of every new unit while claiming to help affordability.  
10. **Grandfathering incumbents** — existing uses protected; only new entrants face the full barrier stack.  
11. **Opaque variance / waiver markets** — project-specific deals unavailable on equal, published terms.  
12. **State preemption gaps** — state law appears to open entry; local ordinances, design codes, or fees quietly close it.  
13. **Local cartel dynamics (homevoters)** — concentrated homeowner political power protecting scarcity rents; document incentives, not conspiracy narratives.

**Analysis requirements before a brief is adoption-ready:**

1. **Steelman the official rationale** — strongest honest case for the status quo, with linked sources (planning literature, local-government associations, safety or environmental claims).  
2. **Search for who benefits from the status quo** — incumbents, homevoters, permitted rivals, fee-funded agencies; use public filings, maps, prices, and timelines—not motive mind-reading.  
3. **Evidence standard** — statute/code cites, permit timelines, fee schedules, price–cost gaps, production data. Slogans and unverified social posts are not enough.  
4. **Bipartisan frames when both point at artificial scarcity** — include progressive YIMBY / supply evidence and conservative property-rights / anti-exaction frames when both identify the same operative barriers. Reject either side’s ask for new rents, opaque discretion, or named privileges.  
5. **Publish in the brief** — a dedicated **Hidden barriers / buried mechanisms** section (see [`ai-reviews/issues/_brief-template.md`](ai-reviews/issues/_brief-template.md)).

This section applies to **all CFMI issue domains**, not only housing. Licensing boards, CON, water transfers, franchises, and industrial privileges use the same narrative-vs-mechanism discipline.

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

## 7. Influence & Transparency Research

Companion research to bill scores. When a review Hard-Flags rents, barriers, or opaque discretion, CFMI may publish a short **influence memo** that maps **publicly available** disclosure trails to those provisions—and always pairs that map with open fix / alignment language already in the parent review.

Educational/(c)(3)-safe research only. Not private investigation, not counsel to any person, not a vote whip.

### 7.1 Purpose

1. Show readers **who reported lobbying** on bills that contain Charter Hard Flags.  
2. Distinguish **disclosed lobbying** (LDA / OpenSecrets aggregates) from **opaque political spending** (non-disclosing 501(c)(4)/super PAC patterns)—and use “dark money” **only** when that opaque pattern is sourced. Prefer “opaque political spending” when unsure.  
3. Keep exposure tied to **open alternatives** (least-coercive fix language)—never exposure alone.

### 7.2 Sources hierarchy (prefer higher rungs)

| Rank | Source class | Examples |
|------|----------------|----------|
| 1 | Primary public filings | Senate/House LDA reports; FEC filings when cited for independent expenditures |
| 2 | Reputable aggregators of filings | [OpenSecrets / CRP](https://www.opensecrets.org/) bill and client pages |
| 3 | Official legislative record | Congress.gov text, sponsors/cosponsors; committee reports |
| 4 | Authoritative secondary | CRS products when cited by number/title |
| 5 | Company public claims | 10-K / earnings / official press **only** when sourced and labeled as company statements |

If a claim cannot rest on rungs 1–4 (or a clearly labeled rung-5 company statement), write: **“not established from public filings in this pass.”** Do not invent or stretch.

### 7.3 What we publish

- Bill ID, Hard-Flagged provisions (cross-link to the scored review).  
- Organizations that **reported lobbying** on the bill or on named provision themes, with links to OpenSecrets/LDA-style pages.  
- Aggregate client counts when OpenSecrets publishes them (with the usual caveat that LDA “lobbying on” a bill ≠ endorsement of every section).  
- Public statements by trade associations or officials that are on the record.  
- Cross-link to **open fix / alignment language** in the parent review (mandatory).  
- Interest-disclosure reminder for commenters (§5).

### 7.4 What we will not allege

- Private motives, side deals, or “captured the vote” claims without a public-record hook.  
- Doxxing, home addresses, family details, or non-public personal data.  
- Unverified conspiracy narratives or anonymous “sources say” as fact.  
- That disclosed lobbying spending **caused** a specific statutory line—correlation of filings with outcomes is research context, not proof of causation.  
- Defamatory characterizations; attribute to filings (“reported lobbying on H.R. …”; “OpenSecrets lists N clients”).

### 7.5 Separation of layers

| Layer | Content |
|-------|---------|
| **Facts** | Filings, aggregates, bill text, dated public statements |
| **Charter analysis** | Why a provision is a Hard Flag / artificial manipulation |
| **Alternatives** | Open fix language already published with the score |

Never blend motive mind-reading into the facts layer.

**Always keep three claims separate in influence products:**

| Label | Meaning |
|-------|---------|
| **(A) Disclosed financial / organizational interest** | LDA clients & amounts, FEC/OpenSecrets donor industries or PACs, 990 funders, revolving-door employment—sourced and linked |
| **(B) Stated policy reason** | On-the-record public justification (floor remarks, releases, hearings) |
| **(C) Corruption = quid pro quo** | **Not established** unless a public-record chain connects payment/privilege to a specific official act |

### 7.6 Deep public-records layer (mandatory after stated reasons)

After documenting **stated reasons** for each key blocker or advocacy side, investigators **must attempt** a deeper pass over harder-to-find but **publicly available** data. Public statements alone are insufficient for influence claims.

For each key blocker / advocacy side, attempt:

| Check | Sources (examples) |
|-------|-------------------|
| LDA / OpenSecrets clients & amounts on the bill or closely related election bills | [OpenSecrets bill pages](https://www.opensecrets.org/), Senate/House LDA |
| FEC: top donors / PACs to named senators in relevant cycles | [FEC](https://www.fec.gov/) candidate pages · OpenSecrets industry/PAC tables (link both when used) |
| Independent expenditures / opaque (“dark money”) vehicles **if disclosed** | Name the vehicle from filings or reputable aggregator pages; **do not invent** |
| Personal financial disclosures / STOCK Act filings where relevant and findable | Senate/House disclosure portals |
| Nonprofit 990 funders of lead advocacy orgs | [ProPublica Nonprofit Explorer](https://projects.propublica.org/nonprofits/), org-published annual reports / 990s |
| Revolving door: prior employer of staff/sponsors if public | OpenSecrets Revolving Door · bio pages tied to LDA |

If a check yields nothing usable, write **“not established from public filings in this pass”** for that cell—do not pad with quotes.

**Required output table** (influence digs / stall analyses that claim interest-group or corruption angles):

| Actor | Stated reason | Disclosed $ / org ties | Conflict hypothesis | Evidence grade |
|-------|---------------|------------------------|---------------------|----------------|
| … | (B) | (A) | One-sentence hypothesis, labeled as hypothesis | **strong** / **moderate** / **weak** / **not established** |

Evidence-grade meanings: **strong** = multi-source public chain to the contested act; **moderate** = clear disclosed interest + temporal/issue overlap without causation proof; **weak** = aggregate industry or org funding with no act-specific link; **not established** = no public chain (default for quid-pro-quo claims).

Pipeline placement and dig prompts: [`ops/ai-investigation-architecture.md`](ops/ai-investigation-architecture.md) (Deep public-records layer). Publish gate: [`ops/civic-action-pack.md`](ops/civic-action-pack.md) — deep records layer completed before publishing influence claims.

### 7.7 Product placement

- Template: [`ai-reviews/influence-template.md`](ai-reviews/influence-template.md)  
- Companions: `ai-reviews/influence-*.md` linked from parent reviews and [`docs/reviews.html`](docs/reviews.html)  
- Parent bill reviews remain the score of record; influence memos are research companions.

---

## 8. Bootstrap Constraints

Until funded:

- Tools are free-tier only (git hosting, static markdown, free AI tiers as available).  
- Cadence may be irregular; quality and Charter compliance beat volume.  
- Legal formation, tax status, and formal board governance are tracked as open milestones—not implied by this repository alone. **CFMI does not claim any IRS tax-exempt status.**

---

*Methodology version: 0.6.2 (bootstrap) — scoring + conflict publish + open fix language + influence/transparency research + §7.6 deep public-records layer (after stated reasons) + bipartisan sample-act comment + issue-brief steelman / counterevidence loop + §4.7 hidden barrier analysis + §2.5 bounded multi-agent investigation pointer.*
