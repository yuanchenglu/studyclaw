# StudyClaw Agent Guidelines

> 教育垂直 AI 助手平台 — 让学习更智能

---

## 项目概述

**StudyClaw** 是基于 [OpenClaw](https://github.com/openclaw/openclaw) 构建的教育垂直 AI 助手平台。

- **产品定位**: 网关 + Agent 平台
- **目标用户**: 学生、教师、终身学习者
- **核心价值**: 内置教育场景 Agent 和 Skill，开箱即用

### 部署域名

| 区域 | 域名                         |
| ---- | ---------------------------- |
| 全球 | https://studyclaw.org        |
| 中国 | https://studyclaw.7color.vip |

---

## 内置 Agent 配置

StudyClaw 默认提供 4 个教育 Agent：

| Agent ID           | 名称         | 默认 | Skills                               |
| ------------------ | ------------ | ---- | ------------------------------------ |
| `ai-tutor`         | AI 导师      | ✅   | studyclaw, tutoring, problem-solving |
| `homework-grader`  | 作业批改助手 | ❌   | studyclaw, grading, problem-solving  |
| `learning-planner` | 学习规划助手 | ❌   | studyclaw, tutoring                  |
| `language-learner` | 语言学习助手 | ❌   | studyclaw, translation, quiz         |

### Agent Workspace 路径

```
~/.studyclaw/
├── workspace/           # 默认 workspace
└── workspaces/
    ├── ai-tutor/        # AI 导师 workspace
    ├── homework-grader/ # 作业批改 workspace
    ├── learning-planner/# 学习规划 workspace
    └── language-learner/# 语言学习 workspace
```

---

## Skills 目录结构

```
skills/
├── studyclaw/           # 核心功能
├── tutoring/            # 辅导教学
├── problem-solving/     # 问题解答
├── grading/             # 作业批改
├── translation/         # 翻译支持
├── quiz/                # 测验生成
└── downloaded/          # 从 ClawHub 下载的 skills
    ├── english-learn-cards/
    ├── adaptivetest/
    ├── curriculum-generator/
    └── adaptive-learning-agents/
```

---

## 开发指南

### 环境要求

- Node.js ≥22
- pnpm (推荐) 或 npm

### 常用命令

```bash
# 安装依赖
pnpm install

# 构建
pnpm build

# 类型检查
pnpm tsgo

# 代码检查
pnpm check

# 运行测试
pnpm test

# 启动开发环境
pnpm dev

# 启动网关
pnpm studyclaw gateway --port 18789
```

### 代码风格

- TypeScript (ESM)
- 严格类型检查，避免 `any`
- 文件控制在 ~500 行内
- 添加必要的注释说明复杂逻辑

---

## 命名约定

| 场景          | 命名                       |
| ------------- | -------------------------- |
| 产品/文档标题 | **StudyClaw**              |
| CLI 命令      | `studyclaw`                |
| 包名          | `studyclaw`                |
| 配置文件      | `openclaw.json` (保持兼容) |
| 数据目录      | `~/.studyclaw/`            |

---

## Git 工作流

### 提交信息格式

```
<scope>: <description>

# 示例
agent: add new language-learner agent
skill: update tutoring skill with SRS support
docs: update README with quick start guide
```

### 分支策略

- `main` — 稳定版本
- `develop` — 开发版本
- `feature/*` — 功能分支
- `fix/*` — 修复分支

---

## 文档链接

- [OpenClaw 文档](https://docs.openclaw.ai)
- [ClawHub Skills 市场](https://clawhub.ai)
- [OpenClaw GitHub](https://github.com/openclaw/openclaw)

---

## 联系方式

- **用户**: 小路
- **邮箱**: ycl_pj@163.com

---

## 更新日志

| 日期       | 变更                     |
| ---------- | ------------------------ |
| 2026-03-10 | 创建 StudyClaw AGENTS.md |
