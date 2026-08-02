# Claim Triage from Viral Sources

**Status:** Operating lane for CFMI AI research  
**Parent:** [ai-investigation-architecture.md](ai-investigation-architecture.md)  
**Companion:** [anti-narrative-capture.md](anti-narrative-capture.md)  
**Implements:** [CHARTER.md](../CHARTER.md), [METHODOLOGY.md](../METHODOLOGY.md) §4.7, §7.5–§7.6  
**Publish gate:** [civic-action-pack.md](civic-action-pack.md)

Educational research only—not legal advice, voting instructions, or counsel to any person.

---

## 1. Founder method (why this lane exists)

One of the best ways to find **real** issues is to treat conspiracy theories, influencer threads, and viral public claims as **leads**—then dig for **actual** links in public records. Neither believe nor dismiss out of hand.

| Viral / conspiracy / influencer claim | CFMI treatment |
|---------------------------------------|----------------|
| Social post, streamer segment, chain email, “everyone knows” narrative | **Lead / hypothesis** — not evidence |
| Disclosed filing, statute, audit, court record, agency dataset | **Evidence candidate** — grade after check |

**Rule:** High-virality is a signal to *investigate*, not a reason to *amplify* or to *dismiss*.

**Adversarial pass required:** Do **not** treat leadership or institutional **self-description** (“we lack the votes,” job-title explanations, press-release process stories) as a sufficient close. Start from critical/conspiracy leads; hunt suspicious public data (schedule gaps, priority inversion, rhetoric vs action timeline); grade suspicion flags separately from proven corruption / quid pro quo. Example product: [`ai-reviews/claim-triage-thune-save-act-deep.md`](../ai-reviews/claim-triage-thune-save-act-deep.md).

---

## 2. Hard bans

Agents **must not**:

1. **Launder rumor into CFMI voice** — Quoting or paraphrasing an unverified viral claim as if CFMI established it.  
2. **Reflexive dismissal** — “That’s a conspiracy theory, so it’s false” without a records pass. Labeling a claim *viral* or *conspiratorial* is taxonomy, not a falsification.  
3. **Authority laundering (either side)** — Closing the question by citing institutional press releases *or* influencer consensus.  
4. **Motive fiction** — Inferring private bribes, secret cabals, or intent without a public-record chain (METHODOLOGY §7.4–§7.5).

When evidence is thin: **“not established from public sources in this pass.”** Do not fill gaps with belief or scorn.

---

## 3. Pipeline

Run in order. Skip a step only with an explicit note.

| Step | Action | Output |
|------|--------|--------|
| 1 | **Collect claim** | Verbatim quote; source URL/date; who originated or amplified (public identity only) |
| 2 | **Extract falsifiable sub-claims** | Split slogans into checkable propositions (who / what / when / where / how much) |
| 3 | **Steelman both sides** | Strongest honest case for mainstream denial **and** for the claim (mechanisms, not vibes) |
| 4 | **Deep public-records dig** | METHODOLOGY §7.5–§7.6 / architecture §3.3a on each sub-claim that implies influence, corruption, or official misconduct |
| 5 | **Grade each sub-claim** | Supported / Partially supported / Not established / Contradicted |
| 6 | **Handoffs** | FOIA targets, journalist tips, or “stop—no public chain” when records do not exist publicly |

Depth caps and stop conditions match [ai-investigation-architecture.md](ai-investigation-architecture.md) §3.3–§3.4. Human editor gate before any public product.

### 3.1 Grades (per sub-claim)

| Grade | Meaning |
|-------|---------|
| **Supported** | Multi-source public chain (filings, primary text, published datasets) establishes the proposition as stated |
| **Partially supported** | Public records support a narrower or related fact; the full viral framing does not follow |
| **Not established** | No adequate public chain in this pass—default for corruption = quid pro quo |
| **Contradicted** | Public records affirmatively refute the proposition as stated |

Grades are **per sub-claim**, not a single vibe score for the whole thread.

---

## 4. Required dual steelman

Before grading, every triage pass must produce:

1. **Steelman of mainstream denial** — Best mechanism-based case that the claim is wrong, overstated, or outside what audits/records can show.  
2. **Steelman of the claim** — Best mechanism-based case that something real is being pointed at (even if the viral framing is wrong).

If either steelman is missing, the pass is incomplete. Do not pick a team.

---

## 5. Required output structure

```
1. Origin claim (quoted verbatim + source/date)
2. Claim type: viral | influencer | conspiracy-framed | mixed
3. Falsifiable sub-claims (numbered)
4. Steelman — mainstream denial (mechanisms + sources)
5. Steelman — the claim (mechanisms + sources)
6. What would need to be true for the strongest sub-claim to hold
7. What records would prove it (named filing types / agencies / datasets)
8. What was checked (table: check → result → grade)
9. Per-sub-claim grades: Supported | Partially supported | Not established | Contradicted
10. Separation: (A) disclosed interest · (B) stated reason · (C) quid pro quo — default not established
11. Open FOIA / journalist handoffs (or “none—public chain exhausted”)
12. CFMI publish stance: may cite graded facts only; must not amplify unverified framing
13. Recommendation: CLOSE | NARROW publish of [supported facts] | ESCALATE dig on [target] | HAND OFF FOIA/journalism
```

### 5.1 Civic Action Pack field (optional)

When a dig started from a viral lead, the pack may include:

| Field | Content |
|-------|---------|
| **Origin claim** | Short quote + link (labeled as lead, not CFMI finding) |
| **Triage grades** | Per-sub-claim grades from this lane |

See [civic-action-pack.md](civic-action-pack.md) §2.

---

## 6. Orchestrator integration

1. If intake is a viral/influencer/conspiracy-framed claim **or** Stage 2 surfaces one that would short-circuit analysis, spawn this lane (or run playbook **I5**).  
2. May run **alongside** Consensus claim tester ([anti-narrative-capture.md](anti-narrative-capture.md)) when the claim is also high-consensus—tester stresses “secure/unsafe” framing; this lane grades **falsifiable sub-claims** against records.  
3. Synthesis may publish only **Supported** / carefully labeled **Partially supported** facts. **Not established** and **Contradicted** viral framing stays out of CFMI voice.  
4. Human editor gate still required.

See [ai-investigation-architecture.md](ai-investigation-architecture.md) §3.2b.

---

## 7. Worked example (SAVE / election space — method only)

**Origin claim (illustrative, not endorsed):** A viral post asserts that “Senate stalling on the SAVE Act proves senators are paid by open-borders lobbies to keep non-citizens on the rolls.”

**Falsifiable sub-claims (examples):**

| # | Sub-claim | Records dig | Typical grade pattern |
|---|-----------|-------------|------------------------|
| 1 | Named senators reported lobbying contacts / disclosed donors tied to immigration or election NGOs | LDA, OpenSecrets, FEC, 990s (§7.6) | Often **Partially supported** (disclosed ties exist) or **Not established** (no bill-specific chain) |
| 2 | Those disclosures **caused** a hold or vote | Public-record causation chain | Almost always **Not established** (correlation ≠ causation—§7.4) |
| 3 | Non-citizens are registered or voted at a stated scale in a named jurisdiction | Audit reports, court findings, state datasets | Grade only what the named source measures; do not import national slogans |
| 4 | “Everything is stolen / rolls are fake” as outcome conspiracy | Mechanism + audits (anti-narrative-capture) | **Not established** or **Contradicted** unless a specific public chain exists |

**What would need to be true (for #2):** A public trail linking a specific payment or privilege to a specific official act on the bill.  
**What records would prove it:** Indictment/plea, verified communication + contemporaneous official act, or equivalent public adjudication—not industry aggregate totals.  
**CFMI stance:** May publish the Actor | Stated reason | Disclosed $ table with evidence grades; must **not** amplify the viral “paid to steal elections” framing. Hand off FOIA/journalism where filings stop.

This example shows **triage method**. It does not endorse election-fraud theories or claim any senator committed bribery.

---

## 8. Copy-paste: Viral claim triage prompt

```
You are CFMI specialist: Viral / conspiracy claim triage (parallel lane).

Obey CHARTER.md, METHODOLOGY.md §4.7 and §7.5–§7.6, ops/claim-triage-from-viral-sources.md,
and ops/anti-narrative-capture.md. Educational research only—not legal advice or voting instructions.

Origin claim (quote exactly):
"[CLAIM]"

Source / date: [URL or description]
Scope: [jurisdiction / bill / process facet]
Depth: [0 | 1 | 2]

Hard bans:
- Do not launder rumor into CFMI voice.
- Do not dismiss as false merely because it is labeled a conspiracy theory.
- No private motives or quid pro quo without a public-record chain.
- Training-data prevalence ≠ truth.

Pipeline:
1. Extract falsifiable sub-claims.
2. Steelman mainstream denial AND steelman the claim.
3. Deep public-records dig (§7.6) on each sub-claim that implies influence or misconduct.
4. Grade each: Supported | Partially supported | Not established | Contradicted.
5. State what would need to be true; what records would prove it; what was checked;
   FOIA/journalist handoffs when public records do not exist.

Return ONLY the structured block in ops/claim-triage-from-viral-sources.md §5.
Mark gaps "not established from public sources in this pass."
Do not write the final publish package.
```

---

## 9. Version

*Claim-triage-from-viral-sources version: 0.1.1 — viral claims as leads; adversarial pass required (no leadership self-description close); falsifiable sub-claims; dual steelman; §7.6 grades; no rumor laundering / no reflexive dismissal.*
