# Explanatory notes The Farm Scale Evaluations (FSE) were setup to determine whether genetically-modified herbicide-tolerant (GMHT) crops might have any significant effects on farmland wildlife resulting from the way the crops would be managed.

## Dataset scope and crops
- Data collected for four crops: Beet, Maize, Spring-sown oilseed rape, and Winter-sown oilseed rape.

## Data collection categories
- Seedbank
  - Seedbank: counts of plant species germinating from soil samples before planting.
  - Seedbank Follow-up 1: repeat soil sample one year after initial seedbank sample.
  - Seedbank Follow-up 2: final soil sample two years after initial seedbank sample.
- Vegetation in the crop
  - First-seedling: first vegetation survey before herbicide application.
  - Mezzanine: Beet includes an additional survey between herbicide applications on conventional vs GM sides; Winter rape Mezzanine survey in spring before any herbicide.
  - Post-herbicide: vegetation survey after herbicide on both conventional and GM sides.
  - Final Counts: vegetation survey concurrent with biomass sampling.
  - Biomass: weeds sampled month before harvest.
  - Seed Rain: seeds collected throughout the growing season.
  - Follow-up 1: vegetation survey one year after the trial.
  - Follow-up 2: vegetation survey two years after the trial.
- Field edge vegetation
  - Margin Attributes: data from field boundary, margin, verge.
  - Edge Veg Cover: cover of plant species in June.
  - Edge Veg Flower: flowering data from April–August.
  - Edge Veg Seed: seed setting in July–August.
  - Edge Bare Ground: percent bare ground.
  - Edge Spray Damage: vegetation damage from spraying.
- Invertebrates
  - Bee and Butterfly transects: monthly counts in crop and field margins (April–August); Pollinators combines Bee and Butterfly counts.
  - Crop Pests: counts of herbivores on the crop early and late in the season.
  - Gastropod Search: gastropods in the field margin.
  - Gastropod Trap: gastropods trapped in the crop (spring and autumn).
  - Pitfall: counts of surface-active invertebrates (early, mid, late).
  - Vortis: arthropods on plants (early and late) in field verge and crop.
- Additional tables
  - Date drilled; Herbicides applied; Height/Cover of weeds and crops.

## Data structure, naming, and organization
- Table name convention: abbreviatedprefix_crop_(sample date)_protocol (e.g., sum_b_seedrain; sum_b_early_pitfall).
- Generic table properties:
  - Each row = half-field totals (counts/biomass/mean percent cover) for a separate site.
  - Group totals and individual species contributed to these groups are included.
  - Sites referenced within Defra Government regions; South-eastern and Eastern England regions aggregated for farmer confidentiality.
  - Nulls indicate no verified data; some counts shown with decimals due to partial transects.
- Specific table properties:
  - All crop_pest tables have a name suffix of 'W+' or 'W-' to indicate winged vs wingless.

## Column headings and data codes
- Examples of columns:
  - conv_count, conv_count_FL, conv_count_GE4TL, conv_count_L4TL, conv_count_SE
  - crop_cover, crop_unit (C = conventional crop, GM = GM crop)
  - crop_height
  - gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE
  - name (species or group name)
  - site_ref (site reference number, consistent across all tables)
  - Region (Defra Government region or aggregates)
  - VEG/ARTHROPOD/GASTROPOD/BB_BRC (Biological Records Centre code)
  - weed_cover_pc (percent cover of non-crop vegetation)

## Relevance and usage
- Designed to enable analysis of potential effects of GMHT herbicide management on farmland wildlife across multiple ecological indicators (seedbank, vegetation, margins, invertebrates, pests, gastropods) and crop types.
- Provides structured, standardized data across sites and regions to support cross-crop comparisons and temporal analyses.
- Methodological context references:
  - Spring crops: Phil. Trans. Royal Soc. B, 2003
  - Winter-sown oilseed rape: Proceedings of the Royal Society B, 2005