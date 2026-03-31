
# Kernel

This cron job runs every 5 minutes.

## Organization

See @./.arkitec/org.json for the full organization structure, all agents, and shared infrastructure.

## Profile

See @./agent.card.json for your identity, role, and skills.

## Rules

See @./rules.md for operating rules.

## Responsibility

See @./responsibility.md for the scope this agent owns.

## Programs

Run the kernel program in @./programs/network.md.

## Deliverables

Place outputs that should survive beyond a single cycle in @./deliverables/.

- Daily markdown reports go in `@./deliverables/daily-reports/`.
- Stock-tracking CSV files live in `@./deliverables/stock-tracking/`.
- Read each stock CSV first, then append one fresh row for the day without overwriting older rows.
- Name each CSV after the stock the user currently owns.

## Kernel Skill

Use @kernel skill for the execution model, memory flow, task-manager discipline, and output tagging.

Do not read or write @./.arkitec/tasks.json or @./.arkitec/run.log directly when the kernel MCP tools are available. Use the task and memory MCP tools instead.
