# Impact of Weather Conditions on Air Quality

![](https://github.com/Ebuka456/Impact-of-Weather-Conditions-on-Air-Quality/blob/main/Weather%20Data/DA%20Scenario%201.png)

## 🛡️ Introduction
How is the Air quality affected by weather and atmospheric conditions?

This project uses an hourly data collection that includes PM2.5 data from the US Embassy in Beijing from January 2010 to December 2014 to assess Beijing's air quality and track the effects of weather and atmospheric conditions on the city's air quality.

The tools I used to perform this analysis are Python and Power Bi. I wrote an article on this project and it featured on [Microsoft Tech Community Blog](https://techcommunity.microsoft.com/t5/educator-developer-blog/data-analytics-with-powerbi-student-project-showcase-impact-on/ba-p/3747374)

## 🛡️ Background Study
According to Department of Health, New York, Fine particulate matter (PM2.5) is an air pollutant that is a concern for people’s health when levels in air are high. PM2.5 are tiny particles in the air that reduce visibility and cause the air to appear hazy when levels are elevated.

Air Quality in this dataset is determined by the level (Concentration in Ug/m3) of Particulate matter (PM2.5) in the atmosphere. According to Breeze Technologies, PM2.5 levels over 55Ug/m3 shows a poor level of air quality and above 110Ug/m3 shows a severe level of air quality. For this analysis, a limit of 100Ug/m3 was placed to signify that the air quality is getting to a severe level.

The bulk of the analysis is centered around how the concentration of PM 2.5 changes due to a change in the atmospheric condition.

## 🛡️ Data Gathering
The dataset was sourced from the academic source of [archive.ics.uci.edu](https://archive.ics.uci.edu/ml/datasets/Beijing+PM2.5+Data). The data was loaded into a Jupyter Notebook to begin the data Assessment and Cleaning process using Python.

 

## 🛡️ Data Assessment and Cleaning
The Dataset was assessed for issues with its Quality and issues with its structure. The snapshot of the data is seen below.

![](https://github.com/Ebuka456/Impact-of-Weather-Conditions-on-Air-Quality/blob/main/Weather%20Data/Capture.JPG)

The dataset was assessed visually and programmatically (using codes). Then the appropriate steps were taken to clean the data. The steps are:

- Created a Date column using the year, month and day column. After it was created, the datatype was corrected
- Handled the null in the pm2.5 column
- In the cbwd column, replaced ‘cv’ with ‘SW’ representing the South West
- The PRES column which is representing the atmospheric pressue is in Hecto-paschal. I convert the unit to atm (Standard unit for pressure) and saved it in a new column atm_pressure 
- Classified the months into four seasons
Winter — December, January and February
Autumn — September, October and November
Spring — March, April and May
Summer — June, July and August
 

The full data cleaning procedure are documented here on my [GitHub Repo](https://github.com/Ebuka456/Impact-of-Weather-Conditions-on-Air-Quality/blob/main/Weather%20Data/Impact%20of%20Weather%20Conditions%20on%20Air%20Quality.ipynb). 

The look of the cleaned dataset is shown below

![](https://github.com/Ebuka456/Impact-of-Weather-Conditions-on-Air-Quality/blob/main/Weather%20Data/Capture%202.JPG)

## 🛡️ Exploratory Data Analysis
For the purpose of exploring the data is to find patterns, identify anomalies, test hypotheses, and verify presumptions with the aid of summary statistics and graphical representations, The following Questions asked of the data are
- What can be observed about the PM2.5 Concentration with respect to time?
- Does the Wind Speed Affect PM 2.5? In which direction does the wind direction often go? Does the Wind Direction impact the concentration of the PM 2.5?
- What is the rate of Precipitation (rainfall) and Snowfall in the city especially during each season? Does this influence the concentration of the PM 2.5?
- What is the atmospheric Temperature and Pressure of the city during each season? Do they affect the Air Quality?

The Exploratory Data Analysis was carried using Python which can be accessed [Here](https://github.com/Ebuka456/Impact-of-Weather-Conditions-on-Air-Quality/blob/main/Weather%20Data/Impact%20of%20Weather%20Conditions%20on%20Air%20Quality-%20Exploratory%20Data%20Analysis.ipynb)  

## 🛡️ Data Visualization

The Data Visualization was done using Power Bi and Python. 

Check out the link to the interactive dashboard: [Interactive Dashboard](https://app.powerbi.com/view?r=eyJrIjoiMGJkNTc4ZGUtNTU3MS00NmY1LWIxYmYtNDQzYmViM2U1ZjkzIiwidCI6IjUwZDA2MjZhLTcwN2UtNDk2ZC1iOGU1LTIwYjk1NzA5MTYzZSJ9)

![](https://github.com/Ebuka456/Impact-of-Weather-Conditions-on-Air-Quality/blob/main/Weather%20Data/Dashboard_page-0001.jpg)

![](https://github.com/Ebuka456/Impact-of-Weather-Conditions-on-Air-Quality/blob/main/Weather%20Data/Dashboard_page-0002.jpg)


The wind chart was constructed using Python and It is also interactive but for some reason, it isnt displayed on power bi service. I would appreciate any recommendation on how to get past this issue. The pdf file of the dashboard can be viewed [Here](https://github.com/Ebuka456/Impact-of-Weather-Conditions-on-Air-Quality/blob/main/Weather%20Data/Impact%20of%20Weather%20Conditions%20Dashboard.pdf)

## 🛡️ Recommendations 
After gathering insights from the data, I would love to make a few recommendations
- Since the city's average PM2.5 level is normally high, I strongly advise the government to check into United State's National Action Plan on Pollutant & Control, which intends to reduce PM 2.5 (respirable, pollution particles) concentrations by 20% to 30% above 2017 annual levels in more than 100 cities. By reducing reliance on coal, limiting car emissions, expanding the production of renewable energy sources, and strictly enforcing emissions regulations, the plan promised to achieve these objectives.
- When the wind is blowing in the south-west and south-east directions, high levels of PM2.5 are seen. Tracking the sources of the pollutants and putting a stop to them will help lower the PM2.5 concentration.
- The PM2.5 concentration was seen to rise quickly throughout the winter months. This may be due to the extensive use of coal and other fossil fuels in the production of heat. When possible, I advise replacing biomass fuels, such as wood, animal dung, and crop wastes, or coal, in homes that use them for cooking and heating with cleaner fuels, including biogas (methane), liquid petroleum gas (LPG), electricity, or solar cookers..
- From the Analysis, A High Amount of hours of rain and snow shows a low level of PM2.5 levels. According to Davis Instrument, Rain and Snow can wash particulate matter out of the air and destroy dissolvable pollutants. While the pollutants are washed out or dispersed, they are not gone. They are just moved somewhere else. They end up in someone else's lungs, or dropped into bodies of water for aquatic plants and animals to deal with. It is advised that citizens who are very sensitive health-wise should refrain from excessive outdoors activities so that they would not get infected.
