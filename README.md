# Boot.dev AI Agent

This project follows Boot.dev's course on building an AI agent in Python. It
uses the OpenAI Python SDK with OpenRouter's API and the `openrouter/free`
model router.

## Progress

Last updated: 2026-09-18

Completed through Chapter 1, Lesson 6:

- OpenRouter client configuration and API-key validation
- Chat completion requests using `openrouter/free`
- Prompt and completion token metadata
- Required command-line prompts with `argparse`
- A standalone conversation `messages` list

Next lesson: L7, Verbose Output.

## Current Behavior

`main.py` accepts one required prompt, sends it to OpenRouter, and prints the
prompt token count, response token count, and model response. Running it
without a prompt intentionally exits with code 2 and shows `argparse` usage.

```bash
uv run main.py "Explain Python functions in one paragraph."
```

## Setup

Dependencies are managed with `uv` and declared in `pyproject.toml`.

Create a `.env` file in the project root containing the actual OpenRouter
secret key:

```env
OPENROUTER_API_KEY='your_actual_key_here'
```

The `.env` file is ignored by Git and must never be committed or shared.

## Session Workflow

For each Boot.dev lesson:

1. Read the active lesson requirements and inspect the current project first.
2. Implement only the requested lesson changes while preserving prior work.
3. Validate offline with a mocked OpenAI client when practical.
4. Explain the changes so they can be reviewed and understood.
5. Do not run `bootdev run -s`; the user reviews and submits the lesson.
