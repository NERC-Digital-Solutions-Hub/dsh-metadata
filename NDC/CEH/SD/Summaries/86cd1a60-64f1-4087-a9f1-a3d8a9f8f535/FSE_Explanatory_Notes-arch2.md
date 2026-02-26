# Farm Scale Evaluations (FSE)

## Purpose and scope
- Established to determine if genetically-modified herbicide-tolerant (GMHT) crops have significant effects on farmland wildlife due to management practices.
- Data cover four crops: Beet, Maize, Spring-sown Oilseed Rape, and Winter-sown Oilseed Rape.

## Datasets and data categories
- Seedbank
  - Seedbank counts of germinating plant species from soil samples taken before planting; includes Follow-up 1 (one year after) and Follow-up 2 (two years after).
- Vegetation in the crop
  - First-seedling survey (pre-herbicide).
  - Mezzanine surveys (Beet: between herbicide applications on conventional vs GM sides; Winter Rape: spring before herbicide).
  - Post-herbicide survey (after herbicide on both sides).
  - Final Counts (aligned with biomass sampling).
  - Biomass (weeds in the crop, sampled the month before harvest).
  - Seed Rain (continuous seed production through the season).
  - Follow-up surveys (Follow-up 1 after one year; Follow-up 2 after two years).
- Field edge vegetation
  - Margin Attributes near field boundary.
  - Edge Veg Cover, Edge Veg Flower, Edge Veg Seed, Edge Bare Ground, Edge Spray Damage (collected across the field margin/ verge data).
- Invertebrates
  - Bee and Butterfly transects (monthly, April–August, within crop and field margins).
  - Pollinators (combined Bee and Butterfly counts).
  - Crop Pests (herbivores on the crop, early and late season).
  - Gastropods (Gastropod Search in margins; Gastropod Trap in crop; spring and autumn).
  - Pitfall traps (surface-active invertebrates, early/mid/late season).
  - Vortis (arthropods on plants, early and late season, in verge and crop).
- Additional tables
  - Dates crops were drilled; herbicides applied; height/cover of weeds and crop.

## Data structure, standardization, and metadata
- Naming conventions
  - Tables named with a consistent abbreviated prefix for crop, sample date, and protocol (e.g., sum_b_seedrain for Beet seed rain; sum_b_early_pitfall for Beet early pitfall).
- Generic properties
  - Each row represents half-field totals for a single site; includes group totals and species-level details.
  - Sites referenced within Defra Government regions; South-eastern and Eastern England regions are aggregated.
  - Nulls indicate missing verified data; some counts shown with decimals due to partial transects.
- Specific table properties
  - Crop pest tables use a naming suffix of W+ (winged) or W- (wingless).
- Column headings (example)
  - conv_count, conv_count_FL, conv_count_GE4TL, conv_count_L4TL, conv_count_SE
  - crop_cover, crop_unit, crop_height
  - gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE
  - name (species or group name), site_ref, Region
  - VEG/ARTHROPOD/GASTROPOD/BB_BRC codes, weed_cover_pc
- Data scope and regionalization
  - Data are compiled by site and region; regional aggregation applies to certain regions for confidentiality or reporting purposes.

## Temporal design and sampling schedule
- Seedbank and vegetation surveys conducted at specified pre- and post-treatment intervals (before planting, before/after herbicide applications, final counts, and multiple follow-ups).
- Field margins and invertebrate surveys span active growing season months (e.g., April–August for many transects).

## Data quality, accessibility, and documentation
- Emphasizes standardized methods and cross-dataset comparability to support policy evaluation and environmental health monitoring.
- Data are organized to allow traceability to sites and Defra regions; some regional aggregation is applied.
- Notes provide references to detailed methodological and ecological analyses (e.g., Royal Society Proceedings papers for spring crops and winter rape).

## References and further information
- Detailed methodological context and findings available in:
  - Theoretical and empirical treatment of spring crops: Phil. Trans. Royal Soc. B (2003/2005) on weed and invertebrate responses to GM herbicide management in crops.
  - Specific analyses on effects of GMHT on winter-sown oilseed rape (2005 Royal Society Proceedings).

## Implications for analysts monitoring the environment
- The dataset provides a standardized, multi-taxa, temporally rich framework to assess environmental health and potential GM crop effects on farmland wildlife.
- Useful for cross-study comparisons, integration with other environmental data, and monitoring policy performance over time.
- Analysts should note regional aggregation, data completeness (nulls), and the need to maintain data lineage via site_ref and table-naming conventions when aggregating or deriving outputs.