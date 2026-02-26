# Supporting documentation for datasets published under McCracken, M.E., Woodcock, B.A., Lobley, M., Pywell, R.F., Saratsi, E., Swetnam, R.D., Mortimer, S.R., Harris, S.J., Winter, M., Hinsley, S. & Bullock, J.M (2015). Biodiversity, environmental and social data for the FarmCAT project 2007-2008.

## Overview
- Documents the experimental design, sampling, and data structure used to evaluate the two English Entry Level agrienvironment scheme (ELS) habitat options: Nectar Flower Mixture (NFM) and Wild Bird Seed Mixture (WBM).
- Aims to assess biodiversity responses (pollinators and granivorous birds) and habitat quality (resources for target taxa) in farmed landscapes.
- Combines ecological surveys, farmer attitudes, landscape context, and weather data across two regions and two years (2007–2008).

## Study sites and agrienvironment options
- 48 arable or mixed farms chosen to represent eastern (Cambridgeshire, Lincolnshire) and south-west English farming landscapes (Wiltshire, Dorset, Devon, Somerset).
- Regions: 24 farms in the east; 24 farms in the south-west.
- Each region had an equal split: NFM option or WBM option.
- All farms had at least two fields with the relevant ELS option.
- Selection process: Natural England GENESIS database first, followed by farmer recruitment.

## Farmer interviews
- Semi-structured interviews conducted in 2007.
- Aimed to understand farmer attitudes toward environmental management and understanding of NFM/WBM requirements.
- Measures derived:
  - Experience: 1–4 scale (history of engagement with environmental management).
  - Concerns: 1–5 mean score reflecting perceived ease of meeting habitat stipulations.
  - Motivation: three categories—best for wildlife, to fit farming operations, or to fulfill ELS requirements.

## Ecological surveys
- Conducted in 2007 and repeated in 2008.
- Strips: three per farm (or two if fewer strips available), with a nearby matched control area.
- Habitat covariates: shelter score (0–8), Agricultural Land Classification (ALC, 1–5), and soil type (Light, Medium, Heavy).
- NFM strips:
  - Flower units counted and identified to species in five 1 m² quadrats across two 50 m transects (July and August).
  - Bumblebees and butterflies surveyed along a 4 m band around transects; weather and time recorded.
- WBM strips:
  - Seed resource estimated by collecting and weighing seeds from each sown species in three 1 m² quadrats along two 50 m transects (September).
  - Bird use monitored in November, January, and February via timed counts with birds flushed at the end.
- Weather and activity windows: surveys conducted 10:30–17:00 on dry days with >16°C.

## Landscape and seasonal weather variables
- Landscape context: 4x4 km land-cover map around each farm (Google Earth/CEH Land Cover Map 2007).
- Species pools: national datasets mapped on 10x10 km grids (butterflies 2005–2009; granivorous birds winter 2007–2011; bumblebees 2000–2010).
- Weather data: daily data from the British Atmospheric Data Centre, averaged seasonally for analyses (winter, spring, summer, autumn).
  
## Nature and units of recorded values, and data structure
- Six data files record data used to analyze habitat success and biodiversity responses:
  - Biodiversity: butterfly counts (Butterflydata.csv), bumblebee counts (Beedata.csv), granivorous bird counts (Birddata.csv).
  - Habitat resources: mean flower units and species per quadrat (Flowerdata.csv), mean seed weight per quadrat (Seeddata.csv).
- Data organization:
  - Response variables include counts and species richness across surveys (annual totals or multi-survey totals).
  - Explanatory/fixed effects include habitat type (NFM/WBM), landscape and soil covariates, and weather-related variables.
  - Random effects structure: year nested within the smallest sampling unit (strip), with strips nested within farm to allow analysis at both farm and strip scales.
- Column-level descriptions indicate hierarchical sampling details (farm, region, patch/strip, year), taxa counts (bees, butterflies, birds), habitat metrics (flowers, seeds, shelter), soil/ALC classifications, farmer attitude metrics (Motivation, Concerns, Experience), and landscape/biogeographic indicators (semi-natural habitat cover, regional species pools, national biodiversity datasets). Weather metrics (temperature, wind, seasonal maxima/minima) accompany survey data.