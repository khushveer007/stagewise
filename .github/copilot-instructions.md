# Development Workflow Instructions

We use Task Master CLI for task-driven development workflow management. Use `task-master` commands instead of custom scripts when discussing task management.

When suggesting task management operations, always reference these commands:
- `task-master list` to view current tasks
- `task-master next` to identify the next task to work on
- `task-master expand --id=<id>` to break down complex tasks
- `task-master set-status --id=<id> --status=done` to mark completed tasks

For code analysis and refactoring, prefer grep pattern matching to identify functions across the codebase using: `grep -E "export (function|const) \w+|function \w+\(|const \w+ = \(|module\.exports" --include="*.js" -r ./`

When generating code or documentation, follow these task structure standards:
- Include task ID, title, description, status, dependencies, priority, details, and test strategy
- Use dependency chains with status indicators (✅ for completed, ⏱️ for pending)
- Reference tasks by numeric IDs and maintain valid dependency structures

For rule documentation, use this structure:
- Start with frontmatter containing description, globs, and alwaysApply fields
- Use bold headers for main points with bullet sub-points
- Include both DO and DON'T examples with ✅ and ❌ markers
- Reference related rules using ALL_CAPS_SECTION format

When suggesting improvements or new patterns, trigger rule updates when:
- New patterns appear in 3+ files
- Common bugs could be prevented
- Code reviews repeatedly mention the same feedback
- Better examples exist in the codebase

Always prioritize actionable, specific guidance over theoretical examples when generating responses.
