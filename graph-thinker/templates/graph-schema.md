# Graph Schema Template

## Node
{
  "id": "unique-id",
  "type": "entity|event|decision|artifact|task",
  "name": "human-readable name",
  "properties": {
    "created_at": "ISO timestamp",
    "provenance": "source",
    "confidence": 0.0-1.0
  }
}

## Edge
{
  "id": "unique-id",
  "source": "node-id",
  "target": "node-id",
  "type": "depends-on|caused-by|related-to|contradicts",
  "properties": {
    "weight": 0.0-1.0,
    "bidirectional": true|false
  }
}

## Validation Rules
1. Source/target must reference existing node
2. No self-loops
3. Contradictions flagged for human review
4. Destructive modifications require policy gate
5. Append-only (no deletes, only new edges)
