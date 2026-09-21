# Phase 3D — Territorial investment opportunities refinement

## Scope

Only the French and English investors-guide semantic documents were modified. Raw page text is preserved in exact source spans; no RAG or vector-store files were changed.

## Chunk counts

- FR: 166 chunks (previously 95)
- EN: 76 chunks (previously 70)
- Identified project profiles: FR 50; EN 50

## Canonical opportunity IDs

The paired project IDs are stable, language-independent identifiers derived from project names and profile meaning:

`agri_food_flour_mill`, `agri_food_couscous_unit`, `agri_food_fig_processing`, `agri_food_red_fruit_processing`, `agri_food_olive_oil`, `agri_food_biscuit_factory`, `agri_food_sunflower_oil`, `automotive_cannabis_processing`, `automotive_shock_absorbers`, `automotive_filters`, `automotive_brake_pads`, `automotive_electric_bikes`, `construction_cannabis_processing`, `cannabis_cbd_supplements`, `cannabis_cosmetics`, `cannabis_pharmaceuticals`, `tetouan_shopping_center`, `french_school`, `automotive_training_institute`, `electrical_conductors`, `renewable_electricity`, `industrial_thermosetting`, `container_manufacturing`, `wind_turbine_components`, `naval_shipyard`, `fish_canning_unit`, `seafood_waste_processing`, `agar_agar_aquaculture`, `cannabis_seed_import`, `cannabis_transport`, `distribution_company`, `al_hoceima_clinic`, `offshoring_center`, `startup_accelerator`, `textile_cannabis_processing`, `textile_spinning`, `textile_zippers`, `textile_buttons`, `tourism_five_star_hotel`, `tourism_chefchaouen_hotel`, `tourism_club_hotel`, `tourism_water_park`, `tourism_theme_park`, `tourism_science_culture_park`, `tourism_seaside_resort`, `tourism_mini_ski`, `tourism_mountain_lodge`, `tourism_boat_rental`, `tourism_club_biladi`, `tourism_residential_complex`

## FR/EN alignment

| Canonical opportunity ID | FR pages | EN pages | FR title | EN title | Status |
|---|---:|---:|---|---|---|
| `agri_food_flour_mill` | 17–19 | 16–18 | Minoterie industrielle | Industrial flour mill | aligned_with_translation_difference |
| `agri_food_couscous_unit` | 20–22 | 19–21 | Unité industrielle de fabrication du couscous | Industrial unit for couscous | aligned_with_translation_difference |
| `agri_food_fig_processing` | 23–27 | 22–25 | Unité industrielle de valorisation de figues | Industrial unit for fig processing | aligned_with_translation_difference |
| `agri_food_red_fruit_processing` | 28–30 | 26–29 | Unité de valorisation de fruits rouges | Industrial unit for red fruit processing | aligned_with_translation_difference |
| `agri_food_olive_oil` | 31–34 | 30–32 | Unité industrielle d’huile d’olive | Industrial unit for olive oil | aligned_with_translation_difference |
| `agri_food_biscuit_factory` | 35–36 | 33–35 | Unité industrielle de biscuiterie | Biscuit factory | aligned_with_translation_difference |
| `agri_food_sunflower_oil` | 37–40 | 36–41 | Unité industrielle d’huile de tournesol | Industrial unit for sunflower oil | aligned_with_translation_difference |
| `automotive_cannabis_processing` | 43–48 | 42–45 | Unité de transformation du cannabis pour l’industrie automobile | Cannabis processing unit for the automotive industry | aligned_with_translation_difference |
| `automotive_shock_absorbers` | 49–49 | 46–48 | Unité industrielle d’amortisseurs | Industrial unit for shock absorbers | aligned_with_translation_difference |
| `automotive_filters` | 50–52 | 49–51 | Unité industrielle de filtres automobiles | Industrial unit for automotive filters | aligned_with_translation_difference |
| `automotive_brake_pads` | 53–55 | 52–54 | Unité Industrielle De Plaquettes De Freins | Brake pad industrial unit | aligned_with_translation_difference |
| `automotive_electric_bikes` | 56–58 | 55–59 | Assemblage de Vélos & Motos électriques | Electric bike & motorcycle assembly | aligned_with_translation_difference |
| `construction_cannabis_processing` | 61–64 | 60–63 | Unité de transformation du cannabis pour l’industrie du BTP | Cannabis processing unit for the construction materials industry | aligned_with_translation_difference |
| `cannabis_cbd_supplements` | 67–70 | 64–69 | Unité de production de compléments alimentaires à base de CBD | Cannabis-based dietary supplements production unit | aligned_with_translation_difference |
| `cannabis_cosmetics` | 71–74 | 70–73 | Unité de transformation du cannabis pour un usage cosmétique | Cannabis processing unit for cosmetic use | aligned_with_translation_difference |
| `cannabis_pharmaceuticals` | 75–77 | 74–78 | Unité de transformation du cannabis pour un usage pharmaceutique | Cannabis processing unit for pharmaceutical use | aligned_with_translation_difference |
| `tetouan_shopping_center` | 80–82 | 79–81 | Centre commercial | Shopping center | aligned_with_translation_difference |
| `french_school` | 85–86 | 84–85 | École Française | French school | aligned_with_translation_difference |
| `automotive_training_institute` | 87–88 | 86–89 | Institut de Formation aux Métiers de l’Industrie Automobile | Training institute for professions in the automobile industry | aligned_with_translation_difference |
| `electrical_conductors` | 91–94 | 90–93 | Unité industrielle de conducteurs électriques | Industrial Unit for Electrical Conductors | aligned_with_translation_difference |
| `renewable_electricity` | 97–100 | 94–99 | Production électrique renouvelable | Renewable electricity production | aligned_with_translation_difference |
| `industrial_thermosetting` | 103–105 | 102–103 | Unité de thermo-laquage | Thermosetting Unit | aligned_with_translation_difference |
| `container_manufacturing` | 106–107 | 104–106 | Production de conteneurs | Container Manufacturing Unit | aligned_with_translation_difference |
| `wind_turbine_components` | 108–110 | 107–109 | Unité de production d'éoliennes et de leurs parties | Wind Turbine and Components Production Facility | aligned_with_translation_difference |
| `naval_shipyard` | 111–112 | 110–113 | Chantier naval pour bateaux économiques | Naval Shipyard for Economical Pleasure Boats | aligned_with_translation_difference |
| `fish_canning_unit` | 115–117 | 114–116 | Unité de conserves de poisson | Canned Fish Unit | aligned_with_translation_difference |
| `seafood_waste_processing` | 118–121 | 117–120 | Unité de transformation des déchets des industries de transformation de produits de la mer | Unit for the Transformation of Waste from Seafood Processing Industries | aligned_with_translation_difference |
| `agar_agar_aquaculture` | 122–126 | 121–126 | Unité d’aquaculture et industrielle pour la production d’agar agar | Aquaculture and Industrial Unit for Agar Agar Production | aligned_with_translation_difference |
| `cannabis_seed_import` | 128–129 | 127–129 | Importation de semences et de plants de Cannabis | Importation of Cannabis Seeds and Plants | aligned_with_translation_difference |
| `cannabis_transport` | 130–132 | 130–132 | Transport du cannabis | Transportation of Cannabis | aligned_with_translation_difference |
| `distribution_company` | 133–138 | 133–138 | Société de distribution | Distribution Company | aligned_with_translation_difference |
| `al_hoceima_clinic` | 140–142 | 139–141 | Clinique à Al-Hoceima | Clinic in Al-Hoceima | aligned_with_translation_difference |
| `offshoring_center` | 145–147 | 144–147 | Centre d’Offshoring | Offshoring Center | aligned_with_translation_difference |
| `startup_accelerator` | 148–153 | 148–151 | Accélérateur de Start-Up | Start-up Accelerator | aligned_with_translation_difference |
| `textile_cannabis_processing` | 155–158 | 154–157 | Unité de transformation du cannabis pour l’industrie textile | Cannabis Transformation Unit for the Textile Industry | aligned_with_translation_difference |
| `textile_spinning` | 159–161 | 158–160 | Unité industrielle de filature | Industrial Spinning Unit | aligned_with_translation_difference |
| `textile_zippers` | 162–164 | 161–163 | Unité industrielle de fermetures éclair | Industrial Zipper Unit | aligned_with_translation_difference |
| `textile_buttons` | 165–168 | 164–167 | Unité industrielle de boutonnerie | Industrial Button Manufacturing Unit | aligned_with_translation_difference |
| `tourism_five_star_hotel` | 171–172 | 170–171 | Hôtel 5 étoiles | 5-Star Hotel | aligned_with_translation_difference |
| `tourism_chefchaouen_hotel` | 173–175 | 172–174 | Hôtel 4 ou 5 étoiles à Chefchaouen | 4 or 5-Star Hotel in Chefchaouen | aligned_with_translation_difference |
| `tourism_club_hotel` | 176–178 | 175–177 | Hôtel-Club | Club Hotel | aligned_with_translation_difference |
| `tourism_water_park` | 179–181 | 178–180 | Parc Aquatique | Water Park | aligned_with_translation_difference |
| `tourism_theme_park` | 182–183 | 181–182 | Parc d’attractions (A thème) | Theme Park | aligned_with_translation_difference |
| `tourism_science_culture_park` | 184–185 | 183–184 | Parc d’attraction : Science et culture | Theme Park: Science and Culture | aligned_with_translation_difference |
| `tourism_seaside_resort` | 186–189 | 185–188 | Centre balnéaire | Seaside Resort | aligned_with_translation_difference |
| `tourism_mini_ski` | 190–193 | 189–192 | Mini station de Ski à Chakrane | Mini Ski Resort in Chakrane | aligned_with_translation_difference |
| `tourism_mountain_lodge` | 194–197 | 193–196 | Gîte en montagne | Mountain Lodge | aligned_with_translation_difference |
| `tourism_boat_rental` | 198–201 | 197–200 | Agence de plaisance et de location d'embarcations | Pleasure and Boat Rental Agency | aligned_with_translation_difference |
| `tourism_club_biladi` | 202–205 | 201–204 | Village de vacances touristique (Club Biladi) | Touristical holiday village (Club Biladi) | aligned_with_translation_difference |
| `tourism_residential_complex` | 206–210 | 205–208 | Complexe touristique et résidentiel | Tourist and Residential Complex | aligned_with_translation_difference |

The alignment is content-based: titles, sector, territory and profile attributes were compared. It does not require equal page ranges. Both editions contain the same main opportunity catalogue in different layouts; wording and page extents differ.

## Content, sector and territory distributions

### FR

Content types: narrative=28, investment_opportunity=50, statistics=13, service=10, contact_information=65

Sectors: agri_food=7, automotive=5, industry=12, services=2, education=2, renewable_energy=2, fisheries=3, logistics=3, healthcare=1, digital=1, tourism=12

Territories: ouezzane=9, larache=10, al_hoceima=16, chefchaouen=10, tetouan=17, fahs_anjra=12, tanger_assilah=23, mdiq_fnideq=1, regional=2

### EN

Content types: narrative=20, investment_opportunity=50, statistics=5, contact_information=1

Sectors: agri_food=7, automotive=5, industry=12, services=2, education=2, renewable_energy=2, fisheries=3, logistics=3, healthcare=1, digital=1, tourism=12

Territories: ouezzane=9, larache=10, al_hoceima=16, chefchaouen=10, tetouan=17, fahs_anjra=12, tanger_assilah=23, mdiq_fnideq=1, regional=2

## Project page ranges

Project ranges are listed in the alignment table. Multi-page ranges are retained where the source profile is a single coherent opportunity sheet.

## Chunk-size diagnostics

- Total chunks: 242
- Minimum: 21
- Median: 2334.5
- Average: 4488.7
- Maximum: 25916
- >3000: 109
- >5000: 99
- >8000: 62
- >12000: 13

Large chunks:
- `fr` investors_guide_territorial_opportunities_fr_chunk_0001: 25916 chars, pages 1–15
- `fr` investors_guide_territorial_opportunities_fr_chunk_0002: 7637 chars, pages 17–19
- `fr` investors_guide_territorial_opportunities_fr_chunk_0003: 5814 chars, pages 20–22
- `fr` investors_guide_territorial_opportunities_fr_chunk_0004: 11989 chars, pages 23–27
- `fr` investors_guide_territorial_opportunities_fr_chunk_0005: 8223 chars, pages 28–30
- `fr` investors_guide_territorial_opportunities_fr_chunk_0006: 8952 chars, pages 31–34
- `fr` investors_guide_territorial_opportunities_fr_chunk_0007: 5008 chars, pages 35–36
- `fr` investors_guide_territorial_opportunities_fr_chunk_0008: 9154 chars, pages 37–40
- `fr` investors_guide_territorial_opportunities_fr_chunk_0009: 16579 chars, pages 43–48
- `fr` investors_guide_territorial_opportunities_fr_chunk_0011: 7881 chars, pages 50–52
- `fr` investors_guide_territorial_opportunities_fr_chunk_0012: 6058 chars, pages 53–55
- `fr` investors_guide_territorial_opportunities_fr_chunk_0013: 7417 chars, pages 56–58
- `fr` investors_guide_territorial_opportunities_fr_chunk_0014: 10856 chars, pages 61–64
- `fr` investors_guide_territorial_opportunities_fr_chunk_0015: 11197 chars, pages 67–70
- `fr` investors_guide_territorial_opportunities_fr_chunk_0016: 13186 chars, pages 71–74
- `fr` investors_guide_territorial_opportunities_fr_chunk_0017: 9589 chars, pages 75–77
- `fr` investors_guide_territorial_opportunities_fr_chunk_0021: 8128 chars, pages 91–94
- `fr` investors_guide_territorial_opportunities_fr_chunk_0023: 10307 chars, pages 103–105
- `fr` investors_guide_territorial_opportunities_fr_chunk_0024: 3943 chars, pages 106–107
- `fr` investors_guide_territorial_opportunities_fr_chunk_0026: 4417 chars, pages 111–112
- `fr` investors_guide_territorial_opportunities_fr_chunk_0036: 15181 chars, pages 155–158
- `fr` investors_guide_territorial_opportunities_fr_chunk_0037: 6809 chars, pages 159–161
- `fr` investors_guide_territorial_opportunities_fr_chunk_0038: 9234 chars, pages 162–164
- `fr` investors_guide_territorial_opportunities_fr_chunk_0039: 9027 chars, pages 165–168
- `fr` investors_guide_territorial_opportunities_fr_chunk_0018: 5817 chars, pages 80–82
- `fr` investors_guide_territorial_opportunities_fr_chunk_0034: 10286 chars, pages 145–147
- `fr` investors_guide_territorial_opportunities_fr_chunk_0019: 5483 chars, pages 85–86
- `fr` investors_guide_territorial_opportunities_fr_chunk_0020: 4930 chars, pages 87–88
- `fr` investors_guide_territorial_opportunities_fr_chunk_0022: 11168 chars, pages 97–100
- `fr` investors_guide_territorial_opportunities_fr_chunk_0025: 9480 chars, pages 108–110
- `fr` investors_guide_territorial_opportunities_fr_chunk_0027: 5622 chars, pages 115–117
- `fr` investors_guide_territorial_opportunities_fr_chunk_0028: 12395 chars, pages 118–121
- `fr` investors_guide_territorial_opportunities_fr_chunk_0029: 10737 chars, pages 122–126
- `fr` investors_guide_territorial_opportunities_fr_chunk_0030: 6891 chars, pages 128–129
- `fr` investors_guide_territorial_opportunities_fr_chunk_0031: 9033 chars, pages 130–132
- `fr` investors_guide_territorial_opportunities_fr_chunk_0032: 12423 chars, pages 133–138
- `fr` investors_guide_territorial_opportunities_fr_chunk_0033: 9729 chars, pages 140–142
- `fr` investors_guide_territorial_opportunities_fr_chunk_0035: 12451 chars, pages 148–153
- `fr` investors_guide_territorial_opportunities_fr_chunk_0040: 6389 chars, pages 171–172
- `fr` investors_guide_territorial_opportunities_fr_chunk_0041: 8577 chars, pages 173–175
- `fr` investors_guide_territorial_opportunities_fr_chunk_0042: 6126 chars, pages 176–178
- `fr` investors_guide_territorial_opportunities_fr_chunk_0043: 8831 chars, pages 179–181
- `fr` investors_guide_territorial_opportunities_fr_chunk_0044: 4616 chars, pages 182–183
- `fr` investors_guide_territorial_opportunities_fr_chunk_0045: 8054 chars, pages 184–185
- `fr` investors_guide_territorial_opportunities_fr_chunk_0046: 10718 chars, pages 186–189
- `fr` investors_guide_territorial_opportunities_fr_chunk_0047: 9697 chars, pages 190–193
- `fr` investors_guide_territorial_opportunities_fr_chunk_0048: 9732 chars, pages 194–197
- `fr` investors_guide_territorial_opportunities_fr_chunk_0049: 9991 chars, pages 198–201
- `fr` investors_guide_territorial_opportunities_fr_chunk_0050: 9580 chars, pages 202–205
- `fr` investors_guide_territorial_opportunities_fr_chunk_0051: 8261 chars, pages 206–210
- `fr` investors_guide_territorial_opportunities_fr_chunk_0055: 6620 chars, pages 5–5
- `fr` investors_guide_territorial_opportunities_fr_chunk_0058: 3492 chars, pages 8–8
- `fr` investors_guide_territorial_opportunities_fr_chunk_0064: 6031 chars, pages 14–14
- `fr` investors_guide_territorial_opportunities_fr_chunk_0094: 4345 chars, pages 213–213
- `fr` investors_guide_territorial_opportunities_fr_chunk_0103: 3375 chars, pages 222–222
- `fr` investors_guide_territorial_opportunities_fr_chunk_0104: 3780 chars, pages 223–223
- `fr` investors_guide_territorial_opportunities_fr_chunk_0127: 4466 chars, pages 246–246
- `fr` investors_guide_territorial_opportunities_fr_chunk_0141: 3321 chars, pages 260–260
- `en` investors_guide_territorial_opportunities_en_chunk_0001: 12533 chars, pages 1–15
- `en` investors_guide_territorial_opportunities_en_chunk_0002: 6097 chars, pages 16–18
- `en` investors_guide_territorial_opportunities_en_chunk_0003: 5772 chars, pages 19–21
- `en` investors_guide_territorial_opportunities_en_chunk_0004: 7801 chars, pages 22–25
- `en` investors_guide_territorial_opportunities_en_chunk_0005: 8031 chars, pages 26–29
- `en` investors_guide_territorial_opportunities_en_chunk_0006: 5426 chars, pages 30–32
- `en` investors_guide_territorial_opportunities_en_chunk_0007: 6270 chars, pages 33–35
- `en` investors_guide_territorial_opportunities_en_chunk_0008: 8429 chars, pages 36–41
- `en` investors_guide_territorial_opportunities_en_chunk_0009: 15709 chars, pages 42–45
- `en` investors_guide_territorial_opportunities_en_chunk_0010: 5624 chars, pages 46–48
- `en` investors_guide_territorial_opportunities_en_chunk_0011: 7905 chars, pages 49–51
- `en` investors_guide_territorial_opportunities_en_chunk_0012: 5738 chars, pages 52–54
- `en` investors_guide_territorial_opportunities_en_chunk_0013: 7193 chars, pages 55–59
- `en` investors_guide_territorial_opportunities_en_chunk_0014: 10351 chars, pages 60–63
- `en` investors_guide_territorial_opportunities_en_chunk_0015: 10960 chars, pages 64–69
- `en` investors_guide_territorial_opportunities_en_chunk_0016: 9223 chars, pages 70–73
- `en` investors_guide_territorial_opportunities_en_chunk_0017: 13391 chars, pages 74–78
- `en` investors_guide_territorial_opportunities_en_chunk_0021: 7913 chars, pages 90–93
- `en` investors_guide_territorial_opportunities_en_chunk_0023: 6516 chars, pages 102–103
- `en` investors_guide_territorial_opportunities_en_chunk_0024: 8497 chars, pages 104–106
- `en` investors_guide_territorial_opportunities_en_chunk_0026: 8296 chars, pages 110–113
- `en` investors_guide_territorial_opportunities_en_chunk_0036: 13614 chars, pages 154–157
- `en` investors_guide_territorial_opportunities_en_chunk_0037: 7754 chars, pages 158–160
- `en` investors_guide_territorial_opportunities_en_chunk_0038: 10227 chars, pages 161–163
- `en` investors_guide_territorial_opportunities_en_chunk_0039: 8257 chars, pages 164–167
- `en` investors_guide_territorial_opportunities_en_chunk_0018: 5412 chars, pages 79–81
- `en` investors_guide_territorial_opportunities_en_chunk_0034: 11631 chars, pages 144–147
- `en` investors_guide_territorial_opportunities_en_chunk_0019: 5007 chars, pages 84–85
- `en` investors_guide_territorial_opportunities_en_chunk_0020: 7157 chars, pages 86–89
- `en` investors_guide_territorial_opportunities_en_chunk_0022: 9992 chars, pages 94–99
- `en` investors_guide_territorial_opportunities_en_chunk_0025: 8377 chars, pages 107–109
- `en` investors_guide_territorial_opportunities_en_chunk_0027: 5595 chars, pages 114–116
- `en` investors_guide_territorial_opportunities_en_chunk_0028: 8657 chars, pages 117–120
- `en` investors_guide_territorial_opportunities_en_chunk_0029: 10950 chars, pages 121–126
- `en` investors_guide_territorial_opportunities_en_chunk_0030: 10877 chars, pages 127–129
- `en` investors_guide_territorial_opportunities_en_chunk_0031: 9731 chars, pages 130–132
- `en` investors_guide_territorial_opportunities_en_chunk_0032: 13127 chars, pages 133–138
- `en` investors_guide_territorial_opportunities_en_chunk_0033: 12163 chars, pages 139–141
- `en` investors_guide_territorial_opportunities_en_chunk_0035: 9444 chars, pages 148–151
- `en` investors_guide_territorial_opportunities_en_chunk_0040: 5710 chars, pages 170–171
- `en` investors_guide_territorial_opportunities_en_chunk_0041: 9390 chars, pages 172–174
- `en` investors_guide_territorial_opportunities_en_chunk_0042: 7932 chars, pages 175–177
- `en` investors_guide_territorial_opportunities_en_chunk_0043: 6023 chars, pages 178–180
- `en` investors_guide_territorial_opportunities_en_chunk_0044: 6837 chars, pages 181–182
- `en` investors_guide_territorial_opportunities_en_chunk_0045: 7106 chars, pages 183–184
- `en` investors_guide_territorial_opportunities_en_chunk_0046: 9537 chars, pages 185–188
- `en` investors_guide_territorial_opportunities_en_chunk_0047: 8881 chars, pages 189–192
- `en` investors_guide_territorial_opportunities_en_chunk_0048: 11141 chars, pages 193–196
- `en` investors_guide_territorial_opportunities_en_chunk_0049: 9023 chars, pages 197–200
- `en` investors_guide_territorial_opportunities_en_chunk_0050: 11072 chars, pages 201–204
- `en` investors_guide_territorial_opportunities_en_chunk_0051: 7834 chars, pages 205–208

## Repeated boilerplate

Repeated sector labels, investment-advantage headings, support-program references and tourism/agri-food market-statistics blocks remain in their original source spans. They were not removed; they should be considered later for retrieval weighting or deduplication.

## Temporal metadata

Publication year is `null` for both documents because the guide edition year was not safely established from an explicit publication marker. Explicit years found in each chunk are retained in `temporal_scope.years_mentioned`; no edition year was inherited.

## OCR and identity confidence

Some source pages contain OCR noise, especially cover/table-of-contents pages and a small number of English headings. Project identities are directly supported by explicit titles on profile pages or by title plus continuation evidence. The following should receive later manual review: English pages 25–29 (fig/red-fruit transition), French pages 112–121 (naval/seafood transition), and service-directory pages after the opportunity catalogue.

## Validation

Phase-specific exact provenance validation: PASS for FR and EN. Every emitted source span is a non-empty exact substring of its raw page; chunk text is the ordered span concatenation; page bounds match span extrema.

Canonical validator: run separately with `scripts/validate_semantic_json.py --source-dir data/raw/json`.

## Raw SHA-256 integrity

| File | Before | After | Unchanged |
|---|---|---|---|
| `Investors_Guide_territorial_opportunities_FR.json` | `518A5307E090C60F99E3A56F8129E8B9205B99B2A0A457CDE9FBA8295F02B462` | `518A5307E090C60F99E3A56F8129E8B9205B99B2A0A457CDE9FBA8295F02B462` | yes |
| `Investors_Guide_territorial_opportunities_EN.json` | `0962FD8F0B18071629C8AF7C672BA970160FDCBC0B3409279D2EC87738245D6E` | `0962FD8F0B18071629C8AF7C672BA970160FDCBC0B3409279D2EC87738245D6E` | yes |

## Manual review items

- Verify the few profile transitions identified above against rendered PDF pages before using these semantic chunks for ingestion.
- Review OCR-degraded English titles and the service-directory page-level units; no source text was corrected or invented.
