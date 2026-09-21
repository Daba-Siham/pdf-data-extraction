# Phase 3F — Substantial semantic refinement

Only the seven phase-3E `REFINE` documents were modified. Raw JSON, previously reviewed families, and the production RAG stack were not modified.

## Documents and chunk counts

- `Manar_Al_Moustatmir_News.json`: 31 → 31 chunks; types: {'statistics': 8, 'narrative': 12, 'service': 3, 'investment_opportunity': 5, 'faq': 2, 'contact_information': 1}
- `Manar_Al_Moustatmir_ENG_PNG.json`: 31 → 31 chunks; types: {'statistics': 8, 'narrative': 12, 'service': 3, 'investment_opportunity': 5, 'faq': 2, 'contact_information': 1}
- `Akhbar_Al_Moustatmir_News.json`: 30 → 30 chunks; types: {'statistics': 7, 'narrative': 12, 'service': 3, 'investment_opportunity': 5, 'faq': 2, 'contact_information': 1}
- `Guide_branchement_electricite_eau_assainissement.json`: 13 → 13 chunks; types: {'narrative': 2, 'service': 3, 'procedure': 7, 'contact_information': 1}
- `Nv_Guide_Cout_facteurs_CRI_2024.json`: 37 → 37 chunks; types: {'narrative': 4, 'table': 15, 'cost_information': 10, 'legal_information': 3, 'statistics': 2, 'service': 2, 'contact_information': 1}
- `Investment_Business_Support_Single_Window_FR.json`: 12 → 12 chunks; types: {'narrative': 1, 'service': 9, 'procedure': 1, 'contact_information': 1}
- `Investment_Business_Support_Single_Window_ES.json`: 12 → 12 chunks; types: {'narrative': 1, 'service': 9, 'procedure': 1, 'contact_information': 1}

## News article units and multilingual alignment

The three editions were split into independent event, tourism, statistics, support, conciliation, aquaculture interview/FAQ, guide, project-announcement, and contact units. FR/EN follow the same editorial concepts; AR has a shorter layout and was aligned only where subject and named context support equivalence. Alignment is semantic, not ordinal.

| Canonical concept | FR | EN | AR | Assessment |
|---|---|---|---|---|
| `news_edition_2023` / editorial | yes | yes | yes | aligned |
| `tourism` territorial feature | yes | yes | yes | aligned conceptually |
| `crui_activity` | yes | yes | yes | aligned |
| `conciliation` | yes | yes | yes | aligned |
| `aquaculture_aquago_interview` | yes | yes | yes | aligned |
| `anda_aquaculture_interview` | yes | yes | yes | aligned |
| `project_announcement` / trusted projects | yes | yes | yes | likely equivalent; layout differs |
| `contact_information` | yes | yes | yes | aligned |

Some tourism territory pages and individual event cards are edition-specific in wording; they were not forced into identical chunk counts.

## Cost-guide categories created

The 2024 cost guide now separates company creation, architecture, land, construction materials, construction, labor/legal calendar/social charges, insurance, electricity, water, transport modes, customs, certification, telecom/banking, training, production-cost comparison, quality of life, and contact information. Tables remain intact as coherent table units.

## Utility procedures created

The utility guide now separates electricity overview, provisional/low-voltage/medium-voltage connections, electrical workflow, water/sanitation overview, provisional water, fire connection, AEP/fire workflow, and contacts. The unsupported 2002 publication metadata was removed; historical 2002 remains only where present in chunk text/year metadata.

## Single-window services created

FR and ES now share canonical concepts for CRI role, investor services, Manar digital requests, incentives/financing, territorial intelligence, entrepreneurship/innovation, investment procedures, Investangier Academy, single-window support, guide announcement, and contact information. The previous 2019 publication metadata was cleared because the source pages inspected did not provide a reliable explicit edition marker.

## Temporal and OCR corrections

- News documents use explicit edition year 2023 at document level; article years remain in `years_mentioned` and are not overwritten.
- Cost guide uses explicit 2024 edition metadata; table-specific explicit years remain in chunk `years_mentioned`.
- Utility guide no longer claims publication year 2002.
- Single-window publication year is null pending an explicit edition marker.
- Unusable fixed-group headings were replaced with conservative source-language semantic titles; raw source text is unchanged.

## Metadata topics consistency

- `Manar_Al_Moustatmir_News.json`: PASS — exact union of chunk tags.
- `Manar_Al_Moustatmir_ENG_PNG.json`: PASS — exact union of chunk tags.
- `Akhbar_Al_Moustatmir_News.json`: PASS — exact union of chunk tags.
- `Guide_branchement_electricite_eau_assainissement.json`: PASS — exact union of chunk tags.
- `Nv_Guide_Cout_facteurs_CRI_2024.json`: PASS — exact union of chunk tags.
- `Investment_Business_Support_Single_Window_FR.json`: PASS — exact union of chunk tags.
- `Investment_Business_Support_Single_Window_ES.json`: PASS — exact union of chunk tags.

## Chunk-size diagnostics

| Document | Chunks | Min | Median | Mean | Max | >3k | >5k | >8k | >12k |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Manar_Al_Moustatmir_News.json | 31 | 91 | 697.0 | 1382.2 | 8497 | 4 | 2 | 1 | 0 |
| Manar_Al_Moustatmir_ENG_PNG.json | 31 | 73 | 908.0 | 1478.6 | 7505 | 4 | 2 | 0 | 0 |
| Akhbar_Al_Moustatmir_News.json | 30 | 99 | 516.0 | 1061.0 | 6222 | 4 | 1 | 0 | 0 |
| Guide_branchement_electricite_eau_assainissement.json | 13 | 29 | 1880.0 | 1531.3 | 2966 | 0 | 0 | 0 | 0 |
| Nv_Guide_Cout_facteurs_CRI_2024.json | 37 | 9 | 1003.0 | 1270.0 | 5429 | 2 | 1 | 0 | 0 |
| Investment_Business_Support_Single_Window_FR.json | 12 | 181 | 1364.5 | 1246.8 | 2024 | 0 | 0 | 0 | 0 |
| Investment_Business_Support_Single_Window_ES.json | 12 | 185 | 1263.0 | 1212.2 | 2130 | 0 | 0 | 0 | 0 |

### Recommended for retrieval subchunking (report only)

- `Manar_Al_Moustatmir_News.json` `manar_al_moustatmir_news_phase3f_0026`: 5999 characters, pages 33–36
- `Manar_Al_Moustatmir_News.json` `manar_al_moustatmir_news_phase3f_0027`: 8497 characters, pages 37–41
- `Manar_Al_Moustatmir_ENG_PNG.json` `manar_al_moustatmir_eng_png_phase3f_0026`: 5667 characters, pages 33–36
- `Manar_Al_Moustatmir_ENG_PNG.json` `manar_al_moustatmir_eng_png_phase3f_0027`: 7505 characters, pages 37–41
- `Akhbar_Al_Moustatmir_News.json` `akhbar_al_moustatmir_news_phase3f_0027`: 6222 characters, pages 36–39
- `Nv_Guide_Cout_facteurs_CRI_2024.json` `nv_guide_cout_facteurs_cri_2024_phase3f_0024`: 5429 characters, pages 40–43

## Validation

Phase-specific exact provenance validation: PASS for all seven documents. Every span is a non-empty exact substring of its raw page; page bounds and ordered text concatenation are consistent.

Canonical validator: PASS for all seven documents using `scripts/validate_semantic_json.py --source-dir data/raw/json`.

## Raw SHA-256 integrity

| File | Before | After | Unchanged |
|---|---|---|---|
| `Manar_Al_Moustatmir_News.json` | `EEDB674ECF83F998F82C32C0141C1B45995AC608AB3D841476438A4C47FED0A9` | `EEDB674ECF83F998F82C32C0141C1B45995AC608AB3D841476438A4C47FED0A9` | yes |
| `Manar_Al_Moustatmir_ENG_PNG.json` | `302A39A4AB553092100106FBCC8F0F1D4B31B5820A3FB1C35E297B8A7CC07BC5` | `302A39A4AB553092100106FBCC8F0F1D4B31B5820A3FB1C35E297B8A7CC07BC5` | yes |
| `Akhbar_Al_Moustatmir_News.json` | `374043D95A534BF79C5BC8286E2AA08FECE2697BEFC39C03327D8FCA65D4F641` | `374043D95A534BF79C5BC8286E2AA08FECE2697BEFC39C03327D8FCA65D4F641` | yes |
| `Guide_branchement_electricite_eau_assainissement.json` | `F819E95CC3714532976B30DAB1EF8B4E76A201F03CEC6FDBE78CD859F9072354` | `F819E95CC3714532976B30DAB1EF8B4E76A201F03CEC6FDBE78CD859F9072354` | yes |
| `Nv_Guide_Cout_facteurs_CRI_2024.json` | `7A00656783CC67C48920269CE3D7EE263B20DC73AA122366BA69BA82B48665D1` | `7A00656783CC67C48920269CE3D7EE263B20DC73AA122366BA69BA82B48665D1` | yes |
| `Investment_Business_Support_Single_Window_FR.json` | `22157D3D489F8964FFA0AF2209CE8B7C690020A638C48F88CE8E585DA7A26526` | `22157D3D489F8964FFA0AF2209CE8B7C690020A638C48F88CE8E585DA7A26526` | yes |
| `Investment_Business_Support_Single_Window_ES.json` | `9BEFBB8644EB2F8E8BB1E3B7B7A7BB72BDEC1C39367054198F64DA3CCA4C7931` | `9BEFBB8644EB2F8E8BB1E3B7B7A7BB72BDEC1C39367054198F64DA3CCA4C7931` | yes |

## Remaining manual review

- Review visual PDF renderings for English/Arabic news pages where OCR headings remain degraded.
- Confirm whether single-window guides have an explicit edition year outside the extracted page text before assigning one.
- Review cost-guide table subcategories during later retrieval design; semantic parents were retained without arbitrary character splitting.
