# Joseph Schady

CS @ Princeton · Backend & Infrastructure

I'm looking for a Summer 2027 software engineer internship in backend, infrastructure, or platform engineering. I'll be a rising junior that summer.

I wrote backend services and AWS infrastructure at Gnosis Freight, a logistics SaaS company, from April to August 2025 and again from May to August 2026. I started there as a high school senior. That code is in private repos, and working on it is what turned up the two Pulumi bugs below. Everything else here I built on my own time.

### Merged upstream

- On a refresh, the Docker Build provider dropped live resources from state on any non-404 registry error, such as an expired ECR token. I filed the issue and wrote the patch. Pulumi merged [pulumi/pulumi-docker-build #930](https://github.com/pulumi/pulumi-docker-build/pull/930) in July 2026.
- In the core engine, replacing a `deletedWith` target left state out of sync with the cloud. The dependent was gone in the cloud, but it had no input diff of its own, so the engine kept its state entry and reported success. My patch replaces the dependent too. Pulumi merged [pulumi/pulumi #23818](https://github.com/pulumi/pulumi/pull/23818) in August 2026.

### Pulumi providers

I maintain two community Pulumi providers in Go, one written from scratch and one bridged from an existing Terraform provider. Both ship generated SDKs to npm, PyPI, and NuGet, and Go users import the module straight from the repository.

- [MailSlurp](https://github.com/jschady/pulumi-mailslurp) is the one I wrote from scratch, on a Go API client I also wrote, with retry, pagination, and error mapping.
- [Files.com](https://github.com/jschady/pulumi-filescom) is bridged from the Files.com Terraform provider, and it covers 60 resource types and 81 functions.

### Other projects

- [autonomous-sre](https://github.com/jschady/autonomous-sre) is a LangGraph agent that triages Prometheus Alertmanager alerts from a Kubernetes cluster. A FastAPI webhook receives each alert, the agent matches it to a runbook with pgvector similarity search, and nothing changes in the cluster until someone approves the action in Slack.
- [Street Swap](https://apps.apple.com/us/app/street-swap-princeton/id6755552977) is an iOS app on the App Store that digitizes party passes at Princeton, with more than 150 downloads.
- [scaffold-cli](https://github.com/jschady/scaffold-cli) bootstraps a Next.js project and provisions the GitHub, Supabase, and Vercel resources it needs. It ships as [@jschady/scaffold-cli](https://www.npmjs.com/package/@jschady/scaffold-cli) on npm.

### Stack

**In my internships:** Go · Python · TypeScript · FastAPI · AWS · Pulumi · Docker · Kafka · Next.js

**Also in side projects:** Kubernetes · LangGraph · PostgreSQL · pgvector · React Native

### Elsewhere

[LinkedIn](https://linkedin.com/in/joseph-schady) · jlschady[at]gmail[dot]com

