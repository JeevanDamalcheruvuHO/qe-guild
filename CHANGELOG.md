# Changelog

All notable changes to the QE Guild repository will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- Complete repository restructure with improved organisation
- Decision tree framework for tool selection
- GitHub issue templates for template submissions, tool evaluations, bug reports, and feature requests
- Pull request template for standardised contributions
- CODEOWNERS file for automated review assignments
- Comprehensive `.gitignore` for security and cleanliness
- `.editorconfig` for consistent code formatting
- `SECURITY.md` for responsible vulnerability disclosure
- `CONTRIBUTORS.md` for community recognition
- Automated CI/CD workflows:
  - Markdown link checker (weekly + on PR)
  - Markdown linting
- Dependabot configuration for dependency updates
- `package.json` with linting and formatting scripts
- Testing Principles documentation
- Prettier and Markdownlint configurations
- Comprehensive documentation structure under `/docs`
- Getting started guides and decision trees
- Quick start guide stubs for common frameworks
- Standards and design patterns sections
- Enhanced tooling documentation structure
- Governance framework for tool approval and template lifecycle
- Training and learning path sections
- Examples directory for real-world scenarios
- Tools and utilities directory for scripts and configs
- Metrics tracking framework

### Changed
- Reorganized existing tooling documents into new structure
- Updated CONTRIBUTING.md with detailed workflow
- Fixed CODE_OF_CONDUCT.md contact placeholder
- Improved template standards documentation

### Fixed
- Typo in "contributers" → "contributors"
- Missing contact method in CODE_OF_CONDUCT.md
- Capitalization inconsistencies in CONTRIBUTING.md

## [1.0.0] - 2025-10-28

### Added
- Initial repository structure
- Basic README with mission and purpose
- CODE_OF_CONDUCT.md
- CONTRIBUTING.md
- LICENSE.md (MIT)
- Template standards documentation
- Initial tooling strategy documents:
  - UI/E2E Automation Tooling comparison
  - API Automation Tooling recommendations
  - NFR Automation Tooling (Performance & Accessibility)
  - Playwright language comparison (TS/Python/Java)
- Placeholder files for future documentation:
  - CI/CD tooling
  - Linters and Formatters
  - Observability tooling
  - Data migration pipeline tooling
  - Infrastructure testing tooling
  - Design patterns (POM/Screenplay)

### Recommendations Established
- **UI Testing:** Playwright + TypeScript for new projects; Selenium + Java + Cucumber for large existing Java frameworks
- **API Testing:** Bruno as HO-approved tool (replacing Postman)
- **BDD:** Cucumber/Serenity for Java projects

---

## Release Categories

### Added
New features, templates, documentation, or tools added to the repository.

### Changed
Changes to existing functionality, documentation updates, or reorganisation.

### Deprecated
Features or tools that are being phased out.

### Removed
Features, tools, or documentation that have been removed.

### Fixed
Bug fixes, typo corrections, or error resolutions.

### Security
Security-related changes or updates.

---

## Upcoming Changes

See [ROADMAP.md](/docs/governance/roadmap.md) for planned features and improvements.

## Past Decisions

See [Decision Log](/docs/governance/decision-log.md) for historical decision records.
