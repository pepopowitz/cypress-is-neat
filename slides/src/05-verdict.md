---
Layout: module
# The Verdict

---

Trail: Verdict

## Does Cypress replace Selenium?

### **No**

<!-- .element: class="fragment" -->

Notes:

the cypress team thinks it could

but they wield strong opinions

which is great for their velocity!

but limitations & lack of IE will prevent it from replacing selenium

---

Trail: Verdict

## Cypress is a great tool.

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

1. no need for qa

2. ...

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

## The **pyramid** doesn't have to be a **pyramid**

Notes:

But the thing I've most learned from Cypress

is that we no longer need to be bound to the pyramid.

Now that integration & e2e tests are so much easier with Cypress,

We can use a shape that makes most sense to us

---

Trail: Verdict

<!-- .slide: data-background="/images/pyramid-1-pyramid.jpg" -->

Notes:

And maybe that means _actually_ building a pyramid, instead of just unit tests

---

Trail: Verdict

<!-- .slide: data-background="/images/pyramid-2-ice-cream-cone.jpg" -->

Notes:

or maybe we feel like the e2e tests, inspiring the most confidence of all tests, is where we want to focus

---

Trail: Verdict

<!-- .slide: data-background="/images/pyramid-3-diamond.jpg" -->

Notes:

or maybe we really want to focus on the middle

and while we're at it, let's get rid of these tiers that don't make sense anymore

unit vs integration vs e2e implies that 

the difference between the easy tests at the bottom 

and the hard tests at the top

is the amount of your code that's involved in the tests.

and that's true to some degree, but not enough to define how many tests we write

---

Trail: Verdict

<!-- .slide: data-background="/images/pyramid-4-diamond-with-systems.jpg" -->


Notes:

our app interacts with all these other systems

that our outside of our code's control.

and the tests that are hard to write/maintain

---

Trail: Verdict

<!-- .slide: data-background="/images/pyramid-5-diamond-connected.jpg" -->


Notes:

are the ones that include these other systems

---

Trail: Verdict

<!-- .slide: data-background="/images/pyramid-6-diamond-isolated.jpg" -->

Notes:

and the ones that isolate themselves from these other systems

are easy to write/maintain

---

Trail: Verdict

<!-- .slide: data-background="/images/pyramid-7-new-diamond.jpg" -->

Notes:

so I vote that we start thinking of tests in terms of connected vs isolated

because that's a better representation of when tests are easy and when tests are hard

PAUSE

choose your shape - 

a diamond where you write as many isolated as connected

---

Trail: Verdict

<!-- .slide: data-background="/images/pyramid-8-new-ice-cream-cone.jpg" -->

Notes:

or focus more on connected tests for greater confidence

---

Trail: Verdict

<!-- .slide: data-background="/images/pyramid-9-new-pyramid.jpg" -->

Notes:

or focus on isolated tests for greater control

PAUSE
