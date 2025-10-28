# Decision Log

This document records significant decisions made by the QE Guild regarding tool adoption, standards, and strategic direction.

This follows the [Architecture Decision Records (ADR)](https://adr.github.io/) format.

---

## [2025-10-28] Repository Restructure

**Status:** Accepted

**Context:**
The QE Guild repository had grown organically with:
- Scattered documentation across different directories
- 50% of tooling strategy documents empty
- Missing GitHub infrastructure (CODEOWNERS, issue templates)
- No clear decision-making process documented
- Difficult for new members to navigate

**Decision:**
Restructure the repository with:
- Clear separation of docs, templates, examples, and tools
- Decision tree framework for tool selection
- Comprehensive GitHub infrastructure
- Documented governance processes
- Improved navigation and discoverability

**Rationale:**
- Scalability: Easy to add new content without restructuring
- Discoverability: Logical hierarchy aids finding information
- Professionalism: Matches industry standards for guild repositories
- Onboarding: Clear path for new QE members
- Governance: Transparent decision-making

**Consequences:**
-  Better organisation and navigation
-  Clear contribution process
-  Easier onboarding
-  Breaking change: Files moved to new locations
-  Requires updating existing bookmarks/links

---

## [2024-11] Bruno Approved for API Testing

**Status:** Invest (Recommended)

**Context:**
Postman was widely used but has security concerns:
- Cloud sync of potentially sensitive API data
- Account management outside HO control
- Compliance risks for sensitive projects

**Decision:**
Approve Bruno as the recommended API testing tool for manual + automation scenarios.

**Rationale:**
-  File-based collections (Git-friendly)
-  No cloud sync (security compliant)
-  Open source
-  Similar UI/UX to Postman (easy migration)
-  Scriptable for automation
-  Environment management

**Consequences:**
- Teams should migrate from Postman to Bruno
- New projects must use Bruno (not Postman)
- Template and documentation created
- Training provided for teams

**Alternatives Considered:**
- Postman: Rejected due to security concerns
- Insomnia: Less feature-rich, smaller community
- Thunder Client: VS Code only, limited collaboration

---

## [2023-Q4] Playwright as Primary UI Automation Framework

**Status:** Invest (Recommended for new projects)

**Context:**
Teams were using various UI automation frameworks:
- Selenium (Java) - dominant but aging
- Cypress - limited browser support
- TestComplete - expensive
- No clear Microsoft/PowerApps recommendation

**Decision:**
Recommend Playwright + TypeScript as the primary UI automation framework for new projects.

**Rationale:**
-  Microsoft officially supported
-  Best choice for PowerApps/Dynamics (Microsoft ecosystem)
-  Modern features (auto-wait, trace viewer, component testing)
-  Cross-browser support
-  Multi-language (TS, Python, Java, .NET)
-  TypeScript binding has best support
-  Active development and community

**Consequences:**
- New UI automation projects should use Playwright + TypeScript
- Existing large Selenium frameworks can remain (Hold status)
- Migration guide provided for teams wanting to switch
- Training and templates created
- TypeScript skills need to be developed

**Alternatives Considered:**
- Selenium: Mature but slower, more complex. Status: Hold (legacy)
- Cypress: Limited to Chromium browsers, JS only. Status: Assess
- Puppeteer: Chrome-only, limited test runner. Status: Assess

---

## [2023-Q4] Rest Assured for Java API Testing

**Status:** Invest (Recommended for Java projects)

**Context:**
Java projects needed a robust API testing framework with excellent reporting.

**Decision:**
Recommend Rest Assured for Java-based API testing projects.

**Rationale:**
-  Excellent request/response logging and tracking
-  Fluent Java DSL
-  Deep JUnit/TestNG integration
-  Mature and stable
-  Great for debugging with detailed reports
-  Strong community support

**Consequences:**
- Java projects should use Rest Assured for API testing
- Template created with best practices
- Can be combined with Cucumber for BDD

**Alternatives Considered:**
- Karate: Good all-in-one, but less detailed Java integration
- HTTP Client + JUnit: Too low-level, lots of boilerplate

---

## [2023-Q3] Selenium + Cucumber for Enterprise Java Frameworks

**Status:** Hold (Acceptable for existing frameworks)

**Context:**
Many teams have large, established Selenium + Java test suites (10k+ tests).

**Decision:**
Status: Hold - Acceptable to keep existing Selenium frameworks, but recommend Playwright for new projects.

**Rationale:**
-  Massive existing investment
-  Team expertise in place
-  Stable and proven
-  High migration cost
-  Slower than modern alternatives
-  More complex maintenance

**Consequences:**
- Large existing frameworks can stay on Selenium
- Should modernize to Selenium 4
- Consider adding Cucumber for BDD
- New projects should evaluate Playwright first
- Incremental migration path available

---

## Template

Use this template for new decisions:

```markdown
## [YYYY-MM-DD] Decision Title

**Status:** Invest/Trial/Assess/Hold/Avoid

**Context:**
What is the situation prompting this decision?

**Decision:**
What did we decide to do?

**Rationale:**
Why did we make this decision? (Pros and cons)

**Consequences:**
What are the positive and negative implications?

**Alternatives Considered:**
What other options were evaluated?
```

---

**Maintained by:** QE Guild Maintainers (Edmond Chhung, Guru Bangalore Venkatesh)  
**Review Frequency:** Quarterly  
**Last Review:** October 2025  
**Next Review:** January 2026
