---
name: pdfgod-project
description: PDFGOD — Tauri 桌面 PDF 全能转换工具，当前状态、进度、后续方案
metadata: 
  node_type: memory
  type: project
  originSessionId: 21f1b9c2-e8be-40ce-b2c4-a25d16235fbd
---

PDFGOD 是一个基于 Tauri 的 Windows 桌面 PDF 全能转换工具。

**路径:** `D:\AI\mywork\PDFGOD\`
**远程仓库:** https://github.com/menglei3002/PDFGOD (git@github.com:menglei3002/PDFGOD.git)
**技术栈:** Tauri (Rust + Web 前端) + Python 后端引擎
**当前版本:** 0.1.0 (MVP)
**最近提交 (2026-05-26):** `39ad339` — UX 重构 + OCR 引擎 + 编码修复

## 转换引擎 (位于 `engine/`)
- `pdf_to_word.py` — PDF 转 Word (pdf2docx)
- `pdf_to_txt.py` — PDF 转文本 (PyMuPDF + pdfplumber)
- `pdf_to_image.py` — PDF 转图片 (PyMuPDF)
- `pdf_to_excel.py` — PDF 转 Excel (camelot + tabula + openpyxl 后备)
- `pdf_to_ppt.py` — PDF 转 PPT (pdf2image + python-pptx)
- `pdf_ocr.py` — PDF OCR 识别 (PaddleOCR v3 + Tesseract 后备)

## 最新完成的工作
- OCR 引擎完善：PaddleOCR v3 API 适配、oneDNN bug 规避、模型缓存迁 D 盘
- 编码问题修复：Python stdout UTF-8 + Rust from_utf8_lossy 处理中文路径
- UX 重构：格式优先选择 → 多文件管理 → 批量逐文件转换
- 纯黑主题，无第三方 UI 组件库
- 输出路径选择改用动态 import 方案

## 已知限制
- **Excel 引擎弱**：camelot 需 Ghostscript、tabula 需 Java，否则仅创建空 Excel
- **pdf2docx 不保留字体**：PDF 存储位置字形，不存储字体名
- **Save Dialog 不稳定**：动态 import 方案待验证，备选用 open dialog 选目录
- **窗口固定 620x700**：不可缩放，批量结果空间紧张

## 后续方案（待确认优先级）

### 第一优先级：验证 + 修复
1. 端到端测试每种格式，确认 UX 重构无回归
2. Save Dialog 彻底修复（备选：用 open dialog 选目录）
3. 结果卡片增加"打开文件"和"打开目录"按钮

### 第二优先级：功能增强
4. Excel 引擎强化（pdfplumber 纯 Python 方案减少外部依赖）
5. 转换选项面板（图片 DPI、页面范围、OCR 语言选择）
6. 取消转换按钮

### 第三优先级：体验升级
7. 窗口可缩放
8. 本地历史记录持久化
9. GitHub Release + NSIS 安装包发布
