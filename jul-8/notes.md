# Development Tools

## Primary Tools
- **Claude Code CLI** - Main code editing and generation tool
- **Zed.dev** - Primary code editor

## MCP
- **Supabase MCP** - Database and backend services integration
- **GitHub MCP** - Repository management and version control

# Workflow Principles

## 1. Parallel-First Thinking

### Identifying Parallelizable Tasks
- **Independent operations**: File reads, API calls, and searches that don't depend on each other
- **Multi-file edits**: Changes across different files that don't conflict
- **Information gathering**: Research tasks, documentation lookups, and context collection

## 2. Context-Gathering Checklist

Before any implementation:
- [ ] Search for existing patterns in the codebase
- [ ] Identify all files that will be affected
- [ ] Check for dependencies and imports
- [ ] Review adjacent code for conventions
- [ ] Gather architectural decisions from docs/comments
- [ ] Understand data flow through the system

## 3. Speed Optimization Guide

### Snippet Shortcuts
- `/par` → continue, execute subtasks in parallel if possible
- `/review` → can you code review this and check for breaking bugs or crucial breaking points?
- `/improve` → give me two suggested solutions how we can improve this
- `/clarify` → Ask any clarifying questions before proceeding

### Speech-to-Text Dictionary
Common technical terms to add:
- "supabase" (not "super base")
- "zed" (not "said")
