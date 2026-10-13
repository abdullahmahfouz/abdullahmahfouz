<div align="center">

<img src="assets/banner.png" alt="Abdullah Mahfouz" width="100%">

<br>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abdullah-mahfouz-5188b1306/)
[![Portfolio](https://img.shields.io/badge/Portfolio-0F172A?style=for-the-badge&logo=githubpages&logoColor=white)](https://abdullahmahfouz.github.io)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:abdullahmahfouz@trentu.ca)

[**Featured projects**](#featured-projects) &nbsp;|&nbsp; [**Systems**](#systems-programming) &nbsp;|&nbsp; [**Client work**](#client-work) &nbsp;|&nbsp; [**Stack**](#tech-stack) &nbsp;|&nbsp; [**Contact**](#contact)

</div>

---

## About

I just finished my CS degree at Trent University. I live between Peterborough and Toronto, and I'm looking for a full-time role in Toronto.

Lately I've been building apps where an LLM does more than chat. HomeAgent searches real listings and works out the mortgage itself, and my telematics project lets you ask questions about a vehicle's driving data. I also like going low-level: I've written a garbage collector in C and a Unix-style shell in C#.

I mostly work in Python, JavaScript/React, Java with Spring Boot, C# and C.

---

## Featured projects

Click any screenshot to open the live app.

### Telematics Pipeline: driver safety analytics

![.NET](https://img.shields.io/badge/.NET_9-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini-4285F4?style=flat-square&logo=googlegemini&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Mapbox](https://img.shields.io/badge/Mapbox-000000?style=flat-square&logo=mapbox&logoColor=white)

Real-time ingestion and driver-safety analytics for a vehicle fleet, from raw accelerometer streams to a live dashboard. [**View code**](https://github.com/abdullahmahfouz/Telematics-Ingestion-Driver-Safety-Analytics-Pipeline)

- Rule-based engine flags harsh braking, cornering, and acceleration; events persist to PostgreSQL and roll up into a Redis leaderboard that degrades gracefully when Redis is down
- Two-tier auth: hashed per-device API keys gate ingestion, while operators get short-lived JWTs that the Python AI service validates and forwards instead of using a blanket service credential
- Gemini safety assistant answers plain-English questions about a device's driving data via tool calling; a C# trip simulator replays scripted harsh events for demo data

### NeoWatch: near-Earth object tracker

[<img src="assets/shot-neowatch.png" alt="NeoWatch live dashboard" width="100%">](https://main.d2m0an0vcg1iwk.amplifyapp.com/)

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=threedotjs&logoColor=white)

Live 3D dashboard of near-Earth objects from NASA's public feed, with impact-energy trends and hazard alerts. [**View code**](https://github.com/abdullahmahfouz/Neo-Watch)

- Daily ingest into PostgreSQL with impact-energy snapshots, so you see a trend, not one number
- Real 3D Earth with a custom day/night shader; objects positioned from actual miss distance and velocity
- Redis-cached endpoints, rate limiting, CORS lockdown, secret-gated ingest

### HomeAgent: agentic real estate assistant

[<img src="assets/shot-homeagent.png" alt="HomeAgent live app" width="100%">](https://homeagent-deuf.onrender.com/)

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini-4285F4?style=flat-square&logo=googlegemini&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)

Ask for properties in plain English across 8 US states; the agent searches listings and runs mortgage math itself. [**View code**](https://github.com/abdullahmahfouz/homeagent)

- Hand-rolled Gemini function-calling loop (blocking and SSE streaming)
- Session rate limiter plus token-budget guard with persisted state

### DSA Visualizer: interactive data-structures platform

[<img src="assets/shot-dsa.png" alt="DSA Visualizer live app" width="100%">](https://dsa-visualizer-ksnl.onrender.com/)

![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini-4285F4?style=flat-square&logo=googlegemini&logoColor=white)

About 15 data structures, 30+ operations, live time/space benchmarking, and a time-travel step scrubber. [**View code**](https://github.com/abdullahmahfouz/dsa-visualizer)

### Funniest Friend: group chat humor analyzer

[<img src="assets/card-funniest.png" alt="Funniest Friend overview" width="100%">](https://github.com/abdullahmahfouz/Funniest-friend)

Decodes iMessage's binary `chat.db` and ranks friends by comedic engagement. Privacy-first: private data never touches git. [**View code**](https://github.com/abdullahmahfouz/Funniest-friend)

---

## Systems programming

<table>
<tr>
<td width="50%" valign="top">

[<img src="assets/card-gc.png" alt="Mark-and-Sweep GC" width="100%">](https://github.com/abdullahmahfouz/Mark-Sweep)

**[Mark-and-Sweep GC](https://github.com/abdullahmahfouz/Mark-Sweep)**
Stack-based VM in C with a tagged-union object model. Reclaims 100% of unreachable memory, including circular references that defeat ref-counting.

</td>
<td width="50%" valign="top">

[<img src="assets/card-shell.png" alt="Custom CLI Shell" width="100%">](https://github.com/abdullahmahfouz/Shell)

**[Custom CLI Shell](https://github.com/abdullahmahfouz/Shell)**
Unix-style shell in C# with pipes, redirection, 10+ builtins, a hand-rolled tokenizer, and tab completion.

</td>
</tr>
</table>

---

## Client work

- **Brendon Rodney**: portfolio site for the Paris 2024 Olympic gold medalist (4x100m relay). Zero-dependency static site, 100/100 Lighthouse, $0/month hosting.

---

## Tech stack

<div align="center">

![C](https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=black)
![C#](https://img.shields.io/badge/C%23-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)

</div>

**AI and agents:** Gemini API, Claude API, tool use / function calling
**Spoken languages:** English (fluent), Arabic (native)

---

## GitHub stats

<div align="center">

![Stats](https://github-readme-stats.vercel.app/api?username=abdullahmahfouz&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&hide_rank=true)
![Top languages](https://github-readme-stats.vercel.app/api/top-langs/?username=abdullahmahfouz&layout=compact&theme=tokyonight&hide_border=true)

</div>

---

## Contact

I recently graduated and I'm open to opportunities in Toronto. The fastest way to reach me is [LinkedIn](https://www.linkedin.com/in/abdullah-mahfouz-5188b1306/) or [email](mailto:abdullahmahfouz@trentu.ca).
