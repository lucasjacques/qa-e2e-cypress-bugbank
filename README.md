<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/lucasjacques/qa-e2e-cypress-bugbank/">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center"></h3>

# Lucas Jacques' E2E Automation with Cypress

This project contains End-to-End automated tests using Cypress to validate key flows of the BugBank application.

---

## 📌 Automated Scenarios

- ✅ Successful user registration  
- ✅ Login attempt with invalid credentials  

---

## ⚙️ Prerequisites

- Node.js (version 16+ recommended)  
- bun or npm or yarn  

---

## 🚀 Setup

Install dependencies:

```bash
bun install
```

---

## ▶️ Running the tests

### Interactive mode (GUI)

```bash
bunx cypress open
```

- Select **E2E Testing**
- Choose a browser (e.g., Chrome)
- Run the `.cy.js` test files

---

### Headless mode (terminal)

```bash
bunx cypress run
```

---

## 📁 Project structure

```bash
cypress/
  e2e/
    bugbank/
      login.cy.js
      register.cy.js
  support/
    commands.js
cypress.config.js
package.json
```

---

## 🧠 Technical approach

- Use of **custom commands** for reusability (`fillLogin`, `fillRegister`)
- Dynamic test data to avoid registration conflicts
- Independent and isolated test scenarios
- Selectors based on attributes (`name`, `contains`)

---

## ⚠️ Application notes

The application uses CSS transitions (transform/rotate/backface), keeping multiple elements in the DOM simultaneously.

To ensure test stability, the following strategies were applied:

- Scoped element selection using `.within()`
- Use of `{ force: true }` for interactions affected by animations
- Cypress implicit waits (`should('be.visible')`)

---

## 📦 Installation Summary

```bash
# Install dependencies
bun install

# Run tests (GUI)
bunx cypress open

# Run tests (headless)
bunx cypress run
```

---

## 💡 Notes

- Tests were designed to be simple, readable, and maintainable.
- The focus was on demonstrating E2E automation structure and handling real-world UI challenges.