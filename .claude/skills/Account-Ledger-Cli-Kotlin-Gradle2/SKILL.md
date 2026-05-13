```markdown
# Account-Ledger-Cli-Kotlin-Gradle2 Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the development patterns and conventions used in the `Account-Ledger-Cli-Kotlin-Gradle2` repository, a TypeScript-based project for managing account ledgers via a command-line interface. The guide covers file naming, import/export styles, commit patterns, and testing approaches, enabling consistent contributions and easier onboarding.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `accountLedger.ts`, `transactionManager.ts`

### Import Style
- Use **relative imports** for referencing modules within the project.
  - Example:
    ```typescript
    import { LedgerEntry } from './ledgerEntry';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    export function addTransaction(entry: LedgerEntry) { ... }
    export const TRANSACTION_LIMIT = 1000;
    ```

### Commit Patterns
- Commit messages are **freeform** (no strict prefixes).
- Typical commit message length: ~19 characters.
  - Example: `fix balance calculation`

## Workflows

### Adding a New Ledger Entry
**Trigger:** When you need to add a new transaction or entry to the ledger.
**Command:** `/add-ledger-entry`

1. Create or update a module (e.g., `ledgerManager.ts`) using camelCase naming.
2. Use relative imports to include necessary types or utilities.
   ```typescript
   import { LedgerEntry } from './ledgerEntry';
   ```
3. Export the new function or constant using named exports.
   ```typescript
   export function addLedgerEntry(entry: LedgerEntry) { ... }
   ```
4. Write or update a corresponding test file (e.g., `ledgerManager.test.ts`).
5. Commit your changes with a concise, descriptive message.

### Running Tests
**Trigger:** When verifying code changes.
**Command:** `/run-tests`

1. Ensure test files follow the `*.test.*` pattern (e.g., `accountLedger.test.ts`).
2. Use the project's test runner (framework unknown; check project documentation or scripts).
3. Run all tests and review results for failures.

## Testing Patterns

- Test files are named using the `*.test.*` pattern.
  - Example: `transactionManager.test.ts`
- The testing framework is **unknown**; refer to project scripts or documentation for details.
- Place tests alongside or near the modules they cover.

Example test file:
```typescript
import { addLedgerEntry } from './ledgerManager';

describe('addLedgerEntry', () => {
  it('should add a new entry to the ledger', () => {
    // test implementation
  });
});
```

## Commands
| Command             | Purpose                                 |
|---------------------|-----------------------------------------|
| /add-ledger-entry   | Add a new transaction to the ledger     |
| /run-tests          | Run all test suites                     |
```
