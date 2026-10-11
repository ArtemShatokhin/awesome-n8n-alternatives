# Self-hosting an n8n alternative

Kortix is the open-source AI Operating System, and it self-hosts for free, which makes it the natural first stop if running an n8n alternative on your own infrastructure is the goal. This guide covers what self-hosting actually buys you, then the exact install path for each option that supports it, and the ones that do not.

## What self-hosting actually buys you

Self-hosting decides who holds the configuration, the working data and the ability to change the runtime. A tool you host on your own network keeps those inside your perimeter. A managed cloud keeps them inside the vendor's, which is fine until a security review, a data-residency rule or a procurement policy asks harder questions.

For agent platforms there is a second layer. An agent platform's configuration is the agents, their skills, the memory they accumulate and the connectors they may reach. Kortix keeps all of that as files in one git repo you own, so the whole system is something you can clone, diff, audit and roll back. That property survives self-hosting, so a self-hosted Kortix is a system you can still inspect and change.

## Kortix

Kortix installs from a single command, then brings up its own stack.

```bash
curl -fsSL https://kortix.com/install | bash
kortix self-host start
```

`kortix self-host start` runs one Docker Compose stack on your own machine. The first run asks six questions and no model key, GitHub connects later in the dashboard, and models are bring-your-own-key in the app. The stack has no Redis and no separate worker process. Self-hosting is free, and the same project can also run in your VPC or on your own on-prem network, or on Kortix Cloud, without changing the configuration. The install command and the self-host start command are documented in the [Kortix on GitHub](https://github.com/kortix-ai/suna) README, and the project structure is described in the [Kortix docs](https://kortix.com/docs).

## n8n

n8n is the tool this guide is named for, and its self-host path is mature. The quickest route needs Docker on Linux or macOS, or on WSL on Windows:

```bash
curl -fsSL https://get.n8n.io | sh
```

For a production deployment, n8n documents Docker Compose, Google Cloud Run, npm, and a manual Docker run, among other methods. All self-hosted n8n installations use the same core product, and without a license key n8n runs as the free Community edition. On its site n8n describes the option to deploy on-premises in a private cloud. Consult the [n8n hosting documentation](https://docs.n8n.io/deploy/host-n8n) for the current options, and read the [community license page](https://docs.n8n.io/n8n-community-license) to understand what the Sustainable Use License allows before you plan around it.

## Windmill

Windmill is the other fully self-hostable option in this comparison, and it is open source under AGPLv3. The fast path is three files and one command:

```bash
curl https://raw.githubusercontent.com/windmill-labs/windmill/main/docker-compose.yml -o docker-compose.yml
curl https://raw.githubusercontent.com/windmill-labs/windmill/main/Caddyfile -o Caddyfile
curl https://raw.githubusercontent.com/windmill-labs/windmill/main/.env -o .env
docker compose up -d
```

Windmill also ships a Helm chart for Kubernetes and runs on the major clouds, and its own pricing page lists a free self-hosted tier and a paid Enterprise tier. Reach for Windmill when your team already thinks in code and wants its workflows, scripts and jobs defined that way. The commands and the deployment options come from the [Windmill repository](https://github.com/windmill-labs/windmill) and the [Windmill pricing page](https://www.windmill.dev/pricing).

## Make and Zapier

Neither Make nor Zapier is self-hostable. Both run in the vendor's cloud. Make offers what it calls an on-prem agent on the Enterprise plan, which lets a scenario reach systems on a local network, but the automation engine itself still runs in Make's cloud on AWS. Zapier is hosted only and publishes no self-host option. If owning the runtime is a requirement, these two drop out on that criterion alone, whatever else they do well.

## How the options compare on self-hosting

| Tool | Self-host | Method |
| --- | --- | --- |
| Kortix | Yes, free | Install the CLI, then `kortix self-host start`, one Docker Compose stack |
| n8n | Yes, Community edition | One-line setup, or Docker Compose and other documented methods |
| Windmill | Yes, free tier | Three files with Docker Compose, or Helm on Kubernetes |
| Make | No | On-prem agent on the Enterprise plan, engine still in Make's cloud |
| Zapier | No | Cloud only |

## Next steps

If self-hosting is settled and the open-source question is not, [the open-source n8n alternative](https://n8n-alternative.com/open-source-n8n-alternative) explains the licensing difference in plain terms. When you are ready to move a workflow, [migrate from n8n](https://n8n-alternative.com/migrate-from-n8n) lays out the steps. Common questions about pricing and support are collected in the [n8n alternatives FAQ](https://n8n-alternative.com/faq).
