---
title: 'Reshaping The Testing Pyramid With Cypress - Steven J Hicks'
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

## Reshaping The Testing Pyramid With **Cypress**

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
</svg> stevenhicks.me/cypress-reshapes-the-pyramid
</p>

</div>
Notes:

pre-game:

- STICKERS!
- dad's root beer
- javascript

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

so that everyone can be moved by art daily.

and we're doing that with a platform for collecting and discovering art.
---
<!-- .slide: data-background="/images/testing-pyramid.jpg" -->

Trail: Testing Strategies

Notes:

Testing strategies

- Mike Cohn, Succeeding with Agile, 2009
- explain types of tests
- opinions over shape, names of tests, validity, etc
- but it's still a useful metaphor to talk about tradeoffs in testing


---
<!-- .slide: data-background="/images/testing-pyramid-tradeoffs.jpg" -->

Trail: Testing Strategies

Notes:

it's a pyramid because there are tradeoffs

1) cost: to write & maintain
2) speed
3) reliability: how often does this test fail or break?
4) confidence: how confident about your app?

- 3 on the left have better outcomes lower in the pyramid
- 1 on the right has better outcomes higher in the pyramid

we'll talk about the top of they pyramid today, e2e

and I'm especially interested in addressing one question:

---

Layout: list
Trail: Testing Strategies

## Why are end-to-end tests hard?

### • Many moving parts

<!-- .element: class="fragment" -->

### • State

<!-- .element: class="fragment" -->

### • Data

<!-- .element: class="fragment" -->

### **•** **Tooling**

<!-- .element: class="fragment" -->

Notes:

0) those 3 left columns all have poorer outcomes for e2e. why?

1) parts: you're not just testing individual units anymore

(parts): more could go wrong

2) state: to complete a test, you need to put the system into a specific state; state is hard to deal with

3) data: you need reliable data so that your tests aren't flaky. If they're flaky, they'll get turned off or deleted.

4) tooling - may vary depending on tech stack (rails vs js)

focus on tooling

but we'll also circle back to this list at the end
---
Layout: module

# Cypress

Fast, easy and reliable testing for anything that runs in a browser.

[cypress.io](https://cypress.io)

---

Trail: Cypress

> All-in-one testing framework, assertion library, with mocking and stubbing, all without Selenium.

[cypress.io](https://cypress.io)

---

Trail: Cypress

> Cypress focuses on doing end-to-end testing REALLY well.

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

## It's JavaScript
### and so are the tests you write

Notes:

selling point? not sure.

Selenium supports many languages

---

Trail: Cypress, Architecture

## It's somewhat cross-browser
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

## Tests run when files update *

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

Layout: module

# Cypress at Artsy

---
Trail: Cypress at Artsy

## Smoke Tests

Notes:

We started with some real simple POC tests

to prove we could get value from cypress

and that meant writing some smoke tests

to make sure the site was up after each deployment.

---
Footer: false

<!-- .slide: data-background="/images/artwork-page.jpg" data-background-size="contain" -->

Notes:

this is our artwork page

---
LineNumbers: 3,4,5

Trail: Cypress at Artsy, Smoke Tests

```javascript
describe("Artwork", () => {
  it("/artwork/:id", () => {
    cy.visit("artwork/andy-goldsworthy-ammonite")
    cy.get("h1").should("contain", "Andy Goldsworthy")
    cy.get("h2").should("contain", "Ammonite")
  })
})
```

Notes:

this is what our test looked like. 

Not a lot to it

But it proves to us that we didn't totally break the artwork page

---
Trail: Cypress at Artsy

## Critical Flows

Notes:

and then we moved on to testing critical flows of our app

---
Trail: Cypress at Artsy, Critical Flows

## Logging In

Notes:

like logging in

---
Footer: false
<!-- .slide: data-background-video="/images/logging-in.webm" data-background-size="contain" -->


---
Trail: Cypress at Artsy, Critical Flows, Logging In
LineNumbers: 100

```javascript
it("logs in admin user", () => {
  // 1. visit home
  // 2. pop login modal
  // 3. log in admin user
  // 4. verify logged in
})
```

Notes:

kind of a lot going on - broken down into multiple slides

---
Trail: Cypress at Artsy, Critical Flows, Logging In
LineNumbers: 3,6,7,8,9

```javascript
it("logs in admin user", () => {
  // 1. visit home
  cy.visit("/")

  // 2. pop login modal
  cy.get("header")
    .find("button")
    .contains("Log in")
    .click()

  // 3. log in admin user
  // 4. verify logged in
})
```


---
Trail: Cypress at Artsy, Critical Flows, Logging In
LineNumbers: 6-14,17

```javascript
it("logs in admin user", () => {
  // 1. visit home
  // 2. pop login modal

  // 3. log in admin user
  cy.get("input[type=email]")
    .type(Cypress.env("ADMIN_USER"))
  cy.get("input[type=password]")
    .type(Cypress.env("ADMIN_PASSWORD"), {
      log: false,
    })
  cy.get("button")
    .contains("Log in")
    .click()

  // 4. verify logged in
  cy.get("header").find("a[href='/works-for-you']")
})
```

---
Trail: Cypress at Artsy, Critical Flows

## Finding Art

Notes:

and finding art

---
Footer: false
<!-- .slide: data-background-video="/images/finding-art.webm" data-background-size="contain" -->

Notes:

many ways to filter:
- filter by buy now
- filter by medium and a few other options 
- filter by price

It's important to us that our collectors can find artwork that moves them.

---
LineNumbers: 100
Trail: Cypress at Artsy, Critical Flows, Finding Art

```javascript
it("filters by medium", () => {
  cy.visit("/collect")

  cy.contains("Ways to buy")

  cy.get("input[type=radio]").contains("Painting").click()

  cy.url().should("contain", "/collect/painting")
})
```

Notes:

...
and if you have consistent reliable results, you could specify which artworks appeared

we don't - our inventory is changing frequently, 

and our artwork sort has a touch of "trending" to it

---
Trail: Cypress at Artsy, Critical Flows

## Buying Art

Notes:

when they find something they love, we want to make sure they can

buy art

- negotiate with the gallery
- make an offer

---
Footer: false
<!-- .slide: data-background-video="/images/buying-art.webm" data-background-size="contain" -->

Notes: 

- or buy it immediately

---
LineNumbers: 100

Trail: Cypress at Artsy, Critical Flows, Buying Art

```javascript
it("can buy an individual work", () => {
  // 1. log in as partner
  // 2. upload new artwork for sale
  // 3. log in as collector
  // 4. buy artwork
  // 5. verify artwork is sold
})
```

Notes: 

no code - too much!

you start to smell the aroma of one of our biggest challenges so far

how to deal with data & state?

We're chaining together a series of actions for this test

And that has tradeoffs

---
Trail: Cypress at Artsy

## Challenges

---
Trail: Cypress at Artsy, Challenges
Layout: list

## Why are end-to-end tests hard?

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

## 1. Use a live database

### 👍🏼 Tests the entire stack
### 👎 Depends on live data not changing
### 👎 Requires fake users

Notes:

live db - from staging or production site

1) one of our goals was to prevent "breaking the site" & without testing entire stack we couldn't be sure

(confidence)

2) (not much control)

3) fake users: 
3a) have to store them in the live db
3b) have to store _creds_ somewhere the tests can access

---

Trail: Cypress at Artsy, Challenges, Data
Layout: list

## 2. Use a test database

### 👍🏼 Tests the entire stack
### 👍🏼 We can seed it however we want
### 👎 Hard to set up

Notes:

1) confidence

2) control

3) We don't have one source of data; we have five to ten. Mongodb, postgres, elastic

---

Trail: Cypress at Artsy, Challenges, Data
Layout: list

## 3. Use no database (mock data calls)

### 👍🏼 Easier to set up
### 👍🏼 We can mock it however we want
### 👎 Doesn't test the entire stack

Notes:

1) 
2) control
3) entire stack: and you might say it's leaving out the most important part 

(less confidence)

---

Trail: Cypress at Artsy, Challenges, Data
Layout: list

## 1. Use a live database
## 2. Use a test database
## 3. Use no database (mock data calls)

Notes:

which did we choose?

which would YOU choose?

point: it depends on context & circumstances!

---

Trail: Cypress at Artsy, Challenges, Data
Layout: list

## **1. Use a live database** 👈🏼
## 2. Use a test database
## 3. Use no database (mock data calls)

Notes:

We settled on #1

it was really important to us to test the whole stack

2 seems like the "right way" for testing the entire stack, 

but it also has the biggest upfront cost - setting up all that data, in many different systems.

I wouldn't be surprised to see us end up here _eventually_

---

Trail: Cypress at Artsy, Challenges, Data
Layout: list

## 1. Use a live database
## 2. Use a test database
## 3. **Use no database (mock data calls) **

Notes:

But also - #3 is really intriguing

in a different way

---
Trail: Cypress at Artsy, Challenges, Data

## 3. Use no database (mock data calls)

# **TDD**

<!-- .element: class="fragment" -->

Notes:

if you can mock out all your network calls, it makes it easy for you to use cypress for...

---
Trail: Cypress at Artsy, Challenges, Data, TDD

# Demo!

Notes:

so I want to take a few minutes for another demo

to show how you could TDD with Cypress

if you mock out all your network communication

---

Trail: Cypress at Artsy, Challenges

## Finding Elements

Notes:

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

0) key to meaningful tests that last

1) Text: that they can read on the screen
1a) target buttons and links with the text they see

...

In general, the closer you are to testing your app the way a real user uses it, the more reliable & resilient your tests are going to be.

But sometimes you need to find an element and there's **no way to target it** that a user would experience

---
<!-- .slide: data-background="/images/double-rail.jpg" -->
Footer: false

Notes:

We use these rails all over our site to display different contexts of artwork

And in each rail is a series of artwork cards

If we imagine a scenario where we want to find an artwork 

but it appears in two separate rails

How do we target the one under "Your favorite works?"

---

Trail: Cypress at Artsy, Challenges, Finding Elements
LineNumbers: 1,7

## Semantic CSS

```html
<div class="recently-viewed">
  <h2>Recently viewed</h2>
  <ul>
    <li><...Andy Goldsworthy artwork card... /></li>
  </ul>
</div>
<div class="your-favorite-works">
  <h2>Your favorite works</h2>
  <ul>
    <li><...Andy Goldsworthy artwork card... /></li>
  </ul>
</div>
```

Notes:

semantic css: css selectors describe an element's usage in the app

so you might put a class on the element surrounding the card you want to grab

---

Trail: Cypress at Artsy, Challenges, Finding Elements
LineNumbers: 100

## Semantic CSS

```javascript
cy.get(".your-favorite-works").contains("Andy Goldsworthy")
```

Notes:

and then to find it, your query looks like this

it's definitely better than trying to use indexes of elements on the page

and it works.

until it doesn't, because a dev removes the semantic class or renames it.

...

At Artsy, we don't even write semantic markup

---
LineNumbers: 1,7

Trail: Cypress at Artsy, Challenges, Finding Elements

## React + Styled Components

```html
<div class="sc-bdVaJa jVrsza">
  <h2>Recently viewed</h2>
  <ul>
    <li><...Andy Goldsworthy artwork card... /></li>
  </ul>
</div>
<div class="sc-bdVaJa bOgaFD">
  <h2>Your favorite works</h2>
  <ul>
    <li><...Andy Goldsworthy artwork card... /></li>
  </ul>
</div>
```

Notes:

Styled components: more stable styling

We have no semantics in our markup

Compounding this: our test project is in a separate codebase than UI

---
LineNumbers: 1,7

Trail: Cypress at Artsy, Challenges, Finding Elements

## **data-** Attributes

```html
<div class="sc-bdVaJa jVrsza">
  <h2>Recently viewed</h2>
  <ul>
    <li><...Andy Goldsworthy artwork card... /></li>
  </ul>
</div>
<div class="sc-bdVaJa bOgaFD" data-test="your-favorite-works">
  <h2>Your favorite works</h2>
  <ul>
    <li><...Andy Goldsworthy artwork card... /></li>
  </ul>
</div>
```

---
LineNumbers: 100

Trail: Cypress at Artsy, Challenges, Finding Elements

```javascript
cy.get("[data-test=your-favorite-works]").contains("Andy Goldsworthy")
```

Notes:

Recommended by cypress for *all* elements (I disagree)

More robust tests


---
Trail: Cypress at Artsy, Challenges, Finding Elements
LineNumbers: 2,5

## cypress-testing-library
github.com/testing-library/cypress-testing-library

```javascript
cy.contains("Learn about and collect art")
cy.findByText("Learn about and collect art")

cy.get('[placeholder="Search"]')
cy.findByPlaceholderText("Search")
```

Notes:

a tool that enforces finding elements by what the user sees

this is a rewrite of our example test

findBy....

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
```

Notes:

- different ways to search for elements how the _user_ experiences your app
- dataId - escape hatch
- different methods to fail or not fail when something's not found

---
Trail: Cypress at Artsy, Challenges

## Working With Variables

Notes:

is way harder than you would expect

I actually intended to not talk about this

I'd read that it was a difficult thing to do in Cypress, but thought it was an edge case I wouldn't need

---

Trail: Cypress at Artsy, Challenges, Working With Variables

> You cannot assign or work with the return values of any Cypress command. **Commands are enqueued and run asynchronously.**

[cypress.io](https://docs.cypress.io/guides/core-concepts/variables-and-aliases.html#Return-Values)

Notes:


---
LineNumbers: 6

Trail: Cypress at Artsy, Challenges, Working With Variables


```javascript
 // example pathname: /articles/12344

function extractIDFromURL() {
  return cy
    .location('pathname')
    .split('/')[2];
}
```

### 👎🏼 This won't work.

<!-- .element: class="fragment" -->

Notes:

Imagine you have a test where you want to extract the id from the url of the current page

To extract that ID and store it, you might think...

...

but due to the nature of all commands in cypress being asynchronous

which is what allows them all to automatically wait

you can't do this - the result of location isn't a string

it's cypress's implementation of a promise

---
LineNumbers: 100

Trail: Cypress at Artsy, Challenges, Working With Variables

```javascript
 // example pathname: /articles/12344

function extractIDFromURL() {
  cy.location('pathname')
    .invoke('split', '/')
    .its(2)
    .as('articleID');
}
```

### 👍🏻

Notes:

so instead....

and that "aliases" the value as a variable named articleID

which you can access through a special cypress command

---

Trail: Cypress at Artsy, Challenges

## Limitations

[https://docs.cypress.io/guides/references/trade-offs.html](https://docs.cypress.io/guides/references/trade-offs.html)

Notes:

There are acknowledged limitations of Cypress

and a few of them have affected us in our short time of using it

url - don't write it down. go to my slides and click on the link.

---

Trail: Cypress at Artsy, Challenges, Limitations

> There will never be support for **multiple browser tabs**.

[cypress.io](https://docs.cypress.io/guides/references/trade-offs.html)

Notes:

tests for a CMS tool that pops the page you're editing in another tab

and you want to inspect the value that's rendered there

it's not as simple as `cy.contains()`

workaround: request page programmatically & inspect contents 

---

Trail: Cypress at Artsy, Challenges, Limitations

> You cannot use Cypress to drive **two browsers at the same time**.

[cypress.io](https://docs.cypress.io/guides/references/trade-offs.html)

Notes:

We've talked about doing some complex auction bidding scenarios between multiple bidders

workarounds described at url

---

Trail: Cypress at Artsy, Challenges, Limitations

> Each test is bound to a **single origin**.

[cypress.io](https://docs.cypress.io/guides/references/trade-offs.html)

Notes:

SSO

if you're using a 3rd party auth provider, 

you'll need to do some trickery to visit that second origin

(request page programmatically & inspect response)

(me: set cookies/local storage with spoofed auth)

---

Layout: module

# The Verdict

---

Trail: Verdict

## Does Cypress replace Selenium?

### **No**

<!-- .element: class="fragment" -->

Notes:

the cypress team thinks it will eventually, they just have to resolve:

1) javascript only

2) cross-browser testing

but they wield strong opinions (limitations)

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

developers enjoying writing end-to-end tests can end one of two ways

which you end up following says a lot about the relationships of your organization.

1) no need for qa

2) ...

---

Trail: Verdict

## Developers and QA can **share ownership**.

Notes:

historically there's been a wall that devs chuck things over for qa to look at

but if we are co-owning the codebase

it's a chance for us to smash silos

and get totally cross-functional

and help each other out more

---

Trail: Verdict

## The pyramid doesn't have to be a pyramid anymore

Notes:

Now that integration & e2e tests are so much easier with Cypress,

we don't have to be bound to the pyramid.

We can use a shape that makes most sense to us

---

Trail: Verdict

TODO: image of just the pyramid

Notes:

And maybe that means _actually_ building a pyramid, instead of just unit tests

---

Trail: Verdict

TODO: image of ice cream cone

Notes:

or maybe we feel like the e2e tests, inspiring the most confidence of all tests, is where we want to focus

---

Trail: Verdict

TODO: image of diamond

Notes:

or maybe we really want to focus on the middle

and while we're at it, let's get rid of these tiers that don't make sense anymore

because it's not "e2e" vs "integration" that makes it hard

---

Trail: Verdict

TODO: image of diamond with scale of dependence vs independence

Notes:


it's "do my tests depend on something I don't control?"

unit tests don't. 

e2e tests do.

integration tests...depend on what they're all testing.

---

Trail: Verdict

TODO: image of diamond with two tiers

Notes:

and that's what separates the easy tests from the hard tests

are they independent? Do we control everything this test needs?

Or are they dependent on something out of our control?

...

Choose your shape

---

Trail: Verdict

TODO: image of ice cream cone with two tiers

---

Trail: Verdict

TODO: image of pyramid with two tiers

Notes:
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
</svg> stevenhicks.me/cypress-reshapes-the-pyramid
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

Wrapper: double-wide

Layout: long-list

Trail: Resources, Further Reading

##### [Cross-browser GitHub issue](https://github.com/cypress-io/cypress/issues/310)
