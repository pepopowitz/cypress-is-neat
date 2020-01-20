---

- verdict: Is it a replacement for selenium?
  - No, I don't think so. Not yet.
    - it's another TOOL
    - it can be really useful to get you to a place where QA and engineers are working in the same tests
    - it can give engineers more confidence in their changes
    - but it still lacks cross-browser testing
    - It makes it easier for engineers to write e2e tests, which can end one of two ways:
      - no need for qa
      - engineers & qa can share tests
      - which you end up following says a lot about the relationships of your organization.

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

