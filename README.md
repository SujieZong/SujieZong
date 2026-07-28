# Hi, I'm Sujie Zong

**AI + full-stack engineer**. I build end-to-end
products: an LLM/agent brain, a real backend and UI around it, and the cloud
infrastructure to ship and run it. I care about systems that stay correct under
load and AI that behaves honestly instead of guessing.

**Open to AI/ML, full-stack, and backend engineering roles.**

`Python` · `Go` · `JavaScript/Node` · `React` · `SQL` · `LangGraph` · `AWS` · `Terraform` · `Docker`

- **AI**: agentic RAG, tool-use agents, grounded and cited generation, embeddings / pgvector, PEFT
- **Full-stack**: React frontends, Node/Express and Go services, event-driven backends, CQRS, idempotency
- **Ops**: AWS (ECS, RDS, SQS/SNS, ElastiCache), Terraform, Docker, CI/CD, load and chaos testing

---

## Featured projects

### [LocalLens](https://github.com/SujieZong/LocalLens) — agentic-RAG city assistant · Python, LangGraph · [live demo](https://sujiez-locallens.hf.space)
- Killed confident-wrong legal answers by routing each query across 3 source lanes (legal docs, live APIs, web) and refusing honestly when nothing grounds it.
- Added a bounded self-correction loop (grader retry ≤2, best-of) with per-claim citations traced to source in SQLite; ≥93% core coverage in CI.
- Ran at $0 with a live demo, using local bge-small embeddings (Chroma) and a Groq→Gemini→Ollama fallback chain.

### [ticketstorm-platform](https://github.com/SujieZong/ticketstorm-platform) — distributed ticketing platform · Go, Node, React, AWS
- Hit 78.6% vs 19.5% seat-acquisition success in a 1,000-buyer flash sale by fronting an atomic Redis hold with a virtual waiting room instead of a contended Postgres row lock.
- Held zero oversell under contention and across a forced Redis failover; drained a 78-message backlog after a consumer outage with no lost events (CQRS, read lag p50 71 ms).
- Shipped a 6-service Go/Node/React stack to AWS via Terraform (ECS, RDS, ElastiCache, SQS/SNS) with CPU autoscaling (1→2); added a Gemini tool-use concierge and pgvector search.

### [silero-vad-dysarthric-adapter](https://github.com/SujieZong/silero-vad-dysarthric-adapter) — parameter-efficient speech-model adaptation · Python, PyTorch
- Lifted dysarthric-speech VAD F1 from 0.43 to 0.80 and cut false-rejection from 0.71 to 0.24 (leave-one-speaker-out, TORGO).
- Trained a 193-parameter adapter head on a frozen 20M-hour Silero encoder (<400 trainable params, ~32 KB checkpoints) instead of retraining.
- Guaranteed zero train/eval leakage via replayed pre-computed probabilities, manual labels held out for test, per-microphone heads across 8 LOSO checkpoints.

---

## Reach me
sjzong1016@outlook.com · [LinkedIn](https://www.linkedin.com/in/sujie-zong-58321514b) · [github.com/SujieZong](https://github.com/SujieZong)
