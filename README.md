# Evaluating Affordable Housing Sites in the City of Los Angeles
## Introduction
#### The City of Los Angeles faces an ongoing housing crisis common up and down the West Coast of the United States and has been working for many years to fund and permit affordable housing in the city. Over 500 affordable housing projects have been built since 2003 totalling more than 45,000 units (Los Angeles Housing Department, 2024). This report seeks to understand how these affordable housing projects have been distributed geographically, and to evaluate their sites through the creation a suitability index that grades locational amenities and hazards in the vicinity of each project. 

Data for this project was found through the LA City Open Data portal via the Los Angeles Housing Department ("LAHD") and contains information on all "affordable housing" projects in the city since 2003. For the purposes of this project, the term "affordable housing" means any housing project that received LAHD funding from any program, including the Affordable Housing Managed Pipeline, the Supportive Housing Program, the Affordabel Housing Bond Program, and the Proposition HHH Supportive Housing Loan Program.

## Data Exploration
Summary Statistics:
* Total completed projects: 505
* Total units constructed citywide to date: 46,867
* Total units in development: 5,209
* Average units/project: 91
* Average construction duration: 1.77 years

![Project Status by Council District](docs/assets/status_by_cd_white.png)

![Average Project Units by Council District](docs/assets/units_per_proj.png)

![Units per Type by Council District](docs/assets/units_per_cd_by_type.png)

![](docs/assets/distribution_map_2.png)

<p float="left">
  <img src="docs/assets/count_per_cd_map.png" width="400" /> 
  <img src="docs/assets/units_per_cd_map.png" width="400" />
</p>

## Suitability Analysis
#### To evaluate the suitability of each affordable housing site an index was created using various environmental factors that might impact livability in the immediate area around each project. 500-foot buffers were generated from the geolocated data for each project, and these buffers were used to represent this immediate area. Factors included the following items which were each assigned a positive or negative weight based on their estimated impact on livability:
* Proximity to parks - +1
* Proximity to freeways - -1
* Proximity to High-Injury Network - -1
* Proximity to Metro rail portals - +2
* Presence of fatal pedestrian crashes over the last five years - -2

Buffers for each project were reviewed against the factor layers to see which factors, if any, were present within the 500-foot buffer radius. The overall suitability score for each project would be the sum total value of the weights of all factors present within the 500-foot buffer. 

![](docs/assets/suitability_factors_map.png)


