# academic-editing

### 学术编辑 — 证据优先的论文润色

**[🇺🇸 English](README.md)** | **🇨🇳 中文**

<p>
  <img src="https://img.shields.io/badge/Claude_Code-black?style=flat-square&logo=anthropic&logoColor=white" alt="Claude Code">
  <img src="https://img.shields.io/badge/OpenAI_Codex_CLI-412991?style=flat-square&logo=openai&logoColor=white" alt="OpenAI Codex CLI">
  <img src="https://img.shields.io/badge/Evidence-First-blue?style=flat-square" alt="证据优先">
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square" alt="MIT License">
</p>

> **证据优先的 SCI 论文润色**。在修改任何包含数字、模型结果、样本量、效应估计的句子之前，必须先验证原始证据。

一个 AI Agent 技能，用于医学/生物 SCI 论文润色，强制执行**证据优先验证**。在提升语言的同时保持科学准确性。

## 核心原则：证据优先

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

## 工作流程

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

## 研究类型路由

| 研究类型 | 内部参考文档 |
|----------|-------------|
| 临床队列 / 观察性研究 | `references/cohort-study-edit.md` |
| 生信分析（GWAS、单细胞、MR） | `references/bioinfo-edit.md` |
| 综述、观点、综述式文章 | `references/journal-writing.md` |
| 临床稿件、事实密集型文本 | `references/clinical-accuracy.md` |
| 全文论文、重大修改 | `references/manuscript-coherence.md` |

## 报告规范

润色前必须映射到报告规范：

- **临床试验**: CONSORT / SPIRIT
- **观察性/队列研究**: STROBE
- **综述/Meta 分析**: PRISMA
- **诊断/预测**: STARD / TRIPOD
- **MR/GWAS/Omics**: STROBE-MR / STREGA

## 与 bioinfo-autopilot 的集成

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

## 安装

### 快速安装（告诉 AI Agent）

**Codex CLI:**
```
告诉 Codex: "根据 https://github.com/laleoarrow/academic-editing#installation 的说明安装 academic-editing"
```

**Claude Code:**
```
告诉 Claude: "根据 https://github.com/laleoarrow/academic-editing#installation 的说明安装 academic-editing"
```

### 手动安装

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

## 相关 Skills

| Skill | 用途 | GitHub |
|-------|------|--------|
| **bioinfo-autopilot** | 生信分析，官方文档优先 | https://github.com/laleoarrow/bioinfo-autopilot |
| **pua-academic** | 学术压力引擎 | https://github.com/laleoarrow/pua-academic |

## License

MIT License

---

**GitHub**: https://github.com/laleoarrow/academic-editing
