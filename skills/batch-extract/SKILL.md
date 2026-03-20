---
name: batch-extract
description: Extract content from multiple URLs at once. Use when the user has a list of URLs to process in bulk for RAG preparation, research, or archiving.
---

Extract content from multiple URLs using markgrab's Python API. Install if not available:

```bash
pip install markgrab
```

For batch extraction, use the Python API:

```python
import asyncio
from markgrab import extract

async def batch_extract(urls: list[str]) -> list:
    results = []
    for url in urls:
        try:
            result = await extract(url, max_chars=30_000)
            results.append({"url": url, "title": result.title, "markdown": result.markdown, "word_count": result.word_count})
        except Exception as e:
            results.append({"url": url, "error": str(e)})
    return results

urls = $ARGUMENTS  # list of URLs
results = asyncio.run(batch_extract(urls))
```

Report the results: how many succeeded, how many failed, total word count extracted.
