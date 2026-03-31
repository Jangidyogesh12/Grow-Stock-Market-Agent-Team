RUN PROGRAM: network
  TASK: startup
    read_memory()
    Review @./rules.md
    Review @./responsibility.md
    Check the task manager for active work in this program
    Check for new inbox activity or messages that affect current work
    Summarize the most important priorities for this cycle
  END TASK

  TASK: execute
    read_memory(taskId=execute, limit=20, order=desc)
    Continue the highest-priority work for this agent
    Write any reusable outputs to @./deliverables/
    Update tasks when status changes or blockers appear
  END TASK

  TASK: wrap-up
    read_memory(taskId=wrap-up, limit=10, order=desc)
    Summarize what changed this cycle
    Note blockers, follow-ups, and deliverables created
  END TASK
END PROGRAM
