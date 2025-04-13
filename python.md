# Python Scripting Guidelines for LLMs

**Context:** Assume you are assisting an experienced and pragmatic Python developer.

**Dependency Management:**
- Use `uv run script.py` with dependencies declared in script comments.
- Prioritize the Python standard library; use external packages only when necessary.
- Example:
  ```python
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

**Core Principles:**
- **Simplicity:** Always prefer the simplest, most straightforward implementation.
- **Readability & Maintainability:** Write code that is easy to read, understand, and extend. Use verbose and descriptive naming.
- **Structure:** For simple scripts, aim for a single file. Refactor into modules as complexity grows.

**Configuration & Data Handling:**
- **No Hardcoding:** Never hardcode sensitive information (PII, URLs, API keys) or configuration values. Use environment variables (`.env` files) or configuration files.
- **Persistence:** Use SQLite for simple data persistence needs.
- **File Paths:** Do not hardcode file paths. Accept paths via command-line arguments, providing sensible defaults. Use distinct names for input and output files to prevent accidental data loss.

**Logging:**
- Implement comprehensive logging for all significant steps.
- Make logging levels configurable (e.g., via environment variables or CLI arguments).

**Documentation:**
- **Code:** Document code thoroughly using docstrings and comments.
- **README:** Always include a `README.md` explaining the script's purpose, architecture (if applicable), setup, and usage instructions.

**Internationalization (i18n):**
- Design code with internationalization in mind. Ask for the primary language and make text localization straightforward.

**Security:**
- Implement relevant OWASP Top Ten security recommendations pragmatically.

**Command-Line Interfaces (CLIs):**
- Use `click` for building CLIs.
- Prefer named arguments (`--option`) over positional arguments.
- Use `rich` for enhanced terminal output (e.g., tables, colors, progress bars).
