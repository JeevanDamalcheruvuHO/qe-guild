# Templates

Welcome to the QE Guild template library! This directory contains production-ready boilerplate frameworks for common testing scenarios.

## 🎯 What are Templates?

Templates are complete, runnable automation frameworks that:
- **Work out of the box** - Clone and run immediately
- **Follow best practices** - Demonstrate recommended patterns
- **Include examples** - Real working tests you can learn from
- **Are fully documented** - Setup, usage, and troubleshooting guides
- **Are maintained** - Regularly updated by designated owners

## 📂 Available Templates

### UI Automation

#### Playwright
- **[TypeScript](/templates/ui-automation/playwright/typescript/)** ✅ Recommended
  - Modern, fast, Microsoft-supported
  - Best for PowerApps/Dynamics
  - Auto-wait, trace viewer, component testing
  
- **[Python](/templates/ui-automation/playwright/python/)**
  - For Python-centric teams
  - Good for data-heavy testing
  - Slightly slower updates than TypeScript
  
- **[Java](/templates/ui-automation/playwright/java/)** ⚠️ Use with caution
  - Limited community support
  - Consider Selenium for Java projects

#### Selenium
- **[Java + JUnit](/templates/ui-automation/selenium/java-junit/)**
  - For existing Java frameworks
  - Mature and stable
  
- **[Java + Cucumber](/templates/ui-automation/selenium/java-cucumber/)**
  - BDD with Java
  - Business-readable tests

### API Automation

- **[Bruno](/templates/api-automation/bruno/)** ✅ HO Approved
  - Manual + automation
  - No cloud sync (security compliant)
  - Git-friendly collections
  
- **[Rest Assured](/templates/api-automation/rest-assured/)** ✅ Best for Java
  - Excellent request/response tracking
  - Fluent Java DSL
  - Great reporting
  
- **[Karate DSL](/templates/api-automation/karate/)**
  - All-in-one: testing + mocking + performance
  - Gherkin-style syntax
  
- **[Pytest + Requests](/templates/api-automation/pytest-requests/)**
  - Python API testing
  - Great for data-heavy scenarios

### Performance Testing

- **[JMeter](/templates/performance-testing/jmeter/)**
  - Enterprise standard
  - Comprehensive features
  
- **[k6](/templates/performance-testing/k6/)**
  - Modern, developer-friendly
  - JavaScript/TypeScript
  
- **[Gatling](/templates/performance-testing/gatling/)**
  - Scala-based
  - Excellent reporting

### Mobile Automation

- **[Appium - Android](/templates/mobile-automation/appium/android/)**
- **[Appium - iOS](/templates/mobile-automation/appium/ios/)**

### BDD Frameworks

- **[Cucumber + Java](/templates/bdd-frameworks/cucumber-java/)**
- **[Cucumber + JavaScript](/templates/bdd-frameworks/cucumber-js/)**
- **[Behave + Python](/templates/bdd-frameworks/behave-python/)**

## 🚀 How to Use a Template

### 1. Choose the Right Template

Not sure which template to use? See our [Decision Trees](/docs/getting-started/decision-trees.md):
- [UI Testing Decision Tree](/docs/getting-started/ui-testing-decision.md)
- [API Testing Decision Tree](/docs/getting-started/api-testing-decision.md)
- [Full Stack Decision Guide](/docs/getting-started/full-stack-decision.md)

### 2. Clone the Template

```bash
# Copy the template to your project
cp -r /path/to/qe-guild/templates/ui-automation/playwright/typescript my-new-tests

# Or clone directly if using Git
git clone <template-repo> my-new-tests
```

### 3. Follow the README

Each template includes a comprehensive README with:
- Prerequisites
- Installation steps
- Quick start guide
- Configuration options
- How to write tests
- Running tests
- Troubleshooting

### 4. Customize for Your Project

- Update configuration files
- Add your test cases
- Configure environments
- Set up CI/CD

## 📝 Template Structure

Every template follows a consistent structure:

```
template-name/
├── README.md              # Complete setup and usage guide
├── .github/
│   └── workflows/
│       └── ci.yml         # CI/CD example
├── tests/                 # Example test files
├── pages/                 # Page objects (UI) or API clients
├── fixtures/              # Test data
├── config/                # Configuration
├── .env.example           # Environment variables
├── .gitignore
└── TROUBLESHOOTING.md    # Common issues
```

See [Template Guidelines](/templates/TEMPLATE_GUIDELINES.md) for complete structure details.

## ✅ What's Included

Every template includes:

✅ **Working Examples**
- Basic example test
- Real-world scenario
- Advanced pattern demonstration

✅ **Complete Documentation**
- Setup instructions
- Usage guide
- Configuration options
- Troubleshooting

✅ **CI/CD Integration**
- GitHub Actions workflow
- Example for other CI platforms

✅ **Best Practices**
- Recommended patterns
- Code organization
- Error handling
- Logging

✅ **Development Tools**
- Linting configuration
- Formatting setup
- Pre-commit hooks (where applicable)

## 🎓 Learning from Templates

Templates are excellent learning resources:

1. **Read the code** - See how best practices are implemented
2. **Run the examples** - Understand how things work
3. **Modify and experiment** - Learn by doing
4. **Compare templates** - See different approaches

## 🤝 Contributing Templates

Want to contribute a template? Great!

### Before You Start

1. Check if a similar template exists
2. Review [Template Guidelines](/templates/TEMPLATE_GUIDELINES.md)
3. Submit a [Template Submission Issue](/.github/ISSUE_TEMPLATE/template_submission.yml)

### Submission Process

1. **Prepare Your Template**
   - Follow the template structure
   - Include all required documentation
   - Ensure it works from fresh clone
   - Test on clean environment

2. **Submit for Review**
   - Create template submission issue
   - Fork the repository
   - Add your template
   - Create pull request

3. **Review and Approval**
   - CODEOWNERS will review
   - Address feedback
   - Template merged and published

See [CONTRIBUTING.md](/CONTRIBUTING.md) for complete guidelines.

## 🔧 Template Maintenance

### Ownership

Each template has designated owners (see [CODEOWNERS](/.github/CODEOWNERS)) responsible for:
- Keeping dependencies updated
- Fixing bugs
- Responding to issues
- Reviewing PRs
- Adding improvements

### Updates

Templates are reviewed and updated:
- **Quarterly** - Dependency updates, minor improvements
- **As needed** - Bug fixes, security patches
- **Annually** - Major version updates, refactoring

### Version Control

Templates follow semantic versioning:
- **Major** (1.0.0) - Breaking changes
- **Minor** (0.1.0) - New features, backward compatible
- **Patch** (0.0.1) - Bug fixes

## ⚠️ Template Status

Templates may have different status levels:

- ✅ **Production Ready** - Fully tested and maintained
- 🚧 **Beta** - Functional but may have rough edges
- 📝 **Placeholder** - Planned but not yet created
- 🗃️ **Deprecated** - No longer recommended

## 🐛 Reporting Issues

Found a problem with a template?

1. Check [TROUBLESHOOTING.md] in the template
2. Search existing issues
3. Submit [Bug Report](/.github/ISSUE_TEMPLATE/bug_report.yml)
4. Contact template owner (see CODEOWNERS)

## 💡 Requesting Features

Want a new template or feature?

1. Submit [Feature Request](/.github/ISSUE_TEMPLATE/feature_request.yml)
2. Describe the use case
3. Propose a solution
4. Consider contributing!

## 📊 Template Usage

See [Metrics](/metrics/) for template usage statistics and adoption rates.

## 📞 Help and Support

**Template Questions:**
- Check template's README and TROUBLESHOOTING
- Review [Documentation](/docs/)
- Contact template owner (see CODEOWNERS)

**General Questions:**
- Edmond Chhung
- Guru Bangalore Venkatesh
- qe-guild-leads@homeoffice.gov.uk

## 📚 Related Documentation

- [Template Guidelines](/templates/TEMPLATE_GUIDELINES.md) - For contributors
- [Decision Trees](/docs/getting-started/decision-trees.md) - Choose the right template
- [Tooling Documentation](/docs/tooling/) - Detailed tool comparisons
- [Standards](/docs/standards/) - Quality and code standards

---

**Last Updated:** October 2025  
**Next Review:** January 2026

*Templates are living resources. We continuously improve them based on feedback and emerging best practices.*
