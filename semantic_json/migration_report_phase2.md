# Semantic JSON migration report — phase 2

## Scope

Schema 2.1 was applied to the existing French 2025 key-figures document and one additional French financing guide. The remaining 31 source documents were not converted.

## 1. Schema changes from 2.0 to 2.1

- `schema_version` is now `2.1`.
- `section.topic` was replaced by language-independent `section.topic_id`.
- Human-readable section titles, subsection titles, and `heading_path` are now in the source language.
- Every chunk now has controlled `semantic_tags`.
- Every chunk now has `temporal_scope`, including `primary_year`, explicit `years_mentioned`, and a structured `reference_period`.
- Content types were reviewed as the primary form of knowledge rather than as a broad subject label.
- Page ranges remain provenance metadata and are not used as the semantic section hierarchy.

## 2. Corrections to the 2025 key-figures document

- Display headings were translated back to French: for example, `Création d’entreprises`, `Bilan de la CRUI`, and `Promotion et partenariats`.
- Pages 7–9 are classified as `statistics`; industrial, tourism, and energy concepts are represented through tags.
- Page 11 is `statistics`, because it reports PIAFE results rather than defining a financial product.
- Page 13 is `statistics`, because it reports competition results.
- Page 16 is `service`, because it mentions eligibility conditions but does not enumerate them.
- Key-figures chunks: **18**; useful pages represented: 1–18.

## 3. Financing-guide semantic structure

The 184-page guide is organized into semantic areas: guide presentation, contacts and navigation, financing matrices, equity and entrepreneur support, microcredit, bank financing, leasing, public financing bodies, international financing, equity investment, capital markets, business-plan preparation, credit guarantees, contact directory, and financial glossary.

The product-oriented sections preserve coherent multi-page units such as Green Invest, Renovotel, MDM Invest, PIAFE, leasing, bank credit categories, public programmes, FINÉA, FDII, FDA, export support, investment funds, and share issuance.

- Financing-guide chunks: **46**
- Chunks spanning multiple pages: **38**
- Pages producing multiple chunks: none in this phase
- Empty separator pages were not included in provenance ranges: 16, 22, 40, 46, 54, 58, 70, 76, 80, 82, 94, 102, 116, 120, 124, 130, 136, and 176.

## 4. Financing-guide content types

| Content type | Chunk count |
|---|---:|
| `contact_information` | 2 |
| `financial_product` | 28 |
| `legal_information` | 2 |
| `narrative` | 8 |
| `procedure` | 1 |
| `service` | 3 |
| `table` | 2 |

The guide uses `financial_product` for product/programme descriptions, `eligibility_conditions` through tags where eligibility is discussed, `procedure` for business-plan guidance, `contact_information` for contact directories, `table` for matrices/financial tables, `service` for support/expertise, `legal_information` for legal annexes/guarantees, and `narrative` for explanatory material.

## 5. Semantic tags

Tags are language-independent snake_case identifiers. The most frequent guide tags are:

- `public_financing`: 14
- `bank_credit`: 7
- `investment_financing`: 5
- `financing_products`: 4
- `guide_overview`: 4
- `working_capital`: 4
- `business_financing`: 3
- `business_plan`: 3
- `guarantees`: 3
- `trade_finance`: 3
- `business_support`: 2
- `contact_information`: 2
- `eligibility_conditions`: 2
- `equipment_financing`: 2
- `equity_financing`: 2
- `export_financing`: 2
- `industrial_investment`: 2
- `international_financing`: 2
- `investment_agreements`: 2
- `investment_charter`: 2
- `startup_financing`: 2
- `agricultural_investment`: 1
- `bank_financing`: 1
- `beneficiaries`: 1
- `business_creation`: 1
- `business_growth`: 1
- `capital_markets`: 1
- `cofinancing`: 1
- `collateral`: 1
- `credit_guarantees`: 1
- `entrepreneur_support`: 1
- `entrepreneurship`: 1
- `equity_investment`: 1
- `expertise`: 1
- `financial_glossary`: 1
- `financial_literacy`: 1
- `financial_plan`: 1
- `financial_tables`: 1
- `financing_matrix`: 1
- `financing_organizations`: 1
- `green_investment`: 1
- `guide_structure`: 1
- `import_financing`: 1
- `income_generating_activities`: 1
- `innovation`: 1
- `investor_support`: 1
- `leasing`: 1
- `legal_information`: 1
- `love_money`: 1
- `marketing_support`: 1
- `microcredit`: 1
- `mre_support`: 1
- `participative_finance`: 1
- `piafe`: 1
- `private_markets`: 1
- `project_preparation`: 1
- `public_markets`: 1
- `real_estate_financing`: 1
- `renovation`: 1
- `signature_credit`: 1
- `sme_support`: 1
- `subsidy`: 1
- `tax_information`: 1
- `tourism_financing`: 1
- `tpe_financing`: 1
- `tpe_support`: 1
- `treasury_financing`: 1
- `venture_capital`: 1
- `youth_support`: 1

## 6. Temporal metadata examples

- The 2025 cover chunk has `primary_year: 2025` and `years_mentioned: [2025]`.
- The 2025 promotion page contains several explicit years, so its `primary_year` is null while all explicit years remain in `years_mentioned`.
- The financing-guide cover/front-matter chunk has `primary_year: 2022`, supported by the edition text.
- Financing-product chunks do not inherit 2022 as a primary year unless the chunk itself clearly states that year.

## 7. Uncertain classifications

- Some table-of-contents pages are retained with their surrounding semantic section because they contain navigation information, not new factual product terms.
- Several pages contain multiple product labels or continuation material. Where the source page did not provide safe text offsets in the target schema, the related page group was kept as one coherent product-family chunk rather than duplicating or inventing text boundaries.
- The document-level 2022 edition year is reliable; individual products may reflect different programme periods that are not always explicitly dated.

## 8. OCR concerns

The source contains OCR/layout artifacts such as `L`, `a`, broken words, decorative page elements, URLs, and inconsistent spacing. No aggressive OCR correction was applied. Numbers, rates, amounts, names, and source wording were preserved.

## 9. Validation results

- UTF-8 JSON parsing: passed for both documents.
- Schema 2.1 validator: passed for both documents.
- Unique chunk IDs: passed.
- Page provenance and exact source-page text comparison: passed.
- Useful-page coverage: passed for both documents.
- Source-language headings: present in French for both documents.
- Original numerical/source information: preserved; no translation or LLM summary was used.
- Source files in `data/raw/json`: not modified.
