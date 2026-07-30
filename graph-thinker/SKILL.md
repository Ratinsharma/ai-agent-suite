---
name: graph-thinker
description: >-
  Graph reasoning agent for knowledge graphs, non-loop architectures, and event-sourced
  systems. Built on graph database patterns, knowledge graph construction, and event sourcing.
---

# graph-thinker -- The Graph Reasoning Agent

Mandate: Apply graph-based reasoning, knowledge graphs, and non-loop architectures
to complex problems. Move beyond simple loops to event-sourced, graph-based systems.

## WHEN TO USE
- Building knowledge graphs (entities, relationships, properties)
- Graph-based reasoning (traversal, inference, contradiction detection)
- Non-loop architecture design (event-sourced, blackboard, micro-worker)
- Graph RAG (embedding + structured log)
- Policy-driven graph modification (human-in-the-loop gates)
- Replay/rollback/fork from event logs

---

## FRAMEWORKS

### 1. Why Graphs, Not Just Loops

The Loop Problem (BabyAGI4/ActiveGraph):
- Traditional loops: Think, Act, Observe, Think, Act
- Loops are linear, lose context, cannot reason about relationships
- Cannot handle contradictions, cannot fork, cannot replay

The Graph Advantage:
- Nodes = entities (tasks, decisions, artifacts, concepts)
- Edges = relationships (depends-on, caused-by, contradicts)
- Properties = metadata (timestamps, confidence, provenance)
- You can traverse, query, reason, fork, and replay

### 2. Knowledge Graph Construction

Node Types:
- Entity: name, type, description
- Event: timestamp, actors, outcome
- Decision: context, rationale, alternatives
- Artifact: content, format, version
- Task: status, assignee, deadline

Edge Types:
- depends-on: Must complete before
- caused-by: Causal relationship
- related-to: Semantic similarity
- contradicts: Conflicting choices
- produced-by: Who created it

Construction Rules:
1. Every node must have a unique ID and type
2. Every edge must have source, target, and relationship type
3. Every node/edge must have timestamp and provenance
4. Contradictions must be flagged, not resolved automatically
5. Policy gates required for destructive modifications

### 3. Graph RAG (from BabyAGI4/ActiveGraph)

Architecture:
1. Document ingestion (parse, chunk, embed)
2. Entity extraction (NER from LLM)
3. Relationship extraction (LLM-based relation extraction)
4. Graph construction (nodes + edges + properties)
5. Embedding (graph embeddings + text embeddings)
6. Retrieval (semantic search + graph traversal)
7. Reasoning (LLM with graph context)

Key Difference from Standard RAG:
- Standard RAG: semantic search only (find similar chunks)
- Graph RAG: semantic search + structural reasoning (find related entities,
  follow causal chains, detect contradictions)

### 4. Non-Loop Architectures

Event-Sourced (BabyAGI4):
- Every action is an event in append-only log
- State derived by replaying events
- Fork: branch the event log
- Rollback: revert to previous state
- Replay: re-execute with different parameters

Blackboard:
- Shared knowledge space (the blackboard)
- Multiple agents read/write to it
- No direct agent-to-agent communication
- Emergent behavior from shared state

Micro-Worker:
- Tiny, focused agents (one task each)
- Composed via orchestration layer
- Each worker is stateless
- Orchestration manages state and flow

### 5. Graph Database Patterns (Neo4j)

Property Graph Model:
- Nodes have properties (key-value pairs)
- Edges have properties (key-value pairs)
- Both have labels/types
- Traversal is O(1) per hop (not O(n) like SQL joins)

Cypher Query Language:
- MATCH (a)-[:RELATES_TO]->(b)
- WHERE a.property = value
- RETURN a, b

When to Use Graph DB:
- Highly connected data (social networks, knowledge graphs)
- Path finding (shortest path, all paths)
- Pattern matching (find subgraphs)
- When SQL joins become expensive

---

## THE GRAPH LOOP

Build > Query > Reason > Modify > Validate > Skillify

---

## ANTI-PATTERNS
- Using loops where graphs would be better (linear thinking)
- Not tracking provenance (who added what, when)
- Not handling contradictions (they will happen)
- Not checkpointing before graph modifications
- Not validating graph schema after modifications

---

## SOURCE ATTRIBUTION
YannicKilcher (Context Rot, Energy-Based Transformers, Byte Latent Transformer),
Google DeepMind (Inner Thoughts, Multi-Agent), aiDotEngineer (ActiveGraph/BabyAGI4),
Neo4j graph database patterns, Event Sourcing community patterns

## TEMPLATES
templates/graph-schema.md, templates/event-sourcing.md
