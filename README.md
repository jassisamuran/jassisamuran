# Hi, I'm Jaspreet Singh 👋

**AI/Backend Engineer** — I build systems where AI does real engineering work.

---

## 🚀 What I'm Building

### [NEXUS](https://github.com/jassisamuran/nexus) — Autonomous AI Software Engineering Platform
> You paste a GitHub repo URL and describe a task. 5 AI agents plan, code, test, review, and open a Pull Request automatically.

**How it works:**
- 🧠 **Architect** — reads the codebase using AST-based RAG before writing any plan
- 💻 **Coder** — writes complete implementations, self-corrects on test failures
- 🧪 **Tester** — writes and runs unit tests, fixes failures automatically
- 🔍 **Reviewer** — checks for bugs, security issues, missing error handling
- 🔀 **Git Agent** — creates branch, commits, opens Pull Request on GitHub

**Key engineering decisions:**
- AST-based chunking (never splits mid-function) → ChromaDB → cosine similarity search
- Redis pub/sub bridges Celery (sync) ↔ FastAPI WebSocket (async) — sub-100ms latency
- Per-stage executor isolation to prevent AutoGen tool registration conflicts

`AutoGen` `FastAPI` `ChromaDB` `PostgreSQL` `Redis` `Celery` `React` `Docker`

**Live:** [43.205.119.173/dashboard](http://43.205.119.173/dashboard)

---

### [ProShop](https://github.com/jassisamuran/proshop) — E-Commerce Platform with AI Support Agent
> Full-stack e-commerce with a production AI chatbot microservice.

- **LLM selective routing** — order queries handled by rule-based handlers, bypassing GPT-4o (~65% API cost reduction)
- **Semantic cache** using cosine similarity — zero LLM cost for repeated queries
- **Circuit breaker** — auto-fallback from OpenAI → Anthropic on failure
- **Multi-tenant RAG** with ChromaDB — each org has isolated knowledge base
- **Stateful pagination** — 50+ orders in one DB query, 5 per turn, no re-queries

`React` `Node.js` `FastAPI` `GPT-4o-mini` `ChromaDB` `Redis` `MongoDB` `Docker`

**Live:** [ecommercefrontend-theta-lovat.vercel.app](https://ecommercefrontend-theta-lovat.vercel.app/)

---

### [Scalable Notification System](https://github.com/jassisamuran/notification_backend)
> Event-driven Email/SMS/OTP delivery system.

- Kafka producer/consumer groups routing to dedicated worker pipelines
- Redis priority queues with exponential backoff and dead-letter queues
- Full lifecycle tracking: queued → processing → sent → retry → dead-letter in MongoDB

`Kafka` `Redis` `Node.js` `MongoDB`

---

## 🛠️ Tech Stack

```
AI/LLM      AutoGen · RAG · ChromaDB · sentence-transformers · GPT-4o · Claude
Backend     FastAPI · Django · Node.js · Celery · WebSockets · Redis · JWT
Databases   PostgreSQL · MongoDB · MySQL · ChromaDB
Frontend    React · Next.js · TypeScript · TailwindCSS
DevOps      Docker · Docker Compose · AWS EC2 · Nginx · GitHub Actions
Languages   Python · JavaScript · TypeScript · C++
```



## 📫 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-jaspreet--singh-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/jaspreet-singh-7315ba220/)
[![Email](https://img.shields.io/badge/Email-samuran3132@gmail.com-D14836?style=flat&logo=gmail)](mailto:samuran3132@gmail.com)

---

*Open to AI Engineer, Backend Engineer, and Full Stack roles.*
