# scifi-lightnovel-harness — AI 科幻轻小说写作框架

> opencode 入口。加载主编 Agent，管理小说项目。

## 启动

1. 读取 `SKILL.md` — 主编 Agent 定义
2. 读取 `harness/current-project.md` — 活跃项目路径
3. 按需加载 `harness/agents/` 专业 Agent

## 新建项目

```bash
PROJECT=你的小说名
mkdir -p projects/$PROJECT/{设定/{世界观,角色,大纲},正文,词条,harness-project/{reports,状态/配角,记忆}}
cp harness/projects/模板-科幻轻小说.md projects/$PROJECT/harness-project/constraints.md
cp harness/memory/*模板.md projects/$PROJECT/harness-project/状态/或记忆/
echo "path: projects/$PROJECT" > harness/current-project.md
```

详见 `SKILL.md` §五、项目体系。
