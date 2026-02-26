# EIDC dataset: Tritrophic phenology and associated data from 44 sites in Scotland, 2014-2021

## Overview
- A multi-year, multi-site dataset designed to analyse interactions between trees, herbivores (caterpillars), and a passerine bird (blue tit) across 44 sites in Scotland (2014–2021).
- Data types include temperature, tree phenology, caterpillar abundance/mass, and detailed blue tit breeding phenology and outcomes.
- Data are organized into seven CSV files and are linked via a consistent three-letter site code across files.

## Sampling design and study site
- 30 woodland sites initially, located between Edinburgh and Dornoch; sites spaced out and near major roads (M90 and A9).
- Eight Schwegler 1B nestboxes per site were deployed; by 2017, 44 sites with most sites having eight boxes.
- Field visits: every 2 days from early April to mid/late June (2014–2016 started in mid-late March; 2020 COVID-19 shifted timing).
- In 2020, fieldwork began in early May; data recording for some measures (e.g., tree phenology, first egg date) incomplete; southern 22 sites visited regularly.

## Data collection details and variables

- Temperature
  - Hourly air temperatures recorded at each site using two DS1922 L thermochron loggers.
  - Loggers positioned at opposite ends of each site, approx. 1.5 m above ground, on the north side of large tree trunks.
  - Temperature data cover mid-Feb to mid-Jun; data are stored as hourly values, with NA for missing periods.

- Tree phenology
  - Representative deciduous taxa sampled; phenophases recorded at each visit.
  - Four phenophases: first budburst (fbb), complete budburst (cbb), first leaf (flf), complete leaf (clf).
  - Taxon can be species (e.g., Alder) or genus (e.g., Oak, Willow, Birch).
  - Data stored in Tree_Phenology file.

- Caterpillars (branch beating)
  - Branch beating conducted when at least 45% of trees in a year reached first leaf.
  - Branches marked and beaten every four days; one branch beaten on alternating visit sequences.
  - Each beating involves dislodging caterpillars with a 30-stroke beat into a plastic sack; counts recorded for caterpillars >1 mm.
  - From 2017, caterpillars weighed; mass <0.02 g recorded as <0.02 g.
  - Data stored in Branch_Beating file (including counts and caterpillar mass).

- Blue tit breeding phenology and outcomes
  - Nestboxes visited every 2 days until first egg date; eggs assumed to hatch at 1 day intervals.
  - Post-egg observations include first incubation date, clutch size, hatching date; nestlings ringed and weighed at ~6 and ~12 days; adults captured at nest day 10 for morphometrics.
  - Breeding success quantified as the number of fledglings.
  - Data split into three files: Bird_Phenology (nestbox phenology and treatment info), Nestlings (individual nestling IDs, mass, wing length, fledging status), and Adults (adult morphometrics and ring info).

## Data structure and files
- Seven CSV files in total:
  - site_details: site code, site name, mean latitude, mean longitude, mean elevation (per site).
  - temperatures: site, year, and hourly temperature columns (X46 to X163); includes NA where data are missing.
  - Tree_Phenology: year, site, TreeID, taxon, fbb, cbb, flf, clf.
  - Branch_Beating: year, site, treeID, taxon, date, weather, recorder, caterpillar count, caterpillar.mass, notes, mass.uncertain.
  - Bird_Phenology: year, site, box, species, fed (first egg date), cs (clutch size), fki (first incubation), clutch_swap_treatment, Hatching_first_recorded, uhe, v1date/v1alive/v1time, v2date/v2alive/v2time, suc.
  - Nestlings: year, site, box, ring, v1date, v1mass, v1ringer, v2alive, v2date, v2mass, v2wing, v2ringer, fledged.
  - Adults: ring, year, site, box, age, sex, wing, mass, date, time, ringer.
- Data integration: the same sites and years can be combined across files using site and year variables.
- Data notes: -999 values should be excluded; NA indicates missing data; mass < 0.02 g recorded as <0.02 g.

## Data quality, limitations, and accessibility
- COVID-19 impact in 2020 caused delayed start and incomplete data collection for some measures; southern 22 sites were visited regularly that year.
- Some records include notes on issues (e.g., unbalanced sampling, clustering of missing data).
- Fine-scale, multi-year, site-specific data allow robust analyses but require careful handling of missing values and potential treatment effects (e.g., clutch_swap_treatment).

## Potential analyses and questions for data scientists
- Tritrophic linkages: how temperature and tree phenology influence caterpillar availability across years and sites, and how these, in turn, relate to blue tit breeding timing and success.
- Spatial and temporal patterns: across 44 sites with varying habitats and microclimates, examine how site-level variables (latitude, elevation) and proximity to roads relate to phenology and breeding outcomes.
- Predictive modeling: develop models predicting first egg dates, hatch dates, clutch sizes, and fledging success from temperature, tree phenology, and caterpillar measures.
- Data integration and provenance: combine datasets across files for multi-variable analyses; account for clutch_swap_treatment and COVID-era data gaps in inference.

## References
- Macphie, K., Samplonius, J.M., Hadfield, J.D., Pearce-Higgins, J. & Phillimore, A.B. (2020). Among tree and habitat differences in the timing and abundance of spring caterpillars. EcoEvoRxiv.
- Shutt, J.D., Bolton, M., Benedicto Cabello, I., Burgess, M.D. & Phillimore, A.B. (2018). The effects of woodland habitat and biogeography on blue tit territory occupancy and productivity along a 220 km transect. Ecography.
- Shutt, J.D., Burgess, M.D. & Phillimore, A.B. (2019a). A spatial perspective on the phenological distribution of the spring woodland caterpillar peak. American Naturalist.
- Shutt, J.D., Cabello, I.B., Keogan, K., Leech, D.I., Samplonius, J.M., Whittle, L. et al. (2019b). The environmental predictors of spatio-temporal variation in the breeding phenology of a passerine bird. Proceedings of the Royal Society B.