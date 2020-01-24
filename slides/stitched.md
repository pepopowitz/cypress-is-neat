---
title: 'Cypress: End-to-end Testing For Developers & Quality Engineers - Steven J Hicks'
theme: css/theme.css
revealOptions:
  transition: 'none'
  controls: false
  progress: false
  center: true
css: css/custom.css
preprocessor: _build/inject.js
highlightTheme: 'mono-blue'
width: '100%'
height: '100%'
template: '_template/reveal.html'
---
Footer: false

<!-- .slide: data-background="/images/title.jpg" class="title" -->

<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" style="width:0;height:0;position:absolute;overflow:hidden;">
  <defs>
<symbol viewBox="0 0 567.31298828125 409.60003662109375" aria-labelledby="apsi-zocial-cloudapp-title" id="si-zocial-cloudapp"><title id="apsi-zocial-cloudapp-title">icon cloudapp</title><path d="M.001 280.576c0-35.504 12.544-65.872 37.632-91.136 25.087-25.264 55.215-37.888 90.368-37.888l.511.512c0-1.024-.08-2.224-.255-3.584-.176-1.36-.256-2.384-.256-3.072 0-40.272 14.08-74.576 42.24-102.912C198.401 14.16 232.449 0 272.385 0c35.152 0 66.048 11.264 92.672 33.792s43.008 50.864 49.152 84.992h8.704c39.92 0 73.984 14.16 102.144 42.496s42.256 62.64 42.256 102.912c0 40.288-14.096 74.592-42.256 102.928s-62.223 42.48-102.144 42.48c-2.736 0-4.784-.16-6.144-.495v.495H120.816v-.512c-33.792-1.712-62.367-15.023-85.76-39.935C11.68 344.24 0 314.72 0 280.576z"/></symbol>
<symbol viewBox="0 0 514.8550415039062 347.53997802734375" aria-labelledby="aysi-zocial-email-title" id="si-zocial-email"><title id="aysi-zocial-email-title">icon email</title><path d="M0 316.758V30.782c0-.33.496-3.475 1.49-9.433l168.308 143.98L1.986 326.688c-1.323-4.634-1.985-7.944-1.985-9.93zM22.342 1.49C24.659.497 27.472 0 30.782 0h453.29c2.98 0 5.958.497 8.937 1.49L324.204 145.968l-22.342 17.873-44.187 36.244-44.187-36.244-22.342-17.873zm.496 344.56L192.14 183.7l65.536 53.123 65.536-53.124L492.513 346.05c-2.648.994-5.461 1.49-8.44 1.49H30.783c-2.649 0-5.297-.496-7.945-1.49zm322.716-180.719L513.366 21.35c.993 2.98 1.489 6.124 1.489 9.434V316.76c0 2.978-.496 6.288-1.49 9.93z"/></symbol>
<symbol viewBox="0 0 640.0180053710938 520.3389892578125" aria-labelledby="dnsi-zocial-twitter-title" id="si-zocial-twitter"><title id="dnsi-zocial-twitter-title">icon twitter</title><path d="M0 461.54c10.42 1.014 20.826 1.548 31.22 1.548 61.048 0 115.528-18.732 163.387-56.17-28.424-.352-53.933-9.041-76.477-26.043-22.57-16.99-37.984-38.675-46.323-65.056 6.933 1.418 15.102 2.095 24.456 2.095 12.15 0 23.766-1.575 34.862-4.684-30.517-5.866-55.766-20.891-75.709-44.996-19.955-24.13-29.919-51.969-29.919-83.527v-1.574c18.395 10.42 38.31 15.805 59.826 16.13-18.016-11.798-32.338-27.304-42.915-46.57-10.575-19.24-15.87-40.13-15.87-62.675 0-23.597 6.088-45.607 18.212-66.095 32.6 40.586 72.418 72.938 119.431 97.055 47 24.092 97.368 37.53 151.158 40.327-2.432-11.448-3.655-21.516-3.655-30.18 0-36.085 12.84-66.954 38.505-92.62C375.868 12.839 406.893 0 443.342 0c37.79 0 69.7 13.88 95.73 41.64 30.167-6.257 57.926-17.015 83.255-32.261-9.718 31.558-28.815 55.845-57.238 72.847 25.327-3.109 50.304-10.055 74.929-20.813-16.651 26.017-38.336 48.742-65.056 68.151v17.198c0 34.992-5.125 70.128-15.35 105.355-10.211 35.214-25.848 68.853-46.83 100.972-20.996 32.065-46.05 60.619-75.189 85.569-29.126 24.977-64.08 44.853-104.849 59.592-40.755 14.752-84.555 22.089-131.398 22.089-72.483-.014-139.606-19.605-201.345-58.8z"/></symbol>
  </defs>
</svg>

## **Cypress:** End-to-end Testing For Developers & Quality Engineers

<div class="contact">
<h3>Steven Hicks</h3>

<p>
<svg class="icon">
  <use xlink:href="#si-zocial-twitter" />
</svg>@pepopowitz
</p>

<p>
<svg class="icon">
  <use xlink:href="#si-zocial-email" />
</svg>steven.j.hicks@gmail.com
</p>

<p>
<svg class="icon">
  <use xlink:href="#si-zocial-cloudapp" />
</svg> stevenhicks.me/cypress-for-devs-and-qa
</p>

</div>
Notes:

pre-game:

- STICKERS!
- dad's root beer

go-time:

- thanks to organizers
- thanks to centare
- thanks to you

---

Footer: false

<!-- .slide: data-background="/images/artsy.svg" data-background-size="750px" data-background-color="black" -->

Notes:

Tech Lead at Artsy

NYC, MKE

our mission is to expand the art market,

and we're doing that with a platform for collecting and discovering art.

---

<!-- .slide: data-background="/images/star-student.jpg" class="title" -->

Notes:


---

Trail: Testing Strategies

## Testing Pyramid

TODO: test pyramid

Notes:

Testing strategies

---

Trail: Testing Strategies

## Testing Pyramid

TODO: test pyramid, with costs/benefits

Notes:

- Lack of confidence in unit
- More confidence in e2e, but they're harder

---

Layout: list
Trail: Testing Strategies, Testing Pyramid

## Why are integration/e2e tests hard?

### • Many moving parts

<!-- .element: class="fragment" -->

### • State

<!-- .element: class="fragment" -->

### • Data

<!-- .element: class="fragment" -->

### **•** **Tooling**

<!-- .element: class="fragment" -->

Notes:

1) parts: you're not just testing individual units anymore

(parts): more could go wrong

2) state: to complete a test, you need to put the system into a specific state; state is hard to deal with

3) data: you need reliable data so that your tests aren't flaky. If they're flaky, they'll get turned off or deleted.

4.)tooling - may vary depending on tech stack (rails vs js)

focus on tooling

but we'll also circle back to this list at the end
---
Layout: module

# Cypress

Fast, easy and reliable testing for anything that runs in a browser.

[cypress.io](https://cypress.io)

---

todo: gif of tests running

Notes:

what it looks like

We'll look at an actual running test later

---

Trail: Cypress

> All-in-one testing framework, assertion library, with mocking and stubbing, all without Selenium.

[cypress.io](https://cypress.io)

---

Trail: Cypress

> Cypress focuses on doing end-to-end testing REALLY well.

[cypress.io](https://cypress.io)

Notes:

---

Trail: Cypress, Architecture

## It's not Selenium

Notes:

many e2e tools _are_, under the covers

---

Trail: Cypress, Architecture

todo: drawing of selenium architecture

---

Trail: Cypress, Architecture

todo: drawing of cypress architecture

Notes:

executed in the same run loop as your app

so it can interact with your app & all events in your app, 

including all network activity

also makes it **faster** because the communication is more direct

---

Trail: Cypress, Architecture

## It's JavaScript
### and so are the tests you write

Notes:

selling point? not sure.

Selenium supports many languages

---

Trail: Cypress, Architecture

## It's Chrome only
### for now...

Notes:

let's get that out of the way

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

## Tests run when files update

### tightening your **feedback loop**

Notes:

When you're running the tests locally, 

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

### making your tests **fast**

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

---

Layout: module

# The Verdict

---

Trail: Verdict

## Does Cypress replace Selenium?

### **Not yet.**

<!-- .element: class="fragment" -->

Notes:

1) javascript only

2) cross-browser testing

they're working on it - but it's far away from being usable in ie.

---

Trail: Verdict

## Cypress is a tool.

Notes:

It's useful

It can give you a lot of confidence to change your software

---

Trail: Verdict

## Cypress is young.

Notes:

It has a lot of growing to do

But it shows a ton of promise

---

Trail: Verdict

## Developers like to write Cypress tests.

Notes:

- we write JS - same language in app & tests

- maybe not for a team that wasn't familiar with JS

- it's not like you're doing COMPLICATED js. But the learning curve is a consideration

developers enjoying writing end-to-end tests can end one of two ways

which you end up following says a lot about the relationships of your organization.

1) no need for qa

2) ...

---

Trail: Verdict

## Developers and QA can **share ownership**.

Notes:

This is the holy grail for me

This is how we smash silos

and get totally cross-functional

---

Layout: module

# Soapbox

---

Trail: Soapbox

todo: drawing of traditional pyramid

Notes:

not sure how to do this. does it belong at the beginning when we first talk about the pyramid?

---



- return to what makes integration/e2e testing hard
  - many moving parts
  - stateful
  - data
    - long-living data
    - or lots of fake data to set up/tear down
  - tooling

  - the pyramid is wrong
    - with tooling like cypress & even selenium,
      - it's not about unit vs integration vs e2e

---

    - line between independent & dependent tests
      - this is where it goes from hard to easy
      - and it's not because of what types of tests they are
      - it's because of the first three things listed above
        - moving parts, state, data
    - and those things mean our tests are dependent on things outside of themselves

---

  - independent vs dependent


---

Footer: false

<!-- .slide: data-background="/images/title.jpg" class="title" -->

# Thank you!

<div class="contact">
<h3>Steven Hicks</h3>

<p>
<svg class="icon">
  <use xlink:href="#si-zocial-twitter" />
</svg>@pepopowitz
</p>

<p>
<svg class="icon">
  <use xlink:href="#si-zocial-email" />
</svg>steven.j.hicks@gmail.com
</p>

<p>
<svg class="icon">
  <use xlink:href="#si-zocial-cloudapp" />
</svg> stevenhicks.me/cypress-for-devs-and-qa
</p>

</div>


Notes:

- Thank you for your time!

- Questions afterward

- Enjoy the rest of \_\_\_

---

Wrapper: double-wide

Layout: long-list

Trail: Resources, Image Credits

##### [Cover - Wil Stewart](https://unsplash.com/photos/UErWoQEoMrc)

---

Layout: long-list

Trail: Resources, Further Reading

##### [Cross-browser GitHub issue](https://github.com/cypress-io/cypress/issues/310)
