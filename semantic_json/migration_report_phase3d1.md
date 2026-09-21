# Phase 3D.1 — Targeted final cleanup

## Scope

Only the two investors-guide semantic documents were changed. The 50 opportunity catalogue was retained; raw JSON and production RAG files were not modified.

## Chunk counts

- FR: 136 chunks (previous phase 3D: 166); introduction: 6 chunks; support-directory units: 54; opportunities: 50
- EN: 68 chunks (previous phase 3D: 76); introduction: 6 chunks; support-directory units: 1; opportunities: 50

## Introduction refinement

The former duplicated 1–15 block was replaced with six source-supported units per language: cover/title, director message, table of contents, Manar Al Moustatmir, territorial methodology, and the first sector overview. Empty page 3 is omitted. No source text was rewritten.

## Transition verification

| Language | Area | Assignment | Result | Evidence |
|---|---|---|---|---|
| EN | pages 25–29 | fig processing 22–25; red-fruit processing 26–29 | confirmed | page 25 closes the fig profile; page 26 begins the red-fruit title/description |
| FR | pages 112–121 | naval shipyard 111–112; fish canning 115–117; seafood waste 118–121 | confirmed | pages 113–114 are fisheries overview; explicit profile titles begin at 115 and 118 |

No partial-page boundary was required: affected project starts and endings are identifiable at page boundaries. Opportunity count remains 50 in both editions.

## Support-directory refinement

The French directory was regrouped around named organizations/programmes and continuation pages, rather than assigning every page the contact-information type. Service, financing, entrepreneurship, eligibility, table, and contact-information types are now used according to the unit’s primary content. The English edition has only a final contact page after its opportunity catalogue.

## Metadata topics consistency

For both documents, `metadata.topics` is the exact sorted union of all chunk `semantic_tags`. It includes `investment_opportunity`, canonical opportunity IDs, sector/territory tags, and support/contact tags; no unused stale topic is retained.

## Chunk-size diagnostics

- Total chunks: 204
- Minimum: 21 characters
- Median: 4773.0
- Average: 5139.5
- Maximum: 16579
- >3000: 117
- >5000: 101
- >8000: 63
- >12000: 11

### Recommended for retrieval subchunking (report-only)

- FR `investors_guide_territorial_opportunities_fr_phase3d1_chunk_0002`: 6620 chars, pages 5–5
- FR `investors_guide_territorial_opportunities_fr_phase3d1_chunk_0003`: 9500 chars, pages 6–9
- FR `investors_guide_territorial_opportunities_fr_phase3d1_chunk_0005`: 6089 chars, pages 13–14
- FR `investors_guide_territorial_opportunities_fr_chunk_0002`: 7637 chars, pages 17–19
- FR `investors_guide_territorial_opportunities_fr_chunk_0003`: 5814 chars, pages 20–22
- FR `investors_guide_territorial_opportunities_fr_chunk_0004`: 11989 chars, pages 23–27
- FR `investors_guide_territorial_opportunities_fr_chunk_0005`: 8223 chars, pages 28–30
- FR `investors_guide_territorial_opportunities_fr_chunk_0006`: 8952 chars, pages 31–34
- FR `investors_guide_territorial_opportunities_fr_chunk_0007`: 5008 chars, pages 35–36
- FR `investors_guide_territorial_opportunities_fr_chunk_0008`: 9154 chars, pages 37–40
- FR `investors_guide_territorial_opportunities_fr_chunk_0009`: 16579 chars, pages 43–48
- FR `investors_guide_territorial_opportunities_fr_chunk_0011`: 7881 chars, pages 50–52
- FR `investors_guide_territorial_opportunities_fr_chunk_0012`: 6058 chars, pages 53–55
- FR `investors_guide_territorial_opportunities_fr_chunk_0013`: 7417 chars, pages 56–58
- FR `investors_guide_territorial_opportunities_fr_chunk_0014`: 10856 chars, pages 61–64
- FR `investors_guide_territorial_opportunities_fr_chunk_0015`: 11197 chars, pages 67–70
- FR `investors_guide_territorial_opportunities_fr_chunk_0016`: 13186 chars, pages 71–74
- FR `investors_guide_territorial_opportunities_fr_chunk_0017`: 9589 chars, pages 75–77
- FR `investors_guide_territorial_opportunities_fr_chunk_0018`: 5817 chars, pages 80–82
- FR `investors_guide_territorial_opportunities_fr_chunk_0019`: 5483 chars, pages 85–86
- FR `investors_guide_territorial_opportunities_fr_chunk_0021`: 8128 chars, pages 91–94
- FR `investors_guide_territorial_opportunities_fr_chunk_0022`: 11168 chars, pages 97–100
- FR `investors_guide_territorial_opportunities_fr_chunk_0023`: 10307 chars, pages 103–105
- FR `investors_guide_territorial_opportunities_fr_chunk_0025`: 9480 chars, pages 108–110
- FR `investors_guide_territorial_opportunities_fr_chunk_0027`: 5622 chars, pages 115–117
- FR `investors_guide_territorial_opportunities_fr_chunk_0028`: 12395 chars, pages 118–121
- FR `investors_guide_territorial_opportunities_fr_chunk_0029`: 10737 chars, pages 122–126
- FR `investors_guide_territorial_opportunities_fr_chunk_0030`: 6891 chars, pages 128–129
- FR `investors_guide_territorial_opportunities_fr_chunk_0031`: 9033 chars, pages 130–132
- FR `investors_guide_territorial_opportunities_fr_chunk_0032`: 12423 chars, pages 133–138
- FR `investors_guide_territorial_opportunities_fr_chunk_0033`: 9729 chars, pages 140–142
- FR `investors_guide_territorial_opportunities_fr_chunk_0034`: 10286 chars, pages 145–147
- FR `investors_guide_territorial_opportunities_fr_chunk_0035`: 12451 chars, pages 148–153
- FR `investors_guide_territorial_opportunities_fr_chunk_0036`: 15181 chars, pages 155–158
- FR `investors_guide_territorial_opportunities_fr_chunk_0037`: 6809 chars, pages 159–161
- FR `investors_guide_territorial_opportunities_fr_chunk_0038`: 9234 chars, pages 162–164
- FR `investors_guide_territorial_opportunities_fr_chunk_0039`: 9027 chars, pages 165–168
- FR `investors_guide_territorial_opportunities_fr_chunk_0040`: 6389 chars, pages 171–172
- FR `investors_guide_territorial_opportunities_fr_chunk_0041`: 8577 chars, pages 173–175
- FR `investors_guide_territorial_opportunities_fr_chunk_0042`: 6126 chars, pages 176–178
- FR `investors_guide_territorial_opportunities_fr_chunk_0043`: 8831 chars, pages 179–181
- FR `investors_guide_territorial_opportunities_fr_chunk_0045`: 8054 chars, pages 184–185
- FR `investors_guide_territorial_opportunities_fr_chunk_0046`: 10718 chars, pages 186–189
- FR `investors_guide_territorial_opportunities_fr_chunk_0047`: 9697 chars, pages 190–193
- FR `investors_guide_territorial_opportunities_fr_chunk_0048`: 9732 chars, pages 194–197
- FR `investors_guide_territorial_opportunities_fr_chunk_0049`: 9991 chars, pages 198–201
- FR `investors_guide_territorial_opportunities_fr_chunk_0050`: 9580 chars, pages 202–205
- FR `investors_guide_territorial_opportunities_fr_chunk_0051`: 8261 chars, pages 206–210
- FR `investors_guide_territorial_opportunities_fr_phase3d1_chunk_1003`: 8714 chars, pages 213–215
- FR `investors_guide_territorial_opportunities_fr_phase3d1_chunk_1028`: 6181 chars, pages 246–247
- FR `investors_guide_territorial_opportunities_fr_phase3d1_chunk_1054`: 8907 chars, pages 280–285
- EN `investors_guide_territorial_opportunities_en_chunk_0002`: 6097 chars, pages 16–18
- EN `investors_guide_territorial_opportunities_en_chunk_0003`: 5772 chars, pages 19–21
- EN `investors_guide_territorial_opportunities_en_chunk_0004`: 7801 chars, pages 22–25
- EN `investors_guide_territorial_opportunities_en_chunk_0005`: 8031 chars, pages 26–29
- EN `investors_guide_territorial_opportunities_en_chunk_0006`: 5426 chars, pages 30–32
- EN `investors_guide_territorial_opportunities_en_chunk_0007`: 6270 chars, pages 33–35
- EN `investors_guide_territorial_opportunities_en_chunk_0008`: 8429 chars, pages 36–41
- EN `investors_guide_territorial_opportunities_en_chunk_0009`: 15709 chars, pages 42–45
- EN `investors_guide_territorial_opportunities_en_chunk_0010`: 5624 chars, pages 46–48
- EN `investors_guide_territorial_opportunities_en_chunk_0011`: 7905 chars, pages 49–51
- EN `investors_guide_territorial_opportunities_en_chunk_0012`: 5738 chars, pages 52–54
- EN `investors_guide_territorial_opportunities_en_chunk_0013`: 7193 chars, pages 55–59
- EN `investors_guide_territorial_opportunities_en_chunk_0014`: 10351 chars, pages 60–63
- EN `investors_guide_territorial_opportunities_en_chunk_0015`: 10960 chars, pages 64–69
- EN `investors_guide_territorial_opportunities_en_chunk_0016`: 9223 chars, pages 70–73
- EN `investors_guide_territorial_opportunities_en_chunk_0017`: 13391 chars, pages 74–78
- EN `investors_guide_territorial_opportunities_en_chunk_0018`: 5412 chars, pages 79–81
- EN `investors_guide_territorial_opportunities_en_chunk_0019`: 5007 chars, pages 84–85
- EN `investors_guide_territorial_opportunities_en_chunk_0020`: 7157 chars, pages 86–89
- EN `investors_guide_territorial_opportunities_en_chunk_0021`: 7913 chars, pages 90–93
- EN `investors_guide_territorial_opportunities_en_chunk_0022`: 9992 chars, pages 94–99
- EN `investors_guide_territorial_opportunities_en_chunk_0023`: 6516 chars, pages 102–103
- EN `investors_guide_territorial_opportunities_en_chunk_0024`: 8497 chars, pages 104–106
- EN `investors_guide_territorial_opportunities_en_chunk_0025`: 8377 chars, pages 107–109
- EN `investors_guide_territorial_opportunities_en_chunk_0026`: 8296 chars, pages 110–113
- EN `investors_guide_territorial_opportunities_en_chunk_0027`: 5595 chars, pages 114–116
- EN `investors_guide_territorial_opportunities_en_chunk_0028`: 8657 chars, pages 117–120
- EN `investors_guide_territorial_opportunities_en_chunk_0029`: 10950 chars, pages 121–126
- EN `investors_guide_territorial_opportunities_en_chunk_0030`: 10877 chars, pages 127–129
- EN `investors_guide_territorial_opportunities_en_chunk_0031`: 9731 chars, pages 130–132
- EN `investors_guide_territorial_opportunities_en_chunk_0032`: 13127 chars, pages 133–138
- EN `investors_guide_territorial_opportunities_en_chunk_0033`: 12163 chars, pages 139–141
- EN `investors_guide_territorial_opportunities_en_chunk_0034`: 11631 chars, pages 144–147
- EN `investors_guide_territorial_opportunities_en_chunk_0035`: 9444 chars, pages 148–151
- EN `investors_guide_territorial_opportunities_en_chunk_0036`: 13614 chars, pages 154–157
- EN `investors_guide_territorial_opportunities_en_chunk_0037`: 7754 chars, pages 158–160
- EN `investors_guide_territorial_opportunities_en_chunk_0038`: 10227 chars, pages 161–163
- EN `investors_guide_territorial_opportunities_en_chunk_0039`: 8257 chars, pages 164–167
- EN `investors_guide_territorial_opportunities_en_chunk_0040`: 5710 chars, pages 170–171
- EN `investors_guide_territorial_opportunities_en_chunk_0041`: 9390 chars, pages 172–174
- EN `investors_guide_territorial_opportunities_en_chunk_0042`: 7932 chars, pages 175–177
- EN `investors_guide_territorial_opportunities_en_chunk_0043`: 6023 chars, pages 178–180
- EN `investors_guide_territorial_opportunities_en_chunk_0044`: 6837 chars, pages 181–182
- EN `investors_guide_territorial_opportunities_en_chunk_0045`: 7106 chars, pages 183–184
- EN `investors_guide_territorial_opportunities_en_chunk_0046`: 9537 chars, pages 185–188
- EN `investors_guide_territorial_opportunities_en_chunk_0047`: 8881 chars, pages 189–192
- EN `investors_guide_territorial_opportunities_en_chunk_0048`: 11141 chars, pages 193–196
- EN `investors_guide_territorial_opportunities_en_chunk_0049`: 9023 chars, pages 197–200
- EN `investors_guide_territorial_opportunities_en_chunk_0050`: 11072 chars, pages 201–204
- EN `investors_guide_territorial_opportunities_en_chunk_0051`: 7834 chars, pages 205–208

## Boilerplate findings

Repeated sector headings, investment-advantage sections, IDMAJ/TAEHIL references, market-statistics blocks, SWOT labels, and footer/contact strings recur across project sheets. They remain preserved in source spans. Future retrieval preprocessing should avoid embedding these repeated blocks as independent evidence or downweight them when they carry no project-specific facts.

## Validation

Phase-specific exact provenance validation: PASS for FR and EN. All spans are exact non-empty substrings of raw pages, page bounds match, and chunk text is the ordered span concatenation.

Canonical validator: PASS for both documents using `scripts/validate_semantic_json.py --source-dir data/raw/json`.

## Raw SHA-256 integrity

| File | Before | After | Unchanged |
|---|---|---|---|
| `Investors_Guide_territorial_opportunities_FR.json` | `518A5307E090C60F99E3A56F8129E8B9205B99B2A0A457CDE9FBA8295F02B462` | `518A5307E090C60F99E3A56F8129E8B9205B99B2A0A457CDE9FBA8295F02B462` | yes |
| `Investors_Guide_territorial_opportunities_EN.json` | `0962FD8F0B18071629C8AF7C672BA970160FDCBC0B3409279D2EC87738245D6E` | `0962FD8F0B18071629C8AF7C672BA970160FDCBC0B3409279D2EC87738245D6E` | yes |

## Remaining manual review

- Render-check the English pages 25–29 and French pages 112–121 if visual confirmation is required; textual boundaries are confirmed.
- Review OCR-degraded directory headings and repeated boilerplate during later retrieval design.
