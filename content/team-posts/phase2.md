---
title: "Phase II"
date: 2025-05-27
draft: false
description: "Our proposal for our data literacy app"
tags: ["project", "updates"]
slug: "phase-2"
authors:
  - "sean_blundin"
  - "paulo_martinez_amezaga"
  - "michael_song"
  - "sam_pollak"
showAuthorsBadges: false
---

# Phase II \- Blog Post 2: Deliverable 2

## Executive Summary

Perhaps unsurprisingly, the direction of our project has radically changed since our last post. What began as a lightweight data visualization app has been expanded into a “stack overflow of policymaking”, if you will—a social, interactive discussion board where policymakers, voters, and economists can voice their opinions through user experiences that are meaningfully tailored to each persona. Furthermore, each of their experiences are deeply linked to one another, connected in ways that suit each persona’s needs and desires. Such an undertaking has taken considerable effort on the part of all members of our capable team.

*See the full updates in our plan reflected in our [updated Phase I post](../phase-1).*

**Updated Product Description:** Policy papers are frequently black box and inaccessible, often missing voter and data-backed perspectives. Additionally, it is hard to know how economic factors, such as corporate tax rate or government spending, will affect abstract characteristics such as wealth inequality without doing complex analyses or spending a lot of time.

## Key Updates

* **Drastically expanded scope; data viz app became a policy discussion board**  
* **Adjacently… New data sources, user stories, & database schema**  
* **Overhaul of Menu System on our Team Blog site**

*Reminder: Find full updates reflected in our [updated Phase I blog post](../phase-1)*

## Timeline of Updates

Seven days ago, our product was a simple data visualization tool. Such a simple product yielded a very straightforward database design. Knowing that our professors expected more from us, we took our simple mockup to Dr. Fontenot. His ensuing comments made it clear that our current product was far from adequate, setting off a four-day period of rapidfire team debate, product development and database design, only to repeat the process again. Such a cycle yielded the following evolution:

* We were informed that the scope of our project had to be greatly increased.  
* Frustrated, we discussed changes to our core product as a team.  
* The product evolved from a visualization app to a lightweight discussion board.  
* We added new features to the roadmap, such as the ability to “post” graphs  
* We took our revised idea back to our professors; they told us to reach for the moon with product design.  
* The complexity of our app continued to significantly expand as we discussed features such as saving graph metadata, adding community moderation, politicians “endorsing” posts, and replying to posts with graphs rather than plain text.

Although we were initially disappointed that our carefully crafted app idea was dismissed as too limited in scope, we’ve come to appreciate the final result which we have worked towards diligently. It is clear in retrospect that we had been limiting ourselves by focusing too hard on feasibility rather than creativity. With the benefit of hindsight, it’s clear that our initial idea was too simple, and we ultimately made the right decision to drastically expand the aim of our product.

## Data Visualization Models

### Line Graph of Unemployment & Long-Term Interest Rates Over Time

![Line Graph One](/Plot_UNE_ITR.png)

To examine trends in our dataset, we created a line graph of unemployment and long-term interest rates by country over time. We wanted a time series, and wanted to examine how the variables above would change overtime. We also wanted to examine the different trends between nations over time. Which they all showed similar variance. And to top it off, plotting both of them would allow us to examine possible relationships between the two variables.

### Distribution of GINI Index by Country Over Time

![Histogram Graph One](/Plot_Gini.png)

Another plot we made was of the GINI Index distribution by country. Through it, we could see that each country varies around a certain level of inequality with a roughly similar variance. 

### Pairplot of All Feature Variables

![Pairplot Graph One](/Plot_Pairplot.png)

Additionally, we explored the relationships between features by creating a pair plot, with the intent of sleuthing out any potential collinearity between features. The pair plot raised some concerns surrounding some data that may be static for each country. This could create limitations for our model, and may mean we have to go back through our data collection methods and make sure it is robust. The reason we did a pairplot was to look for colinearity between variables, and our pairplot showed us that there was no collinearity which is a good sign. In phase 3 we should further examine outliers in the pairplot.

## Machine Learning Models

We have not yet implemented any machine learning models. Soon, we will be implementing our logistic regression model to predict the GINI coefficient based on the other features. Evaluation and interpretation of our model is different from a typical logistic regression model, since we are not actually predicting the probability of  a value of 0 or 1, but instead predicting a value between 0 and 1\. This means that we cannot evaluate our model with accuracy, precision or recall, but rather with some proximity metric such as mean squared error.

# Entity Relationship Models

## Local Models
*Due to the highly interconnected nature of our personas' experiences on our app, each of our local models are remarkably similar to one another. Most of the meaningful differentiation lies in the few changes in schema hidden in a sophisticated and highly connected schema—this schema fuels the core functioning of the app, such as ensuring every post has a politician name attached to it, even for the  voter's local ER diagram*

### "Voter" Persona

*As the most lightweight level of privelege, Voters have the lightest ER Diagram.*

![Voter ER](/ER_Voter.png)

### "Politician" Persona

*Politicans have higher priveleges than a Voter. For example, in the ER diagram, politicians can create posts whereas Voters cannot.*

![Politican ER](/ER_Politician.png)

### "Economist" Persona

*Economists represent the verified "experts" that have a special level of privelege to leave comments on Politicians' posts. For example, in the ER diagram, Economists can yappasdfpasdpfpasdfp.*

![Economist ER](/ER_Economist.png)

## Global Model

![Global ER](/ER_Global.png)

## DDL
![Global ER](/ER_RELATIONAL_MODEL.png)