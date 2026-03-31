# StockMarket
`StockMarket` is a Groww-specific multi-agent stock analysis and portfolio research workspace.
It is designed to orchestrate a set of specialized agents that work together to analyze your portfolio, discover realistic stock opportunities, track company fundamentals, monitor relevant news, and generate daily research outputs.
## What It Does
This repo uses a central `market-orchestrator` agent to coordinate multiple supporting agents, including:
- `broker` - tracks Groww holdings, account balance, and potential stock opportunities
- `company-finance-tracker` - analyzes financial health, trends, and red flags for portfolio and shortlisted companies
- `news-reporter` - tracks relevant company and market news, catalysts, and sentiment changes
The orchestrator collects these handoffs and produces:
- dated daily markdown market reports
- company-wise research summaries
- per-stock CSV tracking files for currently held investments
## Workflow
The system follows a structured research flow:
1. The `broker` agent reviews current Groww holdings and identifies realistic new opportunities.
2. Shortlisted companies are passed to the finance and news agents.
3. The `company-finance-tracker` analyzes fundamentals and financial trends.
4. The `news-reporter` gathers current news, risks, and catalysts.
5. The `market-orchestrator` combines all findings into a final daily report and updates stock tracking files.
## Requirements
To use this repo, you must provide your own credentials:
- Groww API bearer token
- `SerpAPI` API key
These are required for fetching portfolio/account data and retrieving market/news information.
## Output Structure
The repo stores reusable outputs and agent handoffs in deliverable folders, including:
- daily reports in `market-orchestrator/deliverables/daily-reports/`
- stock tracking CSVs in `market-orchestrator/deliverables/stock-tracking/`
- agent-specific handoff files inside each agent's `deliverables/` directory
## Purpose
This project is meant to act as an orchestrated stock research system for Groww users, combining portfolio tracking, financial analysis, and news monitoring into a repeatable daily workflow.