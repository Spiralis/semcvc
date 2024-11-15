
---
layout: default
title: Semantic CVC (Commit, Versioning & Changelog)
---

# Semantic CVC (Commit, Versioning & Changelog)

**Version:** Semantic CVC v0.1.0 (Development)  
**Status:** This specification is currently in development and has not been officially released.  
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

## Specification Summary (Development Version)

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

<p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><span property="dct:title">Semantic CVC</span> by <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://github.com/Spiralis">Ronny Hanssen</a> is licensed under <a href="https://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY 4.0<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" alt=""></a></p>
