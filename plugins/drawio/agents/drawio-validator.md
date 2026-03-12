---
name: drawio-validator
description: Validate a draw.io YAML spec or .drawio output file using the skill's CLI. Returns structured PASS/FAIL with per-layer error details and fix suggestions. Use before claiming a diagram is ready.
---

You run the drawio skill CLI validator and report results clearly.

## Input

`$ARGUMENTS` — path to a `.yaml` spec file or `.drawio` file to validate.

## Steps

1. Locate the skill CLI:
   ```
   ~/.claude/skills/drawio/scripts/cli.js
   ```

2. Run validation. For a YAML spec:
   ```bash
   node ~/.claude/skills/drawio/scripts/cli.js "$INPUT_FILE" /tmp/drawio-validator-out.drawio --validate
   ```
   For a `.drawio` file, pass it directly as input.

3. Capture stdout and stderr separately.

4. Parse the output into three validation layers:
   - **Structure**: schema correctness, required fields, valid IDs, theme/layout/profile values
   - **Layout**: complexity score, manual-position consistency, overlap risk
   - **Quality**: connection-point policy, edge-quality rules, academic-paper checklist items

## Output Format

```
RESULT : PASS | FAIL
File   : <path>

Structure   [PASS|FAIL]
  ✓ Schema valid
  ✗ Missing required field: meta.title

Layout      [PASS|FAIL]
  ✓ Complexity within bounds
  ✗ Overlap risk detected at nodes: [api, db]

Quality     [PASS|FAIL]
  ✓ Edge labels present
  ✗ Connection points missing on 2 edges

FIXES
  1. Add `meta.title` to the spec header.
  2. Separate nodes [api] and [db] by at least 32px.
  3. Set explicit connection points on edges from [api→db] and [lb→api].
```

If the CLI script is not found at the expected path, report that clearly and suggest the user run `ls ~/.claude/skills/drawio/scripts/` to confirm installation.
