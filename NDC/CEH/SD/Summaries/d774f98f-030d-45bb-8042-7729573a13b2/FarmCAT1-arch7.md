# Supporting documentation for datasets published under McCracken, M.E., Woodcock, B.A., Lobley, M., Pywell, R.F., Saratsi, E., Swetnam, R.D., Mortimer, S.R., Harris, S.J., Winter, M., Hinsley, S. & Bullock, J.M (2015). Biodiversity, environmental and social data for the FarmCAT project 2007-2008. - 1) Experimental design, sampling and collection methods

- Study sites and agri-environment options
  - Evaluates two English Entry Level agri-environment options: Nectar Flower Mixture (NFM) and Wild Bird Seed Mixture (WBM) sown at field edges.
  - 48 arable or mixed farms (24 east, 24 southwest); half with NFM and half with WBM; each farm had at least two eligible fields with the option.
  - Selection: GENESIS database screening by Natural England, followed by farmer recruitment.

- Farmer interviews
  - Semi-structured interviews (2007) to assess attitudes towards environmental management and management requirements for NFM/WBM.
  - Measures derived: 
    - Experience (4-point scale of engagement with environmental management)
    - Concerns (mean difficulty rating across management requirements)
    - Motivation ( wildlife-focused, farming-aligned, or to fulfill ELS requirements)

- Ecological surveys
  - Conducted in 2007 and 2008 on 3 strips per farm (or 2 if fewer strips available) plus nearby control areas.
  - Shelter score (0–8) indicating hedge/edge protection.
  - National data: Agricultural Land Classification (ALC) 1–5; soil type (Light/Medium/Heavy).
  - NFM surveys: flower units and species identified in five 1 m² quadrats along transects; bumblebees and butterflies recorded along a 4 m band around the transects.
  - WBM surveys: seed resource estimated by collecting seeds from sown species in three 1 m² quadrats along transects; seeds dried, weighed, and stored for processing.
  - Bird use: seasonal counts (Nov, Jan, Feb) for the entire strip; birds counted from a distance with birds then flushed.

- Landscape and seasonal weather variables
  - Landscape context: 4×4 km cell around each farm using Google Earth and CEH Land Cover Map 2007.
  - Species pools: national datasets mapped on 10×10 km grids (butterflies 2005–2009; granivorous birds winter 2007–2011; bumblebees 2000–2010).
  - Weather: daily data (2007–2008) from BDAC near each farm; seasonal means calculated for winter, spring, summer, autumn.

- Nature and units of recorded values, and data structure
  - Aimed at two outcomes: biodiversity responses and habitat quality (resources for target taxa).
  - Biodiversity responses:
    - Butterflies: Butterflydata.csv (count and species richness across surveys per year, patch-level)
    - Bumblebees: Beedata.csv (count and species richness per patch-year)
    - Granivorous birds: Birddata.csv (count and species richness per patch-year)
  - Habitat resources (means across quadrats/surveys per patch-year):
    - Flowers: Flowerdata.csv (mean number of flower units; mean flower species per quadrat)
    - Seeds: Seeddata.csv (mean seed weight per quadrat)
  - Data structure and variables
    - Each record includes Farm, Region, Patch_No, Year, and a set of response variables (counts and species richness) plus covariates (Shelter score; Soil type; ALC; and landscape/meteorological covariates such as semi-natural habitat cover, BWARS/NBN/BTO species counts, and seasonal temperature and wind).
    - Random effects: year nested within the smallest sampling unit (the strip) to account for repeated measures; strips nested within farms for farm- and strip-level analyses.
  - Column headings (summary)
    - Farm, Region, Patch_No; Year
    - Biodiversity: Bees, BeeSp, Butts, ButtSp, Birds, BirdSp
    - Habitat resources: Flowers, FlowerSp, Seed_Wgt, Seed_Wgt (mean per quadrat)
    - Shelter, Soil, ALC, Motivation, Concerns, Experience
    - Landscape/attendance covariates: PCSemi_Nat, BWARS, NBN, BTO
    - Weather: Temp, Wind, Summer_Max, Spring_Max, Winter_Min, Autumn_Max
  - Overall purpose of the datasets: enable analysis of how NFM and WBM strips affect pollinator and bird biodiversity and habitat resources, with context from landscape features and weather, using a nested, repeated-measures structure suitable for GIS-friendly, map-based analysis and spatially explicit modeling.