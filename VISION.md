# Everything Claude Code - Vision

## What This Is
A third-party open-source plugin/configuration system for Claude Code (and other AI agent harnesses). Production-ready agents, skills, hooks, commands, rules, and MCP configs. Cloned locally as a reference for building out James's own Claude Code workflows.

## The Problem
Claude Code out of the box is powerful but generic. This repo is a battle-tested collection of patterns -- TDD workflows, code review agents, implementation planners, security scanning -- that make Claude Code dramatically more effective for real development work.

## What It Does Today
- Specialized subagents (planner, code reviewer, TDD guide)
- Slash commands (/tdd, /plan, /e2e, /code-review, /build-fix)
- Hook automations (session persistence, pre/post-tool hooks)
- Rules (security, coding style, testing)
- MCP server configurations for external integrations
- Cross-platform support (macOS, Linux, Windows)

## Where It's Going
This is a reference repo, not something James actively develops. It's here to steal good ideas from. The patterns worth adopting get built into James's own `~/apps/cc/` tooling.

A cookbook for Claude Code power users.
