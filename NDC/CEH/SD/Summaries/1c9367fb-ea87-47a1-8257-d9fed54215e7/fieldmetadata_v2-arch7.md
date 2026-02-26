# Long-term multisite Scots pine trial, Scotland: field phenotypes, 2013-2020

## Overview
- A long-term, multisite field phenotyping study of Scots pine (Pinus sylvestris) conducted across three field sites in Scotland (Yair/FS, Glensaugh/FE, Inverewe/FW).
- Seed from 21 native Scottish populations (10 trees per population) collected in 2007; trees germinated and grown in nurseries before field planting in 2012.
- Traits measured include plant height, basal stem diameter, and phenology (budburst timing) collected over multiple growing seasons.
- Field measurements span 2013–2020 for FE and FW; 2014–2020 for FS; 2020 data collection limited by COVID-19 restrictions.

## Spatial configuration and field layout
- Field sites and coordinates:
  - FS (Yair, southern Scotland): 55.603625 N, -2.893025 W
  - FE (Glensaugh, eastern Scotland): 56.893567 N, -2.535736 W
  - FW (Inverewe, western Scotland): 57.775714 N, -5.597181 W
- Seed origin reference:
  - James Hutton Institute location: 57.133214 N, -2.158764 W
- Experimental design:
  - Trees planted in randomised blocks with 3 m x 3 m spacing; a periphery guard row established.
  - Each block contains one tree from each of eight of the ten families from each of the 21 populations (168 trees per block).
  - At least 159 families represented at all three sites; nine under-represented families replaced at FS with alternative families from the same population.
  - FW includes cohorts from all three nurseries (NW, NG, NE) for a mixedorigin design.
- Tree identifiers:
  - FieldCode provides a unique code for each tree (range examples: 5001–5672, 6001–6004, 7001–7672); NA when not transplanted.
  - Block, Row, Column specify planting position within each site.

## Data structure and fields (FieldTraits.txt)
- Core metadata:
  - PopulationCode and Description: population identity and description.
  - Family: family code; individuals sharing a mother tree.
  - FieldSite: FE, FS, or FW indicating planting site.
  - FieldCode: unique tree identifier; NA if not transplanted.
  - Block: randomised block code (A–D at FW; others vary by site).
  - Row and Column: planting row/column coordinates within the block.
- Phenotypic measurements (example groupings and units):
  - Height (HA13–HA20): height after specified growing seasons (2013–2020); units are millimetres.
  - Height increments (HI13–HI20): annual height increase (mm).
  - Base stem diameter (DA13–DA20): base diameter after specified seasons (mm).
  - Diameter increments (DI13–DI20): annual base diameter increase (mm).
  - Budburst duration (BD15–BD19; 2015–2019): duration of budburst in days for spring seasons.
  - BT15_4, BT15_5, BT15_6; ... BT19_6: days since 31 March to reach budburst stages 4, 5, and 6 (various years), including multiple years and replicates.
  - The FieldTraits.txt file provides detailed mapping of each variable to its year, stage, and site, with NA where not applicable (e.g., not transplanted at a site).
- Notes on data structure:
  - Each column includes a description and the unit; many variables are year- or stage-specific (e.g., HA13 versus HA20; BD15 versus BD19; BT15_4 versus BT19_6).
  - The dataset comprises a single file (FieldTraits.txt) with numerous trait columns representing longitudinal measurements and phenology indicators.

## Temporal coverage
- Seed collection and nursery phase: 2007.
- Field establishment: 2012 transplant to field sites.
- Phenotypic measurements on height and diameter: 2013–2020 (varies by site; FE and FW extend to 2020; FS to 2020 with 2014 start for height).
- Phenology (spring assessments): 2015–2019 (2020 not possible due to COVID-19 restrictions).

## Data quality, limitations, and caveats
- 2020 data for phenology were not collected due to COVID-19 restrictions.
- Some families were replaced at FS due to insufficient tree numbers; field representation of certain populations may vary by site.
- Transplant origins differ by site (e.g., FW includes trees raised in three nurseries), which can affect comparability across sites.
- FieldCode availability: NA for trees not transplanted; linkage to spatial location relies on site coordinates and planting layout rather than a per-tree geolocation point in this dataset.
- Data are organized in a single large file (FieldTraits.txt) with many columns; users may need to join with population/family metadata and reconstruct spatial coordinates from Block/Row/Column to generate GIS-ready layers.

## GIS-ready considerations and recommended visualizations
- How to map:
  - Create a spatial layer per field site with planting positions defined by Block, Row, and Column; assign coordinates based on the 3 m x 3 m grid spacing and the site’s relative origin.
  - Link FieldCode to per-tree trait data (height, diameter, budburst, increments) for time-series visualization.
  - Attach PopulationCode/Description and Family to enable population- and family-level mapping.
- Suggested analyses and visuals:
  - Site-level choropleth maps of mean height or diameter by year (2013–2020) to compare growth across FE, FS, and FW.
  - Time-series visualizations (line charts) for selected traits (e.g., HA, DA, HI) by site, population, or family.
  - Phenology maps showing variation in budburst timing (BD, BT/BT_4..6) across sites and populations.
  - Spatial patterns of growth by population origin to explore genotype-environment interactions.
- Data integration tips:
  - Create a spatial index by combining FieldSite with Block/Row/Column to derive approximate coordinates for each tree.
  - Use PopulationCode and Family fields to join with broader provenance data or seed-zone information for enriched GIS analyses.

## Provenance and access
- Source: FieldTraits.txt, part of the metadata for the Long-term multisite Scots pine trial, Scotland: field phenotypes, 2013-2020.
- Scope: One primary data file containing detailed trait metadata and year-specific measurements across three field sites and 21 populations.
- Practical notes:
  - When building GIS products, account for NA values where trees were not transplanted or measurements were not collected in certain years.
  - Be mindful of site-specific differences in nursery origin for FW and FS replacement of underrepresented families at FS.