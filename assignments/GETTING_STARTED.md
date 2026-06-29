# Getting Started with the CallMissed API

Both engineering assignments use the **CallMissed API**. It's **OpenAI-compatible**, so you can use the official OpenAI SDKs by changing only the base URL and the key.

👉 **Read the official docs — they have everything (auth, examples, streaming, errors):**
**[docs.callmissed.com](https://docs.callmissed.com)**

Key pages you'll want:
- **Get an API key / Chat:** https://docs.callmissed.com/chat-completion
- **Image generation:** https://docs.callmissed.com/image-generation
- **Vision (image input):** https://docs.callmissed.com/chat-completion#vision-image-input
- **Models & free tier:** https://docs.callmissed.com/models

---

## 1. Get your free API key

1. Sign up / log in at **[app.callmissed.com](https://app.callmissed.com)** → **Profile → API Keys → Create API Key**.
2. Give the key the **`llm`** and **`image`** permissions.
3. Copy it (looks like `cm_xxxx…`, shown once). Put it in an env var — never commit it.

```bash
export CALLMISSED_API_KEY="cm_your_key_here"
```

- **Base URL:** `https://api.callmissed.com/v1`
- **Auth header:** `Authorization: Bearer cm_your_key`

---

## 2. Models to use for these assignments

Use **exactly these two free-tier models** — nothing else:

| Use | Model ID |
|-----|----------|
| **Chat + Vision (image input)** | `kimi-k2.7-code` |
| **Image generation** | `flux-2-klein-9b` |

`kimi-k2.7-code` is vision-capable, so the **same** model powers both text chat and image-understanding. You do **not** need a model selector for this assignment — just use these two.

---

That's it. Everything else (request/response shapes, streaming, base64 image decoding, error codes) is in the **[docs](https://docs.callmissed.com)**. Build something you'd be proud to show us. 🙌
