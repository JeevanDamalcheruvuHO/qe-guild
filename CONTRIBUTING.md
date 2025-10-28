# Contribution Guide

We are looking for contributors to expand the templates and tooling section to help fellow QE members. If you would like
to contribute, please link your template repo or send a pull request to the relevant template. Alternatively contact
Edmond Chhung or Guru Bangalore Venkatesh.


This repository uses a `CODEOWNERS` file to define **who is responsible for reviewing pull requests/owns templates/boilerplates** for different parts of the codebase.

### File location

- Global owners: `.github/CODEOWNERS`
- Framework-specific folders:  
`templates/playwright/`

### How to add or update owners

1. Open `.github/CODEOWNERS`.
2. Add the GitHub usernames or teams responsible for a file or folder.
3. Commit the change and push to a branch.
4. Open a PR to have the change reviewed by existing owners.

## Contribution Workflow

### For Template Contributors

1. **Prepare Your Template**
   - Follow [Template Guidelines](/templates/TEMPLATE_GUIDELINES.md)
   - Include README with setup instructions
   - Add example tests and configuration
   - Test locally to ensure it works

2. **Submit for Review**
   - Create a [Template Submission Issue](/.github/ISSUE_TEMPLATE/template_submission.yml)
   - Fork the repository
   - Add your template to the appropriate directory
   - Create a pull request

3. **Review Process**
   - CODEOWNERS will review your submission
   - Address feedback and make requested changes
   - Once approved, your template will be merged

### For Documentation Contributors

1. **Identify the Gap**
   - What documentation is missing or needs improvement?
   - Check existing docs to avoid duplication

2. **Make Your Changes**
   - Follow Markdown best practices
   - Use Mermaid for diagrams where appropriate
   - Add cross-references to related documents

3. **Submit Pull Request**
   - Clear description of what you're improving
   - Link to any related issues

### For Tool Evaluations

1. **Submit Evaluation Request**
   - Use [Tool Evaluation template](/.github/ISSUE_TEMPLATE/tool_evaluation.yml)
   - Provide comprehensive comparison
   - Include POC results if available

2. **Guild Review**
   - QE Guild will evaluate the tool
   - Discussion and feedback period
   - Decision recorded in /docs/governance/decision-log.md

## Contribution Guidelines

- **Quality over quantity** - Well-tested, documented contributions
- **Follow standards** - Use existing templates as examples
- **Be responsive** - Address review feedback promptly
- **Share knowledge** - Help others learn from your contributions
