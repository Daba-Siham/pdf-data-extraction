# Phase 3F.1 — Content-based NEWS verification

## Scope

This was a read-only verification of the three phase-3F news documents. No semantic JSON, raw JSON, non-news family, RAG, or vector-store file was modified. Current units were checked against their own raw page text and then compared cross-lingually using subject, headings, named entities, statistics, and project/event context.

## Units checked

- FR: `Manar_Al_Moustatmir_News.json` — 31 units checked; exact-span diagnostics: PASS
- EN: `Manar_Al_Moustatmir_ENG_PNG.json` — 31 units checked; exact-span diagnostics: PASS
- AR: `Akhbar_Al_Moustatmir_News.json` — 30 units checked; exact-span diagnostics: PASS

Article boundaries confirmed: FR 31/31, EN 31/31, AR 30/30. Corrected boundaries: 0. Current ranges are supported by the source editorial headings and page-level starts/ends; no affected range contained two independent articles requiring a safe partial-page split.

## Boundary verification

| Edition | Current multi-page unit | Content evidence | Assessment |
|---|---|---|---|
| FR | 2–5 editorial | pages 2–3 contain the royal quotation; pages 4–5 contain the editorial continuation and 2023 CRUI/investment context | confirmed |
| EN | 2–5 editorial | pages 2–3 contain the quotation; pages 4–5 are the English editorial continuation | confirmed |
| AR | 2–5 editorial | Arabic quotation and editorial continuation are contiguous | confirmed |
| FR/EN | 11–12 tourism dossier | section cover/introduction followed by the tourism dossier opening | confirmed |
| AR | 11–12 tourism dossier | Arabic tourism dossier opening and regional framing | confirmed |
| FR/EN | 23–24 entrepreneurship | business creation ranking and sector distribution continue across both pages | confirmed |
| AR | 23–24 entrepreneurship | regional business-creation statistic and sector distribution continue across both pages | confirmed |
| FR/EN/AR | 25–26 CRUI | CRUI 2023 activity figures followed by investment/job trend charts | confirmed |
| FR/EN | 31–32 aquaculture | section cover followed by marine aquaculture/hatchery feature | confirmed |
| AR | 31–32 aquaculture | Arabic section cover followed by hatchery/aquaculture context | confirmed |
| FR/EN | 33–36 Aquago | one interview with sequential questions on project rationale, administration, studies, and CRI support | confirmed |
| AR | 33–35 Aquago | one Arabic Aquago interview with sequential questions and answers | confirmed |
| FR/EN | 37–41 ANDA | one ANDA director interview with sequential aquaculture questions and future outlook | confirmed |
| AR | 36–39 ANDA | one Arabic ANDA interview with process, challenges, and future perspectives | confirmed |
| FR/EN | 44–46 featured projects | company/project cards continue across the three pages | confirmed |
| AR | 41–43 featured projects | Arabic company/project cards continue across the three pages | confirmed |

No boundary correction was necessary. The AR later layout is different from FR/EN and was verified independently rather than inherited from their page ranges.

## Multilingual alignment table

| Canonical concept | FR pages | EN pages | AR pages | Evidence | Assessment |
|---|---:|---:|---:|---|---|
| `edition_2023` | 1–1 | 1–1 | 1–1 | 2023 edition title/editorial | confirmed_equivalent |
| `tourism` | 11–12 | 11–12 | 11–12 | special tourism dossier, named territories and tourism assets | confirmed_equivalent |
| `crui_activity` | 25–26 | 25–26 | 25–26 | CRUI statistics, approved acts/projects and PIAFE context | confirmed_equivalent |
| `conciliation` | 28–28 | 28–28 | 28–28 | 148 resolved conciliation files/cases | confirmed_equivalent |
| `aquaculture` | 31–32 | 31–32 | 31–32 | aquaculture focus and hatchery context | confirmed_equivalent |
| `aquago_interview` | 33–36 | 33–36 | 33–35 | Aquago marine-fish-hatchery interview and administrative/technical questions | confirmed_equivalent |
| `anda_interview` | 37–41 | 37–41 | 36–39 | ANDA director interview, aquaculture policy and future perspectives | confirmed_equivalent |
| `guides` | 43–43 | 43–43 | 40–40 | guide/brochure announcement; Arabic edition begins this material at page 40 | likely_equivalent |
| `project_announcement` | 29–29 | 29–29 | 29–29 | TDC2023 call and territorial-promotion events | likely_equivalent |
| `featured_projects` | 44–46 | 44–46 | 41–43 | company/project cards with activity, investment, jobs and location | likely_equivalent |
| `contact_information` | 47–47 | 47–47 | 44–44 | CRI contact block | confirmed_equivalent |

The alignment assessment is content-based. Shared facts include the 2023 edition, CRUI activity, 148 conciliation cases, aquaculture/hatchery coverage, Aquago and ANDA interviews, and company/project cards. Tourism territory profiles are conceptually aligned but individual wording and visual layout differ. No incorrect alignment was found; likely-equivalent items remain marked because the editions use different layouts or extraction quality.

## Titles and OCR

- FR headings are readable enough for the current conservative titles.
- EN pages 10, 13–18 and some project/event cards contain OCR fragments in raw extraction, but the semantic headings are source-language English and identity is supported by readable surrounding content.
- AR contains mixed-language cover material and OCR artifacts; the semantic headings use conservative Arabic descriptions rather than copying broken fragments.
- Raw source text and source spans were not changed.

## Temporal metadata

All three documents retain explicit edition year 2023. Article-level historical/current years remain in `years_mentioned`; no article-specific year was replaced by 2023.

## Metadata topics

- FR: PASS — metadata.topics equals the exact union of chunk semantic_tags.
- EN: PASS — metadata.topics equals the exact union of chunk semantic_tags.
- AR: PASS — metadata.topics equals the exact union of chunk semantic_tags.

## Validation

Phase-specific exact provenance validation: PASS for FR, EN, and AR. Every source span is a non-empty exact substring of its corresponding raw page; page bounds and ordered chunk text are consistent.

Canonical validator: PASS for all three news documents using `scripts/validate_semantic_json.py --source-dir data/raw/json`.

## Raw SHA-256 integrity

| File | SHA-256 after verification | Unchanged during audit |
|---|---|---|
| `Manar_Al_Moustatmir_News.json` | `EEDB674ECF83F998F82C32C0141C1B45995AC608AB3D841476438A4C47FED0A9` | yes |
| `Manar_Al_Moustatmir_ENG_PNG.json` | `302A39A4AB553092100106FBCC8F0F1D4B31B5820A3FB1C35E297B8A7CC07BC5` | yes |
| `Akhbar_Al_Moustatmir_News.json` | `374043D95A534BF79C5BC8286E2AA08FECE2697BEFC39C03327D8FCA65D4F641` | yes |

## Final result

- Confirmed alignments: 8 core concepts.
- Likely-equivalent alignments: guides, promotion/project announcements, and featured project cards.
- Edition-specific units: tourism territory profiles and some event/company card wording/layouts.
- Incorrect alignments corrected: 0.
- Unresolved units: 0 boundary failures; OCR rendering review remains advisable for selected EN/AR pages.
- News documents are suitable for the next semantic-loader phase, subject to the documented OCR caveat.
