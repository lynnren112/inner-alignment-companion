# Inner Alignment Companion

![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)
![Skill](https://img.shields.io/badge/type-Hermes%20skill-blue)
![Language](https://img.shields.io/badge/language-zh--CN-red)
![Status](https://img.shields.io/badge/status-public%20repo-ready-brightgreen)

> A Hermes-compatible skill for emotional clarity, belief inspection, and aligned next steps.  
> 一个面向 Hermes / agent skill 系统的内在对齐陪伴 skill，用来帮助人从情绪触发中看见结构、恢复主体性，并找到更真实的下一步。

---

## Table of Contents

- [Quick Start](#quick-start)
- [中文简介](#中文简介)
- [English Summary](#english-summary)
- [What this skill is for](#what-this-skill-is-for)
- [Who this is for / not for](#who-this-is-for--not-for)
- [Core orientation](#core-orientation)
- [Default output structure](#default-output-structure)
- [Installation](#installation)
- [How to invoke it](#how-to-invoke-it)
- [Example output shape](#example-output-shape)
- [Repository structure](#repository-structure)
- [Reuse this repo as a template](#reuse-this-repo-as-a-template)
- [Examples](#examples)
- [Boundaries and safety](#boundaries-and-safety)
- [Sources of inspiration](#sources-of-inspiration)
- [License](#license)

---

## Quick Start

### Install locally into Hermes

```bash
mkdir -p ~/.hermes/skills/personal/inner-alignment-companion
cp SKILL.md ~/.hermes/skills/personal/inner-alignment-companion/SKILL.md
```

### Invoke it

```text
请用 inner-alignment-companion 帮我拆一下：我最近总被关系里的沉默触发。
```

### Learn the shape quickly

- Read [`SKILL.md`](SKILL.md) for the full agent-facing definition
- Read [`examples/`](examples/) for concrete usage scenarios
- Read [`references/README.md`](references/README.md) for boundaries and orientation

---

## 中文简介

`inner-alignment-companion` 结合《太傻天书》《与神对话》《你值得过更好的生活》与巴夏（Bashar）体系中的共同内核，
帮助使用者在情绪触发、关系困惑、自我怀疑、重复模式和人生卡点中，看见：

- 发生了什么
- 自己给事件下了什么定义
- 背后被触发了什么信念
- 情绪在反馈什么
- 更对齐、更真实、可执行的一小步是什么

它不是“替人给答案”的工具，
而是一个帮助人从混乱中看见结构、从痛苦中恢复主体性的陪伴框架。

---

## English Summary

`inner-alignment-companion` is a public Hermes-compatible skill for reflective emotional support.
It is designed to help a user move from surface-level distress into a clearer structure:

- what actually happened
- what meaning they assigned to it
- which belief or identity pattern got activated
- what the emotion may be feeding back
- what the smallest aligned next step could be

It does **not** try to replace therapy, crisis support, or concrete professional advice.
Its purpose is to help people regain clarity, agency, and honesty in moments of emotional contraction.

---

## What this skill is for

This skill is especially useful for:

- **情绪困扰**：焦虑、委屈、羞耻、嫉妒、空虚、内耗
- **关系卡点**：被忽视、害怕失去、舍不得离开、不敢表达
- **成长停滞**：拖延、卡住、自我怀疑、害怕成功
- **选择困难**：怕选错、怕后悔、不知道自己真正想要什么
- **高视角理解**：想从“定义—信念—情绪反馈—对齐行动”的视角理解一件事

---

## Who this is for / not for

### 适合谁

- 想从情绪里看见结构，而不是只想被安慰一下的人
- 愿意区分“事实”与“定义”的人
- 想识别旧信念、旧身份、重复模式的人
- 想要一个兼顾现实感与高视角的陪伴框架的人
- 希望 agent 在回应中更有穿透力、更少空泛鸡汤的人

### 不适合谁

- 只想让 skill 替自己做决定的人
- 希望得到绝对正确答案、命运判断或灵性背书的人
- 正处于急性危机、自伤/伤人风险、严重精神失控的人
- 需要法律、财务、医疗、投资等专业判断的人

---

## Core orientation

这个 skill 的核心不是鸡汤，也不是宿命论，而是一套相对稳定、能落地的理解框架：

1. **现实是镜子，不只是墙**  
   外在事件很真实，但体验质量常常取决于你如何定义它。

2. **事实和定义不是一回事**  
   发生了什么是一层；你把它解释成什么，是另一层。

3. **情绪是反馈，不是敌人**  
   情绪通常在反馈你此刻相信了什么、活在哪套旧模式里。

4. **限制性信念会塑造体验**  
   常见如：
   - 我不够好
   - 我不值得被爱
   - 我必须证明自己才配拥有
   - 我必须控制才能安全

5. **成长不是更用力，而是更对齐**  
   更少背叛真实感受、真实需要和真实边界，从清明中行动。

6. **最高兴奋不是冲动，而是最有生命感的方向**  
   既跟随真实感，又不过度执着结果。

---

## Default output structure

This skill usually responds in 6 parts:

1. 你现在真正卡住的点
2. 事实 vs 定义
3. 被触发的核心信念
4. 这件事在反馈你什么
5. 更对齐的理解方式
6. 今天可以做的一小步

---

## Installation

### Option 1 — Copy `SKILL.md` into your Hermes skills directory

If you already use Hermes and just want to install the skill locally, copy `SKILL.md` into your skills library.

```bash
mkdir -p ~/.hermes/skills/personal/inner-alignment-companion
cp SKILL.md ~/.hermes/skills/personal/inner-alignment-companion/SKILL.md
```

Then invoke it by skill name inside Hermes.

### Option 2 — Clone this repository and keep it as the source of truth

```bash
git clone https://github.com/lynnren112/inner-alignment-companion.git
cd inner-alignment-companion
```

Then either:

- copy `SKILL.md` into your Hermes skills directory, or
- keep this repo as your editable source and sync updates into your Hermes environment when needed.

### Option 3 — Share it as a public skill repo

If you want others to learn from or reuse the skill, this repository is already structured as a public-facing reference repo.

---

## How to invoke it

You can trigger it directly with prompts like:

- `用 inner-alignment-companion 看一下`
- `用内在对齐陪伴看这件事`
- `用巴夏一点的视角看`
- `从定义 / 信念 / 情绪反馈角度帮我拆`
- `帮我做一次内在对齐解读`

### 5 ready-to-use prompt templates

1. **关系触发**  
   `请用 inner-alignment-companion 帮我拆一下：对方最近不回消息，我很焦虑。`

2. **情绪混乱**  
   `我现在很乱，你用定义—信念—情绪反馈的结构帮我看一下。`

3. **选择卡点**  
   `我在两个选择之间很卡，请用 inner-alignment-companion 帮我看我到底在怕什么。`

4. **重复模式**  
   `我好像总在重复同一种关系模式，帮我看背后在信什么。`

5. **行动拖延**  
   `我知道该开始了，但就是拖延。请用内在对齐视角帮我拆开。`

---

## Example output shape

A typical answer is structured like this:

1. **你现在真正卡住的点** — name the real knot, not just the surface story
2. **事实 vs 定义** — separate event from meaning-making
3. **被触发的核心信念** — identify 1–2 likely active beliefs
4. **这件事在反馈你什么** — interpret the emotion/event as feedback, not punishment
5. **更对齐的理解方式** — offer a clearer and less self-harming frame
6. **今天可以做的一小步** — end with a light, concrete next step

---

## Repository structure

```text
inner-alignment-companion/
├─ README.md
├─ SKILL.md
├─ CHANGELOG.md
├─ LICENSE
├─ PUBLISHING-CHECKLIST.md
├─ examples/
│  ├─ README.md
│  ├─ anxiety-after-no-reply.md
│  ├─ relationship-boundary.md
│  └─ self-doubt-procrastination.md
├─ references/
│  └─ README.md
└─ templates/
   ├─ CHANGELOG_TEMPLATE.md
   ├─ README_TEMPLATE.md
   └─ SKILL_FRONTMATTER_TEMPLATE.yaml
```

### File roles

- `README.md`: public-facing project introduction
- `SKILL.md`: the actual Hermes skill definition
- `examples/`: realistic example prompts and response shapes
- `references/`: orientation, boundaries, and source notes
- `templates/`: starting points for your next public skill repo
- `PUBLISHING-CHECKLIST.md`: step-by-step release checklist for future skill repos
- `CHANGELOG.md`: version history for the public repo

---

## Reuse this repo as a template

If you want to publish more public Hermes skills, you can use this repo as a repeatable pattern.

### Recommended workflow

1. Copy this repo or just copy the `templates/` folder
2. Rename the skill, README title, and install path
3. Replace the core orientation, examples, and references
4. Fill the publishing checklist before making the repo public
5. Keep `SKILL.md` as the single install entry

Start here:

- [`PUBLISHING-CHECKLIST.md`](PUBLISHING-CHECKLIST.md)
- [`templates/README_TEMPLATE.md`](templates/README_TEMPLATE.md)
- [`templates/CHANGELOG_TEMPLATE.md`](templates/CHANGELOG_TEMPLATE.md)
- [`templates/SKILL_FRONTMATTER_TEMPLATE.yaml`](templates/SKILL_FRONTMATTER_TEMPLATE.yaml)

---

## Examples

- [`examples/anxiety-after-no-reply.md`](examples/anxiety-after-no-reply.md)
- [`examples/relationship-boundary.md`](examples/relationship-boundary.md)
- [`examples/self-doubt-procrastination.md`](examples/self-doubt-procrastination.md)

These examples are not meant to be rigid answer keys.
They show how the skill moves from surface story → definition → belief → feedback → action.

---

## Boundaries and safety

This skill:

- does **not** replace therapy, medical care, or crisis intervention
- does **not** replace legal, financial, investment, or clinical advice
- does **not** reduce all suffering to “you attracted this”
- does **not** use spiritual language to erase reality or pressure the user
- does **not** make fatalistic or destiny-based claims

If there is acute crisis, self-harm risk, violent risk, severe insomnia, severe dysregulation, or a need for professional care,
please prioritize real-world support and qualified help.

---

## Sources of inspiration

- 《太傻天书》
- 《与神对话》
- 《你值得过更好的生活》
- 巴夏（Bashar）体系

See also: [`references/README.md`](references/README.md)

---

## License

MIT

---

## One-line summary

**不是替人消灭痛苦，而是帮助人借由痛苦的反馈，更接近真实的自己。**
