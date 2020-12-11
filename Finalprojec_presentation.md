Predicting farmer's profits in rural Kenya
========================================================
author: Giuliana Daga
date: 12/02/2020
autosize: true
Problem statement and background
========================================================

- Client: The product is piloted by Agriculture and Climate Risk Enterprise (ACRE), working in Kenya since 2009.
- Index-based insurance insurance links payouts not to actual crop losses but to exogenous events (in their case, rains).
- However, basis risk is an issue, given that the correlation between payouts (calculated over rain amounts) and actual yields is imperfect.


Our goal is twofold: transform a previous statistical analysis into a geospatial one with good visualizations: and include more weather variables to improve ACRE's model and protect better farmers against weather hazards.



Where are our farmers?
========================================================

<img src="Finalprojec_presentation-figure/figures-side1-1.png" title="plot of chunk figures-side1" alt="plot of chunk figures-side1" width="50%" /><img src="Finalprojec_presentation-figure/figures-side1-2.png" title="plot of chunk figures-side1" alt="plot of chunk figures-side1" width="50%" />

How is ACRE aggregating farmers to calculate their payouts?
========================================================
<img src="Finalprojec_presentation-figure/figures-side-1.png" title="plot of chunk figures-side" alt="plot of chunk figures-side" width="50%" /><img src="Finalprojec_presentation-figure/figures-side-2.png" title="plot of chunk figures-side" alt="plot of chunk figures-side" width="50%" />

What are they using to calculate payouts?
========================================================

Currently, they are only using IRI/LDEO Climate Data Library daily rainfall data. They aggregate data into four periods: germination, flowering, vegetation and pre-harvest.






<img src="Finalprojec_presentation-figure/unnamed-chunk-3-1.png" title="plot of chunk unnamed-chunk-3" alt="plot of chunk unnamed-chunk-3" style="display: block; margin: auto;" />

How can we improve their model?
========================================================
Giovanni - NASA Data Collection: humidity, soil moisture, surface air temperature, pressure, wind speed, evapotranspiration, etc.

<img src="Finalprojec_presentation-figure/unnamed-chunk-4-1.png" title="plot of chunk unnamed-chunk-4" alt="plot of chunk unnamed-chunk-4" style="display: block; margin: auto;" />



Outcome: Total profits in Short rains season 2018
========================================================

We have extensive data for each farmers: like investment on inputs, seeds, acreage, household characteristics, etc.

<img src="Finalprojec_presentation-figure/unnamed-chunk-5-1.png" title="plot of chunk unnamed-chunk-5" alt="plot of chunk unnamed-chunk-5" style="display: block; margin: auto;" />

Methods/ Approaches considered
========================================================
We will apply supervised learning methods using farmer's profits as an output and weather variables (divided by our 4 periods) as our input. 

We will follow the steps as learned in class: prepare and bake recipe, split data into training and test, and set cross/validation methods for all our statistical learning algorithms.
We will estimate:
- Regression trees
- Random Forest
- Support Vector Machines (svmPoly)
Preliminary results and conclusions
========================================================
So far, I overcame fundamental challenges: 
- building the fishnet (or grid) to fit pixel ids form the points provided by ACRE (using Arcmap)
- gather geospatial weather data for the right locations (Northern Siaya County) and time (short seasons 2018)
- manipulating data to be able to join them all together in one data frame.


Having the required data built, I will be able to follow steps for analysis. 
