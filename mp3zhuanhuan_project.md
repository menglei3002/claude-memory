---
name: mp3zhuanhuan-project
description: 音乐加密解密转MP3桌面工具 — QQ音乐/网易云/酷狗/酷我加密格式解密转标准格式
metadata: 
  node_type: memory
  type: project
  originSessionId: db77a346-2596-4c79-96dc-33b2dcb526a2
---

# 音乐加密解密转MP3

桌面端万能音频格式转换工具，支持 QQ 音乐、酷狗、酷我等平台的加密歌曲解密并转码为标准格式。

**位置**: `D:\AI\mp3zhuanhuan`
**Git**: `github.com/menglei3002/mp3zhuanhuan`
**当前版本**: v1.0
**状态**: 已发布，有安装包和使用手册

**支持的加密格式**:
- NCM (网易云) — takiyasha 纯 Python 库
- QMC/QMC0/QMC3/QMC4/QMCv2 (QQ 音乐旧版) — takiyasha
- MGG/MFLAC (QQ 音乐 musicex) — Frida 17.x 动态注入，需 QQ 音乐客户端运行
- KGM/KGMA/VPR (酷狗) — takiyasha
- KWM (酷我) — takiyasha

**输出格式**: MP3(320kbps), OGG, FLAC, WAV, AAC(320kbps), Opus(256kbps)

**技术栈**:
- GUI: tkinter + tkinterdnd2 (拖放支持)
- 解密: Frida 17.x + takiyasha
- 转码: FFmpeg (`dist/ffmpeg.exe`)
- 打包: PyInstaller (安装包含 FFmpeg，无需 Python 环境)
- 主程序: `build_gui.py` → 打包为 exe

**关键文件**:
- `build_gui.py` — 主程序源码
- `build_exe.py` / `build_gui.py` — PyInstaller 打包脚本
- `installer.py` — NSIS 风格安装器
- `音乐加密解密转MP3.spec` / `音乐加密解密转MP3_安装包.spec` — PyInstaller spec
- `使用手册.txt` — 用户手册
- `音乐加密解密转MP3_广告文案.docx` — 营销文案
- `hook_qq_music.js` — Frida 注入脚本 (QQ 音乐 musicex 解密)
- `dist/ffmpeg.exe` — 完整版 FFmpeg (也用于 AIMUSIC 项目)

**配置路径**:
- 配置文件: `%APPDATA%\音乐加密解密转MP3\config.json`
- 缓存目录: `%TEMP%\qqmusic_convert_cache`
- 安装路径: `%LocalAppData%\Programs\音乐加密解密转MP3` (无需管理员权限)

**待办**:
- [ ] 创建 GitHub 远程仓库并推送
