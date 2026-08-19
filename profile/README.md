# Javier Mellado

**Solo builder. I orchestrate fleets of AI agents to ship software, and I create the tooling that makes that work.**

Agentic engineer in Edinburgh, 21 years writing code. These days I spend less time typing and more time at the level above the code: planning, reviewing, merging, and designing the systems that let a fleet of agents work together. Local-first whenever it is feasible.

## The system

**🪨 [La Roca](https://github.com/thellmwhisperer/la-roca)**  
Local semantic memory for agent fleets. One Go binary, one SQLite file, zero dependencies: it ingests every session your agents leave on the machine (Claude, Codex, Pi, OpenCode, Hermes, even your claude.ai export) and answers natural-language questions about it, with per-answer provenance: which model said it, how much it thought, what it cost. Agents plug in over MCP and stop starting from zero. No login: it reuses the agent CLIs already installed. Private by construction; nothing leaves your machine.

**🤖 [combo-chen](https://github.com/thellmwhisperer/combo-chen)**  
Deterministic harness for autonomous issue-to-PR pipelines. An event-sourced state machine drives fixed roles (coder, gatekeeper, reviewer) with strict role separation, SHA-pinned review gates, CI reconciliation, and a human-in-the-loop merge. Built on git worktrees and tmux.

**☁️ [roca-cloud](https://github.com/thellmwhisperer/roca-cloud)**  
MCP-native memory store deployed on AWS as a single ARM64 Lambda behind API Gateway, backed by private RDS PostgreSQL and Secrets Manager, provisioned end-to-end with CDK. Roca Cloud is its own durable memory plane: Bedrock and AgentCore workloads run around it, as agents, distillers, runners, and observability pipelines, all reading from and writing to the same shared memory.

**🛡️ [human.md](https://github.com/thellmwhisperer/human.md)**  
A guardrail framework for human-agent pairing: declarative rules that tell a coding agent when to defer, stop, or hand back control, enforced through hooks.

**🧹 [slopslint](https://github.com/thellmwhisperer/slopslint)**  
Blocking slop gate for AI-assisted repos: duplication detector, tombstones, ceiling ratchet. Extracted from roca-madre.

**🎯 [quick-fire](https://github.com/thellmwhisperer/quick-fire)**  
Keep your agent focused, not rambling.

## Applied AI

**🎥 [conferenceDB](https://github.com/thellmwhisperer/conferenceDB)**  
Agent-native RAG over conference talks. Hybrid retrieval over SQLite FTS5 full-text search and sqlite-vec vector embeddings, fully local. Turns video transcripts into a queryable knowledge base.

**🏠 [land-registry-nlq](https://github.com/thellmwhisperer/land-registry-nlq)**  
Text-to-SQL over 31M UK Land Registry transactions. Plain-English questions compiled to PostgreSQL and validated against the query AST (libpg-query) before execution, with Claude Haiku in the loop.

**🎬 [twitch-toolkit](https://github.com/teseo/twitch-toolkit)**  
End-to-end pipeline that turns a multi-hour stream VOD into publishable content. Whisper transcribes speech while ACRCloud detects music and Demucs separates audio, then an LLM scores segments for highlights by context not audio peaks before chapters and SEO are pushed to YouTube automatically. Multi-LLM by design: DeepSeek, OpenAI, Groq and OpenRouter, with a local-first path through Ollama.

## How I work

- I design the system and the guardrails, then let agents execute inside them.
- Local-first. I run models on my own hardware (Ollama, MLX) when it is feasible.
- Tests and review are not optional. Determinism, gates, and a human merge decision are baked into how my agents ship.

## Skills

- Agent fleet orchestration: six frontier models plus local ones, working in parallel under supervision.
- Natural language to structured systems: SQL, git logs, Playwright tests, Bazel queries.
- AI-assisted delivery pipelines: review gates, slop detection, deterministic issue-to-PR flows.
- Token economics: choosing the right model tier per task, and knowing when a 65KB classifier beats a frontier call.
- Sovereign AI: local models, private memory, intelligence without your data leaving your machines.
- Team enablement: prompt and context training, agentic workflow installation, AI review tooling.

## Tooling

Go · TypeScript · Python · Node · React / React Native · SQLite · MCP. Claude, Codex, Pi, OpenCode, Hermes, and local models via Ollama and MLX.

## Videos

[The LLM Whisperer on YouTube](https://youtube.com/@thellmwhisperer): building with agent fleets, in public. Live demos, real sessions, what works and what doesn't.

[LinkedIn](https://www.linkedin.com/in/javier-mellado-10545ba/) · [Activity](https://github.com/teseo)

---

<p align="center">
  🎵 Multi-instrumentalist · 🌧️ Scottish weather lover
</p>
