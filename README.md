# Sci-Fi Light Novel Harness

归零 项目的 AI 写作管线。

## 架构

```
scifi-lightnovel-harness/
├── SKILL.md                          ← L1: 主编 Agent（协调层）
├── .harness/
│   ├── agents/                       ← L2: 专业 Agent
│   │   ├── 上下文Agent.md            ← 状态追踪 + 上下文打包
│   │   ├── 规划Agent.md              ← 剧情构思 + 大纲设计
│   │   ├── 写作Agent.md              ← 正文生成
│   │   └── 审稿Agent.md              ← 多维度质量审查
│   ├── skills/                       ← L3: 审查模块
│   │   ├── sci-fi-consistency/       ← 科学自洽（原创）
│   │   ├── light-novel-style/        ← 轻小说风格（原创）
│   │   ├── daily-weave/              ← 日常主线交织（原创）
│   │   ├── tech-accuracy/            ← 科幻技术自洽（原创）
│   │   ├── human-linguistics/        ← 语感/AI味（继承）
│   │   └── plot-review/              ← 情节一致性（继承）
│   ├── rules/                        ← 规则体系
│   │   ├── 用户身份适配指南.md
│   │   ├── 审稿输出模板.md
│   │   └── 反馈追踪流程.md
│   ├── projects/
│   │   └── 模板-科幻轻小说.md        ← 通用题材约束（R1-R8）
│   ├── current-project.md            ← 当前项目指针
│   ├── memory/README.md
│   └── cases/
├── projects/
│   └── 归零/                         ← 项目专属
│       ├── constraints.md            ← R-G 系列规则 + 卷级周期
│       ├── 状态/主角.md
│       └── 记忆/（伏笔/事件/风格/章节摘要）
└── README.md
```

## 使用

加载 SKILL.md 后，主编 Agent 自动协调全管线。
当前项目：归零（第一卷「连接」）。

## 继承自

- [novel-harness](https://github.com/manhai934/novel-harness) — Agent 架构 + 语感/情节审查
- 天命AI写手 — 题材 Spec 方法论
