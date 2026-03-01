# Prompts — Pending Review

This directory holds prompt submissions that have not yet been validated against
the marketplace schema or classified with safety tags.

## Required Before Promotion

Each prompt must pass the following before moving to `prompts/approved/`:

1. **Schema validation** — must conform to the prompt schema (inputs, constraints,
   expected outputs, versioning, pricing tier)
2. **Safety tag assignment** — at least one safety tag must be applied
3. **Content review** — prompts involving security, legal, medical, or financial
   topics require manual review before approval
4. **Pricing tier assignment** — must be assigned a valid pricing tier

## Files in This Directory

| File | Inferred Topic | Safety Review Required |
|------|---------------|------------------------|
| `333` | Security engineering / red-team prompts | **Yes — offensive security content** |
| `544444` | Mixed: technical prompts + security prompts | **Yes — offensive security content** |
| `66uu888` | Mixed: architecture + general prompts | Yes — review advised |

> **Note:** Files with offensive security content (supply chain attacks, container
> escapes, credential exfiltration techniques) must be reviewed against the
> platform's acceptable use policy before approval. These prompts may be suitable
> for verified security professionals only, and must be gated behind appropriate
> access controls and safety tags.
