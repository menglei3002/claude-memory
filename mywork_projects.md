---
name: mywork-projects
description: Complete inventory of all projects under D:\AI\mywork\ with categories and status
metadata: 
  node_type: memory
  type: project
  originSessionId: db77a346-2596-4c79-96dc-33b2dcb526a2
---

# D:\AI\mywork 项目全景

## 活跃项目

### myshipintest — 视频工具测试工作区
- **路径**: `D:\AI\mywork\myshipintest`
- **内容**: claude-code-video-toolkit (git clone from github.com/digitalsamba) + video-studio skill
- **关键工具**:
  - `claude-code-video-toolkit/tools/music_gen.py` — ACE-Step 音乐生成
  - `claude-code-video-toolkit/tools/jianying.py` — 剪映 CLI
  - `claude-code-video-toolkit/tools/flux2.py` — FLUX.2 图片生成
  - `claude-code-video-toolkit/_external/capcut-mate/` — capcut-mate 服务 (uv run main.py)
  - `video-studio/` — FFmpeg 视频编辑管线
- **环境**: ACEMUSIC_API_KEY 已配置; ACE-Step 需要 NO_PROXY="*"

### AIMUSIC — AI 音乐工厂
- 见 [[aimusic-project]]

### hailuoshipin — 海螺 AI 视频
- **路径**: `D:\AI\mywork\hailuoshipin`
- **用途**: 用 MiniMax Hailuo 生成 AI 视频片段，组装成 MV
- **当前作品**: 《推开世界的门》(杨乃文) — 5 个 AI 场景 + 字幕
- **Git**: github.com/menglei3002/hailuoshipin

### PHILIPSCTtube — 飞利浦 CT 球管讲解视频
- **路径**: `D:\AI\mywork\PHILIPSCTtube`
- **用途**: 飞利浦纳米 CT 球管工程深度讲解（8 场景，~9.5 分钟）
- **工具链**: Python 生成背景 + Remotion 3D 动画 + 剪映整合
- **产出**: `philips_nano_ct_tube.mp4` (90 MB，gitignore 排除)
- **Git**: github.com/menglei3002/philips-ct-tube

### xunlian — CT 维修培训内容
- **路径**: `D:\AI\mywork\xunlian`
- **用途**: 飞利浦 Brilliance 64 排 CT 换球管 3D 动画教学视频
- **内容**: 33 镜头脚本 + 维修流程文档 + 3D 制作指南 + 剪映大纲
- **Git**: github.com/menglei3002/xunlian-ct-training

### hushichaxun — 护士资格查询工具
- **路径**: `D:\AI\mywork\hushichaxun`
- **用途**: 爬取四川省政务服务网护士执业资格数据
- **工具**: Python (AES 加密 API 调用) + PowerShell + Bash
- **Git**: github.com/menglei3002/hushichaxun **(私有仓库)**

### wenzizhengli — 文字整理 + 自动存档
- **路径**: `D:\AI\mywork\wenzizhengli`
- **用途**: 视频创作构思文档 + 自动 git 存档脚本
- **关键文件**: `auto-save.sh` — 扫描 `D:/AI/` 下所有 git 仓库自动提交
- **Git**: github.com/menglei3002/wenzizhengli

### QUANJU — 全聚 AI 工作区
- **路径**: `D:\AI\mywork\QUANJU`
- **用途**: 通用 AI 辅助任务工作区，配置了知识库引用
- **Git**: github.com/menglei3002/quanju-ai

### PDFGOD — Tauri PDF 工具
- 见 [[pdfgod-project]]

### mp3zhuanhuan — 音乐加密解密转MP3
- **路径**: `D:\AI\mp3zhuanhuan`
- **用途**: 解密 QQ 音乐/网易云/酷狗/酷我加密歌曲（NCM/MGG/MFLAC/KWM/QMC 等），转 MP3/FLAC/OGG/WAV/AAC/Opus
- **技术**: Python tkinter + Frida 17.x + takiyasha + FFmpeg, PyInstaller 打包
- **Git**: github.com/menglei3002/mp3zhuanhuan
- 见 [[mp3zhuanhuan-project]]

## 轻量/一次性项目

| 项目 | 说明 |
|------|------|
| ceshicundang | 空骨架项目（测试用） |
| cut | 临时图片素材（8 张 PNG） |
| philips | 飞利浦 CT 文档优化（单次格式转换） |
| seedancebushu | 空目录（预留给 Seedance 部署） |
