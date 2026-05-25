---
name: pdfgod-project
description: PDFGOD — Tauri 桌面 PDF 全能转换工具，位置、仓库、构建信息
metadata: 
  node_type: memory
  type: project
  originSessionId: cfec81be-822b-4513-b3f8-1340603dda5c
---

PDFGOD 是一个基于 Tauri 的 Windows 桌面 PDF 全能转换工具。

**路径:** `D:\AI\mywork\PDFGOD\`
**远程仓库:** https://github.com/menglei3002/PDFGOD (git@github.com:menglei3002/PDFGOD.git)
**技术栈:** Tauri (Rust + Web 前端) + Python 后端引擎

**转换引擎 (位于 `engine/`):**
- `pdf_to_word.py` — PDF 转 Word
- `pdf_to_txt.py` — PDF 转文本
- `pdf_to_image.py` — PDF 转图片
- `pdf_to_excel.py` — PDF 转 Excel
- `pdf_to_ppt.py` — PDF 转 PPT
- `pdf_ocr.py` — PDF OCR 识别

**可执行文件:** `src-tauri/target/release/bundle/nsis/PDFGOD/pdfgod.exe`
**当前版本:** 0.1.0 (MVP)
