```markdown
# voltagent Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `voltagent` TypeScript codebase. You'll learn how to structure files, write imports/exports, follow commit message standards, and organize tests. This guide also provides suggested commands for common workflows.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `myModule.ts`, `userProfile.test.ts`

### Import Style
- Use **relative imports** for referencing other files.
  - Example:
    ```typescript
    import { myFunction } from './utils';
    ```

### Export Style
- Use **named exports**.
  - Example:
    ```typescript
    // In myModule.ts
    export function myFunction() { ... }
    export const MY_CONST = 42;

    // In another file
    import { myFunction, MY_CONST } from './myModule';
    ```

### Commit Messages
- Follow **Conventional Commits**.
- Use prefixes such as `chore`.
- Keep messages concise (average ~76 characters).
  - Example:
    ```
    chore: update dependencies to latest versions
    ```

## Workflows

### Commit Changes
**Trigger:** When committing code changes  
**Command:** `/commit-changes`

1. Stage your changes:
   ```
   git add .
   ```
2. Write a commit message using the conventional format:
   ```
   git commit -m "chore: describe your change"
   ```
3. Push to your branch:
   ```
   git push
   ```

### Add a New Module
**Trigger:** When creating a new feature or utility  
**Command:** `/add-module`

1. Create a new file using camelCase, e.g., `newFeature.ts`.
2. Use named exports for your functions or constants.
   ```typescript
   // newFeature.ts
   export function newFeature() { ... }
   ```
3. Import it using a relative path where needed.
   ```typescript
   import { newFeature } from './newFeature';
   ```

### Write and Run Tests
**Trigger:** When adding or updating functionality  
**Command:** `/run-tests`

1. Create a test file named with the pattern `*.test.ts`, e.g., `myModule.test.ts`.
2. Write your tests (testing framework is unknown; use standard TypeScript test patterns).
3. Run your test suite (replace with your project's test runner):
   ```
   npm test
   ```

## Testing Patterns

- Test files are named using the pattern `*.test.ts`.
- Place tests alongside or near the modules they test.
- Use the same import/export conventions in test files.
- Example:
  ```typescript
  // myModule.test.ts
  import { myFunction } from './myModule';

  describe('myFunction', () => {
    it('should work as expected', () => {
      // test implementation
    });
  });
  ```

## Commands
| Command         | Purpose                                   |
|-----------------|-------------------------------------------|
| /commit-changes | Guide for making conventional commits     |
| /add-module     | Steps to add a new module or feature      |
| /run-tests      | Instructions for writing and running tests|
```
