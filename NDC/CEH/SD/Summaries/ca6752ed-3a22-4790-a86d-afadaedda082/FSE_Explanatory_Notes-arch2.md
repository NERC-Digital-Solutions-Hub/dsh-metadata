# Farm Scale Evaluations (FSE) Dataset Descriptions

## Aim and Scope
- The Farm Scale Evaluations (FSE) were set up to determine whether genetically-modified herbicide-tolerant (GMHT) crops might have significant effects on farmland wildlife due to management practices.
- Crops studied: Beet, Maize, Spring-sown oilseed rape, Winter-sown oilseed rape.

## Data collected and domains
- Seedbank
  - Seedbank: counts of plant species germinating from soil samples taken before planting.
  - Seedbank Follow-up 1: repeat soil sample one year after initial seedbank sample.
  - Seedbank Follow-up 2: final soil sample two years after the initial sample.
- Vegetation in the crop
  - First-seedling: first vegetation survey before herbicide is applied.
  - Mezzanine: Beet includes an additional vegetation survey between herbicide on conventional vs GM side; Winter rape includes a spring pre-herbicide survey.
  - Post-herbicide: vegetation survey after herbicide applied to both conventional and GM sides.
  - Final Counts: vegetation survey aligned with biomass sampling.
  - Biomass: weeds sampled in the crop, taken in the month before harvest.
  - Seed Rain: seeds collected throughout the growing season.
  - Follow-up 1: vegetation survey one year after the trial.
  - Follow-up 2: vegetation survey two years after the trial.
- Field edge vegetation
  - Margin Attributes: physical features around the trial field boundary.
  - Edge Veg Cover: percent cover of non-crop vegetation in June.
  - Edge Veg Flower: plant flowering from April to August.
  - Edge Veg Seed: plant seed setting in July and August.
  - Edge Bare Ground: percent bare ground.
  - Edge Spray Damage: vegetation damage from spraying.
- Invertebrates
  - Bee and Butterfly transects: monthly (April–August) in the crop and field margins; Pollinators = combined Bee and Butterfly counts.
  - Crop Pests: counts of herbivores on the crop early and late in the season.
  - Gastropod Search: gastropods in the field margin.
  - Gastropod Trap: gastropods trapped in the crop in spring and autumn.
  - Pitfall: counts of surface-active invertebrates early, mid, and late in the season.
  - Vortis: counts of arthropods on plants, in field verge and crop, early and late.
- Additional tables
  - Date the crops were drilled.
  - Herbicides applied to the crops.
  - Height/Cover of weeds and crop.

## Table naming conventions
- All tables use: abbreviatedprefix_crop_(sample date)_protocol (e.g., sum_b_seedrain for Beet crop seedrain; sum_b_early_pitfall for Beet crop early pitfall).

## Generic properties
- Each row represents half-field totals (counts/biomass/mean percent cover) for a separate individual site.
- Group totals are provided along with individual species contributing to those groups.
- Sites are referenced within Defra Government regions; South-eastern and Eastern England regions are aggregated for confidentiality.
- Nulls appear where no verified data were collected.
- Some counts include decimals due to calculation from a proportion of transects.

## Specific table properties
- All crop_pest tables: name suffix 'W+' or 'W-' indicates winged or wingless.

## Column headings (examples)
- conv_count, conv_count_FL, conv_count_GE4TL, conv_count_L4TL, conv_count_SE (conventional crop counts).
- crop_cover, crop_unit, crop_height (crop metrics).
- gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE (GMHT crop counts).
- name (species or group name), site_ref (site reference), Region (Defra region).
- VEG/ARTHROPOD/GASTROPOD/BB_BRC (code for data type).
- weed_cover_pc (percent cover of non-crop vegetation).

## Context and references
- Related methodological notes and background: 
  - The spring crops theme issue: The Farm Scale Evaluations of spring-sown genetically modified crops (Phil. Trans. Royal Soc., 2003).
  - Winter rape study: Effects on weed and invertebrate abundance and diversity of herbicide management in GMHT winter-sown oilseed rape (Proc. Royal Soc. B, 2005).

## Relevance for Analysts Monitoring the Environment
- Provides standardized, multi-endpoint environmental data to assess ecological health and policy performance over time.
- Enables comparisons between GMHT and conventional management across weed communities, invertebrate diversity, and edge habitat conditions.
- Structured for reproducibility and temporal analysis with clear data conventions and regional aggregation rules.

## Data management and accessibility
- Datasets are prepared with quality-conscious processes (verification, QA, cleaning, transformation) and stored/uploaded to appropriate portals.

## Challenges and opportunities
- Increase dataset value by integrating with other relevant environmental data.
- Improve access to underlying data used to generate outputs for broader scrutiny and reuse.