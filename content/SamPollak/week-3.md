---
title: "Phase III Updates"
date: 2025-06-05
draft: false
description: "Sam updates the world on his awesome journey"
slug: "week-2"
tags: ["updates"]
authors:
  - "sam_pollak"
showAuthorsBadges : false
---

# My contribution to phase 3:

This week has been an emotional roller coaster in creating our ML model. At first, our logistic regression model was somehow yielding a cross-validated r2 score of -31, and then overnight it seemed to switch to a very normal .47. By playing with the alpha and max iterations, we managed to get a cross-validated r2 score of .633. The linear regression model performed slightly better, with a cross-validated r2 score of .644.

This week, my contributions started with making slight changes to the data. I resolved an issue where all our countries had the same inflation, gdp per capita, population and GINI data - turns out I hard-coded Australia into the API requests from world bank - oops. I also downloaded a csv containing countries by region and implemented it into the megaframe.

Then, I wrote the code to read the data, standardize it, create the models, export the weights to csv, exports the means and standard deviations to csv so that test data can be standardized, cross-validated the models, and then created residual plots to examine for assumptions. These efforts were primarily led by me, though Paulo did offer a significant helping hand.

I also made a function in predict.py to predict the GINI index based on inputted X values.

## Git commits

My git commits are too numerous to put all of them here, but I will link some of the most important ones:

committed various changes related to data reading:
https://github.com/NEU-Khoury-DoC/25su-DoC-Project-Template/commit/d0b1befa26500644ec51a29528512e08ad4737b5

fixed issue with duplicate data:
https://github.com/NEU-Khoury-DoC/25su-DoC-Project-Template/commit/348f972946976e79126f719236587eb799451879

Added region to megaframe, removed indices from megaframe, started log model notebook:
https://github.com/NEU-Khoury-DoC/25su-DoC-Project-Template/commit/7af530a291ffeeec9b0e565967fe4cc84af21f90

created logistic and linear model:
https://github.com/NEU-Khoury-DoC/25su-DoC-Project-Template/commit/bedd377f0a855525ddce9626f1b21267df619d87

refined logistic regression model and exported model weights to csv:
https://github.com/NEU-Khoury-DoC/25su-DoC-Project-Template/commit/f1b2571a11a73b33db6a0f1b125f1b70c54de898

Polished log models notebook and created prediction function:
https://github.com/NEU-Khoury-DoC/25su-DoC-Project-Template/commit/a8673a622eb7dbd3066aad91987d338cfdfb8357