# DocuMind Development Guidelines

## 1. Purpose

This document is to know the development standards and
quality checks for the DocuMind project I am developing as part of the task given to me during my Internship.

## 2. Development Workflow

For each development task:

1. Understand the task and expected outcome.
2. Create or switch to a focused Git branch.
3. Implement the change.
4. Review the changed files.
5. Run the required quality checks.
6. Commit the changes with a meaningful message.
7. Push the branch to the remote repository.
8. Create a Pull Request when appropriate.

## 3. Branching Conventions

Use focused branches for development tasks.

Branch naming patterns:

- feat/<short-description>
- fix/<short-description>
- docs/<short-description>
- chore/<short-description>

Avoid committing development changes directly
to the main branch unless explicitly required.

## 4. Coding Standards

- Prefer TypeScript for application code.
- Use descriptive variable and function names.
- Keep functions focused on a single responsibility.
- Use Prettier for formatting.
- Use ESLint for code quality checks.
- Avoid unnecessary nesting and complex logic.
- Remove unused and dead code.
- Avoid magic numbers and unexplained strings.

## 5. Validation and Error Handling

- Validate external input at application boundaries.
- Use schema validation for request data.
- Handle expected errors explicitly.
- Do not silently swallow errors.
- Return safe and useful error messages.
- Handle rejected asynchronous operations.

## 6. Security Requirements

- Never commit secrets, API keys, or passwords.
- Store secrets in environment variables.
- Do not commit sensitive .env files.
- Validate uploaded files and external input.
- Do not log sensitive information.
- Never expose LLM provider API keys in frontend code.

## 7. Testing Requirements

- Test successful behavior.
- Test obvious failure cases.
- Add regression tests for fixed bugs.
- Keep tests independent and repeatable.
- Do not use production data in tests.
- Run relevant tests before pushing changes.

## 8. Pre-Push Checklist

Before pushing code:

- [ ] Review changed files.
- [ ] Check for secrets and sensitive files.
- [ ] Run the configured formatter.
- [ ] Run linting.
- [ ] Run relevant tests.
- [ ] Check for unintended changes.
- [ ] Confirm the commit message is meaningful.
- [ ] Verify the changes match the task requirements.

## 9. Commit Conventions

- Keep commits focused on one logical change.
- Use clear and descriptive commit messages.
- Review staged changes before committing.

Examples:

- docs: add development guidelines
- feat: initialize frontend application
- fix: handle expired access token
- chore: configure linting