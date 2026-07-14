---
description: Ask the SAP Clean Core documentary expert a question (read-only, source-cited answers)
argument-hint: <your SAP Clean Core question>
---

Use the `sap-clean-core-expert` skill to answer the SAP Clean Core question below.

Follow that skill's workflow exactly:
1. Resolve the bundled knowledge base path and check `HAS_RAW`.
2. Retrieve with `graphify` against the bundled graph (`query` / `explain` / `path` / `affected`,
   always with `--graph "$GRAPH"`). Pick anchors from `references/knowledge-map.md`.
3. Ground the answer: read the cited `raw/*.md` when present, otherwise cite the SAP publication
   by page.
4. Answer concisely, compare options where relevant, and cite every claim.

Stay strictly read-only: never propose or perform a SAP system change. If the question requires
live-system planning or execution, say so and hand off to `sap-erp-clean-core-refactor`.

Respond in the user's language.

Question: $ARGUMENTS
