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
