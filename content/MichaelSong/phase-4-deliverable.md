---
title: "Phase 4 Deliverable Individual Response"
date: 2025-06-13
draft: false
description: "Phase 4 individual response!"
slug: "michael-fourth"
tags: ["reflections"]
authors:
  - "michael_song"
showAuthorsBadges : false
---

# Phase 4 Deliverable

## My Contributions
This phase, I continued to focus on our webapp by adding more role-specific features and adding mock data through mockaroo.

### Route Implementation
#### Expanded Posts Page
The expanded posts page involves a lot of moving parts, and I focused on adding routes for getting a full post, retrieving and adding posts in the expert opinion section, retrieving and adding questions and answers, and retrieving the information needed for plotly for a specific graphID. All of these routes also kept track of the logged in user and post ID, allowing different users and posts to interact together.

#### Make Post Page
I also added routes for making a post and scrolling through a user's saved graph. This involved collaborating with Sean to ensure that getting saved graphs worked in the data playground. 

#### Home Page
After I mockaroo'd more users, I also added a more robust route to get user data for the homepage.

### Frontend
#### Expanded Posts Page
In addition to making the routes, I also connected the backend and made the entire frontend for expanding a post. This included handling what goes on in the app's session state when a user goes from the Feed to Expanded Posts page. I needed to handle a complex layout, as the post description, post graph, expert opinion, and voter questions sections all needed to be correctly placed and formatted onto this page. I also abstracted some rendering code from the feed and added it to the expanded posts page.

#### Make Post Page
For the frontend, I also made the two pages necessary to make a post. This just hitting the endpoints I had created earlier and rendering a basic frontend that could take user input. I also ensured that this page was role specific.

#### Feed and Home Page
Over the course of Phase 4, I also focused on revamping the UI for the Feed and Home Page, which included making the buttons more obvious and less cluttered.

### Mock Data
I populated our feed with mock data by using mockaroo and coding CSV to SQL functions to convert the mockaroo csvs. I also populated the bridge tables that mockaroo was not able to automatically populate.