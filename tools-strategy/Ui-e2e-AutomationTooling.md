# Automation Frameworks

This document provides an overview of popular automation tools available in the market, along with a comparison table highlighting their pros and cons.

### List of Automation Tools in Market

- Selenium
- Cypress
- Playwright
- Appium
- TestComplete
- Robot Framework
- Puppeteer
- Katalon Studio
- Cucumber
- Ranorex

### Automation Tools Comparison Table

| Framework        | Version | Open Source | Active Contributions | Cost                | Type     | Pros                                                        | Cons                                                      |
|------------------|---------|-------------|----------------------|---------------------|----------|-------------------------------------------------------------|-----------------------------------------------------------|
| Selenium         | 4.x     | Yes         | Yes                  | Free                | UI/API   | Mature, large community, supports many languages/browsers   | Steep learning curve, no built-in reporting               |
| Cypress          | 13.x    | Yes         | Yes                  | Free (Pro paid)     | UI/API   | Fast, easy setup, great debugging, modern JS support        | Limited browser support, JS only, not for legacy apps      |
| Playwright       | 1.x     | Yes         | Yes                  | Free                | UI/API   | Cross-browser, multi-language, modern features              | Newer, smaller community than Selenium                    |
| Appium           | 2.x     | Yes         | Yes                  | Free                | UI       | Mobile automation, cross-platform, supports many languages  | Slower execution, setup complexity                        |
| TestComplete     | 15.x    | No          | Yes                  | Paid                | UI/API   | Easy to use, supports many technologies, good support       | Expensive, Windows-centric                                |
| Robot Framework  | 6.x     | Yes         | Yes                  | Free                | UI/API   | Keyword-driven, extensible, easy to learn                   | Python-centric, less flexible for complex scenarios        |
| Puppeteer        | 21.x    | Yes         | Yes                  | Free                | UI/API   | Headless Chrome/Firefox, fast, JS/TS support                | Chrome/Firefox only, JS only                              |
| Katalon Studio   | 9.x     | Partial     | Yes                  | Free (Pro paid)     | UI/API   | All-in-one, easy UI, built-in integrations                  | Advanced features paid, less customizable                  |
| Cucumber         | 7.x     | Yes         | Yes                  | Free                | UI/API   | BDD support, readable syntax, multi-language                | Needs runner, can be slow                                 |
| Ranorex          | 10.x    | No          | Yes                  | Paid                | UI       | Easy UI, supports many apps, good reporting                 | Expensive, Windows only                                   |

### BDD-Based Frameworks

Below are popular Behavior-Driven Development (BDD) frameworks, with a comparison of their features, pros, cons, cost, and open source status.

- Cucumber
- SpecFlow
- Serenity BDD
- Behave
- JBehave
- Gauge

### BDD Frameworks Comparison Table

| Framework      | Version | Open Source | Active Contributions | Cost                | Type    | Pros                                                        | Cons                                                      |
|----------------|---------|-------------|----------------------|---------------------|---------|-------------------------------------------------------------|-----------------------------------------------------------|
| Cucumber       | 7.x     | Yes         | Yes                  | Free                | UI/API  | Widely used, readable Gherkin syntax, multi-language        | Needs runner (e.g. Selenium), can be slow                 |
| SpecFlow       | 3.x     | Partial     | Yes                  | Free (Pro paid)     | UI/API  | .NET support, integrates with Visual Studio, Gherkin syntax | Advanced features paid, .NET only                         |
| Serenity BDD   | 3.x     | Yes         | Yes                  | Free                | UI/API  | Rich reporting, integrates with Selenium/Appium/Cucumber    | Java only, setup can be complex                           |
| Behave         | 1.x     | Yes         | Yes                  | Free                | API     | Python support, simple syntax, easy integration             | Python only, smaller community                            |
| JBehave        | 4.x     | Yes         | Limited              | Free                | UI/API  | Java support, flexible configuration                        | Less active, steeper learning curve                       |
| Gauge          | 1.x     | Yes         | Yes                  | Free                | UI/API  | Language agnostic, extensible, readable specs               | Smaller ecosystem, fewer integrations than Cucumber        |

**Notes:**
- "Partial" in Open Source means core is open source but some features may be paid.
- "Active Contributions" indicates if the project is actively maintained and updated.
- Type: UI = User Interface testing, API = API/Web Service testing, UI/API = supports both.
- Cost: "Free (Pro paid)" means a free tier exists, but advanced features require payment.


# Recommendation by Guild
Given our current large-scale Java automation framework built on Selenium, it is recommended to continue leveraging this robust and widely supported stack, especially due to its maturity, extensive community support, and compatibility with enterprise needs. To further enhance test readability and collaboration, adopting a BDD approach using Cucumber/ Serinity (Java) is advised, enabling clear communication between technical and non-technical stakeholders.

Additionally, the Guild suggests exploring modern tools like Playwright for new projects or pilot initiatives. Playwright offers advanced cross-browser automation, multi-language support, and modern features that can complement or gradually extend existing capabilities. This dual approach ensures stability with proven tools while staying current with emerging automation technologies.
