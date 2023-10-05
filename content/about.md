---
title: "About"
tags: [K18, K22, S4, S8]
---

## My Team

I am a DevOps engineer apprenctice in Hack IT and Whip IT team within Universal Credit, DWP digital.
We are the DevOps team that build and support infrastructure for products and projects on HCL2 and UC platforms.
Within our team, there is a delivery manager, team Lead, several seniors, one junior and four apprentices:

**Delivery Manager:** Lynsey Cutt

**Team Lead:** Stuart Tansley

**Senior Engineers:** Kyle Oldfield , Steve Iveson, Marco Chessa, Simon Watts

**Junior Engineer:** Royston Pierre-Pinnock

**Apprentices:** *Me*, Ben Fielding, Tom Chisholm, Sid Rahman

We work closely with the feature teams in Leeds and Manchester. These teams include developers, QAs (testing engineers), delivery managers and architects.
(**[K18](/tags/K18)**).

We are currently using the Scrum framework to organise and manage our work. That means we have decide on sprint tickets in week/two week blocks, have daily scrum meetings as well as retrospectives.

There are many benefits to this way if working especially when contrasted with a method such as Waterfall. Waterfall is linear and is focused on moving from one stage of the software development process to the next and having clear requirement from the beginning of the process. Agile methodologies (Such as Scrum) are usually focuseed on (relatively) small, incremental and iterative changes to a code base where time is time-boxed into sprints. One benefit of this way of working is that we can be very flexible, move quickly.
One potential issue with an Agile way of working is that sometimes it can be hard to make large scale changes and applications can grow in complexity in unforeseen and undesirable ways as constant small changes are made as reactions to issues or customer requests.

(**[K9](/tags/K9)**)

For example, a few weeks ago, the strategy team gave us the requirement to replace the single AWS IAM role we used to create resources in terraform with a solution adhering to the principle of least privilege.
Our project manager and team lead then decided that this would be the focus of a two week sprint.
We ultimately decided to have "minimal" policies corresponding to each AWS resource and then creating a role for each project that could assume the role needed to create the resources required (and nothing else).

This required our team to first ascertain what actions for each resource were required by each project.
I wrote a short script that analysed our terraform code and listed necessary actions.
After meeting with one of the seniors, I understood that my method was a good first start but was ultimately incomplete.
He then managed to find an existing tool that could achieve the same result in a more comprehensive manner.
He then went on to develop a process by which we could assign these policies in configuration files that manage our gitlab repositories (where our terraform was deployed from) with the assistance of a team called delivery systems (in charge of pipelines and deployments).
It was then the task of the rest of the team to align all of our projects to this new standard and modifying it where we found potential problems.

 (**[S8](/tags/S8)**).

We are a generally supportive team and endevour to share knowledge as much as possible. For example, a new apprentice joined the team recently and didn't have much experience in writing bash scripts so I said to him that I would assign him a ticket and pair with him on it. I was able to share, not only my knowledge of bash scripting but also my workflow and things that he could try. (**[S4](/tags/S4)**)

![](../posts/about/sid.png)

## My Journey to becoming an apprentice

In 2021, I had been working with one organisation for a number of years and felt like I wanted a change.
I had an interest in computers had written some simple programs. I considered that this interest might offer a potential candidate for the career change I had been searching for.
After looking on the internet, I came across this apprenticeship and I thought that being able to learn while studying would be an invaluable opportunity, so I promptly applied.

## Universal Credit

## DWP digital

The DWP is UK’s largest public service department and thus manages one of the most complex IT systems in western europe with 7.35 million benefit claims each year, paying £165 billion in benefits and pensions.

## How to navigate this portfolio

This website is divided into three sections. This is the about section. The home section will take you to a list of projects I have worked on with the relevent KSBs linked underneath.
If you click on any of these it will take you to a page that shows all projecs with the same KSBs.
If you click on the KSBs link at the top, you will see a list of all KSBs that display all of the projects that demonstrate their requirements.
Each stage is on its own branch in the github repo for **[this site.](https://github.com/barringtonbrook/barringtonbrook.github.io)**
