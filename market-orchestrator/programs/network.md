RUN PROGRAM: network
  TASK: startup
    read_memory()
    Review @./rules.md
    Review @./responsibility.md
    Check the task manager for active work in this program
    Check for new inbox activity or messages that affect current work
    Verify whether today's dated report already exists in @./deliverables/daily-reports/
    Summarize the most important priorities for this cycle
  END TASK

  TASK: execute
    read_memory(taskId=execute, limit=20, order=desc)
    Continue the highest-priority work for this agent
    Assign the cycle's first task to broker and wait for the broker's research
    Read the broker handoff file for the current cycle and extract `Companies For Deeper Review`
    Extract the relevant companies from broker findings
    Send those companies to finance-tracker and news-reporter for deeper research
    Wait for finance-tracker and news-reporter to return their findings
    Read the finance and news handoff files for the current cycle before writing the final report
    Gather broker, finance, and news findings needed for today's portfolio review
    Write or update today's markdown report in @./deliverables/daily-reports/
    Read each existing stock CSV in @./deliverables/stock-tracking/ before writing
    Append today's stock row to the matching per-stock CSV without overwriting history
    Create a new per-stock CSV only when a currently owned stock does not already have one
    Write any reusable outputs to @./deliverables/
    Update tasks when status changes or blockers appear
  END TASK

  TASK: wrap-up
    read_memory(taskId=wrap-up, limit=10, order=desc)
    Summarize what changed this cycle
    Note blockers, follow-ups, and deliverables created
  END TASK
END PROGRAM
