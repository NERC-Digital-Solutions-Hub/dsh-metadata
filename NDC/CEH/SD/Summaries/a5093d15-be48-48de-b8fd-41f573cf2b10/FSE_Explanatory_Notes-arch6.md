# Explanatory notes The Farm Scale Evaluations (FSE) were setup to determine whether genetically-modified herbicide-tolerant (GMHT) crops might have any significant effects on farmland wildlife resulting from the way the crops would be managed.

- Purpose and scope
  - The Farm Scale Evaluations (FSE) were established to assess potential effects of GMHT crops on farmland wildlife due to management practices.

- Datasets and crops
  - Four crops studied: Beet, Maize, Spring-sown oilseed rape, Winter-sown oilseed rape.

- Data collection domains and protocols
  - Seedbank
    - Seedbank: counts of plant species germinating from soil before planting.
    - Seedbank Follow-up 1: repeat soil sample one year after initial seedbank sample.
    - Seedbank Follow-up 2: final soil sample taken two years after the initial sample.
  - Vegetation in the crop
    - First-seedling: first vegetation survey before herbicide application.
    - Mezzanine (Beet): vegetation survey between herbicide applications on conventional vs GM sides.
    - Winter Rape Mezzanine: vegetation survey in spring before any herbicide.
    - Post-herbicide: vegetation survey after herbicide application on both conventional and GM sides.
    - Final Counts: vegetation survey concurrent with biomass sampling before harvest.
    - Biomass: weed biomass sampled in the month before harvest.
    - Seed Rain: seeds collected throughout the crop season.
    - Follow-up 1: vegetation survey one year after the trial crop.
    - Follow-up 2: vegetation survey two years after the trial crop.
  - Field edge vegetation
    - Margin Attributes: physical features around trial field edges.
    - Protocols for field boundary, margin, verge:
      - Edge Veg Cover: plant cover in June.
      - Edge Veg Flower: flowering from April–August.
      - Edge Veg Seed: seed setting in July–August.
      - Edge Bare Ground: percent bare ground.
      - Edge Spray Damage: vegetation damage from spraying.
  - Invertebrates
    - Bee and Butterfly transects: monthly counts April–August in crop and field margins.
    - Pollinators: combined Bee and Butterfly counts.
    - Crop Pests: herbivores on the crop early and late season.
    - Gastropod Search: gastropods in field margins.
    - Gastropod Trap: gastropods trapped in crop in spring and autumn.
    - Pitfall: counts of surface-active invertebrates early/mid/late season.
    - Vortis: arthropods on plants early/late season in verge and crop.
  - Additional tables
    - Date drilled, Herbicides applied, Height/Cover of weeds and crop.

- Table naming convention
  - All tables named and referenced as: abbreviatedprefix_crop_(sample date)_protocol
  - Examples: sum_b_seedrain (Beet crop summary for seedrain), sum_b_early_pitfall (Beet crop early-season pitfall summary).

- Generic table properties
  - Each row represents half-field totals (counts/biomass/mean percent cover) for a separate site.
  - Group totals and individual species contributing to groups are provided.
  - Sites are referenced within Defra Government regions; South-eastern and Eastern England regions are aggregated for confidentiality.
  - Null values indicate no verified data collected.
  - Some counts include decimals due to calculations across a proportion of transects.

- Specific table properties and column headings
  - Crop-pest tables include a suffix in the name of 'W +' or 'W-' to indicate winged vs wingless (where applicable).
  - Key column headings and meanings:
    - conv_count, conv_count_FL, conv_count_GE4TL, conv_count_L4TL, conv_count_SE: conventional crop counts (overall, flowering, ≥4 true-leaved, <4 true-leaved, seeding).
    - gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE: GMHT crop counts (analogous breakdowns).
    - crop_cover: percent cover of the crop.
    - crop_unit: C for conventional crop, GM for GM crop.
    - crop_height: crop height in centimetres.
    - name: species or group name (scientific or common British name).
    - site_ref: site reference number (consistent across all tables).
    - Region: Defra Government region or aggregate.
    - VEG/ARTHROPOD/GASTROPOD/BB_BRC: code for vegetation/arthropods/gastropods/bees & butterflies.
    - weed_cover_pc: percent cover of non-crop vegetation.
  - Notes: For additional information on spring crops and winter rape data, refer to the listed Royal Society and Proceedings of the Royal Society references.

- Data context, references, and guidance
  - The document provides prompts to consult the theme issue and peer-reviewed references for detailed methodology and interpretation:
    - The theme issue: The Farm Scale Evaluations of spring-sown GM crops (Phil. Trans. Royal Soc., 2003; 358(1439)).
    - Winter rape study: Effects on weed and invertebrate abundance and diversity of herbicide management in GMHT winter-sown oilseed rape (Proc. R. Soc. B, 2005).
  - Data organization supports cross-crop analyses, region-based aggregation, and creation of self-serve data products, with attention to data quality, missing values, and detailed protocol-specific measurements.