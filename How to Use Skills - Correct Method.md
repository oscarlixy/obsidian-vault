# ⚠️ 重要：技能使用的正确方法

## ❌ 错误的命令
```bash
/Skill doc-coauthoring  # ❌ 这不是正确的命令
```

## ✅ 正确的使用方法

### 方法 1：直接描述需求（推荐！）

在 Claude Code 中，**直接用自然语言描述你想要什么**，Claude 会自动选择合适的技能：

```bash
cd /Users/oscar/CSlearning/obsidian
claude
```

然后直接对话：

| 你想做什么 | 直接说 |
|------------|--------|
| 头脑风暴 | "帮我头脑风暴一些博客选题" |
| 写文档 | "帮我写这个功能的文档" |
| 处理 PDF | "从这个 PDF 中提取内容" |
| 整理文件 | "帮我整理 notes 文件夹" |
| 代码审查 | "审查这段代码" |

---

### 方法 2：使用 Skill 工具（如果可用）

某些技能可以作为工具调用：

```bash
claude
```

然后：
```
你: 使用 brainstorming 技能来帮我生成文章选题
你: 使用 debugging 技能来排查这个问题
```

---

### 方法 3：安装技能到本地目录

```bash
# 创建技能目录
mkdir -p ~/.claude/skills

# 复制你想要的技能
cp -r /Users/oscar/CSlearning/obsidian/notes/claude-skills/skills/brainstorming ~/.claude/skills/

# 技能现在自动可用！
```

---

## 🎯 实际示例

### 示例 1：头脑风暴
```bash
cd /Users/oscar/CSlearning/obsidian
claude
```
```
你: 我要写一篇关于 AI 工具的文章，帮我头脑风暴几个角度

Claude: 当然！以下是一些可以探讨的角度：
1. 工具对比评测
2. 实际应用案例
3. 技术深度解析
4. ROI 分析

你对哪个方向最感兴趣？
```

### 示例 2：文档协作
```bash
cd /Users/oscar/CSlearning/obsidian
claude
```
```
你: 帮我改进这段文档的写作

Claude: [阅读你的内容后提供建议]

我建议以下几点改进：
1. 添加一个引言段落
2. 使用更清晰的标题结构
3. 补充一些例子

要我帮你重写吗？
```

### 示例 3：文件整理
```bash
cd /Users/oscar/CSlearning/obsidian
claude
```
```
你: 我的 notes 文件夹很乱，帮我整理一下

Claude: [分析文件夹结构]

我看到可以按主题分类：
- AI 相关
- 开发相关
- 个人笔记

需要我帮你重新组织吗？
```

---

## 📋 可用的内置技能

这些技能是**内置的**，直接用自然语言调用即可：

| 技能 | 触发方式 |
|------|----------|
| **brainstorming** | 说 "帮我头脑风暴..." |
| **debugging** | 说 "帮我调试..." 或 "排查这个问题" |
| **test-driven-development** | 说 "用 TDD 方法..." |
| **code-reviewer** | 说 "审查这段代码" |
| **systematic-debugging** | 说 "系统地调试..." |

---

## 🔧 如果某个技能不可用

如果某个特定技能（如 `doc-coauthoring`）不可用，你可以：

1. **用自然语言描述相同需求**
   ```
   不要说: /Skill doc-coauthoring
   应该说: 帮我编辑和改进这个文档
   ```

2. **复制技能到本地**
   ```bash
   mkdir -p ~/.claude/skills
   cp -r notes/claude-skills/skills/doc-coauthoring ~/.claude/skills/
   ```

3. **检查技能是否已安装**
   ```bash
   ls ~/.claude/skills/
   ```

---

## 💡 关键提示

| ❌ 不要 | ✅ 应该 |
|---------|---------|
| `/Skill brainstorming` | "帮我头脑风暴..." |
| `/Skill debugging` | "帮我调试这个..." |
| `/Skill pdf` | "处理这个 PDF 文件" |
| 使用特殊命令 | 用自然语言描述需求 |

---

## 🆘 如果遇到问题

**问题：** Claude 没有使用我想要的技能
```
解决：更具体地说明
你: "用系统化的调试方法来排查这个错误"
```

**问题：** 技能不存在
```
解决：描述你想要的结果
你: "帮我整理文件" 而不是 "/Skill file-organizer"
```

**问题：** 不知道说什么
```
解决：直接说你的需求
你: "我想写一篇文章，给我一些选题建议"
```

---

## 📚 更新你的笔记

请用这个新笔记更新你的理解：
- [[Quick Start - Using Skills]] - 需要更新 ⚠️
- [[Skills Quick Reference]] - 需要更新 ⚠️

---

*最后更新：2026-01-21 - 修正了技能调用方法*
