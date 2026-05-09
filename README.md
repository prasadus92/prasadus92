<div align="center">

# Prasad Subrahmanya

**Founder** · [Luminik](https://luminik.io)
12 years shipping software · Based in Oslo · Building solo

[prasad.tech](https://prasad.tech) · [LinkedIn](https://linkedin.com/in/prasadus) · [prasadus92@gmail.com](mailto:prasadus92@gmail.com)

</div>

---

## What I'm building now

[**Luminik**](https://luminik.io) helps B2B sales and marketing teams turn the events they attend (RSA, Black Hat, Money20/20, fintech summits) into pipeline. Bootstrapped, live with paying customers. I am the only full-time person on the team.

A couple of outcomes from our customers:

- A Series C cybersecurity company attributed $2.4M of pipeline to RSA, Black Hat, and one regional summit, sourced and sequenced through Luminik.
- A Series A identity verification company attributed $2M across fifteen fintech events in the second half of 2025.

## What I've shipped before

- **Aura** at Bain Founder's Studio: a PE due-diligence platform. Took it from 0 to $3.6M ARR in 18 months. The team grew from five engineers to thirty-three over the same window.
- **Mainteny**: co-founded. $2.7M seed, European field-services SaaS.
- **SnowOptix**: Snowflake cost-optimisation tool. Bootstrapped, used by a top-3 global consulting firm.
- **BlueJeans** (started 2014): backend engineer on the video conferencing team. Where I first watched a real engineering org coordinate, before I had to do it myself with no team to lean on.

## How the work actually happens

A dedicated team of agents, named after Batman side-characters, handles the recurring engineering work for Luminik. Each one is shaped around a specific job and operates under a contract for what it can decide alone and what comes through me.

| Codename       | Role                                          | Trigger                  |
|----------------|-----------------------------------------------|--------------------------|
| Lucius         | Feature development, one repo at a time       | `agent:implement` label  |
| Alfred         | Cross-repo coordinator                        | `agent:cross-repo` label |
| Bane           | Test coverage (max one PR per run)            | Daily cron               |
| Oracle         | Staging monitor (escalates above threshold)   | Daily 06:00 UTC          |
| Ra's al Ghul   | PR review (correctness, security, integrity)  | PR opened                |
| Bat-Signal     | Slack notifier, relay only                    | Called by other agents   |

The stack is open source: Hermes Agent (Nous Research) drives the orchestration loop on free Gemini Flash, Claude Code handles real coding work via ACP, and a local gbrain (Garry Tan) instance holds a 107-page knowledge base of specs and CLAUDE.md files queryable from anywhere on the box. The whole thing runs on a Mac Mini.

Full write-up: [*Building Toward a Team of Digital Employees on a Mac Mini*](https://prasad.tech/blog/dedicated-mac-mini-solo-startup.html).

## Recent open source contributions

While setting up the agent stack, three things were broken or badly defaulted in tools I depended on. All in public trackers.

- [**Hermes Agent #12251**](https://github.com/NousResearch/hermes-agent/pull/12251). Gemini auth regression after the project switched Google AI Studio auth from `Bearer` to `x-goog-api-key`. I isolated the repro on the live `/v1beta/openai` endpoint, and the maintainer landed a clean superseding fix the same day. *Merged.*
- [**Hermes Agent #12224**](https://github.com/NousResearch/hermes-agent/issues/12224). The WhatsApp `PLATFORM_HINT` told every model "WhatsApp does not render markdown" and silently overrode persona files. WhatsApp does support `*bold*`, `_italic_`, `~strike~`, code, fenced blocks, and bullet lists. *Open.*
- [**gbrain #89**](https://github.com/garrytan/gbrain/pull/89). v0.12.0 hardcodes OpenAI embeddings, which silently undoes the zero-marginal-cost story for anyone running Gemini elsewhere. Confirmed the community Gemini-embedding patch on the same 107-page corpus and left a +1 with a repro. *Open.*

## Recent writing

Long-form on solo building, agent infrastructure, encoding judgment for AI tooling, and what coordination looks like when you are the team.

- [*Building Toward a Team of Digital Employees on a Mac Mini*](https://prasad.tech/blog/dedicated-mac-mini-solo-startup.html). Hermes Agent + Claude Code via ACP + gbrain, three upstream bugs filed along the way.
- [*gstack, CLAUDE.md, and the Work That Frameworks Don't Cover*](https://prasad.tech/blog/gstack-solo-builder.html). Where in-repo instruction files stop, and cross-session memory needs to start.
- [*What It Actually Costs to Build a Serious Product Alone in 2026*](https://prasad.tech/blog/building-alone-in-2026.html). The cost structure of compressing a team into one desk.
- [*Building a $3.6M ARR Product Inside a Consulting Firm*](https://prasad.tech/blog/zero-to-one-bain.html). The Aura story, five engineers to thirty-three.

[All posts at prasad.tech](https://prasad.tech).

## Stack

| Layer                 | What I use                                                  |
|-----------------------|-------------------------------------------------------------|
| Backend               | Kotlin · Quarkus · Postgres · AWS ECS                       |
| Frontend              | React · TypeScript · Vite · Tailwind                        |
| Mobile                | Expo · React Native                                         |
| Data and integrations | Python workers · Nango · Apollo · Salesforce · HubSpot      |
| AI / agent loop       | Claude Code · Gemini Flash · Hermes Agent · gbrain · MCP    |
| Writing               | Astro (prasad.tech) · CLAUDE.md spec discipline            |

## Where to find me

[**LinkedIn**](https://linkedin.com/in/prasadus) · [**prasad.tech**](https://prasad.tech) · [prasadus92@gmail.com](mailto:prasadus92@gmail.com)

For Luminik specifically: [luminik.io](https://luminik.io).

---

<div align="center">

*Batman taught me preparation beats superpowers. The Batmobile is not on the Luminik roadmap, but the codenames suggest otherwise.*

</div>
