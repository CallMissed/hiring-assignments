# Assignment — Next.js Engineer

Hey 👋 Build a small but real AI chatbot on **Next.js** that talks to the **CallMissed API**. This mirrors the kind of product surface we ship — so we care about both the engineering and the product feel.

**Time:** ~6–10 focused hours. AI tools (Cursor, v0, Claude, Copilot, …) are fully allowed and encouraged — tell us how you used them.

> First, read [`GETTING_STARTED.md`](GETTING_STARTED.md) to get your free `cm_` API key and see working examples.

---

## What to build

A **chatbot web app in Next.js (App Router)** with **serverless API routes** (Route Handlers / Server Actions — your CallMissed key must stay server-side, never shipped to the browser). It must:

### Core features (required)
1. **Chat** — a clean conversational UI with the **`kimi-k2.7-code`** model. **Stream** the responses (SSE / streaming) for good UX.
2. **Generate images** — the user can ask for an image (e.g. "draw a neon city") and the bot returns a generated image inline, using **`flux-2-klein-9b`** (`POST /v1/images/generations`).
3. **Image input (vision)** — the user can **upload/paste an image** and ask about it; you send it to **`kimi-k2.7-code`** (it's vision-capable) and show the answer.
4. **A short in-app guide** — somewhere in the UI, briefly tell the user how to get their own CallMissed API key (link to [docs.callmissed.com](https://docs.callmissed.com)) and which models this app uses. This is part of the product, not just the README.

> Use exactly these two models: **`kimi-k2.7-code`** (chat + vision) and **`flux-2-klein-9b`** (images). No model selector needed.

### Make it solid
- Keep the API key **server-side only** (serverless route). The browser should never see `cm_`.
- Handle loading, errors (402/403/429/`unsupported_image_input`), and empty states gracefully.
- Decode base64 images (`data[].b64_json`) and render them; let the user download a generated image.
- Reasonable responsive layout. It doesn't need to be gorgeous, but it should feel intentional.

### Nice-to-haves (only if you have time — pick what interests you)
- Deploy it (Vercel/Cloudflare/Netlify) and share the live URL.
- Conversation history / multiple chats, markdown rendering, copy-code buttons.
- Image **size**/aspect controls, choosing among the 6 free image models.
- Light/dark theme, keyboard shortcuts, streaming "stop" button.
- Basic rate-limit / abuse guard on your serverless route.

We are **not** expecting all of these. A focused, polished core beats a pile of half-finished extras.

---

## Tech constraints
- **Next.js** (App Router) with **serverless** API routes/server actions for all CallMissed calls.
- TypeScript preferred. Any styling approach (Tailwind, CSS modules, shadcn, …) is fine.
- Use the OpenAI SDK pointed at `https://api.callmissed.com/v1`, or `fetch` directly — your call.

---

## What we're evaluating
- **Architecture** — clean separation of server/client, sensible serverless route design, streaming done right.
- **Product taste** — does it feel good to use? Are loading/error/empty states handled well?
- **Code quality** — readability, types, structure, no dead code, no leaked secrets.
- **Correctness** — chat (`kimi-k2.7-code`), image gen (`flux-2-klein-9b`), and vision actually work against the free tier.
- **Communication** — your README + commit history tell the story of your decisions.

---

## Submission
See the [root README rules](../README.md). In short:
1. Build in a **public** GitHub repo under your account.
2. Update the repo **`README.md`**: what you built, how to run it locally (env vars + `.env.example`), trade-offs, what you'd do next, and where you used AI.
3. Commit your **`resume.pdf`**.
4. If deployed, include the live URL.
5. **Email the repo link to [karan@callmissed.com](mailto:karan@callmissed.com)** — subject `Assignment — Next.js — <Your Name>`.

Have fun with it — we genuinely enjoy seeing how people build these. 🚀
