---
name: hushichaxun-project
description: 护士资格查询+法律维权文书项目，四川省执业护士系统API查询+python-docx生成投诉模板和法律指南
metadata: 
  node_type: memory
  type: project
  originSessionId: 581cc4cd-be8c-4e9d-9d13-c6f7c0ab72d8
---

# hushichaxun — 护士查询与法律维权

**路径**: `D:\AI\mywork\hushichaxun`
**Git**: github.com/menglei3002/hushichaxun (私有仓库)

## 项目背景
用户父亲2026年癌症去世，再婚妻子王英及其女儿邓雨婷（继女，无血缘关系）私藏骨灰、拒不告知安葬地点、侵占全部遗产。邓雨婷是成都成华寰亚医院执业护师（证书编号201251008743，有效期至2027-07-31）。

## 核心功能

### 1. 护士执业资格查询
- **`query_nurse.py`** — 核心脚本，调用四川省政务服务网API (tftb.sczwfw.gov.cn)，AES-256-ECB加密通信
- **`query_dengyuting_now.py`** — 实时查询邓雨婷在三家医院的执业状态
- 已确认：邓雨婷在成都成华寰亚医院，护师，证书有效

### 2. 法律维权文档生成
- **`generate_inheritance_guide.py`** → `遗产继承与骨灰追索_法律维权指南_v3.docx`
  - 亲属关系分析（继女继承权判断标准）
  - 遗产分配公式（两种情况）
  - 五步行动方案
- **`generate_lawyer_templates.py`** → `法律投诉文书_三合一_v2.docx`（最新版）
  - 模板一：致成华区卫健局实名举报信（护士职业道德）
  - 模板二：致成都成华寰亚医院正式投诉函
  - 模板三：致成华区公安分局刑事报案书（侵占罪）
  - 含证据清单、录音文字稿、法律条文索引
- **`generate_response_plan.py`** → `应对方案与投诉模板_基于录音.docx`
- **`generate_nurse_complaint.py`** → `护士投诉举报全方位指南.docx`
- **`generate_radiation_report.py`** → `放射设备投诉举报指南.docx`
- **`generate_report.py`** → `成都成华寰亚医院_投诉指南.docx`

### 3. 录音证据
- 通话录音文字整理稿（已转录）
- 关键内容：邓雨婷承认参与遗体处理并知晓安葬地点但拒绝告知

## 关键技术
- Python AES-256-ECB 加密/解密（PKCS7 padding / zero padding）
- python-docx 生成专业法律文书
- Google SpeechRecognition 中文语音转文字
- ffmpeg 音频格式转换

## 案件关键事实（2026-05-26）
- 被继承人：用户父亲，2026年癌症去世
- 王英：被继承人再婚配偶，下落不明/回避
- 邓雨婷：王英之女，无血缘继女，成都成华寰亚医院护师
- 母女私藏骨灰、拒不告知安葬地点、侵占全部遗产
- 对方以"再找就报警"相威胁（尚未请律师）
- 用户核心诉求：拿回骨灰、知道安葬地址、分得遗产
