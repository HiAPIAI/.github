# HiAPI

**One API, all AI models.**

HiAPI is an AI API platform for developers and AI Agents. Use one key to call image, video, music, and text models, or start from tested creative recipes that already include prompts, output examples, and runnable API request shapes.

[Website](https://www.hiapi.ai) · [Get API Key](https://www.hiapi.ai/en/register) · [Pricing](https://www.hiapi.ai/en/pricing) · [Docs](https://docs.hiapi.ai) · [Remote MCP](https://docs.hiapi.ai/for-ai/)

> **HiAPI Matrix:** 🎨 [Image Prompts](https://github.com/HiAPIAI/awesome-gpt-image-2-prompts) · 🎬 [Video Prompts](https://github.com/HiAPIAI/awesome-seedance-2-0-prompts) · 🛠️ [Agent Skills](https://github.com/HiAPIAI/hiapi-skills) · 🤖 [Remote MCP](https://docs.hiapi.ai/for-ai/) · 📖 [API Docs](https://docs.hiapi.ai)

**Latest:** 🎬 [hiapi-video-prompt-generator-skill](https://github.com/HiAPIAI/hiapi-video-prompt-generator-skill) — direct briefs and sources into runnable Seedance/HappyHorse prompts · 🎬 [awesome-seedance-2-0-prompts](https://github.com/HiAPIAI/awesome-seedance-2-0-prompts) — 160+ Seedance 2.0 video recipes · 🎨 [awesome-gpt-image-2-prompts](https://github.com/HiAPIAI/awesome-gpt-image-2-prompts) — 100+ GPT Image 2 cases · 🤖 [Remote MCP](https://docs.hiapi.ai/for-ai/) at `mcp.hiapi.ai`.

---

## Quickstart

Every media model runs on one contract — the [Unified Async API](https://docs.hiapi.ai/async-api/). Create a task:

```bash
curl -X POST https://api.hiapi.ai/v1/tasks \
  -H "Authorization: Bearer $HIAPI_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "gpt-image-2",
    "input": {
      "prompt": "Create a cinematic product image for an AI API platform",
      "aspect_ratio": "16:9",
      "resolution": "1K"
    }
  }'
```

It returns `data.taskId`. Poll until the task succeeds:

```bash
curl https://api.hiapi.ai/v1/tasks/{taskId} \
  -H "Authorization: Bearer $HIAPI_API_KEY"
```

```json
{
  "data": {
    "taskId": "task_123",
    "status": "success",
    "output": [{ "type": "image", "url": "https://cdn.example.com/image.png" }]
  }
}
```

The same `POST /v1/tasks` shape works for every model — swap `model` and `input` per the [model pages](https://docs.hiapi.ai/models/). Get your key at [Dashboard → API Keys](https://www.hiapi.ai/en/register).

---

## Start Here

| What you need | Link | Use it for |
| --- | --- | --- |
| API key | [Register](https://www.hiapi.ai/en/register) | Create the key used by the API, agents, and MCP clients |
| Image prompt gallery | [awesome-gpt-image-2-prompts](https://github.com/HiAPIAI/awesome-gpt-image-2-prompts) | Output-backed GPT Image 2 recipes you can copy and adapt |
| Video prompt gallery | [awesome-seedance-2-0-prompts](https://github.com/HiAPIAI/awesome-seedance-2-0-prompts) | 160+ Seedance 2.0 recipes across product, social, cinematic, image-to-video |
| Agent Skills | [hiapi-skills](https://github.com/HiAPIAI/hiapi-skills) | Generate images/videos by just asking Claude Code, Codex, or OpenClaw |
| Remote MCP | `https://mcp.hiapi.ai/mcp` | One connection that gives MCP clients every HiAPI image/video tool |
| API docs | [docs.hiapi.ai](https://docs.hiapi.ai) | Model parameters, pricing, and integration guides |

---

## Use HiAPI from AI Agents

**Skills** — install once, then just ask your agent ("generate a poster", "make a 5-second video"):

```bash
npx -y github:HiAPIAI/hiapi-gpt-image-2-skill -y
```

All skills and install commands: [hiapi-skills](https://github.com/HiAPIAI/hiapi-skills) · [Skills guide](https://docs.hiapi.ai/skills/)

**Remote MCP** — for Claude Code, Cursor, and other MCP clients:

```json
{
  "mcpServers": {
    "hiapi": {
      "url": "https://mcp.hiapi.ai/mcp",
      "headers": {
        "Authorization": "Bearer YOUR_HIAPI_API_KEY"
      }
    }
  }
}
```

Setup guide: [Remote MCP docs](https://docs.hiapi.ai/for-ai/)

---

## 中文

**一个 API，所有 AI 模型。**

HiAPI 是面向开发者和 AI Agent 的 AI API 平台。图像、视频、音乐和文本，一个密钥全搞定；也可以从已经验证过的创意配方开始，直接拿到提示词、效果图和可运行的 API 请求形态。

[官网](https://www.hiapi.ai/zh) · [免费获取 API Key](https://www.hiapi.ai/zh/register) · [查看价格](https://www.hiapi.ai/zh/pricing) · [文档](https://docs.hiapi.ai/zh/) · [Remote MCP](https://docs.hiapi.ai/zh/for-ai/)

**最新动态：** 🎬 [hiapi-video-prompt-generator-skill](https://github.com/HiAPIAI/hiapi-video-prompt-generator-skill) — 把一句话想法变成可直接生成的视频提示词 · 🎬 [awesome-seedance-2-0-prompts](https://github.com/HiAPIAI/awesome-seedance-2-0-prompts) — 160+ Seedance 2.0 视频配方 · 🎨 [awesome-gpt-image-2-prompts](https://github.com/HiAPIAI/awesome-gpt-image-2-prompts) — 100+ GPT Image 2 案例 · 🤖 [Remote MCP](https://docs.hiapi.ai/zh/for-ai/) 已上线 `mcp.hiapi.ai`。

### 快速上手

所有媒体模型都走同一套[统一异步接口](https://docs.hiapi.ai/zh/async-api/)。创建任务：

```bash
curl -X POST https://api.hiapi.ai/v1/tasks \
  -H "Authorization: Bearer $HIAPI_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "gpt-image-2",
    "input": {
      "prompt": "为一个 AI API 平台生成一张电影感产品图",
      "aspect_ratio": "16:9",
      "resolution": "1K"
    }
  }'
```

接口返回 `data.taskId`，轮询 `GET /v1/tasks/{taskId}` 直到 `status` 为 `success`，结果在 `data.output[]`。换模型只需替换 `model` 和 `input`，参数见[模型页](https://docs.hiapi.ai/zh/models/)。

### 从这里开始

| 你需要什么 | 链接 | 用途 |
| --- | --- | --- |
| API Key | [注册获取](https://www.hiapi.ai/zh/register) | 创建 API、Agent、MCP 调用所需的 Key |
| 图片提示词库 | [awesome-gpt-image-2-prompts](https://github.com/HiAPIAI/awesome-gpt-image-2-prompts) | 带真实效果图的 GPT Image 2 配方，可直接复制改写 |
| 视频提示词库 | [awesome-seedance-2-0-prompts](https://github.com/HiAPIAI/awesome-seedance-2-0-prompts) | 160+ Seedance 2.0 配方，涵盖产品、社媒、电影感、图生视频 |
| Agent Skills | [hiapi-skills](https://github.com/HiAPIAI/hiapi-skills) | 在 Claude Code、Codex、OpenClaw 里对话即可生成图片视频 |
| Remote MCP | `https://mcp.hiapi.ai/mcp` | MCP 客户端连接一次即获得全部 HiAPI 图像/视频工具 |
| API 文档 | [docs.hiapi.ai](https://docs.hiapi.ai/zh/) | 模型参数、价格和接入指南 |

### 在 AI Agent 中使用

**Skills** — 安装一次，之后直接对 Agent 说「生成一张海报」「做一条 5 秒视频」：

```bash
npx -y github:HiAPIAI/hiapi-gpt-image-2-skill -y
```

全部技能与安装命令：[hiapi-skills](https://github.com/HiAPIAI/hiapi-skills) · [技能指南](https://docs.hiapi.ai/zh/skills/)

**Remote MCP** — 适用于 Claude Code、Cursor 等 MCP 客户端，配置见上方英文区或[接入文档](https://docs.hiapi.ai/zh/for-ai/)。
