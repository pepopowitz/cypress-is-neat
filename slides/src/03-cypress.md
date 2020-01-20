---
Layout: module

# Cypress

Fast, easy and reliable testing for anything that runs in a browser.

---

  - architecture
    - built on mocha
    - something about chrome/electron
      - the browser itself is executing your tests
        - which makes it faster than selenium
        - tight feedback loop
        - allows you to easily intercept/mock network activity
    - NOT built on selenium

---

  - ide
    - time traveling

---

  - vs selenium
    - > Most end-to-end testing tools are Selenium-based, which is why they all share the same problems. To make Cypress different, we built a new architecture from the ground up. Whereas Selenium executes remote commands through the network, Cypress runs in the same run-loop as your application.
      - https://www.cypress.io/how-it-works/
    - automatically waits :)
    - file watching to trigger execution :)
    - debugging within chrome :)
    - not cross-browser :(
      https://github.com/cypress-io/cypress/issues/310

  v javascript only
    selenium supports many languages
  v chrome only
    selenium supports many
  ^ quick setup
  ^ runs directly in the browser
    selenium has layers between your code & the browser
    you can inspect things in your console!
  ^ fast
    fewer layers
  ^ reliable
    fewer layers
    less waiting - it automatically waits for you.
  ^ interactive
    time travelling
  ^ server mocking
    maybe you don't want this

---

* examples

  - cy.visit
  - cy.get
  - cy.contains

---

* mocking

  - you can mock network responses easily
    - https://docs.cypress.io/api/commands/server.html#Syntax
    - but you probably don't want to - that just gives you a less reliable test.
