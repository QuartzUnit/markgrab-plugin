---
name: extract-url
description: Extract content from a web URL and convert to clean LLM-ready markdown. Use when the user wants to read, summarize, or process web page content, YouTube transcripts, or online documents.
---

Extract web content using the markgrab library. Install if not available:

```bash
pip install markgrab
```

Then extract the content:

```bash
python -m markgrab $ARGUMENTS
```

The output is clean, LLM-ready markdown with noise removed (nav, sidebar, ads, scripts).

**Supported URL types** (auto-detected):
- HTML pages — content density filtering, auto-fallback to Playwright for JS-heavy sites
- YouTube — transcript extraction with timestamps
- PDF — text extraction with page structure
- DOCX — paragraph and heading extraction

**Options**:
- `--format markdown` (default) or `--format text` or `--format json`
- `--browser` to force Playwright rendering for JS-heavy pages
- `--max-chars 30000` to limit output length
- `--stealth` for anti-bot stealth scripts (opt-in)

After extraction, present the markdown content to the user or use it for the requested task (summarization, analysis, etc.).
