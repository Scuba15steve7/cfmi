# Federal Election Transparency and Citizenship Verification Standards Act

**Model Federal Act — CFMI Outline Draft**  
**Version:** 0.1.0 (section outline + operative design notes; not a 50-page engrossed bill)  
**Date:** August 2026  
**Status:** Public draft for bipartisan comment. Not enacted law. Not legal advice.  
**Companion analysis:** [ai-reviews/issues/federal-election-transparency-package.md](../ai-reviews/issues/federal-election-transparency-package.md)  
**Parent issue brief:** [election-administration-integrity.md](../ai-reviews/issues/election-administration-integrity.md)

---

## Free-Market / Charter Impact Statement

**Bill:** Federal Election Transparency and Citizenship Verification Standards Act  
**Version:** 0.1.0  
**Date:** August 2026  
**Editor:** CFMI bootstrap

### One-sentence claim

This Act sets a **uniform transparency, custody, observer, audit-scope, and citizenship-verification floor for federal elections**, using published objective criteria and machine-readable data—without commandeering states for state/local offices and without creating new opaque discretion or vendor monopolies.

### Status quo distortion

| Distortion type | Present? | Brief evidence |
|-----------------|----------|----------------|
| Opaque discretion | Yes | Soft “secure” messaging; unpublished reject/cure criteria; observer rules that gut access |
| Entry / verification barrier (blunt) | Risk | Pure documentary rules without failsafe can block eligible citizens |
| Legal privilege / monopoly | Risk | Single interstate consortium or vendor lock-in for list matching |
| Incumbent subsidy | Sometimes | Election-vendor contracting opacity (secondary to this Act) |
| Other | Yes | Audit scope sold beyond what was measured; attestation without verification |

### What this proposal does

- **Lowers information barriers:** Mandatory public metrics and custody summaries for federal contests.  
- **Clarifies eligibility process:** Documentary + alternative + provisional pathways with published criteria.  
- **Leaves unchanged:** State administration of state/local offices; competitive federalism to exceed the floor.  
- **Risks new rents (mitigated):** No exclusive ERIC/vendor mandate; no vague security waivers; limited enforcement designed not to chill failsafe processing.

### Instruments used (least → more coercive)

1. Transparency / reporting mandates (machine-readable)  
2. Uniform audit-scope and certification milestone publication  
3. Observer access rules with published denial reasons  
4. Citizenship verification pathways for federal registration  
5. Limited civil enforcement (state AG / cabined private right)  
6. **Not used:** Nationalizing state races; commandeering; vague waivers

### Anti-capture checklist

- [x] No named private beneficiary class  
- [x] No exclusive franchise for list matching  
- [x] Approvals/removals use published objective criteria  
- [x] Strict non-preemption of stronger compatible state protections  
- [x] Failsafe not chilled by overbroad official criminalization  

### Bottom line

Doubt about federal election outcomes shrinks when the public can see list quality, custody, curing, observers, and what audits measured—and when citizenship for federal registration is verified under pathways that minimize false exclusion. Slogans do not substitute for that floor.

---

## Constitutional Basis Statement

**Jurisdiction:** Federal model act (Elections Clause primary; careful presidential scope; dual system for state offices).

### One-sentence constitutional claim

Congress may prescribe times, places, and manner regulations for congressional elections, including transparency and federal-registration verification floors; presidential-contest provisions are drafted tightly and severable; state/local offices remain state-run without commandeering.

### Source of authority

| Level | Authority invoked | Notes |
|-------|-------------------|-------|
| Federal — Congress | U.S. Const. art. I, § 4 | Primary hook for House/Senate election manner rules |
| Federal — Congress | Art. II / Amend. XII + necessary and proper (careful) | Presidential electors / timing / counting adjacency; severable |
| Federal — Congress | Existing citizenship requirement for federal voting; NVRA amendment pattern | Verification of an existing eligibility rule |
| State | Retained for state/local offices | Dual registration/ballot systems expressly allowed |
| Anti-commandeering | Printz / New York line | No order that states regulate their own offices under federal political terms |

### Federalism design

| Principle | How the text complies |
|-----------|------------------------|
| Anti-commandeering | Duties attach to **federal contests** and **federal registrants**; states may keep separate state-office rules |
| Preemption scope | **Floor, not ceiling:** stricter compatible state transparency/observer/custody rules preserved |
| Experimentation | States may exceed metrics cadence, observer access, or verification rigor |
| Competitive pressure | Public metrics enable comparison across states |

### Separation of powers

Legislative standards define data fields, verification pathways, and audit-scope legends. Agency (EAC/NIST-adjacent technical standards, DHS/SSA data access) applies published specs—not open-ended “election security as appropriate” policymaking.

---

## Unintended Consequences Statement

| Risk | Mitigation in outline |
|------|------------------------|
| Eligible citizens blocked | Alternative pathways + provisional failsafe + vital-record fee waivers + name-change procedures |
| Unfunded mandate burden | Authorize formula grants tied to objective compliance metrics; phased effective dates |
| Failsafe chilled | Limit criminal exposure to knowing falsification / willful refusal of published criteria; good-faith safe harbor |
| Privacy over-disclosure | Publish aggregates and exception rates; personal data under existing privacy constraints |
| Vendor monopoly | Interoperable standards; no exclusive consortium mandate |
| Scope creep to state races | Explicit non-application to purely state/local contests; severability |
| Performative compliance | Machine-readable schemas + denial-reason logs beat checkbox affidavits |

---

## Short title; findings (drafting notes)

**§1. Short title.** Federal Election Transparency and Citizenship Verification Standards Act.

**§2. Findings.** Findings shall:

- State that citizenship is already required for federal elections; the Act addresses **verification and transparency gaps**, not inventing the citizenship rule.  
- **Not** recite unverified national fraud rates or stolen-election claims.  
- Note that risk-limiting audits answer tabulation questions unless eligibility sampling is separately authorized.  
- Note GAO/CISA-style residual process risks as *mechanism* context, without vibe alarm.

---

## Title I — Definitions and Scope

**§101. Definitions.** Include: federal office; federal election; federal registrant; chain-of-custody event; custody exception; meaningful observer access; risk-limiting audit; eligibility sample; machine-readable; interoperable list-match standard; alternative evidence; provisional federal ballot.

**§102. Federal election scope.**

(a) This Act applies to elections for Senator, Representative, and—subject to §103—President and Vice President (electors).  
(b) **Non-application to state offices.** Nothing in this Act requires a state to apply these rules to elections for state or local office.  
(c) **Dual systems.** A state may maintain separate registration or ballot rules for state/local offices so long as federal contests and federal registrants meet this Act.  
(d) **Strict non-preemption.** State laws that provide greater transparency, observer access, custody logging, or verification for federal contests remain effective if compatible.

**§103. Presidential contests; severability.** Provisions applying to presidential electors are severable. If held invalid, Titles II–V remain for congressional elections.

---

## Title II — Public Data Floor

**§201. Required publications.** For each jurisdiction administering a federal election, the chief state election official shall publish, in a national machine-readable schema (to be specified by regulation within objective statutory fields):

1. Voter-list metrics (active/inactive; notices; removals by reason; interstate match hits/appeals; death-file hits).  
2. Mail/absentee metrics (issued; returned; rejected by reason; cured; pending).  
3. Custody-exception summaries (seal breaks; unscheduled collections; lost/spoiled batches—counts).  
4. Observer metrics (requests; grants; denials with coded reasons).  
5. Audit results with **scope legend** (tabulation / eligibility sample / custody review).

**§202. Cadence.** Pre-election baseline; election night / +7 / +30 / +90 days; quarterly list metrics in federal-election years. Delayed certification triggers public milestone status within 24 hours of missing a published deadline.

**§203. No vague waiver.** No authority to waive §201–202 for “security” or “as appropriate” without a published, time-limited, factual finding meeting statutory criteria (narrow emergency only).

---

## Title III — Chain of Custody; Drop Boxes; Curing

**§301. Federal ballot custody minimums.** Written SOP for each hop of mail/absentee and drop-box federal ballots; bipartisan or multiparty collection where state law uses party observers; seal and log requirements; exception reporting into §201.

**§302. Drop boxes.** If used for federal ballots: published locations; collection schedule; logged retrievals; video or equivalent where feasible under state privacy law—summaries public, not necessarily raw video dump if privacy conflicts (statute sets hierarchy).

**§303. Curing transparency.** Published signature/reject criteria; notice timelines; public reject/cure rates by reason. Criteria must be objective; changes logged with effective dates.

---

## Title IV — Observers

**§401. Meaningful access.** For federal contests, credentialed observers shall be allowed to view material steps (intake, curing desk process from a non-interfering distance, tabulation, audit) under published distance/conduct rules that do not nullify observation.

**§402. Denials.** Written denial with coded reason within a short statutory clock; aggregate denials published under §201.

**§403. Non-interference.** Observers may not touch ballots or disrupt process; violations are sanctionable without using “interference” as a pretext to bar observation of lawful public steps.

---

## Title V — List Maintenance Coordination (No Monopoly)

**§501. Interoperable matching.** States participating in federal elections shall implement or join **interoperable** interstate duplicate/death/move matching meeting published technical standards.

**§502. No exclusive consortium.** The Act shall not require membership in any single named organization (including ERIC or successors). Multiple compliant networks or bilateral agreements may satisfy §501.

**§503. Due process for removals.** Notice, opportunity to cure/appeal, published criteria; statistics under §201. NVRA consistency: amend NVRA only as needed for federal-registrant citizenship verification and transparent maintenance—not silent purges.

---

## Title VI — Citizenship Verification for Federal Registration

**§601. Requirement.** An application to register to vote in a federal election shall include proof of U.S. citizenship under §602 or §603.

**§602. Documentary pathway.** Accept documents substantially aligned with SAVE Act lists (passport; birth certificate + photo ID; REAL ID indicating citizenship; military ID with birth record; other objectively listed docs). EAC (or designated agency) may update the list by rule within statutory categories after notice and comment.

**§603. Alternative pathway.** Applicants lacking §602 documents may:

1. Submit other evidence under a published schedule; and/or  
2. Consent to database corroboration (vital records, SSA, DHS systems as authorized); and  
3. Attest under penalty of perjury.

Acceptance/rejection rates and median times published under §201.

**§604. Provisional / fail-safe.** If verification is pending at the close of registration, the applicant shall be offered a provisional or conditioned federal ballot with a cure window through a statutory date. States shall facilitate low/no-cost vital records for this purpose where the state controls issuance.

**§605. Anti-chill.** Officials acting in good faith under published §603–604 criteria shall have a safe harbor from criminal penalties. Penalties target knowing acceptance of falsified evidence, knowing registration of noncitizens, or willful refusal to apply published pathways.

**§606. SAVE Act relationship.** This Title is the CFMI-modified counterpart to SAVE-style documentary proof: **keep** core verification; **strengthen** alternative/failsafe; **modify** enforcement chill; **reject** nationalizing state offices.

---

## Title VII — Audits (Tabulation and Eligibility Sampling)

**§701. Tabulation audits.** Each state shall conduct a risk-limiting audit (or statistically equivalent method) for federal contests where paper/voter-verifiable records exist, with results and scope legend published under §201.

**§702. Eligibility sampling (where feasible).** Direct a pilot-then-floor program for statistically designed samples checking registration eligibility attributes (including citizenship pathway documentation on file)—**separate** from RLA. Results shall not be marketed as RLAs.

**§703. Pre-commitment.** Audit plans filed before election day: methods, contests, what is and is not measured.

---

## Title VIII — Enforcement; Grants; Severability

**§801. Enforcement.**

(a) **Primary:** Civil actions by the Attorney General and by state attorneys general for pattern-or-practice violations of Titles II–VII.  
(b) **Limited private right of action:** Cabined to denial of meaningful observer access or failure to publish required §201 datasets after notice and opportunity to cure—**not** open-ended private prosecution of individual registration decisions.  
(c) Individual registration disputes proceed through state administrative appeal + existing judicial review unless Congress specifies otherwise.

**§802. Conditional grants.** Authorize formula grants for schema implementation, custody logging, and vital-record fee waivers—objective compliance metrics; no speech conditions inconsistent with Charter funding rules for CFMI itself (note: this is statutory grant design for states).

**§803. Severability.** Standard severability; §103 presidential provisions severable.

**§804. Effective dates.** Phased: Title II data floor first; Titles III–IV next; Titles VI–VII after schema and failsafe infrastructure online.

---

## What NOT to include (drafting redlines)

- Vague “election security” waiver authority  
- Partisan boards with unpublished discretionary standards  
- Mandated ERIC-only membership  
- Federal takeover language for state/local races  
- Findings that assert unverified national fraud percentages  
- Criminal exposure that nullifies §603–604 in practice  

---

## Open drafting questions

1. Exact presidential-electors drafting that survives severability stress—counsel required.  
2. Grant size vs bare mandate for passability.  
3. Whether eligibility sampling (§702) starts as optional pilot or day-one floor.  
4. Interaction with existing NVRA private right of action—harmonize, do not accidentally expand capture opportunities.  
5. Privacy rules for drop-box video vs public summary sufficiency.

---

## Improve this outline

Feedback: [docs/tool.html](../docs/tool.html) · [counterevidence issue](https://github.com/scuba15steve7/cfmi/issues/new?template=counterevidence.yml)  
Analysis package: [federal-election-transparency-package.md](../ai-reviews/issues/federal-election-transparency-package.md)

*End of outline draft v0.1.0.*
