# StudyClaw Core Skill

## 概述

StudyClaw 核心技能，提供教育场景的基础上下文和通用功能。

## 功能

### 1. 教育上下文理解

- 识别学习场景类型（解题、讲解、练习等）
- 理解学科领域（数学、语文、英语、物理、化学等）
- 适配学习者水平（小学、初中、高中、大学）

### 2. 学习风格适配

- 根据用户反馈调整解释方式
- 支持视觉、文字、步骤化等不同风格
- 记住用户偏好以便后续交互

### 3. 教育内容生成规范

- 内容准确、有教育价值
- 语言适合目标学习者水平
- 提供必要的背景知识
- 鼓励批判性思维

## 使用场景

```
User: "帮我理解这个物理概念"
AI: [使用 StudyClaw 上下文，识别学科和水平，提供适合的解释]
```

## 配置

```json
{
  "skill": "studyclaw",
  "config": {
    "defaultLevel": "auto",
    "language": "zh-CN",
    "encourageQuestions": true
  }
}
```

## 与其他 Skill 的关系

- 作为基础 skill 被所有教育 Agent 使用
- 提供 `tutoring`、`problem-solving` 等共享上下文
- 可与其他 skill 组合使用

---

_StudyClaw — 让学习更智能_
