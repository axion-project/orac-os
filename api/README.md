# ORAC-OS API Layer

The API layer provides **semantic system calls** and **network interfaces** for ORAC-OS.
Unlike classic OS APIs, ORAC-OS APIs are **meaning-aware** and integrate with LLM/agent workflows.

## Goals
- Provide both **programmatic** (C, RPC, gRPC) and **semantic** (natural language) interfaces.
- Support **local + distributed** calls across ORAC-OS nodes.
- Enforce **security** at the API boundary (cryptographic IDs and signed requests).
- Be **extensible** — new syscalls can be added without breaking the interface.

## Core Components
- **syscalls.c:** Dispatches semantic and structured API calls to the kernel.
- **rest_gateway.c:** REST/gRPC endpoints for external clients.
- **cli_interface.c:** LLM-native prompt shell; commands can be NL or structured.
- **rpc_server.c:** Distributed node API for orac-node integration.

## Example API Flow
1. An agent issues: `store_context("Project Thorac", embedding_vector)`.
2. The API routes it to `memory_api.h` → `memory_manager.c` with cryptographic auth.
3. Semantic syscalls allow natural language: `api.execute("retrieve insights on Thorac")`.

## Roadmap
- [ ] Define core syscall interface (semantic + structured)
- [ ] Add gRPC/REST for external clients
- [ ] Secure APIs with signed tokens + zero-trust
- [ ] CLI prompt shell with hybrid NL/command input
