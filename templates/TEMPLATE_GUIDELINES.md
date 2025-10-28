# Template Guidelines

This document defines the standards for creating and maintaining templates in the QE Guild repository.

## 🎯 What Makes a Good Template?

A quality template should be:
- **Production-ready** - Works out of the box
- **Well-documented** - Clear setup and usage instructions
- **Best-practice** - Demonstrates recommended patterns
- **Maintainable** - Easy to understand and extend
- **Tested** - Includes working example tests

## 📂 Template Structure

Every template must follow this structure:

```
template-name/
├── README.md              # Setup and usage guide
├── .github/
│   └── workflows/
│       └── ci.yml         # CI/CD example
├── tests/                 # Example test files
│   ├── example.spec.ts    # Working test examples
│   └── ...
├── pages/                 # Page objects (UI) or clients (API)
│   └── ...
├── fixtures/              # Test data and fixtures
│   └── ...
├── config/                # Configuration files
│   ├── test.config.ts
│   └── ...
├── .env.example           # Environment variables template
├── .gitignore             # Appropriate ignores
├── package.json           # Dependencies (Node.js)
│   or pom.xml            # Dependencies (Java)
│   or requirements.txt   # Dependencies (Python)
└── TROUBLESHOOTING.md    # Common issues and solutions
```

## 📝 README Requirements

Every template README must include:

### 1. Overview
- What this template does
- When to use it
- Key features

### 2. Prerequisites
- Required software and versions
- System requirements
- Access/permissions needed

### 3. Installation
Step-by-step setup instructions:
```bash
# Clone the template
git clone ...

# Install dependencies
npm install  # or equivalent

# Setup environment
cp .env.example .env
```

### 4. Quick Start
Basic usage example:
```bash
# Run tests
npm test

# View results
npm run report
```

### 5. Project Structure
Explanation of the directory layout

### 6. Configuration
How to customize the template:
- Environment variables
- Config file options
- Test data setup

### 7. Writing Tests
Examples of creating new tests:
```typescript
// Example test structure
test('user can login', async () => {
  // Test implementation
});
```

### 8. Running Tests
Different execution modes:
- Local execution
- CI/CD execution
- Debugging
- Parallel execution

### 9. Reporting
How to generate and view test reports

### 10. Troubleshooting
Link to TROUBLESHOOTING.md or include common issues

### 11. Contributing
How to contribute improvements to the template

### 12. License
Link to repository license

## 🧪 Example Tests

Templates must include:

1. **Basic Example** - Simple "hello world" test
2. **Real-World Example** - Practical scenario
3. **Advanced Example** - Complex scenario showing best practices

Examples should be:
- **Runnable** - Work without modification
- **Commented** - Explain key concepts
- **Representative** - Show typical usage

## ⚙️ Configuration Standards

### Environment Variables
- Use `.env.example` for templates
- Document all variables in README
- Never commit actual `.env` files
- Use sensible defaults where possible

### Test Configuration
- Externalize configuration
- Support multiple environments (dev, staging, prod)
- Allow override via environment variables
- Include comments in config files

## 🔄 CI/CD Integration

Every template should include:

1. **GitHub Actions workflow** (`.github/workflows/ci.yml`)
   - Run on pull requests
   - Run on push to main
   - Generate test reports
   - Upload artifacts

2. **Example for other CI platforms** (optional)
   - Azure DevOps
   - Jenkins
   - GitLab CI

## 🎨 Code Quality

Templates must demonstrate:

### Naming Conventions
- Clear, descriptive names
- Follow language conventions (camelCase, snake_case, etc.)
- Avoid abbreviations

### Code Organization
- Logical file structure
- Separation of concerns
- DRY (Don't Repeat Yourself)

### Comments and Documentation
- Explain "why" not "what"
- Document complex logic
- JSDoc/JavaDoc for public APIs

### Error Handling
- Graceful error handling
- Meaningful error messages
- Proper logging

## 🔒 Security Best Practices

Templates must:
- ❌ Never include credentials
- ✅ Use environment variables for sensitive data
- ✅ Include `.gitignore` to prevent credential commits
- ✅ Demonstrate secure practices
- ✅ Follow HO security requirements

## 📦 Dependencies

### Version Pinning
- Pin major versions in package.json/requirements.txt/pom.xml
- Allow minor/patch updates
- Document breaking changes in updates

### Dependency Selection
- Use well-maintained packages
- Minimize dependency count
- Justify each dependency
- Keep dependencies updated

## 🧪 Testing the Template

Before submission, verify:

- [ ] All example tests pass
- [ ] Documentation is accurate
- [ ] Setup instructions work from scratch
- [ ] CI/CD pipeline runs successfully
- [ ] No credentials or sensitive data included
- [ ] All links work
- [ ] Code follows best practices
- [ ] Troubleshooting guide is helpful

## 🏷️ Versioning

Templates should follow semantic versioning:
- **Major** - Breaking changes
- **Minor** - New features, backward compatible
- **Patch** - Bug fixes

Document changes in template's CHANGELOG.md

## 👥 Ownership and Maintenance

### Template Owners
- Listed in [CODEOWNERS](/.github/CODEOWNERS)
- Responsible for:
  - Reviewing pull requests
  - Keeping template updated
  - Responding to issues
  - Updating dependencies

### Maintenance Expectations
- **Quarterly reviews** - Update dependencies, documentation
- **Respond to issues** - Within 1 week
- **Review PRs** - Within 1 week
- **Breaking changes** - Communicate clearly with migration guide

## 📋 Submission Checklist

Before submitting a new template:

- [ ] Follows template structure
- [ ] README includes all required sections
- [ ] Example tests are included and pass
- [ ] CI/CD workflow is configured
- [ ] No credentials or sensitive data
- [ ] Code follows best practices
- [ ] Dependencies are justified and pinned
- [ ] TROUBLESHOOTING.md exists
- [ ] .env.example provided
- [ ] .gitignore configured
- [ ] Tested from fresh clone
- [ ] [Template Submission Issue](/.github/ISSUE_TEMPLATE/template_submission.yml) created

## 🚫 Common Mistakes to Avoid

1. **Too Generic** - Templates should be opinionated and demonstrate best practices
2. **Too Specific** - Avoid organization-specific details that don't generalize
3. **Incomplete Documentation** - Every step must be documented
4. **Untested Instructions** - Verify setup works from scratch
5. **Outdated Dependencies** - Keep dependencies current
6. **Missing Error Handling** - Show how to handle failures
7. **No Real Examples** - Include practical, real-world scenarios

## 📚 Template Categories

### UI Automation
- Must include page object examples
- Demonstrate element interaction patterns
- Show how to handle waits and synchronization

### API Automation
- Must include request/response examples
- Demonstrate authentication
- Show how to validate responses

### Performance Testing
- Must include load profile examples
- Demonstrate metrics collection
- Show how to analyze results

### Mobile Automation
- Must include platform-specific examples
- Demonstrate app interaction patterns
- Show how to handle device capabilities

## 🔄 Template Lifecycle

1. **Submission** - via Template Submission Issue
2. **Review** - by CODEOWNERS
3. **Approval** - merge to repository
4. **Active** - maintained and updated
5. **Deprecated** - marked for replacement
6. **Archived** - moved to archive directory

## 💡 Tips for Success

- **Start with the README** - Clear documentation drives good structure
- **Keep it simple** - Focus on one framework/pattern
- **Show, don't tell** - Working code > lengthy explanations
- **Test everything** - Every instruction, every example
- **Ask for feedback** - Before official submission
- **Iterate** - Templates improve with use and feedback

## 📞 Questions?

- Review existing templates in [`/templates`](/templates/)
- Check [Template Submission guide](/.github/ISSUE_TEMPLATE/template_submission.yml)
- Contact maintainers: Edmond Chhung, Guru Bangalore Venkatesh
- Open a discussion in GitHub issues

---

**Last Updated:** October 2025
