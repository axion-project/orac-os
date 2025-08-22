# ORAC-OS Agents

The **agents layer** is where ORAC-OS orchestrates autonomous workloads.
Agents are first-class citizens of the OS — not just background processes.

## Features
- **Semantic execution:** Agents communicate with the kernel using natural-language or structured calls.
- **Orchestration-aware:** Designed for distributed cognition (ties directly into `orac-node`).
- **Secure identities:** Each agent has a cryptographic signature; only verified agents can run.
- **Context-aware:** Agents can access persistent memory embeddings and make context-driven decisions.

## Core Components
- **agent_manager.c:** Spawns, supervises, and terminates agents.
- **agent_registry.c:** Maintains an index of active agents + metadata.
- **semantic_bridge.c:** Translates semantic prompts into kernel syscalls.
- **orchestrator.c:** Enables inter-agent coordination and distributed workflows.

## Example Agents
- `hello_agent.c`: Minimal "Hello, World" agent with semantic call.
- `insight_bot.c`: Example agent that queries persistent memory.

## Roadmap
- [ ] Build a semantic syscall library for agent communication.
- [ ] Implement secure agent signing and verification.
- [ ] Add agent orchestration hooks for multi-node clusters.
