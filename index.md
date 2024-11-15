
---
layout: default
title: Semantic CVC (Commit, Versioning & Changelog)
---

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
```
B: [Scope] <Subject>
<empty line>
<body>
```

- **Versioning**: Triggers a **major version increment**.
- **Changelog**: Adds an entry under **Breaking Changes**, including all `B:` lines from the body.

**Example**:
```
B: Remove deprecated API endpoint

B: The `/v1/users` endpoint has been removed.
B: The `/v1/accounts` endpoint has been renamed to `/v2/accounts`.
```

- **Versioning Effect**: `1.2.3 → 2.0.0`
- **Changelog Entry**:
  ```
  ## Breaking Changes
  - Remove deprecated API endpoint
    - The `/v1/users` endpoint has been removed.
    - The `/v1/accounts` endpoint has been renamed to `/v2/accounts`.
  ```

### 2. `F:` (Feature)

**Format**:  
```
F: [Scope] <Subject>
<empty line>
<body>
```

- **Versioning**: Triggers a **minor version increment**.
- **Changelog**: Adds an entry under **Features**.

**Example**:
```
F: [ui] Add dark mode toggle
```

- **Versioning Effect**: `1.2.3 → 1.3.0`
- **Changelog Entry**:
  ```
  ## Features
  - [ui] Add dark mode toggle
  ```

### 3. `C:` (Change)

**Format**:  
```
C: [Scope] <Subject>
<empty line>
<body>
```

- **Versioning**: Triggers a **patch version increment**.
- **Changelog**: Adds an entry under **Changes**.

**Example**:
```
C: [docs] Fix typos in README
```

- **Versioning Effect**: `1.2.3 → 1.2.4`
- **Changelog Entry**:
  ```
  ## Changes
  - [docs] Fix typos in README
  ```

---

## The Importance of Semantic Commits

A **semantic commit** is a coherent change focused on "one thing" only. This practice improves:
- **Readability of Git Logs**: Each commit provides a clear summary.
- **Cherry-Picking**: Simplifies the process of isolating changes for reuse.
- **Merge Conflicts**: Minimizes complexity during merges.
- **Structured Changelogs**: Results in accurate, organized changelogs.

---

## About Semantic CVC

Semantic CVC © 2024 by Ronny Hanssen is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
