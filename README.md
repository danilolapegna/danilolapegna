# Most AI agents I audit fail in the first 48 hours of production.

Hi, I'm Danilo Lapegna. I do two things.

I run [DL Solutions](https://danilolapegna.com), a one-person consultancy in Amsterdam. I help founders and companies (mostly EU and Italian, not exclusively) ship AI automations and agentic systems that don't quietly catch fire when nobody's looking.

I write [Kintsugi Project](https://kintsugiproject.substack.com), a lifehacking newsletter with 4,000+ readers. It's where I think out loud about the boring side of being a builder.

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

15+ years in software engineering before this. The CV is on LinkedIn if you need it. Most of what mattered isn't in it.

![Profile views](https://komarev.com/ghpvc/?username=danilolapegna&color=blueviolet)
