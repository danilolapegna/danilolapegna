# I build systems across AI, software and business, and I run them myself before I recommend them.

Hi, I'm Danilo Lapegna. Amsterdam.

I run [DL Solutions](https://danilolapegna.com), a one-person company. I help founders and companies, mostly in the EU, ship AI automations and agentic systems that keep working when nobody is watching. In parallel I build and operate my own products, which is where most of what I know about failure modes actually comes from. Advising on someone else's architecture teaches you a lot. Being on the hook for yours at 4am teaches you the rest.

Process comes before technology. That is the part most people skip.

I also write [Tech, AI & Life Quests](https://danilolapegna.substack.com), a weekly builder newsletter with 4,000+ readers, where I think out loud about the boring side of building.

<p align="center">
  <a href="https://danilolapegna.com">
    <img src="https://img.shields.io/badge/site-danilolapegna.com-1A1A2E?style=for-the-badge&labelColor=C9A84C&color=1A1A2E" alt="danilolapegna.com" />
  </a>
  <a href="https://www.linkedin.com/in/danilo-lapegna/">
    <img src="https://img.shields.io/badge/LinkedIn-danilo--lapegna-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="https://www.wikidata.org/wiki/Q139593287">
    <img src="https://img.shields.io/badge/Wikidata-Q139593287-006699?style=for-the-badge&logo=wikidata&logoColor=white" alt="Wikidata" />
  </a>
</p>

---

### Tech stack I ship with

<p>
  <img src="https://img.shields.io/badge/-Anthropic_Claude-D97757?style=flat-square&logoColor=white" alt="Claude" />
  <img src="https://img.shields.io/badge/-AWS_Bedrock-FF9900?style=flat-square&logo=amazon-aws&logoColor=white" alt="AWS Bedrock" />
  <img src="https://img.shields.io/badge/-Azure_OpenAI-0078D4?style=flat-square&logo=microsoft-azure&logoColor=white" alt="Azure OpenAI" />
  <img src="https://img.shields.io/badge/-OpenAI-412991?style=flat-square&logo=openai&logoColor=white" alt="OpenAI" />
  <img src="https://img.shields.io/badge/-TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/-PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/-Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white" alt="Supabase" />
  <img src="https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/-OpenTelemetry-425CC7?style=flat-square&logo=opentelemetry&logoColor=white" alt="OpenTelemetry" />
  <img src="https://img.shields.io/badge/-OWASP_ASI-000000?style=flat-square&logo=owasp&logoColor=white" alt="OWASP" />
</p>

---

### The three ways I work

**Reuse what I have already built.** Products and tools that exist and run today, so you start from something working instead of from a blank repo. The open-source part of that lives here on GitHub.

**Hand me a project.** AI automations, MVPs, agentic systems and the cloud infrastructure under them. I map the thing, build it, automate the repetitive parts, then hand over something that runs without me in the loop.

**Bring me a business doubt.** Sometimes the useful thing is not a build, it is one conversation with someone who has shipped this before and will tell you which of your three options is actually two.

The current state of each project, with honest labels (in production, internal use, experiment, prototype), lives on [danilolapegna.com](https://danilolapegna.com). I keep it there rather than here, so that this page does not quietly go stale while I am busy building.

---

### Open source

- **[vibecoding-skill-pack](https://github.com/danilolapegna/vibecoding-skill-pack)**. A Claude Code skill pack for structured agentic building, with a Failure Mode Registry at its core: a catalogue of failure modes from real post-mortems, split between how agentic systems get designed wrong and how green code reaches production and does not work. Every generated prompt declares which failure modes it prevents and which test gate verifies the prevention. MIT, drop-in install.

New entries land in that registry when something actually breaks and gets diagnosed, not on a content schedule. That is the honest version of "regularly updated".

---

### Field notes from running agents in production

1. **Prompt injection isn't a future risk.** It happened to a client of mine in week 2. The mitigation isn't filtering input. It's restricting what the agent is allowed to do, period.

2. **The "agent" abstraction lies to you.** Once an LLM has tools and memory, it's a distributed system with non-determinism baked in. Treat it like one: logs, dead-letter queues, idempotency, human-in-the-loop circuit breakers.

3. **The hardest part isn't the model, it's the second time the agent runs.** State leakage, role confusion, tool misuse: these only surface in repeated invocations under real workload. Single-prompt evals catch maybe 30% of what breaks.

4. **Green CI is not a working product.** Code compiles, deploys, and is still dead: env vars missing at build time, a shared module that takes down every function importing it, an endpoint that answers your tests and rejects the credential its own scheduler sends. Verify from the artifact you actually served, never from the toast that said it worked.

5. **A rule nobody can fail is not a rule.** Written guidance that asks people, or agents, to remember something has a measurable half-life of about a week. If it matters, it needs a command that fails when it is skipped.

---

### What I am not

- A "vibe-coding" influencer. I write code that runs at 4am for paying clients.
<!-- leak-scan-allow: public business register identity, deliberately published so the claim is verifiable -->
- A founder who rebrands every six months. DL Solutions is the same boring entity since 2017. Dutch ZZP, KvK 67250742, Amsterdam. You can verify it.
- An "AI optimist" or "AI pessimist". Both positions are advertising.

---

### Five rules I've stolen and apply

1. **"Make it work, then make it right, then make it fast."** *Knuth, basically.* Premature optimization in agentic systems shows up as three-step chains that should have been one.

2. **"If you can't ship in 4 weeks, the scope is wrong, not the timeline."** *Myself, after watching 6-month proofs-of-concept die unshipped.* Most clients agree once you show them what 4 weeks actually buys.

3. **"Distrust your own demo."** *Paraphrased from every infra engineer who's ever been on call.* A demo runs once. Production runs ten thousand times. Build for the second number.

4. **"The cost of the wrong abstraction is greater than the cost of duplication."** *Sandi Metz.* Especially true for agent tools. Two ugly tools that ship beat one elegant one that doesn't.

5. **"Async by default, sync by exception."** *Adapted from the Basecamp playbook.* I don't take phone calls. Calendar is public. The work is the deliverable, not the meetings.

---

### Reach me

- Site: [danilolapegna.com](https://danilolapegna.com), public calendar booking, async-first, no phone
- LinkedIn: [danilo-lapegna](https://www.linkedin.com/in/danilo-lapegna/)
- Wikidata: [Q139593287](https://www.wikidata.org/wiki/Q139593287)

### Find me elsewhere

- [IndieHackers](https://indiehackers.com/danilolapegna), solopreneur community
- [F6S](https://www.f6s.com/danilolapegna), founder profile
- [Sessionize](https://sessionize.com/danilolapegna), speaker bio
- [Gravatar](https://gravatar.com/danilolapegna), cross-platform avatar
- [Newsletter](https://danilolapegna.substack.com), Tech, AI & Life Quests

15+ years in software engineering before this. The CV is on LinkedIn if you need it. Most of what mattered isn't in it.

---
