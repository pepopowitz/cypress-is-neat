---
Layout: module

# Cypress

Fast, easy and reliable testing for anything that runs in a browser.

[cypress.io](https://cypress.io)

Notes:

(definition on next slide)

---

Trail: Cypress

> All-in-one testing framework, assertion library, with mocking and stubbing, all without Selenium.

[cypress.io](https://cypress.io)

---

Trail: Cypress

> Cypress focuses on doing **end-to-end** testing REALLY well.

[cypress.io](https://cypress.io)

Notes:

not unit, not integration
 
---

Footer: false
<!-- .slide: data-background-video="/images/running-tests.webm" data-background-size="contain" -->

Notes:

what it looks like

We'll look at an actual running test later

left panel: every single event in browser

right panel: your app

---

Trail: Cypress, Architecture

## It's not Selenium

Notes:

kind of a joke but also not really

many e2e tools _are_, under the covers

---
<!-- .slide: data-background="/images/architecture-selenium.jpg" -->

Trail: Cypress, Architecture, Selenium

Notes:

the cypress team goes out of their way to compare the architectures of cypress & selenium

---
<!-- .slide: data-background="/images/architecture-cypress.jpg" -->

Trail: Cypress, Architecture, Cypress

Notes:

executed in the same run loop as your app

so it can interact with your app & all events in your app, 

including all network activity

also makes it **faster** because the communication is more direct

---

Trail: Cypress, Architecture

## It's **JavaScript**
### and so are the tests you write

Notes:

selling point? not sure.

Selenium supports many languages

---

Trail: Cypress, Architecture

## It's somewhat **cross-browser**
### Chrome, Edge, & Firefox

Notes:

Safari & IE are "under consideration"

so let's get that out of the way

this might be a dealbreaker for you

but it might also mean you can use Cypress for most tests, and another tool for cross-browser testing

---

Trail: Cypress, Features

## Tests automatically wait

### so they're more **reliable**

Notes:

up to 4.5 seconds

if you look for an element and it's not there because React is still rendering,

you have up to 4.5 seconds before the test fails

...

flake!

anyone experience e2e tests that fail because of timing issues?

---

Trail: Cypress, Features

## Tests run when files update *****

### tightening your **feedback loop**

Notes:

When you're running the tests locally, 

Asterisk: when the _test_ files update.

---

Trail: Cypress, Features

## You can time travel through tests

### for **easier debugging**

Notes: 

successful or failing

Cypress logs every event along the way

...

debug using the chrome dev tools at any point in your test

---

Trail: Cypress, Features

## Cypress runs in your browser

### making your tests **fast \***

Notes:

relatively. it's still e2e, so db, network latency, etc.

- fewer layers between your code & the browser

---

Trail: Cypress, Features

## You have access to all network activity

### so you can **inspect** it or **mock** it

Notes:

or do whatever you want with it

maybe you don't want to do this; 

we'll talk more about the tradeoffs of mocking.

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
Footer: false
<!-- .slide: data-background-video="/images/search-homepage.webm" data-background-size="contain" -->

Notes:

artsy homepage

searchbox - search for artists you love

let's build a cypress test for it

---

Trail: Cypress, Example
LineNumbers: 1,2

## Syntax of a test

```javascript
describe("searching", () => {
  it("searches for an artist", () => {





    // your test goes in here!






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

Notes:

Lots of commands available on global cy object

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
