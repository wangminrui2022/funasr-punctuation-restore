---
name: funasr-punctuation-restore
version: 1.5.1
description: 使用 FunASR ct-punc 模型一键恢复标点（支持文本/文件/目录）。目录模式会在同级创建结构完全一致的 _punctuated 镜像目录（原目录不变）。GPU 加速 + 自动清理显存 + 下载失败美观提示。
author: lao
category: text-processing
tags: [funasr, punctuation, gpu, 目录镜像, 标点恢复, modelscope]
---

# FunASR 标点恢复技能（v1.5.1 最终版）

## 🎯 何时触发本技能
用户提到以下任意情况时立即调用：
- “帮我给这段文字恢复标点”“加标点：xxx”
- “把这个记事本文件恢复标点” + 文件路径
- “把这个文件夹所有记事本文件都恢复标点” + 目录路径

## 📋 执行步骤（Agent 必须严格执行）

1. **进入技能目录**
   ```bash
   cd ~/.openclaw/skills/funasr-punctuation-restore