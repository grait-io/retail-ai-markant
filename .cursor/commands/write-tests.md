---
description: Generate comprehensive tests for the current file or function
---

Analyze the referenced file or function and generate comprehensive tests:

1. Identify all public functions and their edge cases
2. Generate tests using the AAA pattern (Arrange-Act-Assert)
3. Include:
   - Happy path tests
   - Error/edge case tests
   - Boundary value tests
   - Null/undefined handling tests
4. Place tests in a co-located file: `{filename}.test.ts`
5. Run the tests to verify they pass
6. Report coverage for the tested functions
