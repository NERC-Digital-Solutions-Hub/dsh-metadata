# Explanatory notes

- The Farm Scale Evaluations (FSE) were set up to determine whether genetically-modified herbicide-tolerant (GMHT) crops might have significant effects on farmland wildlife resulting from the way the crops would be managed.

## Overview of datasets and crops

- Four crops studied: Beet, Maize, Spring-sown oilseed rape, Winter-sown oilseed rape.
- Data collected across multiple ecological components to assess potential GMHT effects.

## Data collection domains

- Seedbank
  - Seedbank: counts of plant species germinating from a soil sample taken before planting.
  - Seedbank Follow-up 1: repeat soil sample one year after the initial seedbank.
  - Seedbank Follow-up 2: final soil sample taken two years after the initial seedbank.
- Vegetation in the crop
  - First-seedling: first vegetation survey before herbicide application.
  - Beet Mezzanine: additional survey in Beet between herbicide applications on conventional vs. GM sides.
  - Winter rape Mezzanine: vegetation survey in spring before any herbicide.
  - Post-herbicide: vegetation survey after herbicide on both conventional and GM sides.
  - Final Counts: vegetation survey coinciding with biomass sampling, taken before harvest.
  - Biomass: weed biomass sampled the month before harvest.
  - Seed Rain: seeds collected throughout the growing season.
  - Follow-up 1 and Follow-up 2: vegetation surveys one and two years after the trial crop.
- Field edge vegetation
  - Margin Attributes: physical features around the trial field edge.
  - Edge Veg Cover: cover of plant species in June.
  - Edge Veg Flower: flowering from April to August.
  - Edge Veg Seed: seed setting in July and August.
  - Edge Bare Ground: percent bare ground.
  - Edge Spray Damage: vegetation damage from spraying.
- Invertebrates
  - Bee and Butterfly transects: monthly counts in the crop and field margins (April–August).
  - Pollinators: combined count of bees and butterflies.
  - Crop Pests: herbivores on the crop early and late in the season.
  - Gastropod Search: gastropods in the field margin.
  - Gastropod Trap: gastropods trapped in the crop (spring and autumn).
  - Pitfall: counts of surface-active invertebrates (early, mid, late season).
  - Vortis: arthropods on plants (early and late season) in the verge and crop.
- Additional tables
  - Dates crops were drilled.
  - Herbicides applied to the crops.
  - Height/Cover of weeds and crop.

## Data structure and conventions

- Table naming convention
  - Example format: sum_b_seedrain (summary for Beet crop for seedrain) or sum_b_early_pitfall (Beet crop for early-season pitfalls); uses the pattern crop_(sample date)_protocol with an abbreviated prefix.
- Generic table properties
  - Each row represents half-field totals (counts/biomass/mean percent cover) for a single site.
  - Includes both group totals and contributions from individual species.
  - Sites are referenced within Defra Government regions; South-eastern and Eastern England regions are aggregated.
  - Nulls appear where no verified data were collected.
  - Some counts are decimal due to calculations based on a subset of transects.
- Specific table properties
  - All crop_pest tables use a suffix of 'W +' or 'W-' to indicate winged vs. wingless forms.
- Column headings and data meaning
  - conv_count, conv_count_FL, conv_count_GE4TL, conv_count_L4TL, conv_count_SE: conventional crop counts at various plant stages.
  - crop_cover, crop_unit, crop_height: percent cover of crop, unit type (C = conventional, GM = GM crop), and crop height in cm.
  - gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE: GMHT crop counts at corresponding stages.
  - name: species or group name (scientific or common British name).
  - site_ref: site reference number (consistent across all tables for cross-crop alignment).
  - Region: Defra Government region or aggregates; VEG/ARTHROPOD/GASTROPOD/BB_BRC codes: data codes for vegetation/arthropods/gastropods/Bees&Butterflies.
  - weed_cover_pc: percent cover of non-crop vegetation.
- Context and references
  - Further information on spring crops: The Farm Scale Evaluations of spring-sown genetically modified crops (Phil. Trans. Royal Soc. B, 2003).
  - Winter rape study: Effects on weed and invertebrate abundance and diversity of herbicide management in GM herbicide-tolerant winter-sown oilseed rape (Proc. R. Soc. B, 2005).

## Timing, protocols, and data quality

- Sampling cadence
  - Vegetation and invertebrate surveys conducted across critical stages (pre- and post-herbicide applications; monthly transects Apr–Aug; follow-ups 1 and 2 years later).
- Data quality and standardisation
  - Established protocols, verification and quality assurance processes, and standardised data representations to support cross-site and cross-crop comparisons.
- Data accessibility and reuse
  - Dataset structure is designed to enable integration with other data sources and to facilitate access to underlying data for broader scrutiny and secondary analyses.

## Relevance for environmental monitoring and analysis

- Enables assessment of potential ecological impacts of GMHT crop management on farmland wildlife and vegetation.
- Provides standardized, multi-domain datasets (seedbank, vegetation, field margins, invertebrates) suitable for trend analysis over time and across regions.
- Supports data-driven policy evaluation and monitoring through structured, queryable tables with clear site, region, and temporal linkages.