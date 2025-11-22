---
applyTo: "**/tests/*.spec.ts"
---

## Playwright test requirements

When writing Playwright tests, please follow these guidelines to ensure consistency and maintainability:

1. **Use stable locators** - Prefer `getByRole()`, `getByText()`, and `getByTestId()` over CSS selectors or XPath
1. **Write isolated tests** - Each test should be independent and not rely on other tests' state
1. **Follow naming conventions** - Use descriptive test names and `*.spec.ts` file naming
1. **Implement proper assertions** - Use Playwright's `expect()` with specific matchers like `toHaveText()`, `toBeVisible()`
1. **Leverage auto-wait** - Avoid manual `setTimeout()` and rely on Playwright's built-in waiting mechanisms
1. **Configure cross-browser testing** - Test across Chromium, Firefox, and WebKit browsers
1. **Use Page Object Model** - Organize selectors and actions into reusable page classes for maintainability
1. **Handle dynamic content** - Properly wait for elements to load and handle loading states
1. **Set up proper test data** - Use beforeEach/afterEach hooks for test setup and cleanup
1. **Configure CI/CD integration** - Set up headless mode, screenshots on failure, and parallel execution
