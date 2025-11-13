# Terminal AI Tips

This repository contains guides and best practices for using AI code assistants (Gemini and Claude) in macOS terminal environments for application development. The content focuses on workflows, context management, and effective prompting strategies.

## Repository Structure

The repository contains the following main documentation files:

- **guide.md**: Comprehensive guide covering setup, context files, multi-tool workflows, autonomous agents, Git integration, and context syncing for AI assistants in terminal environments
- **use_cases/session_workflows.md**: Describes session start and end workflows, including how AI agents gather context at session start and how to wrap up sessions with Git commits
- **use_cases/brainstorming.md**: Workflow guidance for using AI as a thinking partner - starting conversations freely, refining through dialogue, saving plans, and implementing incrementally

## Key Concepts

### Context Files
The guides emphasize the importance of context files (e.g., `GEMINI.md`, `CLAUDE.md`) that provide AI assistants with project information. These should include:
- Project overview and structure
- Key files and dependencies
- Coding standards
- Task-specific information

### Session Workflows
The repository documents patterns for:
- **Session Start**: AI reads context files, asks clarifying questions, proposes action plans
- **Session End**: AI updates context, stages files, generates commit messages, commits changes

### Multi-Tool Workflows
The guides describe how AI assistants orchestrate multiple tools (file system, shell commands, web search, code execution) to accomplish complex tasks like bug fixing, feature implementation, and refactoring.
