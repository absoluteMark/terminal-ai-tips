# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a documentation repository containing guides and best practices for using AI code assistants (Gemini and Claude) in macOS terminal environments for application development. The content focuses on workflows, context management, and effective prompting strategies.

## Repository Structure

The repository contains three main documentation files:

- **gemini_claude_macos_terminal_guide.md**: Comprehensive guide covering setup, context files, multi-tool workflows, autonomous agents, Git integration, and context syncing for AI assistants in terminal environments
- **session_workflows.md**: Describes session start and end workflows, including how AI agents gather context at session start and how to wrap up sessions with Git commits
- **brainstorming.md**: Workflow guidance for using AI as a thinking partner - starting conversations freely, refining through dialogue, saving plans, and implementing incrementally

## Key Concepts

### Context Files
The guides emphasize the importance of context files (e.g., `gemini.md`, `claude.md`) that provide AI assistants with project information. These should include:
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

## Content Editing Guidelines

When editing documentation in this repository:
- Maintain the instructional, guide-like tone
- Keep practical examples that demonstrate concepts
- Preserve the macOS terminal focus
- Ensure consistency across the three documents when discussing overlapping concepts
- Use clear markdown formatting with appropriate headings and code blocks
