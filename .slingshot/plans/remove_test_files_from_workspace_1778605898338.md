---
name: Remove Test Files from Workspace
overview: Identify and delete all test files and test-related directories from the current workspace
userQuery: remove all the test cases already written I don't need them now
createdAt: '2026-05-12T17:11:38.338Z'
agentPhase: completed
todos:
  - id: 1
    content: Identify existing test files in the workspace
    status: completed
  - id: 2
    content: Remove all identified test files
    status: completed
  - id: 3
    content: Clean up test-related dependencies and configurations
    status: completed
executionStartedAt: '2026-05-12T17:12:55.147Z'
executionCompletedAt: '2026-05-12T17:15:29.553Z'
---

# Test File Removal Strategy

## Identification Approach
Use workspace exploration tools to systematically locate all test-related files and directories across the project structure.

### Common Test File Patterns
- **Test Files**: Files with `.test.js`, `.test.ts`, `.spec.js`, `.spec.ts`, `.test.tsx`  extensions
- **Test Directories**: Folders named `test`, `tests`, `__tests__`, `spec`, `specs`
- **Framework-Specific**: Jest, Mocha, Jasmine, Cypress, Playwright test configurations
- **Coverage Reports**: `coverage/`, `.nyc_output/`, test coverage artifacts

## Execution Steps

### 1. Workspace Analysis
First, explore the workspace structure to understand the current test file organization and identify all test-related content.

### 2. Test File Discovery
Use file search patterns to locate:
- All test files by extension patterns
- Test directories at any level in the project
- Test configuration files (jest.config.js, mocha.opts, etc.)
- Test-related dependencies in package.json

### 3. Safe Removal Process
- Validate each identified file/directory before deletion
- Remove test files and directories systematically
- Clean up test-related configuration entries
- Update package.json to remove test scripts and dependencies if desired

### 4. Verification
Confirm all test files have been successfully removed and the workspace is clean of test-related artifacts.

## Considerations
- **Backup Safety**: Ensure user has version control or backup before permanent deletion
- **Configuration Cleanup**: Remove test scripts from package.json and test-related configurations
- **Dependency Management**: Optionally remove test-only dependencies to reduce project size
- **Build Process**: Update any build scripts that reference removed test files