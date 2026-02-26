# Farm Scale Evaluations (FSE)

- Purpose and scope
  - Established to determine whether genetically-modified herbicide-tolerant (GMHT) crops have significant effects on farmland wildlife due to management practices.
  - Case studies span four crops: Beet, Maize, Spring-sown oilseed rape, and Winter-sown oilseed rape.
  - Data are collected to monitor environmental health and policy performance over time using standardized protocols.

- Data collected and themes
  - Seedbank
    - Seedbank: counts of plant species germinating from soil samples before planting.
    - Seedbank Follow-ups: follow-up samples at 1 year and 2 years after the initial sample.
  - Vegetation in the crop
    - First-seedling: initial vegetation survey before herbicide.
    - Mezzanine: additional survey in beet and winter rape comparing conventional vs GM sides (Beet Mezzanine; Winter Rape Mezzanine).
    - Post-herbicide: vegetation survey after herbicide application on both conventional and GM sides.
    - Final Counts: vegetation survey concurrent with biomass sampling.
    - Biomass: weed biomass measured in the month before harvest.
    - Seed Rain: seeds produced during the growing season.
    - Follow-up vegetation surveys at 1 year and 2 years.
  - Field edge vegetation
    - Margin Attributes: physical features around field edges.
    - Edge Veg Cover: cover of non-crop vegetation in June.
    - Edge Veg Flower: flowering from April to August.
    - Edge Veg Seed: seed setting in July–August.
    - Edge Bare Ground: percent bare ground.
    - Edge Spray Damage: vegetation damage from spraying.
  - Invertebrates
    - Bee and Butterfly transects: monthly counts April–August in crop and margins (Pollinators combines bees & butterflies).
    - Crop Pests: herbivores on crops early and late in the season.
    - Gastropods: Gastropod Search (field margins) and Gastropod Trap (in crop, spring and autumn).
    - Pitfall: surface-active invertebrates early, mid, and late season.
    - Vortis: arthropods on plants, early and late season in verge and crop.
  - Additional tables
    - Dates crops were drilled; herbicides applied; height/cover of weeds and crop.
  - Data conventions
    - Table naming follows: abbreviatedprefix_crop_(sample date)_protocol, e.g., sum_b_seedrain or sum_b_early_pitfall.
    - Each row represents half-field totals for a separate site; group totals and species contributions are included.
    - Sites are referenced within Defra regions; South-eastern and Eastern England regions are aggregated for confidentiality.
    - Nulls indicate missing verified data; some counts include decimals due to partial transects.
    - Crop_pest tables use a suffix of W+ (winged) or W- (wingless).

- Data structure and variables
  - Column headings include:
    - conv_count, conv_count_FL, conv_count_GE4TL, conv_count_L4TL, conv_count_SE
    - crop_cover (percent cover of crop), crop_unit (C for conventional, GM for GM crop)
    - crop_height (cm), gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE
    - name (species or group), site_ref (site identifier), Region (Defra region or aggregates)
    - VEG/ARTHROPOD/GASTROPOD/BB_BRC (codes for flora/arthropods/gastropods/bees & butterflies)
    - weed_cover_pc (percent cover of non-crop vegetation)
  - Specific conventions
    - Region data may be aggregated for confidentiality reasons.
    - W+ / W- suffixes indicate winged vs wingless forms in pest tables.

- Data management, QA, and outputs
  - Data are verified, quality assured, cleaned, and transformed.
  - Outputs are presented as reports, maps, and charts.
  - Datasets are stored and uploaded to appropriate portals for accessibility and long-term monitoring.

- Relevance to environmental monitoring and policy
  - Provides standardized, repeatable datasets to assess environmental health and GMHT crop impacts over time.
  - Facilitates cross-site and cross-crop comparisons within Defra-regulated monitoring.
  - Highlights both direct biological responses (seedbank, vegetation, invertebrates) and edge/landscape interactions (field margins, spray damage).

- Notable references
  - Thematic note: The spring-sown GM crop theme issue (Phil. Trans. Royal Soc. B, 2003).
  - Winter rape study: Effects on weed and invertebrate abundance/diversity under GM herbicide management (Proc. Royal Soc. B, 2005).