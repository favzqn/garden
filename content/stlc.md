---
title: STLC Checklist
draft: false
tags:
  - tech
  - qa
---

- [ ] Have a clear understanding of new features for each sprint, and make sure all related data/mocks are ready at the grooming session to clearly understand the impacts/Risks and proper estimations (PIC: All teams)
- [ ] Test cases to be prepared with proper coverage like positive/negative/existing features impact areas test cases (PIC: QA team)
- [ ] Test cases will be reviewed with 100% coverage by Sr QA / Leads/TPMs. (Each bug should refer to a test case)
- [ ] Unit test cases are to be prepared by the dev team and execution results are to be shared along with the Dev/sandbox Build to QA teams (PIC: Dev team)
- [ ] QA team Prepared Sanity Suite (with happy and E2E paths to all squads) and created a CI/CD pipeline to execute these scripts once a new build is triggered (PIC: SDET)
- [ ] QA team will accept the build after the build passed with 99% of test cases executed or review the failed test cases if below 99% and decide to accept or reject the build
- [ ] QA Team will start executing the Feature test cases and impact areas and errors guessing area and post bugs if any defects found
- [ ] QA Team will get a new build from the Dev team with bug fixes and Retest the failed test cases or posted bugs, making sure all test cases should be passed (98%) or all bugs (only low bugs will be accepted) to be closed.
- [ ] QA Team / Lead will give signoff the tested Features are fair enough to move to staging.
