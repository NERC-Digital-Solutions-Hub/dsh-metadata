# Supporting documentation for datasets published under McCracken, M.E., Woodcock, B.A., Lobley, M., Pywell, R.F., Saratsi, E., Swetnam, R.D., Mortimer, S.R., Harris, S.J., Winter, M., Hinsley, S. & Bullock, J.M (2015). Biodiversity, environmental and social data for the FarmCAT project 2007-2008.

## Overview
- Documents datasets used to evaluate two agri-environment options within the English Entry Level scheme (ELS): Nectar Flower Mixture (NFM) and Wild Bird Seed Mixture (WBM).
- Study scope: 48 arable/mixed farms across two English regions (east and southwest) with NFM or WBM strips established between 2005–2006.
- Data collected across 2007–2008 include ecological surveys (biodiversity and habitat resources), farmer interviews (attitudes and engagement), and landscape/weather context.
- Data are organized to support analyses of biodiversity responses (butterflies, bees, granivorous birds) and habitat quality (flower and seed resources), with attention to spatial and temporal structure (patch, strip, farm, year).

## Study design and data collection
- Study sites and agri-environment options
  - 48 farms selected to represent East (Cambridgeshire, Lincolnshire) and Southwest (Wiltshire, Dorset, Devon, Somerset) landscapes.
  - Each farm had both a NFM and a WBM strip option, with at least two fields featuring the relevant option.
  - Farmers were recruited through Natural England and direct contact.
- Farmer interviews
  - Semi-structured interviews in 2007 to explore environmental management history, understanding of NFM/WBM requirements, and attitudes.
  - Measures derived: Experience (1–4), Concerns (1–5 mean across requirements), Motivation (wildlife-focused, farming operations, or ELS compliance).
- Ecological surveys
  - Conducted in 2007 and 2008 on 3 strips per farm (or 2 if fewer available), with a nearby control area.
  - NFM: flower units counted in 1 m2 quadrats along transects; bees and butterflies recorded within a 4 m band; weather conditions logged.
  - WBM: seed mass estimated per sown species via 1 m2 quadrats; bird use monitored in winter months with timed counts.
  - Habitat context data: shelter score (0–8), Agricultural Land Classification (1–5), soil type (Light/Medium/Heavy).
- Landscape and seasonal variables
  - Landscape context mapped in 4x4 km squares; semi-natural habitat cover assessed from 10x10 km grids (BWARS, BTO, NBN data).
  - Species pools compiled for butterflies, granivorous birds, and bumblebees.
  - Daily weather data collected near each farm; seasonal aggregates calculated to test hypotheses about weather effects on responses.

## Data structure and files
- Six data files capture biodiversity responses and habitat resources:
  - Butterflydata.csv: butterfly counts and species richness per patch and year.
  - Beedata.csv: bee counts and species richness per patch and year.
  - Birddata.csv: granivorous bird counts and species richness per patch and year.
  - Flowerdata.csv: mean flower units per quadrat and mean flower species richness per patch/year.
  - Seeddata.csv: mean seed mass per quadrat (seed resource) per patch/year.
  - Additional variables and metadata describing each observation unit (patch/farm/year) and environmental context.
- Data structure concepts
  - Response variables include total counts and species richness aggregated across surveys for each taxon.
  - Fixed effects comprise continuous and categorical environmental variables; year treated as a repeated measure within the smallest sampling unit (strip).
  - Random effects account for hierarchical design: year nested within strip, with strips nested within farm.
- Key field naming and units
  - Fields include Farm, Region, Patch_No, Year; ecological measures (Bees, BeeSp, Buts, ButtSp, Birds, BirdSp, Flowers, FlowerSp, Seed_Wgt, Seed_Wgt); habitat/context variables (Shelter, Soil, ALC); socio-behavioral measures (Motivation, Concerns, Experience); landscape context (PCSemi_Nat, BWARS, NBN, BTO); weather variables (Temp, Wind, Summer_Max, Spring_Max, Winter_Min, Autumn_Max).
  - Data are structured to support nested, multi-level analyses across farm, strip, and year.

## Data quality, provenance and accessibility
- Data collected under explicit experimental designs with standardized field procedures (e.g., transect-based surveys, quadrat sampling, and consistent timing).
- Integration with national datasets (NBN, BWARS, BTO) enhances context and comparability.
- Clear documentation of units and data structure aids reproducibility and interoperability for data leaders planning cross-study analyses.

## Use cases and implications for data leaders
- Facilitates evaluation of ELS habitat options (NFM vs. WBM) on biodiversity and resource availability for target taxa.
- Supports multi-level modeling and hierarchical analysis due to nested design (year within strip within farm) and repeated measures.
- Enables integration with broader biodiversity and agricultural datasets for regional or policy-relevant assessments.
- Highlights the importance of rich metadata (units, definitions, sampling protocols) for long-term data discoverability and reuse.

## Gaps and considerations
- Geographic and option coverage is limited to 48 farms and two options; generalizability may be constrained.
- Data availability is tied to the FarmCAT project years (2007–2008) and may require careful temporal alignment with external datasets.
- Potential data gaps due to uneven sampling across farms or strips and the need to harmonize weather and landscape variables across sites.