<div align="center">

<img src="https://avatars.githubusercontent.com/u/338186716?s=200&v=4" alt="SpicyAPI" width="88" height="88">

# SpicyAPI

### One API for image, video, audio and text models — including the uncensored ones

**140+ model families · 210+ endpoints · priced in dollars, not credits**

[**Get an API key**](https://spicyapi.ai) &nbsp;·&nbsp; [Models](https://spicyapi.ai/models) &nbsp;·&nbsp; [Documentation](https://docs.spicyapi.ai) &nbsp;·&nbsp; [Status](https://status.spicyapi.ai)

</div>

<br>

Every generative model worth using lives behind a different account, a different contract and a
different client library. We put one endpoint in front of all of them — so switching from one video
model to another is a string change, not a migration.

Two things here work differently from the rest of the category, and both are deliberate.

<br>

## 🔓 &nbsp;No content review on our side

What a model produces is decided by **the model you pick** — not by a flag you have to set, an
approval queue, or a classifier sitting between you and the thing you paid for.

We measured how every route actually behaves and put the result on its model page, so you know what
you are buying *before* the bill arrives. That includes the uncomfortable cases: a model that
quietly returns something tamer than you asked for is worse than one that refuses outright, and we
label both rather than pretending the difference does not exist.

A sizeable part of the catalogue is LoRA-tuned for uncensored work. Those models live in their own
families with their own pricing and docs.

## 💵 &nbsp;Dollars, not credits

Prices are plain USD per request. Ask what a specific call will cost, get a number, and that number
is what gets held — then you are charged the real cost when it settles, never more than the hold.

No expiring balance. No conversion rate to reason about. No minimum top-up.

## 🔁 &nbsp;One request shape

Media generation is asynchronous everywhere, so it behaves the same everywhere: create a task, get a
`202`, then poll or take a webhook. Text models speak the OpenAI, Anthropic and Gemini wire formats
— point an existing client at our base URL and it keeps working.

<br>

## What you can generate

| | |
|:--|:--|
| 🎬 **Video** | Text-to-video, image-to-video, reference-to-video, editing, lip-sync and talking avatars, up to 4K<br><sub>Seedance 2.5 · Kling 3.0 · MiniMax H3 · Wan 3.0 · HappyHorse 1.1 · LTX 2.5 · Vidu Q3</sub> |
| 🎨 **Image** | Generation, editing, LoRA, upscaling, face and head swap<br><sub>GPT Image 2.5 · Nano Banana Pro · Seedream 5.0 Pro · Qwen Image 3.0 · Krea 2 · Z-Image · FLUX.1 Dev LoRA</sub> |
| 💬 **Text** | Chat and reasoning through compatible wire formats, with image, video and audio input on supported models<br><sub>Claude Opus 5.5 · Claude Sonnet 5.5 · Grok 4.7 · Gemini 3.7 Flash · DeepSeek V4 Pro · Kimi K3 · GLM 5.3</sub> |
| 🎧 **Audio** | Text-to-speech, music and transcription<br><sub>Gemini 3.8 TTS · Suno v6 · MiniMax Music 3.0 · Seed Speech 2.0 · MiniMax Speech 2.8 · HeartMuLa Transcribe</sub> |

<div align="right"><a href="https://spicyapi.ai/models"><b>Browse all 210+ endpoints »</b></a></div>

<br>

## Your first request

```bash
curl https://api.spicyapi.ai/api/v1/jobs/createTask \
  -H "Authorization: Bearer $SPICY_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
        "model": "bytedance/seedance-2.5/text-to-video",
        "input": { "prompt": "a lantern drifting through fog" }
      }'
```

A `202` means accepted, not finished. Read the task back until it reaches a terminal state, or hand
us a `callBackUrl` and we will tell you.

<br>

## Clients

| Language | Install | Source |
|:--|:--|:--|
| **TypeScript** | `npm i @spicyapi/sdk` | [spicy-sdk](https://github.com/spicyapi-ai/spicy-sdk) |
| **Go** | `go get github.com/spicyapi-ai/spicy-go` | [spicy-go](https://github.com/spicyapi-ai/spicy-go) |
| **Python** | `pip install spicyapi` | [spicy-python](https://github.com/spicyapi-ai/spicy-python) |
| **PHP** | from source for now | [spicy-php](https://github.com/spicyapi-ai/spicy-php) |
| **Java** | Maven `ai.spicyapi:spicyapi-java` | [spicy-java](https://github.com/spicyapi-ai/spicy-java) |

### For agents and the terminal

| | | Source |
|:--|:--|:--|
| **CLI** | `npx @spicyapi/cli status` — no key required | [spicy-cli](https://github.com/spicyapi-ai/spicy-cli) |
| **MCP server** | lets an agent inspect models and generate media itself | [spicy-mcp](https://github.com/spicyapi-ai/spicy-mcp) |
| **Agent Skill** | teaches Claude to drive any of the above | [spicy-skill](https://github.com/spicyapi-ai/spicy-skill) |
| **Proxy** | call us from a browser app without shipping your key | [spicy-proxy](https://github.com/spicyapi-ai/spicy-proxy) |

### For node-based workflows

| | | Source |
|:--|:--|:--|
| **ComfyUI** | every image, video and audio model as a ComfyUI node, no GPU needed | [comfyui-spicyapi](https://github.com/spicyapi-ai/comfyui-spicyapi) |

<br>

<div align="center">
<sub>

[spicyapi.ai](https://spicyapi.ai) &nbsp;·&nbsp; [docs.spicyapi.ai](https://docs.spicyapi.ai) &nbsp;·&nbsp; [@spicyapi_ai](https://x.com/spicyapi_ai) &nbsp;·&nbsp; [support@spicyapi.ai](mailto:support@spicyapi.ai)

</sub>
</div>
