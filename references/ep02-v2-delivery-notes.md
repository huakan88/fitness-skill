# Ep.02 v2 交付浓缩笔记（三点必改 · 过眼通过）

- **题名（池 #2）**：不胖，小腹为什么先往前拱？
- **channelLabel**：工作族有好身材 · 不胖，小腹为什么先往前拱？
- **交付时**：2026-10-31 约 21:35 America/Adak（UTC-9）
- **规格**：1080×1920 · 30fps · 约 **123.4 s** · Integrated **−16.2 LUFS**
- **旁白**：刘飞 · rate=−5 · 口语 v2 语义未改（未重切旁白轨）
- **定妆**：v3；动作仍 TX-HK H3 R2V follow-clean（v2 **未重渲 H3**，改在 Remotion 叠层）
- **终稿名**：`out/ep02-v2.mp4`（`out/ep02.mp4` 仅对照，勿当终稿）

## 侃华三点必改落地（成片硬规则来源）

### 1. 动作流畅 + 髋关键姿势讲解
- FollowClip 略收构图（约 108% cover + center 38%）降漂移。
- 死虫：`TeachCallout`「髋关节怎么动：几乎不动。腿在伸，骨盆像钉在床上。」+ `PelvisBrace`「骨盆稳住」。
- 收肋：`TeachCallout`「髋与骨盆：坐骨压住椅面。肋骨往下收，髋别跟着前倒。」+ `PelvisBrace`「髋·骨盆坐稳」。
- 叠字级讲解即可；若需真插极短旁白句，另轮补录对齐。

### 2. 肌肉标注（红标 + 旁侧字 · 禁糊一团）

| 段 | 标签示例 |
|----|----------|
| 科学 | 髋关节（底座铰链） |
| 死虫 | 腹直肌 / 腹横肌 / **髋关节** |
| 收肋 | 腹直肌 / 腹横肌 / 臀大肌 / **髋关节** |
| 做错分屏 | 腹直肌 + 髋关节 |

实现：`MuscleTag`（锚点红环 + 折线引线 + 旁侧字牌）。

### 3. 动作引导线
- 死虫：手臂/对侧腿慢伸 · `TrajectoryArc` + `GuideArrow`
- 收肋：肋骨下沉 ↓ · 轻夹臀轨迹 · `GuideArrow`

## 动作 clip 映射

| 段 | 文件模式 |
|----|----------|
| 死虫 | `clips/deadbug-follow-clean.mp4` |
| 收肋+轻夹臀 | `clips/rib-follow-clean.mp4` |
| 做错 | `clips/wrong-follow-clean.mp4` |
| Hook/科学/CTA | v3 静图 + Remotion |

## 复用检查清单

- [x] 三点视觉可验：标签可读、引导线可见、髋讲解瞬间有叠字
- [x] follow-clean + 定妆 v3；无外部视频 API；无诊疗主画面
- [x] Gofile 主备**新**链；旧成片勿交

> 叠层 API 摘要见 `remotion-layers-notes.md`。原完整 DELIVERY：`fitness-ep02-2026-11-01/DELIVERY.md`。
