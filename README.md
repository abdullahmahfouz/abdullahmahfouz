### Hi, I'm Abdullah 
 
Computer Science Graduate @ Trent University · Peterborough / Toronto, Ontario
 
I'm a full-stack developer focused on building agentic AI tools and end-to-end applications, from hand-rolled systems code to production-deployed web apps.
 
[LinkedIn](https://linkedin.com/in/abdullah-mahfouz-5188b1306) · [Portfolio](https://abdullahmahfouz.github.io) · abdullahmahfouz@trentu.ca
 
---

<div align="center">
  <img src="https://skillicons.dev/icons?i=tailwind" height="60" alt="tailwindcss logo" />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=py" height="60" alt="python logo" />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" height="60" alt="react logo" />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/csharp/csharp-original.svg" height="60" alt="csharp logo" />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" height="60" alt="git logo" />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" height="60" alt="html5 logo" />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="60" alt="javascript logo" />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/npm/npm-original-wordmark.svg" height="60" alt="npm logo" />
</div>

---

### Projects

**[NeoWatch](https://main.d2m0an0vcg1iwk.amplifyapp.com/)** — Near-Earth Object Tracking Dashboard · [repo](https://github.com/abdullahmahfouz/Neo-Watch)
Live 3D dashboard tracking near-Earth objects from NASA's public feed, with impact-energy trends and hazard alerts.
- Daily scheduled ingest of NASA's NeoWs feed into PostgreSQL, computing kinetic-impact-energy estimates (E = ½mv²) snapshotted on every run to build a trend rather than a single number, returning `null` instead of a fabricated value when source data is missing or invalid
- Built a real 3D Earth in Three.js with NASA texture maps and a custom day-night terminator shader, rendering tracked objects as orbiting bodies positioned from their actual miss distance and velocity
- Redis-cached read endpoints with cache invalidation tied to ingest, plus CORS lockdown, per-IP rate limiting, and a shared-secret gate on the ingest endpoint
- Java, Spring Boot, PostgreSQL, Redis, React, Three.js, Tailwind CSS
 
**[HomeAgent](https://homeagent-deuf.onrender.com/)** — Agentic Real Estate Assistant · [repo](https://github.com/abdullahmahfouz/homeagent)
Conversational agent that automates end-to-end property search across 8 US states through natural language.
- Hand-rolled a two-tool Gemini 2.5 Flash function-calling loop (listings search, mortgage calculation) with automatic function-calling disabled, run as both blocking and SSE-streaming variants
- Built `guards.py`, a session-scoped rate limiter and daily/monthly token budget guard with disk-persisted state, plus strict CORS allowlisting and secret redaction
- React, Python, FastAPI, Gemini API, Repliers MLS API, Mapbox

**[Funniest Friend](https://github.com/abdullahmahfouz/Funniest-friend)** — Group Chat Humor Analyzer
Ranks friends by comedic tapback engagement across an iMessage group chat.
- Decoded iMessage's binary `chat.db` format in Python and computed a deterministic laugh score in JS from tapbacks, threaded replies, and reaction-y text, kept fully separate from an LLM layer that only narrates the funniest message
- Built a privacy-first split deployment: real chat data never touches git, only a generated static leaderboard ships to Vercel, gated behind custom session-cookie auth for in-app browser compatibility
- Next.js, React, Python, Gemini API, Vercel

**[DSA Visualizer](https://dsa-visualizer-ksnl.onrender.com/)** — Interactive DS&A Platform · [repo](https://github.com/abdullahmahfouz/dsa-visualizer)
Visualizes ~15 data structures and 30+ operations with a live time/space benchmarking engine.
- Time-travel scrubber via immutable per-step snapshots; Gemini-powered study assistant with automated code review scoring across 6 languages
- React, Flask, Gemini API

**Mark-and-Sweep Garbage Collector** · [repo](https://github.com/abdullahmahfouz/mark-and-sweep-gc)
Stack-based VM in C with a tagged-union object model.
- Recursive DFS from stack roots reclaims 100% of unreachable heap memory, including circular references that defeat reference counting; dynamic heap growth doubles capacity each collection cycle
- C

**Custom CLI Shell** · [repo](https://github.com/abdullahmahfouz/custom-cli-shell)
Unix-style shell with pipes, stream redirection, and 10+ builtins.
- Hand-rolled tokenizer handling nested quoting and escape sequences across a modular 5-layer architecture; tab auto-completion via Longest Common Prefix
- C#, .NET 9.0

**Freelance — Brendon Rodney**
Portfolio site for the Paris 2024 Olympic Gold Medalist (4x100m relay).
- Zero-dependency, build-free static site achieving a 100/100 Lighthouse score across performance, accessibility, and SEO; deployed on GitHub Pages at $0/month
---
 
### Technical Skills
 
- **Languages:** C, C#, Python, JavaScript, Java, SQL
- **Frontend:** React, Next.js, Tailwind CSS
- **Backend:** Flask, FastAPI, .NET 9.0, REST APIs
- **AI / Agents:** Gemini API, Claude API, tool-use / function calling
- **Databases:** MySQL, Supabase, PostgreSQL
- **Tools:** Git, GitHub, Linux/Unix, Vercel, Railway, Render
### Spoken Languages
- English: Fluent
- Arabic: Native
---
 
*Currently job searching for SWE roles in Toronto — always open to connecting.*
 
<div align="center">
  <a href="https://www.linkedin.com/in/abdullah-mahfouz-5188b1306/" target="_blank">
    <img src="https://img.shields.io/static/v1?message=LinkedIn&logo=linkedin&label=&color=0077B5&logoColor=white&labelColor=&style=for-the-badge" height="25" alt="linkedin logo" />
  </a>
</div>


