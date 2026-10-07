### Hi, I'm Yash 👋

**Software engineer building production AI systems: voice agents, MCP servers, LLM pipelines, and the full-stack products around them.**
SDE at [SalesUp](https://salesup.club) (B2B sales-tech, remote) since Dec 2024 · Navi Mumbai, India

---

#### What I've built (in private company repos, so here's the short version)

- **PitchArena ([pitcharena.club](https://pitcharena.club)), a live voice-AI sales-training platform.** Reps practise live calls with AI prospects in the browser, and an LLM scores every line. I built it nearly solo (300+ commits):
  - Iterated through four real-time voice architectures, ending on LiveKit Agents.
  - Tuned turn-taking from production call data.
  - Multilingual STT/TTS routing across English and 9 Indic languages.
  - A per-call cost model.
  - About 1,000 graded practice calls in the first quarter.
- **A multi-tenant MCP server over a production Postgres database.** Clients and leadership query their own data from Claude. Isolation is defence in depth:
  - per-user scoped tokens
  - Postgres RLS (`SET LOCAL ROLE`), column grants and a table allowlist
  - a response guard that scrubs any cross-tenant rows

  Our CEO wrote about it [here](https://www.linkedin.com/posts/ychowdhury_99-reduction-in-time-to-identify-great-performers-share-7441930022124187648-3YZg/).
- **A per-client AI agent fleet.** One Docker container per client, managed by a host daemon so the API never touches the Docker socket. It has health reconciliation, Slack/WhatsApp gateways and persistent memory.
- **The core backend (Node/Express + Postgres):** I'm the #1 contributor. It handles ~1.8M leads and ~1.5M call logs, with a WhatsApp gateway (Meta/Twilio), LLM qualification and transcription pipelines, and a security audit across 5 repos.

#### Stack
`TypeScript` `Node.js` `PostgreSQL` `Supabase` `React` `Next.js` `Astro` · `LiveKit` `Deepgram` `Claude` `Gemini` `MCP` · `Docker` `GitHub Actions` `Cloudflare Workers` `AWS`

#### Elsewhere
[LinkedIn](https://www.linkedin.com/in/yash-bisht/) · beyash08@gmail.com

