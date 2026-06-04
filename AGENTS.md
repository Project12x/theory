# AGENTS.md

## Purpose

This repository is a philosophy-first Obsidian LLM Wiki for compiling Eric Steenwerth's worldview into persistent, cross-linked markdown notes while preserving original source texts and clearly separating Eric's intended claims from AI-organized or AI-injected material.

The wiki's job is not to replace the source documents. The wiki is the compiled interface: it extracts concepts, claims, domains, tensions, questions, and formalization paths so the system can be queried, extended, challenged, and eventually split into focused repos.

## Repository Layout

```text
raw/
  sources/       # User-controlled source drop zone. Agents read from here but should not modify source files.

wiki/
  index.md       # Master Obsidian index.
  log.md         # Append-only operation log.
  sources/       # One compiled page per source document.
  concepts/      # Atomic conceptual primitives.
  domains/       # Broad philosophical territories.
  threads/       # Cross-domain arguments.
  claims/        # Strong propositions, predictions, or falsifiable statements.
  questions/     # Open questions and research prompts.
  examples/      # Concrete examples used to ground claims.

catalog/         # Earlier catalog layer; useful reference, gradually superseded by wiki/.
templates/       # Reusable markdown templates.
```

Original source documents may remain at repo root during the early phase. If the repo later splits, move or copy source documents into the appropriate `raw/sources/` folder before ingesting new revisions.

## Entity Types

### Source

A source is an original essay, thesis, paper, note, transcript, or draft.

Provenance values:

- `original`: authored directly by Eric without meaningful AI shaping.
- `ai-organized`: Eric's ideas arranged, expanded, or polished with AI assistance.
- `ai-assisted`: Eric supplied direction, while AI contributed substantial structure or formalization.
- `mixed`: multiple provenance layers are present and need page-level notes.

Claim confidence values:

- `core`: Eric explicitly owns this claim.
- `likely`: consistent with Eric's direction but not yet explicitly confirmed.
- `suspect`: may be AI-injected, over-personalized, or over-postulated.
- `rejected`: Eric clarified that this is not his current position.

Frontmatter:

```yaml
---
type: source
status: raw | ingested | partial
domain: []
provenance: original | ai-organized | ai-assisted | mixed
claim_confidence: core | likely | suspect | mixed
created: YYYY-MM-DD
updated: YYYY-MM-DD
source_path: ""
---
```

Required sections:

- `# Page Title`
- `## Summary`
- `## Core Contributions`
- `## Key Concepts`
- `## Important Claims`
- `## Open Questions`
- `## Links`

### Concept

A concept is an atomic idea that can recur across sources.

Frontmatter:

```yaml
---
type: concept
status: seed | developed | contested
domain: []
created: YYYY-MM-DD
updated: YYYY-MM-DD
---
```

Required sections:

- `# Concept Name`
- `## Definition`
- `## Explanation`
- `## Appears In`
- `## Related Concepts`
- `## Notes`

### Domain

A domain is a broad area of the philosophy.

Frontmatter:

```yaml
---
type: domain
status: active
created: YYYY-MM-DD
updated: YYYY-MM-DD
---
```

Required sections:

- `# Domain Name`
- `## Scope`
- `## Core Sources`
- `## Central Concepts`
- `## Central Claims`
- `## Open Questions`
- `## Related Domains`

### Thread

A thread is an argument or pattern that crosses multiple domains.

Frontmatter:

```yaml
---
type: thread
status: active
domain: []
created: YYYY-MM-DD
updated: YYYY-MM-DD
---
```

Required sections:

- `# Thread Name`
- `## Pattern`
- `## Cross-Domain Movement`
- `## Appears In`
- `## Related Concepts`
- `## Open Questions`

### Claim

A claim is a strong proposition that may need evidence, formalization, falsification, or revision.

Frontmatter:

```yaml
---
type: claim
status: speculative | argued | formalizing | testable | contested | suspect | rejected
domain: []
claim_confidence: core | likely | suspect | rejected
created: YYYY-MM-DD
updated: YYYY-MM-DD
---
```

Required sections:

- `# Claim Name`
- `## Claim`
- `## Reasoning`
- `## Implications`
- `## Evidence Or Support`
- `## Revision Or Falsification Conditions`
- `## Related Pages`

### Question

A question is an unresolved inquiry that should guide future writing, research, or formalization.

Frontmatter:

```yaml
---
type: question
status: open | partial | resolved | retired
domain: []
created: YYYY-MM-DD
updated: YYYY-MM-DD
---
```

Required sections:

- `# Question`
- `## Why It Matters`
- `## Current State`
- `## Relevant Pages`
- `## Possible Next Steps`

### Example

An example is a concrete case that grounds a claim or concept.

Frontmatter:

```yaml
---
type: example
status: seed | developed
domain: []
created: YYYY-MM-DD
updated: YYYY-MM-DD
---
```

Required sections:

- `# Example Name`
- `## Example`
- `## Why It Matters`
- `## Pattern`
- `## Related Pages`

## Cross-Link Conventions

- Use Obsidian wikilinks: `[[Page Name]]`.
- Link concepts the first time they appear in a page section.
- Prefer meaningful concept pages over thin stubs.
- Create a page when a concept, claim, or question is likely to be queried later.
- Use plural links sparingly; prefer canonical singular concept names.
- Link source pages from all derived concept, claim, domain, and thread pages.

## Philosophy-First Rule

The central spine is the philosophy: symbolic operation, consciousness, civilization, AI, collapse cosmology, and formalization.

Physics material such as CHPE should be treated as a formalization branch unless the user explicitly asks to make it the repo's main spine.

## Source Handling Rules

- Do not rewrite or "clean up" raw source documents unless the user asks.
- Compile sources into wiki pages.
- Distinguish source claims from wiki synthesis.
- Preserve provenance. If a source is AI-assisted formalization based on the user's direction, mark it that way. If it is the user's original writing, mark it as original.
- Treat AI-organized drafts as drafts, not doctrine. AI may have injected extra postulation, personalization, certainty, or claims Eric did not intend.
- When extracting claims from AI-organized or mixed documents, default to `claim_confidence: suspect` unless Eric has explicitly affirmed the claim or it is strongly supported by multiple original statements.
- When a claim is speculative, mark it as speculative.
- When a claim touches established physics, preserve the claim but avoid presenting it as established fact unless supported by sources.
- When two pages conflict, document the tension explicitly rather than silently resolving it.
- When Eric clarifies a claim is not his current position, mark it as `rejected` or move it to a review queue instead of deleting the history.

## Ingest Workflow

1. Read this file.
2. Read `wiki/index.md` to understand existing compiled pages.
3. Read the source fully enough to extract its conceptual payload.
4. Create or update the source page.
5. Create or update related concept, domain, thread, claim, and question pages.
6. Update `wiki/index.md`.
7. Append an entry to `wiki/log.md`.

## Query Workflow

1. Read `wiki/index.md`.
2. Open the most relevant wiki pages.
3. Answer from compiled wiki pages.
4. If the answer creates reusable synthesis, file it back as a wiki page and update the index/log.

## Lint Workflow

Run periodically, not after every edit.

Check for:

- Orphan pages
- Stale index entries
- Contradictions or unresolved tensions
- Concepts mentioned repeatedly without pages
- Claims missing revision or falsification conditions
- Physics claims that need clearer status labels
- AI-injected postulation that has not been explicitly confirmed by Eric
