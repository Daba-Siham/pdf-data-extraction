# Phase 3G.1 — Section topic-ID consistency fix

Only section-level `topic_id` values were checked and synchronized in the eight phase-3G documents. Chunk IDs, chunk boundaries, source spans, source text, temporal metadata, and all non-target files were left unchanged.

## Documents checked

- `Fr_Indicateurs_climat_investissement.json`: 1 section(s), 0 section topic ID(s) changed, 14 chunks preserved.
- `ENG_Indicateurs_climat_investissement.json`: 1 section(s), 0 section topic ID(s) changed, 14 chunks preserved.
- `ESP_Indicateurs_climat_investissement.json`: 1 section(s), 0 section topic ID(s) changed, 14 chunks preserved.
- `Guide_de_Conciliation_AR.json`: 1 section(s), 0 section topic ID(s) changed, 7 chunks preserved.
- `Guide_de_Conciliation_ES.json`: 1 section(s), 0 section topic ID(s) changed, 7 chunks preserved.
- `Guide_programme_integre_appui_financement_entreprises_AR.json`: 1 section(s), 0 section topic ID(s) changed, 3 chunks preserved.
- `Brochure_secteur_Logistique.json`: 1 section(s), 0 section topic ID(s) changed, 6 chunks preserved.
- `FR_Chiffres_cles_CRITTA_30_Sept_2024.json`: 1 section(s), 1 section topic ID(s) changed, 14 chunks preserved.

## Topic-ID changes

| Document | Old topic_id | New topic_id |
|---|---|---|
| `FR_Chiffres_cles_CRITTA_30_Sept_2024.json` | `regional_statistics` | `crui_activity` |

The corpus uses one root section with multiple one-chunk subsections in these files. The root section therefore retains the family/document primary concept; granular concepts remain in each chunk’s canonical `semantic_tags`. The only stale root ID was CRUI `regional_statistics`, corrected to `crui_activity`. Climate, conciliation, integrated-financing, and logistics root IDs were already the intended primary concepts.

## Consistency checks

- `Fr_Indicateurs_climat_investissement.json`: PASS — canonical section topic, metadata.topics union, and unchanged chunk structure.
- `ENG_Indicateurs_climat_investissement.json`: PASS — canonical section topic, metadata.topics union, and unchanged chunk structure.
- `ESP_Indicateurs_climat_investissement.json`: PASS — canonical section topic, metadata.topics union, and unchanged chunk structure.
- `Guide_de_Conciliation_AR.json`: PASS — canonical section topic, metadata.topics union, and unchanged chunk structure.
- `Guide_de_Conciliation_ES.json`: PASS — canonical section topic, metadata.topics union, and unchanged chunk structure.
- `Guide_programme_integre_appui_financement_entreprises_AR.json`: PASS — canonical section topic, metadata.topics union, and unchanged chunk structure.
- `Brochure_secteur_Logistique.json`: PASS — canonical section topic, metadata.topics union, and unchanged chunk structure.
- `FR_Chiffres_cles_CRITTA_30_Sept_2024.json`: PASS — canonical section topic, metadata.topics union, and unchanged chunk structure.

## Change invariants

- Chunk boundaries changed: 0
- Chunk IDs changed: 0
- Source spans changed: 0
- Source text changed: 0
- Temporal metadata changed: 0

## Exact provenance validation

PASS for all eight documents. Every source span remains an exact non-empty substring of its corresponding raw page; page bounds and ordered chunk text remain consistent.

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
