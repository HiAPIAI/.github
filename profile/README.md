# HiAPI

**One API, all AI models.**

HiAPI is an AI API platform built for developers. Images, video, music, and text, all with one key.

[Website](https://www.hiapi.ai) · [Get API Key](https://www.hiapi.ai/en/register) · [Pricing](https://www.hiapi.ai/en/pricing) · [Docs](https://docs.hiapi.ai)

---

## Start Here

| What you need | Repository / Link | Use it for |
| --- | --- | --- |
| GPT Image 2 in AI Agents | [hiapi-gpt-image-2-skill](https://github.com/HiAPIAI/hiapi-gpt-image-2-skill) | Generate images from Codex, Claude Code, OpenCode, OpenClaw, and similar agents |
| Seedance 2.0 in AI Agents | [hiapi-seedance-2-0-video-skill](https://github.com/HiAPIAI/hiapi-seedance-2-0-video-skill) | Generate videos from text or animate images from Codex, Claude Code, OpenCode, OpenClaw, and similar agents |
| HappyHorse 1.0 in AI Agents | [hiapi-happyhorse-1-0-video-skill](https://github.com/HiAPIAI/hiapi-happyhorse-1-0-video-skill) | Generate text-to-video clips from Codex, Claude Code, OpenCode, OpenClaw, and similar agents |
| Remote MCP server | `https://mcp.hiapi.ai/mcp` | Let MCP-compatible clients call HiAPI tools directly |
| API documentation | [docs.hiapi.ai](https://docs.hiapi.ai) | Model endpoints, request parameters, and integration guides |
| API key | [HiAPI API Key](https://www.hiapi.ai/en/register) | Create the key used by SDKs, agents, and MCP clients |

---

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

HiAPI 是为开发者打造的 AI API 平台。图像、视频、音乐和文本，一个密钥全搞定。

[官网](https://www.hiapi.ai/zh) · [免费获取 API Key](https://www.hiapi.ai/zh/register) · [查看价格](https://www.hiapi.ai/zh/pricing) · [文档](https://docs.hiapi.ai)

### 从这里开始

| 你需要什么 | 仓库 / 链接 | 用途 |
| --- | --- | --- |
| 在 AI Agent 中使用 GPT Image 2 | [hiapi-gpt-image-2-skill](https://github.com/HiAPIAI/hiapi-gpt-image-2-skill) | 在 Codex、Claude Code、OpenCode、OpenClaw 等 Agent 中生成图片 |
| 在 AI Agent 中使用 Seedance 2.0 | [hiapi-seedance-2-0-video-skill](https://github.com/HiAPIAI/hiapi-seedance-2-0-video-skill) | 在 Codex、Claude Code、OpenCode、OpenClaw 等 Agent 中生成视频，或让图片动起来 |
| 在 AI Agent 中使用 HappyHorse 1.0 | [hiapi-happyhorse-1-0-video-skill](https://github.com/HiAPIAI/hiapi-happyhorse-1-0-video-skill) | 在 Codex、Claude Code、OpenCode、OpenClaw 等 Agent 中生成文生视频 |
| 远程 MCP 服务 | `https://mcp.hiapi.ai/mcp` | 让支持 MCP 的客户端直接调用 HiAPI 工具 |
| API 文档 | [docs.hiapi.ai](https://docs.hiapi.ai) | 查看模型接口、请求参数和接入指南 |
| API Key | [HiAPI API Key](https://www.hiapi.ai/zh/register) | 创建 SDK、Agent、MCP 调用所需的 Key |

### AI Agent 接入

- **Skill：** 如果只需要 GPT Image 2 图像生成，安装 [hiapi-gpt-image-2-skill](https://github.com/HiAPIAI/hiapi-gpt-image-2-skill)。
- **Skill：** 如果只需要 Seedance 2.0 文生视频或图生视频，安装 [hiapi-seedance-2-0-video-skill](https://github.com/HiAPIAI/hiapi-seedance-2-0-video-skill)。
- **Skill：** 如果只需要 HappyHorse 1.0 文生视频，安装 [hiapi-happyhorse-1-0-video-skill](https://github.com/HiAPIAI/hiapi-happyhorse-1-0-video-skill)。
- **远程 MCP：** 如果你的客户端支持远程 MCP URL 和自定义请求头，可以连接 `https://mcp.hiapi.ai/mcp`。

---

## Public Repositories

| Repository | Status |
| --- | --- |
| [hiapi-gpt-image-2-skill](https://github.com/HiAPIAI/hiapi-gpt-image-2-skill) | GPT Image 2 image generation skill |
| [hiapi-seedance-2-0-video-skill](https://github.com/HiAPIAI/hiapi-seedance-2-0-video-skill) | Seedance 2.0 video generation skill |
| [hiapi-happyhorse-1-0-video-skill](https://github.com/HiAPIAI/hiapi-happyhorse-1-0-video-skill) | HappyHorse 1.0 text-to-video skill |

Only public, ready-to-use repositories are listed here.
