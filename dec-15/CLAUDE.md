# User-Level Claude Code Instructions

## Subagent Prompt Quality Standards

A good subagent prompt is:
- **Specific**: No ambiguity about what "done" means
- **Complete**: All context needed to start immediately
- **Constrained**: Clear boundaries on what NOT to do
- **Structured**: Uses XML/markdown for scanability
- **Example-driven**: Shows desired patterns when applicable
- **Token-aware**: Guides agent to be concise or thorough as needed

A bad subagent prompt is:
- **Vague**: "Implement the handler"
- **Context-free**: Agent must search blindly for patterns
- **Unconstrained**: Agent makes architectural decisions randomly
- **Wall-of-text**: No structure, hard to parse
- **Missing success criteria**: "Done" is subjective

## Subagent Report Format

Every subagent MUST return a concise, structured report:

```xml
<agent_report>
  <task_id><!-- unique identifier --></task_id>
  <status><!-- complete | partial | blocked | failed --></status>

  <work_completed>
    <!-- Bullet list of what was done -->
  </work_completed>

  <outcomes>
    <what_worked><!-- Successes --></what_worked>
    <what_failed><!-- Failures and why --></what_failed>
  </outcomes>

  <incomplete_tasks>
    <!-- If status != complete, what remains -->
  </incomplete_tasks>

  <challenges>
    <!-- Blockers, edge cases, or decisions needed -->
  </challenges>

  <artifacts>
    <!-- Files created/modified with paths -->
  </artifacts>

  <recommendations>
    <!-- Next steps or follow-up tasks -->
  </recommendations>
</agent_report>
```

## Subagent Handoff Best Practices

### When Spawning a Subagent

1. **Provide full context**: Include relevant file paths, function names, and existing patterns
2. **Define success criteria**: What specific outcome indicates the task is complete?
3. **Set boundaries**: What should the agent NOT touch or change?
4. **Include examples**: Show the desired output format or code pattern when possible

### When Receiving Subagent Results

1. **Verify completeness**: Check the status field first
2. **Review artifacts**: Confirm files were modified as expected
3. **Handle partial completion**: If blocked, address blockers before continuing
4. **Incorporate learnings**: Note what worked/failed for future tasks
