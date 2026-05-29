```markdown
# psychic-invention Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `psychic-invention` TypeScript codebase. It covers file and code organization, import/export styles, commit habits, and testing patterns. While no specific framework or automated workflows were detected, this guide provides best practices and command suggestions to streamline development.

## Coding Conventions

### File Naming
- **PascalCase** is used for file names.
  - Example: `MyComponent.ts`, `UserService.ts`

### Import Style
- **Relative imports** are preferred.
  - Example:
    ```typescript
    import { UserService } from './UserService';
    ```

### Export Style
- **Named exports** are used instead of default exports.
  - Example:
    ```typescript
    // In UserService.ts
    export function getUser(id: string) { ... }

    // In another file
    import { getUser } from './UserService';
    ```

### Commit Patterns
- Commit messages are **freeform** (no enforced structure).
- Sometimes use prefixes, but not consistently.
- Average commit message length is short (about 9 characters).

## Workflows

_No automated workflows detected in the repository._

## Testing Patterns

- **Test files** follow the `*.test.*` naming pattern.
  - Example: `UserService.test.ts`
- **Testing framework is unknown** (not detected), but tests are separated by naming convention.
- To run tests, use your preferred TypeScript test runner (e.g., Jest, Mocha) configured to recognize `*.test.ts` files.

  ```typescript
  // UserService.test.ts
  import { getUser } from './UserService';

  test('should fetch user by id', () => {
    expect(getUser('123')).toEqual({ id: '123', name: 'Alice' });
  });
  ```

## Commands

| Command         | Purpose                                      |
|-----------------|----------------------------------------------|
| /create-file    | Scaffold a new PascalCase TypeScript file    |
| /add-test       | Create a new test file with *.test.ts pattern|
| /list-imports   | List all relative imports in a file          |
| /list-exports   | List all named exports in a file             |
| /run-tests      | Run all test files matching *.test.ts        |
```