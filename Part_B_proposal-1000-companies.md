# 1000 ICP-Qualified Company Proposal — 1 Month Plan

## Overview
Target: 1,000 genuinely ICP-qualified Federer companies across India.
Yield assumption: 10,000 raw → 3,000 rough filter → 1,200 scored → 1,000 final.
Tools: Claude API, Python, LinkedIn Sales Navigator, Screener/Tofler, PHARMEXCIL, Naukri API.

## Week 1 — Build Raw Universe (~10,000 companies)
Sources:
- MCA NIC code 21001 scrape filtered by 10 target states + paid-up capital >Rs.5Cr
- PHARMEXCIL USFDA-registered site full list
- Genome Valley + 7 other Pharma SEZ/PCPIR cluster tenant lists
- CPhI India 2023+2024 exhibitor lists
- LinkedIn Sales Navigator bulk export (pharma mfg, 50-500 employees, 10 cities)
- BioSpectrum India and PharmAcompass company databases

Tool: Python script to deduplicate, normalize names, add CIN for MCA cross-reference.
Expected output: ~9,000-10,000 unique raw companies.

## Week 2 — Automated Rough Filter (~3,000 surviving)
- Auto-disqualify: revenue >500Cr (Screener API), PE-owned (Tracxn), no website (URL checker)
- Segment + C1/C3 scoring via Claude API: feed company name + website → Claude classifies
- Human QC: spot-check 100 companies, recalibrate if >15% error rate
Expected output: ~3,000 companies passing rough filter.

## Week 3 — Full Federer Scoring (~1,200 companies)
- C4 (Tech DM): LinkedIn scrape → Claude classifies as technical/non-technical
- C5 (Sector): pre-built sector tailwind lookup table
- C6 (Growth): Naukri job count + Google News API + Tofler revenue trend
- Federer Score auto-calculated per company
Expected output: ~1,200 companies scoring 60+ (B-band or above).

## Week 4 — QC + Enrichment → Final 1,000
- 2-person team spot-checks 200 random companies
- False positive check: verify C1 for all borderline cases
- Enrichment: DM name + LinkedIn URL + personalization hook (Claude generates from website)
- Flag ~150 borderline C-band companies for human review before outreach
Expected output: 1,000 companies with full score, DM contact, hook, confidence rating.

## Yield Table
10,000 raw → 3,000 filter (30%) → 1,200 scored → 1,000 final (83%)

## Quality Control: 3 Layers
1. Automated: regex/API checks for all auto-disqualifiers
2. Sampling: 200-company human spot-check in Week 4
3. Outreach feedback: track reply rates, iterate Claude scoring prompt if accuracy drops

## Sourcing Methods (Q1)
1. PHARMEXCIL Database — USFDA-registered Indian mfg sites
2. MCA/Tofler — NIC code 21001 filtered by city + revenue band
3. Genome Valley / Pharma SEZ tenant lists — curated manufacturer clusters
4. USFDA Site Registration Database — directly identifies USFDA-compliant manufacturers
5. LinkedIn Sales Navigator — real-time hiring + DM research in one tool
6. CPhI India Exhibitor Lists — intent-signaling, growth-oriented companies
7. PLI Scheme Beneficiary List — government-curated specialty API manufacturers
8. Indian Patent Office (IPO) Database — companies with recent pharma patents = R&D active
9. Zauba/Volza Export Data — real transaction data, revenue-adjacent signal
10. DSIR-Recognized R&D Lab List — government-verified R&D investment signal
