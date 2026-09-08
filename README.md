<p align="center">
  <img src="./new1.png" width="900" alt="Cheon Youngjo — ocean banner with a circular profile photo">
</p>

<h1 align="center">Hi, I'm Youngjo.</h1>

<p align="center">
  <strong>Backend & Data Systems Engineer</strong><br>
  I follow my curiosity by building things, then making them more reliable.
</p>

<p align="center">
  <a href="https://pknb213.github.io/">Portfolio</a> ·
  <a href="https://pknb213.github.io/#experience">Work experience</a> ·
  <a href="https://www.instagram.com/cheonyj">Instagram</a> ·
  <a href="mailto:pknb213@naver.com">Email</a>
</p>

## About me

I build systems that connect data collection, APIs, background jobs, and search indexes.<br>
Working mainly with Python, Kotlin, and TypeScript, I care about **designs that make data correctness and recovery from failure explicit**.

### What I work on

- **Backend systems** — Separate API and worker responsibilities, with explicit job states, retries, and duplicate handling.
- **Data platforms** — Connect ingestion, batch and stream processing, storage, and operational observability.
- **Retrieval systems** — Keep source data separate from search indexes, and verify rebuilds, incremental updates, and retrieval quality.

## A closer look at my projects

My portfolio documents the architecture and verification evidence I can share publicly from my professional work.

### [cms-rag · Rebuildable search indexes](https://pknb213.github.io/#cms-rag)

I kept the source database as the source of truth and treated the vector store as a derived search index. A replacement index is built and verified before the switch, while change events are applied incrementally.

**23,601 items — matching source and index counts** · **2 vector store adapters** · **58 test functions**

`Python` `FastAPI` `BGE-M3` `pgvector` `Qdrant`

### [cms-api · Background jobs and data consistency](https://pknb213.github.io/#cms-api)

The API records a job and returns its ID; the worker owns execution and state transitions. I separated user-facing job states from internal index-update events to give each a clear failure and retry boundary.

**14 API routes** · **9 database migrations** · **19 test functions**

`Python` `FastAPI` `SQS` `SQLAlchemy` `Alembic`

> Figures reflect July 2026 code snapshots and development-environment checks. Test function counts are not pass rates or coverage figures; item counts are not production traffic metrics. [Evidence and measurement scope](https://pknb213.github.io/#evidence)

## Learning by building

These public repositories are personal learning and experimentation projects, separate from my professional work. Here is one representative repository for each main server language.

- **[Python-Projects](https://github.com/pknb213/Python-Projects)** — REST APIs, batch scheduling, caching, and crawlers
  - Flask · APScheduler · Redis · SQLAlchemy
- **[Kotlin-SpringBoot-Servers](https://github.com/pknb213/Kotlin-SpringBoot-Servers)** — Async APIs, authentication, and reactive data access
  - Spring WebFlux · Coroutines · R2DBC · Kafka
- **[TypeScript-Servers](https://github.com/pknb213/TypeScript-Servers)** — REST, GraphQL, and WebSocket servers, authentication, and messaging
  - NestJS · TypeORM · Redis · Kafka

**AI learning notes** — [LangChain-Challenge](https://github.com/pknb213/LangChain-Challenge): Nomad Coder coursework exploring document retrieval, memory, tool calling, and Streamlit apps.

[Explore more public projects and what they implement](https://pknb213.github.io/#open-source)

## How I approach my work

- Distinguish source data from derived data, and leave a way to rebuild the latter.
- Treat failures, retries, and state transitions as part of the system, not just the happy path.
- Explain what I built, how I measured it, and what the evidence supports—not just the technology list.

---

Thanks for stopping by. If there is something you would like to build together, I'd love to hear about it.<br>
I'm open to opportunities and conversations around backend engineering, data platforms, and retrieval systems.<br>
[pknb213@naver.com](mailto:pknb213@naver.com) · [Engineering portfolio](https://pknb213.github.io/)
