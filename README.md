<p align="center">
  <img src="assets/banner.svg" alt="Awesome Codex CLI" width="600">
</p>

<h1 align="center">Awesome Codex CLI <a href="https://awesome.re"><img src="https://awesome.re/badge.svg" alt="Awesome"></a></h1>

<p align="center">
  <a href="https://github.com/RoggeOhta/awesome-codex-cli"><img src="https://img.shields.io/github/stars/RoggeOhta/awesome-codex-cli?style=social" alt="GitHub stars"></a>
  <img src="https://img.shields.io/badge/resources-200%2B-blue" alt="Resources">
  <a href="https://github.com/RoggeOhta/awesome-codex-cli/commits/main"><img src="https://img.shields.io/github/last-commit/RoggeOhta/awesome-codex-cli" alt="Last Commit"></a>
  <a href="https://github.com/RoggeOhta/awesome-codex-cli/pulls"><img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg" alt="PRs Welcome"></a>
  <img src="https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg" alt="License: CC0">
</p>

> A curated list of awesome tools, skills, subagents, plugins, and resources for [OpenAI Codex CLI](https://github.com/openai/codex) - the open-source AI coding agent that runs in your terminal.

Codex CLI is OpenAI's open-source terminal-based coding agent. It lets you use GPT models to write, refactor, debug, and reason about code directly from the command line - with sandboxed execution, multi-agent orchestration, MCP support, and a growing ecosystem of skills and plugins. Think of it as an AI pair programmer that lives in your terminal.

**Why this list?** The Codex CLI ecosystem is fragmented across dozens of repos - subagents here, skills there, plugins somewhere else. This list consolidates **200+ resources** into one place, organized by feature category, with opinionated descriptions so you know what's actually worth your time.

**Looking for Claude Code or Gemini CLI?** Check the [comparison table](#codex-cli-vs-claude-code-vs-gemini-cli) below.

If you find this useful, please give it a star - it helps others discover the list.

---

## Contents

- [Official Resources](#official-resources)
- [Getting Started](#getting-started)
- [AGENTS.md Templates](#agentsmd-templates)
- [Subagents](#subagents)
- [Skills](#skills)
- [Plugins](#plugins)
- [Hooks](#hooks)
- [MCP Servers](#mcp-servers)
- [IDE & Editor Integrations](#ide--editor-integrations)
- [GUI & Desktop Apps](#gui--desktop-apps)
- [Session & Workflow Management](#session--workflow-management)
- [Model Providers & Proxies](#model-providers--proxies)
- [CI/CD & Automation](#cicd--automation)
- [Cross-Agent Tools](#cross-agent-tools)
- [Monitoring & Analytics](#monitoring--analytics)
- [Docker & Sandboxing](#docker--sandboxing)
- [Account & Auth](#account--auth)
- [Tutorials & Articles](#tutorials--articles)
- [Videos & Podcasts](#videos--podcasts)
- [Comparisons](#comparisons)
- [Community](#community)
- [Shell & Terminal](#shell--terminal)
- [Remote Access](#remote-access)

---

## Official Resources

- [Documentation](https://developers.openai.com/codex) - Official docs covering setup, config, security, and all features.
- [Config Reference](https://developers.openai.com/codex/config-reference) - All 85+ config properties for `config.toml`.
- [Skills Docs](https://developers.openai.com/codex/skills) - How to create and use SKILL.md files.
- [Subagents Docs](https://developers.openai.com/codex/subagents) - Multi-agent orchestration with `.toml` agent definitions.
- [Plugins Docs](https://developers.openai.com/codex/plugins) - Distributable bundles of skills + apps + MCP servers.
- [MCP Docs](https://developers.openai.com/codex/mcp) - Using Codex as MCP client and server.
- [Hooks Docs](https://developers.openai.com/codex/hooks) - User-defined shell scripts in the agentic loop (beta).
- [Security & Sandboxing](https://developers.openai.com/codex/security) - Seatbelt (macOS), Landlock/Bubblewrap (Linux), restricted-token (Windows).
- [Non-interactive Mode](https://developers.openai.com/codex/noninteractive) - `codex exec` for CI/CD and scripting.
- [Slash Commands](https://developers.openai.com/codex/cli/slash-commands) - All 29 built-in commands: `/plan`, `/skills`, `/fast`, `/fork`, `/review`, etc.
- [Best Practices](https://developers.openai.com/codex/learn/best-practices) - Official tips for getting the most out of Codex.
- [Multi-Agent Guide](https://developers.openai.com/codex/multi-agent/) - Parallel fan-out, `max_threads`, depth control.
- [Workflows](https://developers.openai.com/codex/workflows/) - Automation recipes and patterns.
- [Exec Policy](https://developers.openai.com/codex/exec-policy) - Starlark-based fine-grained permission rules.
- [Speed / Fast Mode](https://developers.openai.com/codex/speed) - 1.5x speed, 2x credits.
- [AGENTS.md Guide](https://developers.openai.com/codex/guides/agents-md) - Project-level instructions for Codex.
- [Codex Web](https://chatgpt.com/codex) - Cloud-hosted Codex via ChatGPT.
- [Codex for OSS Fund](https://openai.com/form/codex-for-oss/) - Free Codex access for open-source maintainers.
- [Skills Catalog](https://github.com/openai/skills) - Official skills catalog: `.system`, `.curated`, and `.experimental` skills. The authoritative upstream source. ![GitHub stars](https://img.shields.io/github/stars/openai/skills?style=flat-square)
- [Codex Action](https://github.com/openai/codex-action) - Official GitHub Action for running `codex exec` in CI with sandbox controls. ![GitHub stars](https://img.shields.io/github/stars/openai/codex-action?style=flat-square)
- [Codex Plugin for Claude Code](https://github.com/openai/codex-plugin-cc) - Official plugin to use Codex from Claude Code for code reviews and task delegation. ![GitHub stars](https://img.shields.io/github/stars/openai/codex-plugin-cc?style=flat-square)

## Getting Started

- [DataCamp Tutorial](https://www.datacamp.com/tutorial/open-ai-codex-cli-tutorial) - Beginner-friendly walkthrough with screenshots. Good first read.
- [Blott Studio Guide](https://www.blott.studio/blog/post/openai-codex-cli-build-faster-code-right-from-your-terminal) - Practical getting-started guide focused on real development workflow.
- [Medium Quick Setup](https://medium.com/ai-software-engineer/how-to-install-and-use-openai-codex-cli-in-2-minutes-29e9fdd0e8c5) - 2-minute install-to-first-prompt guide. No fluff.
- [OpenReplay Integration Guide](https://blog.openreplay.com/integrate-openais-codex-cli-tool-development-workflow/) - How to weave Codex into an existing dev workflow.
- [Machine Learning Mastery](https://machinelearningmastery.com/understanding-openai-codex-cli-commands/) - Command reference with examples for each mode.

## AGENTS.md Templates

Project-level instruction files that tell Codex how to work with your codebase - the equivalent of Claude Code's `CLAUDE.md`.

- [agents.md (Open Standard)](https://agents.md) - The cross-agent standard used by 20k+ projects. Works with Codex, Claude Code, Gemini CLI, and more.
- [codex-cli-best-practice](https://github.com/shanraisshan/codex-cli-best-practice) - Battle-tested AGENTS.md patterns with sandbox mode recommendations and approval policies. ![GitHub stars](https://img.shields.io/github/stars/shanraisshan/codex-cli-best-practice?style=flat-square)
- [claude-codex-settings](https://github.com/fcakyon/claude-codex-settings) - Dual AGENTS.md + CLAUDE.md setup for teams running both agents side-by-side. ![GitHub stars](https://img.shields.io/github/stars/fcakyon/claude-codex-settings?style=flat-square)
- [caliber-ai-org/ai-setup](https://github.com/caliber-ai-org/ai-setup) - Cross-tool config generator - outputs AGENTS.md, CLAUDE.md, and .cursorrules from one source. ![GitHub stars](https://img.shields.io/github/stars/caliber-ai-org/ai-setup?style=flat-square)
- [agentsmd/agents.md](https://github.com/agentsmd/agents.md) - The open AGENTS.md specification under Linux Foundation. 60k+ adopting projects. ![GitHub stars](https://img.shields.io/github/stars/agentsmd/agents.md?style=flat-square)

## Subagents

Multi-agent orchestration with `.toml` definitions. Codex supports parallel fan-out with up to 6 threads by default.

### Collections

- [VoltAgent/awesome-codex-subagents](https://github.com/VoltAgent/awesome-codex-subagents) - The definitive collection. 136+ agents across 10 categories (core dev, language specialists, infra, security, data/AI, DX, domains, business, meta, orchestration). Just clone and use. ![GitHub stars](https://img.shields.io/github/stars/VoltAgent/awesome-codex-subagents?style=flat-square)
- [betterup/codex-cli-subagents](https://github.com/betterup/codex-cli-subagents) - Enterprise-focused agents for code review, migration, and compliance. ![GitHub stars](https://img.shields.io/github/stars/betterup/codex-cli-subagents?style=flat-square)

### Specialized Subagents

- [leonardsellem/codex-specialized-subagents](https://github.com/leonardsellem/codex-specialized-subagents) - Niche agents: accessibility auditor, i18n extractor, performance profiler. Fills gaps VoltAgent doesn't cover. ![GitHub stars](https://img.shields.io/github/stars/leonardsellem/codex-specialized-subagents?style=flat-square)
- [CoderMageFox/claudecode-codex-subagents](https://github.com/CoderMageFox/claudecode-codex-subagents) - Agents that work across both Codex and Claude Code. Good for mixed teams. ![GitHub stars](https://img.shields.io/github/stars/CoderMageFox/claudecode-codex-subagents?style=flat-square)
- [Alexin09/cc-subagent-codex](https://github.com/Alexin09/cc-subagent-codex) - Lightweight subagent pack focused on TypeScript/React projects. ![GitHub stars](https://img.shields.io/github/stars/Alexin09/cc-subagent-codex?style=flat-square)

### Multi-Agent Orchestration

- [basilisk-labs/codex-swarm](https://github.com/basilisk-labs/codex-swarm) - Swarm intelligence pattern - multiple Codex agents collaborating on large refactors. ![GitHub stars](https://img.shields.io/github/stars/basilisk-labs/codex-swarm?style=flat-square)
- [aannoo/hcom](https://github.com/aannoo/hcom) - Hierarchical agent communication framework. Agents delegate subtasks with context preservation. ![GitHub stars](https://img.shields.io/github/stars/aannoo/hcom?style=flat-square)
- [obra/external-subagents](https://github.com/obra/external-subagents) - Run subagents as external processes with custom sandboxing. ![GitHub stars](https://img.shields.io/github/stars/obra/external-subagents?style=flat-square)

## Skills

Reusable instruction bundles in `SKILL.md` format. Place in `~/.codex/skills/` (global) or `.agents/skills/` (project).

### Collections

- [ComposioHQ/awesome-codex-skills](https://github.com/ComposioHQ/awesome-codex-skills) - 38 skills across dev tools, productivity, communication, data analysis. Heavy Composio integration for 1000+ SaaS apps. ![GitHub stars](https://img.shields.io/github/stars/ComposioHQ/awesome-codex-skills?style=flat-square)
- [heilcheng/awesome-agent-skills](https://github.com/heilcheng/awesome-agent-skills) - Cross-platform skills that work in Codex, Claude Code, and Gemini CLI. ![GitHub stars](https://img.shields.io/github/stars/heilcheng/awesome-agent-skills?style=flat-square)
- [Prat011/awesome-llm-skills](https://github.com/Prat011/awesome-llm-skills) - Platform-agnostic skills organized by use case. ![GitHub stars](https://img.shields.io/github/stars/Prat011/awesome-llm-skills?style=flat-square)
- [skillmatic-ai/awesome-agent-skills](https://github.com/skillmatic-ai/awesome-agent-skills) - Community-driven skill marketplace with quality ratings. ![GitHub stars](https://img.shields.io/github/stars/skillmatic-ai/awesome-agent-skills?style=flat-square)
- [proflead/codex-skills-library](https://github.com/proflead/codex-skills-library) - Focused collection: code review, Git workflow, documentation generation. ![GitHub stars](https://img.shields.io/github/stars/proflead/codex-skills-library?style=flat-square)
- [sickn33/antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) - 1,340+ installable skills with CLI installer, role-based bundles, and searchable catalog. ![GitHub stars](https://img.shields.io/github/stars/sickn33/antigravity-awesome-skills?style=flat-square)
- [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills) - 1,000+ agent skills from official dev teams and community. Works with Codex, Claude Code, Gemini CLI, Cursor. ![GitHub stars](https://img.shields.io/github/stars/VoltAgent/awesome-agent-skills?style=flat-square)
- [alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills) - 220+ skills across engineering, marketing, compliance, C-level advisory. Works with Codex despite the name. ![GitHub stars](https://img.shields.io/github/stars/alirezarezvani/claude-skills?style=flat-square)
- [JimLiu/baoyu-skills](https://github.com/JimLiu/baoyu-skills) - Large curated skills repository with broad category coverage. ![GitHub stars](https://img.shields.io/github/stars/JimLiu/baoyu-skills?style=flat-square)
- [mxyhi/ok-skills](https://github.com/mxyhi/ok-skills) - 55 curated skills and AGENTS.md playbooks: research, planning, GitHub automation, browser QA, frontend design. ![GitHub stars](https://img.shields.io/github/stars/mxyhi/ok-skills?style=flat-square)
- [affaan-m/everything-claude-code](https://github.com/affaan-m/everything-claude-code) - Performance optimization system with 36 agents and 147 skills. Has `/codex-setup` command for Codex CLI. ![GitHub stars](https://img.shields.io/github/stars/affaan-m/everything-claude-code?style=flat-square)

### Specialized Skills

- [Upskill](https://github.com/huggingface/upskill) - Hugging Face's official skill pack for ML/AI development workflows. ![GitHub stars](https://img.shields.io/github/stars/huggingface/upskill?style=flat-square)
- [Mukul975/Anthropic-Cybersecurity-Skills](https://github.com/mukul975/Anthropic-Cybersecurity-Skills) - Security-focused skills: vulnerability scanning, dependency auditing, OWASP checks. Works in Codex too despite the name. ![GitHub stars](https://img.shields.io/github/stars/mukul975/Anthropic-Cybersecurity-Skills?style=flat-square)
- [nicepkg/ai-workflow](https://github.com/nicepkg/ai-workflow) - Workflow automation skills - chained multi-step tasks with conditional logic. ![GitHub stars](https://img.shields.io/github/stars/nicepkg/ai-workflow?style=flat-square)
- [cathrynlavery/codex-skill](https://github.com/cathrynlavery/codex-skill) - Clean, well-documented single-purpose skills. Good reference for writing your own. ![GitHub stars](https://img.shields.io/github/stars/cathrynlavery/codex-skill?style=flat-square)
- [Karanjot786/agent-skills-cli](https://github.com/Karanjot786/agent-skills-cli) - CLI tool to discover, install, and manage skills from the community. ![GitHub stars](https://img.shields.io/github/stars/Karanjot786/agent-skills-cli?style=flat-square)
- [twostraws/SwiftUI-Agent-Skill](https://github.com/twostraws/SwiftUI-Agent-Skill) - SwiftUI agent skill by Paul Hudson. Covers navigation, layout, animations, state management, VoiceOver. ![GitHub stars](https://img.shields.io/github/stars/twostraws/SwiftUI-Agent-Skill?style=flat-square)
- [Dimillian/Skills](https://github.com/Dimillian/Skills) - Codex skills by Thomas Ricouard: App Store changelog, iOS debugging, macOS packaging, SwiftUI perf audits. ![GitHub stars](https://img.shields.io/github/stars/Dimillian/Skills?style=flat-square)
- [dpearson2699/swift-ios-skills](https://github.com/dpearson2699/swift-ios-skills) - 76 agent skills for iOS 26+, Swift 6.3, SwiftUI, and modern Apple frameworks. ![GitHub stars](https://img.shields.io/github/stars/dpearson2699/swift-ios-skills?style=flat-square)
- [callstackincubator/agent-skills](https://github.com/callstackincubator/agent-skills) - Agent-optimized React Native skills by Callstack: best practices, optimization, upgrade workflows. ![GitHub stars](https://img.shields.io/github/stars/callstackincubator/agent-skills?style=flat-square)
- [Bhanunamikaze/Agentic-SEO-Skill](https://github.com/Bhanunamikaze/Agentic-SEO-Skill) - LLM-first SEO analysis with 16 sub-skills, 10 specialist agents, and 33 utility scripts. ![GitHub stars](https://img.shields.io/github/stars/Bhanunamikaze/Agentic-SEO-Skill?style=flat-square)

### Skills Management

- [runkids/skillshare](https://github.com/runkids/skillshare) - CLI to sync skills across 55+ AI CLI tools from a single source. Security-audited Go binary. ![GitHub stars](https://img.shields.io/github/stars/runkids/skillshare?style=flat-square)
- [Dimillian/CodexSkillManager](https://github.com/Dimillian/CodexSkillManager) - macOS SwiftUI app to manage local Codex and Claude Code skills. Browse and download from Clawdhub. ![GitHub stars](https://img.shields.io/github/stars/Dimillian/CodexSkillManager?style=flat-square)
- [jiweiyeah/Skills-Manager](https://github.com/jiweiyeah/Skills-Manager) - Cross-platform desktop app (Tauri 2.0 + React 19 + Rust) for managing skills across multiple AI tools. ![GitHub stars](https://img.shields.io/github/stars/jiweiyeah/Skills-Manager?style=flat-square)
- [aiskillstore/marketplace](https://github.com/aiskillstore/marketplace) - Security-audited skills marketplace. One-click install with automated security analysis. ![GitHub stars](https://img.shields.io/github/stars/aiskillstore/marketplace?style=flat-square)

### Domain-Specific Skills

- [aklofas/kicad-happy](https://github.com/aklofas/kicad-happy) - KiCad PCB design assistant. Proof that skills can go deep into niche domains. ![GitHub stars](https://img.shields.io/github/stars/aklofas/kicad-happy?style=flat-square)
- [qtzx06/yolodex](https://github.com/qtzx06/yolodex) - Computer vision / YOLO model training workflow. ![GitHub stars](https://img.shields.io/github/stars/qtzx06/yolodex?style=flat-square)
- [Frankieli123/grok-skill](https://github.com/Frankieli123/grok-skill) - Log analysis and pattern matching. Useful for debugging production issues. ![GitHub stars](https://img.shields.io/github/stars/Frankieli123/grok-skill?style=flat-square)

## Plugins

Distributable bundles combining skills + app integrations + MCP servers. Defined in `.codex-plugin/plugin.json`. Browse with `/plugins`.

- [hashgraph-online/awesome-codex-plugins](https://github.com/hashgraph-online/awesome-codex-plugins) - The first plugin directory. Lists 12 official + ~20 community plugins with install instructions. ![GitHub stars](https://img.shields.io/github/stars/hashgraph-online/awesome-codex-plugins?style=flat-square)
- [agent-sh/agentsys](https://github.com/agent-sh/agentsys) - Plugin framework with dependency resolution and version management. ![GitHub stars](https://img.shields.io/github/stars/agent-sh/agentsys?style=flat-square)
- [xmm/codex-bmad-skills](https://github.com/xmm/codex-bmad-skills) - BMAD methodology plugin - structured planning, design, and implementation workflow.
- [regenrek/codex-1up](https://github.com/regenrek/codex-1up) - Bootstrap tool that installs Codex CLI plus curated power tools and an AGENTS.md template. Three profiles: balanced, safe, yolo. ![GitHub stars](https://img.shields.io/github/stars/regenrek/codex-1up?style=flat-square)

## Hooks

User-defined shell scripts that run at specific points in the agentic loop. Requires `codex_hooks = true` feature flag.

- [shanraisshan/codex-cli-hooks](https://github.com/shanraisshan/codex-cli-hooks) - Starter hooks collection: pre-commit validation, cost tracking, notification triggers. ![GitHub stars](https://img.shields.io/github/stars/shanraisshan/codex-cli-hooks?style=flat-square)
- [liewcf/codex-notify-macos](https://github.com/liewcf/codex-notify-macos) - macOS notification hook - get alerted when long-running tasks complete. ![GitHub stars](https://img.shields.io/github/stars/liewcf/codex-notify-macos?style=flat-square)

## MCP Servers

Codex can connect to MCP servers (as client) and expose itself as an MCP server (`codex mcp-server`).

### Codex as MCP Client

- [tuannvm/codex-mcp-server](https://github.com/tuannvm/codex-mcp-server) - General-purpose MCP server for Codex with file operations, web search, and database queries. ![GitHub stars](https://img.shields.io/github/stars/tuannvm/codex-mcp-server?style=flat-square)
- [FYZAFH/mcp-codex-dev](https://github.com/FYZAFH/mcp-codex-dev) - Development-focused MCP server: linting, testing, deployment tools. ![GitHub stars](https://img.shields.io/github/stars/FYZAFH/mcp-codex-dev?style=flat-square)
- [cexll/codex-mcp-server](https://github.com/cexll/codex-mcp-server) - Lightweight MCP server with minimal dependencies. Good starting point for custom servers. ![GitHub stars](https://img.shields.io/github/stars/cexll/codex-mcp-server?style=flat-square)
- [Wildcard-Official/deepcontext-mcp](https://github.com/Wildcard-Official/deepcontext-mcp) - Codebase understanding server - builds semantic index for smarter code navigation. ![GitHub stars](https://img.shields.io/github/stars/Wildcard-Official/deepcontext-mcp?style=flat-square)
- [DeusData/codebase-memory-mcp](https://github.com/DeusData/codebase-memory-mcp) - Persistent project memory across sessions. Codex remembers decisions, patterns, and context. ![GitHub stars](https://img.shields.io/github/stars/DeusData/codebase-memory-mcp?style=flat-square)
- [Shelpuk-AI-Technology-Consulting/kindly-web-search-mcp-server](https://github.com/Shelpuk-AI-Technology-Consulting/kindly-web-search-mcp-server) - Web search MCP with rate limiting and caching. ![GitHub stars](https://img.shields.io/github/stars/Shelpuk-AI-Technology-Consulting/kindly-web-search-mcp-server?style=flat-square)
- [milisp/mcp-linker](https://github.com/milisp/mcp-linker) - Link multiple MCP servers together. Chain tools across servers. ![GitHub stars](https://img.shields.io/github/stars/milisp/mcp-linker?style=flat-square)

### Codex as MCP Server

- [leonardsellem/codex-subagents-mcp](https://github.com/leonardsellem/codex-subagents-mcp) - Expose Codex subagents as MCP tools. Other agents (Claude Code, Cursor) can call Codex agents. ![GitHub stars](https://img.shields.io/github/stars/leonardsellem/codex-subagents-mcp?style=flat-square)
- [Mr-Tomahawk/codex-cli-mcp-tool](https://github.com/Mr-Tomahawk/codex-cli-mcp-tool) - Wrap Codex CLI as an MCP tool for use in other agent frameworks. ![GitHub stars](https://img.shields.io/github/stars/Mr-Tomahawk/codex-cli-mcp-tool?style=flat-square)
- [agency-ai-solutions/openai-codex-mcp](https://github.com/agency-ai-solutions/openai-codex-mcp) - Full-featured Codex MCP bridge with streaming support. ![GitHub stars](https://img.shields.io/github/stars/agency-ai-solutions/openai-codex-mcp?style=flat-square)

### General-Purpose MCP

- [PleasePrompto/notebooklm-mcp](https://github.com/PleasePrompto/notebooklm-mcp) - Connect Codex to NotebookLM for research-augmented coding. ![GitHub stars](https://img.shields.io/github/stars/PleasePrompto/notebooklm-mcp?style=flat-square)

## IDE & Editor Integrations

- [VS Code Extension (Official)](https://marketplace.visualstudio.com/items?itemName=openai.chatgpt) - The official extension. Inline chat, terminal integration, code actions.
- [johnseth97/codex.nvim](https://github.com/johnseth97/codex.nvim) - Neovim plugin with floating terminal, keybindings, and context passing. ![GitHub stars](https://img.shields.io/github/stars/johnseth97/codex.nvim?style=flat-square)
- [milanglacier/yarepl.nvim](https://github.com/milanglacier/yarepl.nvim) - REPL framework for Neovim. Supports Codex as a REPL target alongside Python, R, etc. ![GitHub stars](https://img.shields.io/github/stars/milanglacier/yarepl.nvim?style=flat-square)
- [xenodium/agent-shell](https://github.com/xenodium/agent-shell) - Emacs integration that works with Codex, Claude Code, and other terminal agents. Best-in-class Emacs experience. ![GitHub stars](https://img.shields.io/github/stars/xenodium/agent-shell?style=flat-square)
- [tninja/ai-code-interface.el](https://github.com/tninja/ai-code-interface.el) - Emacs interface for multiple AI coding agents including Codex. ![GitHub stars](https://img.shields.io/github/stars/tninja/ai-code-interface.el?style=flat-square)
- [bennfocus/codex-cli.el](https://github.com/bennfocus/codex-cli.el) - Lightweight Emacs wrapper. Minimal, focused. ![GitHub stars](https://img.shields.io/github/stars/bennfocus/codex-cli.el?style=flat-square)
- [dliedke/ClaudeCodeExtension](https://github.com/dliedke/ClaudeCodeExtension) - Visual Studio .NET extension that supports both Claude Code and Codex CLI. ![GitHub stars](https://img.shields.io/github/stars/dliedke/ClaudeCodeExtension?style=flat-square)
- [smallmain/vscode-unify-chat-provider](https://github.com/smallmain/vscode-unify-chat-provider) - Unify multiple AI agents (Codex, Claude, Copilot) under one VS Code chat interface. ![GitHub stars](https://img.shields.io/github/stars/smallmain/vscode-unify-chat-provider?style=flat-square)
- [folke/sidekick.nvim](https://github.com/folke/sidekick.nvim) - Neovim AI sidekick supporting Claude, Gemini, Grok, Codex, Copilot CLI and more. Built-in AI terminal. ![GitHub stars](https://img.shields.io/github/stars/folke/sidekick.nvim?style=flat-square)

## GUI & Desktop Apps

- [milisp/codexia](https://github.com/milisp/codexia) - Desktop GUI for Codex CLI. macOS/Windows/Linux. Visual session management, file tree, diff viewer. ![GitHub stars](https://img.shields.io/github/stars/milisp/codexia?style=flat-square)
- [xintaofei/codeg](https://github.com/xintaofei/codeg) - Electron-based GUI with project templates and one-click sandboxing. ![GitHub stars](https://img.shields.io/github/stars/xintaofei/codeg?style=flat-square)
- [nkmr-jp/prompt-line](https://github.com/nkmr-jp/prompt-line) - Minimal prompt-centric UI. Stays out of your way. ![GitHub stars](https://img.shields.io/github/stars/nkmr-jp/prompt-line?style=flat-square)
- [zhu1090093659/CodeConductor](https://github.com/zhu1090093659/CodeConductor) - Orchestrator GUI for managing multiple Codex agents visually. ![GitHub stars](https://img.shields.io/github/stars/zhu1090093659/CodeConductor?style=flat-square)
- [Dimillian/CodexMonitor](https://github.com/Dimillian/CodexMonitor) - Tauri/React/Rust desktop app for orchestrating multiple Codex agents across workspaces. Multi-workspace, git integration, prompt library. ![GitHub stars](https://img.shields.io/github/stars/Dimillian/CodexMonitor?style=flat-square)
- [slopus/happy](https://github.com/slopus/happy) - Mobile and web client for Codex and Claude Code with end-to-end encryption. iOS/Android, push notifications, open-source. ![GitHub stars](https://img.shields.io/github/stars/slopus/happy?style=flat-square)
- [just-every/code](https://github.com/just-every/code) - Enhanced Codex CLI fork with browser integration, multi-agent automation, Auto Drive orchestration, and theming. ![GitHub stars](https://img.shields.io/github/stars/just-every/code?style=flat-square)

## Session & Workflow Management

- [UfoMiao/zcf](https://github.com/UfoMiao/zcf) - Zero-config workflow framework. Chain prompts, branch on results, auto-retry failures. ![GitHub stars](https://img.shields.io/github/stars/UfoMiao/zcf?style=flat-square)
- [gotalab/cc-sdd](https://github.com/gotalab/cc-sdd) - Spec-driven development workflow. Write specs, Codex implements, auto-validates against spec. ![GitHub stars](https://img.shields.io/github/stars/gotalab/cc-sdd?style=flat-square)
- [covibes/zeroshot](https://github.com/covibes/zeroshot) - Zero-shot task runner. Describe what you want in plain English, get a working codebase. ![GitHub stars](https://img.shields.io/github/stars/covibes/zeroshot?style=flat-square)
- [waskosky/codex-cli-farm](https://github.com/waskosky/codex-cli-farm) - Run multiple Codex instances in parallel on different tasks. Session isolation built-in. ![GitHub stars](https://img.shields.io/github/stars/waskosky/codex-cli-farm?style=flat-square)
- [joseferben/hands-please](https://github.com/joseferben/hands-please) - Human-in-the-loop workflow. Codex pauses at decision points and asks for your input. ![GitHub stars](https://img.shields.io/github/stars/joseferben/hands-please?style=flat-square)
- [standardagents/dmux](https://github.com/standardagents/dmux) - Dev agent multiplexer: isolated tmux pane + git worktree per task. Supports 11+ agents including Codex. ![GitHub stars](https://img.shields.io/github/stars/standardagents/dmux?style=flat-square)
- [mixpeek/amux](https://github.com/mixpeek/amux) - Open-source agent multiplexer. Run dozens of parallel Codex/Claude agents unattended via tmux. Self-healing watchdog. ![GitHub stars](https://img.shields.io/github/stars/mixpeek/amux?style=flat-square)

## Model Providers & Proxies

Codex supports `openai_base_url` for custom model providers. Use any OpenAI-compatible API.

- [feiskyer/codex-settings](https://github.com/feiskyer/codex-settings) - Ready-to-use configs for LiteLLM, Ollama, LM Studio, OpenRouter, and Azure OpenAI. ![GitHub stars](https://img.shields.io/github/stars/feiskyer/codex-settings?style=flat-square)
- [teabranch/open-responses-server](https://github.com/teabranch/open-responses-server) - OpenAI Responses API-compatible server. Run Codex with local models. ![GitHub stars](https://img.shields.io/github/stars/teabranch/open-responses-server?style=flat-square)
- [erans/lunaroute](https://github.com/erans/lunaroute) - Model router with cost tracking, rate limiting, and fallback chains. ![GitHub stars](https://img.shields.io/github/stars/erans/lunaroute?style=flat-square)
- [ben-vargas/ai-sdk-provider-codex-cli](https://github.com/ben-vargas/ai-sdk-provider-codex-cli) - Vercel AI SDK provider for Codex. Use Codex in your AI applications. ![GitHub stars](https://img.shields.io/github/stars/ben-vargas/ai-sdk-provider-codex-cli?style=flat-square)
- [router-for-me/CLIProxyAPI](https://github.com/router-for-me/CLIProxyAPI) - Wrap Codex, Claude Code, Gemini CLI as OpenAI-compatible API endpoints. Multi-account load balancing, streaming. ![GitHub stars](https://img.shields.io/github/stars/router-for-me/CLIProxyAPI?style=flat-square)
- [codingmoh/open-codex](https://github.com/codingmoh/open-codex) - Open-source Codex-inspired CLI running 100% locally with Ollama. No API key required, offline capable. ![GitHub stars](https://img.shields.io/github/stars/codingmoh/open-codex?style=flat-square)

## CI/CD & Automation

Use `codex exec` for non-interactive automation in pipelines.

- [onurkanbakirci/awesome-codex-automations](https://github.com/onurkanbakirci/awesome-codex-automations) - 35 automation recipes organized by category: code quality, CI/CD, releases, deps, security. ![GitHub stars](https://img.shields.io/github/stars/onurkanbakirci/awesome-codex-automations?style=flat-square)
- [openai/codex-action](https://github.com/openai/codex-action) - Official GitHub Action: install Codex, configure sandbox, run `codex exec` in CI. ![GitHub stars](https://img.shields.io/github/stars/openai/codex-action?style=flat-square)

### Patterns

```bash
# Run Codex in CI to auto-fix lint errors
codex exec "Fix all ESLint errors in src/" --approval-mode full-auto

# Generate PR descriptions from diffs
git diff main | codex exec "Write a PR description for these changes"

# Pipe output for processing
codex exec "List all TODO comments" --ephemeral | sort
```

## Cross-Agent Tools

Tools that bridge Codex with other AI coding agents.

- [DeepMyst/Mysti](https://github.com/DeepMyst/Mysti) - Universal agent orchestrator. Route tasks between Codex, Claude Code, and Gemini CLI based on model strengths. ![GitHub stars](https://img.shields.io/github/stars/DeepMyst/Mysti?style=flat-square)
- [athola/skrills](https://github.com/athola/skrills) - Cross-platform skill format. Write once, use in Codex and Claude Code. ![GitHub stars](https://img.shields.io/github/stars/athola/skrills?style=flat-square)
- [jcputney/agent-peer-review](https://github.com/jcputney/agent-peer-review) - Codex reviews Claude Code's output (and vice versa). Catches model-specific blind spots. ![GitHub stars](https://img.shields.io/github/stars/jcputney/agent-peer-review?style=flat-square)
- [abhishekgahlot2/codex-claude-bridge](https://github.com/abhishekgahlot2/codex-claude-bridge) - Run Codex and Claude Code in tandem on the same codebase. ![GitHub stars](https://img.shields.io/github/stars/abhishekgahlot2/codex-claude-bridge?style=flat-square)
- [lbb00/ai-rules-sync](https://github.com/lbb00/ai-rules-sync) - Sync AGENTS.md ↔ CLAUDE.md ↔ .cursorrules. One source, all formats. ![GitHub stars](https://img.shields.io/github/stars/lbb00/ai-rules-sync?style=flat-square)
- [sypsyp97/claude-skill-codex](https://github.com/sypsyp97/claude-skill-codex) - Run Codex CLI as a Claude Code skill. ![GitHub stars](https://img.shields.io/github/stars/sypsyp97/claude-skill-codex?style=flat-square)
- [chenhg5/cc-connect](https://github.com/chenhg5/cc-connect) - Bridge Codex/Claude Code to 10 messaging platforms (Telegram, Slack, DingTalk, WeChat Work, LINE). No public IP required. ![GitHub stars](https://img.shields.io/github/stars/chenhg5/cc-connect?style=flat-square)
- [bfly123/claude_code_bridge](https://github.com/bfly123/claude_code_bridge) - Real-time multi-AI collaboration: Claude, Codex, Gemini in simultaneous split-pane sessions with persistent context. ![GitHub stars](https://img.shields.io/github/stars/bfly123/claude_code_bridge?style=flat-square)
- [AgentsMesh/AgentsMesh](https://github.com/AgentsMesh/AgentsMesh) - AI Agent Fleet Command Center. Orchestrate Codex, Claude Code, Gemini CLI, Aider from a single platform with Kanban and SSO/RBAC. ![GitHub stars](https://img.shields.io/github/stars/AgentsMesh/AgentsMesh?style=flat-square)
- [dsifry/metaswarm](https://github.com/dsifry/metaswarm) - Self-improving multi-agent orchestration: 18 agents, 13 skills, TDD enforcement, quality gates. ![GitHub stars](https://img.shields.io/github/stars/dsifry/metaswarm?style=flat-square)
- [pchalasani/claude-code-tools](https://github.com/pchalasani/claude-code-tools) - Practical productivity tools for Claude Code and Codex CLI: session management, terminal automation, voice integration. ![GitHub stars](https://img.shields.io/github/stars/pchalasani/claude-code-tools?style=flat-square)

## Monitoring & Analytics

- [NihilDigit/waybar-ai-usage](https://github.com/NihilDigit/waybar-ai-usage) - Waybar widget showing real-time Codex token usage and costs. Linux desktop integration. ![GitHub stars](https://img.shields.io/github/stars/NihilDigit/waybar-ai-usage?style=flat-square)
- [yoavf/ai-sessions-mcp](https://github.com/yoavf/ai-sessions-mcp) - MCP server that tracks session history, token usage, and cost across agents. ![GitHub stars](https://img.shields.io/github/stars/yoavf/ai-sessions-mcp?style=flat-square)
- [HizTam/codex-history-viewer](https://github.com/HizTam/codex-history-viewer) - Browse and search past Codex sessions with full context. ![GitHub stars](https://img.shields.io/github/stars/HizTam/codex-history-viewer?style=flat-square)
- [steipete/CodexBar](https://github.com/steipete/CodexBar) - macOS menu bar app showing usage stats for Codex, Claude, Cursor, Gemini without login. On-device parsing. ![GitHub stars](https://img.shields.io/github/stars/steipete/CodexBar?style=flat-square)
- [ryoppippi/ccusage](https://github.com/ryoppippi/ccusage) - CLI for analyzing Codex/Claude Code usage from local JSONL files. Daily/monthly reports, cost breakdown, MCP server mode. ![GitHub stars](https://img.shields.io/github/stars/ryoppippi/ccusage?style=flat-square)
- [junhoyeo/tokscale](https://github.com/junhoyeo/tokscale) - CLI + TUI + web dashboard tracking token usage across 16+ AI coding platforms. Rust core, contribution graphs, leaderboard. ![GitHub stars](https://img.shields.io/github/stars/junhoyeo/tokscale?style=flat-square)

## Docker & Sandboxing

- [Codex Universal](https://github.com/openai/codex-universal) - Official Docker base image. Pre-configured sandbox, multi-language support.
- [DeepBlueDynamics/gnosis-container](https://github.com/DeepBlueDynamics/gnosis-container) - Codex CLI in Docker with 275+ MCP tools, cron/file-watcher/webhook triggers, multi-model support. ![GitHub stars](https://img.shields.io/github/stars/DeepBlueDynamics/gnosis-container?style=flat-square)

## Account & Auth

- [numman-ali/opencode-openai-codex-auth](https://github.com/numman-ali/opencode-openai-codex-auth) - Use your ChatGPT Plus/Pro subscription as a Codex auth source. The most popular auth tool. ![GitHub stars](https://img.shields.io/github/stars/numman-ali/opencode-openai-codex-auth?style=flat-square)
- [Lampese/codex-switcher](https://github.com/Lampese/codex-switcher) - Switch between multiple OpenAI accounts. Useful for work/personal separation. ![GitHub stars](https://img.shields.io/github/stars/Lampese/codex-switcher?style=flat-square)
- [bashar94/codex-cli-account-switcher](https://github.com/bashar94/codex-cli-account-switcher) - Simple account switcher with profile support. ![GitHub stars](https://img.shields.io/github/stars/bashar94/codex-cli-account-switcher?style=flat-square)
- [bddiudiu/cpa-codex-auth-sweep-cliproxy](https://github.com/bddiudiu/cpa-codex-auth-sweep-cliproxy) - Auth proxy for enterprise SSO environments. ![GitHub stars](https://img.shields.io/github/stars/bddiudiu/cpa-codex-auth-sweep-cliproxy?style=flat-square)
- [Loongphy/codex-auth](https://github.com/Loongphy/codex-auth) - CLI to switch and manage multiple Codex accounts with usage stats and automatic switching. ![GitHub stars](https://img.shields.io/github/stars/Loongphy/codex-auth?style=flat-square)

## Tutorials & Articles

- [How Codex is Built (Pragmatic Engineer)](https://newsletter.pragmaticengineer.com/p/how-codex-is-built) - Deep technical dive into Codex's architecture. Rust, sandboxing, the TUI. Essential reading.
- [Dogfood: Codex Builds Codex (Stack Overflow)](https://stackoverflow.blog/2026/02/24/dogfood-so-nutritious-it-s-building-the-future-of-sdlcs/) - How the Codex team uses their own tool. Real-world workflow patterns.
- [How Codex Team Uses Their Agent (Every)](https://every.to/podcast/transcript-how-openai-s-codex-team-uses-their-coding-agent) - Transcript of the team discussing daily usage, tips, and antipatterns.
- [Why Humans are AI's Biggest Bottleneck (Lenny's Newsletter)](https://www.lennysnewsletter.com/p/why-humans-are-ais-biggest-bottleneck) - Broader perspective on AI coding agents, with Codex as a case study.
- [Apidog: OpenAI Codex CLI](https://apidog.com/blog/openai-codex-cli/) - API-focused guide. Good for integrating Codex into existing toolchains.

## Videos & Podcasts

*Know a great video or podcast episode about Codex CLI? [Submit it!](https://github.com/user/awesome-codex-cli/issues/new)*

## Comparisons

### Codex CLI vs Claude Code vs Gemini CLI

| Feature                  | Codex CLI                                                                        | Claude Code                        | Gemini CLI                                                                           |
| ------------------------ | -------------------------------------------------------------------------------- | ---------------------------------- | ------------------------------------------------------------------------------------ |
| **Language**             | Rust                                                                             | TypeScript                         | Python                                                                               |
| **License**              | Apache-2.0                                                                       | Proprietary                        | Apache-2.0                                                                           |
| **Pricing**              | ChatGPT Pro $20/mo or API usage                                                  | Max $100/mo or API usage           | Free (Gemini API)                                                                    |
| **Config file**          | `config.toml`                                                                    | `settings.json`                    | `settings.json`                                                                      |
| **Project instructions** | `AGENTS.md`                                                                      | `CLAUDE.md`                        | `GEMINI.md`                                                                          |
| **Sandbox**              | Seatbelt/Landlock/Bubblewrap                                                     | macOS Seatbelt, Linux containers   | Docker-based                                                                         |
| **Multi-agent**          | Built-in (6 parallel threads)                                                    | Subagent spawning                  | Limited                                                                              |
| **Skills**               | `SKILL.md` files                                                                 | Slash-command skills               | N/A                                                                                  |
| **Plugins**              | `.codex-plugin/` bundles                                                         | N/A                                | Extensions                                                                           |
| **Hooks**                | Shell scripts (beta)                                                             | Pre/post hooks                     | N/A                                                                                  |
| **MCP support**          | Client + Server                                                                  | Client only                        | Client only                                                                          |
| **IDE**                  | VS Code, Neovim, Emacs, Zed                                                      | VS Code, JetBrains, Web            | VS Code                                                                              |
| **Auth**                 | ChatGPT sub or API key                                                           | Anthropic API key                  | Google account                                                                       |
| **Models**               | GPT-5.x, o-series                                                                | Claude 4.x                         | Gemini 2.x                                                                           |
| **Non-interactive**      | `codex exec`                                                                     | `claude -p`                        | `gemini exec`                                                                        |
| **Context window**       | 200k tokens                                                                      | 200k tokens                        | 1M tokens                                                                            |
| **Image input**          | Yes                                                                              | Yes                                | Yes                                                                                  |
| **GitHub stars**         | ![](https://img.shields.io/github/stars/openai/codex?style=flat-square)          | Closed source                      | ![](https://img.shields.io/github/stars/google-gemini/gemini-cli?style=flat-square)  |
| **Ecosystem size**       | Growing (plugins, skills, subagents)                                             | Mature (MCP, skills, hooks)        | Early (extensions)                                                                   |

### Related Comparisons

- [Hacker News Discussion](https://news.ycombinator.com/item?id=43708025) - Community comparison thread with real-world experiences.
- [Reddit AMA with Codex Team](https://www.reddit.com/r/ChatGPT/comments/1ko3tp1/ama_with_openai_codex_team/) - Team answers questions about design decisions and how Codex differs from alternatives.
- [duanyytop/agents-radar](https://github.com/duanyytop/agents-radar) - Side-by-side benchmark of terminal AI agents on real coding tasks. ![GitHub stars](https://img.shields.io/github/stars/duanyytop/agents-radar?style=flat-square)

## Community

- [GitHub Discussions](https://github.com/openai/codex/discussions) - Official discussion forum. Feature requests, bug reports, tips.
- [Reddit r/ChatGPT](https://www.reddit.com/r/ChatGPT/) - Active discussions about Codex CLI in the broader ChatGPT community.
- [OpenAI Developer Forum](https://community.openai.com/) - Official OpenAI community with Codex-specific threads.
- [@OpenAIDevs on X](https://x.com/OpenAIDevs) - Official announcements and tips.

### People to Follow

Codex CLI team members and frequent contributors:

- [@thsottiaux](https://x.com/thsottiaux) - Tibo, Codex team.
- [@embirico](https://x.com/embirico) - Embiricos, Codex team.
- [@jxnlco](https://x.com/jxnlco) - Jason, Codex team.
- [@romainhuet](https://x.com/romainhuet) - Romain Huet, OpenAI DevRel.
- [@dkundel](https://x.com/dkundel) - Dominik Kundel, OpenAI DevRel.
- [@fouadmatin](https://x.com/fouadmatin) - Fouad Matin, Codex team.
- [@bolinfest](https://x.com/bolinfest) - Bolin Fest, Codex team.

## Shell & Terminal

- [tom-doerr/zsh_codex](https://github.com/tom-doerr/zsh_codex) - Zsh plugin for AI-powered command completion using Codex. ![GitHub stars](https://img.shields.io/github/stars/tom-doerr/zsh_codex?style=flat-square)
- [gravtice/ohmyzsh-ai-cli-plugins](https://github.com/gravtice/ohmyzsh-ai-cli-plugins) - Oh My Zsh plugins for AI coding agents. ![GitHub stars](https://img.shields.io/github/stars/gravtice/ohmyzsh-ai-cli-plugins?style=flat-square)
- [sadjow/codex-cli-nix](https://github.com/sadjow/codex-cli-nix) - Nix flake for reproducible Codex CLI installation. ![GitHub stars](https://img.shields.io/github/stars/sadjow/codex-cli-nix?style=flat-square)
- [kunal12203/Codex-CLI-Compact](https://github.com/kunal12203/Codex-CLI-Compact) - Stripped-down Codex binary. Smaller install, faster startup. ![GitHub stars](https://img.shields.io/github/stars/kunal12203/Codex-CLI-Compact?style=flat-square)
- [tom-doerr/codex.fish](https://github.com/tom-doerr/codex.fish) - Fish shell plugin for AI-powered command completion using Codex. ![GitHub stars](https://img.shields.io/github/stars/tom-doerr/codex.fish?style=flat-square)

## Remote Access

- [K9i-0/ccpocket](https://github.com/K9i-0/ccpocket) - Access Codex from mobile devices via web UI. ![GitHub stars](https://img.shields.io/github/stars/K9i-0/ccpocket?style=flat-square)
- [MackDing/CodexClaw](https://github.com/MackDing/CodexClaw) - Telegram bot that proxies commands to a remote Codex instance. ![GitHub stars](https://img.shields.io/github/stars/MackDing/CodexClaw?style=flat-square)
- [chuvadenovembro/script-to-use-codex-cli-on-remote-server](https://github.com/chuvadenovembro/script-to-use-codex-cli-on-remote-server-without-visual-environment) - Headless server setup guide with auth workarounds. ![GitHub stars](https://img.shields.io/github/stars/chuvadenovembro/script-to-use-codex-cli-on-remote-server-without-visual-environment?style=flat-square)
- [Emanuele-web04/remodex](https://github.com/Emanuele-web04/remodex) - Local-first iOS app + Mac bridge for remote Codex control. Encrypted sessions, git integration, App Store available. ![GitHub stars](https://img.shields.io/github/stars/Emanuele-web04/remodex?style=flat-square)

---

## Contributing

Contributions welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the authors have waived all copyright and related or neighboring rights to this work.
