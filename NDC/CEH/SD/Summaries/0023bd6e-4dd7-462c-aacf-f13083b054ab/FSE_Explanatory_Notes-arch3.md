# Explanatory notes

- The Farm Scale Evaluations (FSE) were set up to determine whether genetically-modified herbicide-tolerant (GMHT) crops might have significant effects on farmland wildlife due to how the crops are managed.

## Dataset scope

- Crops studied: Beet, Maize, Spring-sown oilseed rape, Winter-sown oilseed rape.
- Data collection domains:
  - Seedbank: Counts of germinating plant species from soil samples before planting; Follow-up samples at one year and two years after.
  - Vegetation in the crop: Surveys including First-seedling; Mezzanine surveys (Beet and Winter rape); Post-herbicide surveys on conventional vs GM sides; Final counts aligned with biomass sampling; Seed rain; Follow-up vegetation surveys at one and two years.
  - Field edge vegetation: Margin Attributes and a suite of boundary/verge protocols (Edge Veg Cover, Edge Veg Flower, Edge Veg Seed, Edge Bare Ground, Edge Spray Damage).
  - Invertebrates: Monthly Bee and Butterfly transects (April–August); Pollinators (combined bee and butterfly counts); Crop Pests; Gastropods (Search in margins, Trap in crop); Pitfall; Vortis (arthropods on plants) across verge and crop.
  - Additional tables: Crop drilling dates, herbicide applications, weed/crop height and cover.
  
## Table naming convention and data structure

- Table naming: Abbreviatedprefix_crop_(sample date)_protocol (e.g., sum_b_seedrain for Beet seed rain; sum_b_early_pitfall for Beet early-season pitfall).
- Generic properties:
  - Each row represents half-field totals (counts/biomass/mean percent cover) for a separate site.
  - Both group totals and individual species contributions are provided.
  - Sites are referenced within Defra Government regions; Southeastern and Eastern England regions are aggregated for confidentiality.
  - Nulls indicate no verified data.
  - Some counts use decimal places due to sampling proportions.
- Specific properties:
  - For crop pest tables, suffixes include W+ or W- to denote winged/wingless forms.
  
## Column headings and key variables

- Conventional vs GMHT comparisons:
  - conv_count, conv_count_FL (flowering), conv_count_GE4TL (≥4 true-leaved), conv_count_L4TL (<4 true-leaved), conv_count_SE (seeding).
  - gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE.
  - crop_cover (percent cover of crop), crop_unit (C = conventional crop, GM = GM crop), crop_height (cm).
  - name (species or group name), site_ref (site identifier), Region (Defra region or aggregate).
- Other data descriptors:
  - VEG/ARTHROPOD/GASTROPOD/BB_BRC codes (IDs for vegetation/arthropods/gastropods/bees & butterflies).
  - weed_cover_pc (percent cover of non-crop vegetation).

## Data context and governance considerations

- Data are designed to enable analysis of GMHT management effects on wildlife by providing site-level and region-level context, with standardized reporting through reports, charts, or dashboards.
- Metadata and data sharing considerations are implicit in the dataset structure:
  - Aggregation for confidentiality (e.g., regional aggregation) and explicit recording of nulls where data are absent.
  - The dataset emphasizes the need for clear communication of complex findings and the ability to verify data through robust metadata and consistent table schemas.
- Contextual references:
  - The document notes alignment with related research, including: The spring-sown crops theme issue (Phil. Trans. Royal Soc. 2003) and a 2005 Proceedings of the Royal Society paper on effects of herbicide management in winter-sown oilseed rape.

## Relevance to monitoring framework goals

- Provides a comprehensive, standardized data framework to monitor environmental health implications of GMHT crop management.
- Supports evaluation of policy implications and informs future decision-making through cross-cutting measures (seedbank dynamics, vegetation and edge habitat, invertebrate communities, pests, and non-crop flora).
- Demonstrates how to structure datasets for transparency, reproducibility, and governance, including clear data provenance, site-level versus aggregated reporting, and handling of incomplete data.