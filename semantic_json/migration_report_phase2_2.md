# Semantic JSON migration report — phase 2.2

## 1. Changes from 2.1 to 2.2

- Schema version is now `2.2`.
- Canonical language-independent `topic_id` values are enforced.
- Every chunk now contains exact `source_spans`.
- Validation checks exact substring provenance instead of requiring complete pages.
- Coverage reports zero-, one-, and multi-chunk page representation without rejecting repeated page use.
- No embedding-sized or overlap-based subchunking was introduced.

## 2. Corrected topic IDs

| Source-language section | Canonical topic_id |
|---|---|
| Dynamique d’investissement 2025 | `regional_investment_overview` |
| Création d’entreprises | `business_creation` |
| Bilan de la CRUI | `crui_activity` |
| Dynamique des investissements sectoriels | `sector_investment` |
| Accompagnement des entreprises et entrepreneuriat | `business_support` |
| Promotion et partenariats | `promotion_partnerships` |
| Message de clôture | `closing_message` |

## 3. Chunk refinement

- 2025 key-figures chunks: 18 (unchanged)
- Financing-guide chunks before refinement: 46
- Financing-guide chunks after refinement: 113

Independent units separated include microcredit products, INTELAK variants, START TPE, leasing products, amortizable-credit products, treasury products, signature/public-market/import/export products, Mourabaha, Tamwil Chamal, innovation products, Maroc PME programmes, FINÉA products, FDII aids, investment-fund stages, share-issuance products, business-plan tables, contact categories, and glossary ranges.

Multi-page chunks were retained where pages form one product or one coherent continuation, including Prêt TPE, Crédit-bail mobilier, Crédit d’investissement moyen et long terme, Mouwakaba, FINÉA Cautions, industrial ecosystem aid, public share offering, and contact groups.

## 4. Source-span and coverage diagnostics

### FR_Chiffres_cles_annee_2025.json

- Source-span validation: passed
- Useful pages not represented: none
- Useful pages represented once: 18
- Useful pages represented multiple times: 0
- Multi-represented page counts: none

### Guide_du_financement_des_entreprises.json

- Source-span validation: passed
- Useful pages not represented: none
- Useful pages represented once: 164
- Useful pages represented multiple times: 2
- Multi-represented page counts: {29: 2, 37: 2}

## 5. Chunk character-size diagnostics

Statistics cover all 131 semantic chunks across both representative documents.

- Minimum: 37
- Median: 2144
- Average: 2447.79
- Maximum: 10118
- Over 3,000 characters: 36
- Over 5,000 characters: 16
- Over 8,000 characters: 2

Largest chunks:
- `Guide_du_financement_des_entreprises.json` / `guide_du_financement_des_entreprises_contact_directory_banks_leasing`: 10118 characters
- `Guide_du_financement_des_entreprises.json` / `guide_du_financement_des_entreprises_glossary_c_to_e`: 8158 characters
- `Guide_du_financement_des_entreprises.json` / `guide_du_financement_des_entreprises_business_plan_definition`: 7553 characters
- `Guide_du_financement_des_entreprises.json` / `guide_du_financement_des_entreprises_entrepreneurial_support_products`: 7350 characters
- `Guide_du_financement_des_entreprises.json` / `guide_du_financement_des_entreprises_green_invest`: 6907 characters
- `Guide_du_financement_des_entreprises.json` / `guide_du_financement_des_entreprises_business_plan_cover_and_company`: 6758 characters
- `Guide_du_financement_des_entreprises.json` / `guide_du_financement_des_entreprises_credit_bail_mobilier`: 6533 characters
- `Guide_du_financement_des_entreprises.json` / `guide_du_financement_des_entreprises_ebrd_advice`: 6515 characters
- `Guide_du_financement_des_entreprises.json` / `guide_du_financement_des_entreprises_contact_directory_public_capital`: 6339 characters
- `Guide_du_financement_des_entreprises.json` / `guide_du_financement_des_entreprises_partner_messages`: 6293 characters

## 6. Remaining uncertainties and OCR

- Some source pages contain OCR control artifacts, broken words, layout markers, URLs, and inconsistent spacing. No OCR correction was applied.
- Several source pages are continuation pages without repeated product titles; their association was made from the guide’s table of contents and neighboring headings.
- Pages with multiple semantic units are represented by multiple source spans where exact boundaries were identifiable. Other mixed pages remain grouped rather than being split speculatively.
- Exact source spans are validated by substring matching only; no fuzzy matching is used.

## 7. Integrity confirmation

- Both documents validate as schema 2.2.
- Original numerical and factual text is preserved.
- Raw JSON files were read only and their hashes did not change during this phase.
- The remaining 31 documents were not converted.
- Production RAG files were not modified.
