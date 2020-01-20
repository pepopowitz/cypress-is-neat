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

### **-** Many moving parts

<!-- .element: class="fragment" -->

### **-** Stateful

<!-- .element: class="fragment" -->

### **-** Data

<!-- .element: class="fragment" -->

### **-** **Tooling**

<!-- .element: class="fragment" -->

Notes:

parts: you're not just testing individual units anymore

(parts): more could go wrong

state: to complete a test, you need to put the system into a specific state; state is hard to deal with

data: 1. long-living data or 2. lots of fake data to set up/tear down

tooling - may vary depending on tech stack (rails vs js)

(tooling) - selenium

we'll circle back to this list at the end
