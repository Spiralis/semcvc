# Semantic CVC (Commit, Versioning & Changelog)

**Version:** Semantic CVC v1.0.0  
**License:** Semantic CVC © 2024 by Ronny Hanssen is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

---

## Why Semantic CVC?

Semantic CVC improves **developer experience (DX)** by streamlining workflows, maintaining a clear Git history, and automating changelog generation while supporting semantic versioning.

### Key Benefits
- **Developer-Centric**: Reduces manual work for versioning and changelog creation.
- **Clear Git Log**: Provides a consistent, structured commit history.
- **Semantic Versioning**: Adheres to semantic versioning standards.
- **Automated Changelog**: Tracks unreleased changes and finalizes entries upon version tagging.

---

## Specification Summary

| Type  | Purpose                        | Versioning Effect               | Changelog Section |
|-------|--------------------------------|----------------------------------|-------------------|
| `B:`  | Breaking changes               | Major increment (`x+1.0.0`)      | Breaking Changes  |
| `F:`  | New features                   | Minor increment (`x.y+1.0`)      | Features          |
| `C:`  | Backward-compatible changes    | Patch increment (`x.y.z+1`)      | Changes           |

---

## Detailed Specifications

### 1. `B:` (Breaking Change)

**Format**:  
