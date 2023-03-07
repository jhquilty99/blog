---
date: 2023-03-07T15:58:08-04:00
description: "Use Bureau of Labor Statistics's API to collect and analyze data about inflation."
featured_image: "inflation.jpg"
tags: []
title: "Inflation Exploratory Data Analysis"
---
While going through a period of high inflation in 2022 I started to wonder if there were trends in the inflation of certain good by regions. This could prove useful when looking looking to make major purchases for items like homes and automobiles. I created a script that would allow a user to explore different ways of visualizing the inflationary data of housing, renting a house, and the overall CPI by region. I created options to investigate the ratio between inflation indices, monthly change of the index, and the normalized value of each index. 

I noticed that each region did track generally the same movements as the countrywide index, but the magnitude of the change in different regions was more variable. In addition, there is a cyclical pattern between inflation in housing and renting. This can be thought of as the market correcting between being favorable for homeowners versus renters. My current hypothesis would be that it is a good time to buy a rental property when the housing inflation in the region has been superseded by rent inflation for the past 6 months, and that particular region is seeing lower than countrywide housing inflation. Similarly, it might make sense to rent a home when the housing inflation exceeds rental inflation and housing inflation in that region is higher than the countrywide. I will be further expanding this work and will use it to make investment decisions in the future.

Check out the repository here:
https://github.com/jhquilty99/Inflation-EDA 