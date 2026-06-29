# Assignment — Python Backend Engineer

Hey 👋 Build a backend **chatbot API** in **Python** that wraps the **CallMissed API** and adds real product logic. You can pair it with **any frontend you like** (or none — a great API + docs is enough). We care most about the backend.

**Time:** ~6–10 focused hours. AI tools are fully allowed and encouraged — tell us how you used them.

> First, read [`GETTING_STARTED.md`](GETTING_STARTED.md) to get your free `cm_` API key and see working examples.

---

## What to build

A **Python backend service** (FastAPI / Flask / Django / Litestar — your choice; FastAPI is what we use) that exposes a chatbot and proxies CallMissed. It must:

### Core features (required)
1. **Chat endpoint** — a `POST` endpoint that takes a user message (and conversation history) and returns the reply from **`kimi-k2.7-code`**. **Streaming** (SSE) is strongly preferred for chat.
2. **Image generation** — an endpoint that takes a prompt and returns a generated image (base64 or a saved/served file), using **`flux-2-klein-9b`** (`POST /v1/images/generations`).
3. **Vision (image input)** — an endpoint that accepts an **uploaded image** + a question and returns the answer, using **`kimi-k2.7-code`** (it's vision-capable). Multipart upload or base64 — your design.
4. **Document it** — your README must explain how to get a CallMissed API key (link to [docs.callmissed.com](https://docs.callmissed.com)), which two models this service uses, and how to call **your** endpoints (example `curl`s). Treat your API as a product.

> Use exactly these two models: **`kimi-k2.7-code`** (chat + vision) and **`flux-2-klein-9b`** (images). No model selector needed.

### Make it solid
- Keep the CallMissed key in an env var, **server-side only**. Include a `.env.example`.
- Validate input; handle upstream errors (402/403/429/`unsupported_image_input`) and return clean error responses (don't leak raw upstream errors or your key).
- Sensible structure: routing, a service/client layer for CallMissed, models/schemas. Not everything in one file.

### Nice-to-haves (only if you have time — pick what interests you)
- A simple frontend (anything — plain HTML, Streamlit, React, Gradio) to demo it.
- Conversation persistence (SQLite/Postgres/in-memory), per-session history.
- Tests (pytest) for your service layer / routes.
- Dockerfile + run instructions; deploy it and share the URL.
- Rate limiting, request size limits, or a tiny auth layer on your own API.
- Streaming the image-gen progress, or letting the caller pick image size/model.

We are **not** expecting all of these. A clean, well-tested, well-documented core is the goal.

---

## Tech constraints
- **Python 3.10+**, any web framework.
- Use the OpenAI SDK pointed at `https://api.callmissed.com/v1`, or `httpx`/`requests` directly.
- Frontend (if any) is entirely your choice — it does not affect scoring much; the backend does.

---

## What we're evaluating
- **API design** — clear, predictable endpoints; good request/response shapes; streaming done right.
- **Code structure** — separation of concerns, a real CallMissed client/service layer, typed schemas.
- **Robustness** — input validation, error handling, no secret/error leakage, edge cases.
- **Correctness** — chat (`kimi-k2.7-code`), image gen (`flux-2-klein-9b`), and vision actually work against the free tier.
- **Communication** — README + commit history explain your decisions; example requests provided.

---

## Submission
See the [root README rules](../README.md). In short:
1. Build in a **public** GitHub repo under your account.
2. Update the repo **`README.md`**: what you built, how to run it (env vars + `.env.example`), example requests, trade-offs, what you'd do next, and where you used AI.
3. Commit your **`resume.pdf`**.
4. If deployed, include the live URL.
5. **Email the repo link to [karan@callmissed.com](mailto:karan@callmissed.com)** — subject `Assignment — Python — <Your Name>`.

Looking forward to it — show us how you think about backends. 🚀
