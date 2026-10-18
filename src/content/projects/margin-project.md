---
title: "页间 - Margins"
slug: margin-project
published: 2026-10-10
draft: false
order: 100
description: "专属于【我们】的应用。"
image: "images/project0.jpg"
status: "planning"
tags:
  - 笔记
---

::github{repo="Luomic/Margins"}

## 产品定位

> 本地优先、超强自定义、MD3 设计的个人效率软件，集「记账、便签、学习」于一体。

---

## 信息架构

- 账本 快速记账，顺手无脑 记账、分类、自动意图推断、自定义规则

- 便签 随手记录与结构化记事 随心记、记事

- 学习 分学科知识管理 数学、英语、计算机、自定义学科块

- 全局能力：AI 助手、搜索、通知提醒、设置/自定义、模型管理、API Key 管理。

---

## 技术方向

- 平台：安卓优先。

- 技术栈：`Kotlin` + `Jetpack Compose` + `Material Design 3`

- 渲染：`Markdown` 可视化编辑器 + `KaTeX` 类公式渲染。

- 手写转 `LaTeX`

- AI：`llama.cpp` JNI 集成，GGUF 模型下载管理；在线模型走可配置 Provider。

---