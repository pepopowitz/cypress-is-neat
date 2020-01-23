---
Layout: module

# Cypress

Fast, easy and reliable testing for anything that runs in a browser.

[cypress.io](https://cypress.io)

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

Trail: Cypress

## Setup

### **`npm install cypress`**

Notes:

that's really it.

If you're not familiar with npm, it's the "node package manager", which is how modern JS projects manage their dependencies.

This command is telling a js project to pull down the latest version of cypress, and add it to the project manifest so that it works on everyone's machine.

The installation of cypress itself is really this simple - one line in a terminal. 

Depending on your org, *using npm* might be significantly more difficult than getting cypress running.

---

Trail: Cypress

## Example

todo: gif of searching from homepage

Notes:

build a test for searching from homepage

---

Trail: Cypress, Example
LineNumbers: 1,2

## Syntax of a test

```javascript
describe("searching", () => {
  it("searches for an artist", () => {





    // your test goes here!






  })
})
```

Notes:

- describe = "namespace"
- fat arrow functions
- describe can be nested
- it = test

---

Trail: Cypress, Example
LineNumbers: 3,4

## cy.visit

```javascript
describe("searching", () => {
  it("searches for an artist", () => {
    cy.visit("/") 
    // ^^^ browse to the root of our site










  })
})
```

---
Trail: Cypress, Example
LineNumbers: 5,6

## cy.contains

```javascript
describe("searching", () => {
  it("searches for an artist", () => {
    cy.visit("/")

    cy.contains("Learn about and collect art")
    // ^^^ Find an element containing specific text









  })
})
```

Notes:

- you'll probably want to look for more specific data than this
- automatic waiting! (up to 5 seconds by default)

---
Trail: Cypress, Example
LineNumbers: 7,8

## cy.get

```javascript
describe("searching", () => {
  it("searches for an artist", () => {
    cy.visit("/")

    cy.contains("Learn about and collect art")

    cy.get('[placeholder="Search"]')
    // ^^^ Find an element by CSS selector






  })
})
```

---

Trail: Cypress, Example
LineNumbers: 8,9

## click

```javascript
describe("searching", () => {
  it("searches for an artist", () => {
    cy.visit("/")

    cy.contains("Learn about and collect art")

    cy.get('[placeholder="Search"]')
      .click()
      // ^^^ click on the matching element





  })
})
```

---
Trail: Cypress, Example
LineNumbers: 9,10

## type

```javascript
describe("searching", () => {
  it("searches for an artist", () => {
    cy.visit("/")

    cy.contains("Learn about and collect art")

    cy.get('[placeholder="Search"]')
      .click()
      .type("goldsworthy")
      // ^^^ type into the focused element




  })
})
```

---
Trail: Cypress, Example
LineNumbers: 11,12

## cy.contains, click

```javascript
describe("searching", () => {
  it("searches for an artist", () => {
    cy.visit("/")

    cy.contains("Learn about and collect art")

    cy.get('[placeholder="Search"]')
      .click()
      .type("goldsworthy")

    cy.contains("Andy Goldsworthy").click()
    // ^^^ find a search result and click on it


  })
})
```

---
Trail: Cypress, Example
LineNumbers: 13,14

## cy.url

```javascript
describe("searching", () => {
  it("searches for an artist", () => {
    cy.visit("/")

    cy.contains("Learn about and collect art")

    cy.get('[placeholder="Search"]')
      .click()
      .type("goldsworthy")

    cy.contains("Andy Goldsworthy").click()

    cy.url().should("contain", "andy-goldsworthy")
    // ^^^ verify the navigated URL
  })
})
```

---
Trail: Cypress, Example
LineNumbers: 14

## cy.contains

```javascript
describe("searching", () => {
  it("searches for an artist", () => {
    cy.visit("/")

    cy.contains("Learn about and collect art")

    cy.get('[placeholder="Search"]')
      .click()
      .type("goldsworthy")

    cy.contains("Andy Goldsworthy").click()

    cy.url().should("contain", "andy-goldsworthy")
    cy.contains("Andy Goldsworthy creates outdoor sculpture")
  })
})
```

---
Trail: Cypress, Example

# Demo!

Notes:

---

Trail: Cypress, Example

## commands (cy.customName)

---

* mocking

  - you can mock network responses easily
    - https://docs.cypress.io/api/commands/server.html#Syntax
    - but you probably don't want to - that just gives you a less reliable test.
