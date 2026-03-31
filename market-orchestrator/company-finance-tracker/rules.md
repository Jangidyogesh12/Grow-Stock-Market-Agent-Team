# Rules

- Follow the @kernel skill for the execution loop, memory usage, and output tagging.
- Update the task manager whenever task state changes.
- Use task and memory MCP tools instead of reading or writing   @./.arkitec/tasks.json or @./.arkitec/run.log directly.
- Keep work aligned with @./responsibility.md.
- Use MCP tools when available instead of ad hoc shell workflows.
- Take the list of companies sent by `market-orchestrator` as the primary finance research queue.
- Perform financial research for each assigned company and focus on fundamentals, growth, profitability, leverage, cash flow, valuation, and major financial risks.
- Prioritize companies already held in the portfolio and companies shortlisted by the broker agent.
- Report the financial findings back to `market-orchestrator` in a concise, reusable format for the final daily report.
- Write the finance handoff as `YYYY-MM-DD-finance-handoff.md` in `@./deliverables/`.
- Use this fixed section order in every finance handoff: `# Finance Handoff`, `## Report Date`, `## Companies Reviewed`, `## Company Analysis`, `## Cross-Company Takeaways`, `## Key Notes For Orchestrator`.
- In `## Companies Reviewed`, list the exact companies received from `market-orchestrator`.
- In `## Company Analysis`, give one subsection per company with: business snapshot, growth and profitability, balance-sheet or leverage note, cash-flow note if available, valuation note if available, risks, and finance verdict.
- In `## Cross-Company Takeaways`, highlight the strongest and weakest names from a financial perspective.
- In `## Key Notes For Orchestrator`, include only the most decision-useful finance points for the final report.
- Store drafts, reports, plans, generated artifacts, and final outputs in @./deliverables/.
- Keep outputs concrete, searchable, and easy for future cycles to resume.
