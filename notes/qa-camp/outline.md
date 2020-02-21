Cypress

- intro
  - me
  - artsy
  
- Testing strategies

  - Lack of confidence in unit
  - More confidence in e2e, but they're harder

- cypress
  - architecture
    - built on mocha
    - something about chrome/electron
      - the browser itself is executing your tests
        - which makes it faster than selenium
        - tight feedback loop
        - allows you to easily intercept/mock network activity
    - NOT built on selenium
  - ide
    - time traveling
  - vs selenium
    - > Most end-to-end testing tools are Selenium-based, which is why they all share the same problems. To make Cypress different, we built a new architecture from the ground up. Whereas Selenium executes remote commands through the network, Cypress runs in the same run-loop as your application.
      - https://www.cypress.io/how-it-works/
    - automatically waits :)
    - file watching to trigger execution :)
    - debugging within chrome :)
    - not cross-browser :(

* examples

  - cy.visit
  - cy.get
  - cy.contains

* mocking

  - you can mock network responses easily
    - https://docs.cypress.io/api/commands/server.html#Syntax
    - but you probably don't want to - that just gives you a less reliable test.

* Bad tests:

  - flaky/flappy
  - break often

* Artsy

  - no QA
  - heavily automated

* Cypress at Artsy
  - integrity
    - circleci
    - no mocking
      - storing user creds
  - cypress + styled-components
    - data-test- attributes

- Best practices

  - How to keep tests from breaking often
  - same language we use for development
    - I don't know that I'd recommend cypress to a team that wasn't familiar with JS
      - having said that, it's not like you're doing COMPLICATED js. But the learning curve is a consideration
  - Don't mock things
    - or mock things, depending on your goals
  - cypress-testing-library

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

* gotchas

  - when writing a test, you're recording steps...switching on presence of specific elements isn't as obvious as you'd think it would be
    - https://applitools.com/blog/cypress-vs-selenium-webdriver-better-or-just-different
      - search for "bizarre execution"

* Resources

  - https://applitools.com/blog/cypress-vs-selenium-webdriver-better-or-just-different?utm_referrer=https%3A%2F%2Fwww.google.com%2F
  - https://medium.com/@shivambharadwaj/https-medium-com-shivambharadwaj-why-you-should-switch-to-cypress-for-modern-web-testing-5d3739a19e6
  - https://www.cypress.io/how-it-works/

* Outline for abstract

  - What is Cypress?
  - History of e2e testing (i.e. selenium)
  - Neat features
  - Shortcomings
  - Cypress at Artsy
  - Learnings

* Research
  - how to set up data before and after?

selenium webdriver vs cypress
https://dzone.com/articles/cypress-vs-selenium-webdriver-which-is-better-for
https://blog.red-badger.com/2017/6/16/cypress-a-genuine-alternative-to-selenium-at-last

cypress
v javascript only
selenium supports many languages
v chrome only
selenium supports many
^ quick setup
^ runs directly in the browser
selenium has layers between your code & the browser
you can inspect things in your console!
^ fast
fewer layers
^ reliable
fewer layers
less waiting - it automatically waits for you.
^ interactive
time travelling
^ server mocking
maybe you don't want this

colors:

#9C6742
#2D2618
#CAC6BD
#694427
#DAB07D

#fbf6d5 - extra light
#f4d0aa - light
#f29e3b - orange

1.77 = -150
1.6 = -90

calc(-6000 / (17 \* (vw / vh)) + (8070 / 17))

light: #ffce99
medium: #E66C15
dark: #BF4F1B
darker: #872C13
darkest: #420E07
