# 想法拆解器 / Idea Breakdown

一个 [Claude Code](https://claude.com/claude-code) **Skill**：给它一个想法，它从四个维度帮你深度拆解——

- 🧩 **Skill 可行性** — 这个想法能不能用 Claude Code Skill 实现？边界在哪？
- 🛠️ **实现路径** — 纯 Skill / Skill + 后端 / 必须做软件，给出具体方案
- 🙋 **自用优化** — 怎么用最顺手，workflow 怎么设计，能省掉哪些重复劳动
- 💰 **商业化策略** — 护城河在哪，定价模式，防复制方案，目标用户画像

> 适合 AI 工具开发者、独立开发者，在"要不要做这个"和"怎么做"之间快速找到答案。

---

## 一、安装

> 前提：你已经装好 [Claude Code](https://claude.com/claude-code)。

把仓库克隆到 Claude Code 的用户级 skills 目录：

```bash
git clone https://github.com/fgyg007/idea-breakdown-skill.git ~/.claude/skills/idea-breakdown
```

> 注意：克隆目标目录必须叫 `idea-breakdown`（要和 skill 名一致）。

然后**重启 Claude Code（或开个新会话）**，让它加载这个新 skill。

---

## 二、怎么用

装好后，直接调用：

```
/idea-breakdown 我想做一个帮用户管理待办事项的 Telegram Bot
```

```
/idea-breakdown 音视频脚本辅助工具，帮创作者规划拍摄内容
```

```
/idea-breakdown 拼豆图纸生成器，把图片转成像素拼豆图案
```

Claude 会输出一份**结构化分析报告**，四个维度逐一拆解，最后附总结建议和下一步行动。

---

## 三、输出示例结构

```
## 一、Skill 可行性评估
结论：✅ 纯 Skill 就够 / 🔀 Skill + 后端 / 🏗️ 必须做软件

## 二、实现路径设计
输入参数 / 输出格式 / 内部流程 / 需要哪些工具

## 三、自用优化设计
调用方式 / workflow 位置 / 和其他工具的组合 / 可自动化的部分

## 四、商业化路径分析
护城河 / 防复制方案 / 定价模式 / 目标用户 / 第一步从哪里开始

## 总结建议
一段话：怎么做 + 优先级 + 最快跑通的路径
```

---

## 四、适合什么场景

- 有一个新想法，不知道「做 Skill 还是做软件」
- 想清楚一个 Skill 的商业化路径再动手
- 快速评估一个想法的可行性，不想花太多时间分析

---

## License

[MIT](LICENSE) — 随便用、随便改、随便分发。
