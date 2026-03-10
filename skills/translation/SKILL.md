# Translation Skill

## 概述

翻译技能，提供多语言翻译和语言学习支持。

## 功能

### 1. 精准翻译

- 支持多种语言对
- 保留原文语气和风格
- 处理专业术语
- 提供多种译法选择

### 2. 逐句解析

- 语法结构分析
- 词汇用法解释
- 文化背景补充
- 常见表达方式

### 3. 学习模式

- 标注关键词汇
- 提供发音指南
- 关联语法知识点
- 生成练习题

### 4. 对比学习

- 并列显示原文和译文
- 高亮翻译难点
- 对比不同译法
- 解释翻译选择

## 支持的语言

| 语言     | 代码  | 状态 |
| -------- | ----- | ---- |
| 中文     | zh-CN | ✅   |
| 英文     | en    | ✅   |
| 日文     | ja    | ✅   |
| 韩文     | ko    | ✅   |
| 法文     | fr    | ✅   |
| 德文     | de    | ✅   |
| 西班牙文 | es    | ✅   |
| 俄文     | ru    | ✅   |

## 使用场景

### 基础翻译

```
User: "翻译：The quick brown fox jumps over the lazy dog."
AI: "**翻译结果：**
     敏捷的棕色狐狸跳过了懒狗。

     **词汇解析：**
     - quick = 敏捷的、快速的
     - brown = 棕色的
     - fox = 狐狸
     - jump over = 跳过
     - lazy = 懒惰的

     **语法要点：**
     这是一句包含所有英文字母的经典句子，常用于测试字体显示效果。"
```

### 学习模式

```
User: "帮我学习这句话：I have been studying English for three years."
AI: "**句子分析：**

     I have been studying English for three years.
     我已经学习英语三年了。

     **语法重点：现在完成进行时**
     结构：have/has been + doing
     含义：从过去开始，持续到现在，还在继续

     **关键词汇：**
     - study = 学习（studies/studying/studied）
     - for + 时间段 = 表示持续时间

     **类似句型：**
     - She has been working here for two years.
     - They have been waiting for an hour.

     **练习：**
     用「have been doing」造一个句子？"
```

## 配置

```json
{
  "skill": "translation",
  "config": {
    "sourceLanguage": "auto",
    "targetLanguage": "zh-CN",
    "showAnalysis": true,
    "learningMode": true,
    "preserveStyle": true
  }
}
```

---

_StudyClaw — 让学习更智能_
