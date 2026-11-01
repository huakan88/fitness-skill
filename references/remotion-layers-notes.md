# Remotion 叠层约定（浓缩自 Ep.02 `MotionLayers.tsx`）

**勿整树拷贝 remotion/**。新集按需实现同名组件即可；坐标按 1080×1920。

## 组件一览

| 组件 | 用途 | 关键 props |
|------|------|------------|
| `MuscleTag` | 肌群/关节旁标：锚点红环 + 折线引线 + 旁侧字牌 | `ax,ay` 锚点；`lx,ly` 字牌；`text` / `sub`；`color` 默认 `#FF4A30` |
| `GuideArrow` | 跟做方向箭头（手脚/肋骨/夹臀） | `x1,y1→x2,y2`；`progress` 箭头行进；可 `dashed` / `label` |
| `TrajectoryArc` | 伸腿/伸臂弧形轨迹（strokeDash 画出） | SVG `d` path；`progress` 0..1 |
| `PelvisBrace` | 骨盆「别晃」水平稳定线 + 括号 + 短字 | `cx,cy`；`text` 默认「骨盆稳住」 |
| `TeachCallout` | 关键姿势讲解叠字（短旁白级，不改口播轨） | `lines: string[]`；标题区固定「关键姿势 · 髋」感 |
| `RedGlow` | 局部红标发光 blob | 位置尺寸 + opacity；`mix-blend-mode: screen` |
| `RopePath` | 引擎→传动绳发力路径（可 fail 分叉） | `progress` / `slip` / `fail` |
| `HipIris` | 髋区径向聚焦 | `progress` |
| `SwitchBadge` | 「开关 · 开/关」机制徽标 | `on` boolean |
| `Chip` / `CompareLabel` | 短标签 / 分屏对错标 | 红框黑底白字 |

## 使用硬规则（对齐侃华三点）

1. 动作段跟做时：**至少**一对 `MuscleTag`（含髋或主发力肌）+ 一条 `GuideArrow`/`TrajectoryArc`。
2. 髋/骨盆关键帧：叠加 `TeachCallout`（1–2 句人话）和/或 `PelvisBrace`。
3. 禁只丢一团 `RedGlow` 而不写肌肉名。
4. zIndex 参考：轨迹/箭头 ~30–31，MuscleTag ~32，TeachCallout ~40。
5. 分屏做错：`CompareLabel` 灰警告 vs 红标正确半边。

## 跟做 clip 合成提示（Ep.01/02）

- 动作用 `OffthreadVideo` / FollowClip；可略 cover 放大（Ep.02：~108%）并偏锚中心，减轻边缘漂移。
- Hook/科学/CTA 用定妆静图 + 上述机制层，与 follow-clean 黑底红标统一。
