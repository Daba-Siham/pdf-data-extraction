# PDF Data Extraction

This repository contains structured data extracted from PDF documents related to investment, entrepreneurship, territorial opportunities, economic activity zones, and regional development in the Tangier-Tetouan-Al Hoceima region.

The repository keeps the original documents, the V1 extraction layer, and the V2 semantic knowledge layer separate.

## Repository Structure

```text
pdf-data-extraction/
├── original/
│   ├── document_01.pdf
│   ├── document_02.pdf
│   └── ...
│
├── json/
│   ├── document_01.json
│   ├── document_02.json
│   └── ...
│
├── semantic_json/
│   ├── semantic_document_01.json
│   ├── semantic_document_02.json
│   └── ...
│
└── README.md
```

- `original/` contains the source PDF files.
- `json/` contains the V1 page-level extraction JSON files.
- `semantic_json/` contains the V2 semantic JSON files used by the new RAG pipeline.

## JSON V1 — Page-level extraction format

The V1 files in `json/` preserve extracted text page by page and provide direct traceability to the source PDFs. V1 is the extraction/raw representation used by the initial character-based RAG pipeline.

```json
{
  "document_id": "example_document",
  "filename": "example_document.pdf",
  "language": "fr",
  "pages": [
    {
      "page": 1,
      "text": "Text extracted from page 1."
    }
  ]
}
```

## JSON V2 — Semantic format

V2 is a richer semantic representation derived from the extracted document content. It organizes content into sections, subsections, and semantic chunks for retrieval, indexing, and context construction. Values may be null or empty when the source does not provide them.

```json
{
  "schema_version": "2.2",
  "document_id": "...",
  "document_family_id": "...",
  "metadata": {
    "title": "...",
    "filename": "...",
    "language": "...",
    "document_type": "...",
    "publisher": "...",
    "region": "...",
    "publication_year": 2025,
    "reference_period": {
      "year": 2025,
      "type": "...",
      "semester": null,
      "quarter": null,
      "label": "...",
      "start_date": null,
      "end_date": null
    },
    "topics": []
  },
  "sections": [
    {
      "section_id": "...",
      "title": "...",
      "topic_id": "...",
      "subsections": [
        {
          "subsection_id": "...",
          "title": "...",
          "chunks": [
            {
              "chunk_id": "...",
              "content_type": "...",
              "semantic_tags": [],
              "heading_path": [],
              "page_start": 1,
              "page_end": 1,
              "source_spans": [
                {
                  "page": 1,
                  "text": "..."
                }
              ],
              "text": "...",
              "keywords": [],
              "entities": [],
              "temporal_scope": {
                "primary_year": 2025,
                "years_mentioned": [],
                "reference_period": {}
              }
            }
          ]
        }
      ]
    }
  ]
}
```

### Main V2 fields

- `schema_version`: version of the semantic JSON schema.
- `document_id`: identifier for one semantic document.
- `document_family_id`: groups translations or equivalent language versions of the same underlying document when appropriate.
- `metadata`: descriptive and temporal information about the document.
- `title`: document title.
- `language`: primary language of the document.
- `document_type`: kind of source document.
- `publisher`: organization or entity that published the document.
- `region`: geographic scope of the document.
- `publication_year`: year in which the document was published.
- `reference_period`: period discussed by the document, including year, semester, quarter, label, and dates when available.
- `topics`: document-level topics.
- `sections`: high-level semantic organization of the document.
- `section_id`: stable identifier for a section.
- `topic_id`: topic associated with a section.
- `subsections`: subdivisions within a section.
- `chunk_id`: identifier for a retrievable semantic chunk.
- `content_type`: semantic nature of the content, such as `narrative`, `statistics`, `procedure`, `faq`, `financial_product`, `investment_opportunity`, `industrial_zone`, `cost_information`, `contact_information`, `legal_information`, `service`, `eligibility_conditions`, or `table`.
- `semantic_tags`: tags describing the meaning or domain of a chunk.
- `heading_path`: ordered headings leading to the chunk.
- `page_start` and `page_end`: PDF page range covered by the chunk when applicable.
- `source_spans`: exact source page/text fragments supporting the chunk and preserving provenance back to the original document.
- `text`: normalized text used for retrieval and generation.
- `keywords`: important terms associated with the chunk.
- `entities`: people, organizations, places, products, or other identified entities.
- `temporal_scope`: structured time information, including the primary year, mentioned years, and reference period.

## V1 and V2 at a glance

| Aspect | V1 JSON | V2 Semantic JSON |
|---|---|---|
| Purpose | Extraction/raw representation | Semantic knowledge representation |
| Organization | By PDF pages | Sections, subsections, semantic chunks |
| Provenance | Page-level | Exact source spans plus page ranges |
| Metadata | Basic | Rich semantic and temporal metadata |
| Document families | No | Yes |
| Semantic tags | No | Yes |
| Content type | No | Yes |
| Temporal scope | Limited to raw text | Structured |
| RAG usage | Initial pipeline | V2 retrieval pipeline |

V1 is not obsolete. It remains the immutable extraction/raw layer. V2 is derived from V1 and serves as the semantic knowledge layer; it does not replace or delete the raw JSON layer.

## Current dataset

- V1 JSON files are stored in `json/`.
- V2 semantic JSON files are stored in `semantic_json/`.
- The current `semantic_json/` folder contains **33 semantic JSON files**.

The count refers to JSON files currently present in the repository and does not imply a document count; files may include translated, intermediate, or generated variants.

## Languages

The dataset contains documents mainly in French, English, Spanish, and Arabic. UTF-8 encoding is used to preserve multilingual text correctly.

## Data Preparation

The original PDFs were processed page by page. Processing may include extraction of existing PDF text, recovery of text from image-based pages, multilingual handling, and preservation of important values from tables, charts, and infographics when available. The original PDFs remain available for comparison with the structured layers.

## Purpose of Semantic JSON

The semantic layer is intended to support:

- semantic retrieval;
- multilingual RAG;
- document-family-aware retrieval;
- temporal filtering and ranking;
- structured indexing;
- exact provenance;
- better context construction;
- future integration of additional sources such as FAQ data.

## Future FAQ integration

The historical FAQ knowledge base can later be converted into the same semantic representation:

```text
FAQ source/export
    → conversion adapter
    → semantic JSON
    → content_type = "faq"
    → same retrieval/indexing pipeline
```

FAQ records without a PDF source should preserve their real source identity and must not receive fabricated PDF page numbers.

## Usage

Clone the repository:

```bash
git clone https://github.com/Daba-Siham/pdf-data-extraction.git
cd pdf-data-extraction
```

### V1 example

```python
import json

with open("json/example_document.json", "r", encoding="utf-8") as f:
    document = json.load(f)

for page in document["pages"]:
    print(page["page"])
    print(page["text"])
```

### V2 example

```python
import json

with open("semantic_json/example_document.json", "r", encoding="utf-8") as f:
    document = json.load(f)

print(document["document_id"])
print(document["document_family_id"])

for section in document["sections"]:
    for subsection in section["subsections"]:
        for chunk in subsection["chunks"]:
            print(chunk["content_type"])
            print(chunk["text"])
```

## Source Traceability

V1 traceability is provided through the source PDF `filename` and each page number. V2 traceability is provided through `document_id`, `document_family_id`, `page_start`/`page_end`, `source_spans`, and semantic chunk identity. A semantic chunk may cover part of a page or multiple pages; it does not necessarily correspond to a full PDF page.

## Notes

Some PDFs contain scanned pages, complex layouts, charts, tables, or embedded text with encoding issues. The JSON representations focus on useful textual and semantic information rather than reproducing the visual layout of the source PDFs.

## License

The repository contains source documents and structured representations of those documents. Usage rights may depend on the rights associated with each original source document.
