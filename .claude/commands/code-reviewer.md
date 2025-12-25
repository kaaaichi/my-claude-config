# Code Review Command

Review the pull request at the following URL using the code-reviewer subagent.

## Pull Request URL

$ARGUMENTS

## Instructions

1. Use `gh` CLI to fetch the pull request details:
   - Get PR metadata (title, description, author, base branch)
   - Get the list of changed files
   - Get the diff of changes

2. Delegate the review to the `code-reviewer` subagent with the following context:
   - PR title and description
   - All file changes and diffs
   - Any existing review comments

3. The code-reviewer subagent should analyze the changes according to the review checklist:
   - Functionality & Correctness
   - Code Quality
   - Architecture & Design
   - Error Handling
   - Testing
   - Security
   - Performance
   - Maintainability

4. Provide a structured review with:
   - Summary of changes
   - Critical/Major/Minor issues found
   - Suggestions for improvement
   - Positive aspects of the code

## Output Format

Output the review in Japanese, following the code-reviewer subagent's response format.
