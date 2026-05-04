# Most AI agents I audit fail in the first 48 hours of production.

Hi, I'm Danilo Lapegna. I do two things.

I run [DL Solutions](https://danilolapegna.com), a one-person consultancy in Amsterdam. I help founders and companies (mostly EU and Italian, not exclusively) ship AI automations and agentic systems that don't quietly catch fire when nobody's looking.

I write [Kintsugi Project](https://kintsugiproject.substack.com), a lifehacking newsletter with 4,000+ readers. It's where I think out loud about the boring side of being a builder.

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
  <a href="https://hachyderm.io/@danilolapegna" rel="me">
    <img src="https://img.shields.io/badge/Mastodon-@danilolapegna-6364FF?style=for-the-badge&logo=mastodon&logoColor=white" alt="Mastodon" />
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

### What I'm building this week

- An OWASP Top 10 for Agentic Applications mapping for an Italian mid-market client. Real case study, anonymous.
- A RAG pipeline on regulated EU documents that doesn't violate three GDPR principles by accident.
- An internal sales engine that uses Claude as a routing agent. Yes, dogfooding agentic security on my own funnel.

This list is more honest than "currently exploring AI". I update it when something ships or breaks.

---

### Three field notes from 12 months of agentic production

1. **Prompt injection isn't a future risk**. It already happened to a client of mine in week 2. The mitigation isn't filtering input. It's restricting what the agent is allowed to do, period.

2. **The "agent" abstraction lies to you**. Once an LLM has tools and memory, it's a distributed system with non-determinism baked in. Treat it like one: logs, dead-letter queues, idempotency, human-in-the-loop circuit breakers.

3. **The hardest part isn't the model. It's the second time the agent runs**. State leakage, role confusion, tool misuse: these only surface in repeated invocations under real workload. Single-prompt evals catch maybe 30% of what breaks.

---

### What I am not

- A "vibe-coding" influencer. I write code that runs at 4am for paying clients.
- A founder who rebrands every six months. DL Solutions is the same boring entity since 2017. Italian KvK 67250742, Dutch ZZP, you can verify.
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

- Site: [Danilo Lapegna](https://danilolapegna.com) (public calendar booking, async-first, no phone)
- LinkedIn: [danilo-lapegna](https://www.linkedin.com/in/danilo-lapegna/)
- Wikidata: [Q139593287](https://www.wikidata.org/wiki/Q139593287)

### Find me elsewhere (DL canonical identity)

- [Mastodon — hachyderm.io/@danilolapegna](https://hachyderm.io/@danilolapegna) (federated tech, fellow security/infra people)
- [IndieHackers — danilolapegna](https://indiehackers.com/danilolapegna) (solopreneur community)
- [F6S — danilolapegna](https://www.f6s.com/danilolapegna) (founder profile)
- [Sessionize — danilolapegna](https://sessionize.com/danilolapegna) (speaker bio for conference applications)
- [Gravatar — danilolapegna](https://gravatar.com/danilolapegna) (cross-platform avatar)
- [Newsletter — kintsugiproject.substack.com](https://kintsugiproject.substack.com) (lifehacking + builder mindset, evolving toward agentic AI / DL Solutions content)

15+ years in software engineering before this. The CV is on LinkedIn if you need it. Most of what mattered isn't in it.

---

### What I publish (deep guides, not posts)

The serious writing lives at [danilolapegna.com/guides](https://danilolapegna.com/guides) — bilingual EN/IT pillar + cluster:

- 🛡️ [Agentic AI Security for SMEs — the 2026 Guide](https://danilolapegna.com/guides/agentic-ai-security) (3000+ words pillar)
- 🎯 [OWASP Top 10 for Agentic Applications mapped to Italian SMBs](https://danilolapegna.com/guides/owasp-top-10-agentic-applications-italian-smb)
- 💉 [Prompt Injection 2026: real case studies and surgical mitigation](https://danilolapegna.com/guides/prompt-injection-2026-case-studies-italian-smb)
- 📜 [EU AI Act + DORA: regulatory timeline for AI agent builders](https://danilolapegna.com/guides/ai-act-dora-eu-regulatory-timeline-italian-smb)
- 🔐 [Minimum permissions for AI agents — least authority applied](https://danilolapegna.com/guides/least-authority-ai-agents-italian-smb)
- 📊 [Audit-ready agents: the logging that saves you when incidents happen](https://danilolapegna.com/guides/audit-ready-agents-logging-italian-smb)

---

### GitHub stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=danilolapegna&show_icons=true&hide_border=true&bg_color=1A1A2E&title_color=C9A84C&icon_color=C9A84C&text_color=FFFFFF" alt="GitHub stats" height="160" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=danilolapegna&layout=compact&hide_border=true&bg_color=1A1A2E&title_color=C9A84C&text_color=FFFFFF" alt="Top languages" height="160" />
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=danilolapegna&color=C9A84C&style=flat-square&label=Profile+views" alt="Profile views" />
  <img src="https://img.shields.io/github/followers/danilolapegna?style=flat-square&color=C9A84C&labelColor=1A1A2E" alt="Followers" />
</p>
