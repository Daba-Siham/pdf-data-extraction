# Semantic Quality Audit — Phase 3E

## Scope and method

This was a read-only audit. No semantic JSON, raw JSON, application code, vector database, or prompt file was modified. The audit covered the remaining 15 semantic documents in the families listed below. The already reviewed families were excluded from detailed re-audit.

Checks performed:

- inspected section, subsection, chunk, title, topic, tag, content-type, temporal, and provenance metadata;
- compared multilingual family structures where more than one language exists;
- calculated chunk-size diagnostics;
- checked `metadata.topics` against the union of chunk `semantic_tags`;
- ran `scripts/validate_semantic_json.py --source-dir data/raw/json` on every audited document.

## Classification summary

| Recommendation | Documents | Priority meaning |
|---|---:|---|
| `PASS_SEMANTIC` | 0 | Ready for semantic-layer handoff without another refinement pass |
| `MINOR_FIX` | 8 | Metadata, topic, content-type, or temporal corrections; no major boundary redesign |
| `REFINE` | 7 | Meaningful chunk-boundary or conceptual restructuring required |

The classification is conservative: a document can be structurally valid and still require refinement before ingestion because its current units are not sufficiently specific retrieval units.

## Document-by-document audit

### `investment_climate_indicators`

Documents: `Fr_Indicateurs_climat_investissement.json`, `ENG_Indicateurs_climat_investissement.json`, `ESP_Indicateurs_climat_investissement.json`.

Recommendation: **`MINOR_FIX` — medium priority**.

- The 14 two-page units follow real survey/report sections: context, main results, export destinations, satisfaction, motivations, sustainability, CRI support, expectations, improvement areas, and summary.
- `statistics` is appropriate for the current chunks.
- The three editions have aligned 14-unit structures and the same canonical section topic `business_climate`.
- The main weakness is overly generic tagging: every chunk uses only `business_climate`, despite clearly identifiable concepts such as export_destinations, investor_satisfaction, sustainability, cri_support, and improvement_priorities.
- Document-level and chunk-level temporal metadata are null. This is acceptable only if no explicit edition/reference date can be established from the source; the source should be checked for the survey/reference period during a later minor-fix pass.
- No major semantic boundary redesign is required.

### `manar_al_moustatmir_news_2023`

Documents: `Manar_Al_Moustatmir_News.json` (FR), `Manar_Al_Moustatmir_ENG_PNG.json` (EN), `Akhbar_Al_Moustatmir_News.json` (AR).

Recommendation: **`REFINE` — high priority**.

- Current units are mostly fixed three-page groups: 16 FR, 16 EN, and 15 AR chunks.
- Several units contain multiple independent editorial items: highlights, tourism profiles, CRUI statistics, conciliation results, aquaculture focus, interview/FAQ material, guides, and project/news cards.
- The content type is `narrative` for every chunk, although the source visibly contains statistics, FAQ/interview material, institutional news, sector features, and project announcements.
- The current single tag `investment_news` is too generic for independent retrieval.
- FR/EN have broadly parallel page ranges; Arabic has a different page count and layout. The family assignment is plausible, but exact article-level alignment is not established by the current structure.
- Publication/reference metadata is null even though the edition is explicitly 2023 in the source titles. This is a minor metadata issue within the larger required refinement.
- OCR/heading concern: some English headings are visibly unusable (`in @ © f`, `48 on`, `Be .`), and Arabic headings should be checked for broken extraction. Raw text should remain unchanged, but semantic headings need conservative source-supported labels.
- Required future structure: independent article/news units, with separate statistics, FAQ/interview, sector-feature, event, and project-news tags/types.

### `conciliation_guide`

Documents: `Guide_de_Conciliation_AR.json`, `Guide_de_Conciliation_ES.json`.

Recommendation: **`MINOR_FIX` — medium priority**.

- Seven chunks per language correspond to recognizable units: cover/editorial, definition, missions, opening a process, process development, and the conciliator mission.
- The units are already independently retrievable and are not arbitrary multi-page groups.
- `procedure` is too broad for all seven units. Definition/editorial chunks are better represented as `narrative` or `faq`; question-form chunks should use `faq`; process steps can remain `procedure`; contact/request material should be separated if present.
- FR is absent from the current semantic corpus inventory, so cross-language alignment is only AR/ES at present. Do not infer that the family is complete.
- Topic `conciliation` is useful but can be supplemented with stable tags such as conciliation_definition, conciliation_process, conciliator, and eligibility/conditions when explicitly present.

### `investment_business_support_single_window`

Documents: `Investment_Business_Support_Single_Window_FR.json`, `Investment_Business_Support_Single_Window_ES.json`.

Recommendation: **`REFINE` — medium priority**.

- The seven units are broad two-page groups. The overall editorial sequence is meaningful: CRI role, investor support, Manar Al Moustatmir, territorial planning, investment acts/procedures, Manar platform, and contact.
- However, the investment-acts/procedures section contains several independent services and administrative categories in one retrievable unit.
- The Manar and CRI service offerings also combine multiple services that should be independently retrievable: facilitation, authorization, territorial intelligence, support, and digital request tracking.
- All chunks are `service`, including introduction, administrative procedure, and final contact content. Content types should be differentiated into `narrative`, `service`, `procedure`, `contact_information`, and possibly `table`.
- FR/ES have matching seven-unit layouts, shared family ID, shared topic `business_support`, and publication metadata 2019. The 2019 edition value should be retained only if explicitly supported by the source, not merely inherited from a historical reference.

### `electricity_water_sanitation_connection`

Document: `Guide_branchement_electricite_eau_assainissement.json`.

Recommendation: **`REFINE` — high priority**.

- Seven chunks are mostly two-page groups and the source contains materially different procedures: provisional connection, medium-voltage electricity, drinking water, sanitation, documents/requirements, and contacts.
- The current single topic `utility_connections` and all-`procedure` classification hide the service dimension and merge distinct utility procedures.
- Electricity, water, and sanitation should become independently retrievable units, with separate requirements/steps/contact units where source boundaries support them.
- `metadata.publication_year` and `reference_period` are currently 2002/edition. This appears suspicious because the source is a utility guide and the first years in extracted text may be historical/legal references. It requires explicit source confirmation before retaining; otherwise it should be null.
- The largest chunk is 5,444 characters and should be reviewed for semantic boundaries before any later retrieval subchunking decision.

### `integrated_business_support_financing`

Document: `Guide_programme_integre_appui_financement_entreprises_AR.json`.

Recommendation: **`MINOR_FIX` — medium priority**.

- Three chunks cover an overview, the financing offer, and the integrated support/financing programme.
- The chunks are coherent at document level, but all are classified `financial_product`; the overview and explanatory/eligibility material should be differentiated from financial-product content.
- The current tag `integrated_financing` is useful but should be supplemented with product/programme, beneficiaries, eligibility, financing conditions, and support tags when explicitly supported.
- The short document does not require a large boundary redesign, but product amounts, rates, beneficiaries, eligibility, and contacts should be checked for independent retrieval units.
- Only Arabic is currently present in this family inventory; multilingual family completeness should not be assumed.

### `production_factor_cost_guide_2024`

Document: `Nv_Guide_Cout_facteurs_CRI_2024.json`.

Recommendation: **`REFINE` — high priority**.

- The 32 two-page units follow the guide reasonably well, but several units combine multiple independent cost categories or table groups.
- Every chunk is `cost_information` and every tag is only `production_costs`. This loses useful retrieval distinctions such as company creation, architecture, land, construction, labor, energy/water/sanitation, transport, import duties, certification, telecom, training, and quality of life.
- Examples of broad or mixed units include construction/material tables, labor plus legal calendar material, energy/AEP/sanitation tables, multiple transport modes, import-duty tables, telecom, and training programmes.
- The guide is dated 2024 in its metadata and source title context, but individual tables have their own reference dates (for example August 2024 and transport tariffs 2024). These should be represented at chunk level rather than treated as one undifferentiated edition date.
- The semantic parent layer should be reorganized around cost category/table units; later retrieval subchunking can remain separate.

### `logistics_sector_brochure`

Document: `Brochure_secteur_Logistique.json`.

Recommendation: **`MINOR_FIX` — low priority**.

- Six two-page units correspond to recognizable brochure sections: national strategy, regional logistics infrastructure, Fnideq economic activity zone, Tanger Med, and logistics operators.
- The current broad narrative classification is acceptable for explanatory sections, but infrastructure and operator directories should use more specific tags and possibly `statistics`, `industrial_zone`, or `contact_information` where the source is primarily factual.
- All chunks use only `logistics_sector`; useful tags such as logistics_strategy, logistics_infrastructure, fnideq_economic_zone, tanger_med, and logistics_operators are absent.
- Chunk sizes are moderate (maximum 3,744 characters); no urgent retrieval-size problem is present.
- No large semantic restructuring is required.

### `crui_key_figures_2024_09_30`

Document: `FR_Chiffres_cles_CRITTA_30_Sept_2024.json`.

Recommendation: **`MINOR_FIX` — medium priority**.

- One-page chunks are acceptable for this short statistical card because each page contains a distinct indicator or related chart.
- `statistics` is appropriate, but all chunks use only `regional_statistics`; the document should expose stable concepts such as CRUI activity, approved projects, investment amount, jobs, business creation, sector distribution, territorial distribution, conciliation, and CRI academy.
- The source explicitly says “au 30 septembre 2024”, but document and chunk temporal metadata are null. The family should use an as-of date or reference period representing 30 September 2024.
- Headings are often repeated generic OCR/extraction text (“Une fois vous êtes ici, vous êtes partout !”), reducing usability of current semantic metadata.
- No page-boundary restructuring is required.

## Chunk-size table

| Document | Chunks | Min | Median | Mean | Max | >3,000 | >5,000 | >8,000 | >12,000 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Akhbar_Al_Moustatmir_News.json | 15 | 846 | 1,573.0 | 2,124.1 | 4,425 | 2 | 0 | 0 | 0 |
| Brochure_secteur_Logistique.json | 6 | 636 | 3,372.0 | 2,675.8 | 3,744 | 4 | 0 | 0 | 0 |
| ENG_Indicateurs_climat_investissement.json | 14 | 264 | 965.0 | 1,037.6 | 1,988 | 0 | 0 | 0 | 0 |
| ESP_Indicateurs_climat_investissement.json | 14 | 296 | 1,043.5 | 1,177.6 | 2,348 | 0 | 0 | 0 | 0 |
| FR_Chiffres_cles_CRITTA_30_Sept_2024.json | 14 | 101 | 294.0 | 381.1 | 1,422 | 0 | 0 | 0 | 0 |
| Fr_Indicateurs_climat_investissement.json | 14 | 308 | 1,001.0 | 1,189.1 | 2,376 | 0 | 0 | 0 | 0 |
| Guide_branchement_electricite_eau_assainissement.json | 7 | 35 | 2,636.0 | 2,845.6 | 5,444 | 3 | 1 | 0 | 0 |
| Guide_de_Conciliation_AR.json | 7 | 326 | 762.0 | 743.1 | 1,286 | 0 | 0 | 0 | 0 |
| Guide_de_Conciliation_ES.json | 7 | 413 | 1,075.0 | 981.0 | 1,455 | 0 | 0 | 0 | 0 |
| Guide_programme_integre_appui_financement_entreprises_AR.json | 3 | 925 | 1,393.0 | 1,589.7 | 2,451 | 0 | 0 | 0 | 0 |
| Investment_Business_Support_Single_Window_ES.json | 7 | 185 | 2,199.0 | 2,079.4 | 3,385 | 3 | 0 | 0 | 0 |
| Investment_Business_Support_Single_Window_FR.json | 7 | 181 | 2,259.0 | 2,138.9 | 3,473 | 3 | 0 | 0 | 0 |
| Manar_Al_Moustatmir_ENG_PNG.json | 16 | 862 | 2,946.0 | 2,866.8 | 4,616 | 7 | 0 | 0 | 0 |
| Manar_Al_Moustatmir_News.json | 16 | 849 | 2,116.0 | 2,679.9 | 4,936 | 6 | 0 | 0 | 0 |
| Nv_Guide_Cout_facteurs_CRI_2024.json | 32 | 193 | 1,487.0 | 1,468.8 | 3,545 | 1 | 0 | 0 | 0 |

The size findings do not by themselves determine refinement. The news, utility, and cost-guide problems are semantic-boundary problems; moderate-size climate/logistics/statistics chunks mainly need metadata specificity. No audited document has chunks above 8,000 characters.

## Metadata topics consistency

All 15 audited documents have `metadata.topics` equal to the exact union of current chunk `semantic_tags`. No stale or missing document-level topic was detected by the consistency check.

This does not mean the tags are sufficiently useful: many families have one generic tag for every chunk. That is why the climate, logistics, CRUI, financing, and news families still receive metadata or semantic refinement recommendations.

## Multilingual family alignment

| Family | Languages present | Assessment |
|---|---|---|
| `investment_climate_indicators` | FR, EN, ES | Strong structural alignment: 14 corresponding two-page units and shared `business_climate`; concept tags are too generic. |
| `manar_al_moustatmir_news_2023` | FR, EN, AR | Likely same 2023 news edition, but page counts/layouts differ and article-level alignment is not established. Requires article-boundary audit. |
| `conciliation_guide` | AR, ES | Seven corresponding units and shared `conciliation`; content-type specificity is the main issue. |
| `investment_business_support_single_window` | FR, ES | Seven corresponding units and shared `business_support`; several service/procedure concepts remain combined. |
| Other audited families | one language currently present | No cross-language alignment can be verified from the current semantic inventory. |

## OCR and heading concerns

- News: several headings are unusable OCR fragments, especially in the English edition; Arabic and French headings also include extraction artifacts. Semantic headings need conservative reconstruction from readable article content.
- CRUI 30 September 2024: repeated slogan headings obscure the actual statistic represented by each page.
- Utility guide: headings are usable at the procedure level, but the current broad titles do not expose individual utility/service names consistently.
- Cost guide: some table headings are truncated or generic (“Nature du…”, “Prix”, “Missions”), which makes category tagging important.
- Climate and conciliation documents have generally usable headings.

## Provenance and validator results

Canonical validator command:

`python scripts/validate_semantic_json.py --source-dir data/raw/json <15 audited semantic JSON files>`

Result: **15/15 PASS**.

The validator confirmed schema 2.2, required fields, controlled content types, unique chunk IDs, page bounds, exact source-span membership, and UTF-8-readable JSON for every audited document. No provenance failure was found.

## Documents by recommendation

### PASS_SEMANTIC

None. The remaining corpus has no document that needs absolutely no semantic or metadata improvement before the loader phase, although the logistics brochure and climate indicators are close to this threshold.

### MINOR_FIX

- `Fr_Indicateurs_climat_investissement.json` — medium: add specific concept tags and verify reference period.
- `ENG_Indicateurs_climat_investissement.json` — medium: same multilingual concept-tag/period correction.
- `ESP_Indicateurs_climat_investissement.json` — medium: same multilingual concept-tag/period correction.
- `Guide_de_Conciliation_AR.json` — medium: distinguish FAQ, narrative, procedure, and conditions.
- `Guide_de_Conciliation_ES.json` — medium: distinguish FAQ, narrative, procedure, and conditions.
- `Guide_programme_integre_appui_financement_entreprises_AR.json` — medium: correct content-type granularity and add product/eligibility tags.
- `Brochure_secteur_Logistique.json` — low: add infrastructure, zone, operator, statistics, and contact semantics.
- `FR_Chiffres_cles_CRITTA_30_Sept_2024.json` — medium: add 30 September 2024 temporal metadata and specific statistic tags.

### REFINE

- `Manar_Al_Moustatmir_News.json` — high: split independent news/editorial/FAQ/statistics/project items.
- `Manar_Al_Moustatmir_ENG_PNG.json` — high: same article-level restructuring plus OCR heading review.
- `Akhbar_Al_Moustatmir_News.json` — high: same article-level restructuring and Arabic edition alignment.
- `Investment_Business_Support_Single_Window_FR.json` — medium: separate independently retrievable CRI services and procedures.
- `Investment_Business_Support_Single_Window_ES.json` — medium: align the same service/procedure structure in Spanish.
- `Guide_branchement_electricite_eau_assainissement.json` — high: separate electricity, water, sanitation, requirements, steps, and contacts; verify the suspicious 2002 metadata.
- `Nv_Guide_Cout_facteurs_CRI_2024.json` — high: restructure by independent cost categories and reference tables.

## Recommended refinement order

1. Manar/Akhbar news family — article boundaries and multilingual edition audit.
2. Production-factor cost guide — category/table restructuring and reference-date metadata.
3. Utility connection guide — electricity/water/sanitation procedure separation and year correction.
4. Single-window FR/ES — service and procedure separation.
5. CRUI 30 September 2024 — temporal and statistic-tag correction.
6. Integrated financing and conciliation — content-type/tag corrections.
7. Climate indicators and logistics brochure — specific concept tags and modest metadata refinement.

## Final recommendation

Before adapting the RAG loader and Qdrant ingestion, another semantic-refinement phase is required for the three news documents, the production-factor cost guide, the utility-connection guide, and the two single-window documents. The climate indicators, conciliation guides, integrated financing document, logistics brochure, and September 2024 CRUI card can be handled in a smaller metadata/content-type refinement pass first; none currently has a provenance or schema blocker.
