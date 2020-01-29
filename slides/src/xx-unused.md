---

Layout: steve
Trail: Module,Section

# Stuff!

## Including a trail of Module & Section

---

Trail: Module
Layout: module

## More stuff!!!! Including a trail of 'Module'.

### Happening here

<!-- .element: class="fragment" -->

#### If you know what I mean

<!-- .element: class="fragment" -->

---

Trail: Module,Section,Dog

# Three trails!

## Module, section and dog!

Notes:
and I got some notes, too!

---

Footer: false

Trail: Module

# A small trail

## Module

### But no footer

---

LineNumbers: 1,3,4,5-7

```
abc
var x = y;
var x = y;
var x = y;
var x = y;
var x = y;
var x = y;
var x = y;
var x = y;
var x = y;
var x = y;
```
---

# Outro

## But no trail

Note:

and some outro notes

go here

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

Trail: Testing Strategies, Testing Pyramid

todo: drawing of traditional pyramid

Notes:

Let's look back at our testing pyramid

My experience is that 
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

Trail: Cypress, Example

## commands (cy.customName)

---

Footer: false

<!-- .slide: data-background="/images/star-student.jpg" class="title" -->

Notes:

star student
