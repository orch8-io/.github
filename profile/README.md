<div align="center">

# orch8.io

### Durable Workflow Engine

**Single binary. One dependency: PostgreSQL. Built in Rust.**

Define workflows as composable JSON sequences. Every step completes, retries, or surfaces in a dead-letter queue.<br>No lost work. No silent failures. No JVM. No Redis. No Kafka.

[Website](https://orch8.io) &nbsp;&bull;&nbsp; [Docs](https://orch8.io/docs) &nbsp;&bull;&nbsp; [API](https://orch8.io/docs/api) &nbsp;&bull;&nbsp; [Cloud](https://cloud.orch8.io) &nbsp;&bull;&nbsp; [Templates](https://orch8.io/templates)

---

</div>

### &nbsp;&nbsp; Why Orch8

&emsp; **Snapshot-based resume** &mdash; O(1) crash recovery, no history replay, no determinism constraints<br>
&emsp; **10 block types** &mdash; Step &middot; Parallel &middot; Race &middot; Router &middot; TryCatch &middot; Loop &middot; ForEach &middot; SubSequence &middot; ABSplit &middot; CancellationScope<br>
&emsp; **Rate limiting** &mdash; per-resource sliding window, defers instead of rejects<br>
&emsp; **Polyglot workers** &mdash; write handlers in any language via pull-based REST API<br>
&emsp; **200+ integrations** &mdash; native Activepieces connectors, no custom code<br>
&emsp; **1M+ instances per node** &mdash; < 512MB RAM, < 10ms p99 engine overhead<br>

---

### &nbsp;&nbsp; Quick Start

```bash
# Docker (zero config, SQLite default)
docker run -p 8080:8080 ghcr.io/orch8-io/engine:latest

# Or install the binary
curl -fsSL https://raw.githubusercontent.com/orch8-io/engine/main/install.sh | sh
orch8 init && orch8-server
```

---

### &nbsp;&nbsp; Repositories

| | Repo | Stack | What it does |
|---|---|---|---|
| **Core** | [`engine`](https://github.com/orch8-io/engine) | Rust | Scheduler, evaluator, REST + gRPC API, 68 endpoints, 1,100+ tests |
| **SDKs** | [`sdk-node`](https://github.com/orch8-io/sdk-node) | TypeScript | Full client + polling worker, 16 typed interfaces |
| | [`sdk-python`](https://github.com/orch8-io/sdk-python) | Python | Async httpx + Pydantic, 18 models |
| | [`sdk-go`](https://github.com/orch8-io/sdk-go) | Go | Zero deps, context on all methods |
| **Tools** | [`cli`](https://github.com/orch8-io/cli) | Go | Manage sequences, instances, signals from terminal |
| **Deploy** | [`helm-charts`](https://github.com/orch8-io/helm-charts) | Helm 3 | Kubernetes deployment with HA, autoscaling, TLS |

---

### &nbsp;&nbsp; Use Cases

**Outreach & campaigns** &mdash; multi-step email/SMS sequences with per-mailbox rate limits and warmup ramps<br>
**Notification platforms** &mdash; multi-channel fallback (push &rarr; email &rarr; SMS) with timezone-aware send windows<br>
**AI agent pipelines** &mdash; durable execution for tool-calling agents with human-in-the-loop approval<br>
**Fintech & compliance** &mdash; month-long dunning flows with audit trails and SLA enforcement<br>
**Temporal alternative** &mdash; same durability model, no history replay, no determinism constraints, plain functions instead of activity ceremony<br>

---

### &nbsp;&nbsp; Consulting

Need help setting up workflows? We design, build, and deploy production automations on Orch8.

| Package | Price | What you get |
|---|---|---|
| **Workflow Audit** | $500 one-time | Discovery call + sequence designs + architecture recommendation |
| **Implementation** | $2,500 &ndash; $5,000 | End-to-end build: workers, monitoring, deploy, 2 weeks support |
| **Retainer** | $1,500/mo | New workflows, optimization, priority support, monthly review |

[Learn more &rarr;](https://orch8.io/consulting)

---

### &nbsp;&nbsp; License

BUSL-1.1 &mdash; free for internal production use. Converts to Apache 2.0 after 4 years.<br>
Need to embed Orch8 in your SaaS? [Get a commercial license](mailto:hello@orch8.io).

---

<div align="center">

Built by **[Oleksii Vasylenko](https://www.ovasylenko.com)** &nbsp;&bull;&nbsp; [hello@orch8.io](mailto:hello@orch8.io)

</div>
