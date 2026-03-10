# 📚 StudyClaw — Educational AI Assistant Platform

<p align="center">
  <strong>AI-Powered Learning, Anytime, Anywhere</strong>
</p>

<p align="center">
  <a href="https://studyclaw.org"><img src="https://img.shields.io/badge/Website-studyclaw.org-blue?style=for-the-badge" alt="Website"></a>
  <a href="https://studyclaw.7color.vip"><img src="https://img.shields.io/badge/China-studyclaw.7color.vip-red?style=for-the-badge" alt="China"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge" alt="MIT License"></a>
</p>

**StudyClaw** is an educational AI assistant platform built on [OpenClaw](https://github.com/openclaw/openclaw), designed specifically for learning scenarios. It comes with built-in educational agents and skills to help students learn smarter, not harder.

## ✨ Features

### Built-in Educational Agents

| Agent                               | Description                                          | Skills                               |
| ----------------------------------- | ---------------------------------------------------- | ------------------------------------ |
| **AI 导师** (ai-tutor)              | Personal AI tutor for one-on-one learning assistance | studyclaw, tutoring, problem-solving |
| **作业批改助手** (homework-grader)  | Intelligent homework grading and feedback            | studyclaw, grading, problem-solving  |
| **学习规划助手** (learning-planner) | Study plan creation and progress tracking            | studyclaw, tutoring                  |
| **语言学习助手** (language-learner) | Language learning with translation and quizzes       | studyclaw, translation, quiz         |

### Built-in Skills

| Skill               | Description                              |
| ------------------- | ---------------------------------------- |
| **studyclaw**       | Core StudyClaw functionality and context |
| **tutoring**        | Personalized tutoring and explanation    |
| **problem-solving** | Step-by-step problem solving guidance    |
| **grading**         | Homework and assignment grading          |
| **translation**     | Multi-language translation support       |
| **quiz**            | Quiz generation and assessment           |

### Downloaded Educational Skills (from ClawHub)

- **english-learn-cards** — Flashcard English vocabulary learning (SQLite + SRS)
- **adaptivetest** — Adaptive testing engine (IRT/CAT)
- **curriculum-generator** — Intelligent curriculum generation
- **adaptive-learning-agents** — Real-time learning from errors and corrections

## 🚀 Quick Start

### Prerequisites

- Node.js ≥22
- npm, pnpm, or bun

### Installation

```bash
# Clone the repository
git clone https://github.com/openclaw/studyclaw.git
cd studyclaw

# Install dependencies
pnpm install

# Build
pnpm build

# Start the gateway
pnpm studyclaw gateway --port 18789
```

### Configuration

StudyClaw uses `openclaw.json` for configuration. The default configuration includes:

```json
{
  "agents": {
    "defaults": {
      "workspace": "~/.studyclaw/workspace"
    },
    "list": [
      {
        "id": "ai-tutor",
        "name": "AI 导师",
        "default": true,
        "workspace": "~/.studyclaw/workspaces/ai-tutor",
        "skills": ["studyclaw", "tutoring", "problem-solving"]
      },
      {
        "id": "homework-grader",
        "name": "作业批改助手",
        "workspace": "~/.studyclaw/workspaces/homework-grader",
        "skills": ["studyclaw", "grading", "problem-solving"]
      },
      {
        "id": "learning-planner",
        "name": "学习规划助手",
        "workspace": "~/.studyclaw/workspaces/learning-planner",
        "skills": ["studyclaw", "tutoring"]
      },
      {
        "id": "language-learner",
        "name": "语言学习助手",
        "workspace": "~/.studyclaw/workspaces/language-learner",
        "skills": ["studyclaw", "translation", "quiz"]
      }
    ]
  }
}
```

## 📖 Use Cases

### 1. AI Tutoring

```
User: "Can you explain how to solve quadratic equations?"
AI Tutor: [Provides step-by-step explanation with examples]
```

### 2. Homework Grading

```
User: [Uploads homework image]
Homework Grader: [Analyzes and provides detailed feedback]
```

### 3. Study Planning

```
User: "Help me create a study plan for my final exams"
Learning Planner: [Creates personalized study schedule]
```

### 4. Language Learning

```
User: "Teach me Spanish vocabulary for travel"
Language Learner: [Provides lessons, translations, and quizzes]
```

## 🔧 Architecture

```
┌─────────────────────────────────┐
│          StudyClaw              │
│     Educational Platform        │
└───────────────┬─────────────────┘
                │
    ┌───────────┼───────────┐
    │           │           │
    ▼           ▼           ▼
┌───────┐  ┌───────┐  ┌───────┐
│Agent 1│  │Agent 2│  │Agent N│
│AI Tutor│ │Grader │  │Learner│
└───┬───┘  └───┬───┘  └───┬───┘
    │          │          │
    └──────────┼──────────┘
               │
               ▼
┌─────────────────────────────────┐
│       OpenClaw Gateway          │
│     ws://127.0.0.1:18789        │
└─────────────────────────────────┘
```

## 🌐 Deployment

### Global

- Website: https://studyclaw.org

### China

- Website: https://studyclaw.7color.vip

## 📚 Documentation

- [Getting Started](docs/getting-started.md)
- [Agent Configuration](docs/agents.md)
- [Skills Development](docs/skills.md)
- [API Reference](docs/api.md)

## 🤝 Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## 📄 License

MIT License - see [LICENSE](LICENSE) for details.

## 🙏 Acknowledgments

StudyClaw is built on top of [OpenClaw](https://github.com/openclaw/openclaw), an open-source personal AI assistant platform. Special thanks to the OpenClaw team and community.

---

**StudyClaw** — Making Learning Smarter, Together. 📚✨
