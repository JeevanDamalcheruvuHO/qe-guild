# Testing Principles

Core principles that guide quality engineering practices at the Home Office.

## Our Testing Philosophy

Quality is not just about finding bugs—it's about building quality into every stage of development. These principles guide our approach to quality engineering across all projects.

---

## 1. Shift-Left Testing

**Principle:** Find and fix issues as early as possible in the development lifecycle.

### Why It Matters
- Cheaper to fix bugs early
- Faster feedback loops
- Better collaboration between dev and QE

### How We Apply It
- ✅ Code reviews include test considerations
- ✅ Unit tests written alongside code
- ✅ API tests before UI tests
- ✅ Static analysis and linting in IDE
- ✅ Pre-commit hooks for quality checks

### Examples
```bash
# Pre-commit hook runs tests before code is committed
npm run test:unit && npm run lint

# CI pipeline fails fast on quality issues
```

---

## 2. Test Pyramid (and Beyond)

**Principle:** Balance test types for optimal coverage and speed.

### The Test Pyramid

```
        /\
       /  \      E2E Tests (Few, Slow, Brittle)
      /    \     - Critical user journeys
     /------\    - Cross-browser scenarios
    /        \   
   /  API     \  API/Integration Tests (More, Faster)
  /   Tests    \ - Business logic validation
 /--------------\- Contract testing
/   Unit Tests   \ Unit Tests (Many, Fast, Stable)
\----------------/- Function-level validation
                  - Edge cases
```

### Guidelines
- **70% Unit Tests** - Fast, isolated, developer-owned
- **20% API/Integration Tests** - Business logic, contracts
- **10% E2E/UI Tests** - Critical user journeys only

### Anti-Patterns to Avoid
- ❌ Ice cream cone (inverted pyramid)
- ❌ Testing everything through UI
- ❌ No API test coverage
- ❌ Ignoring unit tests

---

## 3. Testing is Everyone's Responsibility

**Principle:** Quality is a team sport, not just QE's job.

### Shared Ownership
- **Developers:** Write unit tests, fix bugs
- **QE Engineers:** Design test strategy, automation, complex scenarios
- **Product Owners:** Define acceptance criteria
- **DevOps:** Ensure tests run reliably in CI/CD

### Quality Gates
- All code requires tests
- PRs must pass all checks
- No bypassing quality gates for "urgent" changes

---

## 4. Automation Where It Matters

**Principle:** Automate strategically, not exhaustively.

### When to Automate
- ✅ Regression-prone areas
- ✅ Repetitive test scenarios
- ✅ Critical user paths
- ✅ API contracts
- ✅ Performance baselines

### When NOT to Automate
- ❌ One-off exploratory testing
- ❌ Rapidly changing features (wait until stable)
- ❌ Visual/UX validation (use manual testing)
- ❌ Cost exceeds benefit

### ROI Considerations
- Maintenance cost vs value
- Execution frequency
- Risk if not tested

---

## 5. Fast, Reliable, and Maintainable Tests

**Principle:** Tests should be trusted and easy to maintain.

### Fast
- **Target:** Unit tests <1s, API tests <5s, E2E tests <30s
- **Techniques:**
  - Parallel execution
  - Test data seeding (not creation in tests)
  - Mock external dependencies
  - Optimise wait strategies

### Reliable
- **Target:** <1% flakiness rate
- **Techniques:**
  - No hard-coded waits
  - Proper wait strategies (Playwright auto-wait)
  - Isolated test data
  - Cleanup after tests

### Maintainable
- **Techniques:**
  - Page Object Model / Screenplay patterns
  - DRY (Don't Repeat Yourself)
  - Clear naming conventions
  - Good test data management

---

## 6. Test Data Management

**Principle:** Test data should be isolated, repeatable, and safe.

### Best Practices
- ✅ Generate test data dynamically
- ✅ Clean up after tests
- ✅ Use realistic but anonymised data
- ✅ Never use production data
- ✅ Seed databases for fast setup

### Anti-Patterns
- ❌ Shared test data across tests
- ❌ Hard-coded IDs
- ❌ Copying production databases
- ❌ Tests that depend on execution order

---

## 7. Security Testing is Not Optional

**Principle:** Security must be validated, not assumed.

### Security Testing Layers
1. **Static Analysis** - Code scanning (SonarQube, Snyk)
2. **Dependency Scanning** - Known CVEs (Dependabot)
3. **Authentication Testing** - Auth flows, token handling
4. **Authorisation Testing** - Role-based access
5. **Input Validation** - SQL injection, XSS
6. **Security Headers** - CSP, HSTS, etc.

### QE Responsibilities
- Validate authentication/authorisation
- Test input validation
- Verify security headers
- Report potential vulnerabilities

---

## 8. Continuous Testing in CI/CD

**Principle:** Tests must run automatically and reliably in pipelines.

### CI/CD Integration
- ✅ Tests run on every PR
- ✅ Fast feedback (<10 minutes for core suite)
- ✅ Block merges on test failures
- ✅ Automatic retries (max 1) for flaky tests
- ✅ Test reports visible to team

### Pipeline Stages
```yaml
1. Lint & Format Check (1 min)
2. Unit Tests (2-3 min)
3. API Tests (3-5 min)
4. E2E Smoke Tests (5-8 min)
5. Full E2E Suite (Post-merge, 15-30 min)
```

---

## 9. Observability and Reporting

**Principle:** Tests should provide actionable insights.

### What to Track
- **Pass/Fail Rates** - Trend over time
- **Flakiness** - Identify unstable tests
- **Execution Time** - Optimise slow tests
- **Coverage** - Code and feature coverage
- **Defect Escape Rate** - Tests missed bugs

### Reporting Standards
- Clear test names (describe behaviour)
- Screenshots/videos on failure
- Request/response logs (API tests)
- Trace files (Playwright)
- Categorised failures (test issue vs product bug)

---

## 10. Accessibility is a Requirement

**Principle:** Applications must be accessible to all users.

### Accessibility Testing
- ✅ Automated a11y scans (axe-core)
- ✅ Keyboard navigation testing
- ✅ Screen reader compatibility
- ✅ Colour contrast validation
- ✅ WCAG 2.1 AA compliance

### Tools
- axe DevTools
- Pa11y
- Lighthouse
- Manual testing with screen readers

---

## 11. Performance Testing is Proactive

**Principle:** Don't wait for production to test performance.

### Performance Testing Types
1. **Load Testing** - Expected user load
2. **Stress Testing** - Breaking point
3. **Spike Testing** - Sudden traffic surges
4. **Endurance Testing** - Sustained load

### When to Test Performance
- ✅ Before major releases
- ✅ After architecture changes
- ✅ When scaling infrastructure
- ✅ Baseline for new features

---

## 12. Exploratory Testing Complements Automation

**Principle:** Automated tests find regressions, exploratory testing finds surprises.

### Exploratory Testing Sessions
- Unscripted investigation
- Focus on edge cases
- UX and usability validation
- Creative test scenarios

### Balance
- **Automation:** Regression, happy paths, contracts
- **Exploratory:** New features, edge cases, UX

---

## Applying These Principles

### For New Projects
1. Start with test strategy aligned to these principles
2. Set up test pyramid from day one
3. Integrate tests into CI/CD early
4. Choose tools that support these principles

### For Existing Projects
1. Assess current state against these principles
2. Identify biggest gaps
3. Incrementally improve (test pyramid, reliability, speed)
4. Refactor tests to patterns (POM, Screenplay)

### For QE Team Members
1. Champion these principles in your projects
2. Share learnings and patterns
3. Mentor developers on testing practices
4. Contribute to guild templates and standards

---

## Related Resources

- [Code Quality Standards](/docs/standards/code-quality-standards.md)
- [Security Guidelines](/docs/standards/security-guidelines.md)
- [Design Patterns](/docs/design-patterns/)
- [Tooling Recommendations](/docs/tooling/)

---

**Maintained by:** QE Guild  
**Last Updated:** October 2025  
**Next Review:** January 2026

*These principles are living standards. Suggest improvements via PR or discussion.*
