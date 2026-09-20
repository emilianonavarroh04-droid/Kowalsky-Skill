# OmniRoute Skills for Kowalsky

This repository contains OmniRoute Agent Skills integrated for the Kowalsky project. OmniRoute provides unified access to multiple LLM providers through a consistent API and CLI interface.

## What are OmniRoute Skills?

OmniRoute Agent Skills are drop-in guides that let AI agents (Claude Desktop, ChatGPT, Cursor, Cline, Continue, etc.) consume OmniRoute capabilities via OpenAI-compatible REST or CLI commands.

## Included Skills

### API Skills (23)

Entry points for REST API access:
- **Authentication** (`omni-auth`) - Start here for API access with Bearer tokens and session management
- **Providers** (`omni-providers`) - Manage provider connections and API keys
- **Models** (`omni-models`) - Query available AI models across providers
- **Inference** (`omni-inference`) - Core OpenAI-compatible endpoints

...and 19 more API skills covering routing, budgets, caching, compression, and more.

### CLI Skills (21)

Entry points for command-line access:
- **Serve** (`cli-serve`) - Start and manage the OmniRoute server
- **Health** (`cli-health`) - Monitor server health and component status
- **Chat** (`cli-chat`) - Interactive chat and REPL sessions
- **Models** (`cli-models`) - List and query available models

...and 17 more CLI skills covering routing, resilience, compression, and more.

## Quick Start

### Using API Skills

1. Start with the Authentication skill (`skills/omni-auth/SKILL.md`)
2. Configure your OmniRoute instance and get an API key
3. Use any API skill to interact with OmniRoute endpoints

### Using CLI Skills

1. Start with the Serve skill (`skills/cli-serve/SKILL.md`)
2. Start the OmniRoute server
3. Use CLI skills to interact with the running server

## Manifest URLs

All OmniRoute skill manifests are public and can be referenced directly:

```
https://raw.githubusercontent.com/diegosouzapw/OmniRoute/main/skills/<id>/SKILL.md
```

Example:
```
https://raw.githubusercontent.com/diegosouzapw/OmniRoute/main/skills/omni-auth/SKILL.md
```

## Documentation

For the full OmniRoute documentation, visit: https://github.com/diegosouzapw/OmniRoute

For agent skills framework reference, see the `docs/frameworks/AGENT-SKILLS.md` file in the main OmniRoute repository.
