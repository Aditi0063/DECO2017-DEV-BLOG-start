---
title: A3 Reflection
date: 2026-06-9
author: Aditi Saligrama Hegde
summary: Reflectively assessing A2
tags:
  - user experience evaluation
  - performance and functionality
  - lessons
---
# Performance Evaluation 

Reflecting on our development and ideation process, the technically challenging moment was the image upload bug. The goal was straightforward: to store an uploaded image against a project and serve it back on the feed and pitch details page. The root cause was the MojoJS constraint with saveFile(), and ctx.parms() both consume the HTTP request, so calling them in the wrong order dropped either the file or the form field with no error displayed, but the form was infinitely loading. Instead of rebuilding the system, my tutor explained to borrow from what the demo in BlaBla Corp offered, calling saveFile() before ctx.parms(), which helped resolve the issue. 

Another issue was that the fresh installations of the app would crash on the feed page with feedback like “no such table:projects: because the user table was auto-created, but all the other tables existed if  schema.sql was run manually. This wasn’t documented in the readme, so teammates couldn’t run the app without deciphering the error message themselves. This gap caused some confusion but helped us develop a thorough readme file for the submission. 

The badge feature was not shipped due to a few reasons. The main idea was to award designers recognition based on their ratings on completed projects in the showcase. We didn’t design the database to support this during the planning stage. We would have had to create a badge table and a user_achievement table, and adding them in later stages of development would have meant redesigning our ERD and DDD, and we wouldn’t have been able to test the feature out in the remaining time. This is something I’d approach differently next time.

## Lighthouse Inspection 

Performance scores ranged from 96 to 99 with our FCP and LCP within the brief’s 3-second maximum. The pages with slightly lower performance scores, especially with the Feed page - 96, My Projects and the Showcase page - 98, are the ones with user-uploaded images. Lighthouse test flagged up to 651 KIB of potential savings from the Feed page as consequences of not processing images at upload time. By contrast, Application, Profile and Post a Pitch scored 99 as they do not load images dynamically. Render-blocking requests (~90-730ms) appear consistently across all six pages, pointing to the overall CSS stylesheet being excessive.



# User Experience and Accessibility

## User Experience (The Flow & Interactions)

The initial project focused on creating only one user flow path of being the owner of a project, but when we tested with multiple accounts, it became clear that the collaborator experience was entirely unaccounted for.  A collaborator viewing the checklist would see the same controls as an owner, including the publish button. Fixing this required substantial rework across the checklist controller, My Projects page and Applicants page to include an isOwner flag pressed through all the relevant templates. This was done to support both roles for giving users the flexibility to decide what they choose to do with Folio Hub.

Two smaller interactions that improved usability were: the “Interest sent” confirmation was added after applying, as the previous iteration had the user clicking the button with no feedback, and the button remained, which confused users. The HTMX state change gives the user clear confirmation without a page reload. Similarly, the published project lock was created to place all completed projects in a showcase to prevent a confusing state where users could continue editing something already public. 

The Current/Applied Projects dropdown on the My Projects page solved the problem of users only viewing their project. This gave them the ability to view projects that they applied to, the status and the pitch.


## Accessibility (Lighthouse & WAVE)

Our project has scored an average of around 95 on our accessibility scores, with the lowest being 90 on the profile page due to the tab panel switching using JavaScript not including proper aria attributes. 100 on Best Practices across all pages. 

The main issue is contrast errors throughout the project, where the buttons or the tags are said to be low contrast and are at risk of falling below the WCAG AA guidelines. This design choice was done to create a muted tone for the secondary text. Using a darker text colour would help resolve this issue while still following the colour theme. All images have alt text with aria labels to ensure an accessible application. 

For future development, we could have gone beyond regular accessibility aspects and made the application keyboard-friendly as well.


## Usability gaps

There is no pop-up notification when a pitch is posted, nor is any notification received when a user is selected for a project. This was an aspect overlooked while creating the project. These are small details to consider, but they could have made a difference in the user experience. 

There are no error states on the forms in case a form fails. The user only receives a server error page rather than inline validation feedback, which shouldn’t have been overlooked. This can create problems in usability, and the users will be at risk of troubleshooting.



# Functional Requirement 

The core feature loop was shipped as intended - pitch posting, applying to projects, accepting and declining applicants, checklist progress tracking, multi-image upload, showcase page with star ratings and session-based authentication. The project status flow goes - open → checklist → completed → published; the owner/collaborator distinction is fully functional across all relevant pages. 
