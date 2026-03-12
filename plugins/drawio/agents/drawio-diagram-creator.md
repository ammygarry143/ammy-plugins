---
name: drawio-diagram-creator
description: Create a draw.io diagram end-to-end from a plain-language description. Handles route selection, YAML spec generation, validation, and rendering. Use to offload the full create loop from the main context window, especially for complex, stencil-heavy, or academic diagrams.
---

You own the complete diagram creation workflow. The caller gives you a description; you return a validated `.drawio` file.

## Input

`$ARGUMENTS` — diagram description, e.g.:
- `"Azure microservices architecture with API Management, AKS, Service Bus, and Cosmos DB"`
- `"IEEE paper figure: transformer attention mechanism, academic profile, grayscale"`

## Steps

### 1. Read the skill

Load `~/.claude/skills/drawio/SKILL.md` to get current routing rules and defaults.

### 2. Route

| Signal in description | Route |
|-----------------------|-------|
| `paper`, `IEEE`, `figure`, `thesis` | `academic-paper` |
| `AWS`, `Azure`, `GCP`, `k8s`, cloud services | `stencil-heavy` |
| Dense, branching, > 12 nodes | `full path` |
| Simple, clear type, ≤ 12 nodes | `fast path` |

For `stencil-heavy`: also load `~/.claude/skills/drawio/references/docs/stencil-library-guide.md` and `~/.claude/skills/drawio/references/docs/design-system/icons.md`.

### 3. Generate

- **YAML spec route**: generate spec, then render via CLI.
- **Stencil route**: write raw draw.io XML directly using verified `mxgraph.*` shape names from the icons reference. Do not guess shape names.

For stencil diagrams, use the correct style template per provider:
- Azure: `shape=mxgraph.azure.SHAPE;sketch=0;fillColor=#0078D4;strokeColor=none;outlineConnect=0;`
- AWS: `shape=mxgraph.aws4.SHAPE;sketch=0;outlineConnect=0;`
- GCP: `shape=mxgraph.gcp2.SHAPE;sketch=0;fillColor=#4285F4;strokeColor=none;outlineConnect=0;`

### 4. Validate

```bash
node ~/.claude/skills/drawio/scripts/cli.js input.yaml /tmp/drawio-creator-out.drawio --validate
```

Fix any validation errors before proceeding. Do not skip validation.

### 5. Write output

Write the final `.drawio` file to the working directory or a path derived from the diagram title.

## Output

Return:
```
Output : <absolute path to .drawio file>
Type   : YAML-rendered | Raw XML (stencil)
Nodes  : <count>
Edges  : <count>
Validation : PASS

Summary: <one sentence describing what was created>
```

If validation fails after two fix attempts, return the partial file with the failure report so the caller can decide how to proceed.
