# Supporting documentation for datasets published under McCracken, M.E., Woodcock, B.A., Lobley, M., Pywell, R.F., Saratsi, E., Swetnam, R.D., Mortimer, S.R., Harris, S.J., Winter, M., Hinsley, S. & Bullock, J.M (2015). Biodiversity, environmental and social data for the FarmCAT project 2007-2008.

## Overview
- Documents the experimental design, sampling, and data collection methods for evaluating two agri-environment scheme options (NFM and WBM) used by arable farmers under the English ELS.
- Aims to assess biodiversity responses and habitat quality for target taxa, and to provide data for broader analyses of environmental management outcomes.
- Study framework includes field experiments, farmer interviews, ecological surveys, and landscape/meteorological context.

## Study sites and options
- 48 arable or mixed farms selected to represent English farming landscapes, split 24 in the east (Cambridgeshire and Lincolnshire) and 24 in the south-west (Wiltshire, Dorset, Devon & Somerset).
- Each farm implemented one of two ELS habitat options: Nectar Flower Mixture (NFM, EF4) or Wild Bird Seed Mixture (WBM, EF2); half the farms had NFM strips, half had WBM strips.
- Farms required a minimum of two fields with the relevant ELS option.
- Selection process: NE GENESIS database screening by geography/date/ELS criteria, followed by farmer recruitment.

## Farmer interviews
- Semi-structured interviews conducted in 2007 to explore farmer attitudes toward environmental management and specifics of NFM/WBM requirements.
- Attitudinal measures derived:
  - Experience: engagement with environmental management on a 4-point scale (higher = more extensive and frequent).
  - Concerns: perceived ease of meeting habitat stipulations (scale 1–5, with higher indicating easier).
  - Motivation: reasons for strip placement on the farm, categorized as wildlife-focused, farming operations-compatible, or simply to fulfill ELS requirements.

## Ecological surveys
- Conducted in 2007 and repeated in 2008.
- For each farm, 3 strips (or 2 if fewer available) and a nearby control area of equivalent size/shape/aspect were surveyed.
- Shelter score (0–8) indicating protection from hedges/areas around the strip.
- National environment data incorporated: Agricultural Land Classification (ALC; 1–5) and soil type (Light/Medium/Heavy).
- NFM strips:
  - Flower units counted and species identified in five 1 m² quadrats along two 50 m transects (July and August).
  - Bumblebees and butterflies surveyed along a 4 m band around transects; weather conditions recorded.
- WBM strips:
  - Seed resource estimated by collecting seeds from each sown species in three 1 m² quadrats along two transects (September); seeds processed and weighed.
  - Bird use of entire strip monitored in November, January, and February through timed counts.

## Landscape and seasonal weather variables
- Landscape context described with a 4×4 km square around each farm using Google Earth and CEH Land Cover Map 2007.
- Species pools estimated from national datasets mapped on a 10×10 km grid:
  - Butterflies (2005–2009)
  - Granivorous birds (winter 2007–2011)
  - Bumblebees (2000–2010)
- Weather data: daily values for 2007–2008 from nearest British Atmospheric Data Centre station.
  - Seasonal averages computed for winter, spring, summer, autumn (based on hypotheses about temperature effects on response variables).

## Nature and units of recorded values, and data structure
- Six data files document biodiversity responses and habitat quality:
  - Butterflydata.csv: butterfly counts and species richness (annual totals per patch).
  - Beedata.csv: bee counts and species richness (annual totals per patch).
  - Birddata.csv: granivorous bird counts and species richness (annual totals per patch).
  - Flowerdata.csv: mean number of flower units and mean flower species per quadrat (per patch/year).
  - Seeddata.csv: mean seed weight per quadrat (per patch/year).
  - Shelter/Soil/Environmental variables: shelter scores, soil category, ALC scores, and other contextual fields.
- Response variables (a) biodiversity metrics and (b) habitat resources:
  - Biodiversity: counts and species richness for bees, butterflies, and granivorous birds.
  - Habitat quality: flower abundance and diversity; seed weight as resources for target taxa.
- Explanatory structure:
  - Fixed effects (subsets of continuous and categorical variables) used to model responses.
  - Year treated as a repeated measure, nested within the smallest sampling unit (the individual strip) to reflect temporal replication.
  - Additional random effects: replicate strips nested within farms to allow analysis at both farm and strip scales.
- Data column structure (example concepts):
  - Farm/Region/Patch identifiers; Year; counts and species richness for Bees, BeeSp, Butts, ButtSp, Birds, BirdSp.
  - Flower counts and FlowerSp; Seed_Wgt (seed weight metrics); Shelter; Soil; ALC; Motivation; Concerns; Experience.
  - National dataset indicators (PCSemi_Nat, BWARS, NBN, BTO) for ecosystem context and species pools.
  - Weather-related variables (Temp, Wind, Seasonal Max/Min temperatures).