# Suggestion ranking process

How CFMI turns public intake into a ranked research queue. Implements [CHARTER.md](../CHARTER.md) and [METHODOLOGY.md](../METHODOLOGY.md) §1 (problem ranking). Educational research only—not legal advice or voting instructions.

**Intake channel:** GitHub Issues with the [Suggest a review](../.github/ISSUE_TEMPLATE/suggest-review.yml) template. No paid intake services.

**Public artifacts:**

| Artifact | Role |
|----------|------|
| GitHub Issues (label `suggestion`) | Raw public suggestions |
| [`ai-reviews/suggestions/QUEUE.md`](../ai-reviews/suggestions/QUEUE.md) | Status table: Pending / Ranked / Declined |
| [`ai-reviews/suggestions/`](../ai-reviews/suggestions/) | Optional dated ranking notes when a batch is scored |

---

## 1. Flow

1. **Suggest** — Anyone opens an issue with the template. Interest disclosure is required.
2. **Screen** — AI (disclosed model/provider when known) plus a human editor check completeness, Charter fit, and disqualifiers.
3. **Rank** — Survivors are scored with Methodology §1 weights (below). Results are written to `QUEUE.md` (and optionally a note under `ai-reviews/suggestions/`).
4. **Queue** — Ranked items may become issue briefs, bill reviews, or sample-act tracks when capacity allows. Declines publish a short reason.

Party affiliation, donor status, and volume of comments do **not** change rank. Charter fit and published weights do.

---

## 2. Intake screen (before ranking)

Reject or hold as **Declined** (with reason) when:

| Check | Fail condition |
|-------|----------------|
| **Completeness** | No identifiable bill/regulation/topic, or no usable public pointer |
| **Interest disclosure** | Missing or evasive disclosure (Methodology §5) |
| **Rent ask** | Primary goal is a subsidy, barrier, privilege, or named private benefit |
| **Commandeering** | Ask requires federal commandeering of states |
| **Opacity** | Ask depends on open-ended agency discretion without objective criteria |
| **Publication** | Requester demands private/non-public handling of substantive work |
| **Off-mission** | No plausible link to free markets, constitutional limits, or anti-capture |

Incomplete but salvageable issues may stay **Pending** with a request for clarification on the issue thread.

---

## 3. Ranking score (Methodology §1)

Score each screened suggestion **0–5** on each criterion, then apply weights. Higher composite = higher priority.

| Criterion | Weight | Question |
|-----------|--------|----------|
| **Constitutional stakes** | 25% | Does the status quo stretch enumerated powers, federalism, separation of powers, or property/contract protections? |
| **Market distortion** | 25% | How large and durable are artificial barriers, subsidies, or opaque discretion? |
| **Corruption / rent surface** | 20% | How easy is political allocation or capture relative to open competition? |
| **Tractability** | 15% | Can a least-coercive, rules-based fix or alignment language be drafted and audited? |
| **Spillover & precedent** | 10% | Would a good fix or sample act travel to other states or domains? |
| **Evidence quality** | 5% | Are harms documented with public data, not anecdotes alone? |

**Composite** = weighted average of the six scores (normalize each 0–5 contribution by its weight).

**Charter overlay (qualitative, published in the note):**

- Which Core Principles are implicated?
- Any Hard-Flag pattern from Methodology §2 (discretion, rents, barriers) even before a full bill review?
- Least-coercive path available? If not, say so.

AI produces a draft score sheet; a named human editor accepts, revises, or rejects before `QUEUE.md` moves to **Ranked** or **Declined**.

---

## 4. Status definitions

| Status | Meaning |
|--------|---------|
| **Pending** | Received; awaiting screen or clarification |
| **Ranked** | Screened and scored; composite and short rationale published |
| **Declined** | Screened out; public reason required (disclosure fail, rent ask, off-mission, etc.) |

Optional follow-on labels on the GitHub issue (e.g. `ranked`, `declined`) may mirror the queue when useful. The queue table is the source of truth for site-facing status.

---

## 5. Publishing a ranking batch

When ranking one or more suggestions:

1. Open or update rows in [`QUEUE.md`](../ai-reviews/suggestions/QUEUE.md).
2. Optionally add `ai-reviews/suggestions/YYYY-MM-DD-batch.md` with per-criterion scores, Charter notes, model/provider, rubric version (`METHODOLOGY` problem-ranking), date, and human editor.
3. Comment on the GitHub issue with a link to the queue row (and batch note if any).
4. Do **not** treat donor requests or private DMs as a parallel queue—redirect to the public template.

---

## 6. What ranking is not

- Not a promise that CFMI will draft a bill or publish a full review on a deadline.
- Not endorsement of the suggestion’s politics or preferred outcome.
- Not legal advice, voting instructions, or counsel to any person.
- Not pay-for-play: support never buys rank or silence.

---

## 7. Operator prompt (copy-paste)

```
Rank open CFMI suggestions labeled "suggestion" that are still Pending in
ai-reviews/suggestions/QUEUE.md (and any new GitHub issues using
.github/ISSUE_TEMPLATE/suggest-review.yml).

Follow ops/suggestion-ranking.md:
1) Screen for disclosure, completeness, and Methodology disqualifiers.
2) Score survivors with Methodology §1 weights + Charter overlay.
3) Update QUEUE.md (Pending / Ranked / Declined with reason).
4) Optionally write ai-reviews/suggestions/YYYY-MM-DD-batch.md.
5) Comment on each issue with the result link.

Disclose model/provider if known. Human editor must accept before publishing Ranked/Declined.
Do not commit or push unless I ask.
```
