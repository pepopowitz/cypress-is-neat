---

Layout: module

# Cypress at Artsy

---
Trail: Cypress at Artsy

- artsy homepage

Notes:

- lots of ways for a collector to explore

---
Trail: Cypress at Artsy

- artsy artwork grid

Notes:

- filter by buy now
- filter by medium and a few other options 
- filter by price

It's important to us that our collectors can find artwork that moves them.

---

Trail: Cypress at Artsy

- artsy artwork to buy now

Notes: 

when they find something they love, we want to make sure they can...

- negotiate with the gallery
- make an offer
- buy it immediately

---
Trail: Cypress at Artsy

# Smoke Tests

todo: gif of artwork page test

---
Trail: Cypress at Artsy, Smoke Tests

todo: code sample from artwork page test

---
Trail: Cypress at Artsy

# Login

todo: gif of login test

---
Trail: Cypress at Artsy, Login

todo: code sample from login test

---
Trail: Cypress at Artsy

# Purchase

todo: gif of buy artwork test

---
Trail: Cypress at Artsy

todo: code sample from buy artwork test

---
Trail: Cypress at Artsy

## Learnings

---
Trail: Cypress at Artsy, Challenges
Layout: list

## Why are integration/e2e tests hard?

### • Many moving parts

### • State

### **•** **Data**

### • Tooling

Notes:

remember?

Before we even started, we wanted to figure out how we would approach the data issue.

---

Trail: Cypress at Artsy, Challenges, Data
Layout: list

## 1. Use a real database

### 👍🏼 Tests the entire stack
### 👎🏼 Depends on live data not changing
### 👎🏼 Requires fake users

Notes:

1) one of our goals was to prevent "breaking the site" & without testing entire stack we couldn't be sure

2) 

3) fake users: 
3a) have to store them in the real db
3b) have to store _creds_ somewhere the tests can access

---

Trail: Cypress at Artsy, Challenges, Data
Layout: list

## 2. Use a test database

### 👍🏼 Tests the entire stack
### 👍🏼 We can seed it however we want
### 👎🏼 Hard to set up

Notes:

1)

2)

3) We don't have one source of data; we have five to ten. Mongodb, postgres, elastic

---

Trail: Cypress at Artsy, Challenges, Data
Layout: list

## 3. Use no database (mock data calls)

### 👍🏼 Easier to set up
### 👍🏼 We can mock it however we want
### 👎🏼 Doesn't test the entire stack

Notes:

3) entire stack: and you might say it's leaving out the most important part 

---

Trail: Cypress at Artsy, Challenges, Data
Layout: list

## 1. Use a real database
## 2. Use a test database
## 3. Use no database (mock data calls)

Notes:


---

Trail: Cypress at Artsy, Challenges, Data
Layout: list

## **1. Use a real database** 👈🏼
## 2. Use a test database
## 3. Use no database (mock data calls)

Notes:

We settled on #1

it was really important to us to test the whole stack

2 seems like the "right way" for testing the entire stack, 

but it also has the biggest upfront cost - setting up all that data, in many different systems.

I wouldn't be surprised to see us end up here _eventually_

also: 3 might be great for you (cory)

---

Trail: Cypress at Artsy, Challenges

## Finding Elements

---

Trail: Cypress at Artsy, Challenges, Finding Elements

Layout: list

### **Rule #1: ** Find elements the way your users would

### • Text

<!-- .element: class="fragment" -->

### • Forms: **label** or **placeholder**

<!-- .element: class="fragment" -->

### • Images: **alt**

<!-- .element: class="fragment" -->

### • SVG: **title**

<!-- .element: class="fragment" -->

Notes:

1) Text: that they can read on the screen
1a) target buttons and links with the text they see

In general, the closer you are to testing your app the way a real user uses it, the more reliable & resilient your tests are going to be.

But sometimes you need to find an element and there's **no way to target it** that a user would experience

---

Trail: Cypress at Artsy, Challenges, Finding Elements

todo: pic of artwork item on site

Notes:

Using an artwork item as an example, a couple ways to approach this:

---

Trail: Cypress at Artsy, Challenges, Finding Elements

## Semantic Markup

```jsx
todo: semantic artwork item code
```

Notes:

tempting.

it's way better than trying to use indexes of elements on the page

and it works.

until it doesn't, because a dev removed this class.

---

Trail: Cypress at Artsy, Challenges, Finding Elements

## **data-** Attributes

```jsx
todo: semantic artwork item code with data-cypress-id
```

Notes:

Recommended by cypress for *all* elements (I disagree)

More robust tests

At Artsy, we don't even write semantic markup

---

Trail: Cypress at Artsy, Challenges, Finding Elements

## React + Styled Components

```jsx
todo: styled components artwork item
```

Notes:

Styled components: more stable styling

We have no semantics in our markup

Compounding this: our test project is in a separate codebase than UI

---
Trail: Cypress at Artsy, Challenges, Finding Elements
LineNumbers: 5,7,11,14

## cypress-testing-library
github.com/testing-library/cypress-testing-library

```javascript
describe("homepage", () => {
  it("searches for an artist", () => {
    cy.visit("/")

    cy.findByText("Learn about and collect art")

    cy.findByPlaceholderText("Search")
      .click()
      .type("goldsworthy")

    cy.findByText("Andy Goldsworthy").click()

    cy.url().should("contain", "andy-goldsworthy")
    cy.findByText(/^Andy Goldsworthy creates outdoor sculpture/)
  })
})
```

---
Trail: Cypress at Artsy, Challenges, Finding Elements
LineNumbers: 100

## cypress-testing-library
github.com/testing-library/cypress-testing-library

```javascript
cy.findByText("...")
cy.findByAltText("...")
cy.findByLabelText("...")
cy.findByPlaceholderText("...")
cy.findByRole("...")
cy.findByTitle("...")
cy.findByDataId("...")

cy.findAllByText("...")
...
```

Notes:

- different ways to search for elements how the _user_ experiences your app
- dataId - escape hatch
- findAll...
- different methods to fail or not fail when something's not found

---
Trail: Cypress at Artsy, Challenges

## Single Sign-On (SSO)

Notes:

(https://github.com/cypress-io/cypress-example-recipes/blob/master/examples/logging-in__single-sign-on/cypress/integration/logging-in-single-sign-on-spec.js)

todo: fill this section in

- issue: only one domain can be `visit`ed
- to use an external sign-in domain,
  - use `cy.request` instead of `cy.visit`, and parse results manually
  - set cookies/local storage/etc with spoofed authentication

---

Trail: Cypress at Artsy, Challenges

## Automation

Notes:

todo: fill this section in

- should failed UI tests block a build? 
  - testing full stack is slow
  - our web app is three npm projects deep
    - our api is 5 to 10 deep
    - should _those_ be blocked by a failed UI test?
- we settled on running every 30 minutes, non-blocking
  - report failures in slack
- env variables 
  - Cypress.env()
  - cypress.json
  - cypress.env.json

