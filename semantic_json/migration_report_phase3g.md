# Phase 3G — Final minor semantic fixes

Only the eight requested MINOR_FIX documents were modified. Existing chunk boundaries and exact source spans were preserved. No raw or production RAG files were modified.

## Chunk counts and boundary changes

- `Fr_Indicateurs_climat_investissement.json`: 14 → 14 chunks; boundary changes: 0
- `ENG_Indicateurs_climat_investissement.json`: 14 → 14 chunks; boundary changes: 0
- `ESP_Indicateurs_climat_investissement.json`: 14 → 14 chunks; boundary changes: 0
- `Guide_de_Conciliation_AR.json`: 7 → 7 chunks; boundary changes: 0
- `Guide_de_Conciliation_ES.json`: 7 → 7 chunks; boundary changes: 0
- `Guide_programme_integre_appui_financement_entreprises_AR.json`: 3 → 3 chunks; boundary changes: 0
- `Brochure_secteur_Logistique.json`: 6 → 6 chunks; boundary changes: 0
- `FR_Chiffres_cles_CRITTA_30_Sept_2024.json`: 14 → 14 chunks; boundary changes: 0

## Investment-climate multilingual alignment

The FR/EN/ES 14-unit structures were preserved. Equivalent units now share canonical tags for business climate, investor profile, export destinations, investor satisfaction, investment motivation, sustainability, CRI support, future expectations, improvement priorities, and regional attractiveness. Source-language headings remain localized. No explicit survey/reference year was sufficiently supported, so document periods remain null.

## Conciliation corrections

AR and ES boundaries were preserved. Cover/contact is `contact_information`; editorial/definition/role units are `narrative` or `faq`; request requirements are `eligibility_conditions`; process steps are `procedure`. Canonical tags distinguish definition, missions, request, conditions, process, and conciliator role.

## Integrated financing corrections

The Arabic programme now distinguishes overview (`narrative`), financing offer (`financial_product`), and programme beneficiaries/requirements (`eligibility_conditions`). Tags include financing programme, products, conditions, beneficiaries, and business support.

## Logistics corrections

The brochure retains six coherent units. Tags/content types now distinguish strategy, infrastructure/statistics, Fnideq economic zone (`industrial_zone`), Tanger Med statistics/infrastructure, and the operator directory (`table` plus contact semantics).

## CRUI 30 September 2024 correction

Document reference period is now `year=2024`, `type=as_of_date`, `quarter=3`, `label=Au 30 septembre 2024`, `end_date=2024-09-30`. Historical 2021–2023 charts and the 30 August 2023 business-creation statistic retain their own years instead of inheriting the report date. Repeated slogan headings were replaced with indicator-specific French headings.

## Metadata topics and content types

- `Fr_Indicateurs_climat_investissement.json`: metadata.topics PASS; content types: {'statistics': 14}
- `ENG_Indicateurs_climat_investissement.json`: metadata.topics PASS; content types: {'statistics': 14}
- `ESP_Indicateurs_climat_investissement.json`: metadata.topics PASS; content types: {'statistics': 14}
- `Guide_de_Conciliation_AR.json`: metadata.topics PASS; content types: {'contact_information': 1, 'narrative': 2, 'faq': 2, 'eligibility_conditions': 1, 'procedure': 1}
- `Guide_de_Conciliation_ES.json`: metadata.topics PASS; content types: {'contact_information': 1, 'narrative': 2, 'faq': 2, 'eligibility_conditions': 1, 'procedure': 1}
- `Guide_programme_integre_appui_financement_entreprises_AR.json`: metadata.topics PASS; content types: {'narrative': 1, 'financial_product': 1, 'eligibility_conditions': 1}
- `Brochure_secteur_Logistique.json`: metadata.topics PASS; content types: {'narrative': 2, 'statistics': 2, 'industrial_zone': 1, 'table': 1}
- `FR_Chiffres_cles_CRITTA_30_Sept_2024.json`: metadata.topics PASS; content types: {'statistics': 12, 'investment_opportunity': 1, 'contact_information': 1}

## Temporal metadata summary

- Climate FR/EN/ES: publication/reference periods remain null because no reliable survey edition date was established.
- Conciliation AR/ES: no explicit edition date retained.
- Integrated financing AR: no explicit publication year retained.
- Logistics brochure: no reliable publication year retained.
- CRUI: explicit as-of date represented at document level and on current-report statistic chunks.

## Exact provenance validation

Phase-specific exact provenance validation: PASS for all eight documents. Source spans, page bounds, and chunk text were unchanged and continue to match raw pages exactly.

## Canonical validator

PASS for all eight documents using `scripts/validate_semantic_json.py --source-dir data/raw/json`.

## Raw SHA-256 integrity

| File | Before | After | Unchanged |
|---|---|---|---|
| `Fr_Indicateurs_climat_investissement.json` | `294E2716329800101FB4160415D09531F5AB0056B06220424F050BEDA939EC53` | `294E2716329800101FB4160415D09531F5AB0056B06220424F050BEDA939EC53` | yes |
| `ENG_Indicateurs_climat_investissement.json` | `6105F9A65D6812B3776E23B78BE4639674E0A4A6BB1C447D9BBB42DEBDF3BD9F` | `6105F9A65D6812B3776E23B78BE4639674E0A4A6BB1C447D9BBB42DEBDF3BD9F` | yes |
| `ESP_Indicateurs_climat_investissement.json` | `FCD3636D53ED268F129F05E80416E3D923F8D6F6EF38A3859F6DC0DC5A3E6A7A` | `FCD3636D53ED268F129F05E80416E3D923F8D6F6EF38A3859F6DC0DC5A3E6A7A` | yes |
| `Guide_de_Conciliation_AR.json` | `6A5E32CFB2B134DA01DF3A70518D4F86C0534D6B36981DC6FE247773012D8BB4` | `6A5E32CFB2B134DA01DF3A70518D4F86C0534D6B36981DC6FE247773012D8BB4` | yes |
| `Guide_de_Conciliation_ES.json` | `824DD5BC30536BC5128BBD0BB82689B555D5B3DCFC47AE58A5F700CA96428DB2` | `824DD5BC30536BC5128BBD0BB82689B555D5B3DCFC47AE58A5F700CA96428DB2` | yes |
| `Guide_programme_integre_appui_financement_entreprises_AR.json` | `285EE42FBEE64F602558610A619273FE83B1F9F20C1B51EB782C7963361FFA6E` | `285EE42FBEE64F602558610A619273FE83B1F9F20C1B51EB782C7963361FFA6E` | yes |
| `Brochure_secteur_Logistique.json` | `BBDCF8A721976A6A9980BC9BC6D836C2A8778ECCBCA2241BC75CE00E4BB13830` | `BBDCF8A721976A6A9980BC9BC6D836C2A8778ECCBCA2241BC75CE00E4BB13830` | yes |
| `FR_Chiffres_cles_CRITTA_30_Sept_2024.json` | `A1C89BB550EBEF09592C362F9C04AC68608B9E9B272BF2645D8006640A2F70F0` | `A1C89BB550EBEF09592C362F9C04AC68608B9E9B272BF2645D8006640A2F70F0` | yes |

## Remaining manual review

- Verify the climate survey reference period from the original publication metadata if a dated edition marker exists outside extracted text.
- Confirm whether the CRUI page 13 TDC2023 finalists should be treated as `investment_opportunity` or an event/statistics unit in a later application-specific review.
- Review OCR quality of Arabic conciliation headings; raw text was intentionally preserved.
