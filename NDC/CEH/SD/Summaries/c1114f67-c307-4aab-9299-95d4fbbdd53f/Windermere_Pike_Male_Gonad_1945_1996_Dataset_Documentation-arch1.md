# Windermere Pike Male Gonad Weight Data (1945 to 1996)

## Overview
- Dataset of estimated gonad weight and associated metadata for male pike (Esox lucius) from net sampling in Windermere Lake, Cumbria.
- Data collection spans 1945–1996; originally collected by the Freshwater Biological Association (FBA) and since 1989 by CEH and its predecessor IFE.
- File: Windermere_Pike_Male_Gonad_Data_1945_to_1996.csv (225 kb, CSV).

## Data structure and key variables
- Columns and data types:
  - Individual (unique identifier)
  - Weight (g) – body weight
  - Length (cm) – length at capture
  - Age (years) – age at capture
  - Year – calendar year of capture
  - Temp (°C) – annual average water surface temperature
  - GSI – Gonadosomatic Index (unitless)
  - Gonad (g) – estimated gonad weight
- Sampling site: Windermere Lake (approximate coordinates provided)
- Fish species: Esox lucius (pike)
- Units: Weight, Length, Gonad in grams and centimeters; Temp in °C; GSI unitless; Gonad weight field is the estimated value

## Sampling design and regime
- Spatial scope: North and South basins of Windermere; pike monitored by gill nets with variations in site selection and effort from 1944 onward.
- Standardization (1982 onward):
  - Nets: 64 mm bar mesh, multifilament
  - Size: 40 m long, 3 m deep
  - Set on the bottom between mid-October and late December
  - Depths around 4–5 m, 10 sites per basin
  - Sampling pattern: five nets fished at a site per week with rotating sites to cover the lake
  - Weekly cycle: set, inspect, harvest, and lift within a repeated weekly sequence
- Sampling effort:
  - 1982–1989: ~348 net days annually (approx. equally distributed between basins)
  - 1990 onward: ~240 net days annually (approx. equally distributed between basins)

## Analytical methods
- Laboratory workflow:
  - Each pike measured (fork length to 1 mm) and weighed (wet weight to 100 g)
  - Sex determined; left opercular bone aged (birth date assumed 1 April)
- Gonad weight estimation:
  - Gonad weight estimated using a linear function based on body weight
  - Lightest individual: gonad ~ 2% of body weight; heaviest: gonad ~ 4% of body weight
  - Method grounded in Craig (1996)
- Quality control:
  - Measurements verified via permutations of three individuals

## Data quality, caveats, and potential uses
- Gonad weight is an estimated value rather than direct measurement for all individuals, which should be considered in analyses and interpretation.
- Changes in sampling methodology prior to 1982 and standardization from 1982 onward may affect temporal comparisons; analyses should account for potential biases related to method consistency.
- Temperature data (Temp) enables exploration of relationships between environmental conditions and gonad development or reproductive condition (GSI).
- Age estimation via opercular bone aging is standard but carries inherent uncertainty; cross-year comparability should consider age-structure differences.
- The dataset supports analyses of:
  - Temporal trends in gonad development and reproductive condition
  - Relationships between GSI, gonad weight, body size, age, and environmental temperature
  - Spatial (basin) comparisons within Windermere
  - Inter-annual variation in reproductive investment given standardized sampling from 1982 onward

## Provenance and key references
- Provenance: Data compiled by FBA; continued by CEH/IFE since 1989
- Core references underpinning methods and data interpretation:
  - Le Cren (2001) Windermere perch and pike project
  - Winfield, James & Fletcher (2008) Northern pike in a warming lake
  - Frost & Kipling (1959) Age and growth assessment from scales and opercular bones
  - Craig (1996) Pike: Biology and Exploitation
- Quality control and documentation linked to the above methodologies ensure traceability and reproducibility of analyses.