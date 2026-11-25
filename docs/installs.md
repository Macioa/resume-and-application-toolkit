# Installs

From `tasks/`.

## MCPs
- EasyPlaywrightMCP — https://github.com/Macioa/EasyPlaywrightMCP
- Supabase MCP
- Composio MCP
  - Gmail
  - Google Calendar

## CLI / local
- `gh` (GitHub CLI)
- `git`
- Node.js
- Playwright (`@playwright/test`)
- ffmpeg / ffprobe — `winget install Gyan.FFmpeg`
- `edge-tts` — `python -m pip install edge-tts`
- `python-docx` — `python -m pip install python-docx` (scripts/docx_to_md.py)
- `curl`
- `pydantic`, `requests`, `pg8000` — `python -m pip install pydantic requests pg8000` (scripts/resume_select, scripts/resume_view.py)
- `reportlab` — `python -m pip install reportlab` (resume and cover letter templates)
- Claude CLI (`claude`, logged in) — fallback runner for scripts/resume_select when the Gemini flash runner fails (`--runner claude`)
