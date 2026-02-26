# Supporting documentation for datasets published under McCracken, M.E., Woodcock, B.A., Lobley, M., Pywell, R.F., Saratsi, E., Swetnam, R.D., Mortimer, S.R., Harris, S.J., Winter, M., Hinsley, S. & Bullock, J.M (2015). Biodiversity, environmental and social data for the FarmCAT project 2007-2008. - 1) Experimental design, sampling and collection methods

## Purpose and scope
- Documents the experimental design, sampling and collection methods for assessing two agri-environment options (NFM and WBM) under the English ELS.
- Aims to link habitat management on farms to biodiversity outcomes (butterflies, bumblebees, granivorous birds) and habitat resources (flowers, seeds).
- Covers data collection across 48 farms representing east England and southwest England, with both NFM and WBM options.

## Study design and sampling
- Regions: 
  - East (Cambridgeshire and Lincolnshire)
  - Southwest (Wiltshire, Dorset, Devon, Somerset)
- Farms: 48 total; 24 per region; split evenly between NFM and WBM; each farm contains at least two fields with the relevant ELS option.
- Farm selection: via Natural England GENESIS database criteria, followed by farmer recruitment.

## Data collection methods

### Farmer interviews
- Semi-structured interviews conducted in 2007.
- Focus areas:
  - Attitudes toward environmental management and scheme requirements.
  - Perceptions of management requirements for NFM or WBM.
- Measures derived:
  - Experience: 1–4 scale of prior engagement with environmental management.
  - Concerns: 1–5 mean score reflecting ease of meeting habitat stipulations.
  - Motivation: wildlife-focused (1), farming-fit (2), or to fulfill ELS (3).

### Ecological surveys
- Conducted in 2007 (and repeated in 2008).
- Strips: 3 per farm (or 2 if limited by site), with a nearby control area for comparison.
- Shelter score: 0–8 representing shelter from hedges and similar features.
- Landscape and soil context:
  - Agricultural Land Classification (ALC) 1–5.
  - Soil type: Light, Medium, Heavy.
- NFM surveys:
  - Flower units counted and species identified in five 1 m2 quadrats along transects; surveys in July and August.
  - Bumblebees and butterflies recorded along a 4 m band around transects; weather and conditions logged.
- WBM surveys:
  - Seed resource estimated by harvesting and weighing seeds from sown species in quadrats along transects (September).
  - Bird use monitored via timed counts in November, January, February.

### Landscape and seasonal weather variables
- Landscape context:
  - 4×4 km mapped around each farm using Google Earth and CEH Land Cover Map (2007).
  - Species pools inferred from 10×10 km grids for butterflies (2005–2009), granivorous birds (2007–2011 winter), bumblebees (2000–2010).
- Weather data:
  - Daily weather from British Atmospheric Data Centre for the nearest station to each farm (2007–2008).
  - Seasonal aggregates defined (winter, spring, summer, autumn) to relate to response variables.

## Data structure and content

### Data files and key variables
- Six data files reporting biodiversity responses and habitat resources:
  - Butterflydata.csv: butterfly counts and species richness (per patch/year).
  - Beedata.csv: bumblebee counts and species richness (per patch/year).
  - Birddata.csv: granivorous bird counts and species richness (per patch/year).
  - Flowerdata.csv: mean number of flower units and mean flower species per quadrat (per patch/year).
  - Seeddata.csv: mean seed weight per quadrat (per patch/year).
  - Patch- and site-level data: includes shelter, soil, ALC, and other context variables; used to model habitat quality and as fixed effects.
- Data structure notes:
  - Response variables summarized as counts or means across surveys within a year.
  - Year treated as a repeated measure nested within the smallest sampling unit (the individual strip).
  - Random effects include strips nested within farms to capture farm- and strip-level variation.

### Variables and units (examples)
- Biodiversity responses:
  - Bees/Bumblebees: count (Beedata.csv), species richness (BeeSp).
  - Butterflies: count (Butterflydata.csv), species richness (ButtSp).
  - Granivorous birds: count (Birddata.csv), species richness (BirdSp).
- Habitat resources:
  - Flowers: count of flower units (Flowers), mean flower units per quadrat (FlowerSp).
  - Seeds: seed weight (Seed_Wgt), mean seed weight per quadrat (Seed_Wgt, 2).
- Contextual factors:
  - Shelter score (0–8), Soil type (Light/Medium/Heavy), ALC (1–5).
  - Farmer factors: Experience, Concerns, Motivation.
  - Landscape and regional context: semi-natural habitat cover (PCSemi_Nat), regional BWARS/NBN/BTO indices.
  - Weather: temperature (Temp), wind (Wind), seasonal max/min temperatures (Summer_Max, Spring_Max, Winter_Min, Autumn_Max).

## Data management, quality and documentation

- Data collection followed standardized protocols across sites and years, enabling cross-site comparisons.
- Insect and bird surveys conducted under defined weather and time windows to ensure comparability.
- Seed and flower data involved laboratory processing (e.g., seed drying and weighing) to ensure consistency.
- Data are accompanied by detailed variable descriptions, units, and coding rules to support reproducibility and reuse.
- Data governance considerations:
  - Data integration from multiple data sources (field surveys, farmer interviews, national species datasets) with clear provenance.
  - Potential sharing constraints and disclosures noted in stewardship context, including considerations of data availability and interoperability.
  - Documentation includes both the ecological data and the sociocultural (farmer) data to support integrated analyses.

## Practical takeaways for data stewards
- The collection provides a multi-faceted, linked dataset tying habitat management (NFM/WBM) to biodiversity and resource metrics across two English regions.
- Rich metadata support discoverability and reuse, with explicit data structure, units, and random effects suitable for reproducible analyses.
- Data governance should preserve provenance, relationship among datasets (biodiversity, resources, farmer attitudes, landscape context), and alignment with user needs (e.g., policy relevance, ecological modeling).
- When sharing, ensure clear documentation of sampling design, site selection criteria, survey timing, and processing steps to facilitate interpretation and re-use across studies.