# ORAC-OS Examples

This folder contains working demos to illustrate **how ORAC-OS subsystems are used**.

## Agents
- **hello_agent.c** – Minimal “Hello, World” agent using semantic calls.
- **insight_bot.c** – Example agent that interacts with persistent memory, queries embeddings, and reports insights.

## Memory
- **memory_store.c** – Demonstrates how to store embeddings and metadata.
- **memory_query.c** – Query semantic memory using API functions.

## CLI
- **demo_script.cli** – Hybrid command & natural language session.
  ```bash
  orac> list agents
  orac> show me all memory items about "Thorac"
  orac> deploy agent insight_bot to node alpha
