---
title: "Gold Standard Pipeline"
tags: [K6, K18, K24]
---
## Introduction

***Date:** 21 Mar 23*

It had been decided in our organisation that we would migrate our repositories from a self-hosted gitlab instance to a SaaS solution on gitlab.com.
There are a number of benefits to this but mainly you are saving time spent mangaging it. Having a self hosted instance can have some benefits mostly to do with customisation. **[K24](/tags/k24)**.

This work involved some co-ordination with a team called  delivery systems. One of the requirements made by the security team for the shift to gitlab.com was to reduce the number of actions that the deploying role could perform. That is to say, have a custom role for each terraform repository with it sown policy and restrict the number of actions it could carry out to reduce possible attack vectors.
After some preliminary research and arranging a meeting with delivery systems, we decided that this would be a large task to undertake and that it would be out of the scope of this particular project, so a ticket was raised to investigate further.

**[K18](/tags/k18)**.

For this work I adhered to a Plan Do Act Check cycle to ensure I was getting the results I required.
First, I gathered information relating to the requirements and best practices, alongside what we were already doing to deploy pipelines in the team. Then I wrote up a "Gold Standard" pipeline that all (required) terraform pipelines should match. After having written this, I ran out wrote an implementation of the standard and tested it against one of repos. There were some problems, for example some of the requirements were not possible to implement, or did not exist as features on the gitlab platform so I had to go back and modify the standard with the possibilities and restrictions of the platform in mind. From then I began the PDAC cycle again.
Affinity mapping, impact maps could have been used to plan the work, since I was carrying out most of the worl myself, in this instance I did not feel they were appropriate.
 **[K6](/tags/k6)**
