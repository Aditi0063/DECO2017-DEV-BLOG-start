---
title: Design Idea and New Direction
date: 2026-04-26
author: Aditi Saligrama Hegde , 550292362
summary: Combining ideas and making a new concept 
tags:
  - group dicussion
  - idea generation
  - main concept
---
# My second blog - Beans and our design idea

As a group (Beans), we decided to bring in three separate concepts and find either one idea that worked or one unique feature for us to start with. All the ideas had their own strengths and weaknesses:  

## Idea 1: Music Collaboration Platform 
The music platform had the most unique concept, but required Web Audio API knowledge and was way beyond our current stack and skillset. 

## Idea 2: Startup Project Builder 
The startup builder platform had a good structure, but felt too corporate and had various other replacement platforms existing. 

## Idea 3: Indie Game Review (mine)
I brought the indie game idea instead because it was slightly more unique, because of the target audience and was simpler to make in terms of the scope.
The indie game review platform had a simple plan, but the community is too narrow for user testing, and after leaving the review, there was no incentive to keep the community coming back for more. 

What emerged was borrowing different ideas from each and then combining and reevaluating to create a platform - a hub for creatives where they pitch short-term projects, build a real team and finish them together. 

## The Concept: SPARK - Pitch the project, rate, team up, build and share with the community!

### The Score System: 
To create a more unique experience, ideas accumulate a score that is a composite of community ratings, nudges received and recent activity. When ideas cross a threshold, they earn “Hot Idea” status in a weekly spotlight section. This matters because a static feed doesn’t retain users and give them a reason to return. A dynamic ranking helps reward the quality of ideas and promote engagement. 

### Teams: 
The team formation uses role-based slots rather than open collaboration for all. The poster defines exactly who they need, like “1 designer and 1 writer needed” with each slot displayed as open or filled. When the designer nudges the poster, they get to specify the exact role they are applying for, and the creator either accepts or declines per slot, giving them the freedom to choose their teammates. Once all the roles are filled, build mode is activated. 

### Build mode: 
We are aiming to make this our core function. The team moves through five structured phases - Ideate, Plan, Build, Post and Reflect. 

### Scope: 
- MUST: Posting the pitch with tags and role slots, Spark Scores, nudge system, discovery feed, build mode phase tracker, outcome card and badge on completion. 
- Can add later: The weekly spotlight feature, advanced feed filtering, and emoji reactions on outcomes for building onto the community aspect. 

### Potential Risks: 
The Spark Score system is the highest technical risk. Tracking ratings, nudges and recency simultaneously will need a significantly complicated backend. It will require three separate data points triggering a recalculation on every interaction. This has a high possibility of introducing bugs and becoming unstable in the future. 

### Accessibility: 
Star ratings and nudge buttons will need aria-labels for screen readers, AA contrast and visible text labels. The progress bar will need to announce the percentage of completion. 

### Next Steps: 
Our concept is currently very ambitious, whether all of it is buildable with our stack is the next question. The next post will focus on feasibility, creating our sitemap and understanding user flow. 
