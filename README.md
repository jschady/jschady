# Joseph Schady

CS @ Princeton · Incoming @ Meta

Backend and infrastructure. Two summers at Gnosis Freight, a logistics SaaS company, starting as a high school senior. Production Engineering at Meta next summer.

The Gnosis code is private. Working on it is what turned up the two Pulumi bugs below. Everything else here I built on my own time.

### Merged upstream

* The Docker Build provider dropped live resources from state on any non-404 registry error, like an expired ECR token. Filed it, patched it. Merged as [pulumi/pulumi-docker-build #930](https://github.com/pulumi/pulumi-docker-build/pull/930), July 2026.
* In the core engine, replacing a `deletedWith` target left a dependent that was gone in the cloud but still in state, and the engine reported success. My patch replaces the dependent too. Merged as [pulumi/pulumi #23818](https://github.com/pulumi/pulumi/pull/23818), August 2026.

### Pulumi providers

Two community providers in Go, both shipping generated SDKs to npm, PyPI, and NuGet, plus a Go module.

* [MailSlurp](https://github.com/jschady/pulumi-mailslurp) — written from scratch, on a Go API client I also wrote.
* [Files.com](https://github.com/jschady/pulumi-filescom) — bridged from the Terraform provider. 60 resource types, 81 functions.

### Other projects

* [autonomous-sre](https://github.com/jschady/autonomous-sre) — a LangGraph agent that triages Alertmanager alerts from a Kubernetes cluster. Matches each alert to a runbook with pgvector, then waits for a Slack approval before touching anything.
* [Street Swap](https://apps.apple.com/us/app/street-swap-princeton/id6755552977) — iOS app for party passes at Princeton. On the App Store, 150+ downloads.
* [scaffold-cli](https://github.com/jschady/scaffold-cli) — bootstraps a Next.js project and provisions its GitHub, Supabase, and Vercel resources. On npm as [@jschady/scaffold-cli](https://www.npmjs.com/package/@jschady/scaffold-cli).

### Stack

Work: Go · Python · TypeScript · AWS · Pulumi · Docker · Kafka · FastAPI · Next.js
Side projects: Kubernetes · LangGraph · PostgreSQL · pgvector · React Native

### Elsewhere

[LinkedIn](https://linkedin.com/in/joseph-schady) · jlschady[at]gmail[dot]com

