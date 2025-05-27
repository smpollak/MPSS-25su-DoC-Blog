---
title: "Phase II Updates"
date: 2025-05-27
draft: false
description: "Sam updates the world on his awesome journey"
slug: "week-2"
tags: ["updates"]
authors:
  - "sam_pollak"
showAuthorsBadges : false
---

# My contribution to my phase 2 deliverable:

Data collection and cleaning proved quite challenging, with plenty of connection errors to go around. I started the week barely able to read an API response to a dataframe, and now I read multiple APIs into dataframes, cleaned data and merged into a "megaframe" that houses all of our data. The data collected by me includes GINI data, government spending by sector, population, gdp per capita, inflation, corporate tax rate, and trade union density.

The biggest challenge was cleaning our government spending data. We started with an enormous API response containing government spending data with over 65,000 rows, which I then made into a more readable dataframe. I then had to request exchange rate data and gdp data from world bank so that I could convert the government spending data from local currency to USD, then divided by the GDPs of those countries in order to get the spending groups as a share of GDP.

### Git commits:

Moved data reading file into project repo (was working on this file before in a separate repo):
https://github.com/Yasoop/GINIndicator/commit/f8618c2f0514b46810a089ef45a490a318e92b6a

Cleaned government expenditure data and converted to share of gdp by collecting exchange rate and gdp data:
https://github.com/Yasoop/GINIndicator/commit/2736994ea21264cee3d82ba4fbff56769ba5bfe2

Finished data cleaning and exported to csv:
https://github.com/Yasoop/GINIndicator/commit/f24b0d8ef570fc216fa8c1ec64535098d281acbc

Started megaframe file:
https://github.com/Yasoop/GINIndicator/commit/856ac5859a679b6ef6e8ccb04a93a1e14fedf4c0

Fixed issue with corporate tax rate data:
https://github.com/Yasoop/GINIndicator/commit/380d9dae9090187d40324181b14823ade19107ff

### Conclusion

While I experienced many obstacles in the data collection and cleaning process, I learned a lot and feel ready to move on to the machine learning aspect of the project. I have already built a logistic regression function and will be training it on the model data soon.

### Life updates:

Went to Brussels Jazz weekend on Friday! Seeing amazing jazz and RnB acts in the moodily lit grand place was awe-inspiring. Paid 15 euro for a waffle though, so it isn't all amazing (even though the waffle was quite scrum-diddly).

Went to Antwerp on Sunday with our honorary fifth group member Nipun. It was lit dingus! I ate fish and chips, saw the sights and I bought a cool jacket.