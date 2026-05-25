---
name: ai-video-workflow
description: "User's first AI video project workflow and lessons learned"
metadata: 
  node_type: memory
  type: project
  originSessionId: 5e718d5d-7c39-484c-9b0d-2b7403a283e1
---

User completed first AI video project: MV for 杨乃文《推开世界的门》

Workflow:
- Concept doc at D:\AI\mywork\wenzizhengli\
- AI video generation via Hailuo AI (free, 200 credits on first login)
- Shots saved to D:\AI\mywork\hailuoshipin\
- FFmpeg used for concatenation, subtitle burning, audio overlay
- Final output: D:\AI\mywork\hailuoshipin\推开的世界的门_完整版_v2.mp4

Pain points:
- AI video tools have inconsistent free tiers; Hailuo was the most reliable
- FFmpeg subtitle/audio sync is painful without hearing the audio — user had to manually timestamp lyrics
- Each shot requires separate generation + download

**How to apply:** Next AI video project, recommend using 剪映 (JianyingPro at D:\AI\jianying\JianyingPro) for the full post-production pipeline — stitching, music, subtitles, color grading — all visual/WYSIWYG instead of CLI blind adjustments.
