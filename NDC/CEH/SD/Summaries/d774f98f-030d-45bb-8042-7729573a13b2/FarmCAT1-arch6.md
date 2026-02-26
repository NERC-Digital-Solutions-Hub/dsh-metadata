# Supporting documentation for datasets published under McCracken, M.E., Woodcock, B.A., Lobley, M., Pywell, R.F., Saratsi, E., Swetnam, R.D., Mortimer, S.R., Harris, S.J., Winter, M., Hinsley, S. & Bullock, J.M (2015). Biodiversity, environmental and social data for the FarmCAT project 2007-2008.

## Purpose and scope
- Documents data collected to assess the success of two agri-environment options (NFM and WBM) under the English Entry Level agrienvironment scheme (ELS).
- Focus on biodiversity responses (pollinators and birds) and habitat resources (flowers and seeds) across farms and field-edge strips.
- Provides data and metadata to enable secondary analyses of habitat management, biodiversity outcomes, and related environmental factors.

## Study design and sampling
- Options studied:
  - Nectar Flower Mixture (NFM, EF4 under ELS): at least three nectar-rich plant species in 6 m wide strips at field edges.
  - Wild Bird Seed Mixture (WBM, EF2 under ELS): at least three small-seed bearing plant species for farmland birds.
- Locations and sampling frame:
  - 48 arable/mixed farms with NFM or WBM strips established between autumn 2005 and autumn 2006.
  - Regional balance: 24 farms in the east (Cambridgeshire, Lincolnshire) and 24 in the southwest (Wiltshire, Dorset, Devon, Somerset).
  - Farm selection: NATURAL England GENESIS database screening, followed by farmer recruitment.
  - Farm-level design: half with NFM, half with WBM; all farms had at least two relevant strips.

## Data collection methods

### Farmer interviews
- Conducted in 2007; semi-structured to explore attitudes toward environmental management and understanding of NFM/WBM requirements.
- Measures derived:
  - Experience: four-point scale (1–4) reflecting history of engagement with environmental management.
  - Concerns: mean score (1–5) across management requirements reflecting perceived difficulty.
  - Motivation: three categories from wildlife focus to operation-fit or ELS compliance.

### Ecological surveys
- Conducted in 2007 and 2008; three strips per farm (or two when needed) plus nearby control areas.
- Shelter: shelter score (0–8) describing protection from hedges and similar features.
- Site context data: Agricultural Land Classification (ALC, 1–5) and soil type (Light/Medium/Heavy).
- NFM surveys:
  - Flower units counted and species identified in five 1 m² quadrats along transects.
  - Bumblebees and butterflies surveyed along transects (4 m band) during suitable weather and times.
  - Weather during insect surveys recorded (temperature, wind).
- WBM surveys:
  - Seed resource estimated by weighing seeds from sown species in quadrats along transects.
  - Bird use of strips monitored in late autumn to winter (Nov, Jan, Feb) with timed counts.

### Landscape and seasonal weather variables
- Landscape context: 4x4 km area around each farm with land-cover mapping; semi-natural habitat cover quantified in a 4x4 km cell.
- Species pools: national datasets (butterflies, granivorous birds, bumblebees) mapped at 10x10 km grid.
- Weather: daily data (2007–2008) from nearest British Atmospheric Data Centre station; seasonal averages computed (winter, spring, summer, autumn).

## Data and variable overview

### Data files and what they contain
- Six data files summary biodiversity and habitat resources:
  - Butterlydata.csv: butterfly counts and metrics
  - Beedata.csv: bumblebee counts and metrics
  - Birddata.csv: granivorous bird counts
  - Flowerdata.csv: mean flower units and flower species per quadrat
  - Seeddata.csv: mean seed weight per quadrat
  - A fifth/related file structure describing shelter, soil, ALC, and related metadata
- For each data file, the core identifiers and variables include:
  - Farm, Region, Patch_No, Year (2007 or 2008)
  - Fine-scale measures at patch level (per strip):
    - Bees, BeeSp (count and species)
    - ButtS/buttSp (butterflies count and species)
    - Birds/BirdSp (granivorous birds count and species)
    - Flowers/FlowerSp (mean number of flower units and mean flower species per quadrat)
    - Seed_Wgt/Seed_Wgt 2 (mean seed mass per quadrat)
    - Shelter (0–8)
    - Soil (Light/Medium/Heavy)
    - ALC (1–5)
  - Farm-level measures:
    - Motivation (S1–S3 categories)
    - Concerns (1–5)
    - Experience (1–4)
    - PCSemi_Nat (percentage cover of semi-natural habitat in the 4x4 km cell)
  - Landscape and national data proxies:
    - BWARS (bumblebee data), NBN (butterfly data), BTO (bumblebee species data)
  - Weather and climate context:
    - Temp (°C), Wind (0–5)
    - Seasonal max/min temps: Summer_Max, Spring_Max, Winter_Min, Autumn_Max

### Data structure and design
- Data reflect two response domains:
  - Biodiversity responses: counts and species richness for butterflies, bumblebees, and granivorous birds.
  - Habitat resources: flower units/species and seed weight.
- Experimental design features:
  - Fixed effects: various continuous and categorical explanatory variables (field-level and site-level).
  - Random effects: year nested within the strip (smallest sampling unit); strips nested within farm to allow analysis at farm and strip scales.
- Data organization emphasizes multi-level, repeated-measures structure suitable for mixed-effects analyses.

## How this data can be used (data-support perspective)
- Enable evaluation of NFM vs. WBM effectiveness on pollinator and bird communities and on floral/seed resources.
- Support analyses of how landscape context (semi-natural habitat, land cover) and weather influence biodiversity outcomes.
- Facilitate exploration of farmer attitudes (Experience, Concerns, Motivation) in relation to scheme adherence and habitat results.
- Provide a multi-resolution dataset (farm → strip/patch → year) for building dashboards, replicable analyses, or data products enabling self-service exploration of biodiversity and habitat associations.

## Key considerations for users
- Multi-level structure requires careful handling of random effects and nested units (year within patch/strip, strips within farms).
- Data come from field campaigns across two years with potential variability in sampling effort across farms and strips.
- Integration across six data files necessitates careful alignment on identifiers (Farm, Region, Patch_No, Year) and consistent interpretation of derived metrics (counts, means, and species richness).