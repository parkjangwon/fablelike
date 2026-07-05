# fableLike

`fableLike` is a portable prompt/skill profile for making different AI agents behave more like a high-agency, Fable-style assistant.

It is based on observed Claude Fable-style system-prompt patterns, but it does not copy leaked prompt text verbatim and does not claim to reproduce the original model's hidden capabilities.

## Goal

Use `SKILL.md` to steer models toward:

- warm, concise prose
- minimal but useful formatting
- direct answers before caveats
- careful memory and preference handling
- current-information verification
- tool-aware task execution
- long-horizon agentic discipline
- short, principled refusals
- copyright-aware sourcing
- non-sycophantic evenhandedness

This improves behavioral similarity only. It cannot transfer the original model's weights, private tools, internal classifiers, or actual reasoning capability.

## Install

Install with the Skills CLI:

```bash
npx skills add parkjangwon/fablelike
```

Install globally:

```bash
npx skills add parkjangwon/fablelike --global
```

Install to all supported agents without prompts:

```bash
npx skills add parkjangwon/fablelike --all
```

Preview/use the skill without installing:

```bash
npx skills use parkjangwon/fablelike@fablelike
```

## Manual Usage

Copy the contents of `SKILL.md` into the strongest instruction layer your agent supports.

For Claude, place the contents in `CLAUDE.md`, project instructions, or a custom command/prompt wrapper.

For OpenAI, DeepSeek, Gemini, Qwen, local models, or custom API agents, place the contents in the system or developer prompt before the user request.

## Recommended Prompt Wrapper

```text
Use the fableLike profile below as the operating style for this conversation.

[paste SKILL.md here]
```

## Files

- `SKILL.md` - the portable behavior profile
- `README.md` - usage notes

## Notes

This repository intentionally keeps only the portable prompt profile and documentation. Product-specific metadata files are omitted so the repo stays model-agnostic.
