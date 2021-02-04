<!-- cSpell:ignore  MTTR,-->

# Describe components for CI/CD pipeline

## Overview

### Continuous integration

* Developers continually merge branches with the main branch to stop merge conflicts
    * Testing of code should be done before pushing the branch back to master
* Some large feature additions may require a big commit, but in general smaller changes should be pushed frequently

### Continuous delivery

* Short sprints so code is always deployable
* Testing be thought about in advance - test often and in an automated approach as part of CI/CD infrastructure 
* If a bug is found, or a vital floor in the code is discovered, development is stopped until it is fixed - the code must be in a deployable state

![](../img/2021-02-04-06-13-48.png)

### Continuous deployment

* Made, tested, integrated with main branch and test again
    * As code is pushed to production right away - your users are your final testers

#### Limit impact to users

* By doing rolling upgrades, if issues are found, you can push the fix and no one has to reinstall the software
* Canary pipeline is a subset of users - almost your guinea pigs. If they don't find any issues, you can push to production
* Blue-green deployment means that the old code is held in reserve - if issues are seen users can be diverted to the older code which should be stable and working

## CI/CD benefits

* Integrates nicely with Agile
    * Agile has sprints, similar to CI/CD
* Shorter mean time to resolution (MTTR)
    * Changes are small - so it's easier to isolate faults
* Automated deployment
    * Testing and deployment is automated (or can be)
    * Blue-green deployments are easy
* Less disruptive releases
* Improve quality
    * Everything is tested often and fast
    * Fault resolution is easier and quicker
* Improved time to market