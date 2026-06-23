```markdown
# andrej-karpathy-skills Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches best practices for developing TypeScript projects in the `andrej-karpathy-skills` style. It covers coding conventions, commit patterns, file organization, and testing strategies. The repository emphasizes clean, conventional commits, consistent code style, and modular TypeScript development without reliance on a specific framework.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `myUtility.ts`, `userProfile.test.ts`

### Imports
- Use **relative imports** for referencing local modules.
  - Example:
    ```typescript
    import { myFunction } from './myUtility';
    ```

### Exports
- Use **named exports** rather than default exports.
  - Example:
    ```typescript
    // myUtility.ts
    export function myFunction() { /* ... */ }
    ```

### Commit Messages
- Follow the **Conventional Commits** specification.
- Use prefixes such as `feat` for new features and `refactor` for code restructuring.
- Keep commit messages concise (average 45 characters).
  - Example:
    ```
    feat: add user authentication module
    refactor: simplify data fetching logic
    ```

## Workflows

### Feature Development
**Trigger:** When adding a new feature  
**Command:** `/feature`

1. Create a new TypeScript file using camelCase naming.
2. Implement your feature using named exports.
3. Import any dependencies using relative paths.
4. Write corresponding tests in a `*.test.ts` file.
5. Commit your changes with a `feat:` prefix and a concise message.

### Refactoring
**Trigger:** When improving or restructuring existing code  
**Command:** `/refactor`

1. Identify code to be improved or reorganized.
2. Refactor while maintaining existing functionality.
3. Update imports/exports as needed to keep code modular.
4. Update or add tests if necessary.
5. Commit your changes with a `refactor:` prefix and a concise message.

## Testing Patterns

- Test files follow the `*.test.*` naming pattern (e.g., `myUtility.test.ts`).
- The specific testing framework is not enforced, but tests should be colocated with the code they test.
- Example test file:
  ```typescript
  // myUtility.test.ts
  import { myFunction } from './myUtility';

  describe('myFunction', () => {
    it('should return correct result', () => {
      expect(myFunction()).toBe(/* expected value */);
    });
  });
  ```

## Commands
| Command   | Purpose                                 |
|-----------|-----------------------------------------|
| /feature  | Start a new feature development workflow|
| /refactor | Begin a code refactoring workflow       |
```
