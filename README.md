# 🧪 Playwright Automation Framework

> 🚀 A complete automation framework using **Playwright + TypeScript**, applying **Page Object Model (POM)**, integrated with **Allure Reports**, supporting **multiple environments**, and ready for **CI/CD pipelines**.

---

## 📘 Table of Contents
1. [Introduction](#-introduction)  
2. [Project Structure](#-project-structure)  
3. [Installation](#-installation)  
4. [Running Tests](#-running-tests)  
5. [Allure Reports](#-allure-reports)   
6. [Best Practices & Extensions](#-best-practices--extensions)

---

## 💡 Introduction
This framework is designed to:
- Automate UI testing with **Playwright**
- Apply the **Page Object Model (POM)** design pattern
- Organize test cases by **feature or module**
- Generate clean **Allure Reports**
- Integrate with **CI/CD (GitHub Actions)**
- Support **multiple environments** (dev, staging, prod)

---

## 🗂️ Project Structure

```bash
playwright-automation/
│
├── 📁 tests/                 # Test cases by feature
│   ├── login/
│   │   └── login.spec.ts
│   └── product/
│       └── product.spec.ts
│
├── 📁 pages/                 # Page Object Models
│   ├── login/login.page.ts
│   └── product/product.page.ts
│
├── 📁 fixtures/              # Test data & shared setup
│   └── user.fixture.ts
│
├── 📁 data/                  # Static test data (JSON, CSV, etc.)
│   └── login.data.json
│
├── 📁 utils/                 # Helper functions & utilities
│   ├── logger.ts
│   └── api.helper.ts
│
├── 📁 config/                # Environment configuration
│   ├── dev.env.ts
│   ├── staging.env.ts
│   └── prod.env.ts
│         
├── allure-results/
├── allure-report/
│
├── 📁 .github/workflows/     # CI/CD pipeline files
│   └── playwright.yml
│
├── 🎛️ playwright.config.ts   # Playwright global config
├── 📦 package.json
└── 📄 README.md
```

---

## ⚙️ Installation

### 1️⃣ Prerequisites
- **Node.js ≥ 16**

Check versions:
```bash
node -v
npm -v
```

### 2️⃣ Install dependencies
```bash
npm install
```

### 3️⃣ Install Playwright browsers
```bash
npx playwright install
```

---

## ▶️ Running Tests

### Run all tests
```bash
npm run test
```

### Run tests by feature
```bash
npm run test tests/login
```

### Run a specific test file
```bash
npm run test tests/login/login.spec.ts
```

### Run with browser UI
```bash
npm run test:headed
```

---

## 📊 Allure Reports

### 1️⃣ Install Allure CLI
```bash
npm install -g allure-commandline --save-dev
```

### 2️⃣ Generate report
```bash
npm run report:generate
```

### 3️⃣ Open report
```bash
npm run report:open
```

---

---

## 🌈 Best Practices & Extensions

| Topic | Recommendation |
|--------|----------------|
| **Test Tags (smoke, regression)** | Use `test.describe('smoke', ...)` or custom tags |
| **Retry failed tests** | Add `retries: 1` in `playwright.config.ts` |
| **Screenshot & Video** | `use: { screenshot: 'only-on-failure', video: 'retain-on-failure' }` |
| **Data-driven tests** | Load test data from JSON or CSV |
| **Parallel execution** | Playwright supports built-in parallel runs |
| **Allure metadata** | Add tags, feature, story for report grouping |

---

## ✨ Author

**👩‍💻 Tran Thi Anh Nhi**  
Frontend Developer → Automation Tester  
📘 Practicing Playwright, Allure, CI/CD  
💬 Contact for setup guidance and mentoring
