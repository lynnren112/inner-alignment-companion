# Public Hermes Skill Standard

This document defines a reusable standard for publishing Hermes skills as clean public GitHub repositories.

Its purpose is to make future skill repos:

- easier to install
- easier to understand
- easier to maintain
- easier to reuse as a productized series rather than one-off artifacts

---

## 1. Naming standard

### Repository name

Use the skill name as the repository name whenever possible.

**Recommended pattern:**

```text
skill-name
```

Examples:

- `inner-alignment-companion`
- `decision-clarity-coach`
- `relationship-pattern-decoder`

### Skill name inside `SKILL.md`

The `name:` field in frontmatter should match the public repo name.

```yaml
name: skill-name
```

### Why this matters

Keeping repo name, install path, and skill name aligned reduces confusion across:

- GitHub URL
- local install path
- Hermes invocation name
- documentation examples

---

## 2. README standard

Every public skill repo should have a README that can serve **both**:

1. first-time human readers on GitHub
2. practical users who want to install and use the skill quickly

### Recommended README sections

1. Title
2. Badges (optional but recommended)
3. One-line summary (EN + ZH if public-facing)
4. Table of contents
5. Quick Start
6. 中文简介
7. English Summary
8. What this skill is for
9. Who this is for / not for
10. Core orientation
11. Default output shape
12. Installation
13. How to invoke it
14. Repository structure
15. Examples
16. Boundaries and safety
17. Sources / references
18. License
19. Contributing

### README writing rules

- Lead with usefulness, not theory
- Show install steps early
- Include at least one copy-pasteable prompt example
- Keep safety/boundary language explicit
- Prefer clarity over poetic abstraction
- Assume a stranger is landing on the repo with zero prior context

---

## 3. `SKILL.md` metadata standard

`SKILL.md` is the primary install artifact.
It should remain the single source of truth for the actual skill definition.

### Required frontmatter fields

```yaml
name: skill-name
description: One-sentence public-facing description.
version: 0.1.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [tag1, tag2]
    related_skills: []
    language: zh-CN
    public_repo: https://github.com/yourname/skill-name
    install_entry: SKILL.md
```

### Metadata rules

- `description` should be concise and readable by humans
- `version` should change for meaningful public updates
- `public_repo` should point to the canonical repo
- `install_entry` should remain `SKILL.md`
- tags should describe the actual use case, not vague aspirations

---

## 4. Examples standard

Every public skill repo should include an `examples/` directory.

### Minimum standard

- at least 3 examples
- each example should show a realistic user input
- each example should show the intended output shape or response style

### Good example qualities

- realistic, not over-polished
- emotionally specific or operationally specific
- demonstrate the distinctive value of the skill
- short enough to skim, clear enough to learn from

### Example file naming

Use descriptive, lowercase, hyphenated filenames:

```text
examples/
├─ example-topic-one.md
├─ example-topic-two.md
└─ example-topic-three.md
```

---

## 5. References standard

If the skill depends on a framework, source tradition, methodology, or special boundary conditions, include:

```text
references/README.md
```

### Purpose of references

- explain where the skill came from
- clarify what it is and is not
- prevent misuse
- preserve conceptual coherence across future revisions

---

## 6. Safety and boundary standard

Every public skill repo should explicitly say what the skill does **not** replace.

At minimum, check whether the README should state that the skill does not replace:

- therapy / mental-health care
- crisis support
- medical advice
- legal advice
- financial or investment advice
- domain-specific professional judgment

### Rule

If the skill touches emotionally sensitive or high-stakes areas, the boundary section is mandatory.

---

## 7. Repo structure standard

### Minimum public repo structure

```text
skill-name/
├─ README.md
├─ SKILL.md
├─ LICENSE
└─ examples/
```

### Recommended public repo structure

```text
skill-name/
├─ README.md
├─ SKILL.md
├─ CHANGELOG.md
├─ LICENSE
├─ CONTRIBUTING.md
├─ PUBLISHING-CHECKLIST.md
├─ GITHUB_REPO_METADATA.md
├─ examples/
│  ├─ README.md
│  └─ ...
├─ references/
│  └─ README.md
├─ templates/
│  ├─ README_TEMPLATE.md
│  ├─ CHANGELOG_TEMPLATE.md
│  └─ SKILL_FRONTMATTER_TEMPLATE.yaml
└─ .github/
   ├─ ISSUE_TEMPLATE/
   └─ pull_request_template.md
```

---

## 8. Versioning standard

Use simple semantic-ish public versions for repo-visible changes.

### Suggested interpretation

- `0.1.0` — initial public draft
- `0.2.0` — repo structure or documentation materially improved
- `0.3.0` — install/readability/template quality materially improved
- patch versions can be used later if you want finer granularity

### Rule of thumb

If a GitHub visitor would notice the difference, update `CHANGELOG.md`.

---

## 9. Release workflow standard

Use this release sequence for future public skill repos:

1. Finalize `SKILL.md`
2. Write a public-facing README
3. Add at least 3 examples
4. Add references / boundaries if needed
5. Add LICENSE
6. Add CHANGELOG entry
7. Validate install path and prompt examples
8. Review rendered README on GitHub
9. Add community files if the repo is meant for collaboration
10. Push only after the repo reads clearly to a stranger

---

## 10. Productization standard

The key principle is:

> Do not publish one-off skill repos as isolated exceptions. Publish them as members of a repeatable system.

That means each new repo should reuse the same core standards for:

- naming
- metadata
- README shape
- example count
- safety framing
- release checklist
- GitHub collaboration files

This turns a collection of random repos into a recognizable public skill catalog.

---

## 11. Anti-patterns to avoid

Avoid these common mistakes:

- repo name and skill name do not match
- README is only philosophical and has no install instructions
- no examples
- no safety/boundary section where one is needed
- `SKILL.md` exists but README never tells users what to do with it
- examples are too polished and not realistic
- metadata is inconsistent across repos
- each repo uses a totally different structure

---

## 12. Operational checklist summary

Before calling a public skill repo “done”, confirm:

- [ ] repo name matches skill name
- [ ] `SKILL.md` is installable and primary
- [ ] README has quick start and prompt example
- [ ] at least 3 examples exist
- [ ] safety/boundary framing is present if needed
- [ ] changelog updated
- [ ] license present
- [ ] template/reuse value preserved if this is part of a broader series

---

## 13. Canonical support files in this repo

This repository already includes reusable support files for the standard:

- [`PUBLISHING-CHECKLIST.md`](PUBLISHING-CHECKLIST.md)
- [`GITHUB_REPO_METADATA.md`](GITHUB_REPO_METADATA.md)
- [`CONTRIBUTING.md`](CONTRIBUTING.md)
- [`templates/README_TEMPLATE.md`](templates/README_TEMPLATE.md)
- [`templates/CHANGELOG_TEMPLATE.md`](templates/CHANGELOG_TEMPLATE.md)
- [`templates/SKILL_FRONTMATTER_TEMPLATE.yaml`](templates/SKILL_FRONTMATTER_TEMPLATE.yaml)

Use these together, not in isolation.
