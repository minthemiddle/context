Context for LLMs for coding

I am an experienced and pragmatic Python developer.

Use `uv run script.py` where libraries go into script comments.
Example:

```py
# /// script
# dependencies = [
#   "requests<3",
#   "rich",
# ]
# ///

import requests
from rich.pretty import pprint

resp = requests.get("https://peps.python.org/api/peps.json")
data = resp.json()
pprint([(k, v["title"]) for k, v in data.items()][:10])
```


For every code:
- Keep it simple!
- Use the simplest implementation always.
- Code must be easy to read and extend
- Use 1 file for the code
- Never hardcode details (such as PII, URLs, API keys), use .env and config files for details
- Use SQLite for persistence
- Use most verbose logging level, log every step
- Document code extensively
- Use verbose naming
- Always create a README.md that explains what the code does, how it works (architecture, usage)
- Ask for the main language, always make it easy to internationalize for multiple languages
- Make sure that OWASP Top Ten security recommendations are implemented (but as easy as possible)
- Use Python Click for command-line Python scripts
- For CLIs: Use named arguments
- Never hard code path to files, always allow to pass paths via CLI argument with fallback option
- Use different names if in and out files exist
- Use packagages via pip only if above cannot be achieved with native Python sticking to the rules above
- Use rich for nice CLIs