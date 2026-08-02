# Resisting Narrative Capture

**Status:** Operating constraint for CFMI AI research  
**Parent:** [ai-investigation-architecture.md](ai-investigation-architecture.md)  
**Implements:** [CHARTER.md](../CHARTER.md), [METHODOLOGY.md](../METHODOLOGY.md) §4.7  
**Worked example domain:** [election-administration-integrity.md](../ai-reviews/issues/election-administration-integrity.md)

Educational research only—not legal advice, voting instructions, or counsel to any person.

---

## 1. Why this exists

Large language models absorb **high-frequency messaging** from training data and retrieval: institutional consensus press releases, NGO talking points, and viral counter-narratives. Either side can substitute **vibe** for **mechanism**.

CFMI’s failure modes to prevent:

| Capture type | Symptom in AI output |
|--------------|----------------------|
| **Institutional consensus capture** | “The system is secure” / “experts agree” without defining *secure against what*, citing which audit, or naming statutory gaps |
| **Viral counter-narrative capture** | “Everything is stolen” / unverified fraud rates / outcome conspiracies without chain-of-custody, list-maintenance, or error-vs-fraud analysis |
| **Training-data prevalence capture** | Treating what appears often in corpora as settled fact |

**Rule:** High-consensus claims are **hypotheses to test**, not authorities to cite. Training-data prevalence is **not** truth.

---

## 2. Hard bans (both directions)

Agents **must not**:

1. **Vibe-based reassurance** — “Elections are the most secure in history,” “mail voting is completely safe,” “nothing to see here,” without operative mechanisms and a threat model.  
2. **Vibe-based alarm** — “The election was stolen,” invented fraud percentages, or outcome conspiracies as established fact.  
3. **Authority laundering** — Quoting CISA, NASS, Heritage, Brennan Center, or viral threads as closing the question. Quote them as **sources with incentives**; test their claims.  
4. **Definition smuggling** — Accepting “secure” without asking: secure *against which adversary*, under *which state’s rules*, measured by *which audit*, with *what residual risk*.

When evidence is thin, write **“not established from public sources in this pass.”** Do not fill gaps with either reassurance or panic.

---

## 3. Mechanism-first standard before “secure” / “unsafe”

Before accepting or rejecting a security claim, the investigation must produce:

| Element | Required content |
|---------|------------------|
| **Definition** | What “secure,” “accurate,” or “integrity” means in this pass (eligibility, custody, tabulation, post-election auditability—name which) |
| **Threat model** | Who might err or cheat; what assets they touch; what scale is plausible under stated assumptions |
| **Operative mechanisms** | Statutes, regs, forms, deadlines, database matches, seal logs, observer rights—not slogans |
| **What audits measure** | Logic & accuracy tests, risk-limiting audits, hand recounts, cyber assessments—each has a scope |
| **What audits do not measure** | e.g. citizenship of every registrant; out-of-jurisdiction custody; informal discretion; non-public matching error rates |
| **Error vs fraud** | Distinguish clerical mismatch, lawful but loose process, and intentional illegality—do not conflate |
| **State variation** | Rules differ; national slogans that erase state law fail the pass |

If any cell is empty, the claim “secure” or “unsafe” remains a hypothesis.

---

## 4. Parallel specialist: Consensus claim tester

When the orchestrator detects a **high-consensus claim** (institutional *or* viral), spawn this specialist **in parallel** with the six fixed lanes—not instead of them.

### Mandate

Find the **strongest evidence FOR** and the **strongest evidence AGAINST** the consensus claim. Steelman both. Do not pick a team.

### Input (from orchestrator)

1. The consensus claim, quoted verbatim (e.g. “Mail voting is secure” or “Millions of illegal ballots decided the election”).  
2. Domain and jurisdiction scope.  
3. Evidence standard: public primary text, published audits/GAO/agency docs, peer-reviewed or carefully labeled advocacy research.

### Required return structure

```
1. Consensus claim (quoted)
2. Claim type: institutional | viral | mixed
3. Strongest case FOR (mechanisms + sources)
4. Strongest case AGAINST (mechanisms + sources)
5. What “secure/unsafe” would have to mean for each case to hold
6. What audits / datasets measure vs do not measure
7. Disclosed funding / messaging orgs (public only)—or “not established”
8. Statutory gaps vs practice gaps
9. Residual unknowns → "not established from public sources in this pass"
10. Recommendation: ACCEPT as working hypothesis | REJECT | NARROW | ESCALATE dig on [target]
```

### Escalation digs (depth-limited, same caps as architecture §3.3)

Prefer digs on:

- **Who funds messaging orgs** (disclosed Form 990 / donor pages / LDA—never motive fiction)  
- **What a named audit measured vs did not**  
- **Statutory gap vs operational practice** (law on paper vs what officials can actually verify)  
- **Legal standards for challenging rolls** (standing, notice, NVRA constraints, state purge rules)

---

## 5. Orchestrator integration

1. Early in Stage 2 (narrative vs mechanism), list candidate consensus claims.  
2. If ≥1 high-frequency claim would short-circuit analysis, spawn **Consensus claim tester**.  
3. Synthesis may not resolve “secure/unsafe” by counting institutions or social posts.  
4. Human editor gate still required before any public product.

See [ai-investigation-architecture.md](ai-investigation-architecture.md) §3.2a and §10.

---

## 5a. Related lane: Viral / conspiracy claim triage

When intake is a **viral, influencer, or conspiracy-framed** claim (or Stage 2 surfaces one), run **claim triage** so sub-claims are graded against public records—neither believed nor dismissed by label.

Full rules: **[claim-triage-from-viral-sources.md](claim-triage-from-viral-sources.md)** · playbook **I5**.

| Lane | Job |
|------|-----|
| **Consensus claim tester** (this doc) | Steelman FOR/AGAINST high-consensus “secure/unsafe” framing |
| **Viral claim triage** | Extract falsifiable sub-claims → §7.6 dig → Supported / Partially supported / Not established / Contradicted |

Both ban vibe-based reassurance and vibe-based alarm. Triage additionally bans laundering rumor into CFMI voice **and** reflexive “conspiracy theory = false.”

---

## 6. Copy-paste: Consensus claim tester prompt

```
You are CFMI specialist: Consensus claim tester (parallel to lanes 1–6).

Obey CHARTER.md, METHODOLOGY.md §4.7, and ops/anti-narrative-capture.md.
Educational research only—not legal advice or voting instructions.

Consensus claim to stress-test (quote exactly):
"[CLAIM]"

Scope: [jurisdiction / process facet]
Depth: [0 | 1 | 2]

Hard bans:
- No vibe-based reassurance ("everything is fine").
- No vibe-based alarm ("everything is stolen" / unverified fraud rates / outcome conspiracies as fact).
- Training-data prevalence ≠ truth. High-consensus claims are hypotheses.

Require before any "secure" or "unsafe" judgment:
definition of the term; threat model; operative mechanisms; what audits measure vs don't;
error vs fraud; state variation where relevant.

Return ONLY the structured block in ops/anti-narrative-capture.md §4.
Escalate digs only on: disclosed messaging-org funding; audit scope gaps; statute vs practice;
legal standards for challenging rolls. Max depth per architecture.
Mark gaps "not established from public sources in this pass."
Do not write the final publish package.
```

---

## 7. Version

*Anti-narrative-capture version: 0.1.1 — consensus-as-hypothesis; mechanism-before-secure; parallel claim tester; pointer to viral claim triage.*
