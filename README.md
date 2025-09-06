# Janitri QA Internship Assignment — Login Page Automation (Java + Selenium + POM + TestNG)

This repository contains an example automation framework for the **Janitri Dashboard Login Page**.

> **Test URL:** https://dev-dash.janitri.in/

## Tech Stack
- Java 17
- Selenium 4
- TestNG
- Maven
- WebDriverManager (for managing the browser driver)

## Project Structure
```
janitri-qa-automation
├── pom.xml
├── src
│   ├── main
│   │   └── java
│   │       └── in
│   │           └── janitri
│   │               └── pages
│   │                   └── LoginPage.java
│   └── test
│       ├── java
│       │   └── in
│       │       └── janitri
│       │           ├── tests
│       │           │   └── LoginTests.java
│       │           └── utils
│       │               └── BaseTest.java
│       └── resources
│           └── testng.xml
└── README.md
```

## Getting Started
1. **Install Java 17** and **Maven 3.9+**
2. Clone or download this project
3. Run tests:
   ```bash
   mvn clean test
   ```

## Handling Notifications Permission
The `BaseTest` configures Chrome to **allow notifications** via Chrome preferences. Adjust if needed.

## Update Locators
The current locators in `LoginPage.java` are **educated guesses**. Inspect the page (F12 DevTools) and update:
- `userIdInput`
- `passwordInput`
- `loginButton`
- `eyeToggle`
- `errorMessage`

## Test Cases Implemented
- `testUIElementsPresent`
- `testLoginButtonDisabledWhenFieldAreEmpty`
- `testPasswordMaskedbutton`
- `testInvalidLoginShowErrorMsg`
- `testBlankFieldsBehavior`

## Notes
- Do **not** include valid credentials.
- For CI runs or headless mode, add `options.addArguments("--headless=new");` in `BaseTest`.
