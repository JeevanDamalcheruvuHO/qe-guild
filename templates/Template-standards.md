# Automation Framework Templates
The template directory functions as a monorepo, offering boilerplate frameworks that QE members can utilize, reuse to explore and implement solutions based on their project requirements.

This document defines the **folder structure, naming conventions, and documentation standards** for all boilerplates and templates within this repository.

Following these conventions ensures:
- Consistent structure across all templates  
- Easier onboarding for new contributors  
- Seamless CI/CD automation and template discoverability  
- Predictable naming and versioning across frameworks and languages  


## Folder & File Naming Principles
* Use lowercase with hyphens
* Avoid spaces or special characters.
* Folder names should be short, descriptive, and action-oriented.
* Keep a consistent hierarchy across all template


## 📁 Folder Structure

```
EXAMPLE: 

template/
├── README.md
├── LICENSE
├── CHANGELOG.md
├── CONTRIBUTING.md
│
├── playwright/
│   ├── .github/
│   ├── README.md
│   ├── js-ts/
│   │   ├── pages/
│   │   │   ├── components/
│   │   ├── tests/
│   │   ├── playwright.config.ts
│   │   └── package.json
│   ├── python/
│   │   ├── pages/
│   │   │   ├── components/
│   │   ├── tests/
│   │   ├── requirements.txt
│   │   └── playwright.config.py
│   ├── .github/
│   ├── java/
│   │   ├── src/test/java/
│   │   ├── pom.xml
│   │   └── README.md
│   ├── .github/
│   └── PLAYWRIGHT-LANGUAGE-COMPARISON.md
│
├── cypress/
│   ├── js-ts/
│   │   ├── cypress.config.js
│   │   ├── cypress/
│   │   │   ├── e2e/
│   │   │   ├── fixtures/
│   │   │   └── support/
│   │   └── package.json
│   ├── .github/
│   └── README.md
│
├── selenium/
│   ├── .github/
│   ├── python/
│   │   ├── tests/
│   │   ├── pages/
│   │   │   ├── components/
│   │   ├── drivers/
│   │   ├── requirements.txt
│   │   └── README.md
│   ├── java/
│   │   ├── src/test/java/
│   │   ├── pom.xml
│   │   └── README.md
│   └── README.md
│
├── api-testing/
│   ├── .github/
│   ├── bruno/
│   │   ├── collections/
│   │   ├── environments/
│   │   └── README.md
│   ├── python/
│   │   ├── tests/
│   │   ├── requests/
│   │   ├── conftest.py
│   │   ├── requirements.txt
│   │   └── README.md
│   └── README.md
│
└── utils/Tools
    ├── scripts/
    │   ├── setup.sh
    │   ├── run-tests.py    
    └── README.md
```

## Summary

* All boilerplates follow the same top-level and internal structure.  
* Each framework and language implementation that includes a `README.md`.  
* CI/CD, docs, and scripts are organized and standardized.  
* Documentation lives under `/docs/` under each boilerplate.  
