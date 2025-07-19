
---
# 💻 Test Automation Framework | API 

[![Playwright](https://img.shields.io/badge/Playwright-34495E?style=for-the-badge&logo=playwright&logoColor=white)](https://playwright.dev/)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://js.org/index.html) 

[![VS Code](https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white)](https://code.visualstudio.com/)
[![Allure Report](https://img.shields.io/badge/Allure%20Report-FF6B6B?style=for-the-badge&logo=allure&logoColor=white)](https://docs.qameta.io/allure/)
[![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)](https://github.com/features/actions) 

## 📑 Table of Contents
<!-- # - [Video Tutorial](#video-tutorial) -->
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Running Tests](#running-tests)
- [Project Structure](#project-structure)
- [Configuration](#configuration)
- [Continuous Integration](#continuous-integration)
- [Reporting](#reporting)
- [Other Projects](#other-projects)
- [Technical Documents](#technical-documents)
- [Contacts](#contacts)

## 📖 Introduction
This repository contains a **Test Automation Framework** built using **Playwright** and **Javascript** for automated testing of **REST APIs**.

<!-- ## 🎥 Video Tutorial

<a href="https://www.youtube.com/watch?v=g0nG6aPbpl4&list=PLrBBHmoBFxBUu9G7haETpa0B03H9GnfKX"> <img src="https://img.youtube.com/vi/g0nG6aPbpl4/0.jpg" alt="Test Automation Framework | WEB | Cypress + JS" width="200"> </a>

Click on the image above to watch the tutorials. -->

## 🛠️ Prerequisites

- [![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/) (v18.16.1 or higher recommended)
- [![npm](https://img.shields.io/badge/npm-CB3837?style=for-the-badge&logo=npm&logoColor=white)](https://www.npmjs.com/) (v9.5.1 or higher recommended)

## ▶️ Getting Started

1. **Clone the repository:**

   ```bash
   git clone https://github.com/Srikanth-Bokka/Playwright_JS_AutomationFramework_Srikanth_Bokka_API.git
   ```

2. **Navigate to the project directory:**

   ```bash
   cd Playwright_JS_AutomationFramework_Srikanth_Bokka_API
   ```

3. **Install dependencies:**

   ```bash
   npm install
   ```

## 🚀 Running Tests

  ```bash
  npm run playwright:tests
  ```

## 📁 Project Structure

The tests follow a modular and maintainable structure:

```
|-- .github
|     |-- workflows
|          |-- 01_api_tests.yml
|          |-- 02_api_tests_select_env.yml
|-- allure-results/          # Allure test results (generated after test execution)
|-- allure-report/           # Allure HTML report (generated after report generation)
|-- test-data
|     |-- request-body
|          |-- users
|              |-- user_create.json
|              |-- user_update_patch.json
|              |-- user_update_put.json
|     |-- schema
|          |-- users
|              |-- user_create.json
|              |-- user_update_patch.json
|              |-- user_update_put.json
|-- tests-reqres
|     |-- login.spec.js
|     |-- register.spec.js
|     |-- users.spec.js
|-- utils
|     |-- EndpointUtils.js
|     |-- RequestBodyUtils.js
|     |-- RequestUtils.js
|     |-- ResponseUtils.js
|     |-- SchemaUtils.js
|     |-- TokenUtils.js
|     |-- VerificationUtils.js
|-- .gitignore
|-- package.json
|-- playwright.config.js
```

- `allure-results`: Contains Allure test results generated after test execution.
- `allure-report`: Contains the generated Allure HTML report with detailed test analytics and visualizations.
- `test-data`: Contains external files (example: user create/update data) that can be used to mock data during tests.
- `tests-reqres`: Contains the actual test files. You can organize your tests into subdirectories as needed. 
- `utils`: Contains the Utilities that provides methods for asserting different conditions on web elements, handling requests and responses.

## ⚙️ Configuration

- Modify `playwright.config.js` for playwright configuration settings such as
  - `baseURL`
  - `testDir`
  - `reporter` (configured for Allure reporting)

## 🔄 Continuous Integration

This project is configured for CI using Github Actions. Check the configurations in `.github/workflows/*.yml`.

- `01_api_tests.yml`: This workflow executes tests in pre-defined environment PROD.
- `02_api_tests_select_env.yml`: This workflow will first ask User to select the environment (DEV / Pre-PROD / PROD) for tests execution.

## 📊 Reporting

This framework uses **Allure Report** for comprehensive test reporting. Allure provides detailed test execution reports with rich features like:

- **Test Execution Timeline**: Visual representation of test execution flow
- **Environment Information**: Detailed system and test environment details
- **Test Categories**: Automatic categorization of tests (failed, broken, skipped, passed)
- **Attachments**: Screenshots, logs, and other test artifacts
- **Trends**: Historical test execution trends and statistics
- **Custom Categories**: Ability to create custom test categories and filters

### Running Tests and Generating Reports

1. **Run tests:**
   ```bash
   npm run playwright:tests
   ```

2. **Generate and open Allure report:**
   ```bash
   npm run allure:report
   ```

3. **Generate report only (without opening):**
   ```bash
   npm run allure:generate
   ```

### Allure Report Structure

- `allure-results/`: Contains raw test execution data
- `allure-report/`: Contains the generated HTML report (created when you run the report command)

### Prerequisites for Allure

Make sure you have Allure command-line tool installed:

**macOS (using Homebrew):**
```bash
brew install allure
```

**Windows (using Scoop):**
```bash
scoop install allure
```

**Linux:**
```bash
sudo apt-add-repository ppa:qameta/allure
sudo apt-get update
sudo apt-get install allure
```
