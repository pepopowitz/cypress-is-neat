---
<!-- .slide: data-background="/images/testing-pyramid.jpg" -->

Trail: Testing Strategies

Notes:

Testing strategies

- Mike Cohn, Succeeding with Agile, 2009
- opinions over shape, names of tests, validity, etc
- but it's still a useful metaphor to talk about tradeoffs in testing
- explain types of tests


---
<!-- .slide: data-background="/images/testing-pyramid-tradeoffs.jpg" -->

Trail: Testing Strategies

Notes:

it's a pyramid because there are tradeoffs

1) cost: to write & maintain
2) speed
3) reliability: how often does this test fail or break?
4) confidence: how confident about your app?

- lower in the pyramid is better for first 3
- higher in the pyramid is better for last 1


---

Layout: list
Trail: Testing Strategies

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

4) tooling - may vary depending on tech stack (rails vs js)

focus on tooling

but we'll also circle back to this list at the end
