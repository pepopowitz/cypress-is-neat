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
it("logs in user", () => {
  // 1. visit home
  // 2. pop login modal
  // 3. log in user
  // 4. verify logged in
})
```

Notes:

kind of a lot going on - broken down into multiple slides

---
Trail: Cypress at Artsy, Critical Flows, Logging In
LineNumbers: 3,6,7,8,9

```javascript
it("logs in user", () => {
  // 1. visit home
  cy.visit("/")

  // 2. pop login modal
  cy.get("header")
    .find("button")
    .contains("Log in")
    .click()

  // 3. log in user
  // 4. verify logged in
})
```


---
Trail: Cypress at Artsy, Critical Flows, Logging In
LineNumbers: 6-14,17

```javascript
it("logs in user", () => {
  // 1. visit home
  // 2. pop login modal

  // 3. log in user
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
### 👎 Requires fake data in live DB

Notes:

live db - from staging or production site

1) one of our goals was to prevent "breaking the site" & without testing entire stack we couldn't be sure

(confidence)

2) (not much control)

3) or creating _fake_ data in your live db

like that artwork we just bought

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

