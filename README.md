# Local Issues Management System

A structured template system for managing project issues locally. This system provides a clear, file-based approach to track user stories, features, bugs, and tests.

English | [简体中文](README_zh.md)

## Table of Contents
- [Features](#features)
- [Directory Structure](#directory-structure)
- [Issue Types](#issue-types)
- [Issue States](#issue-states)
- [File Naming Convention](#file-naming-convention)
- [Templates](#templates)
- [Getting Started](#getting-started)
- [How to Use](#how-to-use)
- [Example](#example)
- [Best Practices](#best-practices)
- [Editor Integration](#editor-integration)
- [FAQ](#faq)
- [Contributing](#contributing)
- [License](#license)

## Features

- 📁 Structured directory organization by milestones
- 📝 Standardized templates for stories and issues
- ✅ Clear task state tracking
- 🔗 Built-in dependency management
- 📊 Progress tracking through status history

## Directory Structure

```
.issues/
├── templates/
│   ├── story.md
│   └── issue.md
├── m001-project-milestone/
│   ├── 001-story-feature-description.md
│   ├── 002-feat-implementation.md
│   ├── 003-test-test-suite.md
│   └── 004-fix-bug-fix.md
└── m002-another-milestone/
    └── ...
```

## Issue Types

- `story`: User stories describing complete user value
- `feat`: New feature implementation
- `fix`: Bug fix implementation
- `test`: Test implementation

## Issue States

- `[ ]` Not started
- `[x]` Completed
- `[-]` In progress
- `[*]` Skipped
- `[!]` Abandoned

## File Naming Convention

Files follow the pattern: `{id}-{type}-{description}.md`

- `id`: Globally unique identifier across all issues
- `type`: Issue type (story/feat/fix/test)
- `description`: Brief kebab-case description

## Templates

Two standard templates are provided:

1. Story Template (`templates/story.md`)
   ```markdown
   # Title
   Brief story title

   # Story
   As a [role]
   I want [goal/action]
   So that [benefit/value]

   # Acceptance Criteria
   - [ ] Criteria 1
   - [ ] Criteria 2

   # Sub-Issues
   - [ ] {id} Issue description

   # Dependencies
   - [ ] {id} Dependency description

   # Status History
   - YYYY-MM-DD: Created
   ```

2. Issue Template (`templates/issue.md`)
   ```markdown
   # Title
   Brief issue title

   # Introduction
   Detailed description of the issue

   # Tasks
   - [ ] Task 1
   - [ ] Task 2

   # Dependencies
   - [ ] {id} Dependency description

   # Status History
   - YYYY-MM-DD: Created
   ```

## Getting Started

1. Clone this repository
2. Create an `.issues` directory in your project
3. Copy `local-issues.mdc` to your project cursor rules directory
4. Copy the templates from `issues-template/templates` to `.issues/templates`
5. Review the sample in `issues-template/sample` to understand the structure
6. Start creating your issues following the naming conventions and using the templates

## How to Use

### Creating a New Milestone

1. Create a new directory under `.issues/` with the pattern `m{number}-{description}`
   ```bash
   mkdir .issues/m001-user-authentication
   ```

### Creating Issues

1. **User Story**
   - Copy the story template
   - Assign a unique ID (e.g., 001)
   - Fill in the user story sections
   - List acceptance criteria
   - Add sub-issues that will implement this story
   ```bash
   cp .issues/templates/story.md .issues/m001-user-authentication/001-story-login-system.md
   ```

2. **Feature/Fix/Test Issues**
   - Copy the issue template
   - Assign the next available ID
   - Choose appropriate type (feat/fix/test)
   - List specific tasks
   - Link dependencies to other issues
   ```bash
   cp issues/templates/issue.md issues/m001-user-authentication/002-feat-login-page.md
   ```

### Tracking Progress

1. Update task states using the defined markers:
   ```markdown
   - [x] Completed task
   - [-] Task in progress
   - [ ] Not started task
   - [*] Skipped task
   - [!] Abandoned task
   ```

2. Always update the Status History when changing states:
   ```markdown
   # Status History
   - 2024-01-08: Created
   - 2024-01-09: Started implementation
   - 2024-01-10: Completed basic features
   ```

### Managing Dependencies

1. Reference other issues using their IDs:
   ```markdown
   # Dependencies
   - [ ] 001 Parent user story
   - [ ] 002 Backend API implementation
   ```

2. Check dependencies before marking an issue as complete

### Best Workflow Practices

1. Create the milestone directory first
2. Start with a user story
3. Break down into implementation issues
4. Update status regularly
5. Keep dependencies up to date
6. Review and update task states daily

## Example

Check out the sample implementation in `issues-template/sample/m001-auth-system/` for a complete example of:
- User authentication story
- Login page implementation
- Test suite
- Bug fix task

## Best Practices

1. Always use the provided templates for consistency
2. Maintain unique IDs across all issues
3. Keep the status history updated
4. Document dependencies clearly
5. Use meaningful descriptions in file names
6. Group related issues under appropriate milestones

## Editor Integration

### Cursor
- The `local-issues.mdc` file in your project cursor rules directory enables Cursor to understand the issue management structure
- Use Cursor's markdown preview to view issues
- Utilize Cursor's file navigation to quickly switch between issues
- Use Cursor's search functionality to find related issues
- Cursor will help enforce naming conventions and structure defined in `local-issues.mdc`

### VSCode
- Install a Markdown preview extension
- Use workspace folders to organize milestones
- Use the integrated terminal for creating new issues
- Enable word wrap for better readability

## Project Progress Tracking

You can track project progress in several ways:
1. **Milestone Overview**: Check the completion status of issues within each milestone
2. **Status Counts**: Count issues by their status within a milestone
3. **Dependencies**: Review the dependency graph to identify bottlenecks
4. **History Timeline**: Review status history across issues to understand progress

## FAQ

### Q: How should I handle urgent hotfixes?
A: Create a new fix issue in the current milestone with a high priority note in the introduction section. Link it to the relevant story or feature.

### Q: What if I need to split an issue into multiple issues?
A: Create new issues and update the original issue to reference them in the Sub-Issues section. Update the original tasks to reflect the split.

### Q: Should I delete completed issues?
A: No, keep all issues for historical tracking. Use the status markers to indicate completion.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the Apache License 2.0 - see the LICENSE file for details.

The Apache License 2.0 is a permissive license that allows you to:
- Use the software for any purpose
- Distribute and modify the software
- Patent rights are explicitly granted
- Distribute modified versions under any license of your choice

This license also provides an express grant of patent rights from contributors to users.
