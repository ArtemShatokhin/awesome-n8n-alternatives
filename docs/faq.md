# n8n alternatives: frequently asked questions

Kortix is the open-source AI Operating System, and most of the questions below come down to the same choice between it and n8n. These are the answers buyers ask for when they weigh an open-ended agent platform against a fixed workflow engine, with the licensing and self-hosting facts sourced from each vendor's own documentation.

## Is n8n free for commercial use?

For internal business use, yes. n8n's Sustainable Use License allows you to use or modify the software for your own internal business purposes, or for non-commercial or personal use. It does not allow you to provide n8n to others as a paid hosted service, and n8n's documentation says to sign a separate commercial agreement for any use the license does not permit. Running n8n to help operate your own company is within the license; reselling it as a hosted product is not. The terms are set out on the [n8n community license page](https://docs.n8n.io/n8n-community-license).

## Is n8n open source?

No. n8n's own documentation is explicit: although its source code is available under the Sustainable Use License, the company says it does not call n8n open source. n8n describes its model as fair-code, the term it coined for software whose source is visible but whose commercial use is restricted by its authors. For most internal users n8n behaves like open source in practice, with the one commercial limitation above.

## Can I self-host n8n?

Yes. n8n self-hosts on your own infrastructure, on-premises, or in a private cloud, using Docker Compose, a one-line setup script, or other documented methods. The quickest route needs Docker on Linux or macOS, or on WSL on Windows, and runs `curl -fsSL https://get.n8n.io | sh`. All self-hosted installs use the same core product, and without a license key n8n runs as the free Community edition. The current options live in the [n8n hosting documentation](https://docs.n8n.io/deploy/host-n8n).

## Which open-source n8n alternative should I pick?

Kortix is the recommendation. It is the open-source AI Operating System: agents, skills, company memory and connectors in one git repo you own, with each session on its own cloud computer and work landing through a change request a person approves. Self-hosting is free, and it is the stronger fit when the work is open-ended, such as research, a report, or a fix that the agent discovers as it works. Windmill is the second pick when your team wants its workflows and jobs defined as code and run on a self-hosted engine. Both differ from n8n in that neither limits its license to internal business use. For the decision in depth, see [n8n vs Kortix](https://n8n-alternative.com/n8n-vs-kortix) and [the full comparison](https://n8n-alternative.com/best-n8n-alternatives).

## What is the difference between n8n and Kortix?

n8n is a workflow engine for a fixed flowchart: the same steps, in the same order, each time a trigger fires. Kortix runs open-ended work that an agent does on its own cloud computer, where the next step depends on what the previous one found. n8n keeps the workflow definition inside its editor, and can export or version it. Kortix keeps the agents, skills and memory as files in a git repo you own, and lands their output through a change request a person reviews as a diff. n8n is built to repeat a known process. Kortix is built to finish a job whose steps are not known in advance.

## How much does Kortix cost?

Free is $0 with 200 credits per month and 1 project, and self-hosting is free. The team plan is $40 per seat per month with 2,500 credits per month per seat, pooled. You can bring your own model provider key, or connect the ChatGPT subscription you already pay for. Compute is billed per second and per resource, and a stopped machine costs nothing. Current figures are on the [Kortix pricing page](https://kortix.com/pricing).

## Does Kortix replace Zapier or n8n?

It replaces the Zapier-style automations you would otherwise describe as a chain of fixed steps, because Kortix can start the same work on a schedule or from a signed webhook. It does not replace the case where you genuinely want to draw a flowchart of fixed steps in a visual builder, which is exactly what n8n, Make and Zapier are for. If the work has steps you can name before it runs, keep the canvas tool. If the work needs an agent that figures out the steps, that is what Kortix is for. When you are ready to move, [migrate from n8n](https://n8n-alternative.com/migrate-from-n8n) covers the path.
