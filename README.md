# AI Workbench

个人 AI 工具集：多 Agent 流水线团队、独立角色、可复用技能、通用规则、工具配置。

## 仓库结构

```
ai-workbench/
├── teams/                        # 🔥 多Agent流水线团队
│   └── wechat-xhs-publisher/     #   微信小红书发布助手
│       ├── team.md               #     主编调度逻辑 + SOP
│       ├── agents/               #     团队角色（4个MD）
│       ├── rules/                #     团队规则（3个MD）
│       └── settings.json         #     MCP 声明
│
├── agents/                       # 🤖 独立单角色（不属于任何团队）
│
├── skills/                       # ⚡ 可复用技能
│
├── rules/                        # 📏 通用规则（跨团队复用）
│
├── tools/                        # 🔧 工具配置和脚本
│   ├── mcp-configs/              #   MCP 配置模板
│   │   ├── claude-code-mcp.json  #     Claude Code 用
│   │   └── copilot-mcp.json      #     Copilot CLI 用
│   └── scripts/                  #   辅助脚本
│
├── CLAUDE.md                     # Claude Code 自动加载
├── .github/
│   └── copilot-instructions.md   # Copilot CLI 自动加载
└── README.md                     # 本文件
```

## 快速开始

### WorkBuddy 用户

将 `teams/` 下的团队目录复制到 WorkBuddy 插件目录即可使用完整多 Agent 并行协作。

### Claude Code 用户

1. 在你的内容项目根目录克隆本仓库：
   ```bash
   git clone https://github.com/jinhui2484/ai-workbench.git
   ```
2. Claude Code 会自动加载 `CLAUDE.md`
3. 配置 MCP：将 `tools/mcp-configs/claude-code-mcp.json` 的内容复制到 `~/.claude/settings.json` 的 `mcpServers` 字段，填入你的 API Key

### Copilot CLI 用户

1. 克隆本仓库到你的项目
2. Copilot CLI 会自动加载 `.github/copilot-instructions.md`
3. 配置 MCP：参考 `tools/mcp-configs/copilot-mcp.json`

## 可用团队

### wechat-xhs-publisher — 微信小红书发布助手

5 人流水线团队，覆盖从选题到发布的全流程：

| 角色 | 职责 |
|------|------|
| 主编 | 选题策划、审核、调度、质检 |
| 撰稿师 | 微信 HTML 文章 + 小红书文案 |
| 视觉师 | 智能配图分析 + AI 封面/配图生成 |
| 微运营 | 微信公众号草稿 + 群发 |
| 红运营 | 小红书笔记发布（多图 3-9 张） |

**SOP 流程**：
- **W1** 双平台完整流程（选题→文案→配图→草稿→确认→发布）
- **W1.5** 单平台流程
- **W2** 内容改写（可衔接到发布）
- **W3** 已有文案直接发布
- **W4** 素材驱动（GitHub/YouTube/视频/网页/PDF/经验/社交媒体）

**依赖 MCP**：wechat-official-account、xiaohongshu-mcp

## 添加新内容

| 类型 | 目录 | 格式 |
|------|------|------|
| 新团队 | `teams/your-team/` | `team.md` + `agents/` + `rules/` |
| 新角色 | `agents/role-name.md` | Markdown 提示词 |
| 新技能 | `skills/skill-name/SKILL.md` | SKILL.md |
| 新规则 | `rules/rule-name.md` | Markdown 规则文档 |
| 工具配置 | `tools/mcp-configs/` | JSON 配置模板 |

## License

MIT
