---
name: 健身
description: 做二号抖音「工作族有好身材」增肌减脂/运动科学竖版（暗色极简带皮3D解剖、刀刀 The Rep Theory 节拍）时用；含定妆v3、口播过眼、follow-clean动作、肌群标注与引导线硬规则。
---

# 健身 · 二号抖音「工作族有好身材」

可复用产线 skill。其他 Grok / bot / Agent 克隆本目录即可按同一套规则出片。

## 1. 何时用 / 账号锁死

- **仅二号抖音**健身竖版。总主题固定为 **「工作族有好身材」**（账号系列名，**不是**单集标题）。
- 单集标题取自选题池痛点/反常识题名（见 `references/topic-pool-30ep.md`）。
- **禁混线**：主号生医 / AI / 猫内容、主号品牌角标（如「花花聊科学」）一律不上本号屏。
- 对标画风与节拍：刀刀 X 帖 The Rep Theory 方法（`references/daodao-reptheory-prompt-pack.md`）。

## 2. 开工前先读 references/

| 文件 | 用途 |
|------|------|
| `references/model-v3-readme.md` + `v3-*.jpg` | 定妆锁定：东亚脸带皮红标纯黑底 |
| `references/daodao-reptheory-prompt-pack.md` | 角色设定、选题公式、脚本节拍、视觉/配音 |
| `references/topic-pool-30ep.md` | 30 期选题权威表（**勿把整表贴进本 SKILL**） |
| `references/ep01-delivery-notes.md` / `ep02-v2-delivery-notes.md` | 已跑通交付要点 |
| `references/remotion-layers-notes.md` | MuscleTag / GuideArrow / TeachCallout 等叠层约定 |
| `examples/ep01-script-outline.md` / `ep02-script-outline.md` | 口播结构样例 |

## 3. 产线 Pipeline（硬顺序）

1. **选题**：优先池内 **#1→#5**；其余待命。改题/换序须改 `topic-pool-30ep.md`。
2. **口播**：按刀刀节拍写**口语人话**（少书面腔、少术语堆）；机制用大白话比喻。
3. **侃华过眼口播** → 未过眼禁止配音/开渲。
4. **配音** → Remotion/代码成片（动作 follow-clean）。
5. **侃华过眼成片** → 未过眼禁止发帖。
6. **未令勿发帖**；勿擅自推 GitHub / 联系用户。

## 4. 脚本节拍（目标 60–90s；Ep.02 约 123s 节奏稳亦可）

1. **黄金 Hook**（约 0–8s）：反常识痛点 → 直接给答案 → 承诺本期在家怎么练
2. **机制比喻**（约 8–28s）：一句科学机制 + 生动比喻（引擎/传动绳、帐篷底座/帆布…）
3. **在家动作**（主体）：零门槛；每步**组数/秒数 + 避坑**；竖版 2–4 个动作，不硬凑
4. **做错细节**（一条说透）：真正白练的那一个代偿点
5. **CTA 打卡**：评论区两字/短词打卡

写作人格：运动科学 + 解剖背景的爆款编剧；开篇 5 秒钩子；办公室/床上/椅边可做。

## 5. 视觉锁死

- 定妆 **v3**：东亚脸、带皮、红橙肌群标、纯黑底、戏剧侧光、工作族精瘦（非壮汉夸张）。参考三图：`v3-model-7view-sheet.jpg` / `v3-sample-wall-pushup.jpg` / `v3-sample-chair-squat.jpg`。
- **禁全程无皮** medical 标本感；机制处允许**局部**红橙透视。
- **禁胶囊人体**作主画面交付。
- **禁外部视频生成 API**（token01、云端 MiniMax-H3、fal 等）。主路径：Remotion / 代码 / 静图 2.5D。
- 动作段必须 **follow-clean**（跟做级流畅）。本机 H3 R2V 可作**已审定妆**对口/动作；**禁止**糊弄微动冒充全程。
- 角标用系列名「工作族有好身材 · Ep.N」；禁旧主号品牌字上屏。

## 6. 直观硬规则（侃华 2026-10-31 Ep.02 过眼通过 · 成片必验）

1. **动作流畅** + **关键姿势特别讲解**（尤其**髋/骨盆**）：叠字级 `TeachCallout` / `PelvisBrace`，与画面对齐。
2. **旁标注具体肌肉群与髋位置**：`MuscleTag`（锚点红环 + 折线引线 + 旁侧字牌）；禁糊一团红光。
3. **做动作时动画旁加引导线**：`GuideArrow` / `TrajectoryArc` 标手脚/肋骨/夹臀走向。

细节见 `references/remotion-layers-notes.md`。

## 7. 音频与规格

- **不露脸旁白**；Ep 线默认 **刘飞**（`zh_male_liufei_uranus_bigtts`）可用；深沉偏慢、人感停顿。
- **禁诊疗话术**、保证疗效、排毒/燃脂神技口吻。
- 响度约 **−16 LUFS**；竖版 **1080×1920** · 30fps · H.264 + AAC。
- BGM 轻氛围（参考 `bgmVol≈0.07` + 淡入淡出）；勿盖过人声。

## 8. 交付物

每集至少：

- `out/epNN-….mp4`（loudnorm 后终稿）
- Gofile **主链 + 备链**
- 关键抽帧（Hook / 科学 / 各动作 / 做错 / CTA）
- `DELIVERY.md`（时长、响度、定妆、follow-clean 来源、禁项自检）

**过眼前禁发帖。** 旧 Gofile / 旧成片路径写明作废，勿再交。

## 9. 样例指针

- Ep.01（选题 #1 · 瘦却没劲 · follow-clean）：`examples/ep01-script-outline.md` + `references/ep01-delivery-notes.md`
- Ep.02 v2（选题 #2 · 小腹前拱 · 三点必改通过）：`examples/ep02-script-outline.md` + `references/ep02-v2-delivery-notes.md`

下一集：打开 `topic-pool-30ep.md` 取下一优先号 → 按本节拍写口语 → 侃华过眼口播 → 配音成片 → 侃华过眼成片。
