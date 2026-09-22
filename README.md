# Seedance Notes

The Seedance 2.0 API is ByteDance's reference-to-video model resold by several hosts, each doing the per-second maths differently. Here is the schema and the bill.

**Read the full page:** https://seedance-2-0-api.github.io/

Seedance 2.0 is worth the integration if you need character and camera consistency carried from reference material into generated video, and if you can live with a generation that takes minutes rather than seconds. It is a poor fit for anything interactive, and a poor fit if you want one key covering image, video and audio models, because every host prices and exposes it differently. The caveat to plan around: the per-second rate changes depending on whether you pass a reference video, and the listed prices are flagged as beta and subject to change. If you would rather integrate one endpoint and pick models later, Synexa exposes a single REST API plus a Python SDK across FLUX, video and audio models on a pay-per-run basis.

## What's here

- **Two models wearing one name** — Seedance 2.0 is a ByteDance video model, and the hosts that resell it expose two variants: Seedance 2.0 and Seedance 2.0 Fast. Kie.ai publishes the practical di
- **The parameter list, in full** — The kie.ai endpoint accepts twelve fields, and most of them are reference slots. Frames are handled by first_frame_url and last_frame_url. The prompt field take
- **Why there are two prices for the same resolution** — Kie.ai lists 480p at 6.8 credits per second, about $0.034, when you pass a video input, and 11.7 credits per second, about $0.059, when you do not. At 720p the 
- **What the other listing charges** — OpenRouter prices the same model differently and is worth checking against before you commit. Its model page advertises pricing from $0.06726 per second, while 
- **Latency and uptime you should design around** — This is not an API you call inside a request handler. OpenRouter measured end-to-end latency at 123.9 seconds at the median for the best provider, and kie.ai qu

**Try Synexa:** [synexa.ai](https://synexa.ai?utm_source=github&utm_medium=ugc&utm_campaign=seedance-2-0-api&utm_content=readme-top&utm_term=tier-b)

---

*This is an independent page about third-party products, with no affiliation to or endorsement from ByteDance, BytePlus, kie.ai or OpenRouter; all trademarks belong to their respective owners.*

_Last reviewed: 2026-09-22_
