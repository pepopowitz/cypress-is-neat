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

