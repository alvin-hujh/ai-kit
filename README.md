# ai-kit

个人 AI 工具集，包含 Claude Code 技能、MCP 服务器、插件和 Agent。

## 目录结构

```
ai-kit/
├── skills/             # Claude Code 技能 (Skill)
│   └── one-on-one-tutor/   # 一对一学习辅导
├── mcp-servers/        # MCP 服务器 (Model Context Protocol)
├── plugins/            # Claude Code 插件
├── agents/             # Agent 定义
└── scripts/            # 辅助脚本
```

## 使用方式

技能通过软链接注册到 `~/.claude/plugins/cache/custom-skills/` 下，
编辑本仓库中的文件即生效，无需重复同步。

## 依赖

### markitdown（文档格式转换）

`one-on-one-tutor` 技能使用 markitdown 将 PDF、Word、PPT、Excel 等格式转换为 markdown。

安装：
```bash
pip install markitdown
# 或
uv tool install markitdown
```

项目已内置 `.claude/settings.json` 配置了 markitdown MCP 服务器，安装后重启 Claude Code 即可使用。
