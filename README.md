# Awesome Codex CLI [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of awesome tools, skills, subagents, plugins, and resources for [OpenAI Codex CLI](https://github.com/openai/codex) — the open-source coding agent that runs in your terminal.

Codex CLI lets you use OpenAI models to write, refactor, and reason about code directly from the command line — with sandboxed execution, multi-agent orchestration, and a growing ecosystem of skills and plugins.

**Why this list?** The Codex ecosystem is fragmented across dozens of repos. This list consolidates the best resources into one place, with opinionated descriptions so you know what's actually worth your time.

---

## Latest Additions

<!-- Keep this section to ~5 items, rotate as new entries are added -->

| Date | Entry | Category |
|------|-------|----------|
| 2026-03-31 | Initial launch | - |

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

---

## Official Resources

- [Codex CLI GitHub](https://github.com/openai/codex) — The source. Rust-based, Apache-2.0. Start here.
- [Documentation](https://developers.openai.com/codex) — Official docs covering setup, config, security, and all features.
- [Config Reference](https://developers.openai.com/codex/config-reference) — All 85+ config properties for `config.toml`.
- [Skills Docs](https://developers.openai.com/codex/skills) — How to create and use SKILL.md files.
- [Subagents Docs](https://developers.openai.com/codex/subagents) — Multi-agent orchestration with `.toml` agent definitions.
- [Plugins Docs](https://developers.openai.com/codex/plugins) — Distributable bundles of skills + apps + MCP servers.
- [MCP Docs](https://developers.openai.com/codex/mcp) — Using Codex as MCP client and server.
- [Hooks Docs](https://developers.openai.com/codex/hooks) — User-defined shell scripts in the agentic loop (beta).
- [Security & Sandboxing](https://developers.openai.com/codex/security) — Seatbelt (macOS), Landlock/Bubblewrap (Linux), restricted-token (Windows).
- [Non-interactive Mode](https://developers.openai.com/codex/noninteractive) — `codex exec` for CI/CD and scripting.
- [Slash Commands](https://developers.openai.com/codex/cli/slash-commands) — All 29 built-in commands: `/plan`, `/skills`, `/fast`, `/fork`, `/review`, etc.
- [Best Practices](https://developers.openai.com/codex/learn/best-practices) — Official tips for getting the most out of Codex.
- [Multi-Agent Guide](https://developers.openai.com/codex/multi-agent/) — Parallel fan-out, `max_threads`, depth control.
- [Workflows](https://developers.openai.com/codex/workflows/) — Automation recipes and patterns.
- [Exec Policy](https://developers.openai.com/codex/exec-policy) — Starlark-based fine-grained permission rules.
- [Speed / Fast Mode](https://developers.openai.com/codex/speed) — 1.5x speed, 2x credits.
- [AGENTS.md Guide](https://developers.openai.com/codex/guides/agents-md) — Project-level instructions for Codex.
- [Codex Universal (Docker)](https://github.com/openai/codex-universal) — Official base Docker image for containerized Codex.
- [Codex Web](https://chatgpt.com/codex) — Cloud-hosted Codex via ChatGPT.
- [VS Code Extension](https://marketplace.visualstudio.com/items?itemName=openai.chatgpt) — Official IDE integration.
- [Codex for OSS Fund](https://openai.com/form/codex-for-oss/) — Free Codex access for open-source maintainers.

## Getting Started

- [DataCamp Tutorial](https://www.datacamp.com/tutorial/open-ai-codex-cli-tutorial) — Beginner-friendly walkthrough with screenshots. Good first read.
- [Blott Studio Guide](https://www.blott.studio/blog/post/openai-codex-cli-build-faster-code-right-from-your-terminal) — Practical getting-started guide focused on real development workflow.
- [Medium Quick Setup](https://medium.com/ai-software-engineer/how-to-install-and-use-openai-codex-cli-in-2-minutes-29e9fdd0e8c5) — 2-minute install-to-first-prompt guide. No fluff.
- [OpenReplay Integration Guide](https://blog.openreplay.com/integrate-openais-codex-cli-tool-development-workflow/) — How to weave Codex into an existing dev workflow.
- [Machine Learning Mastery](https://machinelearningmastery.com/understanding-openai-codex-cli-commands/) — Command reference with examples for each mode.

## AGENTS.md Templates

Project-level instruction files that tell Codex how to work with your codebase — the equivalent of Claude Code's `CLAUDE.md`.

- [agents.md (Open Standard)](https://agents.md) — The cross-agent standard used by 20k+ projects. Works with Codex, Claude Code, Gemini CLI, and more.
- [codex-cli-best-practice](https://github.com/shanraisshan/codex-cli-best-practice) — Battle-tested AGENTS.md patterns with sandbox mode recommendations and approval policies. ⭐ 315
- [codex-settings (feiskyer)](https://github.com/feiskyer/codex-settings) — Curated config + AGENTS.md for multi-provider setups (LiteLLM, Ollama, OpenRouter). ⭐ 166
- [claude-codex-settings](https://github.com/fcakyon/claude-codex-settings) — Dual AGENTS.md + CLAUDE.md setup for teams running both agents side-by-side. ⭐ 554
- [caliber-ai-org/ai-setup](https://github.com/caliber-ai-org/ai-setup) — Cross-tool config generator — outputs AGENTS.md, CLAUDE.md, and .cursorrules from one source. ⭐ 308

## Subagents

Multi-agent orchestration with `.toml` definitions. Codex supports parallel fan-out with up to 6 threads by default.

### Collections

- [VoltAgent/awesome-codex-subagents](https://github.com/VoltAgent/awesome-codex-subagents) — The definitive collection. 136+ agents across 10 categories (core dev, language specialists, infra, security, data/AI, DX, domains, business, meta, orchestration). Just clone and use. ⭐ 3,144
- [betterup/codex-cli-subagents](https://github.com/betterup/codex-cli-subagents) — Enterprise-focused agents for code review, migration, and compliance. ⭐ 17

### Specialized Subagents

- [leonardsellem/codex-specialized-subagents](https://github.com/leonardsellem/codex-specialized-subagents) — Niche agents: accessibility auditor, i18n extractor, performance profiler. Fills gaps VoltAgent doesn't cover. ⭐ 58
- [CoderMageFox/claudecode-codex-subagents](https://github.com/CoderMageFox/claudecode-codex-subagents) — Agents that work across both Codex and Claude Code. Good for mixed teams. ⭐ 41
- [Alexin09/cc-subagent-codex](https://github.com/Alexin09/cc-subagent-codex) — Lightweight subagent pack focused on TypeScript/React projects. ⭐ 12

### Multi-Agent Orchestration

- [basilisk-labs/codex-swarm](https://github.com/basilisk-labs/codex-swarm) — Swarm intelligence pattern — multiple Codex agents collaborating on large refactors. ⭐ 57
- [aannoo/hcom](https://github.com/aannoo/hcom) — Hierarchical agent communication framework. Agents delegate subtasks with context preservation. ⭐ 177
- [obra/external-subagents](https://github.com/obra/external-subagents) — Run subagents as external processes with custom sandboxing. ⭐ 20

## Skills

Reusable instruction bundles in `SKILL.md` format. Place in `~/.codex/skills/` (global) or `.agents/skills/` (project).

### Collections

- [ComposioHQ/awesome-codex-skills](https://github.com/ComposioHQ/awesome-codex-skills) — 38 skills across dev tools, productivity, communication, data analysis. Heavy Composio integration for 1000+ SaaS apps. ⭐ 562
- [heilcheng/awesome-agent-skills](https://github.com/heilcheng/awesome-agent-skills) — Cross-platform skills that work in Codex, Claude Code, and Gemini CLI. ⭐ 3,518
- [Prat011/awesome-llm-skills](https://github.com/Prat011/awesome-llm-skills) — Platform-agnostic skills organized by use case. ⭐ 1,046
- [skillmatic-ai/awesome-agent-skills](https://github.com/skillmatic-ai/awesome-agent-skills) — Community-driven skill marketplace with quality ratings. ⭐ 483
- [proflead/codex-skills-library](https://github.com/proflead/codex-skills-library) — Focused collection: code review, git workflow, documentation generation. ⭐ 71

### Specialized Skills

- [huggingface/upskill](https://github.com/huggingface/upskill) — HuggingFace's official skill pack for ML/AI development workflows. ⭐ 451
- [Mukul975/Anthropic-Cybersecurity-Skills](https://github.com/mukul975/Anthropic-Cybersecurity-Skills) — Security-focused skills: vulnerability scanning, dependency auditing, OWASP checks. Works in Codex too despite the name. ⭐ 3,895
- [nicepkg/ai-workflow](https://github.com/nicepkg/ai-workflow) — Workflow automation skills — chained multi-step tasks with conditional logic. ⭐ 148
- [cathrynlavery/codex-skill](https://github.com/cathrynlavery/codex-skill) — Clean, well-documented single-purpose skills. Good reference for writing your own. ⭐ 136
- [Karanjot786/agent-skills-cli](https://github.com/Karanjot786/agent-skills-cli) — CLI tool to discover, install, and manage skills from the community. ⭐ 104

### Domain-Specific Skills

- [aklofas/kicad-happy](https://github.com/aklofas/kicad-happy) — KiCad PCB design assistant. Proof that skills can go deep into niche domains. ⭐ 115
- [qtzx06/yolodex](https://github.com/qtzx06/yolodex) — Computer vision / YOLO model training workflow. ⭐ 79
- [Frankieli123/grok-skill](https://github.com/Frankieli123/grok-skill) — Log analysis and pattern matching. Useful for debugging production issues. ⭐ 143

## Plugins

Distributable bundles combining skills + app integrations + MCP servers. Defined in `.codex-plugin/plugin.json`. Browse with `/plugins`.

- [hashgraph-online/awesome-codex-plugins](https://github.com/hashgraph-online/awesome-codex-plugins) — The first plugin directory. Lists 12 official + ~20 community plugins with install instructions. ⭐ 11
- [agent-sh/agentsys](https://github.com/agent-sh/agentsys) — Plugin framework with dependency resolution and version management. ⭐ 679
- [xmm/codex-bmad-skills](https://github.com/xmm/codex-bmad-skills) — BMAD methodology plugin — structured planning, design, and implementation workflow.

## Hooks

User-defined shell scripts that run at specific points in the agentic loop. Requires `codex_hooks = true` feature flag.

- [shanraisshan/codex-cli-hooks](https://github.com/shanraisshan/codex-cli-hooks) — Starter hooks collection: pre-commit validation, cost tracking, notification triggers. ⭐ 23
- [liewcf/codex-notify-macos](https://github.com/liewcf/codex-notify-macos) — macOS notification hook — get alerted when long-running tasks complete. ⭐ 1

## MCP Servers

Codex can connect to MCP servers (as client) and expose itself as an MCP server (`codex mcp-server`).

### Codex as MCP Client

- [tuannvm/codex-mcp-server](https://github.com/tuannvm/codex-mcp-server) — General-purpose MCP server for Codex with file operations, web search, and database queries. ⭐ 381
- [FYZAFH/mcp-codex-dev](https://github.com/FYZAFH/mcp-codex-dev) — Development-focused MCP server: linting, testing, deployment tools. ⭐ 162
- [cexll/codex-mcp-server](https://github.com/cexll/codex-mcp-server) — Lightweight MCP server with minimal dependencies. Good starting point for custom servers. ⭐ 161
- [Wildcard-Official/deepcontext-mcp](https://github.com/Wildcard-Official/deepcontext-mcp) — Codebase understanding server — builds semantic index for smarter code navigation. ⭐ 273
- [DeusData/codebase-memory-mcp](https://github.com/DeusData/codebase-memory-mcp) — Persistent project memory across sessions. Codex remembers decisions, patterns, and context. ⭐ 1,087
- [Shelpuk-AI-Technology-Consulting/kindly-web-search-mcp-server](https://github.com/Shelpuk-AI-Technology-Consulting/kindly-web-search-mcp-server) — Web search MCP with rate limiting and caching. ⭐ 254
- [milisp/mcp-linker](https://github.com/milisp/mcp-linker) — Link multiple MCP servers together. Chain tools across servers. ⭐ 298

### Codex as MCP Server

- [leonardsellem/codex-subagents-mcp](https://github.com/leonardsellem/codex-subagents-mcp) — Expose Codex subagents as MCP tools. Other agents (Claude Code, Cursor) can call Codex agents. ⭐ 154
- [Mr-Tomahawk/codex-cli-mcp-tool](https://github.com/Mr-Tomahawk/codex-cli-mcp-tool) — Wrap Codex CLI as an MCP tool for use in other agent frameworks. ⭐ 19
- [agency-ai-solutions/openai-codex-mcp](https://github.com/agency-ai-solutions/openai-codex-mcp) — Full-featured Codex MCP bridge with streaming support. ⭐ 52

### General-Purpose MCP

- [PleasePrompto/notebooklm-mcp](https://github.com/PleasePrompto/notebooklm-mcp) — Connect Codex to NotebookLM for research-augmented coding. ⭐ 1,710

## IDE & Editor Integrations

- [VS Code Extension (Official)](https://marketplace.visualstudio.com/items?itemName=openai.chatgpt) — The official extension. Inline chat, terminal integration, code actions.
- [johnseth97/codex.nvim](https://github.com/johnseth97/codex.nvim) — Neovim plugin with floating terminal, keybindings, and context passing. ⭐ 208
- [milanglacier/yarepl.nvim](https://github.com/milanglacier/yarepl.nvim) — REPL framework for Neovim. Supports Codex as a REPL target alongside Python, R, etc. ⭐ 247
- [xenodium/agent-shell](https://github.com/xenodium/agent-shell) — Emacs integration that works with Codex, Claude Code, and other terminal agents. Best-in-class Emacs experience. ⭐ 971
- [tninja/ai-code-interface.el](https://github.com/tninja/ai-code-interface.el) — Emacs interface for multiple AI coding agents including Codex. ⭐ 186
- [bennfocus/codex-cli.el](https://github.com/bennfocus/codex-cli.el) — Lightweight Emacs wrapper. Minimal, focused. ⭐ 24
- [dliedke/ClaudeCodeExtension](https://github.com/dliedke/ClaudeCodeExtension) — Visual Studio .NET extension that supports both Claude Code and Codex CLI. ⭐ 58
- [smallmain/vscode-unify-chat-provider](https://github.com/smallmain/vscode-unify-chat-provider) — Unify multiple AI agents (Codex, Claude, Copilot) under one VS Code chat interface. ⭐ 307

## GUI & Desktop Apps

- [milisp/codexia](https://github.com/milisp/codexia) — Desktop GUI for Codex CLI. macOS/Windows/Linux. Visual session management, file tree, diff viewer. ⭐ 521
- [xintaofei/codeg](https://github.com/xintaofei/codeg) — Electron-based GUI with project templates and one-click sandboxing. ⭐ 513
- [K9i-0/ccpocket](https://github.com/K9i-0/ccpocket) — Mobile-friendly web UI. Run Codex from your phone via remote server. ⭐ 470
- [nkmr-jp/prompt-line](https://github.com/nkmr-jp/prompt-line) — Minimal prompt-centric UI. Stays out of your way. ⭐ 143
- [Lampese/codex-switcher](https://github.com/Lampese/codex-switcher) — Quick-switch between multiple Codex sessions and configurations. ⭐ 116
- [zhu1090093659/CodeConductor](https://github.com/zhu1090093659/CodeConductor) — Orchestrator GUI for managing multiple Codex agents visually. ⭐ 72

## Session & Workflow Management

- [UfoMiao/zcf](https://github.com/UfoMiao/zcf) — Zero-config workflow framework. Chain prompts, branch on results, auto-retry failures. ⭐ 5,837
- [gotalab/cc-sdd](https://github.com/gotalab/cc-sdd) — Spec-driven development workflow. Write specs, Codex implements, auto-validates against spec. ⭐ 2,999
- [covibes/zeroshot](https://github.com/covibes/zeroshot) — Zero-shot task runner. Describe what you want in plain English, get a working codebase. ⭐ 1,384
- [waskosky/codex-cli-farm](https://github.com/waskosky/codex-cli-farm) — Run multiple Codex instances in parallel on different tasks. Session isolation built-in. ⭐ 25
- [joseferben/hands-please](https://github.com/joseferben/hands-please) — Human-in-the-loop workflow. Codex pauses at decision points and asks for your input. ⭐ 32
- [onurkanbakirci/awesome-codex-automations](https://github.com/onurkanbakirci/awesome-codex-automations) — Automation recipes for CI/CD, code quality, release management, and team communication. ⭐ 20

## Model Providers & Proxies

Codex supports `openai_base_url` for custom model providers. Use any OpenAI-compatible API.

- [feiskyer/codex-settings](https://github.com/feiskyer/codex-settings) — Ready-to-use configs for LiteLLM, Ollama, LM Studio, OpenRouter, and Azure OpenAI. ⭐ 166
- [teabranch/open-responses-server](https://github.com/teabranch/open-responses-server) — OpenAI Responses API-compatible server. Run Codex with local models. ⭐ 153
- [erans/lunaroute](https://github.com/erans/lunaroute) — Model router with cost tracking, rate limiting, and fallback chains. ⭐ 154
- [ben-vargas/ai-sdk-provider-codex-cli](https://github.com/ben-vargas/ai-sdk-provider-codex-cli) — Vercel AI SDK provider for Codex. Use Codex in your AI applications. ⭐ 35
- [numman-ali/opencode-openai-codex-auth](https://github.com/numman-ali/opencode-openai-codex-auth) — Auth proxy to use ChatGPT Plus subscription with third-party tools. ⭐ 1,871

## CI/CD & Automation

Use `codex exec` for non-interactive automation in pipelines.

- [onurkanbakirci/awesome-codex-automations](https://github.com/onurkanbakirci/awesome-codex-automations) — 35 automation recipes organized by category: code quality, CI/CD, releases, deps, security. ⭐ 20
- [openai/codex-universal](https://github.com/openai/codex-universal) — Official Docker base image. Designed for CI/CD runners and cloud environments.

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

- [DeepMyst/Mysti](https://github.com/DeepMyst/Mysti) — Universal agent orchestrator. Route tasks between Codex, Claude Code, and Gemini CLI based on model strengths. ⭐ 1,025
- [athola/skrills](https://github.com/athola/skrills) — Cross-platform skill format. Write once, use in Codex and Claude Code. ⭐ 57
- [jcputney/agent-peer-review](https://github.com/jcputney/agent-peer-review) — Codex reviews Claude Code's output (and vice versa). Catches model-specific blind spots. ⭐ 26
- [abhishekgahlot2/codex-claude-bridge](https://github.com/abhishekgahlot2/codex-claude-bridge) — Run Codex and Claude Code in tandem on the same codebase. ⭐ 24
- [lbb00/ai-rules-sync](https://github.com/lbb00/ai-rules-sync) — Sync AGENTS.md ↔ CLAUDE.md ↔ .cursorrules. One source, all formats. ⭐ 22
- [sypsyp97/claude-skill-codex](https://github.com/sypsyp97/claude-skill-codex) — Run Codex CLI as a Claude Code skill. ⭐ 36

## Monitoring & Analytics

- [NihilDigit/waybar-ai-usage](https://github.com/NihilDigit/waybar-ai-usage) — Waybar widget showing real-time Codex token usage and costs. Linux desktop integration. ⭐ 29
- [yoavf/ai-sessions-mcp](https://github.com/yoavf/ai-sessions-mcp) — MCP server that tracks session history, token usage, and cost across agents. ⭐ 23
- [HizTam/codex-history-viewer](https://github.com/HizTam/codex-history-viewer) — Browse and search past Codex sessions with full context. ⭐ 3

## Docker & Sandboxing

- [openai/codex-universal](https://github.com/openai/codex-universal) — Official Docker base image. Pre-configured sandbox, multi-language support.
- [chuvadenovembro/script-to-use-codex-cli-on-remote-server](https://github.com/chuvadenovembro/script-to-use-codex-cli-on-remote-server-without-visual-environment) — Run Codex on headless servers. Handles auth without a browser. ⭐ 38

## Account & Auth

- [numman-ali/opencode-openai-codex-auth](https://github.com/numman-ali/opencode-openai-codex-auth) — Use your ChatGPT Plus/Pro subscription as a Codex auth source. The most popular auth tool. ⭐ 1,871
- [Lampese/codex-switcher](https://github.com/Lampese/codex-switcher) — Switch between multiple OpenAI accounts. Useful for work/personal separation. ⭐ 116
- [bashar94/codex-cli-account-switcher](https://github.com/bashar94/codex-cli-account-switcher) — Simple account switcher with profile support. ⭐ 64
- [bddiudiu/cpa-codex-auth-sweep-cliproxy](https://github.com/bddiudiu/cpa-codex-auth-sweep-cliproxy) — Auth proxy for enterprise SSO environments. ⭐ 27

## Tutorials & Articles

- [How Codex is Built (Pragmatic Engineer)](https://newsletter.pragmaticengineer.com/p/how-codex-is-built) — Deep technical dive into Codex's architecture. Rust, sandboxing, the TUI. Essential reading.
- [Dogfood: Codex Builds Codex (Stack Overflow)](https://stackoverflow.blog/2026/02/24/dogfood-so-nutritious-it-s-building-the-future-of-sdlcs/) — How the Codex team uses their own tool. Real-world workflow patterns.
- [How Codex Team Uses Their Agent (Every)](https://every.to/podcast/transcript-how-openai-s-codex-team-uses-their-coding-agent) — Transcript of the team discussing daily usage, tips, and antipatterns.
- [Why Humans are AI's Biggest Bottleneck (Lenny's Newsletter)](https://www.lennysnewsletter.com/p/why-humans-are-ais-biggest-bottleneck) — Broader perspective on AI coding agents, with Codex as a case study.
- [Apidog: OpenAI Codex CLI](https://apidog.com/blog/openai-codex-cli/) — API-focused guide. Good for integrating Codex into existing toolchains.

## Videos & Podcasts

*Know a great video or podcast episode about Codex CLI? [Submit it!](https://github.com/user/awesome-codex-cli/issues/new)*

## Comparisons

### Codex CLI vs Claude Code vs Gemini CLI

| Feature | Codex CLI | Claude Code | Gemini CLI |
|---------|-----------|-------------|------------|
| **Language** | Rust | TypeScript | Python |
| **License** | Apache-2.0 | Proprietary | Apache-2.0 |
| **Config file** | `config.toml` | `settings.json` | `settings.json` |
| **Project instructions** | `AGENTS.md` | `CLAUDE.md` | `GEMINI.md` |
| **Sandbox** | Seatbelt/Landlock/Bubblewrap | macOS Seatbelt, Linux containers | Docker-based |
| **Multi-agent** | Built-in (6 parallel threads) | Subagent spawning | Limited |
| **Skills** | `SKILL.md` files | Slash-command skills | N/A |
| **Plugins** | `.codex-plugin/` bundles | N/A | N/A |
| **Hooks** | Shell scripts (beta) | Pre/post hooks | N/A |
| **MCP support** | Client + Server | Client only | Client only |
| **IDE** | VS Code, Neovim, Emacs, Zed | VS Code, JetBrains | VS Code |
| **Auth** | ChatGPT sub or API key | Anthropic API key | Google account |
| **Models** | GPT-5.x, o-series | Claude 4.x | Gemini 2.x |
| **Non-interactive** | `codex exec` | `claude -p` | `gemini exec` |

### Related Comparisons

- [Hacker News Discussion](https://news.ycombinator.com/item?id=43708025) — Community comparison thread with real-world experiences.
- [Reddit AMA with Codex Team](https://www.reddit.com/r/ChatGPT/comments/1ko3tp1/ama_with_openai_codex_team/) — Team answers questions about design decisions and how Codex differs from alternatives.
- [duanyytop/agents-radar](https://github.com/duanyytop/agents-radar) — Side-by-side benchmark of terminal AI agents on real coding tasks. ⭐ 560

## Community

- [GitHub Discussions](https://github.com/openai/codex/discussions) — Official discussion forum. Feature requests, bug reports, tips.
- [Reddit r/ChatGPT](https://www.reddit.com/r/ChatGPT/) — Active discussions about Codex CLI in the broader ChatGPT community.
- [OpenAI Developer Forum](https://community.openai.com/) — Official OpenAI community with Codex-specific threads.
- [@OpenAIDevs on X](https://x.com/OpenAIDevs) — Official announcements and tips.

### People to Follow

Codex CLI team members and frequent contributors:

- [@thsottiaux](https://x.com/thsottiaux) — Tibo, Codex team
- [@embirico](https://x.com/embirico) — Embiricos, Codex team
- [@jxnlco](https://x.com/jxnlco) — Jason, Codex team
- [@romainhuet](https://x.com/romainhuet) — Romain Huet, OpenAI DevRel
- [@dkundel](https://x.com/dkundel) — Dominik Kundel, OpenAI DevRel
- [@fouadmatin](https://x.com/fouadmatin) — Fouad Matin, Codex team
- [@bolinfest](https://x.com/bolinfest) — Bolin Fest, Codex team

## Shell & Terminal

- [tom-doerr/zsh_codex](https://github.com/tom-doerr/zsh_codex) — Zsh plugin for AI-powered command completion using Codex. ⭐ 1,716
- [gravtice/ohmyzsh-ai-cli-plugins](https://github.com/gravtice/ohmyzsh-ai-cli-plugins) — Oh My Zsh plugins for AI coding agents. ⭐ 12
- [sadjow/codex-cli-nix](https://github.com/sadjow/codex-cli-nix) — Nix flake for reproducible Codex CLI installation. ⭐ 69
- [kunal12203/Codex-CLI-Compact](https://github.com/kunal12203/Codex-CLI-Compact) — Stripped-down Codex binary. Smaller install, faster startup. ⭐ 218

## Remote Access

- [K9i-0/ccpocket](https://github.com/K9i-0/ccpocket) — Access Codex from mobile devices via web UI. ⭐ 470
- [MackDing/CodexClaw](https://github.com/MackDing/CodexClaw) — Telegram bot that proxies commands to a remote Codex instance. ⭐ 19
- [chuvadenovembro/script-to-use-codex-cli-on-remote-server](https://github.com/chuvadenovembro/script-to-use-codex-cli-on-remote-server-without-visual-environment) — Headless server setup guide with auth workarounds. ⭐ 38

---

## Contributing

Contributions welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the authors have waived all copyright and related or neighboring rights to this work.
