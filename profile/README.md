# HiAPI

**One API, all AI models.**

HiAPI is an AI API platform for developers and AI Agents. Use one key to call image, video, music, and text models, or start from tested creative recipes that already include prompts, output examples, and runnable API request shapes.

[Website](https://www.hiapi.ai) · [Get API Key](https://www.hiapi.ai/en/register) · [Pricing](https://www.hiapi.ai/en/pricing) · [Docs](https://docs.hiapi.ai) · [Remote MCP](https://docs.hiapi.ai/for-ai/)

> **HiAPI Matrix:** 🎨 [Image Prompts](https://github.com/HiAPIAI/awesome-gpt-image-2-prompts) · 🎬 [Video Prompts](https://github.com/HiAPIAI/awesome-seedance-2-0-prompts) · 🛠️ [Agent Skills](https://github.com/HiAPIAI/hiapi-skills) · 🤖 [Remote MCP](https://docs.hiapi.ai/for-ai/) · 📖 [API Docs](https://docs.hiapi.ai)

**Latest:** 🎬 [awesome-seedance-2-0-prompts](https://github.com/HiAPIAI/awesome-seedance-2-0-prompts) — 160+ Seedance 2.0 video recipes · 🎨 [awesome-gpt-image-2-prompts](https://github.com/HiAPIAI/awesome-gpt-image-2-prompts) — 100+ GPT Image 2 cases · 🤖 [Remote MCP](https://docs.hiapi.ai/for-ai/) at `mcp.hiapi.ai`.

---

## Start Here

| What you need | Repository / Link | Use it for |
| --- | --- | --- |
| GPT Image 2 Prompts | [awesome-gpt-image-2-prompts](https://github.com/HiAPIAI/awesome-gpt-image-2-prompts) | Study output-backed GPT Image 2 recipes, open them in HiAPI Draw, and adapt prompts for your own assets |
| Seedance 2.0 Prompts | [awesome-seedance-2-0-prompts](https://github.com/HiAPIAI/awesome-seedance-2-0-prompts) | Browse 160+ Seedance 2.0 video recipes across product, social, cinematic, and image-to-video categories |
| Agent Skills | [hiapi-skills](https://github.com/HiAPIAI/hiapi-skills) | Choose the right HiAPI skill for focused image or video generation inside AI Agents |
| Remote MCP | `https://mcp.hiapi.ai/mcp` | Let MCP-compatible clients discover and call HiAPI image/video tools directly |
| API Cookbook | [docs.hiapi.ai](https://docs.hiapi.ai) | Copy model endpoints, request parameters, and integration guides |
| GPT Image 2 in AI Agents | [hiapi-gpt-image-2-skill](https://github.com/HiAPIAI/hiapi-gpt-image-2-skill) | Generate images from Codex, Claude Code, OpenCode, OpenClaw, and similar agents |
| Seedance 2.0 in AI Agents | [hiapi-seedance-2-0-video-skill](https://github.com/HiAPIAI/hiapi-seedance-2-0-video-skill) | Generate videos from text or animate images from Codex, Claude Code, OpenCode, OpenClaw, and similar agents |
| HappyHorse 1.0 in AI Agents | [hiapi-happyhorse-1-0-video-skill](https://github.com/HiAPIAI/hiapi-happyhorse-1-0-video-skill) | Generate text-to-video clips from Codex, Claude Code, OpenCode, OpenClaw, and similar agents |
| API key | [HiAPI API Key](https://www.hiapi.ai/en/register) | Create the key used by SDKs, agents, and MCP clients |

---

## Public Matrix

HiAPI's public repositories are organized around four jobs:

- **Prompt Galleries:** output-backed recipes for creators and developers who want a working starting point before calling an API.
- **Agent Skills:** installable single-model workflows for agents that need a stable model-specific tool.
- **Remote MCP:** a hosted MCP endpoint for clients that can pass a HiAPI API key in request headers.
- **API Cookbook:** docs and examples for direct OpenAI-compatible API integration.

This keeps the public surface API-first: every prompt or skill should lead to a usable HiAPI request, not just a static inspiration list.

## OpenAI-Compatible API

Use the same OpenAI-style request shape with the HiAPI base URL:

```bash
curl https://api.hiapi.ai/v1/chat/completions \
  -H "Authorization: Bearer $HIAPI_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "gpt-image-2",
    "stream": false,
    "messages": [
      {
        "role": "user",
        "content": "Create a cinematic product image for an AI API platform"
      }
    ],
    "extra_body": {
      "google": {
        "image_config": {
          "aspect_ratio": "16:9"
        }
      }
    }
  }'
```

---

## AI Agent Integration

HiAPI can be used directly from AI Agent tools:

- **Image prompt gallery:** use [awesome-gpt-image-2-prompts](https://github.com/HiAPIAI/awesome-gpt-image-2-prompts) when you want a tested visual recipe before generating.
- **Video prompt gallery:** use [awesome-seedance-2-0-prompts](https://github.com/HiAPIAI/awesome-seedance-2-0-prompts) when you want a tested video recipe (text-to-video or image-to-video) before generating.
- **Skills directory:** start with [hiapi-skills](https://github.com/HiAPIAI/hiapi-skills) when you want to choose from all public HiAPI skills.
- **Skill:** install [hiapi-gpt-image-2-skill](https://github.com/HiAPIAI/hiapi-gpt-image-2-skill) when you specifically want GPT Image 2 image generation.
- **Skill:** install [hiapi-seedance-2-0-video-skill](https://github.com/HiAPIAI/hiapi-seedance-2-0-video-skill) when you specifically want Seedance 2.0 text-to-video or image-to-video generation.
- **Skill:** install [hiapi-happyhorse-1-0-video-skill](https://github.com/HiAPIAI/hiapi-happyhorse-1-0-video-skill) when you specifically want HappyHorse 1.0 text-to-video generation.
- **Remote MCP:** connect to `https://mcp.hiapi.ai/mcp` when your client supports remote MCP URLs and custom request headers.

Remote MCP configuration shape:

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

---

## 中文

**一个 API，所有 AI 模型。**

HiAPI 是面向开发者和 AI Agent 的 AI API 平台。图像、视频、音乐和文本，一个密钥全搞定；也可以从已经验证过的创意配方开始，直接拿到提示词、效果图和可运行的 API 请求形态。

[官网](https://www.hiapi.ai/zh) · [免费获取 API Key](https://www.hiapi.ai/zh/register) · [查看价格](https://www.hiapi.ai/zh/pricing) · [文档](https://docs.hiapi.ai) · [Remote MCP](https://docs.hiapi.ai/zh/for-ai/)

**最新动态：** 🎬 [awesome-seedance-2-0-prompts](https://github.com/HiAPIAI/awesome-seedance-2-0-prompts) — 160+ Seedance 2.0 视频配方 · 🎨 [awesome-gpt-image-2-prompts](https://github.com/HiAPIAI/awesome-gpt-image-2-prompts) — 100+ GPT Image 2 案例 · 🤖 [Remote MCP](https://docs.hiapi.ai/zh/for-ai/) 已上线 `mcp.hiapi.ai`。

### 从这里开始

| 你需要什么 | 仓库 / 链接 | 用途 |
| --- | --- | --- |
| GPT Image 2 提示词集 | [awesome-gpt-image-2-prompts](https://github.com/HiAPIAI/awesome-gpt-image-2-prompts) | 查看带真实效果图的 GPT Image 2 创意配方，在 HiAPI Draw 打开并改写 |
| Seedance 2.0 提示词集 | [awesome-seedance-2-0-prompts](https://github.com/HiAPIAI/awesome-seedance-2-0-prompts) | 浏览 160+ Seedance 2.0 视频配方，涵盖产品、社媒、电影感、图生视频等类目 |
| Agent Skills | [hiapi-skills](https://github.com/HiAPIAI/hiapi-skills) | 为 AI Agent 选择稳定的单模型图像或视频生成 skill |
| Remote MCP | `https://mcp.hiapi.ai/mcp` | 让支持 MCP 的客户端直接发现并调用 HiAPI 图像/视频工具 |
| API Cookbook | [docs.hiapi.ai](https://docs.hiapi.ai) | 复制模型接口、请求参数和接入指南 |
| 在 AI Agent 中使用 GPT Image 2 | [hiapi-gpt-image-2-skill](https://github.com/HiAPIAI/hiapi-gpt-image-2-skill) | 在 Codex、Claude Code、OpenCode、OpenClaw 等 Agent 中生成图片 |
| 在 AI Agent 中使用 Seedance 2.0 | [hiapi-seedance-2-0-video-skill](https://github.com/HiAPIAI/hiapi-seedance-2-0-video-skill) | 在 Codex、Claude Code、OpenCode、OpenClaw 等 Agent 中生成视频，或让图片动起来 |
| 在 AI Agent 中使用 HappyHorse 1.0 | [hiapi-happyhorse-1-0-video-skill](https://github.com/HiAPIAI/hiapi-happyhorse-1-0-video-skill) | 在 Codex、Claude Code、OpenCode、OpenClaw 等 Agent 中生成文生视频 |
| API Key | [HiAPI API Key](https://www.hiapi.ai/zh/register) | 创建 SDK、Agent、MCP 调用所需的 Key |

### 公开矩阵

HiAPI 的公开仓库按四类组织：

- **Prompt Galleries：** 给创作者和开发者看的真实效果案例，目标是直接导向可用的 HiAPI 请求。
- **Agent Skills：** 给 AI Agent 安装的单模型工作流，减少模型名、端点和参数猜测。
- **Remote MCP：** 给支持远程 MCP 的客户端使用，直接用用户自己的 HiAPI API Key 调用工具。
- **API Cookbook：** 给直接写代码的人用，提供端点、参数和接入示例。

### AI Agent 接入

- **图像 Prompt Gallery：** 如果想先找一个验证过的视觉配方，查看 [awesome-gpt-image-2-prompts](https://github.com/HiAPIAI/awesome-gpt-image-2-prompts)。
- **视频 Prompt Gallery：** 如果想先找一个验证过的视频配方（文生视频或图生视频），查看 [awesome-seedance-2-0-prompts](https://github.com/HiAPIAI/awesome-seedance-2-0-prompts)。
- **Skills 总目录：** 如果想先选择 HiAPI 公开 skill，查看 [hiapi-skills](https://github.com/HiAPIAI/hiapi-skills)。
- **Skill：** 如果只需要 GPT Image 2 图像生成，安装 [hiapi-gpt-image-2-skill](https://github.com/HiAPIAI/hiapi-gpt-image-2-skill)。
- **Skill：** 如果只需要 Seedance 2.0 文生视频或图生视频，安装 [hiapi-seedance-2-0-video-skill](https://github.com/HiAPIAI/hiapi-seedance-2-0-video-skill)。
- **Skill：** 如果只需要 HappyHorse 1.0 文生视频，安装 [hiapi-happyhorse-1-0-video-skill](https://github.com/HiAPIAI/hiapi-happyhorse-1-0-video-skill)。
- **远程 MCP：** 如果你的客户端支持远程 MCP URL 和自定义请求头，可以连接 `https://mcp.hiapi.ai/mcp`。

---

## Public Repositories

| Repository | Status |
| --- | --- |
| [awesome-gpt-image-2-prompts](https://github.com/HiAPIAI/awesome-gpt-image-2-prompts) | GPT Image 2 prompt gallery with real output examples |
| [awesome-seedance-2-0-prompts](https://github.com/HiAPIAI/awesome-seedance-2-0-prompts) | Seedance 2.0 video prompt gallery, 160+ cases across 8 categories |
| [hiapi-skills](https://github.com/HiAPIAI/hiapi-skills) | Official HiAPI AI Agent skills directory |
| [hiapi-gpt-image-2-skill](https://github.com/HiAPIAI/hiapi-gpt-image-2-skill) | GPT Image 2 image generation skill |
| [hiapi-seedance-2-0-video-skill](https://github.com/HiAPIAI/hiapi-seedance-2-0-video-skill) | Seedance 2.0 video generation skill |
| [hiapi-happyhorse-1-0-video-skill](https://github.com/HiAPIAI/hiapi-happyhorse-1-0-video-skill) | HappyHorse 1.0 text-to-video skill |

Only public, ready-to-use repositories are listed here.
