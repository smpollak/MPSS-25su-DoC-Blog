---
title: "Phase III"
date: 2025-06-05
draft: false
description: "Updates on the development of Consensus (patent pending, trademark, copyright)"
tags: ["project", "updates"]
slug: "phase-3"
authors:
  - "sean_blundin"
  - "paulo_martinez_amezaga"
  - "michael_song"
  - "sam_pollak"
showAuthorsBadges: false
---

# Phase III \- Blog Post 3: Deliverable 3

## ML Model

### Dataset tweaks from last phase:

We noticed from our phase 2 pair plot that something was suspicious about a lot of the data matching. Sure enough, our data collection function from world bank was collecting the data from Australia over and over again and assigning that data to each country. That issue was an easy fix.

From phase 2, most of the features of our model remain the same, however upon exploring the data, Costa Rica and Colombia appear to be outliers in the GINI index, so we decided to include regions of the world as a feature to account for these differences. We sourced this data from world bank by downloading a CSV so that we could classify each country to a region and create dummy variables for the regions in the data. (No we didn’t use an API, yes Dr. Gerber said it was okay.)

### ML Features:

The features for our machine learning model are primarily government policy numbers and economic indicators that we hypothesized would have some causal connection to the GINI index. Another reason we chose the datasets we chose is because they are plausible indicators that a policymaker would tweak. 

The OECD datasets we used include trade union density, combined corporate income tax rate, government spending on education, health, housing and community development as a share of GDP, Long-term interest rates and unemployment. From the world bank we got data on inflation rates, GDP per capita, population, and the GINI index. Exchange rate and GDP data were also collected from world bank to derive government spending as a share of GDP, since the original government spending data was in local currency.

### Model Results:

The models work surprisingly well! Our logistic regression model had an R^2 score of .741, or .633 when cross-validated. The linear regression model had an R^2 of .763, or .644 when cross-validated. That being said, there undoubtedly are issues of heteroskedasticity and autocorrelation in the model.

![Residual Plot vs. Order](/ResidPlotOrder.png)
Our data is grouped by country and then ordered by year. As the graph demonstrates, you can see the residual's of an individual country increase or decrease steadily over time. This suggests significant autocorrelation in the data.

![Residual Plot vs. Unemp](/ResidPlotUnemp.png)
![Residual Plot vs. Trade union density](/ResidPlotUnion.png)
![Residual Plot vs. GDP per capita](/ResidPlotGDP.png)

These 3 plots demonstrated the most clear-cut forms of heteroskedasticity in the data. As you can see from the graphs, the variance of the residuals depend on the x feature. 

On the bright side, the relationship between the x values and each residual seems fairly linear.