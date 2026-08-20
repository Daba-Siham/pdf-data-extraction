# PDF Data Extraction

This repository contains a structured dataset created from a collection of PDF documents related to investment, entrepreneurship, territorial opportunities, economic activity zones, and regional development in the Tangier-Tetouan-Al Hoceima region.

The objective of the project is to preserve the useful textual information contained in the original PDF documents in a simple and reusable JSON format.

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
└── README.md
```

### `original/`

Contains the original PDF documents used as source files.

### `json/`

Contains the structured JSON versions of the PDF documents.

Each JSON file corresponds to one source PDF and preserves the textual content page by page.

## JSON Format

The JSON files follow a lightweight structure:

```json
{
  "document_id": "example_document",
  "filename": "example_document.pdf",
  "language": "fr",
  "pages": [
    {
      "page": 1,
      "text": "Text extracted from page 1."
    },
    {
      "page": 2,
      "text": "Text extracted from page 2."
    }
  ]
}
```

### Fields

- `document_id`: unique identifier for the document.
- `filename`: name of the corresponding source PDF.
- `language`: main language of the document.
- `pages`: list of pages contained in the PDF.
- `page`: original PDF page number.
- `text`: textual content associated with the page.

## Languages

The dataset contains documents in several languages, mainly:

- French
- English
- Spanish
- Arabic

UTF-8 encoding is used to preserve multilingual text correctly.

## Data Preparation

The documents were processed page by page in order to preserve as much meaningful textual information as possible.

The preparation process includes:

- extraction of existing PDF text;
- recovery of text contained in image-based pages when necessary;
- handling of multilingual documents;
- preservation of numerical values and important textual information from tables, charts, and infographics when available;
- removal of unnecessary technical metadata from the final JSON files;
- normalization of the final output into a common JSON structure.

The original PDF files are kept in the repository so that the structured JSON content can always be compared with its source document.

## Purpose

This dataset can be used for tasks such as:

- document analysis;
- information retrieval;
- full-text search;
- data exploration;
- document indexing;
- NLP preprocessing;
- knowledge-base construction;
- retrieval-augmented applications.

## Notes

Some source PDFs contain scanned pages, complex layouts, charts, tables, or embedded text with encoding issues. For these documents, additional text recovery and validation were required.

The JSON representation focuses on preserving useful textual information rather than reproducing the visual layout of the original PDF.

## Usage

Clone the repository:

```bash
git clone https://github.com/Daba-Siham/pdf-data-extraction.git
cd pdf-data-extraction
```

Example in Python:

```python
import json

with open("json/example_document.json", "r", encoding="utf-8") as f:
    document = json.load(f)

for page in document["pages"]:
    print(page["page"])
    print(page["text"])
```

## Source Traceability

Each JSON file keeps the original PDF filename in the `filename` field, making it possible to trace structured content back to its source document.

## License

The repository contains source documents and structured representations of those documents. Usage rights may depend on the rights associated with each original source document.
