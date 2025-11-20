# Cypress Test Automation Project - Complete Tutorial & Learning Guide (Gherkin + Cucumber + Mocha + Chai + E2E + BDD + POM + API + Database + Excel + CI/CD + Reporting + Testing)

A comprehensive Cypress test automation framework that combines end-to-end UI testing, Behavior-Driven Development (BDD) with Cucumber/Gherkin, and enterprise integrations including SQL Server database connectivity, Excel file operations, and REST API testing. Built on Page Object Model architecture with custom commands and advanced reporting (Mochawesome & Cucumber HTML), it supports multi-browser execution and CI/CD integration for scalable, maintainable test automation.

![Cypress Automation](https://github.com/user-attachments/assets/22e7e0fc-fa11-4c49-bdab-b645b442404b)

---

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Key Features](#key-features)
- [Prerequisites](#prerequisites)
- [Installation & Setup](#installation-setup)
- [Environment Configuration](#environment-configuration)
- [How to Run Tests](#how-to-run-tests)
- [Understanding the Framework](#understanding-the-framework)
- [Project Components Deep Dive](#project-components-deep-dive)
- [Test Examples & Use Cases](#test-examples-use-cases)
- [Reusing Components in Other Projects](#reusing-components-in-other-projects)
- [Reporting](#reporting)
- [Troubleshooting](#troubleshooting)
- [Keywords](#keywords)
- [Conclusion](#conclusion)

---

## 🎯 Project Overview {#project-overview}

This repository is a **comprehensive learning resource** for mastering Cypress—a leading framework for end-to-end (E2E) test automation of modern web applications. It is designed for both beginners and professionals to understand all aspects of UI test automation, including real-world best practices, reusable patterns, modular test design, custom plugins, and integration with popular CI/CD pipelines.

The project demonstrates:

- **End-to-End UI Automation**: Complete user journey testing in real browsers
- **BDD (Behavior-Driven Development)**: Using Cucumber and Gherkin syntax
- **Page Object Model (POM)**: Maintainable and reusable test architecture
- **API Testing**: Integration with REST APIs
- **Database Integration**: SQL Server connectivity for data-driven testing
- **Excel File Handling**: Read/write operations for test data management
- **Custom Commands**: Reusable test actions
- **Advanced Reporting**: Mochawesome and Cucumber HTML reports

> **Note:** The underlying practice website may change its UI or features over time. If you encounter assertion failures, revalidate selectors or assertions against the live site.

---

## 🛠 Technology Stack {#technology-stack}

### Core Framework

- **Cypress**: `^13.15.1` - Main E2E testing framework
- **Node.js**: v18.x.x or later (tested with Node 18)
- **npm**: Package management

### Testing Libraries & Tools

- **Mocha**: `^10.1.0` - Test runner and assertion library
- **Chai**: Built-in with Cypress - Assertion library
- **@badeball/cypress-cucumber-preprocessor**: `^21.0.2` - BDD support with Gherkin
- **@cypress/browserify-preprocessor**: Latest - Transpiles feature files

### Reporting

- **cypress-mochawesome-reporter**: `^3.8.2` - Enhanced Mocha HTML reports
- **multiple-cucumber-html-reporter**: `^3.0.1` - Beautiful Cucumber HTML reports

### Integrations & Utilities

- **cypress-sql-server**: `^1.0.0` - SQL Server database connectivity
- **convert-excel-to-json**: `^1.7.0` - Excel to JSON conversion
- **exceljs**: `^4.4.0` - Excel file read/write operations
- **cypress-iframe**: `^1.0.1` - Iframe handling support
- **neat-csv**: `5.1.0` - CSV file parsing

---

## 📁 Project Structure {#project-structure}

```bash
CypressAutomation/
├── cypress/
│   ├── fixtures/                    # Test data files (JSON, CSV, Excel)
│   │   └── example.json            # Sample test data
│   ├── integration/                 # Test files
│   │   ├── examples/                # General Cypress examples
│   │   │   ├── BDD/                 # BDD/Cucumber tests
│   │   │   │   ├── ecommerce/
│   │   │   │   │   ├── beforeEach.js
│   │   │   │   │   └── eCommStepDef.js
│   │   │   │   └── ecommerce.feature
│   │   │   ├── Test8Framework.js    # Page Object Model example
│   │   │   ├── sqldb.js             # Database integration example
│   │   │   ├── Excel_Task_validations.js  # Excel handling example
│   │   │   ├── upload-download.js   # File operations example
│   │   │   ├── sampleTest.js        # Iframe handling example
│   │   │   └── ...                  # Other test examples
│   │   └── GreenKart/               # Domain-specific test suite
│   │       ├── Test1.js
│   │       └── Test2.js
│   ├── plugins/                     # Cypress plugins
│   │   └── index.js                 # Plugin configuration
│   ├── support/                     # Support files (loaded before tests)
│   │   ├── commands.js              # Custom Cypress commands
│   │   ├── e2e.js                   # Support file imports
│   │   └── pageObjects/             # Page Object Model classes
│   │       ├── HomePage.js
│   │       ├── ProductPage.js
│   │       ├── CartPage.js
│   │       └── ConfirmationPage.js
│   ├── downloads/                   # Auto-generated download files
│   ├── reports/                     # Auto-generated test reports
│   ├── screenshots/                 # Test failure screenshots
│   └── videos/                      # Test execution videos
├── cypress.config.js                # Main Cypress configuration
├── package.json                     # Dependencies and scripts
├── cucumber-html-report.js          # Cucumber report generator
└── README.md                        # This file
```

---

## ✨ Key Features {#key-features}

### 1. **Page Object Model (POM) Pattern**

- Separates page logic from test logic
- Reusable page classes for maintainability
- Easy to update when UI changes

### 2. **BDD with Cucumber/Gherkin**

- Human-readable test scenarios
- Collaboration between technical and non-technical team members
- Feature files with step definitions

### 3. **Custom Commands**

- Reusable test actions
- API login functionality
- Form submission helpers

### 4. **Database Integration**

- SQL Server connectivity
- Query execution from tests
- Data validation and verification

### 5. **Excel File Operations**

- Read Excel files for test data
- Write/modify Excel files
- Data-driven testing support

### 6. **API Testing**

- REST API calls
- Token-based authentication
- Session management

### 7. **File Upload/Download**

- Handle file downloads
- Upload files in tests
- Validate file contents

### 8. **Advanced Reporting**

- Mochawesome HTML reports
- Cucumber HTML reports
- Screenshots and videos on failure

---

## 📋 Prerequisites {#prerequisites}

Before you begin, ensure you have the following installed:

1. **Node.js** (v18.x.x or later)

   - Download from [nodejs.org](https://nodejs.org/)
   - Verify installation: `node --version`

2. **npm** (comes with Node.js)

   - Verify installation: `npm --version`

3. **nvm** (Node Version Manager) - Recommended

   - For managing multiple Node.js versions
   - Installation: [nvm.sh](https://github.com/nvm-sh/nvm)

4. **Git** (for cloning the repository)

   - Download from [git-scm.com](https://git-scm.com/)

5. **Code Editor** (Optional but recommended)
   - Visual Studio Code
   - WebStorm
   - Any IDE with JavaScript support

---

## 🚀 Installation & Setup {#installation-setup}

### Step 1: Clone the Repository

```bash
git clone <repository-url>
cd CypressAutomation
```

### Step 2: Install Node.js (if not already installed)

Using nvm (recommended):

```bash
nvm install 18
nvm use 18
```

Or download directly from [nodejs.org](https://nodejs.org/)

### Step 3: Install Dependencies

```bash
npm install
```

This will install all required packages listed in `package.json`:

- Cypress framework
- Cucumber preprocessor
- Reporting libraries
- Database and Excel utilities
- All other dependencies

### Step 4: Verify Cypress Installation

```bash
npx cypress verify
```

You should see: "Verified Cypress!"

---

## ⚙️ Environment Configuration {#environment-configuration}

### Understanding Environment Variables

Cypress uses environment variables for configuration. In this project, environment variables are defined in `cypress.config.js` and can be overridden using `.env` files or command-line arguments.

### Current Environment Variables

The project uses the following environment variables (defined in `cypress.config.js`):

```javascript
env: {
  url: "https://rahulshettyacademy.com",
}
```

### Setting Up Environment Variables

#### Option 1: Using cypress.config.js (Current Setup)

Environment variables are directly defined in `cypress.config.js`:

```javascript
module.exports = defineConfig({
  env: {
    url: "https://rahulshettyacademy.com",
    // Add more environment variables here
    apiUrl: "https://api.example.com",
    timeout: 10000,
  },
});
```

Access in tests:

```javascript
Cypress.env("url");
Cypress.env("apiUrl");
```

#### Option 2: Using .env File (Recommended for Sensitive Data)

1. **Create a `.env` file** in the project root:

```bash
touch .env
```

2. **Add your environment variables**:

```env
CYPRESS_BASE_URL=https://rahulshettyacademy.com
CYPRESS_API_URL=https://api.example.com
CYPRESS_DB_USERNAME=your_username
CYPRESS_DB_PASSWORD=your_password
CYPRESS_DB_SERVER=your_server.database.windows.net
CYPRESS_DB_NAME=your_database
```

3. **Install dotenv package** (if not already installed):

```bash
npm install --save-dev dotenv
```

4. **Update cypress.config.js** to load .env file:

```javascript
require("dotenv").config();

module.exports = defineConfig({
  env: {
    url: process.env.CYPRESS_BASE_URL || "https://rahulshettyacademy.com",
    apiUrl: process.env.CYPRESS_API_URL,
    db: {
      userName: process.env.CYPRESS_DB_USERNAME,
      password: process.env.CYPRESS_DB_PASSWORD,
      server: process.env.CYPRESS_DB_SERVER,
      database: process.env.CYPRESS_DB_NAME,
    },
  },
});
```

#### Option 3: Using Command Line

```bash
npx cypress run --env url=https://example.com,apiUrl=https://api.example.com
```

### Database Configuration

For SQL Server integration, configure database credentials in `cypress.config.js`:

```javascript
config.db = {
  userName: "your_username",
  password: "your_password",
  server: "your_server.database.windows.net",
  options: {
    database: "your_database",
    encrypt: true,
    rowCollectionOnRequestCompletion: true,
  },
};
```

> **⚠️ Security Note:** Never commit sensitive credentials (passwords, API keys) to version control. Use `.env` files and add `.env` to `.gitignore`.

### Required Environment Variables for This Project

| Variable             | Description                   | Default Value                    | Required           |
| -------------------- | ----------------------------- | -------------------------------- | ------------------ |
| `url`                | Base URL for the application  | `https://rahulshettyacademy.com` | Yes                |
| `token`              | API authentication token      | -                                | For API tests      |
| Database credentials | SQL Server connection details | -                                | For database tests |

---

## 🏃 How to Run Tests {#how-to-run-tests}

### Open Cypress Test Runner (Interactive GUI)

The Cypress Test Runner provides a visual interface to run and debug tests:

```bash
npx cypress open
```

This opens the Cypress GUI where you can:

- Select tests to run
- Watch tests execute in real-time
- Debug test failures
- View network requests and console logs

### Run All Tests (Headless Mode)

Run all tests in headless mode (no browser window):

```bash
npm run test
```

Or directly:

```bash
npx cypress run
```

### Run Tests in Headed Mode

Run tests with visible browser window:

```bash
npm run headTest
```

Or:

```bash
npx cypress run --headed
```

### Run Tests in Specific Browser

Run tests in Chrome:

```bash
npm run chromeTest
```

Or:

```bash
npx cypress run --browser chrome
```

Available browsers:

- `chrome`
- `firefox`
- `edge`
- `electron` (default)

### Run Specific Test Files

Run a specific test file:

```bash
npx cypress run --spec "cypress/integration/examples/Test8Framework.js"
```

Run all tests in a directory:

```bash
npx cypress run --spec "cypress/integration/GreenKart/*"
```

### Run GreenKart Test Suite

```bash
npm run GreenKartTest
```

### Run Smoke Tests

```bash
npm run SmokeTest
```

### Run with Dashboard Recording

Record test runs to Cypress Dashboard:

```bash
npm run recordDashBoardTest
```

> **Note:** You need a Cypress Dashboard account and project ID configured.

### Run with Custom Environment Variables

```bash
npx cypress run --env url=https://staging.example.com
```

---

## 📚 Understanding the Framework {#understanding-the-framework}

### What is Cypress?

Cypress is a modern end-to-end testing framework built for the modern web. It runs in the same run-loop as your application, providing native access to every DOM element.

**Key Advantages:**

- Fast execution
- Real browser testing
- Automatic waiting and retries
- Time-travel debugging
- Network request control
- Screenshot and video capture

### What is BDD (Behavior-Driven Development)?

BDD is a software development approach that encourages collaboration between developers, QA, and non-technical stakeholders. It uses natural language to describe software behavior.

**In this project:**

- **Gherkin** syntax is used to write feature files (`.feature`)
- **Cucumber** interprets Gherkin and executes step definitions
- Tests are written in plain English, making them readable by non-technical team members

**Example Feature File:**

```gherkin
Feature: End to end Ecommerce validation
  @Regression
  Scenario: Ecommerce products delivery
    Given I am on Ecommerce Page
    When I login to the application
    And I add items to Cart and checkout
    And Validate the total price limit
    Then select the country submit and verify Thankyou
```

### What is Mocha?

Mocha is a feature-rich JavaScript test framework running on Node.js. Cypress uses Mocha as its test runner.

**Mocha Test Structure:**

```javascript
describe("Test Suite Name", function () {
  it("Test Case Name", function () {
    // Test code here
  });
});
```

### What is Chai?

Chai is a BDD/TDD assertion library for Node.js. Cypress bundles Chai, so you can use assertions like:

```javascript
expect(value).to.equal(expected);
expect(value).to.be.true;
cy.get(".element").should("be.visible");
cy.get(".element").should("contain", "text");
```

### What is Page Object Model (POM)?

POM is a design pattern that creates an object repository for web UI elements. Each page has its own class with methods representing page actions.

**Benefits:**

- Code reusability
- Easy maintenance
- Separation of concerns
- Reduced code duplication

**Example:**

```javascript
// HomePage.js
class HomePage {
  goTo(url) {
    cy.visit(url);
  }

  login(username, password) {
    cy.get("#username").type(username);
    cy.get("#password").type(password);
    cy.contains("Sign In").click();
    return new ProductPage();
  }
}
```

---

## 🔍 Project Components Deep Dive {#project-components-deep-dive}

### 1. Custom Commands (`cypress/support/commands.js`)

Custom commands extend Cypress's built-in commands, making tests more readable and reusable.

**Example Custom Commands:**

```javascript
// Login via API
Cypress.Commands.add("LoginAPI", () => {
  cy.request("POST", "https://rahulshettyacademy.com/api/ecom/auth/login", {
    userEmail: "anshika@gmail.com",
    userPassword: "Iamking@000",
  }).then(function (response) {
    expect(response.status).to.eq(200);
    Cypress.env("token", response.body.token);
  });
});

// Form submission helper
Cypress.Commands.add("submitFormDetails", () => {
  cy.get("#country").type("India");
  cy.get(".suggestions ul li a").click();
  cy.get(".btn-success").click();
});
```

**Usage in Tests:**

```javascript
cy.LoginAPI();
cy.submitFormDetails();
```

### 2. Page Object Model Classes

#### HomePage (`cypress/support/pageObjects/HomePage.js`)

```javascript
import ProductPage from "../../support/pageObjects/ProductPage";

class HomePage {
  goTo(url) {
    cy.visit(url);
  }

  login(username, password) {
    cy.get("#username").type(username);
    cy.get("#password").type(password);
    cy.contains("Sign In").click();
    return new ProductPage();
  }
}

export default HomePage;
```

#### ProductPage (`cypress/support/pageObjects/ProductPage.js`)

```javascript
import CartPage from "../../support/pageObjects/CartPage";

class ProductPage {
  pageValidation() {
    cy.contains("Shop Name").should("be.visible");
  }

  getCardCount() {
    return cy.get("app-card");
  }

  selectFirstProduct() {
    cy.get("app-card").eq(0).contains("button", "Add").click();
  }

  goToCart() {
    cy.contains("a", "Checkout").click();
    return new CartPage();
  }

  selectProduct(productName) {
    cy.get("app-card")
      .filter(`:contains("${productName}")`)
      .then(($element) => {
        cy.wrap($element).should("have.length", 1);
        cy.wrap($element).contains("button", "Add").click();
      });
  }
}

export default ProductPage;
```

#### CartPage (`cypress/support/pageObjects/CartPage.js`)

```javascript
import ConfirmationPage from "../../support/pageObjects/ConfirmationPage";

class CartPage {
  checkoutItems() {
    cy.contains("button", "Checkout").click();
    return new ConfirmationPage();
  }

  sumOfProducts() {
    let sum = 0;
    return cy
      .get("tr td:nth-child(4) strong")
      .each(($e1) => {
        const amount = Number($e1.text().split(" ")[1].trim());
        sum = sum + amount;
      })
      .then(() => {
        return sum;
      });
  }
}

export default CartPage;
```

#### ConfirmationPage (`cypress/support/pageObjects/ConfirmationPage.js`)

```javascript
class ConfirmationPage {
  submitFormDetails() {
    cy.get("#country").type("India");
    cy.get(".suggestions ul li a").click();
    cy.get(".btn-success").click();
  }

  getAlertMessage() {
    return cy.get(".alert-success");
  }
}

export default ConfirmationPage;
```

### 3. Cypress Configuration (`cypress.config.js`)

The configuration file sets up:

- Base URL
- Test file patterns
- Custom tasks (Node.js functions)
- Database connections
- Reporters
- Retry logic

**Key Configuration:**

```javascript
module.exports = defineConfig({
  defaultCommandTimeout: 6000,
  env: {
    url: "https://rahulshettyacademy.com",
  },
  reporter: "cypress-mochawesome-reporter",
  retries: {
    runMode: 1,
  },
  e2e: {
    setupNodeEvents,
    specPattern: "cypress/integration/examples/*.js",
  },
});
```

### 4. Custom Tasks (Node.js Functions)

Tasks allow you to run Node.js code from Cypress tests. They're defined in `cypress.config.js`:

**Excel to JSON Converter:**

```javascript
on("task", {
  excelToJsonConverter(filePath) {
    const result = excelToJson({
      source: fs.readFileSync(filePath),
    });
    return result;
  },
});
```

**Excel Writer:**

```javascript
on("task", {
  async writeExcelTest({ searchText, replaceText, change, filePath }) {
    const workbook = new ExcelJs.Workbook();
    await workbook.xlsx.readFile(filePath);
    const worksheet = workbook.getWorksheet("Sheet1");
    const output = await readExcel(worksheet, searchText);

    const cell = worksheet.getCell(
      output.row,
      output.column + change.colChange
    );
    cell.value = replaceText;

    return workbook.xlsx
      .writeFile(filePath)
      .then(() => {
        return true;
      })
      .catch((error) => {
        return false;
      });
  },
});
```

**Database Tasks:**

```javascript
tasks = sqlServer.loadDBPlugin(config.db);
on("task", tasks);
```

**Usage in Tests:**

```javascript
cy.task("excelToJsonConverter", "path/to/file.xlsx").then((data) => {
  // Use Excel data
});

cy.task("writeExcelTest", {
  searchText: "Mango",
  replaceText: 450,
  change: { rowChange: 0, colChange: 2 },
  filePath: "path/to/file.xlsx",
});

cy.sqlServer("SELECT * FROM Person").then(function (result) {
  console.log(result);
});
```

### 5. Fixtures (Test Data)

Fixtures are static data files stored in `cypress/fixtures/`. They're perfect for test data that doesn't change.

**Example Fixture (`cypress/fixtures/example.json`):**

```json
{
  "username": "rahulshettyacademy",
  "password": "learning",
  "productName": "Nokia Edge"
}
```

**Usage in Tests:**

```javascript
cy.fixture("example").then(function (data) {
  this.data = data;
  // Use this.data.username, this.data.password, etc.
});
```

---

## 💡 Test Examples & Use Cases {#test-examples-use-cases}

### Example 1: Basic UI Test (GreenKart)

**File:** `cypress/integration/GreenKart/Test1.js`

```javascript
describe("My First Test Suite", function () {
  it("My FirstTest case", function () {
    cy.visit("https://rahulshettyacademy.com/seleniumPractise/#/");
    cy.get(".search-keyword").type("ca");
    cy.wait(2000);

    // Assertions
    cy.get(".product").should("have.length", 5);
    cy.get(".product:visible").should("have.length", 4);

    // Parent-child chaining
    cy.get(".products").as("productLocator");
    cy.get("@productLocator").find(".product").should("have.length", 4);

    // Click specific product
    cy.get(":nth-child(3) > .product-action > button").click();

    // Iterate through products
    cy.get("@productLocator")
      .find(".product")
      .each(($el, index, $list) => {
        const textVeg = $el.find("h4.product-name").text();
        if (textVeg.includes("Cashews")) {
          $el.find("button").click();
        }
      });

    // Assert logo text
    cy.get(".brand").should("have.text", "GREENKART");
  });
});
```

**Key Concepts:**

- Element selection with `cy.get()`
- Aliases with `.as()`
- Iteration with `.each()`
- Assertions with `.should()`

### Example 2: Page Object Model Test

**File:** `cypress/integration/examples/Test8Framework.js`

```javascript
import HomePage from "../../support/pageObjects/HomePage";

describe("End to End ecommerce Test", function () {
  before(function () {
    // Runs once before all tests
    cy.fixture("example").then(function (data) {
      this.data = data;
      this.homepage = new HomePage();
    });
  });

  it("Submit Order", function () {
    const productName = this.data.productName;

    this.homepage.goTo(Cypress.env("url") + "/loginpagePractise/");
    const productPage = this.homepage.login(
      this.data.username,
      this.data.password
    );

    productPage.pageValidation();
    productPage.getCardCount().should("have.length", 4);
    productPage.selectProduct(productName);
    productPage.selectFirstProduct();

    const cartPage = productPage.goToCart();
    cartPage.sumOfProducts().then(function (sum) {
      expect(sum).to.be.lessThan(200000);
    });

    const confirmationPage = cartPage.checkoutItems();
    confirmationPage.submitFormDetails();
    confirmationPage.getAlertMessage().should("contain", "Success");
  });
});
```

**Key Concepts:**

- Page Object Model pattern
- Fixture data usage
- Test hooks (`before`)
- Chaining page objects

### Example 3: BDD with Cucumber

**Feature File:** `cypress/integration/examples/BDD/ecommerce.feature`

```gherkin
Feature: End to end Ecommerce validation
  @Regression
  Scenario: Ecommerce products delivery
    Given I am on Ecommerce Page
    When I login to the application
    And I add items to Cart and checkout
    And Validate the total price limit
    Then select the country submit and verify Thankyou

  @Smoke
  Scenario Outline: Ecommerce products delivery cucumber driven
    Given I am on Ecommerce Page
    When I login to the application portal
      | username             | password |
      | rahulshettyacademy   | learning |
    And I add items to Cart and checkout
    And Validate the total price limit
    Then select the country submit and verify Thankyou
```

**Step Definitions:** `cypress/integration/examples/BDD/ecommerce/eCommStepDef.js`

```javascript
import { Given, When, Then } from "@badeball/cypress-cucumber-preprocessor";
import HomePage from "../../../../support/pageObjects/HomePage";

const homePage = new HomePage();

Given("I am on Ecommerce Page", () => {
  homePage.goTo(Cypress.env("url") + "/loginpagePractise/");
});

When("I login to the application", function () {
  this.productPage = homePage.login(this.data.username, this.data.password);
  this.productPage.pageValidation();
  this.productPage.getCardCount().should("have.length", 4);
});

When("I add items to Cart and checkout", function () {
  this.productPage.selectProduct(this.data.productName);
  this.productPage.selectFirstProduct();
  this.cartPage = this.productPage.goToCart();
});

When("Validate the total price limit", function () {
  this.cartPage.sumOfProducts().then(function (sum) {
    expect(sum).to.be.lessThan(200000);
  });
});

Then("select the country submit and verify Thankyou", function () {
  const confirmationPage = this.cartPage.checkoutItems();
  confirmationPage.submitFormDetails();
  confirmationPage.getAlertMessage().should("contain", "Success");
});
```

**Key Concepts:**

- Gherkin syntax (Given, When, Then, And)
- Step definitions mapping
- Data tables
- Scenario outlines

### Example 4: Database Integration

**File:** `cypress/integration/examples/sqldb.js`

```javascript
describe("My Second Test Suite", function () {
  it("My FirstTest case", function () {
    cy.log("hello");
    cy.sqlServer("select * from Person").then(function (result) {
      console.log(result[0][1]);
    });
  });
});
```

**Key Concepts:**

- SQL Server connectivity
- Query execution from tests
- Data validation

### Example 5: Excel File Handling

**File:** `cypress/integration/examples/Excel_Task_validations.js`

```javascript
describe("JWT Session", () => {
  it("is logged in through local storage", async () => {
    cy.LoginAPI().then(function () {
      cy.visit("https://rahulshettyacademy.com/client", {
        onBeforeLoad: function (window) {
          window.localStorage.setItem("token", Cypress.env("token"));
        },
      });
    });

    // Get product name
    cy.get(".card-body b")
      .eq(1)
      .then(function (ele) {
        productName = ele.text();
      });

    // Add to cart and checkout
    cy.get(".card-body button:last-of-type").eq(1).click();
    cy.get("[routerlink*='cart']").click();
    cy.contains("Checkout").click();

    // Select country
    cy.get("[placeholder*='Country']").type("ind");
    cy.get(".ta-results button").each(($e1, index, $list) => {
      if ($e1.text() === " India") {
        cy.wrap($e1).click();
      }
    });

    cy.get(".action__submit").click();
    cy.wait(2000);

    // Download Excel file
    cy.get(".order-summary button").contains("Excel").click();
    const filePath =
      Cypress.config("fileServerFolder") +
      "/cypress/downloads/order-invoice_anshika.xlsx";

    // Convert Excel to JSON and validate
    cy.task("excelToJsonConverter", filePath).then(function (result) {
      cy.log(result.data[1].A);
      expect(productName).to.equal(result.data[1].B);
    });

    // Read file content
    cy.readFile(filePath).then(function (text) {
      expect(text).to.include("ADIDAS ORIGINAL");
    });
  });
});
```

**Key Concepts:**

- API authentication
- Local storage manipulation
- File download handling
- Excel to JSON conversion
- File content validation

### Example 6: File Upload/Download

**File:** `cypress/integration/examples/upload-download.js`

```javascript
describe("Upload-download test", () => {
  it("verify excel upload download", () => {
    const replaceNum = 450;
    const searchTextFruit = "Mango";
    const FilePath =
      Cypress.config("fileServerFolder") + "/cypress/downloads/download.xlsx";

    cy.visit("https://rahulshettyacademy.com/upload-download-test/index.html");
    cy.get("#downloadButton").click();

    // Modify Excel file
    cy.task("writeExcelTest", {
      searchText: searchTextFruit,
      replaceText: replaceNum,
      change: { rowChange: 0, colChange: 2 },
      filePath: FilePath,
    });

    // Upload modified file
    cy.get("#fileinput").selectFile(FilePath);

    // Verify changes
    cy.contains(searchTextFruit)
      .parent()
      .parent()
      .find("#cell-4-undefined")
      .should("have.text", replaceNum);
  });
});
```

**Key Concepts:**

- File download
- Excel file modification
- File upload
- Content validation

### Example 7: Iframe Handling

**File:** `cypress/integration/examples/sampleTest.js`

```javascript
import "cypress-iframe";

describe("Iframe Test", () => {
  it("Test 6th", () => {
    cy.visit("https://rahulshettyacademy.com/AutomationPractice/");
    cy.frameLoaded("#courses-iframe");

    // Interact with iframe elements
    cy.iframe().find("li.dropdown").eq(1).invoke("show");
    cy.iframe().contains("Part time jobs").click({ force: true });
    cy.wait(2000);
    cy.iframe().find('select[name="select-jpb-type"]').select("Freelancing");
  });
});
```

**Key Concepts:**

- Iframe detection
- Interacting with iframe content
- Force actions

---

## 🔄 Reusing Components in Other Projects {#reusing-components-in-other-projects}

### 1. Copy Page Object Classes

Copy the entire `cypress/support/pageObjects/` directory to your new project and adapt the selectors and methods to your application.

**Steps:**

1. Copy `pageObjects/` folder
2. Update selectors in each class
3. Modify methods as needed
4. Import and use in your tests

### 2. Reuse Custom Commands

Copy `cypress/support/commands.js` and adapt the commands to your needs.

**Example Adaptation:**

```javascript
// Original
Cypress.Commands.add("LoginAPI", () => {
  cy.request("POST", "https://rahulshettyacademy.com/api/ecom/auth/login", {
    userEmail: "anshika@gmail.com",
    userPassword: "Iamking@000",
  }).then(function (response) {
    expect(response.status).to.eq(200);
    Cypress.env("token", response.body.token);
  });
});

// Adapted for your project
Cypress.Commands.add("LoginAPI", (email, password) => {
  cy.request("POST", Cypress.env("apiUrl") + "/auth/login", {
    userEmail: email,
    userPassword: password,
  }).then(function (response) {
    expect(response.status).to.eq(200);
    Cypress.env("token", response.body.token);
  });
});
```

### 3. Reuse Custom Tasks

Copy the task definitions from `cypress.config.js` to your new project's config file.

**Reusable Tasks:**

- Excel to JSON converter
- Excel writer
- Database tasks (with your credentials)

### 4. Reuse BDD Step Definitions

Copy the BDD structure:

1. Copy feature files and adapt scenarios
2. Copy step definitions and update selectors
3. Ensure Cucumber preprocessor is configured

### 5. Reuse Configuration Patterns

Copy relevant parts of `cypress.config.js`:

- Custom tasks
- Reporter configuration
- Retry logic
- Environment variables structure

### 6. Create a Template Project

Create a reusable template with:

- Folder structure
- Base page objects
- Common custom commands
- Configuration templates
- Example tests

---

## 📊 Reporting {#reporting}

### Mochawesome Reports

Mochawesome generates beautiful HTML reports with:

- Test execution summary
- Pass/fail statistics
- Screenshots on failure
- Execution time
- Test details

**Configuration:**

```javascript
// cypress.config.js
reporter: 'cypress-mochawesome-reporter',
```

**Generate Report:**

Reports are automatically generated after test runs in `cypress/reports/` directory.

**View Report:**

Open `cypress/reports/html/index.html` in a browser.

### Cucumber HTML Reports

Cucumber reports provide Gherkin-based HTML reports with:

- Feature file execution
- Scenario results
- Step definitions mapping
- Tags and metadata

**Configuration:**

```javascript
// package.json
"cypress-cucumber-preprocessor": {
  "json": {
    "enabled": true,
    "output": "cypress/cucumberReports/results.json"
  }
}
```

**Generate Report:**

Run the report generator:

```bash
node cucumber-html-report.js
```

**View Report:**

Open the generated HTML file in `cypress/CucumberReports/`.

### Screenshots and Videos

Cypress automatically captures:

- **Screenshots**: On test failures (stored in `cypress/screenshots/`)
- **Videos**: Complete test execution (stored in `cypress/videos/`)

**Configuration:**

```javascript
// cypress.config.js
screenshotOnRunFailure: true,
video: true,
```

---

## 🔧 Troubleshooting {#troubleshooting}

### Common Issues & Solutions

#### 1. **Missing Dependencies**

**Error:** `Cannot find module 'cypress'`

**Solution:**

```bash
npm install
```

#### 2. **Incorrect Node.js Version**

**Error:** Compatibility issues

**Solution:**

```bash
nvm use 18
# or
nvm install 18 && nvm use 18
```

#### 3. **Syntax Errors**

**Error:** Test file syntax errors

**Solution:**

- Check for typos in test files
- Verify all imports are correct
- Ensure proper closing of brackets and parentheses
- Use a code editor with JavaScript/TypeScript support

#### 4. **File Not Found Errors**

**Error:** `Cannot find file` or `Path does not exist`

**Solution:**

- Double-check file paths in configuration
- Verify fixture files exist in `cypress/fixtures/`
- Check import paths are relative to the test file

#### 5. **"fs" Module Error on Mac**

**Error:** `fs is not defined` in browser test files

**Solution:**

- Only use Node's `fs` module inside Cypress plugins or support files
- Use `cy.task()` in your tests to interact with files via Node context

**Example: Using `fs` in plugins**

```javascript
// cypress/plugins/index.js
const fs = require("fs");
module.exports = (on, config) => {
  on("task", {
    readFile(filePath) {
      return fs.readFileSync(filePath, "utf8");
    },
  });
};
```

**Example: Using `cy.task()` in tests**

```javascript
it("Reads a file using cy.task()", () => {
  cy.task("readFile", "cypress/fixtures/sample.json").then((content) => {
    cy.log(content);
  });
});
```

#### 6. **Database Connection Errors**

**Error:** SQL Server connection failures

**Solution:**

- Verify database credentials in `cypress.config.js`
- Check network connectivity
- Ensure database server allows connections
- Verify firewall rules

#### 7. **Excel File Errors**

**Error:** Excel file read/write failures

**Solution:**

- Verify file paths are correct
- Check file permissions
- Ensure Excel file is not open in another application
- Verify file format is `.xlsx`

#### 8. **Cucumber Step Definition Not Found**

**Error:** `Step definition not found`

**Solution:**

- Verify step definition file is in the correct location
- Check step definition syntax matches feature file
- Ensure Cucumber preprocessor is configured correctly
- Verify step definition file is imported

#### 9. **Element Not Found / Timeout Errors**

**Error:** `Timed out retrying: Expected to find element`

**Solution:**

- Verify selectors are correct
- Add appropriate waits if elements load dynamically
- Check if element is in an iframe (use iframe commands)
- Verify element is visible (not hidden by CSS)

#### 10. **Environment Variable Not Found**

**Error:** `Cypress.env('variable')` returns undefined

**Solution:**

- Verify environment variable is defined in `cypress.config.js`
- Check `.env` file exists and is loaded (if using dotenv)
- Verify variable name spelling
- Use default values: `Cypress.env('url') || 'default-url'`

---

## 🏷 Keywords {#keywords}

**Testing Frameworks:**

- Cypress, E2E Testing, UI Testing, Automation Testing, Test Automation

**BDD & Testing Patterns:**

- Behavior-Driven Development, BDD, Cucumber, Gherkin, Page Object Model, POM

**Programming & Tools:**

- JavaScript, Node.js, Mocha, Chai, npm, nvm

**Integration & Reporting:**

- SQL Server, Database Integration, Excel Automation, API Testing, Test Reporting, Mochawesome, Cucumber Reports

**CI/CD & DevOps:**

- Continuous Integration, CI/CD, Cypress Dashboard, Headless Testing, Test Execution

**Project-Specific:**

- GreenKart, Rahul Shetty Academy, RSA, Test Data, Fixtures, Custom Commands, Test Suites

---

## 🎓 Conclusion {#conclusion}

This Cypress automation project serves as a comprehensive learning resource for mastering end-to-end test automation. It demonstrates:

✅ **Modern Testing Practices**: Page Object Model, BDD, and reusable test patterns

✅ **Real-World Scenarios**: Database integration, Excel handling, API testing, file operations

✅ **Professional Setup**: Custom commands, tasks, reporting, and configuration management

✅ **Educational Value**: Well-documented code with examples for beginners and advanced users

### Key Takeaways

1. **Cypress** provides a powerful, developer-friendly testing framework
2. **BDD** with Cucumber makes tests readable and maintainable
3. **Page Object Model** improves code reusability and maintenance
4. **Custom commands and tasks** extend Cypress capabilities
5. **Proper configuration** is essential for scalable test automation

### Next Steps

- Explore the test examples in `cypress/integration/examples/`
- Modify tests to practice different scenarios
- Create your own page objects and custom commands
- Integrate with your own applications
- Set up CI/CD pipelines
- Contribute improvements to this project

### Learning Resources

- [Cypress Documentation](https://docs.cypress.io/)
- [Cucumber Documentation](https://cucumber.io/docs/)
- [Mocha Documentation](https://mochajs.org/)
- [Chai Assertions](https://www.chaijs.com/api/bdd/)

---

## Happy Coding! 🎉

Feel free to use this project repository and extend this project further!

If you have any questions or want to share your work, reach out via GitHub or my portfolio at [https://arnob-mahmud.vercel.app/](https://arnob-mahmud.vercel.app/).

**Enjoy building and learning!** 🚀

Thank you! 😊

---
