# Explanatory notes

- Purpose of Farm Scale Evaluations (FSE)
  - Set up to determine whether genetically-modified herbicide-tolerant (GMHT) crops might have significant effects on farmland wildlife through crop management.

- Datasets and crops studied
  - Four crops: Beet, Maize, Spring-sown Oilseed Rape, Winter-sown Oilseed Rape.
  - Data categories:
    - Seedbank
      - Seedbank: seed germination from soil before planting.
      - Seedbank Follow-up 1: repeat soil sample one year after initial.
      - Seedbank Follow-up 2: final soil sample two years after initial.
    - Vegetation in the crop
      - First-seedling: first vegetation survey before herbicide.
      - Beet Mezzanine: vegetation survey between herbicide applications on conventional vs GM sides.
      - Winter Rape Mezzanine: spring survey before any herbicide.
      - Post-herbicide: vegetation survey after herbicide on both conventional and GM sides.
      - Final Counts: vegetation survey concurrent with biomass sampling.
      - Biomass: weed biomass sampled month before harvest.
      - Seed Rain: seeds collected throughout the growing season.
      - Follow-up 1/2: vegetation surveys one and two years after the trial crop.
    - Field edge vegetation
      - Margin Attributes (physical features around field edge).
      - Protocols recording field boundary, margin, verge data:
        - Edge Veg Cover: percent cover of plant species (June).
        - Edge Veg Flower: flowering (April–August).
        - Edge Veg Seed: seed setting (July–August).
        - Edge Bare Ground: percent bare ground.
        - Edge Spray Damage: vegetation damage from spraying.
    - Invertebrates
      - Bee and Butterfly transects: monthly (April–August) in crop and margins.
      - Pollinators: combined Bee and Butterfly counts.
      - Crop Pests: herbivores on crop (early and late season).
      - Gastropod Search: gastropods in field margin.
      - Gastropod Trap: gastropods trapped in crop (spring and autumn).
      - Pitfall: surface-active invertebrates (early, mid, late).
      - Vortis: arthropods on plants (early and late) in verge and crop.
    - Additional tables
      - Date drilled; Herbicides applied; Height/Cover of weeds and crop.

- Table naming conventions
  - Format: abbreviatedprefix_crop_(sample date)_protocol
  - Examples: sum_b_seedrain (Beet seed rain), sum_b_early_pitfall (Beet early pitfall).

- Generic table properties
  - Each row represents half-field totals for a separate site.
  - Group totals plus contributing species data are provided.
  - Sites are referenced within Defra Government regions; some regions aggregated for confidentiality.
  - Nulls indicate no verified data.
  - Some counts shown with decimals due to partial transects.

- Specific table properties
  - All crop_pest tables use a name suffix of 'W +' or 'W-' to denote winged vs wingless forms.

- Column headings and data fields (typical examples)
  - conv_count, conv_count_FL, conv_count_GE4TL, conv_count_L4TL, conv_count_SE (conventional crop counts by category)
  - crop_cover (C) and crop_unit (C or GM)
  - crop_height (cm)
  - gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE (GMHT crop counts by category)
  - name (species or group name)
  - site_ref (site identifier consistent across tables)
  - Region (Defra government region or aggregate)
  - VEG/ARTHROPOD/GASTROPOD/BB_BRC (codes for data type)
  - weed_cover_pc (percent cover of non-crop vegetation)

- References and additional notes
  - Background on spring crops: The Farm Scale Evaluations of spring-sown GM crops (Philosophical Transactions of the Royal Society, 2003).
  - Winter rape-specific study: Effects on weed and invertebrate abundance and diversity (Proceedings of the Royal Society B, 2005).