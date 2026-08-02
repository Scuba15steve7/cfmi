# Claim Triage from Viral Sources

**Status:** Operating lane for CFMI AI research  
**Parent:** [ai-investigation-architecture.md](ai-investigation-architecture.md)  
**Companions:** [anti-narrative-capture.md](anti-narrative-capture.md) · [ai-scale-pattern-mining.md](ai-scale-pattern-mining.md)  
**Implements:** [CHARTER.md](../CHARTER.md), [METHODOLOGY.md](../METHODOLOGY.md) §4.7, §7.5–§7.7  
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

**Adversarial pass required:** Do **not** treat leadership or institutional **self-description** (“we lack the votes,” job-title explanations, press-release process stories) as a sufficient close. Start from critical/conspiracy leads; hunt suspicious public data (schedule gaps, priority inversion, rhetoric vs action timeline). Example product: [`ai-reviews/claim-triage-thune-save-act-deep.md`](../ai-reviews/claim-triage-thune-save-act-deep.md).

**Publishable by design:** Absolute proof of corruption is **not** required to publish. Core output = **suspicion flags** so citizens can scrutinize what looks off. Use public labels (METHODOLOGY §7.5 / [ai-scale-pattern-mining.md](ai-scale-pattern-mining.md) §1.1):

| Public label | Role |
|--------------|------|
| **Suspicion flag** | Pattern / opacity / incentive / timing — main transparency product |
| **Supported conflict of interest (disclosed)** | Money/org ties on the public record |
| **Corruption / quid pro quo** | Only when a public-record chain supports; rare |

**Dual output:** Every graded finding → **Flag + Proof-status**. Do not bury flags under a single “not established” close—“not established” is the corruption bar, not a reason to hide the pattern.

**Scale pattern mining (when money / burial / revolving-door sub-claims appear):** After falsifiable sub-claims, run [ai-scale-pattern-mining.md](ai-scale-pattern-mining.md) / playbook **I6**—cross-link FEC, LDA, OpenSecrets, 990s, votes/cosponsors, and related public sets into a conflict graph / pattern table. Suspicion flags ≠ quid pro quo. Required on SAVE-class digs.

---

## 2. Hard bans

Agents **must not**:

1. **Launder rumor into CFMI voice** — Quoting or paraphrasing an unverified viral claim as if CFMI established it.  
2. **Reflexive dismissal** — “That’s a conspiracy theory, so it’s false” without a records pass. Labeling a claim *viral* or *conspiratorial* is taxonomy, not a falsification.  
3. **Authority laundering (either side)** — Closing the question by citing institutional press releases *or* influencer consensus.  
4. **Motive fiction** — Inferring private bribes, secret cabals, or intent without a public-record chain (METHODOLOGY §7.4–§7.5).

When evidence for a **sub-claim** is thin: **“not established from public sources in this pass.”** Do not fill gaps with belief or scorn. When a **suspicion pattern** exists but quid pro quo does not: still publish the **Suspicion flag** with Proof-status = quid pro quo not established (dual output).

---

## 3. Pipeline

Run in order. Skip a step only with an explicit note.

| Step | Action | Output |
|------|--------|--------|
| 1 | **Collect claim** | Verbatim quote; source URL/date; who originated or amplified (public identity only) |
| 2 | **Extract falsifiable sub-claims** | Split slogans into checkable propositions (who / what / when / where / how much) |
| 3 | **Steelman both sides** | Strongest honest case for mainstream denial **and** for the claim (mechanisms, not vibes) |
| 4 | **Deep public-records dig** | METHODOLOGY §7.5–§7.6 / architecture §3.3a on each sub-claim that implies influence, corruption, or official misconduct |
| 4a | **Scale pattern mine** *(when required)* | Cross-actor map-reduce per [ai-scale-pattern-mining.md](ai-scale-pattern-mining.md) / §7.7 — conflict graph / pattern table; SAVE-class or influence/burial claims |
| 5 | **Grade each sub-claim** | Supported / Partially supported / Not established / Contradicted |
| 6 | **Handoffs** | FOIA targets, journalist tips, or “stop—no public chain” when records do not exist publicly |

Depth caps and stop conditions match [ai-investigation-architecture.md](ai-investigation-architecture.md) §3.3–§3.4. Human editor gate before any public product.

### 3.1 Grades (per sub-claim)

| Grade | Meaning |
|-------|---------|
| **Supported** | Multi-source public chain (filings, primary text, published datasets) establishes the proposition as stated |
| **Partially supported** | Public records support a narrower or related fact; the full viral framing does not follow |
| **Not established** | No adequate public chain in this pass—default for corruption = quid pro quo; does **not** erase a separate Suspicion flag with its own Proof-status |
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
10. Dual output table: Flag | Proof-status
    — Flag = Suspicion flag and/or Supported conflict (disclosed)
    — Proof-status = strong/moderate/weak as suspicion or disclosed tie;
      quid pro quo: not established | supported
11. Separation: (A) Supported conflict (disclosed) · (B) stated reason ·
    (C) Corruption/quid pro quo (default not established) · (D) Suspicion flag (publishable)
12. Open FOIA / journalist handoffs (or “none—public chain exhausted”)
13. CFMI publish stance: may publish Flags + Proof-status; must not amplify unverified
    viral framing as established corruption; must not bury Flags under “not established”
14. Recommendation: CLOSE | NARROW publish of [Flags + supported facts] |
    ESCALATE dig on [target] | HAND OFF FOIA/journalism
```

### 5.1 Civic Action Pack fields

When a dig started from a viral lead, the pack includes:

| Field | Content |
|-------|---------|
| **Origin claim** *(optional)* | Short quote + link (labeled as lead, not CFMI finding) |
| **Triage grades** | Per-sub-claim grades from this lane |
| **Suspicion flags** *(mandatory)* | Dual Flag + Proof-status even when corruption / quid pro quo is not established |

See [civic-action-pack.md](civic-action-pack.md) §2.

---

## 6. Orchestrator integration

1. If intake is a viral/influencer/conspiracy-framed claim **or** Stage 2 surfaces one that would short-circuit analysis, spawn this lane (or run playbook **I5**).  
2. May run **alongside** Consensus claim tester ([anti-narrative-capture.md](anti-narrative-capture.md)) when the claim is also high-consensus—tester stresses “secure/unsafe” framing; this lane grades **falsifiable sub-claims** against records.  
3. When sub-claims imply money, revolving door, or organized burial—or the dig is SAVE-class—also spawn **Scale pattern mining** ([ai-scale-pattern-mining.md](ai-scale-pattern-mining.md) / playbook **I6**).  
4. Synthesis may publish **Suspicion flags** and **Supported conflict (disclosed)** with dual Proof-status; also **Supported** / carefully labeled **Partially supported** facts. Unverified viral *framing as proven corruption* and **Contradicted** claims stay out of CFMI voice. “Not established” for quid pro quo must not suppress Flag publication.  
5. Human editor gate still required.

See [ai-investigation-architecture.md](ai-investigation-architecture.md) §3.2b–§3.2c.

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
**CFMI stance:** May publish **Suspicion flags** and disclosed ties with dual Flag + Proof-status (quid pro quo usually **not established**); must **not** amplify the viral “paid to steal elections” framing as proven corruption. Hand off FOIA/journalism where filings stop.

This example shows **triage method**. It does not endorse election-fraud theories or claim any senator committed bribery.

---

## 8. Copy-paste: Viral claim triage prompt

```
You are CFMI specialist: Viral / conspiracy claim triage (parallel lane).

Obey CHARTER.md, METHODOLOGY.md §4.7 and §7.5–§7.7, ops/claim-triage-from-viral-sources.md,
ops/anti-narrative-capture.md, and ops/ai-scale-pattern-mining.md when money/burial claims appear.
Educational research only—not legal advice or voting instructions.

Origin claim (quote exactly):
"[CLAIM]"

Source / date: [URL or description]
Scope: [jurisdiction / bill / process facet]
Depth: [0 | 1 | 2]

Hard bans:
- Do not launder rumor into CFMI voice as proven corruption.
- Do not dismiss as false merely because it is labeled a conspiracy theory.
- No private motives or quid pro quo without a public-record chain.
- Do not bury Suspicion flags under a single "not established" close—use Flag + Proof-status.
- Training-data prevalence ≠ truth.

Pipeline:
1. Extract falsifiable sub-claims.
2. Steelman mainstream denial AND steelman the claim.
3. Deep public-records dig (§7.6) on each sub-claim that implies influence or misconduct.
3a. If SAVE-class or money/burial/revolving-door sub-claims: Scale pattern mine (§7.7 / I6)—
   structured edges → conflict graph / pattern table; suspicion ≠ quid pro quo.
4. Grade each: Supported | Partially supported | Not established | Contradicted.
5. Dual output: Flag (Suspicion flag / Supported conflict disclosed) + Proof-status
   (incl. quid pro quo not established | supported).
6. State what would need to be true; what records would prove it; what was checked;
   FOIA/journalist handoffs when public records do not exist.

Return ONLY the structured block in ops/claim-triage-from-viral-sources.md §5.
Mark corruption-bar gaps "not established from public sources in this pass" without erasing Flags.
Do not write the final publish package.
```

---

## 9. Version

*Claim-triage-from-viral-sources version: 0.1.3 — suspicion flags publishable by design; dual Flag + Proof-status; public labels; adversarial pass; scale pattern mining (I6 / §7.7); dual steelman; no rumor laundering / no reflexive dismissal.*
