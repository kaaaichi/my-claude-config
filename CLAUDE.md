# Claude AI Configuration

This file contains configuration and instructions for Claude AI when working on projects.

## Common Commands

Document frequently used commands for this project:

```bash
# Example: npm run build - Build the project
# Example: npm test - Run all tests
# Example: npm run typecheck - Run type checker
```

> **Note**: Update this section with project-specific commands when starting a new project.

## Core Files & Utilities

Document important files and utility functions:

- Key configuration files
- Core utility functions and their locations
- Important constants and shared resources

> **Note**: Update this section to reflect the specific project structure.

## Reference Books & Standards

This project adheres to industry-standard best practices as defined in the following authoritative books:

### Test-Driven Development

- **Kent Beck's "Test Driven Development: By Example"**: Follow the TDD methodology exactly as described in this book
  - Red-Green-Refactor cycle
  - Small, incremental steps
  - Write the test first, then make it pass

### Clean Code

- **Robert C. Martin's "Clean Code"**: Write code according to Uncle Bob's principles
  - Meaningful names
  - Small functions with single responsibility
  - DRY (Don't Repeat Yourself)
  - Clear intent and readability over cleverness

### Refactoring

- **Martin Fowler's "Refactoring"**: Define and perform refactoring as described in this book
  - Refactoring is a disciplined technique for restructuring code
  - Changes internal structure without changing external behavior
  - Performed through small behavior-preserving transformations
  - Each transformation is followed by running tests

### Tidying Code

- **Kent Beck's "Tidy First?"**: Apply tidying practices before making behavioral changes
  - Separate structure changes from behavior changes
  - Make small tidying commits before feature work
  - Keep tidying and feature work in separate commits
  - Use tidying to make the next change easier

## General Guidelines

- Write clean, maintainable, and well-documented code
- Follow established coding standards and best practices
- Prioritize code readability and clarity
- Write comprehensive tests for new features
- Consider edge cases and error handling

## Code Style Preferences

- Use meaningful variable and function names
- Keep functions small and focused on a single responsibility
- Add comments for complex logic
- Follow language-specific conventions

## Communication Style

- Be concise and clear in explanations
- Provide code examples when helpful
- Explain the reasoning behind technical decisions
- Ask clarifying questions when requirements are ambiguous

## Implementation Guidelines

- **Never suppress exceptions**: Handle errors appropriately and propagate them to upper layers when necessary
- **Follow TDD approach**: Practice test-first development by writing tests before implementation
- **Adhere to PR templates**: Create pull requests according to the project's pull request template
- **Update local main branch before starting tasks**: When working on git-managed source code, always update the local main branch to the latest version before starting development tasks
- **Use git worktree for feature development**: When working on git-managed code, always use `git worktree` to create a separate working directory for each feature branch. This keeps the main working directory clean and allows parallel development on multiple features
  - Create a new worktree: `git worktree add ../feature-branch-name feature-branch-name`
  - List worktrees: `git worktree list`
  - Remove worktree when done: `git worktree remove ../feature-branch-name`

## Project Workflow

Follow the **Explore-Plan-Code-Commit** workflow:

1. **Explore**: Read and understand relevant files before writing code
   - Review existing codebase structure and patterns
   - Identify core files and utility functions
   - Understand the problem context thoroughly
   - Ask clarifying questions when requirements are ambiguous

2. **Plan**: Think through the solution before implementation
   - Use plan mode for deeper problem analysis
   - Create a clear implementation plan
   - Consider architecture and design implications
   - Verify the approach is reasonable

3. **Code**: Implement with quality and testing in mind
   - Write tests first (TDD approach)
   - Write clean, well-documented code
   - Follow established patterns and conventions
   - Verify tests pass and solution works

4. **Commit**: Document changes clearly
   - Review and refactor as needed
   - Commit with clear, descriptive messages
   - Document significant decisions
   - Course-correct early if issues arise

## Testing

Follow Test-Driven Development (TDD) practices:

1. **Write tests first** before implementing functionality
2. **Confirm tests fail** initially (red phase)
3. **Implement code** to make tests pass (green phase)
4. **Refactor** while keeping tests passing
5. **Verify coverage** is sufficient for the changes

Additional testing guidelines:

- Write comprehensive unit tests for new functionality
- Ensure all existing tests pass before committing
- Consider integration and edge case testing
- Test both positive and negative scenarios
- Run the full test suite after significant changes

## Development Environment

Document any important setup or environmental considerations:

- Required tools and versions
- Environment variables or configuration files
- Known issues or unexpected behaviors
- Warnings to be aware of during development
- Local development setup instructions

> **Note**: Update this section with project-specific environment details.

## Documentation

- Update README files when adding new features
- Document API changes and breaking changes
- Include usage examples in documentation
- Keep CLAUDE.md updated with project-specific information
- Document unexpected behaviors or warnings that may occur

## Code Review Guidelines

When reviewing pull requests, evaluate the following aspects:

### 1. Functionality & Correctness

- Does the code meet the stated requirements?
- Is the logic implemented correctly?
- Are edge cases and boundary conditions handled?

### 2. Code Quality

- Is the code readable and well-structured?
- Are variable and function names meaningful and clear?
- Is there any code duplication that should be refactored?
- Is the abstraction level appropriate?

### 3. Architecture & Design

- Does the code architecture align with the overall system design?
- Is the code structure consistent with existing patterns in the codebase?
- Are design patterns used appropriately?
- Does the solution fit well within the existing module structure?

### 4. Error Handling

- Are exceptions handled appropriately?
- Are error messages clear and actionable?
- Are resources properly cleaned up in all scenarios?

### 5. Testing

- Is test coverage sufficient for the changes?
- Are test cases comprehensive and meaningful?
- Do all existing tests pass?
- Are both positive and negative scenarios tested?

### 6. Security

- Are there any potential security vulnerabilities?
- Is input validation implemented properly?
- Are sensitive data and credentials handled securely?
- Are authentication and authorization correctly implemented?

### 7. Performance

- Are there any unnecessary computations or operations?
- Is resource usage (memory, CPU, network) appropriate?
- Are there potential scalability issues?
- Are database queries optimized?

### 8. Maintainability

- Is the code well-documented with appropriate comments?
- Is the impact of changes clearly understood?
- Does the code support future extensibility?
- Are dependencies managed appropriately?

### 9. Project-Specific Considerations

- Review and adhere to any project-specific documentation in relevant directories (e.g., README.md, CONTRIBUTING.md, docs/)
- Check for project-specific coding standards, architectural decisions, or conventions documented in the repository
- Ensure compliance with any module-level or component-level guidelines

## Best Practices

- **Be specific** in instructions and requirements
- **Course-correct early** when issues are identified
- **Keep context focused** by clearing when switching to new tasks
- **Verify solutions** before considering tasks complete
- **Document decisions** for future reference

---

Last updated: 2025-11-19
