# academic-editing

### Academic Editing — Evidence-First Manuscript Polishing

**[🇨🇳 中文](README.zh-CN.md)** | **🇺🇸 English**

<p>
  <img src="https://img.shields.io/badge/Claude_Code-black?style=flat-square&logo=anthropic&logoColor=white" alt="Claude Code">
  <img src="https://img.shields.io/badge/OpenAI_Codex_CLI-412991?style=flat-square&logo=openai&logoColor=white" alt="OpenAI Codex CLI">
  <img src="https://img.shields.io/badge/Evidence-First-blue?style=flat-square" alt="Evidence-First">
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square" alt="MIT License">
</p>

> **证据优先的 SCI 论文润色**。在修改任何包含数字、模型结果、样本量、效应估计的句子之前，必须先验证原始证据。

An AI Agent skill for polishing medical/biological SCI manuscripts with **evidence-first validation**. Preserves scientific correctness while improving language.

## Core Principle: Evidence-First

### 问题：AI 润色的陷阱

| 问题 | 表现 | 后果 |
|------|------|------|
| **数字漂移** | 润色时改错数字 | 数据不一致 |
| **因果夸大** | 润色后因果语气过强 | Reviewer 质疑 |
| **逻辑断裂** | 各段润色后逻辑不一致 | 文章失去连贯性 |
| **规范违反** | 不符合报告规范 | 被要求补充材料 |

### 解决方案

```
润色前必做：
1. 证据锁定：验证数字、模型结果、样本量、效应估计
2. 规范映射：STROBE/CONSORT/PRISMA 等
3. 稿件地图：确认一个论点、一个强度等级、一个期刊定位

润色后必做：
4. Loop 检查：数字是否漂移？逻辑是否断裂？
```

## Workflow

```
用户请求论文润色
        ↓
┌───────────────────┐
│   信息收集        │
│  - 研究问题/标题  │
│  - 文章类型       │
│  - 目标期刊       │
│  - 证据位置       │
└───────────────────┘
        ↓
┌───────────────────┐
│   证据锁定        │
│  - 验证数字       │
│  - 检查表格       │
│  - 确认图表       │
└───────────────────┘
        ↓
┌───────────────────┐
│   规范映射        │
│  - STROBE         │
│  - CONSORT        │
│  - PRISMA         │
└───────────────────┘
        ↓
     润色执行
        ↓
┌───────────────────┐
│   Loop 检查       │
│  - 数字是否漂移   │
│  - 逻辑是否断裂   │
│  - 规范是否满足   │
└───────────────────┘
```

## Study-Type Routing

| Study Type | Internal Reference |
|------------|-------------------|
| Clinical cohort / observational | `references/cohort-study-edit.md` |
| Bioinformatics (GWAS, single-cell, MR) | `references/bioinfo-edit.md` |
| Reviews, perspectives, review-style articles | `references/journal-writing.md` |
| Clinical manuscripts, fact-heavy prose | `references/clinical-accuracy.md` |
| Full papers, major rewrites | `references/manuscript-coherence.md` |

## Reporting Guidelines

Always map to a reporting guideline before polishing:

- **Trials**: CONSORT / SPIRIT
- **Observational/Cohort**: STROBE
- **Reviews/Meta-analyses**: PRISMA
- **Diagnostics/Prediction**: STARD / TRIPOD
- **MR/GWAS/Omics**: STROBE-MR / STREGA

## Integration with bioinfo-autopilot

```
┌─────────────────────────────────────────────────────┐
│  bioinfo-autopilot                                  │
│  官方文档优先，执行生信分析                          │
│                                                      │
│  证据锁定后 ↓ 调用                                   │
├─────────────────────────────────────────────────────┤
│  academic-editing                                    │
│  - 证据优先验证                                      │
│  - 报告规范映射                                      │
│  - 论文润色                                          │
│  - Loop 一致性检查                                   │
└─────────────────────────────────────────────────────┘
```

## Installation

### Quick Install for AI Agents

**For Codex CLI:**
```
Tell Codex: "Install academic-editing according to instructions at https://github.com/laleoarrow/academic-editing#installation"
```

**For Claude Code:**
```
Tell Claude: "Install academic-editing according to instructions at https://github.com/laleoarrow/academic-editing#installation"
```

### Manual Install

**Claude Code:**
```bash
git clone https://github.com/laleoarrow/academic-editing.git ~/agents/academic-editing
ln -s ~/agents/academic-editing/skills/academic-editing ~/.claude/skills/academic-editing
```

**Codex CLI:**
```bash
git clone https://github.com/laleoarrow/academic-editing.git ~/agents/academic-editing
ln -s ~/agents/academic-editing/codex/academic-editing ~/.codex/skills/academic-editing
```

## Related Skills

| Skill | Purpose | GitHub |
|-------|---------|--------|
| **bioinfo-autopilot** | 生信分析，官方文档优先 | https://github.com/laleoarrow/bioinfo-autopilot |
| **pua-academic** | 学术压力引擎 | https://github.com/laleoarrow/pua-academic |

## License

MIT License

---

**GitHub**: https://github.com/laleoarrow/academic-editing
