# ORAC-OS Memory Layer

ORAC-OS memory isn't just bytes; it's **contextual cognition storage**.

## Key Concepts
- **Semantic Persistence:** Memory stores not only data but also context vectors for AI agents.
- **Hot/Warm/Cold Tiering:** Data automatically migrates between tiers based on recency, frequency, and semantic relevance.
- **Distributed Awareness:** Memory spans multiple nodes; local + remote embedding stores supported.
- **Secure & Signed:** All persistent data is cryptographically signed; tampering is detected.

## Components
- **memory_manager.c:** Base runtime allocator, tied to semantic metadata.
- **tiering.c:** Implements automated movement between tiers.
- **embeddings_store.c:** Interfaces with a vector DB or in-memory ANN index.
- **persistence.c:** Handles local & remote persistent storage sync.
- **gc.c:** Garbage collector aware of semantic importance, not just LRU.

## Roadmap
- [ ] Implement embedding-aware allocation API.
- [ ] Add local vector index with ANN (Approximate Nearest Neighbor).
- [ ] Build distributed persistence hooks (peer-to-peer).
- [ ] Integrate encryption & signing for zero-trust persistence.
- [ ] Add semantic cache prefetching for agents.

## Example Use
Agents can:
1. Allocate semantic memory with embeddings.
2. Query context by meaning, not just key.
3. Persist across nodes and rehydrate context on demand.
