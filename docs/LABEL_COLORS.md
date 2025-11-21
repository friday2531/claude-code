# Label Organization Guide

This document provides a comprehensive overview of all labels used in the claude-code repository, their purposes, and usage guidelines.

## Label Categories

| Label Name | Category | Description |
|------------|----------|-------------|
| bug | issue-type | Indicates something isn't working as expected or there's an error in the codebase |
| enhancement | issue-type | Suggests a new feature or improvement to existing functionality |
| documentation | issue-type | Related to improvements or additions to documentation |
| question | issue-type | Indicates a request for information or clarification |
| duplicate | status | Marks an issue or pull request that already exists elsewhere |
| has repro | status | Indicates the issue has reproducible steps provided |
| external | status | Issue is caused by external dependencies or third-party code |
| platform:macos | platform | Specific to macOS operating system |
| platform:linux | platform | Specific to Linux operating system |
| platform:windows | platform | Specific to Windows operating system |
| area:core | area | Related to core functionality and primary features |
| area:tools | area | Related to development tools and utilities |
| area:api | area | Related to API implementation and interfaces |
| area:security | area | Related to security features, authentication, or vulnerabilities |
| area:tui | area | Related to Terminal User Interface |
| area:mcp | area | Related to Model Context Protocol implementation |
| area:ide | area | Related to IDE integrations and plugins |
| area:packaging | area | Related to package distribution and installation |
| area:auth | area | Related to authentication and authorization |
| area:model | area | Related to AI model behavior and interactions |
| memory | performance | Related to memory management issues |
| perf:memory | performance | Specifically indicates memory performance problems |

## Usage Guidelines

### Issue Type Labels

**When to use:**
- Apply exactly ONE issue type label to each issue
- These labels help quickly identify the nature of the issue
- `bug`: Use for any malfunction, error, or unexpected behavior
- `enhancement`: Use for feature requests or improvements
- `documentation`: Use when the issue is about docs (READMEs, guides, API docs)
- `question`: Use for support requests or clarification needs

### Platform Labels

**When to use:**
- Apply when an issue is specific to a particular operating system
- Multiple platform labels can be applied if the issue affects multiple platforms
- If the issue is platform-agnostic, no platform label is needed
- These labels are crucial for platform-specific bug triage

**Examples:**
- Memory issue only on macOS → `platform:macos`
- Installation problem on both Windows and Linux → `platform:windows` + `platform:linux`

### Area Labels

**When to use:**
- Apply to indicate which component or subsystem is affected
- Multiple area labels can be used if the issue spans multiple components
- These labels help route issues to the appropriate maintainers
- Use the most specific area label available

**Key areas:**
- `area:core`: Fundamental functionality, main execution flow
- `area:tools`: Development utilities, CLI tools, build systems
- `area:api`: REST APIs, external interfaces
- `area:tui`: Terminal interface, rendering, input handling
- `area:mcp`: Model Context Protocol features
- `area:ide`: VS Code, JetBrains, or other IDE integrations
- `area:security`: Authentication, permissions, vulnerabilities
- `area:auth`: Specifically authentication mechanisms
- `area:packaging`: Installation, distribution, dependency management
- `area:model`: AI model behavior, prompts, responses

### Status Labels

**When to use:**
- `has repro`: Add when the issue includes clear reproduction steps or test cases
- `duplicate`: Mark when the issue is a duplicate of another (reference the original)
- `external`: Use when the root cause is in a dependency or external system

### Performance Labels

**When to use:**
- Apply when the issue relates to performance degradation
- `memory`: General memory-related issues (leaks, high usage)
- `perf:memory`: Specific memory performance problems (slowdowns due to memory)

## Best Practices

1. **Be Specific**: Use the most specific labels that apply
2. **Multiple Labels**: It's acceptable (and encouraged) to use multiple labels from different categories
3. **Consistency**: Always check existing labels before creating new ones
4. **Update Labels**: Update labels as issues evolve (e.g., add `has repro` when reproduction steps are added)
5. **Label on Creation**: Try to label issues immediately upon creation for better organization

## Examples

### Example 1: Platform-Specific Bug
```
Title: "Clipboard paste fails on macOS Terminal"
Labels: bug, platform:macos, area:tui
```

### Example 2: Cross-Platform Performance Issue
```
Title: "Memory leak during long sessions"
Labels: bug, has repro, memory, perf:memory, area:core
```

### Example 3: Documentation Enhancement
```
Title: "Add API usage examples to README"
Labels: enhancement, documentation, area:api
```

### Example 4: IDE Integration Question
```
Title: "How to configure VS Code extension?"
Labels: question, area:ide
```

## Maintaining This Guide

When adding new labels to the repository:
1. Add them to the appropriate category table above
2. Provide a clear description
3. Update the usage guidelines if needed
4. Keep labels organized by category for easy reference
