---
title: Reevaluating the concept
date: 2026-05-04
author: Aditi Saligrama Hegde , 550292362
summary: Short description
tags:
  - narrowing the idea
  - new target audience
  - sitemap
---
# My third blog -  Reevaluating the concept and new directions 

## Narrowing the Idea
The concept has changed since the last blog. We started with a broad creative hub for anyone with a creative project idea - designers, musicians, filmmakers, etc but after revisiting the brief and understanding the depth of the project, we decided to narrow our target audience to designers. The decision was made based on risk management, with things like ease of user testing and ease of coding the project in mind. 

## Reevaluation and why
The brief originally asks for a community that feels tailored rather than generic. A hub that serves everyone might not work for this short period, as it would just mimic already existing platforms. By restricting the platform to designers specifically like brand, ui/ux, motion, etc, each feature on the platform becomes more intentional and niche. Our main goal is for designers to partner up with fellow designers to work on projects that they can showcase on their portfolios and gain collaborative experience. The tags will work as a filtering system to show the particular discipline of design that the user might be interested in. 

## The Scope: 
Two features from the previous concept were removed. I suggested the removal of Spark Score, the unique ranking system that would have been built from rankings, nudges and recency and replaced the idea with a simple star system rating that applied to completed and shared projects. The logic behind implementing that system was risky because it would require three separate events that each triggered the recalculation cycle, which could introduce bugs and would be complicated to implement in such a short amount of time. A simpler system would assure a working system and still deliver the same intention. 

The completion vote system that required all members to individually confirm the project was also cut. The collective decision was made as it would add a whole database table and multi-user coordination that could be indefinite if one member were inactive. We decided that the owner marking the project complete was sufficient. 

These changes were made to make our features work and be reliable within our ability to code, rather than ambitious wishes we weren’t able to fulfil. 

## New Checklist feature: 
We redesigned the five-phase build tracker with a simple owner-defined checklist. The owner adds up to six items, the team ticks them off, and a progress bar updates live. When all the items are completed, the owner can complete and share the project on the showcase page. 
This aims to serve the same project accountability but with a simple and straightforward database structure: one table, one boolean column per item and one COUNT query for the progression bar calculation. 

## Pages: 
1st Page- Home / Feed
2nd page- Post a pitch
3rd Page- pitch details
4th page- manage applicants
5th page- build a checklist with complete and share
6th page- showcase
7th page- my profile for users

## Sitemap: 
Version 1: 
![Sitemap Version 1](assets/images/SitemapV1.png) 






