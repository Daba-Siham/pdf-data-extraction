# Semantic quality refinement report — phase 3a

## Scope

Only the `chiffres_cles_2025` and `crui_key_figures_2024_h1` families were modified. Schema version remains `2.2`. Raw JSON files and all other semantic families were not modified.

## Documents modified

- `Arabe_Chiffres_cles_2025.json` — `arabe_chiffres_cles_2025` — family `chiffres_cles_2025` — 18 chunks
- `Chiffres_cles_CRUI_1er_semestre_2024_Anglais.json` — `chiffres_cles_crui_1er_semestre_2024_anglais` — family `crui_key_figures_2024_h1` — 7 chunks
- `Chiffres_cles_CRUI_1er_semestre_2024_Arabe.json` — `chiffres_cles_crui_1er_semestre_2024_arabe` — family `crui_key_figures_2024_h1` — 7 chunks
- `Chiffres_cles_CRUI_1er_semestre_2024_Espagnol.json` — `chiffres_cles_crui_1er_semestre_2024_espagnol` — family `crui_key_figures_2024_h1` — 7 chunks
- `Chiffres_cles_CRUI_1er_semestre_2024_Francais.json` — `chiffres_cles_crui_1er_semestre_2024_francais` — family `crui_key_figures_2024_h1` — 7 chunks
- `ESP_Chiffres_cles_annee_2025.json` — `esp_chiffres_cles_annee_2025` — family `chiffres_cles_2025` — 18 chunks
- `Eng_Chiffres_cles_annee_2025.json` — `eng_chiffres_cles_annee_2025` — family `chiffres_cles_2025` — 18 chunks
- `FR_Chiffres_cles_annee_2025.json` — `fr_chiffres_cles_annee_2025` — family `chiffres_cles_2025` — 18 chunks

## Canonical concepts aligned

2025 key figures: `regional_investment_overview`, `business_creation`, `crui_activity`, `sector_investment`, `industrial_investment`, `tourism_investment`, `energy_investment`, `business_support`, `piafe`, `conciliation`, `open_innovation`, `territorial_promotion`, `mre_support`, `tpme_support`, `strategic_partnership`, `closing_message`.

CRUI H1 2024: `crui_activity`, `projects_reviewed`, `sector_distribution`, `industrial_investment`, `investment_amount`, `approved_projects`, `projected_jobs`, `closing_message`.

## Topic ID and semantic-tag changes

The translated 2025 documents were changed from one generic `regional_statistics` section to one source-language section per aligned semantic unit. The CRUI translations were changed from one generic `regional_statistics` section to aligned page-level semantic units. Human-readable titles and original chunk text remain in each source language.

The French 2025 document retained its reviewed semantic section structure; its chunk tags were normalized to the same canonical vocabulary.

## Temporal and metadata corrections

- All four CRUI documents now have document-level `reference_period.type = semester`, `year = 2024`, and `semester = 1`.
- All CRUI chunks now carry the same H1 2024 semester scope while preserving explicit years mentioned in their source text.
- CRUI `publication_year` is `null`; the source supports a reference period, not an independently stated publication year.
- All 2025 documents retain `publication_year = 2025` and a year-2025 reference period because the edition is explicitly identified as 2025.

## Differences not safely aligned

- Source layouts and wording differ across languages, so chunk counts and display headings were not copied across documents.
- Historical years appearing inside CRUI pages remain in `years_mentioned`; they were not replaced with 2024.
- The French reviewed document contains richer existing section-level distinctions than the translated automated outputs; alignment uses canonical IDs and tags without copying French text.

## Validation

- `Arabe_Chiffres_cles_2025.json`: PASS
- `Chiffres_cles_CRUI_1er_semestre_2024_Anglais.json`: PASS
- `Chiffres_cles_CRUI_1er_semestre_2024_Arabe.json`: PASS
- `Chiffres_cles_CRUI_1er_semestre_2024_Espagnol.json`: PASS
- `Chiffres_cles_CRUI_1er_semestre_2024_Francais.json`: PASS
- `ESP_Chiffres_cles_annee_2025.json`: PASS
- `Eng_Chiffres_cles_annee_2025.json`: PASS
- `FR_Chiffres_cles_annee_2025.json`: PASS

## Raw-file integrity

| Raw file | Before SHA-256 | After SHA-256 | Status |
|---|---|---|---|
| `Arabe_Chiffres_cles_2025.json` | `55C60DD7EAE0453E933C2C59CABAD1E7425050844C682293BEEFE2B1F22487B2` | `55C60DD7EAE0453E933C2C59CABAD1E7425050844C682293BEEFE2B1F22487B2` | **unchanged** |
| `Chiffres_cles_CRUI_1er_semestre_2024_Anglais.json` | `E3E16EC4DDDB088AF425A1CC53C2D374B7C352DC179A64E1891177E1213F4CF0` | `E3E16EC4DDDB088AF425A1CC53C2D374B7C352DC179A64E1891177E1213F4CF0` | **unchanged** |
| `Chiffres_cles_CRUI_1er_semestre_2024_Arabe.json` | `C248893E7C681167759ABD96710E98B6F2C42A97F07FE21FC1176A704B39E205` | `C248893E7C681167759ABD96710E98B6F2C42A97F07FE21FC1176A704B39E205` | **unchanged** |
| `Chiffres_cles_CRUI_1er_semestre_2024_Espagnol.json` | `0949D4EB1297677FC5DBDE68DA0B4E3B8BDC44C02531DBE0CDAF5C3F75C2B97F` | `0949D4EB1297677FC5DBDE68DA0B4E3B8BDC44C02531DBE0CDAF5C3F75C2B97F` | **unchanged** |
| `Chiffres_cles_CRUI_1er_semestre_2024_Francais.json` | `CC3954B0DEF435F1EED9285B5ED3D0551B808C9AABAEF24F89B2420ACC2926D7` | `CC3954B0DEF435F1EED9285B5ED3D0551B808C9AABAEF24F89B2420ACC2926D7` | **unchanged** |
| `ESP_Chiffres_cles_annee_2025.json` | `020E8CB83A49193D1EFE7D2FB8CEFC2A79A2FB6373D7E68C52058E0F143BCBA9` | `020E8CB83A49193D1EFE7D2FB8CEFC2A79A2FB6373D7E68C52058E0F143BCBA9` | **unchanged** |
| `Eng_Chiffres_cles_annee_2025.json` | `BE8863389CE4980E9ADC8BF53B892416FFB863809D0E5EE41FC1CE4D9F20BD93` | `BE8863389CE4980E9ADC8BF53B892416FFB863809D0E5EE41FC1CE4D9F20BD93` | **unchanged** |
| `FR_Chiffres_cles_annee_2025.json` | `96DE89AA6BAE24D094142AFE8EE69B550216D78686CA1CD5B4899F434FF9294E` | `96DE89AA6BAE24D094142AFE8EE69B550216D78686CA1CD5B4899F434FF9294E` | **unchanged** |

All eight target documents retain exact source spans and page provenance. No raw JSON file was written.
