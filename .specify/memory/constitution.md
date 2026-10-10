# draft-mcp-server Constitution

> **Version:** 1.1.0
> **Ratified:** 2026-03-03
> **Amended:** 2026-10-02
> **Status:** Active
> **Inherits:** [crunchtools/constitution](https://github.com/crunchtools/constitution) v1.22.0
> **Profile:** Claude Skill

The `/draft-mcp-server` skill builds a production-grade CrunchTools MCP
server from scratch: API research, scaffolding, implementation, tests,
quality gates, GitHub, publishing, and a memory record of the build.

This file holds what is specific to this skill. The fleet rules and the
Claude Skill profile (frontmatter, phased workflow, gates, memory
integration) apply at the inherited version and are checked against this
repo's files by `constitution.yml`. They are not restated here.

## Workflow Executor, Not Standard

The skill defines the sequence of actions to build a server. What the server
must look like comes from the constitution and its MCP Server profile, which
the skill references instead of re-specifying. When those change, the skill
builds to the new standard without an update of its own.

## Phase Gates

- Phase 1 to Phase 2: the user approves the plan (tool inventory, auth flow,
  file structure).
- Phase 2 to Phase 3: all scaffolding files exist.
- Phase 4 to Phase 5: all tests pass.
- Phase 5 to Phase 6: the MCP Server profile's quality gates pass.
- Phase 7 to Phase 8: the server answers test calls.

## Memory Records

Phase 1 Step 1 searches memory for prior context on the target service;
Phase 8 stores the build (server name, version, tool count, architecture
decisions, deployment details).

## History

| Version | Date | Changes |
|---------|------|---------|
| 1.0.0 | 2026-03-03 | Initial constitution |
| 1.1.0 | 2026-10-02 | Manifest under constitution v1.18.0: profile restatement removed, skill specifics kept |
