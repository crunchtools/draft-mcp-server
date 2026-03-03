# draft-mcp-server Constitution

> **Version:** 1.0.0
> **Ratified:** 2026-03-03
> **Status:** Active
> **Inherits:** [crunchtools/constitution](https://github.com/crunchtools/constitution) v1.0.0
> **Profile:** Claude Skill

## Overview

The `/draft-mcp-server` skill is a multi-phase workflow for building production-grade CrunchTools MCP servers from scratch. It covers API research, project scaffolding, implementation, testing, deployment, and registry publishing.

## License

AGPL-3.0-or-later

## Versioning

Follow Semantic Versioning 2.0.0. MAJOR/MINOR/PATCH.

## SKILL.md Standards

- YAML frontmatter with `name`, `description`, `argument-hint`, `allowed-tools`
- Organized into numbered Phases with numbered Steps
- Phase gates prevent proceeding without user approval at critical checkpoints
- References MCP Server profile for architecture and quality standards rather than duplicating them

## Memory Integration

- Phase 1 Step 1: Searches memory for prior context about the target service
- Phase 9: Stores build details (server name, version, tool count, architecture decisions, deployment details)

## User Confirmation Gates

- Phase 1 → Phase 2: User must approve the plan (tool inventory, auth flow, file structure)
- Phase 2 → Phase 3: All scaffolding files created
- Phase 4 → Phase 5: All tests pass
- Phase 5 → Phase 6: All five quality gates pass
- Phase 7 → Phase 8: Server responds to test calls

## Relationship to Constitutions

This skill is a *workflow executor* — it defines the sequence of actions to build a new MCP server. The *standards* for what the server must look like come from:
- `crunchtools/constitution` universal core — license, semver, container registry, commit standards
- `profiles/mcp-server.md` — five-layer security, two-layer architecture, testing standards, quality gates, naming conventions, governance framework

The skill deliberately avoids re-specifying constitutional requirements. When the constitution changes, the skill automatically builds to the updated standard without needing its own update.
