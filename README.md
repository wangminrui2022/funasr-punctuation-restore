# FunASR 标点恢复 - OpenClaw 技能（v1.5.1）

[![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-blue)](https://clawhub.ai)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

**一句话功能**：使用 FunASR 官方 ct-punc 模型，为**一段文本、单个记事本文件、或整个目录**一键恢复标点符号。

**目录模式亮点**：输入目录 `D:\my_notes` → 自动在同级生成 `my_notes_punctuated`，**结构 100% 一致**，文件名不变，原目录完全不修改！

## ✨ 特性一览
- ✅ 支持纯文本 / 单文件 / 目录三种模式
- ✅ **目录镜像输出**（同级 `_punctuated` 文件夹，结构+文件名完全一致）
- ✅ GPU 自动加速 + 推理后自动清理显存（防内存泄漏）
- ✅ 模型永久缓存到 `./models/damo/punc_ct-transformer_cn-en-common-vocab471067-large`
- ✅ 下载失败时自动弹出超友好手动下载指南
- ✅ 跨平台（Windows/Linux/macOS）

## 🚀 快速安装 & 使用

```bash
# 1. 克隆到 OpenClaw 技能目录
git clone https://github.com/你的用户名/funasr-punctuation-restore.git ~/.openclaw/skills/funasr-punctuation-restore

# 2. 进入目录并安装依赖
cd ~/.openclaw/skills/funasr-punctuation-restore
pip install funasr modelscope torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121

# 3. 测试三种模式
python scripts/punctuation_restore.py --text "测试文本恢复标点"
python scripts/punctuation_restore.py --file "D:\test.txt"
python scripts/punctuation_restore.py --dir "D:\我的笔记"   # ← 推荐！