# 想法拆解器 / Idea Breakdown

一个 Claude Code / Codex 通用 Skill，用产品、工程、设计和商业化视角把模糊想法转换成低风险的实现决策。

## 审查模式

- **Product**：目标用户、任务、痛点、范围、替代方案和验证证据。
- **Engineering**：边界、数据流、依赖、安全、失败路径、测试和运营成本。
- **Design**：入口、用户路径、信息层级、状态、可理解性、可访问性和移动端。
- **Full**：运行三种审查，再给出纯 Skill、Skill + 后端或完整软件的结论。

未指定模式时默认使用 Full。分析不等于授权实施。

## 安装

### Codex

```bash
git clone https://github.com/fgyg007/idea-breakdown-skill.git ~/.codex/skills/idea-breakdown
```

### Claude Code

```bash
git clone https://github.com/fgyg007/idea-breakdown-skill.git ~/.claude/skills/idea-breakdown
```

安装后重启对应工具或开始新会话。

## 使用

完整拆解：

```text
使用 $idea-breakdown 完整分析这个想法，判断应该做 Skill、Skill + 后端还是完整软件。
```

单独审查产品：

```text
使用 $idea-breakdown 的 Product 模式挑战用户、痛点和 MVP 范围。
```

单独审查工程：

```text
使用 $idea-breakdown 的 Engineering 模式检查架构、安全、失败路径和最小技术证明。
```

单独审查设计：

```text
使用 $idea-breakdown 的 Design 模式拆解用户路径和所有界面状态，不要写代码。
```

## 输出

Skill 会给出：

1. 用户、价值和关键假设；
2. 选定视角的审查结论；
3. 实现路线及边界；
4. 自用工作流和与现有工具的组合；
5. 在 Full 或明确请求时的商业化分析；
6. 最低风险的下一步及扩大投入所需证据。

## License

[MIT](LICENSE)
