#### CI/CD

1. What Is CI/CD?
    * Continuous Integration Continuous Delivery
(continuous monitoring and automation right from tests to deployment) <br>

This is std practice for businesses that frequently improve apps and require reliable delivery process. CI/CD help teams focus more on enhancing apps than details of delivery to other envs.
__CI/CD Pipelines__ are CI/CD practices or guidelines that app devs use to deliver code changes more frequent and reliable.

> __Build__ > __test__ > __automate__ > __auto release to repo__ > __auto deploy to prod__

2. How does CI improve collaboration and code quality?
    * Teams practicing CI use rules (eg.precommit, github actions) to control what features and code are production ready.
    * Committing small code at a time into version control frequently also allows easy detection of defects/ software quality issues. Shorter commit cycles guarantee less code review/ modification from other developers.

3. CI/CD Tools
    * Supports integration w/ third party platforms, ui, admin'n, source code mgt to build mgt.

    * CI/CD automation will help store env vars to be pkgd w/ dekivery and make the service calls to web servers, dbs, or services that need restarting 

    * Can use Containers or Serverless arch. to deploy and scale apps.
      * Containers allow to pkg and ship apps
      * CSP provide the infrastructure needed and resources the app consumes based on its config.

__Take Aways__
  * Implement CI/CD guidelines/ practices when collaborating on projects for smooth delivery.
  * Hide passwords and everything discrete/ secret in environment variables.
  * Set-up linting & tests passings locally too. Eg w/ Pre-commit, unit tests etc.
  * Push code frequently in smaller pieces for clarity.
  >Best practices to push smaller codes, easy to id mistakes even before github actions reruns it
  * Set-up Github actions to test project from dependencies to unit to       integration test to sieve and correct errors.
  * Set it up to auto deploy to cloud when everything passes.
  >Set up the 'final src of truth' branch to auto deploy to cloud,
  > also to avoid the hassle with manual deploy after every change. Continuous deployment relies heavily on well-designed test automation, so an app can go live if it passes all required tests to function properly.

