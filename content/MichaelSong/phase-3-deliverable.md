---
title: "Phase 3 Deliverable Individual Response"
date: 2025-06-04
draft: false
description: "Phase 3 individual response!"
slug: "michael-third"
tags: ["reflections"]
authors:
  - "michael_song"
showAuthorsBadges : false
---

# Phase 3 Deliverable

## My Contributions
This phase, I focused on building the API routes and frontend of the site, particularly the routes for the landing page, feed, and model predictions, and the frontend for the feed.

### API Route Planning
With Sean, we mapped out all of the routes that we would need for our web app, which we've been referencing as a working list of routes to implement. This has really helped us with making blueprints too, as we're able to more easily divide the routes and divvy up work. I also did much of the work for putting together the REST API Matrix.

### Route Implementation

#### Landing Page
Collaborating with Paulo, who made the initial frontend of the landing page, I created the GET route to get the user information and cache it in the user's session state. I then connected this to the fronetend.

#### Feed
One of the more time-consuming routes, I implemented the GET route to populate a user's feed with posts. This included adding parameters for filtering and sorting posts. Working with Sean, who made the PUT and DELETE requests for when a user upvotes and unupvotes a post, I made the remaining PUT and DELETE requests for downvotes, endorsements, and bookmarks. Using all of these routes, I made the frontend for the feed and connected it to the routes.

#### Model Prediction Generation
Finally, I created the route to generate model predictions for both the feed and the data playground, which involved a lot of communication with Sam, who made the model prediction python function, and Sean, who made the data playground frontend. I also needed to wrangle a lot of data, such as setting up the model weights and describe metrics for the database.

## Reflection outside of the project
This past week was a lot of work, but I still managed to go to Liege, which was a lot of fun and I got the best waffle I've ever had.