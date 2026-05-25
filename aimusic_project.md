---
name: aimusic-project
description: AI Music Factory at D:\AI\mywork\AIMUSIC — 批量生成搞笑/打工人短视频歌曲
metadata: 
  node_type: memory
  type: project
  originSessionId: db77a346-2596-4c79-96dc-33b2dcb526a2
---

# AI Music Factory

AI 音乐工厂项目，批量生产搞笑/打工人短视频歌曲，发布到抖音和 B 站。

**位置**: `D:\AI\mywork\AIMUSIC`
**Git**: `git@github.com:menglei3002/my-knowledge.git` (branch: `aimusic`)
**流水线**: 选题 → 歌词 → Suno/ACE-Step 音乐 → FFmpeg/剪映视频 → 发布

**关键工具**:
- ACE-Step API: `D:\AI\mywork\myshipintest\claude-code-video-toolkit\tools\music_gen.py` (ACEMUSIC_API_KEY 已配置)
- FFmpeg: `D:\AI\mp3zhuanhuan\dist\ffmpeg.exe` (完整版，支持 libass/libx264)
- capcut-mate: `localhost:30000` 启动命令 `cd D:\AI\mywork\myshipintest\claude-code-video-toolkit\_external\capcut-mate && uv run main.py`
- 剪映 CLI: `D:\AI\mywork\myshipintest\claude-code-video-toolkit\tools\jianying.py`

**ACE-Step 生成参数**:
- provider: acemusic (acemusic.ai)
- 需要 NO_PROXY="*" 绕过代理
- 中文歌词使用 --vocal-language zh --no-thinking（thinking 模式会 504 超时）
- 3 variations 需分别调用（variations>1 会超时）

**当前歌曲**: 《班味太重》(打工人发疯版)
- 最新音频: `output/songs/banwei_gen2_v2.mp3` (ACE-Step, 30s)
- v2 表情包视频: `output/videos/banwei_v2_meme.mp4` (1080x1920, 10 meme + Lumina 数字人 + 字幕)

**上一首**: 《我不是不努力 我只是先躺一下》— 歌词完成，音乐待生成
