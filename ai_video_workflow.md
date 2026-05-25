---
name: ai-video-workflow
description: AI视频项目工作流演进 — FFmpeg自动装配 + 剪映手动精调
metadata:
  node_type: memory
  type: project
  originSessionId: 5e718d5d-7c39-484c-9b0d-2b7403a283e1
---

# AI 视频制作工作流（经过两个项目验证）

## 当前最佳方案

**FFmpeg 负责自动化装配**：
- 图片序列 → 视频背景（concat demuxer）
- ASS 字幕烧录（libass，支持中文描边/阴影）
- 数字人/LOGO overlay
- 精确音画对齐（ffprobe 获取时长 + `-t` 精确截断）
- 可靠、可复现、无黑盒问题 → 见 [[ffmpeg-video-compose]]

**剪映负责手动精调**：
- 调色、转场、特效
- 需要实时预览的编辑
- 不适合自动化管线（capcut-mate 加密草稿不兼容本地剪映 Pro）

## 项目验证

| 项目 | 工具 | 结果 |
|------|------|------|
| 《推开世界的门》MV | Hailuo AI + FFmpeg | 成功（手工字幕时间轴较痛苦） |
| 《班味太重》v2 | ACE-Step + FFmpeg | 成功（ASS 字幕自动化，~1.2MB/30s） |
| 《班味太重》capcut-mate 尝试 | capcut-mate API | 失败（图片消失、音画不同步、数字人不可见） |

## 经验教训

- 自动化管线用 FFmpeg，不要用剪映 API（加密格式不兼容）
- 剪映适合最终手动精调，不适合从零自动装配
- FFmpeg 必须用 gyan.dev 完整版（`D:\AI\mp3zhuanhuan\dist\ffmpeg.exe`），剪映自带版本缺少 libass/libx264
- ASS 字幕比 SRT 更适合中文（描边、阴影、精确定位）
