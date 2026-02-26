# Explanatory notes

## Overview
- Farm Scale Evaluations (FSE) were established to determine whether genetically-modified herbicide-tolerant (GMHT) crops might have significant effects on farmland wildlife due to crop management practices.

## Datasets and Crops
- Data collected for four crops:
  - Beet
  - Maize
  - Spring-sown Oilseed Rape
  - Winter-sown Oilseed Rape

## Data collection domains
- Seedbank
  - Seedbank counts: plant species germinating from soil samples taken before planting.
  - Seedbank Follow-up 1: repeat soil sample one year after initial seedbank sample.
  - Seedbank Follow-up 2: final soil sample taken two years after initial sample.
- Vegetation in the crop
  - First-seedling: first vegetation survey before herbicide application.
  - Mezzanine (Beet): vegetation survey between herbicide applications on conventional vs GM sides.
  - Winter Rape Mezzanine: vegetation survey in spring before herbicide on GM side.
  - Post-herbicide: vegetation survey after herbicide on both conventional and GM sides.
  - Final Counts: vegetation survey at the same time as biomass sampling.
  - Biomass: weeds sampled in the month before harvest.
  - Seed Rain: seeds collected throughout the growing season.
  - Follow-up 1: vegetation survey one year after the trial crop.
  - Follow-up 2: vegetation survey two years after the trial crop.
- Field edge vegetation
  - Margin Attributes: data from field boundary, margin, and verge.
  - Edge Veg Cover: cover of plant species in June.
  - Edge Veg Flower: flowering from April to August.
  - Edge Veg Seed: seed setting in July and August.
  - Edge Bare Ground: percent bare ground.
  - Edge Spray Damage: vegetation damage from spraying.
- Invertebrates
  - Bee and Butterfly transects: monthly counts April–August in crop and field margins.
  - Pollinators: combined Bee and Butterfly counts.
  - Crop Pests: counts of herbivores on the crop (early and late season).
  - Gastropod Search: gastropods in field margin.
  - Gastropod Trap: gastropods trapped in crop (spring and autumn).
  - Pitfall: counts of surface-active invertebrates (early, mid, late).
  - Vortis: arthropod counts on plants (early and late) in verge and crop.
- Additional tables
  - Dates crops were drilled.
  - Herbicides applied to the crops.
  - Height/cover of weeds and crops.

## Data structure and naming
- Table naming convention
  - All tables are named using: abbreviatedprefix_crop_(sample date)_protocol
  - Examples: sum_b_seedrain (Beet crop, seedrain), sum_b_early_pitfall (Beet crop, early pitfall)
- Generic table properties
  - Each row represents half-field totals (counts/biomass/mean percent cover) for a separate site.
  - Group totals are provided as well as individual species contributing to groups.
  - Sites are referenced within Defra Government regions; South-eastern and Eastern England regions are aggregated for confidentiality.
  - Nulls appear where no verified data were collected.
  - Some counts are decimals due to calculations using only a proportion of transects.
- Specific table properties
  - crop_pest tables use a naming suffix of 'W+' or 'W-' to indicate winged/wingless forms.

## Column headings and data fields
- Examples of key columns
  - conv_count, conv_count_FL, conv_count_GE4TL, conv_count_L4TL, conv_count_SE
  - crop_cover (percent cover of crop), crop_unit (C = conventional, GM = GM crop)
  - crop_height (crop height in cm)
  - gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE
  - name (species or group name)
  - site_ref (site reference number, consistent across all tables)
  - Region (Defra Government region or aggregate)
  - VEG/ARTHROPOD/GASTROPOD/BB_BRC codes
  - weed_cover_pc (percent cover of non-crop vegetation)
- Additional protocol-specific fields
  - Edge Veg Cover, Edge Veg Flower, Edge Veg Seed, Edge Bare Ground, Edge Spray Damage
  - Pollinators, Beetle/Butterfly counts, herbivore counts, gastropod counts, pitfall counts, Vortis counts
- Data notes
  - Tables include both half-field totals for sites and aggregated region-level context.
  - Data are linked across tables via site_ref and region, enabling spatial joins for GIS analyses.

## GIS-relevant aspects
- Spatial granularity
  - Data are organized at the site level with half-field totals, suitable for mapping site-level biodiversity and management effects.
- Temporal scope
  - Multiple time points from pre-planting through several years (Seedbank, vegetative surveys, follow-ups, and biomass/seed rain) support temporal trend analyses.
- Data integration
  - Consistent site_ref and region fields facilitate joins across vegetation, invertebrate, and field-edge datasets for composite spatial analyses.
- Data quality considerations
  - Nulls indicate missing data; some values are derived from partial transects, which should be considered in uncertainty assessments.
- Usage potential
  - Map-based visualizations of GMHT management effects on flora and invertebrates
  - Spatial pattern analysis by Defra regions
  - Temporal GIS analyses across multiple years and crop types

## References and further information
- Related methodological and thematic information:
  - The spring-sown crops theme: Phil. Trans. Royal Soc. B, 2003
  - Effects on weed and invertebrate abundance and diversity of herbicide management in GMHT winter-sown oilseed rape: Proceedings of the Royal Society B, 2005