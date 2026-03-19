# 崽子 OS：基于 OpenClaw 的长期协作型 AI 员工系统

> 一个基于 OpenClaw 的长期协作型 AI 员工系统，围绕高效沟通、连续性记忆、自我校准、技能沉淀和效率监督，解决 AI 助手长期使用中的失忆、跑偏、模板化和上下文膨胀问题。

## 项目简介

**崽子 OS** 是一个基于 OpenClaw 搭建的长期协作型 AI 员工系统。

它不只是一个“能聊天”的助手，而是一个能够在长期使用中持续保持角色一致性、沟通效率、上下文连续性与自我校准能力的个人生产力系统。

在真实使用过程中，我围绕自己的工作流，逐步把 OpenClaw 从一个即时对话工具，打磨成一个能够长期协助我进行内容运营、工作复盘、效率监督、模型切换、知识沉淀与 skill 封装的 AI 员工。

这个项目重点解决了几个长期使用 AI 助手时非常真实的问题：

- 聊久了之后上下文越来越重，效率越来越低
- 助手容易变得模板化、失去原本的人格与协作感
- 沟通意图不清晰，导致误判、过度输出和重复返工
- 解决过的问题容易停留在聊天记录里，无法沉淀为可复用能力

## 核心能力

### 1. 高效沟通协议
通过【同步 / 快答 / 分析 / 执行 / 存档】五种用途标签，降低误判和上下文膨胀。

对应 skill：
- `openclaw-communication-protocol`

### 2. 长期连续性系统
将即时会话、长期记忆、协作协议、自我校准分层管理，让 AI 助手长期使用后仍然稳定、轻量、可持续。

对应 skill：
- `agent-continuity-system`

### 3. 自我校准机制
当助手逐渐变得像“标准助手”、失去角色感时，能够识别并拉回正确的人格与表达方式。

对应 skill：
- `agent-self-calibration`

### 4. Skill 机会雷达
在长期协作中，自动识别哪些重复解决的问题已经值得沉淀成 skill，避免经验只留在聊天记录里。

对应 skill：
- `skill-opportunity-radar`

### 5. GitHub 项目发布工作流
把一个本地项目从零整理成可发布的 GitHub 仓库，包括仓库结构整理、README 撰写、补充文档、git 初始化、远程仓库推送与常见报错排查。

对应 skill：
- `github-project-publisher`

### 6. 模型切换、短回复保护与重试防护
在 IM 对话中直接切换主模型，并在模型切换、gateway 重启、会话恢复等脆弱窗口里进入短回复保护模式，减少重复回复、半截重发和额外消耗。

对应 skill：
- `message-idempotency-and-retry-guard`

### 7. 效率监督与执行纠偏
结合真实工作周报和复盘，让 AI 助手从“回答问题”升级为“监督执行”。

## 仓库结构

```text
zaizi-os/
├── README.md
├── docs/
│   ├── project-description.md
│   └── repo-description.md
├── skills/
│   ├── openclaw-communication-protocol/
│   ├── agent-self-calibration/
│   ├── agent-continuity-system/
│   └── skill-opportunity-radar/
└── dist/
    ├── openclaw-communication-protocol.skill
    ├── agent-self-calibration.skill
    ├── agent-continuity-system.skill
    └── skill-opportunity-radar.skill
```

## 适合谁

这个项目适合：
- 想把 OpenClaw 从“聊天工具”升级成“长期协作伙伴”的人
- 想降低 AI 助手误判、跑偏、失忆、模板化问题的人
- 想把长期对话经验沉淀成 skill 和方法论的人
- 想让 AI 真正参与个人生产力系统建设的人

## 快速使用

### 方式一：直接安装 skill 包（推荐）
1. 前往 `dist/` 目录，选择需要的 `.skill` 包
2. 导入到你的 OpenClaw 环境
3. 根据自己的协作风格调整协议和角色设定

### 方式二：让你的 OpenClaw 读取仓库学习
1. 把仓库链接发给你的 OpenClaw：
   <https://github.com/zaizhi-1112/zaizi-os>
2. 让它读取仓库中的 README、docs 和 skills
3. 根据你的环境导入或复用这些能力

### 注意
- 仓库需保持公开可访问
- 不同 OpenClaw 环境对 GitHub 读取、skill 导入和工具权限支持不同
- 最稳定的方式仍然是直接使用 `dist/` 里的 `.skill` 包

## 当前包含的 skills

- `openclaw-communication-protocol`
- `agent-self-calibration`
- `agent-continuity-system`
- `skill-opportunity-radar`
- `github-project-publisher`
- `message-idempotency-and-retry-guard`

## 项目定位

这个项目想证明的不是“AI 可以做很多事”，而是：

**AI 助手在长期协作场景下，如何从一次性工具，进化成真正能长期陪跑、持续提效、不断沉淀方法的个人生产力操作系统。**
�何从一次性工具，进化成真正能长期陪跑、持续提效、不断沉淀方法的个人生产力操作系统。**
