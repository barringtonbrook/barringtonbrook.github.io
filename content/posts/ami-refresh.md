---
title: "AMI refresh automation project"
tags: [S4, S13, S21, K9, K20]
---


## Introduction

***Date:** 12 Dec 22*

Every 2 weeks a new *Amazon Machine Image* (AMI) is generated and when this happens we need to update all of our instances with this new AMI.
This can be quite a time consuming job so it was decided in a team day towards the end of the year that we would find a way to automate it.

### How did we get the ticket?

After a brainstorming/whiteboarding session discussing what we wanted out of this piece of work, it was decided that the work would be carried about by me, another apprentice and a fast streamer. **[s21](/tags/s21)**

### Our way of working

The work was coordinated through a mix of meetings slack channels, group calls and messages. We paired and shared information between each other to form an effective team and complete the work using our collective skills.  **[s4](/tags/s4)**  **[s13](/tags/s13)**  **[k20](/tags/k20)**

### The work

We initially considered using Gitlab pipelines but the security team had not had chance to fully review Gitlab Ci/CD as a solution so we had to consider other possibilities. **[k9](/tags/k9)**
![](../ami-refresh/security.png)

I wrote some terraform to set up the necessary infrastructure for our lambda solution, below is the page where you could change variables to allow configuration of the times that the lambda ran by service and by environment.
![](../ami-refresh/terraform.png)

## Conclusion
