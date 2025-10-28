![logo.png](logo.png)

# QE Guild - Quality Engineering Standards & Resources

The purpose of this repository is to:
- Help Quality Engineering (QE) team members become familiar with tools and templates endorsed by the Home Office (HO) QE Guild
- Provide production-ready boilerplate templates for commonly used automation frameworks
- Outline patterns and standards for automation testing
- Facilitate tool comparisons and provide firsthand information to support selecting the most appropriate tools for specific projects
- Establish governance and decision-making processes for tool adoption

## Quick Start

**New to QE Guild?** Start here:
1.  [Getting Started Guide](/docs/getting-started/new-qe-onboarding.md)
2.  [Decision Trees](/docs/getting-started/decision-trees.md) - Find the right tool for your project
3.  [Standards](/docs/standards/) - Learn our testing principles
4.  [Templates](/templates/) - Use production-ready frameworks

**Need to choose a testing tool?**
- [UI Testing Decision Tree](/docs/getting-started/ui-testing-decision.md)
- [API Testing Decision Tree](/docs/getting-started/api-testing-decision.md)
- [Full Stack Decision Guide](/docs/getting-started/full-stack-decision.md)

## Repository Structure

```
qe-guild/
├── docs/              # All documentation
│   ├── getting-started/   # Onboarding and decision trees
│   ├── standards/        # QE testing standards
│   ├── design-patterns/  # Test automation patterns
│   ├── tooling/          # Tool comparisons and guides
│   ├── governance/       # Tool approval and decisions
│   └── training/         # Learning paths and resources
├── templates/        # Production-ready code templates
│   ├── ui-automation/    # Playwright, Selenium, Cypress
│   ├── api-automation/   # Bruno, Rest Assured, Karate
│   ├── performance-testing/
│   └── mobile-automation/
├── examples/         # Real-world examples and integrations
├── tools/            # Scripts, configs, and utilities
└── metrics/          # Adoption tracking and reviews
```

## Templates

Browse production-ready templates in the [`/templates`](/templates/) directory:

### UI Automation
- **[Playwright + TypeScript](/templates/ui-automation/playwright/typescript/)** - Recommended for new projects and PowerApps/Dynamics
- **[Playwright + Python](/templates/ui-automation/playwright/python/)** - For Python-centric teams
- **[Playwright + Java](/templates/ui-automation/playwright/java/)** - Limited support, consider carefully
- **[Selenium + Java](/templates/ui-automation/selenium/java-junit/)** - For large existing Java frameworks
## QE Guild Recommendations (2025)

### UI Testing
-  **Recommended:** Playwright + TypeScript (especially for PowerApps/Dynamics)
-  **Acceptable:** Selenium + Java + Cucumber (for large existing frameworks)
-  **Caution:** Playwright + Java (limited support)

### API Testing
-  **Recommended:** 
  - Bruno (manual + automation, HO approved)
  - Rest Assured (Java backends, excellent reporting)
  - Playwright API (when combined with UI testing)
-  **Avoid:** Postman (account sync security concerns)

### Performance Testing
-  **Recommended:** k6 (modern), JMeter (enterprise), Gatling (Scala teams)

See [Decision Trees](/docs/getting-started/decision-trees.md) for context-specific guidance.

## Documentation

### For New QE Members
- [Getting Started Guide](/docs/getting-started/new-qe-onboarding.md)
- [Decision Trees](/docs/getting-started/decision-trees.md)
- [Quick Start Guides](/docs/getting-started/quick-start-guides/)
- [Learning Paths](/docs/training/learning-paths/)

### Standards & Patterns
- [Testing Principles](/docs/standards/testing-principles.md)
- [Code Quality Standards](/docs/standards/code-quality-standards.md)
- [Page Object Model](/docs/design-patterns/page-object-model.md)
- [Screenplay Pattern](/docs/design-patterns/screenplay-pattern.md)

### Tooling Comparisons
- [UI Automation Tools](/docs/tooling/ui-automation/framework-comparison.md)
- [API Automation Tools](/docs/tooling/api-automation/tool-comparison.md)
- [Performance Testing Tools](/docs/tooling/performance-testing/tool-comparison.md)
- [CI/CD Best Practices](/docs/tooling/ci-cd/pipeline-standards.md)

### Governance
- [Tool Approval Process](/docs/governance/tool-approval-process.md)
- [Decision Log](/docs/governance/decision-log.md)
- [Roadmap](/docs/governance/roadmap.md)

## Contributing

We welcome and encourage contributions from QE team members!

### Ways to Contribute
1. **Submit a Template** - Use [Template Submission](/.github/ISSUE_TEMPLATE/template_submission.yml)
2. **Propose a Tool** - Use [Tool Evaluation](/.github/ISSUE_TEMPLATE/tool_evaluation.yml)
3. **Improve Documentation** - Submit a pull request
4. **Report Issues** - Use [Bug Report](/.github/ISSUE_TEMPLATE/bug_report.yml)
5. **Request Features** - Use [Feature Request](/.github/ISSUE_TEMPLATE/feature_request.yml)

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

### Template Ownership
Each template is maintained by designated owners (see [CODEOWNERS](/.github/CODEOWNERS)):
- Owners are responsible for keeping templates up to date
- Reviews are automated via GitHub CODEOWNERS
- Community contributions are encouraged

## Contact

**QE Guild Maintainers:**
- Edmond Chhung
- Guru Bangalore Venkatesh

**Email:** qe-guild-leads@homeoffice.gov.uk

## Metrics & Adoption

Track our progress and see what others are using:
- [Adoption Dashboard](/metrics/adoption-dashboard.md)
- [Template Usage Statistics](/metrics/template-usage.md)
- [Quarterly Reviews](/metrics/quarterly-reviews/)

## 📜 License

This repository is licensed under the [MIT License](LICENSE.md).

## Recent Updates

See [CHANGELOG.md](CHANGELOG.md) for recent changes and updates.

**Last Updated:** October 2025  
**Next Quarterly Review:** January 2026automation/appium/android/)** - Android app automation
- **[Appium - iOS](/templates/mobile-automation/appium/ios/)** - iOS app automation

**Note:** Each template includes:
- Complete setup instructions
- Example tests
- CI/CD configuration
- Best practices documentation
- Troubleshooting guide

See [Template Guidelines](/templates/TEMPLATE_GUIDELINES.md) for details.

## Tooling / Pattern / Standards
This section includes:
- Standards officially endorsed by the Quality Engineering Guild.
- Recommended design patterns for test automation.
- Tool comparisons to guide informed decision-making.

## Contributing
We welcome and encourage contributions from QE team members to enhance our repository of templates and tooling resources.

If you are interested in contributing:
Please link your template repository or submit a pull request to the relevant template directory.

For questions or further collaboration, feel free to reach out to the maintainers directly.
Alternatively contact 
Edmond Chhung or Guru Bangalore Venkatesh
