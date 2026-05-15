# Sci-Fi Light Novel Harness

科幻轻小说的 AI 写作管线框架。L1-L3 四层 Agent 架构 + 6 审查模块 + 项目约束分离。

适用于科幻悬疑、黑客文化、都市日常等元素的轻小说创作。

## 架构

```
L1: 主编 Agent (SKILL.md)              ← 协调者，不亲自执行
L2: 4 专业 Agent (harness/agents/)     ← 上下文/规划/写作/审稿
L3: 6 审查模块 (harness/skills/)       ← 原创 4 + 继承 2
L0: 项目层 (.harness-project/)          ← 项目专属约束/状态/记忆
```

## 审查模块

| 模块 | 用途 | 来源 |
|:-----|:-----|:-----|
| `sci-fi-consistency` | 科学自洽：设定逻辑、蝴蝶效应、术语层级 | 原创 |
| `light-novel-style` | 轻小说风格：对话、情感克制、翻译腔 | 原创 |
| `daily-weave` | 日常主线交织：功能性、密度统计 | 原创 |
| `tech-accuracy` | 技术自洽：黑客技术描写准确性 | 原创 |
| `human-linguistics` | 通用语感：AI 味检测、语病诊断 | 继承 |
| `plot-review` | 通用情节一致性：角色/时间线/伏笔 | 继承 |

## 快速开始

```bash
git clone <this-repo>
cd scifi-lightnovel-harness

# 1. 创建项目约束
cp harness/projects/模板-科幻轻小说.md my-novel/.harness-project/constraints.md

# 2. 编辑约束 → 填入角色名、卷周期、伏笔清单

# 3. 指向项目
echo "path: /path/to/my-novel" > harness/current-project.md

# 4. 加载 SKILL.md 到你的 AI Agent → 开始写作
```

## 项目结构

```
你的小说项目/
├── 设定/                  ← 世界观/角色/大纲
├── 正文/                  ← 各章正文
└── .harness-project/      ← Harness 项目层
    ├── constraints.md     ← R-G 系列项目约束
    ├── 状态/              ← 角色状态
    └── 记忆/              ← 伏笔/事件/摘要
```

Harness 主体与项目完全解耦——一个 Harness 可复用于多个小说项目。

## 继承自

- [novel-harness](https://github.com/manhai934/novel-harness) — Agent 架构 + 语感/情节审查模块
- 天命AI写手 — 题材 Spec 方法论 + 参数化配置

## License

GNU General Public License v3.0 — see [LICENSE](LICENSE)

工具本身 copyleft；用本工具产出的文字内容版权归创作者所有，不受 GPL 约束。
