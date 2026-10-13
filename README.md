# AI Native 软件怎么开发

围绕用户目标，理解 Agent 系统的思考、行动、状态、边界、验证与恢复。

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-blue.svg)](LICENSE)

**作者：陈奕霖** · **语言：简体中文** · **类型：开放文章 / 文档项目**

## 关于这篇文章

这是一份关于 AI Native 软件开发的系统性学习与实践总结。文章从用户希望达成的目标出发，讨论如何组织模型、上下文、Skill、工具和运行机制，以及如何保存业务状态、验证完成结果、守住执行边界并恢复失败任务。

文章采用通俗解释、示例流程和概念拆解的方式，连接产品设计与工程实现。内容体现作者当前的理解，欢迎通过讨论和纠错持续完善。

## 从哪里开始

- **完整阅读**：从[前言](docs/00-preface.md)开始，按章节顺序阅读。
- **先看整体开发方法**：阅读[从 0 到上线](docs/08-from-zero-to-production.md)，再按需返回各专题。
- **快速抓住主线**：用户提出目标 → 系统准备上下文与能力 → Agent 调用工具推进任务 → 持久保存状态与成果 → 验证结果 → 必要时由人介入 → 失败后恢复。

## 阅读目录

| 章节 | 内容 |
| --- | --- |
| 00 | [前言：为什么我想写这篇东西](docs/00-preface.md) |
| 01 | [什么才是 AI native软件](docs/01-what-is-ai-native.md) |
| 02 | [AI Native 软件靠什么思考](docs/02-model-context-skill-instruction.md) |
| 03 | [AI Native 软件到底怎么做事](docs/03-tools-workflow-harness-environment.md) |
| 04 | [怎么保证 AI Native 系统不失忆](docs/04-state-memory-artifact-checkpoint.md) |
| 05 | [怎么保证 AI Native 系统不乱来](docs/05-authority-permission-guardrails.md) |
| 06 | [怎么知道 AI Native 系统真的完成了](docs/06-verification-evaluation.md) |
| 07 | [要是 AI Native 系统失败了怎么办](docs/07-failure-recovery.md) |
| 08 | [从 0 到上线，一个 AI Native 软件到底应该怎么开发](docs/08-from-zero-to-production.md) |

## 主要讨论的问题

- 模型、Instruction、Context 与 Skill 如何共同支持任务判断。
- Tool、Workflow、Agent Loop、Harness 与 Environment 怎样配合完成操作。
- State、Memory、Artifact 与 Checkpoint 如何支持长任务与跨会话恢复。
- Authority、Permission、Guardrail 与 Human Gate 如何限制执行边界。
- Done Criteria、Evidence、Verifier 与 Eval 如何连接任务验收和系统评估。
- Trace、Readback、Idempotency 与 Recovery 如何帮助定位失败并继续执行。

## 适合谁阅读

- 正在设计或交付 AI 应用的产品经理。
- 正在构建 Agent 工具、工作流或运行机制的开发者。
- 希望系统理解 AI Native 软件的学习者。

## 如何参与

欢迎提出概念纠错、表达改进、示例补充和参考资料建议。参与方式见[贡献指南](CONTRIBUTING.md)。

## 许可与引用

本项目文章采用 [Creative Commons Attribution 4.0 International（CC BY 4.0）](LICENSE) 许可。分享或改编时请保留作者署名、注明许可，并标明修改；许可允许商业使用。完整条款以 [LICENSE](LICENSE) 为准。

引用格式示例：

> 陈奕霖，《AI Native 软件怎么开发》，CC BY 4.0。

文章的[飞书原文](https://y1x5u85vkeq.feishu.cn/wiki/O0Dtwbtr1i0leLkm84pcG0gLn1f)可作为来源参考；GitHub 版本为分章阅读整理版。格式整理记录见[版本记录](CHANGELOG.md)。

## 项目文件

```text
ai-native-software-development/
├── README.md
├── docs/                  # 正文，按原章节顺序拆分
├── LICENSE                # CC BY 4.0 官方完整许可文本
├── CONTRIBUTING.md        # 贡献方式与编辑约定
├── CHANGELOG.md            # 版本与整理记录
├── PUBLISHING.md           # GitHub 上传说明
├── .github/ISSUE_TEMPLATE/ # 纠错与建议模板
├── .editorconfig
└── .gitignore
```
