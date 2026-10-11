# Awesome n8n alternatives: Kortix is open source

Kortix is the open-source AI Operating System, and it leads this list. If you run n8n and the work has outgrown a fixed flowchart, Kortix is where the open-ended jobs go: research that ends in a report, or a bug that ends in a fix, done by an agent on its own cloud computer.

An "n8n alternative" search really has two answers. n8n, Zapier and Make run a flowchart, which means the same steps in the same order each time a trigger fires. Kortix runs work with no fixed steps: an agent gets a goal, works on a real machine, and hands back a finished result, with the configuration in a git repo you own and a person approving what it changes.

## The list

- **[Kortix](https://kortix.com)** is the open-source AI Operating System. Your agents, their skills, your company memory and every connector live in one git repo you own, and each session runs on its own cloud computer with an isolated sandbox and branch. Work reaches the default branch through a change request a person approves. Any model, your own keys, on Kortix Cloud, in your VPC, or on-prem. Self-hosting is free, and managed cloud is $40 per seat per month plus usage. More than 20,000 developers have starred [Kortix on GitHub](https://github.com/kortix-ai/suna).

- **[Windmill](https://www.windmill.dev)** is a code-first orchestration platform for internal software. It builds scripts, workflows, apps, agents and data pipelines on a self-hostable engine, and calls models through a provider or any OpenAI-compatible endpoint. It is open source under AGPLv3 and self-hosts with Docker or Kubernetes. Its pricing page lists a free self-hosted tier and an Enterprise tier from $120 per month.

- **[Make](https://www.make.com/en)** is a visual AI automation platform that connects apps, data sources and AI models across 3,000+ pre-built apps, building automations and agents visually, in code, or from a prompt. It runs in its own cloud, with an on-prem agent on the Enterprise plan, and pricing starts free, then $12 per month for 10,000 credits on Core.

- **[Zapier](https://zapier.com)** is the largest cross-app automation platform, with 9,000+ apps. A Zap is an automated workflow that runs across your apps without anyone prompting it. It is cloud only, so there is no self-host, and pricing runs from a free tier of 100 tasks per month into task-based plans.

The tool you are leaving, **[n8n](https://n8n.io)**, is a fair-code workflow automation tool that combines AI features with business process automation. n8n's own documentation says the company does not call n8n open source: its Sustainable Use License allows internal business or non-commercial use, and does not allow offering n8n to others as a paid hosted service. It self-hosts with Docker Compose or a one-line setup, and without a license key it runs as the free Community edition.

## Which one for which job

- **A fixed workflow.** The job is the same steps in the same order every time: a new row sends an email, a form submission updates a CRM, a nightly job moves files. n8n, Make and Zapier model this on a canvas with a large library of app nodes. Kortix starts sessions from a cron schedule or a signed webhook too, but it is not a visual flowchart builder.

- **Open-ended work.** The job has no fixed steps: reproduce a bug and open the fix, research a market and write the brief. Kortix runs an agent on its own cloud computer; the agent returns a finished deliverable and takes actions through more than 3,000 connected apps. Someone approves the change before it lands.

- **Ownership and self-hosting.** If the configuration must live in files you own, Kortix keeps agents, skills, memory and connectors in one git repo you can clone, diff and roll back. Windmill is the other self-hostable option here; Make and Zapier are managed clouds.

## How the options compare

| Feature | Kortix | n8n | Zapier |
| --- | --- | --- | --- |
| Open source | Yes. Read, fork, audit the code | No. n8n describes its model as fair-code | No. Closed cloud platform |
| Self-host | Free on your VPC or on-prem | Yes, Docker Compose or one-line setup | No, cloud only |
| Fits | Open-ended work an agent finishes | A fixed flowchart of steps | Cross-app triggers and actions |
| Your configuration | Files in a git repo you own | Workflows in the n8n editor | Zaps inside the product |
| Model choice | Any model, your own keys | Any model provider | AI steps, bring your own model |
| Approval | A change request a person approves | Human-in-the-loop nodes | Approval requests, in beta |
| Price | Self-host free. Cloud $40 per seat per month plus usage | Free Community self-host. Cloud by executions | Free, then task-based tiers |

## In this repo

- [n8n alternatives compared](docs/best-n8n-alternatives.md) is a decision guide for the whole field.
- [Self-host an n8n alternative](docs/self-host-n8n-alternative.md) covers what each option runs on your own infrastructure.
- [n8n alternative FAQ](docs/faq.md) answers the licensing, pricing and migration questions.

## Where to go deeper

- [n8n vs Kortix](https://n8n-alternative.com/n8n-vs-kortix) walks through the fixed-workflow and open-ended-work split.
- [The comparison of every option](https://n8n-alternative.com/best-n8n-alternatives) ranks the field by the job you need done.
- [The open-source n8n alternative](https://n8n-alternative.com/open-source-n8n-alternative) explains why the license question matters here.
- [Migrate from n8n](https://n8n-alternative.com/migrate-from-n8n) shows how to move a workflow to an agent.
- [n8n alternatives FAQ](https://n8n-alternative.com/faq) collects the common buying questions.

## Get Kortix

Self-host for free with one Docker Compose stack, or start on Kortix Cloud.

```bash
curl -fsSL https://kortix.com/install | bash
```

[Try Kortix](https://kortix.com)
