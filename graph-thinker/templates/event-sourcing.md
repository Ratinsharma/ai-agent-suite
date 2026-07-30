# Event Sourcing Template

## Event Schema
{
  "id": "unique-event-id",
  "type": "action|decision|observation|error",
  "timestamp": "ISO timestamp",
  "actor": "entity-id",
  "target": "entity-id",
  "data": { ... },
  "metadata": { "version": 1, "provenance": "source" }
}

## Operations
- Append: add event (never modify existing)
- Query: filter by type, actor, time range
- Replay: re-execute from checkpoint
- Fork: branch the event log
- Rollback: revert to checkpoint

## Checkpoint Strategy
- After N events (default: 100)
- After high-stakes actions (Save Button)
- Before graph modifications
- On demand (manual checkpoint)
