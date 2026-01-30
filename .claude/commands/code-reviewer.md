# Code Review Command (Skill)

Review the pull request at the following URL using the code-reviewer subagent and CLAUDE.md Code Review Guidelines.

## Pull Request URL

$ARGUMENTS

## Review Guidelines (from CLAUDE.md)

This skill applies the comprehensive code review guidelines defined in CLAUDE.md (lines 161-224).

## Instructions

1. Use `gh` CLI to fetch the pull request details:
   - Get PR metadata (title, description, author, base branch)
   - Get the list of changed files
   - Get the diff of changes

2. Apply CLAUDE.md Code Review Guidelines - evaluate the following aspects:

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
   - Is the code structure consistent with existing patterns?
   - Are design patterns used appropriately?
   - Does the solution fit within the existing module structure?

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

   - Review project-specific documentation (README.md, CONTRIBUTING.md, etc.)
   - Check for project-specific coding standards and conventions
   - Ensure compliance with module-level or component-level guidelines

3. Delegate the review to the `code-reviewer` subagent with context:
   - PR title and description
   - All file changes and diffs
   - Any existing review comments
   - Reference to CLAUDE.md guidelines

4. Provide a structured review including:
   - Summary of changes
   - Critical/Major/Minor issues found (based on CLAUDE.md guidelines)
   - Suggestions for improvement
   - Positive aspects of the code

## Output Format

Output the review in Japanese, following CLAUDE.md Code Review Guidelines and code-reviewer subagent's response format.
