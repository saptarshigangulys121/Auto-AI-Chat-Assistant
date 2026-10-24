# Auto AI Chat Assistant

A small terminal chatbot that generates replies with Google's Gemini API.

## Requirements

- Python 3.10 or newer
- A Gemini API key

The program uses Python's standard library; no package installation is needed.

## Run

In PowerShell, set your API key for the current terminal session and start the chatbot:

```powershell
$env:GEMINI_API_KEY = "your-api-key"
py main.py
```

Type `exit` or `quit` to end the session. The conversation is not saved between runs.

## Configuration

Optional environment variables:

| Variable | Default | Purpose |
| --- | --- | --- |
| `GEMINI_API_URL` | `https://generativelanguage.googleapis.com/v1beta` | Gemini API base URL |
| `GEMINI_API_KEY` | Not set | API key used to authenticate requests |
| `GEMINI_MODEL` | `gemini-3.5-flash-lite` | Gemini model identifier |
| `GEMINI_SYSTEM_PROMPT` | Helpful, concise assistant prompt | Instructions for the assistant |
| `GEMINI_TIMEOUT` | `30` seconds | Request timeout (clamped to 1-120 seconds) |
| `GEMINI_MAX_TOKENS` | `500` | Maximum generated output tokens (clamped to 1-4,000) |

Keep API keys private. Set them in your environment rather than saving them in source files or committing them to Git.

## Current scope

This is a terminal chatbot, not an integration with a messaging app. It sends each message to Gemini independently and does not retain conversation history. API usage is subject to Google's current quotas and pricing.
