# Explanatory notes

## Overview
- The Farm Scale Evaluations (FSE) were established to assess whether genetically-modified herbicide-tolerant (GMHT) crops have significant effects on farmland wildlife due to management practices.
- Data described cover four crops: Beet, Maize, Spring-sown oilseed rape, and Winter-sown oilseed rape.
- Datasets span multiple domains: seedbank, crop vegetation, field edge vegetation, invertebrates, and additional management tables (e.g., drilling dates, herbicide applications, weed/crop height or cover).

## Dataset structure and contents

- Seedbank
  - Seedbank: counts of plant species germinating from soil samples taken pre-planting.
  - Seedbank Follow-up 1: repeat soil sample one year after initial sample.
  - Seedbank Follow-up 2: final soil sample two years after the initial sample.

- Vegetation in the crop
  - First-seedling: earliest vegetation survey in the crop prior to herbicide.
  - Mezzanine (Beet) / Mezzanine (Winter rape): additional vegetation surveys around herbicide application differences or timing.
  - Post-herbicide: vegetation survey after herbicide application to both conventional and GM sides.
  - Final Counts: vegetation survey concurrent with biomass sampling.
  - Biomass: weeds sampled month before harvest.
  - Seed Rain: counts of seeds produced during the growing season.
  - Follow-up 1 / Follow-up 2: vegetation surveys one and two years after the trial crop.

- Field edge vegetation
  - Margin Attributes: physical features around field edge.
  - Edge Veg Cover: cover of non-crop vegetation in June.
  - Edge Veg Flower: flowering from April to August.
  - Edge Veg Seed: seed setting in July and August.
  - Edge Bare Ground: percent bare ground.
  - Edge Spray Damage: vegetation damage from spraying.

- Invertebrates
  - Bee and Butterfly transects: monthly counts in crop and field margins (April–August); Pollinators combines Bees & Butterflies.
  - Crop Pests: herbivores on the crop early/late in the season.
  - Gastropod Search / Gastropod Trap: gastropod counts in margins and crop (spring/autumn).
  - Pitfall: counts of surface-active invertebrates (early/mid/late).
  - Vortis: arthropods on plants (early/late) in verge and crop.

- Additional tables
  - Date drilled; Herbicides applied; Height/Cover of weeds and crop.

- Table naming convention
  - Format: abbreviatedprefix_crop_(sample date)_protocol (e.g., sum_b_seedrain, sum_b_early_pitfall).

- Generic table properties
  - Each row represents half-field totals for a single site.
  - Group totals plus species-level contributions are included.
  - Sites are referenced within Defra regions; South-eastern and Eastern England regions are aggregated for confidentiality.
  - Nulls appear where data were not collected; some counts shown with decimals due to partial transects.

- Specific table properties
  - All crop_pest tables include suffixes 'W+' or 'W-' to denote winged vs. wingless forms.

- Column headings (examples)
  - conv_count / conv_count_FL / conv_count_GE4TL / conv_count_L4TL / conv_count_SE
  - crop_cover / crop_unit
  - crop_height
  - gm_count / gm_count_FL / gm_count_GE4TL / gm_count_L4TL / gm_count_SE
  - name (species or group name)
  - site_ref
  - Region
  - VEG/ARTHROPOD/GASTROPOD/BB_BRC (code for data type)
  - weed_cover_pc (percent cover of non-crop vegetation)

- Notes on interpretation
  - Some tables present data at half-field and site levels, enabling comparison across conventional vs GMHT management and across regions.
  - Provincial regional aggregation is used to protect farmer confidentiality.

## Data quality, governance, and challenges

- Data governance considerations
  - Ensuring consistent metadata across crops, surveys, and timepoints (definitions for each survey, sampling dates, protocols).
  - Maintaining the table naming conventions for discoverability and interoperability.
  - Documenting units, species names, and region references to support reuse and meta-analyses.
  - Tracking data availability, limitations, and any embargo or proprietary constraints.

- Practical challenges (relevant to data stewards)
  - Incomplete or delayed data from some sites or surveys.
  - Achieving timely data submission from data creators and coordinating across diverse systems/formats.
  - Handling large, multi-year datasets and potential non-interoperable legacy databases.
  - Managing confidentiality leading to region aggregation and potential data gaps for some sites.

## Access, usage, and documentation

- Datasets are linked to published methodological and environmental context (e.g., related Royal Society papers and specific Farm Scale Evaluations reports).
- Users should refer to the detailed table definitions, naming conventions, and protocol descriptions to correctly interpret data across crops and years.
- When updating or sharing datasets, maintain the established conventions, document any deviations, and note any data quality issues or missing values.

## References and further information

- The document references additional methodological context and related publications:
  - Phil. Trans. Royal Soc., 2003; 358 (1439) for spring crops.
  - Bohan et al., 2005, Proceedings of the Royal Society B, for winter rape effects on weed and invertebrate abundance and diversity.