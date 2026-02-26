# Biodiversity, environmental and social data for the FarmCAT project 2007-2008

## Study design and objectives
- Assessing two agri-environment options under the English Entry Level agrienvironment scheme (ELS):
  - Nectar Flower Mixture (NFM, EF4): three or more nectar-rich plant species to support nectar-feeding insects (bumblebees, butterflies)
  - Wild Bird Seed Mixture (WBM, EF2): three or more small-seed bearing species to support farmland birds (especially winter/early spring)
- Field set-up: 48 arable or mixed farms with NFM or WBM strips planted between autumn 2005–2006
  - Regions: 24 farms in the east of England; 24 in the south-west
  - Experimental design: equal representation of NFM and WBM in each region; each farm had at least two relevant fields
- Farmer selection and data collection:
  - Farms selected via Natural England GENESIS database, then farmers recruited
  - Semi-structured interviews conducted in 2007 to assess attitudes toward environmental management and scheme requirements

## Data collected from farmers
- Experience: four-point scale indicating history of environmental management (formal and informal involvement)
- Concerns: mean ease/difficulty of meeting habitat stipulations (1 = very difficult to 5 = easy)
- Motivation: wildlife-focused, farming-operations aligned, or to fulfill ELS requirements

## Ecological surveys and habitat assessment
- Timing: surveys conducted in 2007 and repeated in 2008
- Plot design: on each farm, three strips (or two if needed) plus a nearby control cropped area; identical size/shape/aspect
- Shelter and environment:
  - Shelter score (0–8) reflecting hedge/cover protection
  - Physical context data: Agricultural Land Classification (ALC, 1–5); soil type (Light/Medium/Heavy)
- NFM habitat surveys:
  - Flower units counted and identified to species in five 1 m2 quadrats along two parallel 50 m transects (July & August)
  - Bumblebees and butterflies observed along 4 m-wide band around transects
  - Weather conditions recorded (temperature, wind)
- WBM habitat surveys:
  - Seed resource: seeds weighed from three 1 m2 quadrats along two parallel 50 m transects (September)
  - Bird use: counts in November, January, February; standardized timed counts

## Landscape, seasonal weather, and regional data
- Landscape context:
  - 4x4 km cells centered on each farm from Google Earth and CEH Land Cover Map 2007
  - Species pools estimated from national grids (10x10 km)
    - Butterflies (2005–2009)
    - Granivorous birds (winter, 2007–2011)
    - Bumblebees (2000–2010)
- Weather data:
  - Daily data (2007–2008) from British Atmospheric Data Centre near each farm
  - Seasonal averages (winter, spring, summer, autumn) used for analyses of responses

## Data files and structure
- Six data files used to analyze responses to NFM and WBM:
  - Butterflydata.csv: butterfly numbers and species richness
  - Beedata.csv: bee numbers
  - Birddata.csv: granivorous bird counts and species richness
  - Flowerdata.csv: mean flower units and mean flower species per quadrat
  - Seeddata.csv: mean seed mass per quadrat
  - Additional fields include: shelter, soil, ALC, motivation, concerns, experience
- Data organization and variables:
  - Observations nested in patches within strips, within farms
  - Year treated as a repeated measure nested within the strip (smallest sampling unit)
  - Random effects: year within strip; strips nested within farm
  - Fixed effects: various habitat, landscape, and survey covariates
  - Key column groups and units include:
    - Farm, Region, Patch_No, Year
    - Bees, BeeSp; Butts, ButtSp; Birds, BirdSp
    - Flowers, FlowerSp; Seed_Wgt, Seed_Wgt (mean per quadrat)
    - Shelter (0–8), Soil (Light/Medium/Heavy), ALC (1–5)
    - Motivation, Experience, Concerns
    - PCSemi_Nat (percent semi-natural habitat in 4x4 km cell)
    - BWARS, NBN, BTO (grid-based species counts)
    - Temp, Wind, Summer_Max, Spring_Max, Winter_Min, Autumn_Max

## Analytic potential and applications
- Compare the ecological performance of NFM vs. WBM in terms of:
  - Biodiversity responses: butterfly, bee, and granivorous bird metrics
  - Habitat quality: flower resources and seed resources
- Link biodiversity outcomes to landscape context, weather, habitat features, and farmer attitudes
- Employ multilevel models to account for nested data structure (year within strip within farm)
- Use the six data files together to test hypotheses about predictors of species richness and abundance across farms and years

## Notes on data access and use
- Data were collected to enable analysis of agri-environment options and their ecological benefits
- The study integrates ecological measurements with farmer attitudes and landscape context to understand drivers of success or failure of habitat options
- Data descriptions include extensive metadata and clear units to support reproducibility and discoverability within data portals