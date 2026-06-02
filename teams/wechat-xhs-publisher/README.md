# 微信小红书发布助手

一键发布内容到微信公众号和小红书双平台——从选题策划、文案撰写、封面设计到发布，一站式内容运营。支持从 GitHub 项目、YouTube/B站视频、网页文章、PDF文档、个人经验等多种素材来源驱动写作。

## 类型

Team 型（多角色协作团队）

## 团队成员

| 角色 | 花名 | 职责 |
|------|------|------|
| 主理人 | 主编 | 选题策划、审核、调度、MCP 故障处理 |
| 文案 | 撰稿师 | 微信公众号文章 + 小红书笔记撰写 |
| 视觉设计 | 视觉师 | AI 封面图生成 + 素材搜索 + 视频截帧 |
| 微信发布 | 微运营 | 微信公众号草稿创建、预览、群发 |
| 小红书发布 | 红运营 | 小红书笔记发布、标签优化 |

## 功能

- **双平台发布**：一键写文章并发布到微信公众号 + 小红书
- **单平台发布**：只发微信公众号 或 只发小红书
- **内容改写**：将已有内容改写为适配微信/小红书的版本
- **素材驱动写作**：从 GitHub 项目、YouTube/B站视频、网页链接、PDF文档、个人经验等各类素材中提取内容，生成文章并发布

## 使用示例

- "帮我写一篇关于 AI 编程的文章，发微信公众号和小红书"
- "帮我写一篇 XX 主题的文章，只发小红书"
- "帮我读一下这个 GitHub 项目，写篇文章发出去"
- "帮我把这个 YouTube 视频内容总结成文章发出去"
- "帮我根据这个链接写篇文章"
- "帮我把我的经验总结成文章发出去"
- "把这段内容改写成小红书风格"

## 依赖的 MCP

| MCP | 必需 | 用途 |
|-----|------|------|
| wechat-official-account | 是 | 微信公众号草稿和群发 |
| xiaohongshu-mcp | 是 | 小红书笔记发布 |
| github | 否 | GitHub 项目研读（Workflow 4） |
| youtube | 否 | YouTube 视频解析（Workflow 4 素材驱动） |
| video-context-mcp | 否 | 视频画面分析（Workflow 4 素材驱动可选） |

## 头像

头像已自动生成在 `avatars/` 目录下。如需替换为自定义头像，要求：
- 格式：PNG（推荐）或 JPG
- 尺寸：512×512 px
- 大小：单张不超过 500KB

## 安装

将专家包目录放到以下路径：

```
~/.workbuddy/plugins/marketplaces/my-experts/plugins/wechat-xhs-publisher/
```

然后运行注册命令使其在 WorkBuddy 中可见：

```bash
python3 scripts/register_expert.py ~/.workbuddy/plugins/marketplaces/my-experts/plugins/wechat-xhs-publisher/
```

## 打包分享

```bash
zip -r wechat-xhs-publisher.zip wechat-xhs-publisher/
```
