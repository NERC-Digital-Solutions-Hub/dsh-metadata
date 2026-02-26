# Explanatory notes

- The Farm Scale Evaluations (FSE) were set up to determine whether genetically-modified herbicide-tolerant (GMHT) crops might have any significant effects on farmland wildlife resulting from the way the crops would be managed.

## Dataset scope and components

- Four crops studied: Beet, Maize, Spring-sown oilseed rape, Winter-sown oilseed rape
- Data collection areas cover multiple trial sites and include:
  - Seedbank: initial soil sample before planting, plus Follow-up 1 (one year after) and Follow-up 2 (two years after)
  - Vegetation in the crop: multiple surveys such as First-seedling, Mezzanine surveys, Post-herbicide, Final Counts, Biomass, Seed Rain, Follow-ups
  - Field edge vegetation: Margin Attributes; Edge Veg Cover, Edge Veg Flower, Edge Veg Seed; Edge Bare Ground; Edge Spray Damage
  - Invertebrates: Bee and Butterfly transects; Pollinators; Crop Pests; Gastropod searches and traps; Pitfall; Vortis
  - Additional tables: dates crops were drilled; herbicides applied; weed and crop height/cover
- Provisions for timepoints and seasonal coverage across both crop and field-edge environments

## Data structure and conventions

- Table naming convention: abbreviatedprefix_crop_(sample date)_protocol (e.g., sum_b_seedrain for Beet seed rain; sum_b_early_pitfall for Beet early pitfall)
- Each row represents half-field totals (counts/biomass/mean percent cover) for a separate individual site
- Group totals and individual species data are included
- Sites are referenced within Defra Government regions; South-eastern and Eastern England regions are aggregated
- Nulls appear where no verified data were collected
- Some counts are decimal due to calculations from a proportion of transects

## Tables, properties, and variables

- Generic table properties:
  - Columns include counts, biomass, and percentages (e.g., conv_count, conv_count_FL, conv_count_GE4TL, conv_count_L4TL, crop_cover, crop_unit, crop_height, gm_count, etc.)
  - Name column lists species or groups
  - site_ref: site reference number (consistent across related tables)
  - Region: Defra government region or aggregate
  - VEG/ARTHROPOD/GASTROPOD/BB_BRC: codes for data type
  - weed_cover_pc: percent cover of non-crop vegetation
- Specific table properties:
  - crop_pest tables include a suffix W+ or W- indicating winged vs wingless forms
- Column headers and data types cover: conventional vs GMHT counts, crop and GMHT cover, plant life stages (SE, FL, GE4TL, L4TL), height, and species names

## Metadata, discoverability, and references

- Data are organized to support cross-site and cross-region analyses with clear site references and protocol designations
- References for methodological context:
  - Phil. Trans. Royal Soc., 2003: The spring crops theme issue
  - Proc. Roy. Soc. B, 2005: Effects on weed and invertebrate abundance and diversity of herbicide management in GM herbicide-tolerant winter-sown oilseed rape

## Relevance for Data Leaders

- Demonstrates a comprehensive, multi-component data governance approach:
  - Standardized naming conventions and cross-table linkages
  - Rich metadata with timepoints, protocols, and region classifications
  - Clear data structuring to enable integration across crop types, habitats, and taxa
- Highlights practical data management considerations:
  - Handling of partial transects leading to decimal values
  - Aggregation of regions and site-level granularity
  - Documentation of measurement methods and variables for transparency and reproducibility
- Points to ongoing challenges and opportunities:
  - Ensuring data standards across diverse datasets (seedbank, vegetation, invertebrates, margins)
  - Maintaining discoverability and updatability of assets
  - Coordinating sector-wide data practices to avoid duplication and to support broader analyses