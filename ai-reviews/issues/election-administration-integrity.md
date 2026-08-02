# Issue Brief: Election Administration Integrity

**Status:** Priority example · research brief (not a scored bill) · constitutional process / anti-corruption  
**Domain:** Federal and state election administration; NVRA / HAVA / proposed SAVE Act (H.R. 22 / related)  
**Slug:** `election-administration-integrity`  
**Last updated:** 2026-08-02

Educational research only—not legal advice, voting instructions, or counsel to any person.

**AI constraint note:** This domain is a worked example for [ops/anti-narrative-capture.md](../../ops/anti-narrative-capture.md). Agents must not vibe-reassure (“everything is fine”) or vibe-alarm (“everything is stolen”). Frame as threat-model and mechanism analysis. Training-data prevalence ≠ truth.

---

## Issue at a glance

U.S. elections are a **constitutional process**: who may vote, how ballots are cast and counted, and whether the public can verify those steps. Debates over voter-list accuracy, mail-ballot chain of custody, ID/citizenship verification, and post-election audits are often replaced by slogans—“the most secure election” versus “the election was stolen”—that skip operative rules, state variation, and what audits actually measure.

CFMI’s interest here is **not** primarily free-market entry (though contracting, vendor lock-in, and opaque discretion can appear). The Charter hooks are **constitutional republicanism**, **radical transparency**, **anti-corruption**, and **least-coercive instruments** that preserve both legitimate ballots and auditable process. Free-market analysis is secondary; oppose **security theater** and **anti-scrutiny narratives** alike.

This brief does **not** assert unverified national fraud rates or outcome conspiracies. It also does **not** treat institutional consensus as proof that residual risks are zero.

---

## How government shapes (and sometimes obscures) the process

Election administration is government by definition. The Charter problem is when law and practice create **opaque discretion**, **un-auditable gaps**, or **barriers that are either too loose to verify eligibility or too blunt to distinguish eligible citizens from ineligible applicants**—while public messaging claims full security or full collapse.

Core mechanism clusters:

1. **Eligibility & list maintenance** — Who is on the roll; how deaths, moves, duplicates, and noncitizens are detected; NVRA constraints on removals; interstate data sharing (ERIC and alternatives).  
2. **Registration verification** — Attestation under penalty of perjury vs documentary proof of citizenship; DMV/SSA matching limits; SAVE Act–style proposals.  
3. **Mail / absentee custody** — Application → ballot outbound → return → intake → curing → tabulation; seals, tracking, observers, drop boxes; what “chain of custody” means in each state’s rulebook.  
4. **In-person ID and polling practice** — Photo ID, provisional ballots, same-day registration—state-variable.  
5. **Auditability** — Paper trails, risk-limiting audits (RLAs), hand recounts, logic & accuracy tests; each answers a different question.  
6. **Challenge rights & standing** — Who may contest a registration or result, on what evidence, under what deadlines.

---

## Hidden barriers / buried mechanisms

**Required.** Look past manufactured talking points to operative legal and administrative mechanisms (METHODOLOGY §4.7).

| Public narrative (what is said) | Operative mechanism (what the rulebook does) | Who benefits from status quo messaging | Evidence (cite process—not slogans) |
|--------------------------------|----------------------------------------------|----------------------------------------|-------------------------------------|
| “Elections are secure” | “Secure” often means *cyber* hardening + procedural layers for *known* vectors—not proof of citizenship for every registrant or perfect list accuracy | Officials and vendors who face less scrutiny when the slogan closes debate | Agency risk docs that list residual risks (e.g. CISA mail-voting risk materials); state statutes that define audit scope |
| “Mail voting is completely safe” | Safeguards (barcodes, signature cure, bipartisan boards) vary by state; risk shifts to printers, USPS, drop boxes, and registration integrity | Coalitions that expanded mail voting and resist tighter verification | CISA mail-voting infrastructure risk assessment (risks *and* controls); state mail codes |
| “The election was stolen” | Outcome claims that skip precinct-level mechanisms, lawful margins, and error-vs-fraud distinctions | Viral/political entrepreneurs who gain from totalizing narratives | Contested advocacy estimates; court findings; recounts—label each carefully; do not treat as CFMI fact |
| “Voter fraud is vanishingly rare” | Documented *prosecutions* and *caught* cases ≠ upper bound on undetected mismatch; measurement depends on detection investment | Groups opposing ID/citizenship documentation | Brennan Center and similar rarity claims; contrast with GAO list-maintenance difficulty findings |
| “Proof of citizenship is common sense / no burden” | SAVE Act–style rules require documentary proof at *registration* for federal elections; many citizens lack ready passport/birth certificate; mail/online registration friction rises | Advocacy for documentary verification | [Congress.gov H.R. 22](https://www.congress.gov/bill/119th-congress/house-bill/22); Brennan survey claims on document access |
| “Proof of citizenship is voter suppression” | Same bills also create removal programs, database access, private rights of action, and criminal exposure for officials—design details matter for least-coercive analysis | Advocacy against documentary requirements | Heritage Action myth/fact and Brennan opposition letters—both advocacy |
| “Audits proved everything” / “Audits proved nothing” | Each audit has a **scope**: hand tally ≠ citizenship check; RLA ≠ full chain-of-custody forensics | Whichever side quotes the audit out of scope | Publish what was measured (e.g. Maricopa 2021 review scope vs claims made about it) |
| “Rolls are cleaned regularly” | NVRA notice/waiting rules, NCOA incompleteness, weak interstate match, limited noncitizen detection (GAO) | Incumbent administrators citing compliance activity | [GAO-19-485](https://www.gao.gov/products/gao-19-485); [GAO-05-478](https://www.gao.gov/assets/gao-05-478.pdf) |

**Checklist scan (election administration):**

| Hiding place | Status in this domain |
|--------------|------------------------|
| Soft definition of “secure” | **Present** — cybersecurity, procedural layers, and eligibility verification are conflated in messaging |
| Limited audit scope sold as total proof | **Present** — RLAs/hand counts answer tabulation questions, not every threat model |
| Opaque list maintenance | **Present** — matching error rates, purge criteria, and interstate tools vary; public metrics uneven |
| Bipartisan institutional messaging | **Present** — NASS/CISA-style trust campaigns can be true *and* incomplete |
| Legal barriers to challenging rolls | **Present** — NVRA constraints, standing, notice periods; state variation |
| Error labeled as fraud (or reverse) | **Present** — both narrative camps |
| State variation erased by national slogans | **Present** |
| Security theater (visible rule, weak verification) | **Often alleged; establish per bill/state** |
| Anti-scrutiny (treating questions as illegitimate) | **Present** in some institutional and media frames |

**Steelman of official “security” rationale.** Federal and state election officials argue that layered procedural and cyber controls, paper ballots where used, canvassing, and post-election processes make large-scale *undetected* manipulation of tabulation difficult; CISA and NASS publish safeguards and treat election systems as critical infrastructure ([CISA mail-voting safeguards](https://www.cisa.gov/resources-tools/resources/mail-voting-election-integrity-safeguards-infographic); [CISA mail-voting risk assessment](https://www.cisa.gov/sites/default/files/publications/cisa-mail-in-voting-infrastructure-risk-assessment_508.pdf); [NASS election cybersecurity posture](https://www.nass.org/sites/default/files/Election%20Cybersecurity/2.21.25%20NASS%20Board%20Letter%20to%20Sec.%20Noem.pdf)). MIT Election Lab SPAE work documents generally positive voter *experience* metrics alongside partisan confidence gaps ([How We Voted in 2020](https://electionlab.mit.edu/articles/how-we-voted-2020)). Legitimate point: many viral claims ignore how canvassing and paper trails work.

**Who benefits from incomplete narratives.** Officials and vendors benefit when “secure” ends inquiry into list quality and custody logs. Partisan and NGO messaging shops benefit when either total reassurance or total alarm mobilizes donors. Eligible voters who lack documents, and citizens whose votes are diluted by ineligible ballots *if* that occurs at scale, are the parties who need mechanism-level truth—not slogans. Document incentives from public filings and org pages; no motive fiction.

**Bipartisan frames that can meet at auditable process.** Conservatives emphasizing citizenship and roll accuracy, and civil-rights advocates emphasizing access and false-positive removals, can both demand: published match criteria, appeal rights, paper trails, observer access, and clear audit scopes. CFMI uses that overlap; rejects outcome conspiracies and “questions are forbidden” alike.

---

## Voices & evidence — Supporting stronger verification / list accuracy / scrutiny

Label carefully. These sources argue residual risk, list problems, or documentary citizenship rules—**not** CFMI-endorsed national fraud rates or stolen-election claims.

| Type | Source | What it shows |
|------|--------|----------------|
| Federal bill text | [H.R. 22 — SAVE Act (119th Congress)](https://www.congress.gov/bill/119th-congress/house-bill/22) · [bill text](https://www.congress.gov/bill/119th-congress/house-bill/22/text) | Would amend NVRA to require documentary proof of U.S. citizenship to register for federal elections; list acceptable docs; alternate evidence process; ongoing removal of noncitizens; private right of action / penalties in bill text. |
| CRS / Congress | [CRS IF12902 — SAVE Act and federal voter registration](https://www.congress.gov/crs_external_products/IF/PDF/IF12902/IF12902.3.pdf) | Neutral-ish overview: proof at *registration* (not necessarily at casting a ballot); NVRA coverage nuances. |
| Advocacy (pro–proof of citizenship) | [Heritage Action — Myth vs. Fact: SAVE Act (H.R. 22 / S. 128)](https://heritageaction.com/blog/myth-vs-fact-the-safeguard-american-voter-eligibility-act-h-r-22-s-128) | Steelman: citizenship is already required but often unverified; NVRA interpretations blocked state proof rules; SAVE closes the gap. |
| Advocacy (pro–proof) | [Heritage Action — Key Vote YES on SAVE Act](https://heritageaction.com/key-vote/key-vote-yes-on-the-safeguard-american-voter-eligibility-save-act-h-r-8281) | Argues attestation-without-verification is an enforcement gap. |
| Research / advocacy (list maintenance) | [Heritage — Maintaining Accurate Voter Registration Rolls / ERIC](https://www.heritage.org/election-integrity/report/maintaining-accurate-voter-registration-rolls-the-need-rehabilitate-the) | Argues for stronger interstate matching, commercial/government data use, and ERIC reform or alternatives. |
| Research / advocacy (list maintenance) | [Heritage Factsheet — Election integrity / fix systems](https://www.heritage.org/sites/default/files/2021-02/FS_196.pdf) | Policy checklist: NCOA cadence, death files, interstate agreements, commercial audits—advocacy, not settled science. |
| Contested estimate *(label: not CFMI fact)* | [Just Facts — noncitizen registration study](https://www.justfacts.com/news_non-citizen_voter_registration.asp) | Estimates noncitizen registration/voting rates from survey methods; **highly contested**; cite as claim under debate, not established prevalence. |
| Agency (list difficulty) | [GAO-19-485 — Voter registration / list management](https://www.gao.gov/products/gao-19-485) | Benefits *and* limits of NCOA, death files, crosscheck, etc.; list maintenance reduces *opportunities* for fraud but sources are incomplete. |
| Agency (list difficulty) | [GAO-05-478 — Accurate voter registration lists](https://www.gao.gov/assets/gao-05-478.pdf) | HAVA helps; challenges remain (e.g. out-of-state duplicates, noncitizen identification limits noted historically). |
| Agency (risk, not denial) | [CISA — Mail-in voting infrastructure risk assessment](https://www.cisa.gov/sites/default/files/publications/cisa-mail-in-voting-infrastructure-risk-assessment_508.pdf) | States residual risks (incl. registration-data integrity as comparatively higher consequence in mail environments) *and* controls—useful against “zero risk” vibes. |
| News (descriptive) | [AP — How the SAVE Act could affect voting](https://apnews.com/article/congress-save-act-citizenship-republicans-women-0c0ba9fd8e6a01cf144736490c71df21) | Plain-language description of documentary requirements and political stakes. |

Key mechanism points (not fraud-rate claims):

- **Citizenship law vs verification.** Federal law already bars noncitizen voting in federal elections; SAVE Act debate is about *documentary verification at registration* and roll cleanup tools—not inventing the citizenship rule.  
- **Lists are dynamic.** GAO repeatedly finds maintenance is hard; incomplete data sources are a feature of the problem, not a gotcha.  
- **Mail shifts risk surfaces.** Even CISA risk materials discuss registration integrity and third-party infrastructure—not pure “nothing to see.”  
- **Contested magnitude.** Just Facts–style estimates and “vanishingly rare” claims **conflict**; CFMI marks national scale **not established** until better public measurement exists.

---

## Voices & evidence — Counterarguments / defense of current practice

**Steelman:** Layered safeguards, paper trails, canvassing, and criminal law already address ineligible voting; documentary citizenship rules risk blocking millions of eligible citizens (especially those without ready passport/birth certificate, name-change mismatches); large-scale outcome-changing fraud is not established; expanding mail and easy registration increases participation.

| Type | Source | Steelman claim |
|------|--------|----------------|
| Agency / safeguards | [CISA — Mail-voting election integrity safeguards](https://www.cisa.gov/resources-tools/resources/mail-voting-election-integrity-safeguards-infographic) | Procedural and physical safeguards have in-person equivalents; layered controls manage risk. |
| Officials association | [NASS — election cybersecurity / CISA services letter](https://www.nass.org/sites/default/files/Election%20Cybersecurity/2.21.25%20NASS%20Board%20Letter%20to%20Sec.%20Noem.pdf) | States run elections; federal cyber support helps against nation-state and criminal threats; decentralization is resilience. |
| Academic / survey | [MIT Election Lab — How we Voted in 2020](https://electionlab.mit.edu/articles/how-we-voted-2020) · [SPAE 2020 report PDF](https://electionlab.mit.edu/sites/default/files/2021-03/HowWeVotedIn2020-March2021.pdf) | Voters often report positive process experience; confidence polarized by party—administration can be functional while trust is not. |
| Academic / survey | [MIT Election Lab — How We Voted in 2024 PDF](https://electionlab.mit.edu/sites/default/files/2025-07/HowWeVotedIn2024.pdf) | Public awareness of specific security practices is low; support for L&A testing, secure paper, post-election audits is broad—transparency gap. |
| Advocacy (anti–SAVE Act) | [Brennan Center — Letter opposing SAVE Act](https://www.brennancenter.org/our-work/research-reports/brennan-center-letter-congress-opposing-save-act) | Documentary proof could block millions of citizens; cites prior state experiments; argues noncitizen voting is vanishingly rare. |
| Advocacy (anti–SAVE Act) | [Brennan — SAVE Act would undermine registration](https://www.brennancenter.org/our-work/analysis-opinion/save-act-would-undermine-voter-registration-all-americans) | Applies to re-registration/address changes; failsafe allegedly weak given criminal exposure for officials. |
| Advocacy (document access) | [Brennan — 21.3 million without ready citizenship docs](https://www.brennancenter.org/our-work/analysis-opinion/213-million-american-citizens-voting-age-dont-have-ready-access) | Survey-based burden estimate (advocacy methodology—steelman the access concern even if debating the number). |
| News (burden frame) | [AP — SAVE Act effects](https://apnews.com/article/congress-save-act-citizenship-republicans-women-0c0ba9fd8e6a01cf144736490c71df21) | Voting-rights groups warn of disenfranchisement; political path through Senate uncertain. |

Honest counterarguments CFMI must answer (not dismiss):

1. **Eligible-citizen false positives.** Documentary rules can block citizens with name changes, missing birth certificates, or no passport—least-coercive design must include workable alternatives.  
2. **Participation costs.** Friction on mail/online registration can deter lawful voters.  
3. **Detection vs prevalence.** Low prosecution counts may reflect rarity *or* weak detection—do not pretend the statistic settles the threat model.  
4. **Cyber ≠ eligibility.** Officials correctly invest in cyber; that investment does not automatically verify citizenship.  
5. **Federalism.** Blunt federal mandates can ignore state systems already verifying well—or paper over states that do not.

---

## SAVE Act — accurate description (both sides)

**What the bill does (mechanism, not slogan).** The Safeguard American Voter Eligibility (SAVE) Act (e.g. [H.R. 22, 119th Congress](https://www.congress.gov/bill/119th-congress/house-bill/22)) would amend the National Voter Registration Act to require **documentary proof of U.S. citizenship** when registering to vote in **federal** elections. Acceptable documents in the bill text commonly include REAL ID indicating citizenship, U.S. passport, military ID with U.S. birth record, or specified photo ID + citizenship document combinations; states must also establish a process for applicants who lack listed documents (other evidence + attestation) and take ongoing steps to remove noncitizens from rolls. It is aimed at **registration**, not a new universal rule for presenting citizenship papers at every ballot cast. Status: legislative proposal / House action in recent Congresses—**confirm current status before any public product**; not treated here as enacted law.

**Steelman support.** Citizenship is already required; without verification, the requirement is under-enforced; NVRA litigation history constrained state proof-of-citizenship rules; database access and removal duties close a statutory gap ([Heritage Action myth/fact](https://heritageaction.com/blog/myth-vs-fact-the-safeguard-american-voter-eligibility-act-h-r-22-s-128)).

**Steelman opposition.** Millions of citizens lack ready citizenship documents; re-registration and moves amplify burden; mail/online registration pathways break; failsafe may be chilled by penalties on officials; noncitizen voting is characterized as extremely rare ([Brennan opposition letter](https://www.brennancenter.org/our-work/research-reports/brennan-center-letter-congress-opposing-save-act)).

**CFMI posture (pre-score).** Score living text against Charter filters: transparency, least-coercive verification, false-positive safeguards, anti-opaque-discretion, competitive federalism (no commandeering theater). Neither “support because team” nor “oppose because team.” National magnitude of noncitizen voting remains **not established from public sources in this pass** as a single number—design debates must still confront verification gaps and access costs.

---

## CFMI response

How we weigh both sides against [CHARTER.md](../../CHARTER.md):

1. **What we accept** — Elections need auditable eligibility and custody rules; layered cyber/procedural controls are real; eligible citizens must not be casually purged; state variation matters; error ≠ fraud.  
2. **What we reject or narrow** — Security theater (rules that *look* strict but do not verify); anti-scrutiny narratives that treat mechanism questions as illegitimate; vibe-based “stolen election” claims; vibe-based “zero residual risk” claims; using contested fraud-rate estimates as settled fact.  
3. **Least-coercive path** — Prefer published objective match criteria, appeal/cure rights, paper ballots + meaningful post-election audits with **stated scope**, observer access, and verification tools that minimize false exclusion—before blunt criminalization of officials or performative mandates that do not improve measurement.  
4. **Domain note** — Primary frame is **constitutional process / anti-corruption / transparency**. Free-market filters apply where vendor monopolies or opaque contracting appear; they are not the lead story.  
5. **Bipartisan comment** — Open fix language should be reviewable by access advocates and integrity advocates; Charter hard limits still bind (no new rents for vendors or parties).

---

## Proposed approach

Under [ops/ai-investigation-architecture.md](../../ops/ai-investigation-architecture.md) and [ops/anti-narrative-capture.md](../../ops/anti-narrative-capture.md):

1. **Run Consensus claim tester** on slogans such as “mail voting is secure” and “the election was stolen” before scoring rhetoric.  
2. **Score** living bills (SAVE Act variants, state roll-maintenance bills, mail-voting expansions/restrictions) for mechanism, Hard Flags, and least-coercive design—not team affiliation.  
3. **Publish** narrative-vs-mechanism tables: what audits measure; list-maintenance data limits; custody rules by state sample.  
4. **Offer open fix language** that improves auditability and verification while protecting eligible registrants (cure, alternative evidence, published criteria).  
5. **Circulate** for bipartisan comment; human editor required; mark thin claims “not established.”

### I4 stress-test completed (mail ballots + rolls)

**Published:** [consensus-mail-ballots-voter-rolls-secure.md](../consensus-mail-ballots-voter-rolls-secure.md) (2026-08-02) — claim *“Mail-in balloting and voter rolls are secure.”*  
**Recommendation:** **NARROW** — layered controls are real; unqualified national “secure” is not established; no vibe reassurance and no stolen-election claims.

---

## Federal transparency package (companion)

**Published:** [federal-election-transparency-package.md](federal-election-transparency-package.md) · model outline [Federal Election Transparency and Citizenship Verification Standards Act](../../model-legislation/federal-election-transparency-and-audit-standards-act.md) (2026-08-02).

Constitutional path: Elections Clause floor for congressional (careful presidential) contests; transparency + citizenship verification for **federal** registrants; dual systems allowed; no commandeering of state/local offices; SAVE-style core kept/modified with stronger failsafe—not the whole package alone.

---

## Open questions (from I4 + ongoing)

1. Best public methodologies for state-comparable inactive / duplicate / death rates after ERIC exits?  
2. Empirical signature false-accept rates under production workloads (not only false-reject / cure stories)?  
3. Materiality of drop-box and chain-of-custody incidents after bipartisan canvass—case studies with official records?  
4. SAVE Act alternative-evidence path: workable in practice, or chilled by penalties on officials? *(see package Title VI anti-chill design)*  
5. Which states already publish list-quality KPIs (notices, removals, interstate matches, appeals) in machine-readable form? *(feeds Title II schema)*  
6. Named-state dig: what did 2022–2024 post-election audits **measure vs not** (ERIC member vs exit vs all-mail)?  
7. Legal standards for private roll challenges (standing, notice, deadlines) by state sample?  
8. Presidential-electors drafting: tightest severable federal floor that does not commandeer state offices—counsel review?  
9. Cost of machine-readable data + custody logging: formula grants vs bare mandate for Senate passability?  
10. Eligibility sampling distinct from RLA: feasible day-one floor or pilot-first?

Invite answers via [docs/feedback.html](../../docs/feedback.html) or a [counterevidence issue](https://github.com/scuba15steve7/cfmi/issues/new?template=counterevidence.yml).

---

## What would make reform passable

- **Access concern →** Robust alternative-evidence path, name-change procedures, fee waivers for birth certificates, clear timelines—so documentary rules are not de facto bans.  
- **Integrity concern →** Measurable list-quality metrics, interstate matching with due process, published removal statistics, custody logs—so “secure” is demonstrated, not asserted.  
- **Trust concern →** Audits with pre-committed scopes and public data; reject both “trust us” and “trust the viral thread.”  
- **Federalism concern →** Prefer competitive state improvement and transparent federal data access over opaque commandeering; evaluate NVRA amendments on text.

Passability never outranks the Charter: no performative theater, no anti-scrutiny gag norms, no unverified outcome claims as CFMI product.

---

## Improve this brief

CFMI uses public feedback so AI-assisted research can stay accurate and steelman both sides.

- **Suggest a correction or counterargument:** [docs/feedback.html](../../docs/feedback.html) · open a [counterevidence issue](https://github.com/scuba15steve7/cfmi/issues/new?template=counterevidence.yml)  
- Invite: state-specific custody statutes, RLA results with scope notes, better public measurement of list error rates, steelman defenses of current NVRA practice, or evidence that would change the least-coercive verification path.  
- Interest disclosure is mandatory. Educational research only.

---

### Charter fit (summary)

Fidelity to constitutional elections as republican process; radical transparency on methods and influence; anti-capture (CFMI must not become a messaging shop for either team); least-coercive instruments; competitive federalism. Free markets secondary—note vendor/contract opacity when it appears.

### Hooks to flag

- “‘Secure’ / ‘most secure’ without threat model or audit scope”  
- “Documentary proof of United States citizenship” / NVRA amendment patterns (SAVE-style)  
- Soft failsafe + criminal exposure for registrars (chilling alternative evidence)  
- List maintenance that cites activity without published accuracy metrics  
- Claims of national fraud percentages without methodology and adversarial review  
- Audit headlines that exceed what the audit measured
