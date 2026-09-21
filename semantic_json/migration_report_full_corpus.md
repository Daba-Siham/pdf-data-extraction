# Full corpus semantic JSON migration report

## Summary

- Raw documents discovered: 33
- Semantic documents present: 33
- Documents converted in this run: 31
- Documents skipped: 0
- Total semantic chunks: 767
- Languages: ar: 6, en: 7, es: 7, fr: 13

## Document inventory

| Source file | document_id | family | language | type | chunks |
|---|---|---|---|---|---|
| `AR_Presentation_CRI_TTA.json` | `ar_pr_sentation_cri_tta_vf` | `cri_presentation` | `ar` | `institutional_presentation` | 20 |
| `Akhbar_Al_Moustatmir_News.json` | `akhbar_al_moustatmir_news` | `manar_al_moustatmir_news_2023` | `ar` | `news_review` | 15 |
| `Arabe_Chiffres_cles_2025.json` | `arabe_chiffres_cles_2025` | `chiffres_cles_2025` | `ar` | `key_figures` | 18 |
| `Brochure_secteur_Logistique.json` | `brochure_secteur_logistique` | `logistics_sector_brochure` | `fr` | `sector_brochure` | 6 |
| `Chiffres_cles_CRUI_1er_semestre_2024_Anglais.json` | `chiffres_cles_crui_1er_semestre_2024_anglais` | `crui_key_figures_2024_h1` | `en` | `key_figures` | 7 |
| `Chiffres_cles_CRUI_1er_semestre_2024_Arabe.json` | `chiffres_cles_crui_1er_semestre_2024_arabe` | `crui_key_figures_2024_h1` | `ar` | `key_figures` | 7 |
| `Chiffres_cles_CRUI_1er_semestre_2024_Espagnol.json` | `chiffres_cles_crui_1er_semestre_2024_espagnol` | `crui_key_figures_2024_h1` | `es` | `key_figures` | 7 |
| `Chiffres_cles_CRUI_1er_semestre_2024_Francais.json` | `chiffres_cles_crui_1er_semestre_2024_francais` | `crui_key_figures_2024_h1` | `fr` | `key_figures` | 7 |
| `ENG_Indicateurs_climat_investissement.json` | `eng_indicateurs_climat_dinvestissement` | `investment_climate_indicators` | `en` | `business_climate` | 14 |
| `ENG_Panorama_des_ZI.json` | `eng_panorama_des_zi` | `industrial_zones_panorama` | `en` | `industrial_zones` | 47 |
| `ENG_Presentation_CRI_TTA.json` | `eng_presentation_cri_tta_vf` | `cri_presentation` | `en` | `institutional_presentation` | 20 |
| `ESP_Chiffres_cles_annee_2025.json` | `esp_chiffres_cles_annee_2025` | `chiffres_cles_2025` | `es` | `key_figures` | 18 |
| `ESP_Indicateurs_climat_investissement.json` | `esp_indicateurs_climat_dinvestissement` | `investment_climate_indicators` | `es` | `business_climate` | 14 |
| `ESP_Presentation_CRI_TTA.json` | `esp_presentation_cri_tta_vf` | `cri_presentation` | `es` | `institutional_presentation` | 14 |
| `ES_Panorama_des_ZI.json` | `es_panorama_des_zi` | `industrial_zones_panorama` | `es` | `industrial_zones` | 47 |
| `Eng_Chiffres_cles_annee_2025.json` | `eng_chiffres_cles_annee_2025` | `chiffres_cles_2025` | `en` | `key_figures` | 18 |
| `FR_Chiffres_cles_CRITTA_30_Sept_2024.json` | `fr_chiffres_cles_critta_30_sept_2024` | `crui_key_figures_2024_09_30` | `fr` | `key_figures` | 14 |
| `FR_Chiffres_cles_annee_2025.json` | `fr_chiffres_cles_annee_2025` | `chiffres_cles_2025` | `fr` | `annual_key_figures` | 18 |
| `FR_Panorama_Zones_economiques_industrielles.json` | `panorama_zones_economiques_industrielles_fr` | `industrial_zones_panorama` | `fr` | `industrial_zones` | 47 |
| `FR_Presentation_CRI_TTA.json` | `fr_presentation_cri_tta_vf` | `cri_presentation` | `fr` | `institutional_presentation` | 15 |
| `Fr_Indicateurs_climat_investissement.json` | `fr_indicateurs_climat_dinvestissement` | `investment_climate_indicators` | `fr` | `business_climate` | 14 |
| `Guide_branchement_electricite_eau_assainissement.json` | `guide_branchement_electricite_eau_assainissement_grands_comptes` | `electricity_water_sanitation_connection` | `fr` | `utility_connection_guide` | 7 |
| `Guide_de_Conciliation_AR.json` | `guide_de_conciliation_ar` | `conciliation_guide` | `ar` | `conciliation_guide` | 7 |
| `Guide_de_Conciliation_ES.json` | `guide_de_conciliation_es` | `conciliation_guide` | `es` | `conciliation_guide` | 7 |
| `Guide_du_financement_des_entreprises.json` | `guide_du_financement_des_entreprises` | `financing_guide` | `fr` | `financing_guide` | 113 |
| `Guide_programme_integre_appui_financement_entreprises_AR.json` | `guide_programme_integre_appui_financement_entreprises_ar` | `integrated_business_support_financing` | `ar` | `integrated_financing_programme` | 3 |
| `Investment_Business_Support_Single_Window_ES.json` | `investment_business_support_single_window_es` | `investment_business_support_single_window` | `es` | `single_window_services` | 7 |
| `Investment_Business_Support_Single_Window_FR.json` | `investment_business_support_single_window_fr` | `investment_business_support_single_window` | `fr` | `single_window_services` | 7 |
| `Investors_Guide_territorial_opportunities_EN.json` | `investors_guide_territorial_opportunities_en` | `investors_guide_territorial_opportunities` | `en` | `investment_opportunities` | 70 |
| `Investors_Guide_territorial_opportunities_FR.json` | `investors_guide_territorial_opportunities_fr` | `investors_guide_territorial_opportunities` | `fr` | `investment_opportunities` | 95 |
| `Manar_Al_Moustatmir_ENG_PNG.json` | `manar_al_moustatmir_eng_png` | `manar_al_moustatmir_news_2023` | `en` | `news_review` | 16 |
| `Manar_Al_Moustatmir_News.json` | `manar_al_moustatmir_news` | `manar_al_moustatmir_news_2023` | `fr` | `news_review` | 16 |
| `Nv_Guide_Cout_facteurs_CRI_2024.json` | `nv_guide_cout_facteurs_cri_2024` | `production_factor_cost_guide_2024` | `fr` | `cost_guide` | 32 |

## Document-family consistency audit

### `chiffres_cles_2025`

- Languages: ar, en, es, fr
- Documents: Arabe_Chiffres_cles_2025.json, Eng_Chiffres_cles_annee_2025.json, ESP_Chiffres_cles_annee_2025.json, FR_Chiffres_cles_annee_2025.json
- Topic IDs: business_creation, business_support, closing_message, crui_activity, promotion_partnerships, regional_investment_overview, regional_statistics, sector_investment
- Chunk counts: ar=18, en=18, es=18, fr=18
- Alignment note: chunk counts are not required to match; this audit compares family/topic identifiers and flags no automatic structural failure.

### `conciliation_guide`

- Languages: ar, es
- Documents: Guide_de_Conciliation_AR.json, Guide_de_Conciliation_ES.json
- Topic IDs: conciliation
- Chunk counts: ar=7, es=7
- Alignment note: chunk counts are not required to match; this audit compares family/topic identifiers and flags no automatic structural failure.

### `cri_presentation`

- Languages: ar, en, es, fr
- Documents: AR_Presentation_CRI_TTA.json, ENG_Presentation_CRI_TTA.json, ESP_Presentation_CRI_TTA.json, FR_Presentation_CRI_TTA.json
- Topic IDs: investment_agency
- Chunk counts: ar=20, en=20, es=14, fr=15
- Alignment note: chunk counts are not required to match; this audit compares family/topic identifiers and flags no automatic structural failure.

### `crui_key_figures_2024_09_30`

- Languages: fr
- Documents: FR_Chiffres_cles_CRITTA_30_Sept_2024.json
- Topic IDs: regional_statistics
- Chunk counts: fr=14
- Alignment note: chunk counts are not required to match; this audit compares family/topic identifiers and flags no automatic structural failure.

### `crui_key_figures_2024_h1`

- Languages: ar, en, es, fr
- Documents: Chiffres_cles_CRUI_1er_semestre_2024_Anglais.json, Chiffres_cles_CRUI_1er_semestre_2024_Arabe.json, Chiffres_cles_CRUI_1er_semestre_2024_Espagnol.json, Chiffres_cles_CRUI_1er_semestre_2024_Francais.json
- Topic IDs: regional_statistics
- Chunk counts: en=7, ar=7, es=7, fr=7
- Alignment note: chunk counts are not required to match; this audit compares family/topic identifiers and flags no automatic structural failure.

### `electricity_water_sanitation_connection`

- Languages: fr
- Documents: Guide_branchement_electricite_eau_assainissement.json
- Topic IDs: utility_connections
- Chunk counts: fr=7
- Alignment note: chunk counts are not required to match; this audit compares family/topic identifiers and flags no automatic structural failure.

### `financing_guide`

- Languages: fr
- Documents: Guide_du_financement_des_entreprises.json
- Topic IDs: bank_credit, bank_financing, business_plan, capital_markets, contact_information, credit_guarantees, equity_financing, equity_investment, financial_glossary, financing_matrix, guide_closing, guide_navigation, guide_overview, international_financing, leasing, microcredit, participative_finance, public_financing
- Chunk counts: fr=113
- Alignment note: chunk counts are not required to match; this audit compares family/topic identifiers and flags no automatic structural failure.

### `industrial_zones_panorama`

- Languages: en, es, fr
- Documents: ENG_Panorama_des_ZI.json, ES_Panorama_des_ZI.json, FR_Panorama_Zones_economiques_industrielles.json
- Topic IDs: industrial_zones
- Chunk counts: en=47, es=47, fr=47
- Alignment note: chunk counts are not required to match; this audit compares family/topic identifiers and flags no automatic structural failure.

### `integrated_business_support_financing`

- Languages: ar
- Documents: Guide_programme_integre_appui_financement_entreprises_AR.json
- Topic IDs: integrated_financing
- Chunk counts: ar=3
- Alignment note: chunk counts are not required to match; this audit compares family/topic identifiers and flags no automatic structural failure.

### `investment_business_support_single_window`

- Languages: es, fr
- Documents: Investment_Business_Support_Single_Window_ES.json, Investment_Business_Support_Single_Window_FR.json
- Topic IDs: business_support
- Chunk counts: es=7, fr=7
- Alignment note: chunk counts are not required to match; this audit compares family/topic identifiers and flags no automatic structural failure.

### `investment_climate_indicators`

- Languages: en, es, fr
- Documents: ENG_Indicateurs_climat_investissement.json, ESP_Indicateurs_climat_investissement.json, Fr_Indicateurs_climat_investissement.json
- Topic IDs: business_climate
- Chunk counts: en=14, es=14, fr=14
- Alignment note: chunk counts are not required to match; this audit compares family/topic identifiers and flags no automatic structural failure.

### `investors_guide_territorial_opportunities`

- Languages: en, fr
- Documents: Investors_Guide_territorial_opportunities_EN.json, Investors_Guide_territorial_opportunities_FR.json
- Topic IDs: investment_opportunities
- Chunk counts: en=70, fr=95
- Alignment note: chunk counts are not required to match; this audit compares family/topic identifiers and flags no automatic structural failure.

### `logistics_sector_brochure`

- Languages: fr
- Documents: Brochure_secteur_Logistique.json
- Topic IDs: logistics_sector
- Chunk counts: fr=6
- Alignment note: chunk counts are not required to match; this audit compares family/topic identifiers and flags no automatic structural failure.

### `manar_al_moustatmir_news_2023`

- Languages: ar, en, fr
- Documents: Akhbar_Al_Moustatmir_News.json, Manar_Al_Moustatmir_ENG_PNG.json, Manar_Al_Moustatmir_News.json
- Topic IDs: investment_news
- Chunk counts: ar=15, en=16, fr=16
- Alignment note: chunk counts are not required to match; this audit compares family/topic identifiers and flags no automatic structural failure.

### `production_factor_cost_guide_2024`

- Languages: fr
- Documents: Nv_Guide_Cout_facteurs_CRI_2024.json
- Topic IDs: production_costs
- Chunk counts: fr=32
- Alignment note: chunk counts are not required to match; this audit compares family/topic identifiers and flags no automatic structural failure.

## Content and tag distributions

Content types:
- `contact_information`: 5
- `cost_information`: 32
- `financial_product`: 73
- `industrial_zone`: 141
- `investment_opportunity`: 167
- `legal_information`: 2
- `narrative`: 148
- `procedure`: 23
- `service`: 22
- `statistics`: 146
- `table`: 8
Semantic tags:
- `investment_opportunities`: 166
- `industrial_zones`: 142
- `regional_statistics`: 96
- `investment_agency`: 69
- `investment_news`: 47
- `business_climate`: 42
- `production_costs`: 32
- `bank_credit`: 31
- `public_financing`: 28
- `business_support`: 18
- `conciliation`: 15
- `guarantees`: 10
- `working_capital`: 8
- `business_plan`: 8
- `utility_connections`: 7
- `eligibility_conditions`: 7
- `import_financing`: 7
- `logistics_sector`: 6
- `financing_products`: 6
- `investment_financing`: 6
- `export_financing`: 6
- `sme_support`: 6
- `equity_investment`: 6
- `capital_markets`: 6
- `piafe`: 5
- `contact_information`: 5
- `equity_financing`: 5
- `microcredit`: 5
- `public_markets`: 5
- `startup_financing`: 5

## Chunk-size diagnostics

- Minimum characters: 20
- Median characters: 1630
- Average characters: 2565.64
- Maximum characters: 12547
- Chunks > 3,000 characters: 217
- Chunks > 5,000 characters: 132
- Chunks > 8,000 characters: 41
- Chunks > 12,000 characters: 2

Largest chunks over 12,000 characters:
- `investors_guide_territorial_opportunities_en` / `investors_guide_territorial_opportunities_en_chunk_015`: 12547 characters; Territorial investment opportunities / Cannabis processing unit for the automotive industry; pages 43-45
- `investors_guide_territorial_opportunities_en` / `investors_guide_territorial_opportunities_en_chunk_047`: 12163 characters; Territorial investment opportunities / Province of Al Hoceima (Al Hoceima); pages 139-141

## Provenance and coverage

### `AR_Presentation_CRI_TTA.json`

- Useful pages not represented: none
- Empty source pages ignored: none (no factual text to preserve)
- Pages represented once: 60
- Pages represented multiple times: none

### `Akhbar_Al_Moustatmir_News.json`

- Useful pages not represented: none
- Empty source pages ignored: none (no factual text to preserve)
- Pages represented once: 44
- Pages represented multiple times: none

### `Arabe_Chiffres_cles_2025.json`

- Useful pages not represented: none
- Empty source pages ignored: none (no factual text to preserve)
- Pages represented once: 18
- Pages represented multiple times: none

### `Brochure_secteur_Logistique.json`

- Useful pages not represented: none
- Empty source pages ignored: none (no factual text to preserve)
- Pages represented once: 12
- Pages represented multiple times: none

### `Chiffres_cles_CRUI_1er_semestre_2024_Anglais.json`

- Useful pages not represented: none
- Empty source pages ignored: none (no factual text to preserve)
- Pages represented once: 7
- Pages represented multiple times: none

### `Chiffres_cles_CRUI_1er_semestre_2024_Arabe.json`

- Useful pages not represented: none
- Empty source pages ignored: none (no factual text to preserve)
- Pages represented once: 7
- Pages represented multiple times: none

### `Chiffres_cles_CRUI_1er_semestre_2024_Espagnol.json`

- Useful pages not represented: none
- Empty source pages ignored: none (no factual text to preserve)
- Pages represented once: 7
- Pages represented multiple times: none

### `Chiffres_cles_CRUI_1er_semestre_2024_Francais.json`

- Useful pages not represented: none
- Empty source pages ignored: none (no factual text to preserve)
- Pages represented once: 7
- Pages represented multiple times: none

### `ENG_Indicateurs_climat_investissement.json`

- Useful pages not represented: none
- Empty source pages ignored: none (no factual text to preserve)
- Pages represented once: 28
- Pages represented multiple times: none

### `ENG_Panorama_des_ZI.json`

- Useful pages not represented: none
- Empty source pages ignored: [93] (no factual text to preserve)
- Pages represented once: 93
- Pages represented multiple times: none

### `ENG_Presentation_CRI_TTA.json`

- Useful pages not represented: none
- Empty source pages ignored: [31, 46] (no factual text to preserve)
- Pages represented once: 59
- Pages represented multiple times: none

### `ESP_Chiffres_cles_annee_2025.json`

- Useful pages not represented: none
- Empty source pages ignored: none (no factual text to preserve)
- Pages represented once: 18
- Pages represented multiple times: none

### `ESP_Indicateurs_climat_investissement.json`

- Useful pages not represented: none
- Empty source pages ignored: none (no factual text to preserve)
- Pages represented once: 28
- Pages represented multiple times: none

### `ESP_Presentation_CRI_TTA.json`

- Useful pages not represented: none
- Empty source pages ignored: [25] (no factual text to preserve)
- Pages represented once: 41
- Pages represented multiple times: none

### `ES_Panorama_des_ZI.json`

- Useful pages not represented: none
- Empty source pages ignored: [93] (no factual text to preserve)
- Pages represented once: 93
- Pages represented multiple times: none

### `Eng_Chiffres_cles_annee_2025.json`

- Useful pages not represented: none
- Empty source pages ignored: none (no factual text to preserve)
- Pages represented once: 18
- Pages represented multiple times: none

### `FR_Chiffres_cles_CRITTA_30_Sept_2024.json`

- Useful pages not represented: none
- Empty source pages ignored: none (no factual text to preserve)
- Pages represented once: 14
- Pages represented multiple times: none

### `FR_Chiffres_cles_annee_2025.json`

- Useful pages not represented: none
- Empty source pages ignored: none (no factual text to preserve)
- Pages represented once: 18
- Pages represented multiple times: none

### `FR_Panorama_Zones_economiques_industrielles.json`

- Useful pages not represented: none
- Empty source pages ignored: [93] (no factual text to preserve)
- Pages represented once: 93
- Pages represented multiple times: none

### `FR_Presentation_CRI_TTA.json`

- Useful pages not represented: none
- Empty source pages ignored: none (no factual text to preserve)
- Pages represented once: 44
- Pages represented multiple times: none

### `Fr_Indicateurs_climat_investissement.json`

- Useful pages not represented: none
- Empty source pages ignored: none (no factual text to preserve)
- Pages represented once: 28
- Pages represented multiple times: none

### `Guide_branchement_electricite_eau_assainissement.json`

- Useful pages not represented: none
- Empty source pages ignored: none (no factual text to preserve)
- Pages represented once: 13
- Pages represented multiple times: none

### `Guide_de_Conciliation_AR.json`

- Useful pages not represented: none
- Empty source pages ignored: none (no factual text to preserve)
- Pages represented once: 7
- Pages represented multiple times: none

### `Guide_de_Conciliation_ES.json`

- Useful pages not represented: none
- Empty source pages ignored: none (no factual text to preserve)
- Pages represented once: 7
- Pages represented multiple times: none

### `Guide_du_financement_des_entreprises.json`

- Useful pages not represented: none
- Empty source pages ignored: [16, 22, 40, 46, 54, 58, 70, 76, 80, 82, 94, 102, 116, 120, 124, 130, 136, 176] (no factual text to preserve)
- Pages represented once: 164
- Pages represented multiple times: {29: 2, 37: 2}

### `Guide_programme_integre_appui_financement_entreprises_AR.json`

- Useful pages not represented: none
- Empty source pages ignored: none (no factual text to preserve)
- Pages represented once: 6
- Pages represented multiple times: none

### `Investment_Business_Support_Single_Window_ES.json`

- Useful pages not represented: none
- Empty source pages ignored: [2] (no factual text to preserve)
- Pages represented once: 12
- Pages represented multiple times: none

### `Investment_Business_Support_Single_Window_FR.json`

- Useful pages not represented: none
- Empty source pages ignored: [2] (no factual text to preserve)
- Pages represented once: 12
- Pages represented multiple times: none

### `Investors_Guide_territorial_opportunities_EN.json`

- Useful pages not represented: none
- Empty source pages ignored: [3] (no factual text to preserve)
- Pages represented once: 208
- Pages represented multiple times: none

### `Investors_Guide_territorial_opportunities_FR.json`

- Useful pages not represented: none
- Empty source pages ignored: [3] (no factual text to preserve)
- Pages represented once: 284
- Pages represented multiple times: none

### `Manar_Al_Moustatmir_ENG_PNG.json`

- Useful pages not represented: none
- Empty source pages ignored: none (no factual text to preserve)
- Pages represented once: 47
- Pages represented multiple times: none

### `Manar_Al_Moustatmir_News.json`

- Useful pages not represented: none
- Empty source pages ignored: none (no factual text to preserve)
- Pages represented once: 47
- Pages represented multiple times: none

### `Nv_Guide_Cout_facteurs_CRI_2024.json`

- Useful pages not represented: none
- Empty source pages ignored: [2] (no factual text to preserve)
- Pages represented once: 62
- Pages represented multiple times: none

## Temporal metadata

- Chunks with an explicit primary year: 135
- Chunks with one or more explicit years mentioned: 294
- The migration does not infer a primary year from the document filename when the chunk text is ambiguous.

## OCR and manual-review warnings

- OCR artifacts, broken words, duplicated URLs, layout markers, and mixed-language extraction remain preserved where present.
- Empty source pages were not included in source spans; they are reported through the per-document coverage diagnostics.
- New documents use semantically grouped consecutive page units. Industrial-zone and opportunity guides use smaller groups, but pages with several independently extractable units may require a later manual refinement pass.
- No new content type was introduced.

## Documents requiring manual semantic review

The converted documents below are structurally valid and provenance-safe, but should receive human semantic-boundary review before production ingestion. The automated pass grouped exact consecutive source pages and did not invent or rewrite facts:
- `AR_Presentation_CRI_TTA.json`
- `Akhbar_Al_Moustatmir_News.json`
- `Arabe_Chiffres_cles_2025.json`
- `Brochure_secteur_Logistique.json`
- `Chiffres_cles_CRUI_1er_semestre_2024_Anglais.json`
- `Chiffres_cles_CRUI_1er_semestre_2024_Arabe.json`
- `Chiffres_cles_CRUI_1er_semestre_2024_Espagnol.json`
- `Chiffres_cles_CRUI_1er_semestre_2024_Francais.json`
- `ENG_Indicateurs_climat_investissement.json`
- `ENG_Panorama_des_ZI.json`
- `ENG_Presentation_CRI_TTA.json`
- `ESP_Chiffres_cles_annee_2025.json`
- `ESP_Indicateurs_climat_investissement.json`
- `ESP_Presentation_CRI_TTA.json`
- `ES_Panorama_des_ZI.json`
- `Eng_Chiffres_cles_annee_2025.json`
- `FR_Chiffres_cles_CRITTA_30_Sept_2024.json`
- `FR_Panorama_Zones_economiques_industrielles.json`
- `FR_Presentation_CRI_TTA.json`
- `Fr_Indicateurs_climat_investissement.json`
- `Guide_branchement_electricite_eau_assainissement.json`
- `Guide_de_Conciliation_AR.json`
- `Guide_de_Conciliation_ES.json`
- `Guide_programme_integre_appui_financement_entreprises_AR.json`
- `Investment_Business_Support_Single_Window_ES.json`
- `Investment_Business_Support_Single_Window_FR.json`
- `Investors_Guide_territorial_opportunities_EN.json`
- `Investors_Guide_territorial_opportunities_FR.json`
- `Manar_Al_Moustatmir_ENG_PNG.json`
- `Manar_Al_Moustatmir_News.json`
- `Nv_Guide_Cout_facteurs_CRI_2024.json`

## Validation

- Documents passing in-script exact-span validation: 33/33
- Documents failing validation: 0
- `AR_Presentation_CRI_TTA.json`: PASS
- `Akhbar_Al_Moustatmir_News.json`: PASS
- `Arabe_Chiffres_cles_2025.json`: PASS
- `Brochure_secteur_Logistique.json`: PASS
- `Chiffres_cles_CRUI_1er_semestre_2024_Anglais.json`: PASS
- `Chiffres_cles_CRUI_1er_semestre_2024_Arabe.json`: PASS
- `Chiffres_cles_CRUI_1er_semestre_2024_Espagnol.json`: PASS
- `Chiffres_cles_CRUI_1er_semestre_2024_Francais.json`: PASS
- `ENG_Indicateurs_climat_investissement.json`: PASS
- `ENG_Panorama_des_ZI.json`: PASS
- `ENG_Presentation_CRI_TTA.json`: PASS
- `ESP_Chiffres_cles_annee_2025.json`: PASS
- `ESP_Indicateurs_climat_investissement.json`: PASS
- `ESP_Presentation_CRI_TTA.json`: PASS
- `ES_Panorama_des_ZI.json`: PASS
- `Eng_Chiffres_cles_annee_2025.json`: PASS
- `FR_Chiffres_cles_CRITTA_30_Sept_2024.json`: PASS
- `FR_Chiffres_cles_annee_2025.json`: PASS
- `FR_Panorama_Zones_economiques_industrielles.json`: PASS
- `FR_Presentation_CRI_TTA.json`: PASS
- `Fr_Indicateurs_climat_investissement.json`: PASS
- `Guide_branchement_electricite_eau_assainissement.json`: PASS
- `Guide_de_Conciliation_AR.json`: PASS
- `Guide_de_Conciliation_ES.json`: PASS
- `Guide_du_financement_des_entreprises.json`: PASS
- `Guide_programme_integre_appui_financement_entreprises_AR.json`: PASS
- `Investment_Business_Support_Single_Window_ES.json`: PASS
- `Investment_Business_Support_Single_Window_FR.json`: PASS
- `Investors_Guide_territorial_opportunities_EN.json`: PASS
- `Investors_Guide_territorial_opportunities_FR.json`: PASS
- `Manar_Al_Moustatmir_ENG_PNG.json`: PASS
- `Manar_Al_Moustatmir_News.json`: PASS
- `Nv_Guide_Cout_facteurs_CRI_2024.json`: PASS

## Raw SHA-256 integrity

All raw files were hashed before and after migration. No raw source file was written.

| File | Before | After | Status |
|---|---|---|---|
| `AR_Presentation_CRI_TTA.json` | `5A30BE03DF6490A2C0D2A506122782092F6E901B3FDAC53116C6F34A3ED041DF` | `5A30BE03DF6490A2C0D2A506122782092F6E901B3FDAC53116C6F34A3ED041DF` | **unchanged** |
| `Akhbar_Al_Moustatmir_News.json` | `374043D95A534BF79C5BC8286E2AA08FECE2697BEFC39C03327D8FCA65D4F641` | `374043D95A534BF79C5BC8286E2AA08FECE2697BEFC39C03327D8FCA65D4F641` | **unchanged** |
| `Arabe_Chiffres_cles_2025.json` | `55C60DD7EAE0453E933C2C59CABAD1E7425050844C682293BEEFE2B1F22487B2` | `55C60DD7EAE0453E933C2C59CABAD1E7425050844C682293BEEFE2B1F22487B2` | **unchanged** |
| `Brochure_secteur_Logistique.json` | `BBDCF8A721976A6A9980BC9BC6D836C2A8778ECCBCA2241BC75CE00E4BB13830` | `BBDCF8A721976A6A9980BC9BC6D836C2A8778ECCBCA2241BC75CE00E4BB13830` | **unchanged** |
| `Chiffres_cles_CRUI_1er_semestre_2024_Anglais.json` | `E3E16EC4DDDB088AF425A1CC53C2D374B7C352DC179A64E1891177E1213F4CF0` | `E3E16EC4DDDB088AF425A1CC53C2D374B7C352DC179A64E1891177E1213F4CF0` | **unchanged** |
| `Chiffres_cles_CRUI_1er_semestre_2024_Arabe.json` | `C248893E7C681167759ABD96710E98B6F2C42A97F07FE21FC1176A704B39E205` | `C248893E7C681167759ABD96710E98B6F2C42A97F07FE21FC1176A704B39E205` | **unchanged** |
| `Chiffres_cles_CRUI_1er_semestre_2024_Espagnol.json` | `0949D4EB1297677FC5DBDE68DA0B4E3B8BDC44C02531DBE0CDAF5C3F75C2B97F` | `0949D4EB1297677FC5DBDE68DA0B4E3B8BDC44C02531DBE0CDAF5C3F75C2B97F` | **unchanged** |
| `Chiffres_cles_CRUI_1er_semestre_2024_Francais.json` | `CC3954B0DEF435F1EED9285B5ED3D0551B808C9AABAEF24F89B2420ACC2926D7` | `CC3954B0DEF435F1EED9285B5ED3D0551B808C9AABAEF24F89B2420ACC2926D7` | **unchanged** |
| `ENG_Indicateurs_climat_investissement.json` | `6105F9A65D6812B3776E23B78BE4639674E0A4A6BB1C447D9BBB42DEBDF3BD9F` | `6105F9A65D6812B3776E23B78BE4639674E0A4A6BB1C447D9BBB42DEBDF3BD9F` | **unchanged** |
| `ENG_Panorama_des_ZI.json` | `13CDB1DC6DC139BE04B59A2119F7AC522FF18A085E82D52B5CA15DDFD4E1C5C0` | `13CDB1DC6DC139BE04B59A2119F7AC522FF18A085E82D52B5CA15DDFD4E1C5C0` | **unchanged** |
| `ENG_Presentation_CRI_TTA.json` | `4EF4A90F82639330E5AA8F2B2ECA25595DBBDE78D543EC1EC42EB7D37DFFED86` | `4EF4A90F82639330E5AA8F2B2ECA25595DBBDE78D543EC1EC42EB7D37DFFED86` | **unchanged** |
| `ESP_Chiffres_cles_annee_2025.json` | `020E8CB83A49193D1EFE7D2FB8CEFC2A79A2FB6373D7E68C52058E0F143BCBA9` | `020E8CB83A49193D1EFE7D2FB8CEFC2A79A2FB6373D7E68C52058E0F143BCBA9` | **unchanged** |
| `ESP_Indicateurs_climat_investissement.json` | `FCD3636D53ED268F129F05E80416E3D923F8D6F6EF38A3859F6DC0DC5A3E6A7A` | `FCD3636D53ED268F129F05E80416E3D923F8D6F6EF38A3859F6DC0DC5A3E6A7A` | **unchanged** |
| `ESP_Presentation_CRI_TTA.json` | `A1A475913A920BD7C8A0F97B56B01AB08B5560C289A88C47EB8D28E6E381F012` | `A1A475913A920BD7C8A0F97B56B01AB08B5560C289A88C47EB8D28E6E381F012` | **unchanged** |
| `ES_Panorama_des_ZI.json` | `482AC9C42D5050A8D27002C05533562790246036A0C32E4000EBF51B0788B05B` | `482AC9C42D5050A8D27002C05533562790246036A0C32E4000EBF51B0788B05B` | **unchanged** |
| `Eng_Chiffres_cles_annee_2025.json` | `BE8863389CE4980E9ADC8BF53B892416FFB863809D0E5EE41FC1CE4D9F20BD93` | `BE8863389CE4980E9ADC8BF53B892416FFB863809D0E5EE41FC1CE4D9F20BD93` | **unchanged** |
| `FR_Chiffres_cles_CRITTA_30_Sept_2024.json` | `A1C89BB550EBEF09592C362F9C04AC68608B9E9B272BF2645D8006640A2F70F0` | `A1C89BB550EBEF09592C362F9C04AC68608B9E9B272BF2645D8006640A2F70F0` | **unchanged** |
| `FR_Chiffres_cles_annee_2025.json` | `96DE89AA6BAE24D094142AFE8EE69B550216D78686CA1CD5B4899F434FF9294E` | `96DE89AA6BAE24D094142AFE8EE69B550216D78686CA1CD5B4899F434FF9294E` | **unchanged** |
| `FR_Panorama_Zones_economiques_industrielles.json` | `5389B0F0CD19E4E148CC2F9D0C3FC813E105063702EA083E447C1AB04F4107A7` | `5389B0F0CD19E4E148CC2F9D0C3FC813E105063702EA083E447C1AB04F4107A7` | **unchanged** |
| `FR_Presentation_CRI_TTA.json` | `E0AB74375857182184A517816EA3B8A8B5C2F80A218BE33610E071C4A7686ED9` | `E0AB74375857182184A517816EA3B8A8B5C2F80A218BE33610E071C4A7686ED9` | **unchanged** |
| `Fr_Indicateurs_climat_investissement.json` | `294E2716329800101FB4160415D09531F5AB0056B06220424F050BEDA939EC53` | `294E2716329800101FB4160415D09531F5AB0056B06220424F050BEDA939EC53` | **unchanged** |
| `Guide_branchement_electricite_eau_assainissement.json` | `F819E95CC3714532976B30DAB1EF8B4E76A201F03CEC6FDBE78CD859F9072354` | `F819E95CC3714532976B30DAB1EF8B4E76A201F03CEC6FDBE78CD859F9072354` | **unchanged** |
| `Guide_de_Conciliation_AR.json` | `6A5E32CFB2B134DA01DF3A70518D4F86C0534D6B36981DC6FE247773012D8BB4` | `6A5E32CFB2B134DA01DF3A70518D4F86C0534D6B36981DC6FE247773012D8BB4` | **unchanged** |
| `Guide_de_Conciliation_ES.json` | `824DD5BC30536BC5128BBD0BB82689B555D5B3DCFC47AE58A5F700CA96428DB2` | `824DD5BC30536BC5128BBD0BB82689B555D5B3DCFC47AE58A5F700CA96428DB2` | **unchanged** |
| `Guide_du_financement_des_entreprises.json` | `EDB91587D403985E4628A31C33819F5BA5FD0FB539F88034E9330CEB2BC01888` | `EDB91587D403985E4628A31C33819F5BA5FD0FB539F88034E9330CEB2BC01888` | **unchanged** |
| `Guide_programme_integre_appui_financement_entreprises_AR.json` | `285EE42FBEE64F602558610A619273FE83B1F9F20C1B51EB782C7963361FFA6E` | `285EE42FBEE64F602558610A619273FE83B1F9F20C1B51EB782C7963361FFA6E` | **unchanged** |
| `Investment_Business_Support_Single_Window_ES.json` | `9BEFBB8644EB2F8E8BB1E3B7B7A7BB72BDEC1C39367054198F64DA3CCA4C7931` | `9BEFBB8644EB2F8E8BB1E3B7B7A7BB72BDEC1C39367054198F64DA3CCA4C7931` | **unchanged** |
| `Investment_Business_Support_Single_Window_FR.json` | `22157D3D489F8964FFA0AF2209CE8B7C690020A638C48F88CE8E585DA7A26526` | `22157D3D489F8964FFA0AF2209CE8B7C690020A638C48F88CE8E585DA7A26526` | **unchanged** |
| `Investors_Guide_territorial_opportunities_EN.json` | `0962FD8F0B18071629C8AF7C672BA970160FDCBC0B3409279D2EC87738245D6E` | `0962FD8F0B18071629C8AF7C672BA970160FDCBC0B3409279D2EC87738245D6E` | **unchanged** |
| `Investors_Guide_territorial_opportunities_FR.json` | `518A5307E090C60F99E3A56F8129E8B9205B99B2A0A457CDE9FBA8295F02B462` | `518A5307E090C60F99E3A56F8129E8B9205B99B2A0A457CDE9FBA8295F02B462` | **unchanged** |
| `Manar_Al_Moustatmir_ENG_PNG.json` | `302A39A4AB553092100106FBCC8F0F1D4B31B5820A3FB1C35E297B8A7CC07BC5` | `302A39A4AB553092100106FBCC8F0F1D4B31B5820A3FB1C35E297B8A7CC07BC5` | **unchanged** |
| `Manar_Al_Moustatmir_News.json` | `EEDB674ECF83F998F82C32C0141C1B45995AC608AB3D841476438A4C47FED0A9` | `EEDB674ECF83F998F82C32C0141C1B45995AC608AB3D841476438A4C47FED0A9` | **unchanged** |
| `Nv_Guide_Cout_facteurs_CRI_2024.json` | `7A00656783CC67C48920269CE3D7EE263B20DC73AA122366BA69BA82B48665D1` | `7A00656783CC67C48920269CE3D7EE263B20DC73AA122366BA69BA82B48665D1` | **unchanged** |

## Output boundary

- The two reviewed semantic documents were preserved and validated; they were not regenerated by this full-corpus run.
- No RAG, embedding, Qdrant, retrieval, prompt, API, frontend, or production files were modified.
- No files were skipped due to unsafe conversion.
