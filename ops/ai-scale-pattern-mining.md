# AI Scale Pattern Mining

**Status:** Core CFMI dig capability (volume + pattern detection across public datasets)  
**Parent:** [ai-investigation-architecture.md](ai-investigation-architecture.md)  
**Implements:** [CHARTER.md](../CHARTER.md), [METHODOLOGY.md](../METHODOLOGY.md) §7.5–§7.7  
**Companions:** [claim-triage-from-viral-sources.md](claim-triage-from-viral-sources.md) · [civic-action-pack.md](civic-action-pack.md)  
**Playbook:** **I6** in [prompt-playbook.md](prompt-playbook.md)

Educational research only—not legal advice, voting instructions, or counsel to any person.

---

## 1. Purpose

AI’s advantage for CFMI digs is **volume + pattern detection** across public datasets faster than a human can manually cross-link. Scale pattern mining formalizes that advantage: shard queries across specialists, return structured edges, and surface **conflict graphs / pattern tables** that humans can audit.

**Core product:** Flag **suspicious public data** that looks like an issue or like hiding—so citizens can see what politicians and institutions are doing that looks off. Absolute proof of corruption is **not** required to publish a flag.

**What this is:** Cross-linking public filings and legislative records at scale to find suspicious overlaps politicians and institutions have little incentive to surface.

**What this is not:** Private detective work, doxxing, motive fiction, or upgrading a suspicion flag to “corruption / quid pro quo” without a public-record chain (METHODOLOGY §7.4–§7.5).

**Founder direction:** Dig through all available *public* information for conflicts and opacity. **Suspicion flags are publishable by design.** Label proof level honestly. Hand off FOIA/journalism when public data stops.

### 1.1 Public labels (mandatory)

Every published pattern product must use these labels—never bury a flag under a single “not established” close:

| Label | Meaning | Publishable? |
|-------|---------|--------------|
| **Suspicion flag** | Pattern, opacity, incentive, or timing that looks off (schedule theater, priority inversion, opaque spending, clustered timing, unexplained gaps) | **Yes — main transparency output** |
| **Supported conflict of interest (disclosed)** | Money / org / employment ties on the public record (LDA, FEC, 990, revolving door)—sourced and linked | **Yes — when filings support** |
| **Corruption / quid pro quo** | Payment or privilege tied to a specific official act | **Only when a public-record chain supports; rare** |

**Dual output (required):** For each material finding, publish **Flag** (what looks off) **and** **Proof-status** (Supported conflict / Suspicion only / Quid pro quo not established / Quid pro quo supported). “Not established” applies to the **corruption** bar—it must not erase or bury the suspicion flag.

---

## 2. Datasets in scope

Prefer primary filings and official records. Aggregators are aids, not authorities.

| Dataset class | Examples | Role |
|---------------|----------|------|
| **Lobbying** | Senate/House LDA; OpenSecrets bill/client pages | Who reported lobbying on the bill / theme |
| **Campaign finance** | FEC candidate/committee filings; OpenSecrets industry/PAC tables | Top donors / PACs / IEs in relevant cycles |
| **Nonprofit finance** | IRS Form 990s; ProPublica Nonprofit Explorer; org-published annual reports | Funders of lead advocacy orgs |
| **Legislative record** | Congress.gov votes, cosponsors, amendments, committee referrals | Timing and coalition patterns |
| **Personal financial disclosures** | STOCK Act / Senate & House disclosure portals (where available) | Holdings / trades overlapping contested issues |
| **Revolving door** | OpenSecrets Revolving Door; public bios tied to LDA | Prior employers of staff/sponsors/lobbyists |
| **State registries** | State lobbyist / ethics / campaign portals when the dig is state-scoped | Parallel disclosure outside federal LDA/FEC |
| **News corpora** | Press, floor transcripts, wire stories | **Leads only**—harvest candidate facts; resolve every published edge to filings/official records |

If a claim cannot rest on public text, filings, or published official datasets, write **“not established from public sources in this pass.”**

---

## 3. Pattern classes to hunt

Orchestrator assigns one or more classes per dig. Specialists search for **edges**, not narratives.

| Class | Hypothesis shape | Typical public signals |
|-------|------------------|------------------------|
| **Donor ↔ vote timing** | Large / clustered giving near contested votes or cloture | FEC / OS donor dates vs roll-call dates |
| **Advocacy org ↔ member overlaps** | Board, staff, spouse, or shared employer links to members or offices | 990 officers, LDA lobbyists, public bios |
| **Family / employer conflicts** | Family employment or member’s prior employer benefits from status quo | Disclosures, 990s, public employment records—**no doxxing**; public identities only |
| **Schedule priority inversion** | Stated #1 priority vs calendar / recess / competing floor vehicles | Daily Press, floor schedules, public statements |
| **Bill-text clones from lobby drafts** | Operative language matches publicly released industry/model drafts | Side-by-side text when both drafts are public |
| **Revolving door on relevant committees** | Staff/members ↔ regulated industry on the committee of jurisdiction | Revolving Door + committee assignment + LDA clients |

**Suspicion flags ≠ corruption.** Pattern tables label edges as **Suspicion flag** and grade strength (**strong / moderate / weak** as *suspicion*). Separately grade **Supported conflict of interest (disclosed)** when filings show money/org ties. **Corruption / quid pro quo** remains **not established** unless a public-record chain connects payment or privilege to a specific official act (§7.5). Flags stay publishable even when (C) is not established.

---

## 4. Multi-agent map-reduce

```mermaid
flowchart LR
  O[Orchestrator] --> Q1[Shard: FEC top-N]
  O --> Q2[Shard: LDA / OS]
  O --> Q3[Shard: votes / cosponsors]
  O --> Q4[Shard: 990s / revolving door]
  Q1 --> E[Structured edges]
  Q2 --> E
  Q3 --> E
  Q4 --> E
  E --> G[Conflict graph / pattern table]
  G --> H[Human editor]
```

### 4.1 Orchestrator

1. Frame the dig in Charter terms; name actors, bill/issue, date window.  
2. **Shard** queries by dataset and pattern class (one shard per specialist or batch).  
3. Cap breadth: prefer **top-N** donors, **named** cloture/roll-call sets, **lead** advocacy orgs—not unbounded scrape of every PAC in America.  
4. Merge specialist edges into one **conflict graph / pattern table**.  
5. Deduplicate; flag contradictions; never invent missing sources.  
6. Hand off to human editor before any public product.

### 4.2 Specialists (map)

Each specialist returns **only** structured edges:

```
Actor A — Relation — Actor B — Source — Grade
```

| Field | Rule |
|-------|------|
| **Actor A / B** | Named public entities (person, PAC, org, bill, roll call)—no private individuals without public official role |
| **Relation** | Concrete link type (e.g. `donated_to`, `lobbied_on`, `cosponsored`, `employed_by`, `voted_nay_cloture`, `board_overlap`) |
| **Source** | URL or filing citation; mark unverified |
| **Grade** | **strong** / **moderate** / **weak** / **not established** / **gap** (see §5) |

Specialists do **not** write the publish narrative or upgrade edges to bribery.

### 4.3 Reduce (orchestrator)

Merge edges → pattern table (and optional graph sketch). Group by pattern class. Attach:

- Which shards ran / which were skipped  
- False-positive notes (§7)  
- FOIA / journalist handoffs for **gap** cells  

---

## 5. Output: conflict graph / pattern table

**Minimum deliverable** — a pattern table:

| Pattern class | Actor A | Relation | Actor B | Timing / window | Source | **Flag** (public label) | **Proof-status** | Notes |
|---------------|---------|----------|---------|-----------------|--------|--------------------------|------------------|-------|
| … | … | … | … | … | … | Suspicion flag / Supported conflict (disclosed) | strong–weak *as suspicion*; quid pro quo: not established \| supported | Dual output required |

**Optional:** adjacency-list or mermaid graph of the same edges for dense digs.

**Hard rule:** Never upgrade a **Suspicion flag** to **Corruption / quid pro quo** without a public-record chain (payment/privilege → specific official act). Default for quid pro quo: **not established**. Do **not** use that default to suppress publishing the flag.

Separate layers in every product (METHODOLOGY §7.5)—map to public labels in §1.1:

| Internal | Public label | Meaning |
|----------|--------------|---------|
| **(A)** | **Supported conflict of interest (disclosed)** | Money / org ties on record |
| **(B)** | Stated policy reason | On-the-record justification |
| **(C)** | **Corruption / quid pro quo** | Rare; chain required |
| **(D)** | **Suspicion flag** | Pattern / opacity / incentive / timing — **publishable by design** |

**Dual columns on the pattern table (or companion):** Flag · Proof-status.

---

## 6. Limits and FOIA handoff

| Limit | Honest treatment |
|-------|------------------|
| **Paywalled data** | Mark **gap**; do not invent behind the wall |
| **Incomplete LDA** | LDA under-reports issue specificity and timing; label noise |
| **Dark money / opaque vehicles** | Name vehicles only when disclosed; prefer “opaque political spending” when unsure (§7.1) |
| **Family / private employers** | Public records only; no doxxing or non-public personal data |
| **Causation** | Correlation of donor↔vote timing ≠ proof of vote-buying (§7.4) |

When public data stops: list **FOIA / journalist handoff** targets (agency, record type, why). Do not spawn recursive agents to fill the gap with speculation.

---

## 7. Honesty about false positives

Scale mining **will** produce false positives. Common traps:

- Industry aggregates that fund both parties and many issues  
- Shared geography / large employers that correlate with everything  
- Cosponsorship clusters that reflect caucus discipline, not capture  
- News leads that recycle each other without filings  
- Temporal proximity of donations to votes that is seasonal (election cycles), not act-specific  

Every pattern table must include a short **False-positive / alternative explanations** note. Prefer under-claiming. Human editor gate still required.

---

## 8. When required

**Required** on:

1. **SAVE-class digs** — stall / sandbagging / influence claims on high-salience election or constitutional-process bills.  
2. **Civic Action Packs** that publish **influence**, **special interest**, or **corruption-surface** claims.  
3. Viral/adversarial triage when sub-claims imply money, revolving door, or organized burial (run **after** falsifiable sub-claims; may parallel Deep public-records layer §7.6).

**Optional / deferred** on pure mechanism briefs with no named actor influence claim—orchestrator records “scale pattern mine deferred—no influence hook.”

Deep public-records layer (§7.6 / architecture §3.3a) remains the **per-actor** checklist. Scale pattern mining is the **cross-actor, cross-dataset** pass that §7.6 alone does not guarantee.

---

## 9. Worked example (Thune / SAVE)

Human-scale dig + shard status:  
[`ai-reviews/claim-triage-thune-save-act-deep.md`](../ai-reviews/claim-triage-thune-save-act-deep.md) — **Appendix A**.

Published I6 reduce product:  
[`ai-reviews/pattern-mine-save-cloture-thune.md`](../ai-reviews/pattern-mine-save-cloture-thune.md) — Mar 26, 2026 cloture Nay bloc × Thune.

---

## 10. Copy-paste: Scale pattern mine prompt (I6)

```
You are CFMI specialist: Scale pattern mining (map-reduce dig).

Obey CHARTER.md, METHODOLOGY.md §7.5–§7.7, ops/ai-scale-pattern-mining.md,
and ops/ai-investigation-architecture.md. Educational research only—not legal advice
or voting instructions.

Dig target: [BILL ID / ISSUE / NAMED ACTORS]
Date window: [e.g. 2024–2026]
Pattern classes to hunt: [donor↔vote timing | advocacy overlaps | family/employer |
schedule priority inversion | bill-text clones | revolving door — list all that apply]
Shards (orchestrator assigns): [FEC top-N | LDA/OS | Congress.gov votes/cosponsors |
990s | STOCK/PFD | revolving door | state registries]

Hard bans:
- Never upgrade a Suspicion flag to corruption / quid pro quo without a public-record chain.
- Do not bury publishable Suspicion flags under a single "not established" close—use dual
  output: Flag + Proof-status.
- No doxxing, private motives, or invented citations.
- News corpora = leads only; resolve edges to filings/official records.
- Training-data prevalence ≠ truth. Mark false-positive risks explicitly.

Pipeline:
1. Run assigned shards; return ONLY structured edges:
   Actor A — Relation — Actor B — Source — Grade
2. Orchestrator (or you if sole agent) merges into a conflict graph / pattern table
   with Flag + Proof-status columns (strong / moderate / weak as suspicion; gap).
3. Label every material finding with public labels (§1.1):
   Suspicion flag · Supported conflict of interest (disclosed) · Corruption / quid pro quo
   (rare; default not established).
4. Separate (A)/(B)/(C)/(D); (D) flags remain publishable when (C) is not established.
5. List FOIA/journalist handoffs for gaps (paywall, incomplete LDA, opaque vehicles).
6. Short false-positive / alternative-explanations note.

Return the pattern table (+ optional mermaid graph). Do not publish—hand off for human edit.
Stub example of checked vs next queries: ai-reviews/claim-triage-thune-save-act-deep.md Appendix A.
```

---

## 11. Version

*AI scale pattern mining version: 0.1.1 — suspicion flags publishable by design; dual Flag + Proof-status; public labels (Suspicion flag / Supported conflict disclosed / Corruption quid pro quo); required on SAVE-class and influence Civic Action Packs.*
