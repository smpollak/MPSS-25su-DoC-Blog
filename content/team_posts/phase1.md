---
title: "Project - Phase I - Proposal"
date: 2025-05-20
draft: false
description: "Our proposal for our data science project"
tags: ["project", "Setup"]
slug: "project-phase1-proposal"
authors:
  - "sean_blundin"
  - "paulo_martinez_amezaga"
  - "michael_song"
  - "sam_pollak"
showAuthorsBadges: false
---

# Proposal: Wealth Inequality App

## Project Description

**Problem:** Policymakers, civilians, and economists alike struggle to understand how economic policy—such as minimum wage, tax rates, or interest rates—affects wealth disparity. We are building an interactive app to bring data literacy in policymaking and economics to the average consumer; our app will allow users to intuitively experiment with variables such as minimum wage, unemployment, average income, or corporate tax rate to learn how each might affect wealth disparity (GINI coefficient). 

**Product:** See this [example of an AI-written frontend mockup](https://preview--gini-visualizer-prototype.lovable.app/) to understand what we envision.

Landing on our website, the user finds \~8 input cells, a “Generate” button, and an output cell containing our model’s predicted “Gini Coefficient”. The (approx.) eight fields are the features for our series of models (logistic regression, deep neural network, perhaps more) and the target variable is GINI (a measure of wealth disparity). Since our goal is to empower users to discover how different scenarios affect GINI, our intuitive experience will include presets (such as “Present-Day USA” or “1990s Russia”) which will autofill each cell with the relevant data, which can then be manually edited by the user.

Furthermore, we provide our users with a powerful graphing/visualization feature that enables users to construct graphs of how GINI is affected by the changing of a selected feature variable over a specified range and number of steps. Our product will generate a graph that displays their range along the x axis and GINI on the y axis.

## User Personas

***User Personas:** Civilian Voter, Policymaker, Economist, and Data Geek.*

### **User Story \#1: Civilian Voter** 

![Civilian Voter](/british.png)

* Persona: Prince Maximilian William-Lancelot Robertson III  
  * Demographics:  
    * Voting citizen of UK  
    * 30 years old  
    * Lives in London  
    * College degree in English   
    * High school English teacher  
  * Motivations/behavior:  
    * Watches the news occasionally, but does not follow politics much due to time constraints with his job  
    * Is unhappy with the current economic situation in the UK  
    * Does not read any academic articles or journals  
    * Browses Reddit, Twitter, and other online websites/social media  
  * Goals:  
    * Wants to be more informed about the upcoming election  
    * Would like to see a fairer redistribution of wealth in new policy  
    * Does not want to sift through dense policy papers or reports  
    * Wants an easier way to understand the way politicians will affect economic conditions  
  * User stories:  
    * As a civilian voter that lives in the UK, I want a website with information and characteristics that are relevant to me, such as being able to input the UK as a country.  
    * As a civilian voter, I want a website with straightforward metrics and measures of wealth inequality so that I can learn about how political parties might affect future wealth distribution without keeping up with economic journals and analysts.  
    * As a civilian voter, I want preset inputs, such as the state of the UK in 2001, so that I can compare current metrics to historical economic data without doing my own research about the history of the economy.  
    * As a civilian voter, I want to be able to input future years and get predicted values for the Gini index so that I can ease my worries about the uncertain direction of our country.

### **User Story \#2: Policymaker/Politician**

![Slimy Politician](/jt.png)

* JT Nance  
  * Demographics:  
    * 40 years old  
    * Works in US federal government  
    * Lives in DC  
  * Motivations & Behavior  
    * Is not a data scientist but understands economics in some capacity  
    * Likes to explore experimental policy and its consequences  
    * Interested in how machine learning or AI interprets long-term effects of policy choices  
    * Prefers practical outputs over theoretical reports  
  * Goals:  
    * Wants to better understand the long-term socioeconomic impacts of hypothetical policies  
    * Interested in scenario analysis: what would happen if the U.S. adopted a Nordic-style tax system? What if corporate tax rates were halved?  
    * Desires a digestible dashboard to explore economic outcomes without needing deep technical skill  
  * User stories:  
    * As a policymaker, I want to input policy scenarios (such as higher capital gains tax, increased minimum wage, etc.) so that I can see potential long-term impacts on income inequality and GDP.  
    * As a policymaker, I want a tool that explains economic outcomes in plain language and graphs so that I can quickly summarize insights in briefings and policy memos, while also having the flexibility to go deeper in my explorations  
    * As a policymaker, I want to compare multiple countries’ policy outcomes side by side so that I can draw evidence from real-world examples when proposing new legislation.

### **User Story \#3: Economist**

![Economist](/economist.png)

* Emeka Okonkwo  
  * Demographics:  
    * 58 years old  
    * PhD in Economics from Harvard University  
    * Works in the U.S. Department Of Treasury  
    * Is often consulted as an advisor  
    * Nigerian-American  
    * Sits through extensive briefings and reports/keeps up with economic trends  
  * Motivations & Behavior  
    * Wants to close the wealth gap, via equitable economic policies  
    * Wants to use AI models, to support his goals  
    * Wants to create visualizations to support his arguments  
  * Goals:  
    * Wants to better understand the impact of policy  
    * Wants to dive extremely deeply into different economic niches, with granular control of the details.  
    * Seeks to learn about machines’ understanding of economics  
    * Wants an easier way to understand the way politicians will affect economic conditions  
  * User stories:  
    * As an economist, I want to input a wide range of economic variables with granular precision so that I can simulate some different policy scenarios and their effects on the Gini coefficient.  
    * I want to compare predicted Gini coefficients across multiple countries and time periods to identify trends and outliers that inform policy discussions.  
    * I want customizable visualization tools to create detailed graphs that clearly communicate the relationships between variables and wealth inequality to diverse audiences.

## Models

**Linear Regression:** Built from scratch with NumPy, this model will learn from trends to yield a lightweight predictive model that will enable the functioning of our final prediction-based product. While a linear model will have the potential to yield values outside of the GINI range of 0 to 1, it will serve as a solid foundation for future comparison of other predictive models.

**Logistic Regression:** Though it’s usually used to produce a probability between 0 and 1, we seek to explore if we can use logistic regression to meaningfully predict GINI coefficient (which always lies between 0 and 1).

**Clustering:** With an automated process to detect the optimal “k”, this model will benefit our users by helping them understand the ways in which countries form into related groups. We can run a clustering algorithm per year for all countries, to examine how fringe countries move between different groups over changing years. This can help identify trends within countries’ economies over time.

**Deep Neural Network:** We seek to build a lightweight DNN in TensorFlow (or perhaps PyTorch) to test its performance vs. logistic regression.

## Data Sources

**Focusing on data for 2000-2022**

**Label:**

- Gini Coefficient ([dev info](https://datahelpdesk.worldbank.org/knowledgebase/topics/125589-developer-information))  
  - For the USA (data for 1963-2022):  
    - [https://api.worldbank.org/v2/country/usa/indicator/SI.POV.GINI?format=json](https://api.worldbank.org/v2/country/usa/indicator/SI.DST.10TH.10?format=json)  
  - For Brazil (data for 1981-2022):  
    - [https://api.worldbank.org/v2/country/br/indicator/SI.POV.GINI?format=json](https://api.worldbank.org/v2/country/br/indicator/SI.POV.GINI?format=json)  
  - For UK (data for 1968-2022):  
    - [https://api.worldbank.org/v2/country/gbr/indicator/SI.POV.GINI?format=json](https://api.worldbank.org/v2/country/gbr/indicator/SI.POV.GINI?format=json)  
  - For Argentina (data for 1991-2022):  
    - [https://api.worldbank.org/v2/country/arg/indicator/SI.DST.10TH.10?format=json](https://api.worldbank.org/v2/country/arg/indicator/SI.DST.10TH.10?format=json)  
  - For Germany (data for 1991-2022):  
    - [https://api.worldbank.org/v2/country/deu/indicator/SI.DST.10TH.10?format=json](https://api.worldbank.org/v2/country/deu/indicator/SI.DST.10TH.10?format=json)

**Features:**

- Corporate Tax Rate (OECD)  
  - [https://www.oecd.org/en/data/datasets/corporate-income-tax-rates-database.html](https://www.oecd.org/en/data/datasets/corporate-income-tax-rates-database.html)  
- Trade union density (OECD)  
  - [https://data-explorer.oecd.org/vis?lc=en\&df\[ds\]=dsDisseminateFinalDMZ\&df\[id\]=DSD\_TUD\_CBC%40DF\_TUD\&df\[ag\]=OECD.ELS.SAE\&dq=..\&pd=2000%2C\&to\[TIME\_PERIOD\]=false](https://data-explorer.oecd.org/vis?lc=en&df[ds]=dsDisseminateFinalDMZ&df[id]=DSD_TUD_CBC%40DF_TUD&df[ag]=OECD.ELS.SAE&dq=..&pd=2000%2C&to[TIME_PERIOD]=false)  
- GDP Per Capita (World Bank)  
  - [https://data.worldbank.org/indicator/NY.GDP.PCAP.CD?locations=OE](https://data.worldbank.org/indicator/NY.GDP.PCAP.CD?locations=OE)  
- Government Expenditure by Function (OECD)  
  - [https://data-explorer.oecd.org/vis?lc=en\&df\[ds\]=dsDisseminateFinalDMZ\&df\[id\]=DSD\_NASEC10%40DF\_TABLE11\&df\[ag\]=OECD.SDD.NAD\&dq=A..S13...OTE.....V..\&lom=LASTNPERIODS\&lo=5\&to\[TIME\_PERIOD\]=false\&vw=tb](https://data-explorer.oecd.org/vis?lc=en&df[ds]=dsDisseminateFinalDMZ&df[id]=DSD_NASEC10%40DF_TABLE11&df[ag]=OECD.SDD.NAD&dq=A..S13...OTE.....V..&lom=LASTNPERIODS&lo=5&to[TIME_PERIOD]=false&vw=tb)  
- Population (Worldbank)  
  - [https://data.worldbank.org/indicator/SP.POP.TOTL](https://data.worldbank.org/indicator/SP.POP.TOTL)  
- Key Short-term economic indicators (OECD)  
  - [https://data-explorer.oecd.org/vis?lc=en\&df\[ds\]=dsDisseminateFinalDMZ\&df\[id\]=DSD\_KEI%40DF\_KEI\&df\[ag\]=OECD.SDD.STES\&dq=.M.PRVM.IX.BTE..\&lom=LASTNPERIODS\&lo=5\&to\[TIME\_PERIOD\]=false\&vw=tb](https://data-explorer.oecd.org/vis?lc=en&df[ds]=dsDisseminateFinalDMZ&df[id]=DSD_KEI%40DF_KEI&df[ag]=OECD.SDD.STES&dq=.M.PRVM.IX.BTE..&lom=LASTNPERIODS&lo=5&to[TIME_PERIOD]=false&vw=tb)  
  - Unemployment?  
- Inflation (World bank)  
  - https://data.worldbank.org/indicator/FP.CPI.TOTL.ZG