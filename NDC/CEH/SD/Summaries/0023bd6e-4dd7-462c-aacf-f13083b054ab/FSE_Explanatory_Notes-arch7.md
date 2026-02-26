# Farm Scale Evaluations (FSE) Dataset Descriptions

## Overview
- The Farm Scale Evaluations (FSE) were established to determine whether genetically-modified herbicide-tolerant (GMHT) crops might have significant effects on farmland wildlife due to management practices.
- Data cover four crops: Beet, Maize, Spring-sown oilseed rape, and Winter-sown oilseed rape.
- Data are organized into multiple observational themes, including seedbank, crop vegetation, field-edge vegetation, invertebrates, and additional tables.

## Data categories and what they contain
- Seedbank
  - Seedbank counts from soil samples taken before planting.
  - Follow-ups: Seedbank Follow-up 1 (one year later) and Seedbank Follow-up 2 (two years later).
- Vegetation in the crop
  - First-seedling: vegetation survey before herbicide.
  - Mezzanine: additional survey in Beet (between herbicide applications) and Winter rape (spring, before herbicide).
  - Post-herbicide: vegetation surveyed after herbicide on both conventional and GM sides.
  - Final Counts: vegetation survey concurrent with biomass sampling.
  - Biomass: weeds sampled in the month before harvest.
  - Seed Rain: seeds collected during the growing season.
  - Follow-up 1 and Follow-up 2: vegetation surveys one and two years after the trial.
- Field edge vegetation
  - Margin Attributes around the field boundary.
  - Edge Veg Cover, Edge Veg Flower, Edge Veg Seed, Edge Bare Ground, Edge Spray Damage (recorded at various times).
- Invertebrates
  - Bee and Butterfly transects (monthly Apr–Aug) in crop and margins; Pollinators combines Bee and Butterfly counts.
  - Crop Pests (herbivores on the crop, early and late season).
  - Gastropod Search (gastropods in field margins) and Gastropod Trap (gastropods trapped in crop in spring/autumn).
  - Pitfall (surface-active invertebrates across seasons).
  - Vortis (arthropods on plants, early/late season, in verge and crop).
- Additional tables
  - Date crops were drilled; Herbicides applied; Height/Cover of weeds and crops, etc.

## Data structure, naming conventions and properties
- Table naming convention: abbreviatedprefix_crop_(sample date)_protocol (e.g., sum_b_seedrain for Beet seedrain; sum_b_early_pitfall for Beet early-season pitfall).
- Generic table properties
  - Each row represents half-field totals (counts/biomass/mean percent cover) for a single site.
  - Includes group totals and individual species contributing to groups.
  - Sites are referenced within Defra Government regions; South-eastern and Eastern England regions are aggregated for confidentiality.
  - Nulls indicate missing verified data.
  - Some counts are decimals due to calculations using only a proportion of transects.
- Specific table properties
  - All crop_pest tables use a suffix of 'W+' or 'W-' to denote winged vs. wingless.
- Column headings (examples)
  - conv_count, conv_count_FL, conv_count_GE4TL, conv_count_L4TL, conv_count_SE
  - crop_cover (percent cover of crop), crop_unit (C = conventional, GM = GM crop), crop_height
  - gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE
  - name (species or group name), site_ref (site reference), Region (Defra region)
  - VEG/ARTHROPOD/GASTROPOD/BB_BRC codes (codes used by Biological Records Centre)
  - weed_cover_pc (percent cover of non-crop vegetation)
- References to further information
  - The spring-sown crops theme: Phil. Trans. Roy. Soc. B (2003) 358(1439)
  - Winter rape study: Roy. Soc. B (2005) 272 463–474

## Geographic and temporal scope
- Geographic: Sites are organized by Defra Government regions; some regional aggregation applied for confidentiality.
- Temporal: Multi-year data collection with seasonal surveys (April–August for invertebrates; pre- and post-herbicide timings; seedbank follow-ups at 1 and 2 years; biomass and final counts near harvest).

## How this supports GIS analysis
- Enables map-based visualization of:
  - Seedbank status and changes over time.
  - Vegetation dynamics within crops and at field margins.
  - Field-edge habitat features and spray-damage patterns.
  - Spatial distribution of invertebrates, pollinators, pests, and gastropods.
- Facilitates comparisons between conventional and GMHT crops across sites and regions.
- Data can be joined via site_ref to region shapefiles and crop-type layers; enables aggregation by crop, region, or time period.
- Handles multi-resolution data (site-level totals, species-level groups) with explicit notes on missing data and partial transect calculations.

## Access and usage notes
- Use the table naming convention to locate data by crop and protocol/date.
- Join site_ref with GIS layers to map spatial patterns; use Region for regional analyses.
- Be mindful of missing values (nulls) and decimal values resulting from transect-based calculations.
- For in-depth interpretation, consult the cited publications describing related methods and findings.