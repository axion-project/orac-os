# ORAC-OS CLI

The ORAC-OS CLI is an **LLM-native command line interface** that blends classic shell power with semantic understanding.

## Features
- **Hybrid Input:** Accepts structured commands (`agent list`) and natural language (`show me active agents`).
- **Semantic Parsing:** Uses the same API/syscall layer to execute commands in context.
- **Pluggable Commands:** Dynamically extend with new verbs and agent actions.
- **Rich UX:** History, auto-complete, colored output, contextual suggestions.
- **Scripting:** Can run .cli scripts with semantic or traditional commands.

## Architecture
- **parser.c:** Tokenizes & interprets NL or command input.
- **executor.c:** Dispatches commands to `/api/syscalls.c`.
- **prompt.c:** Interactive REPL with hints and dynamic completions.
- **plugins.c:** Loadable command modules.

## Roadmap
- [ ] Add semantic parsing using embeddings/context
- [ ] Secure CLI sessions with cryptographic identity
- [ ] Support multi-node commands (`agent deploy --node=thorac`)
- [ ] Develop scripting DSL for automation

## Example Usage
