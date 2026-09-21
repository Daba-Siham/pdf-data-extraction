# Semantic JSON migration report — phase 1

Generated: 2026-09-19T13:29:52.684617+00:00

## Scope

Only one representative document was converted. All 33 source JSON files were inspected. No file in `data/raw/json` was written or modified.

## Corpus inventory

- Source JSON files inspected: 33
- Languages by file: French 13, English 7, Spanish 7, Arabic 6
- Main recurring families: CRI presentation; CRUI first-semester 2024 key figures; 2025 key figures; investment-climate indicators; industrial-zones panorama; Manar Al Moustatmir News; conciliation guides; investment/business support single-window guides; territorial-opportunity investor guides.
- Standalone/single-language subjects: financing guide, utility-connection procedure guide, integrated business-support/financing programme, production-factor cost guide, logistics brochure.

## Document-family inventory

| Proposed family ID | Corresponding subject | Languages | Type | Period/uncertainty |
|---|---|---|---|---|
| `cri_presentation` | CRI TTA presentation | fr, en, es, ar | `presentation` | No explicit publication period identified from filenames/content. |
| `crui_key_figures_2024_h1` | CRUI key figures, first semester 2024 | fr, en, es, ar | `statistics` | Reference period is the first semester of 2024. |
| `chiffres_cles_2025` | 2025 key figures | fr, en, es, ar | `annual_key_figures` | Primary reference year is 2025; individual pages can mention other dates. |
| `investment_climate_indicators` | Investment climate indicators | fr, en, es | `business_climate_report` | No single publication year reliably identified from filenames/content. |
| `industrial_zones_panorama` | Industrial/economic zones panorama | fr, en, es | `industrial_zones_panorama` | No single publication year reliably identified from filenames/content. |
| `manar_al_moustatmir_news_2023` | Manar Al Moustatmir News, issue 1 | fr, en, ar | `news_or_annual_review` | The three files have matching 2023 issue structure; family assignment is based on content/title correspondence. |
| `conciliation_guide` | Conciliation guide | ar, es | `guide` | Multilingual family inferred from matching guide title and structure. |
| `investment_business_support_single_window` | Investment and business support single window | fr, es | `service_guide` | Multilingual family inferred from matching title and structure. |
| `investors_guide_territorial_opportunities` | Investors guide to territorial opportunities | fr, en | `investors_guide` | Multilingual family inferred from matching title and subject. |
| `financing_guide` | Guide du financement des entreprises | fr | `financing_guide` | French-only guide; source content identifies 2022 in the opening material. |
| `electricity_water_sanitation_connection` | Large-account utility connection guide | fr | `procedure_guide` | French-only procedural guide. |
| `integrated_business_support_financing` | Integrated business support and financing programme | ar | `financial_product_or_programme` | Arabic-only programme document; no family counterpart identified. |
| `production_factor_cost_guide_2024` | Cost of production factors | fr | `cost_information_guide` | Reference/edition year is 2024. |
| `logistics_sector_brochure` | Logistics sector brochure | fr | `sector_brochure` | No single publication year reliably identified from filename/content. |

Family IDs are proposed from filename/title/content correspondence. They should be reviewed before converting the remaining documents, especially the Manar/Akhbar news files and files with OCR-heavy titles.

## Representative document

- Source file: `data/raw/json/FR_Chiffres_cles_annee_2025.json`
- Document ID: `fr_chiffres_cles_annee_2025` (preserved exactly)
- Document family: `chiffres_cles_2025`
- Detected title: `L’année 2025 — Dynamique d’investissement`
- Language: `fr`
- Document type: `annual_key_figures`
- Publisher: `CRI Tanger-Tétouan-Al Hoceima` (the requested corpus default; the source identifies the CRI/Investangier institution)
- Region: `Tanger-Tétouan-Al Hoceima`
- Publication year: `2025`, supported by the cover/title and repeated 2025 references
- Primary reference period: year 2025
- Reference-period caveat: page 14 includes events from 2023–2026 and page 16 reports a mid-February 2026 balance; those page-level dates remain in source text and are not promoted to the document-level period.

## Sections and subsections

### 2025 investment dynamics

- Annual overview: `fr_chiffres_cles_annee_2025_p01_c01` (pages 1-1)

### Business creation

- New companies and sector breakdown: `fr_chiffres_cles_annee_2025_p02_c01` (pages 2-2), `fr_chiffres_cles_annee_2025_p03_c01` (pages 3-3)

### CRUI report

- CRUI activity and approved investment files: `fr_chiffres_cles_annee_2025_p04_c01` (pages 4-4), `fr_chiffres_cles_annee_2025_p05_c01` (pages 5-5), `fr_chiffres_cles_annee_2025_p06_c01` (pages 6-6)

### Sector investment dynamics

- Industrial investment: `fr_chiffres_cles_annee_2025_p07_c01` (pages 7-7)
- Tourism investment: `fr_chiffres_cles_annee_2025_p08_c01` (pages 8-8)
- Energy investment: `fr_chiffres_cles_annee_2025_p09_c01` (pages 9-9)

### Business support and entrepreneurship

- Business support services: `fr_chiffres_cles_annee_2025_p10_c01` (pages 10-10)
- PIAFE financing: `fr_chiffres_cles_annee_2025_p11_c01` (pages 11-11)
- Conciliation and dispute resolution: `fr_chiffres_cles_annee_2025_p12_c01` (pages 12-12)
- Open innovation competition: `fr_chiffres_cles_annee_2025_p13_c01` (pages 13-13)

### Promotion and partnerships

- Territorial promotion and investment opportunities: `fr_chiffres_cles_annee_2025_p14_c01` (pages 14-14)
- Support for Moroccans of the World: `fr_chiffres_cles_annee_2025_p15_c01` (pages 15-15)
- TPME investment support programme: `fr_chiffres_cles_annee_2025_p16_c01` (pages 16-16)
- Strategic partnership with IFC: `fr_chiffres_cles_annee_2025_p17_c01` (pages 17-17)

### Closing message

- Closing slogan: `fr_chiffres_cles_annee_2025_p18_c01` (pages 18-18)

## Chunk/page mapping

- Generated semantic chunks: **18**

| Chunk ID | Content type | Page(s) | Semantic location |
|---|---|---:|---|
| `fr_chiffres_cles_annee_2025_p01_c01` | `narrative` | 1-1 | 2025 investment dynamics → Annual overview |
| `fr_chiffres_cles_annee_2025_p02_c01` | `statistics` | 2-2 | Business creation → New companies and sector breakdown |
| `fr_chiffres_cles_annee_2025_p03_c01` | `table` | 3-3 | Business creation → New companies and sector breakdown |
| `fr_chiffres_cles_annee_2025_p04_c01` | `statistics` | 4-4 | CRUI report → CRUI activity and approved investment files |
| `fr_chiffres_cles_annee_2025_p05_c01` | `statistics` | 5-5 | CRUI report → CRUI activity and approved investment files |
| `fr_chiffres_cles_annee_2025_p06_c01` | `table` | 6-6 | CRUI report → CRUI activity and approved investment files |
| `fr_chiffres_cles_annee_2025_p07_c01` | `industrial_zone` | 7-7 | Sector investment dynamics → Industrial investment |
| `fr_chiffres_cles_annee_2025_p08_c01` | `investment_opportunity` | 8-8 | Sector investment dynamics → Tourism investment |
| `fr_chiffres_cles_annee_2025_p09_c01` | `statistics` | 9-9 | Sector investment dynamics → Energy investment |
| `fr_chiffres_cles_annee_2025_p10_c01` | `service` | 10-10 | Business support and entrepreneurship → Business support services |
| `fr_chiffres_cles_annee_2025_p11_c01` | `statistics` | 11-11 | Business support and entrepreneurship → PIAFE financing results |
| `fr_chiffres_cles_annee_2025_p12_c01` | `service` | 12-12 | Business support and entrepreneurship → Conciliation and dispute resolution |
| `fr_chiffres_cles_annee_2025_p13_c01` | `statistics` | 13-13 | Business support and entrepreneurship → Open innovation competition results |
| `fr_chiffres_cles_annee_2025_p14_c01` | `investment_opportunity` | 14-14 | Promotion and partnerships → Territorial promotion and investment opportunities |
| `fr_chiffres_cles_annee_2025_p15_c01` | `service` | 15-15 | Promotion and partnerships → Support for Moroccans of the World |
| `fr_chiffres_cles_annee_2025_p16_c01` | `service` | 16-16 | Promotion and partnerships → TPME investment support programme |
| `fr_chiffres_cles_annee_2025_p17_c01` | `investment_opportunity` | 17-17 | Promotion and partnerships → Strategic partnership with IFC |
| `fr_chiffres_cles_annee_2025_p18_c01` | `narrative` | 18-18 | Closing message → Closing slogan |

Every useful source page (1–18) is represented exactly once. Chunk text is copied from the corresponding original page text and joined only with a blank line when multiple pages are used; no translation or generated summary was applied.

## Uncertainty and classification notes

- The document-level publication year and annual reference period are reliable from the title/cover, but the document contains page-level historical/future event dates.
- Page 7 combines industrial investment statistics and named industrial zones; `industrial_zone` was selected because the zone entities are central to the page.
- Page 8 combines tourism statistics and territorial investment information; it is classified as `investment_opportunity`.
- Page 11 reports PIAFE financing results but does not describe product terms, so it is classified as `statistics`.
- Page 13 reports open-innovation competition results, so it is classified as `statistics`, not as a financial product.
- Page 16 mentions eligibility conditions and premiums but does not enumerate the conditions; it is classified as `service` rather than asserting eligibility facts.
- No FAQ, contact-information, legal-information, procedure, or cost-information chunk was identified in this representative document.
- No aggressive OCR cleanup was applied. Source text contains layout markers, URLs, page-number artifacts, and possible OCR irregularities; these remain preserved.

## Validation

- JSON parsing: passed
- UTF-8 read/write: passed
- Required schema fields: passed
- Document ID preservation: passed
- Useful-page coverage: passed
- Exact source-page text preservation: passed

No validation errors.
