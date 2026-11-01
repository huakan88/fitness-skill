# fitness-skill · 健身

二号抖音「**工作族有好身材**」竖版产线 skill（Cursor / Grok Bot 可复用）。

## 给其他 Agent 怎么装

1. 克隆或拷贝本目录到对方 bot 的 skills 路径，例如：
   - `…/skills/fitness-skill/`
   - 或解压 `fitness-skill.zip`
2. 确认入口文件为 `SKILL.md`（frontmatter `name: 健身`）。
3. 在对方环境用 skill 加载器按名 **`健身`** / `fitness-skill` 调用；开工前读 `SKILL.md` 全文，再打开 `references/`。
4. **不要**只抄 SKILL 正文就开渲——定妆图、选题池、刀刀 pack、Ep 交付笔记都在 `references/`。

## 目录

```
fitness-skill/
  README.md
  SKILL.md
  references/          # 定妆、选题、刀刀方法、Ep 交付浓缩、Remotion 叠层约定
  examples/            # Ep.01 / Ep.02 口播结构大纲
```

## 硬边界（摘要）

- 仅二号抖音；总主题「工作族有好身材」≠ 单集名
- 定妆 v3 带皮红标；禁全程无皮、胶囊主画面、外部视频生成 API
- 口播与成片均须侃华过眼；未令勿发帖
- 直观三件套：髋关键讲解 + 肌群旁标 + 动作引导线（Ep.02 过眼通过）

完整步骤见 `SKILL.md`。
