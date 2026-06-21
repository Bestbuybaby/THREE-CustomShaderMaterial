```markdown
# THREE-CustomShaderMaterial Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you how to contribute to and maintain the THREE-CustomShaderMaterial TypeScript codebase. You'll learn the project's coding conventions, file organization, and how to work with custom shader materials for THREE.js. The repository is framework-agnostic and focuses on modular, readable TypeScript code with a clear structure for imports, exports, and testing.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `customShaderMaterial.ts`

### Import Style
- Use **relative imports** for internal modules.
  - Example:
    ```typescript
    import { createShader } from './shaderUtils';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    export function createShader() { ... }
    ```

### Commit Messages
- Commit messages are freeform, with no strict prefix or type required.
- Average commit message length is about 64 characters.

## Workflows

### Adding a New Shader Material
**Trigger:** When you want to introduce a new custom shader material.
**Command:** `/add-shader-material`

1. Create a new TypeScript file using camelCase (e.g., `myCustomMaterial.ts`).
2. Implement your shader logic, using named exports.
    ```typescript
    export function myCustomMaterial(params: MaterialParams) { ... }
    ```
3. Import any shared utilities using relative paths.
4. Add or update relevant tests in a corresponding `.test.ts` file.
5. Commit your changes with a clear, descriptive message.

### Running Tests
**Trigger:** When you need to verify code correctness.
**Command:** `/run-tests`

1. Identify test files by the `*.test.*` pattern (e.g., `customShaderMaterial.test.ts`).
2. Use the project's preferred test runner (framework is unspecified; check documentation or scripts).
3. Run all tests and review results.
4. Fix any failing tests before merging changes.

### Refactoring or Renaming Files
**Trigger:** When improving code organization or clarity.
**Command:** `/refactor-file`

1. Rename files using camelCase.
2. Update all relative imports to reflect the new file name.
3. Ensure all exports remain named.
4. Run tests to confirm nothing is broken.

## Testing Patterns

- Test files follow the `*.test.*` naming convention (e.g., `shaderUtils.test.ts`).
- The specific testing framework is not specified; check for configuration files or scripts in the repository.
- Tests should cover both typical and edge-case usage of shader materials and utilities.

## Commands

| Command              | Purpose                                         |
|----------------------|-------------------------------------------------|
| /add-shader-material | Add a new custom shader material module         |
| /run-tests           | Run all test files in the repository            |
| /refactor-file       | Refactor or rename files following conventions  |
```