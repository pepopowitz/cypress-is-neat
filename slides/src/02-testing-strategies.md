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

we'll talk about all of the pyramid a little later, 

but for now we're going to focus on the top of the pyramid (e2e)

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
