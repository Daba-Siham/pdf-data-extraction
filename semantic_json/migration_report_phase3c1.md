# Industrial-zone identity verification report — phase 3c1

## Scope

Only the ten ambiguous profiles from phase 3c were checked. No non-ambiguous profile, raw file, or application component was modified.

## Verification table

| Language | Current zone ID | Pages | Status | Evidence | Action |
|---|---|---:|---|---|---|
| en | `tanger_free_zone` | 7–9 | `confirmed` | Pages 7 and 9 explicitly say `Tangier Free Zone (TFZ)` and page 9 supplies its profile attributes. matched=['Tangier Free Zone', 'TFZ']; assigned=tanger_free_zone | kept current ID |
| en | `tanger_industrial_zone` | 10–12 | `confirmed` | Pages 10–12 identify `IPZ | Tangier`, the Tangier industrial-zone association, and the 138 Ha / 30,000 jobs profile. matched=['IPZ\\s*\\|\\s*Tangier', 'Total Area']; assigned=tanger_industrial_zone | kept current ID |
| en | `tanger_tech` | 16–18 | `confirmed` | Pages 16 and 18 explicitly identify `Mohammed VI Tangier Tech City`, Smart City activity, and Tangier Tech Development Company. matched=['Mohammed VI Tangier Tech City', 'Smart City', 'Tangier Tech Development']; assigned=tanger_tech | kept current ID |
| en | `tetouan_industrial_zone` | 58–60 | `incorrect_assignment` | Pages 58 and 60 explicitly identify `IPZ | Tetouan Intra-port Zones`, with Tetouan municipality as manager; this is a logistics/intra-port profile, not the generic industrial-zone assignment. matched=['IPZ\\s*\\|\\s*Tetouan Intra-port Zones', 'Commune of Tetouan']; assigned=tetouan_intraport_zone | corrected to `tetouan_intraport_zone` |
| en | `loukkos_agropole` | 66–68 | `confirmed` | Pages 66 and 68 explicitly identify `Agropole of Loukkos`, Larache, agrifood activity, and MEDZ. matched=['Agropole of Loukkos', 'Agrifood', 'MEDZ']; assigned=loukkos_agropole | kept current ID |
| es | `tanger_industrial_zone` | 10–12 | `confirmed` | Pages 10–12 identify `ZI | Tánger`, the 138 Ha / 146 plots profile, and AZIT as administrator. matched=['ZI\\s*I\\s*T[ÃÁ]nger', 'Superficie total', 'AZIT']; assigned=tanger_industrial_zone | kept current ID |
| es | `larache_intraport_zone` | 75–77 | `confirmed` | Pages 75–77 explicitly identify the Larache intra-port zone, fishing-related activity, and ANP. matched=['Zona Intraportuaria de Larache', 'Actividades relacionadas con la pesca', 'ANP']; assigned=larache_intraport_zone | kept current ID |
| fr | `asilah_zone` | 28–30 | `confirmed` | Pages 28–30 explicitly identify `ZAE | ASSILAH` and provide the operational profile and area information. matched=['ZAE\\s*\\|\\s*ASSILAH', 'Superficie Totale', 'Opérationnelle']; assigned=asilah_zone | kept current ID |
| fr | `tetouan_shore` | 50–52 | `confirmed` | Pages 50 and 52 explicitly identify Tétouan Shore and provide the 20 Ha / 10,000 projected-jobs profile. matched=['TETOUAN\\s+SHORE', '10\\s*000', '20 Ha']; assigned=tetouan_shore | kept current ID |
| fr | `loukkos_agropole` | 66–68 | `confirmed` | Pages 66 and 68 explicitly identify Agropole du Loukkos in Larache and its agroalimentaire profile. matched=['Agrop[ÃÔ]le du Loukkos', 'LARACHE', 'Agroalimentaire']; assigned=loukkos_agropole | kept current ID |

## Summary

- Confirmed directly: 9
- Confirmed by cross-language evidence: 0
- Remaining uncertain: 0
- Incorrect assignments corrected: 1
- Semantic files actually changed: ['ENG_Panorama_des_ZI.json', 'FR_Panorama_Zones_economiques_industrielles.json', 'ES_Panorama_des_ZI.json']

## Correction

The English pages 58–60 assignment was corrected from `tetouan_industrial_zone` to `tetouan_intraport_zone`. The raw pages explicitly identify `IPZ | Tetouan Intra-port Zones`, and the profile names Tetouan municipality as manager. The topic is now `logistics_zone_profile`; source spans and source text are unchanged.

## Metadata consistency

For all three panorama documents, `metadata.topics` was recomputed as the exact sorted union of current chunk `semantic_tags`. The stale `tetouan_industrial_zone` value is absent unless supported by another chunk; `tetouan_intraport_zone` is present in the English metadata.

## Validation

- `ENG_Panorama_des_ZI.json` phase-specific exact provenance validation: PASS
- `ES_Panorama_des_ZI.json` phase-specific exact provenance validation: PASS
- `FR_Panorama_Zones_economiques_industrielles.json` phase-specific exact provenance validation: PASS

Canonical validator result: all three documents passed.

## Raw SHA-256 integrity

| Raw file | Before | After | Status |
|---|---|---|---|
| `FR_Panorama_Zones_economiques_industrielles.json` | `5389B0F0CD19E4E148CC2F9D0C3FC813E105063702EA083E447C1AB04F4107A7` | `5389B0F0CD19E4E148CC2F9D0C3FC813E105063702EA083E447C1AB04F4107A7` | **unchanged** |
| `ENG_Panorama_des_ZI.json` | `13CDB1DC6DC139BE04B59A2119F7AC522FF18A085E82D52B5CA15DDFD4E1C5C0` | `13CDB1DC6DC139BE04B59A2119F7AC522FF18A085E82D52B5CA15DDFD4E1C5C0` | **unchanged** |
| `ES_Panorama_des_ZI.json` | `482AC9C42D5050A8D27002C05533562790246036A0C32E4000EBF51B0788B05B` | `482AC9C42D5050A8D27002C05533562790246036A0C32E4000EBF51B0788B05B` | **unchanged** |

## Human review

- No profile remains unresolved by this targeted verification.
- The corrected English Tetouan intra-port profile should be reviewed once against the source PDF layout before production ingestion.
