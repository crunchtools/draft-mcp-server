# draft-mcp-server

Claude Code skill for building CrunchTools MCP servers from scratch.

## What It Does

`/draft-mcp-server <service-name>` runs a multi-phase workflow that takes a service name (e.g., `mediawiki`, `jira`) and builds a complete, production-grade MCP server — from API research through deployment and registry publishing.

## Installation

This skill is installed as a symlink from `~/.claude/skills/draft-mcp-server/` to the repo checkout.

```bash
# Clone
git clone https://github.com/crunchtools/draft-mcp-server ~/Projects/crunchtools/draft-mcp-server

# Symlink into Claude Code skills
ln -sf ~/Projects/crunchtools/draft-mcp-server ~/.claude/skills/draft-mcp-server
```

## Usage

```
/draft-mcp-server mediawiki
/draft-mcp-server jira
/draft-mcp-server slack
```

## Phases

1. **Research and Planning** — API research, tool inventory design, plan approval
2. **Project Scaffolding** — directory structure, governance files, CI workflows
3. **Implementation** — core infrastructure, tools, server registration
4. **Tests** — mocked httpx tests, Pydantic validation tests
5. **Quality Gates** — lint, type check, tests, gourmand, container build
6. **Git and GitHub** — init, push, tag
7. **Deploy Locally** — env file, systemd service, Claude Code config
8. **Publish** — PyPI, container registries, MCP Registry, website
9. **Store in Memory** — build details for future reference

## Governance

Servers built by this skill conform to:
- [crunchtools/constitution](https://github.com/crunchtools/constitution) — universal core
- [MCP Server profile](https://github.com/crunchtools/constitution/blob/main/profiles/mcp-server.md) — subsystem requirements

This skill itself follows the [Claude Skill profile](https://github.com/crunchtools/constitution/blob/main/profiles/claude-skill.md).

## License

AGPL-3.0-or-later
