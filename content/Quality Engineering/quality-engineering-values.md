---
title: My Quality Engineering Values
draft: false
tags:
  - tech
  - qa
  - values
---

Disclaimer: This list reflects my opinions and what I currently believe to be best practices based on my current knowledge. Remember that opinions may vary, and it's always a good idea to seek alternative perspectives and information.

- Test all the time
- [[Quality]] is everyone’s responsibility. QA Don’t need to do sign-off (but at team level decision) Quality Engineers were tasked with ensuring that their teams understood the current state of [[quality]] for a given feature or product, helping to build the team’s confidence in their decision.
- Invest in automation as soon as you can (priority). E2E tests are good but also beware of the testing pyramid.
- Shift testing to the left
- Create a good bug report: At least bug reproduce steps, screenshots/videos if possible, a clear description of actual & expected outcome, and version
- Don't focus only on functional, but also on UI/IX, performance, security
- Automation Benefits:
  - Manual testing hours saved by automated tests
  - Salary savings because hiring too many manual testers
  - Enhanced post-release risk mitigation
- Automation Investments:
  - Building an automation team or using 3rd party testing tools
  - Building automation framework and scenarios
  - Maintenance expenses
- Automation ROI: Savings - Investment / Investment \* 100

**Example:**

Investment Benefits:

- Hours Saved: 100 hours/month
- Money Saved on Salaries: $5000/month
- Avoidable Expenses: $2000/month

Total Benefits = 100 hours/month + $7000/month

        Investment Costs:

        - Cost of Building Automation Team: $20,000
        - Maintenance Expenses: $1000/month

        Total Costs = $21,000

        Calculation:

        - Subtract Costs from Benefits: $7000/month − $21,000 = −$14,000
        - Divide Remaining Amount by Costs: -$14,000 / -$21,000 = 0.6667
        - Multiply by 100: 0.6667 * 100 = 66.67% ROI

### Best Practices

- Decide which features should be automated
- Choose stable features to automate
- Anticipate execution time.
- Consider parallel testing
- **Dismissal spree**. You can’t rely too heavily on any software engineer or QA tester. If they leave, you lose a wealth of technical knowledge, and it may cost a lot to heal the wounds. However, automation can help prevent this by minimizing reliance on the manual skills of a single employee.
- Unit Test Cases:
  - The dev team executes unit tests before pushing builds to the dev environment.
  - Reports on executed unit tests are shared with QA/Product teams.
- Test Cases:
  - QA writes effective test cases covering positive and negative scenarios.
  - Test cases are based on feature behavior and impacted areas.
  - Positive and negative test cases align with the RTM Matrix.
- Test Cases Review:
  - The review involves the Sr QA/QA Lead/Product Manager/Dev Team.
  - Test cases are updated based on feedback received.
- Sanity Testing:
  - QA conducts sanity testing post-build deployment to the Dev environment.
  - Acceptance or rejection of the build is based on sanity testing results.
  - Sanity testing is automated via a CI/CD pipeline.
- Feature Testing (on Dev.):
  - QA performs thorough testing on the dev environment for each sprint's new feature.
  - Bugs are raised on JIRA.
  - Test cases are executed, and defect reports are provided.
- Integration Testing:
  - Integration test cases are created and executed on staging builds.
  - Confirms proper integration of all modules/tech family features.
- Regression Testing:
  - A regression suite is created/maintained for end-to-end flows and impacted areas.
  - Feature testing is conducted again as a second round.
  - Test cases are updated to ensure they are up to date.
- Testing Priority/Cross Browser Testing:
  - Test cases are verified based on customer priority view.
  - Cross-browser testing ensures feature compatibility.
    | Browser | Device |
    | ------- | ------- |
    | Chrome | iOS |
    | Firefox | Xiaomi |
    | Safari | Samsung |
    | Edge | Oppo |
- Additional Testings:
  - Performance and security testing are introduced for each release.
  - Mobile testing includes various aspects like installation, battery usage, CPU, network 2g/3g/4g/wifi, and screen resolutions.
- UAT/DOD (Product Demo) to stakeholders:
  - A demo of each sprint feature is given to Product Leads after staging.
  - Demo serves as the Definition of Done (DOD).
- Build Verify Testing (on production):
  - QA verifies all released features on production with BVT testing.
  - Ensures features are live and functioning properly.
- Prod Issues/Fast Tracks:
  - Prod issues are treated as a very high priority.
  - RCA is initiated promptly.
  - A war room may be created for quick resolution.
  - Issues are tracked and resolved within the running or next sprint based on complexity.
- Patch/Hotfixes:
  - Prod issues are resolved as patches/hotfixes based on business impact.
- **Efficient Selectors Usage**:
  - Utilize Fast Selectors like ID, Class, Name, and Type.
  - Prefer static IDs over dynamic ones for better stability.
- **Atomic Tests Creation**:
  - Write small, atomic scripts for easy troubleshooting.
  - Limit each test to a single functionality with up to 20 steps.
  - Atomic tests facilitate clear identification of failures.
- **Avoid Redundant Testing**:
  - Prevent repetitive testing of the same functionality.
  - For instance, log-in and logout procedures don't need to be reiterated in every test.
- **Create Effective Tests**:
  - Prioritize speed in test execution.
  - Eliminate step duplication to streamline scripts.
  - Maintain independence among tests.
  - Include only the essential steps necessary to reach the desired outcome.
  - Remove extra steps unrelated to the final result.
- **Optimized Waiting Strategies**:
  - Prefer Explicit waits over Implicit waits.
- **Utilize Headless Browsers**:
  - Employ headless browsers for UI tests to enhance execution speed.
  - Expect a performance boost ranging from 2x to 15x compared to traditional browsers with GUI.

### Metrics

- **Test Case Coverage:** This metric indicates the percentage of effective test case coverage by QA.
  Test Case Coverage % = (Number of test cases added by reviewer / Total number of test cases) x 100
  (Target: Test coverage should be 99%)
- **Test Case Execution:** This metric determines the percentage of test cases executed.
  Test Case Execution % = (Number of test cases executed / Total number of test cases written) x 100
  (Target: Test Execution % should be 98% to 100%; All P0 Test cases should be executed)
- **Test Case Pass Rate:** This metric shows the percentage of test cases that have passed among the executed ones.
  Test Case Pass Rate % = (Number of Test cases Passed / Total number of Test cases Executed) x 100
  (Target: Test Passed % should be 98% to 100%; All high priority TC should be passed)
- **Test Efficiency / Defect Removal Efficiency:** This metric reflects the efficiency of the testing process in identifying defects.
  Test Efficiency % = (Number of Defects found during QA testing / (Number of Defects found during QA testing + Number of Defects found by End-user)) x 100
  (Target: Test Efficiency % should be 95% to 100%)
- **Defect Leakage:** Defect Leakage measures the proportion of defects missed during QA testing and appearing in production.
  Defect Leakage % = (Number of Defects found at production / Number of Defects found in QA testing) x 100
  (Target: Defect Leakage % should be 0% to 5%)
