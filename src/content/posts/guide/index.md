---
title: 基于 Kotlin + Jetpack Compse 的 Android Latex 手写识别实现的思考
published: 2026-10-19
pinned: true
description: 关于原生安卓开发下的一些博客
image: https://jetpackcompose.cn/assets/images/demo4-541a9b9ed26bef86e75b05fbeecc51f6.gif
tags:
  - Kotlin
  - Android
  - Compose
category: 安卓开发
series: 杂谈
seriesOrder: 1
---

# 安卓开发的学习博客

## 前言

> 最近想着将自己的一些想法，转换为便捷、可操作的一些应用程序
> 其中就包括基于`ONNX Runtime`快速输出`Latex`数学块、基于`llama.cpp`离线运行本地量化翻译模型。
> 关于这方面技术和生态都比较成熟，底层架构涉及知识盲区，不作讨论。

首先在 `build.gradle` 引入 `OONX Runtime`

```kts
dependencies {
    implementation("com.microsoft.onnxruntime:onnxruntime-android:1.19.0")
}
```

> 注意需要先去 `HuggingFace` 等网站，寻找适配的 `onnx` 模型。

一个完整的识别模型一般包含以下文件

```mermaid
flowchart TB
    root["需求文件"]
    root --- f1["encoder_model.onnx"]
    root --- f2["decoder_model.onnx"]
    root --- f3["config.json"]
    root --- f4["generation_config.json"]
    root --- f5["preprocessor_config.json"]
    root --- f6["tokenizer.json"]
    root --- f7["tokenizer_config.json"]
    root --- f8["special_tokens_map.json"]
```

## kt 大致框架（也可以直接在MainActivity完成所有逻辑）

- MainActivity(主界面)
- Canvas(手写画布逻辑)
- ToBitmap(Canvas转位图)
- LatexPreview(Latex预览)
- Tokenizer(编码解码ONNX的输出)
- FormularRecognizer(识别器)


## 大致代码流程

```kt
LaunchedEffect(strokes.size, recognizer) {

        val r = recognizer ?: return@LaunchedEffect

        if (strokes.isEmpty()) return@LaunchedEffect

        delay(700)

        val bmp = strokesToBitmap(strokes.toList()) ?: return@LaunchedEffect

        status = "识别中…"

        try {

            val t0 = System.currentTimeMillis()

            val result = withContext(Dispatchers.Default) { r.recognize(bmp) }

            latex = result

            status = "完成，用时 ${System.currentTimeMillis() - t0} ms"

        } catch (e: CancellationException) {

            throw e

        } catch (e: Throwable) {

            status = "识别失败：${e.message}"

        }

    }
```