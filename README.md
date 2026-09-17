# QA Automation – Employee Lifecycle Management

## 📌 Project Overview

This project is an end-to-end UI and API automation framework developed as part of the **Quality Engineer (Automation) Technical Assessment**.

The framework automates the complete **Employee Lifecycle Management** workflow using:

* Playwright
* TypeScript
* Playwright Test
* Page Object Model (POM)
* API validation
* Data-driven testing
* HTML reporting
* Test execution video recording

The test scenario covers employee creation, employee information update, API validation, employee deletion, and logout.

---

## 🎯 Objective

The objective of this automation framework is to validate the Employee Lifecycle Management functionality of the OrangeHRM application while demonstrating:

* Maintainable automation framework design
* Page Object Model implementation
* Reusable methods
* Data-driven testing
* UI validations
* API validations
* Meaningful assertions
* Test reporting
* Test execution evidence

---

## 🌐 Application Under Test

**Application:** OrangeHRM Demo

**URL:**

https://opensource-demo.orangehrmlive.com/

### Test Credentials

```text
Username: Admin
Password: admin123
```

---

## 🧪 Automated Test Scenario

The framework automates the following end-to-end workflow.

### 1. Login

* Navigate to the OrangeHRM application.
* Enter valid username and password.
* Click Login.
* Verify successful login by validating the dashboard.

### 2. Add New Employee

* Navigate to **PIM → Add Employee**.
* Create a new employee using data-driven test data.
* Enter:

  * First Name
  * Last Name
  * Employee ID
* Upload a profile picture.
* Save the employee.
* Verify that the employee record is created successfully.

### 3. Edit Employee Information

* Search for the newly created employee using Employee ID.
* Open the employee profile.
* Update:

  * Job Title
  * Employment Status
* Save the changes.
* Verify that the updated information is displayed correctly.

### 4. API Validation

* Validate employee information using API requests.
* Compare API response data with the information displayed in the UI.
* Verify data consistency between UI and API.

### 5. Delete Employee

* Search for the created employee.
* Delete the employee.
* Verify that the employee is no longer available in the UI.
* Validate the deletion through API where applicable.

### 6. Logout

* Click the Logout option.
* Verify that the user is successfully logged out.
* Verify that the authenticated session is no longer accessible.

---

# 🏗️ Framework Architecture

The framework follows the **Page Object Model (POM)** design pattern.

```text
QA-Automation-Project
│
├── tests/
│   └── employeeLifecycle.spec.ts
│
├── pages/
│   ├── LoginPage.ts
│   ├── DashboardPage.ts
│   ├── PIMPage.ts
│   ├── AddEmployeePage.ts
│   └── EmployeeDetailsPage.ts
│
├── test-data/
│   └── employeeData.json
│
├── utils/
│   └── testDataUtils.ts
│
├── api/
│   └── employeeApi.ts
│
├── uploads/
│   └── profile-picture.jpg
│
├── playwright-report/
│
├── test-results/
│
├── EnvironmentConfig/
│   └── .env.qa
│
├── playwright.config.ts
├── package.json
├── package-lock.json
└── README.md
```

---

# 🧩 Page Object Model

Each application page is represented by a separate Page Object class.

### Example

```text
LoginPage
     ↓
DashboardPage
     ↓
PIMPage
     ↓
AddEmployeePage
     ↓
EmployeeDetailsPage
```

The Page Object Model helps to:

* Avoid duplicate locators
* Improve code maintainability
* Reuse common methods
* Separate test logic from page interaction
* Make test cases easier to understand

---

# 📂 Test Data

Employee information is maintained separately from the test script.

Example:

```json
{
  "firstName": "John",
  "lastName": "Automation",
  "employeeId": "EMP1001",
  "jobTitle": "QA Engineer",
  "employmentStatus": "Full-Time Permanent"
}
```

Keeping test data separate allows the same test flow to be executed with different employee information.

---

# ⚙️ Prerequisites

Before running t
