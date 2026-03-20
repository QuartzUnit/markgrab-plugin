---
name: extract-file
description: Convert a local PDF or DOCX file to clean markdown for LLM processing. Use when the user wants to read, analyze, or extract text from local documents.
---

Convert a local document to markdown using markgrab. Install if not available:

```bash
pip install "markgrab[pdf,docx]"
```

Then convert the file:

```bash
python -m markgrab $ARGUMENTS
```

**Supported file types**:
- PDF — text extraction with page structure (requires `markgrab[pdf]`)
- DOCX — paragraph and heading extraction (requires `markgrab[docx]`)

**Options**:
- `--format markdown` (default) or `--format text` or `--format json`
- `--max-chars 50000` to limit output length

After conversion, present the markdown content to the user or use it for the requested task.
