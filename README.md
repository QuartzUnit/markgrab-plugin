# MarkGrab Plugin for Claude Code

> [llms.txt](llms.txt)

Universal web content extraction — any URL to LLM-ready markdown.

## Skills

| Skill | Description |
|-------|-------------|
| `extract-url` | Extract content from a web URL (HTML, YouTube, PDF) |
| `extract-file` | Convert local PDF/DOCX to markdown |
| `batch-extract` | Bulk extract from multiple URLs |

## Requirements

```bash
pip install markgrab          # core
pip install "markgrab[all]"   # all content types
```

## Supported Content Types

- **HTML** — content density filtering, auto-fallback to Playwright for JS-heavy sites
- **YouTube** — transcript extraction with timestamps and multi-language support
- **PDF** — text extraction with page structure
- **DOCX** — paragraph and heading extraction

## Links

- [PyPI](https://pypi.org/project/markgrab/)
- [GitHub](https://github.com/QuartzUnit/markgrab)
- [Documentation](https://github.com/QuartzUnit/markgrab#readme)


---

<sub>Part of the [QuartzUnit](https://github.com/QuartzUnit) ecosystem — composable Python libraries for data collection, extraction, search, and AI agent safety.</sub>
