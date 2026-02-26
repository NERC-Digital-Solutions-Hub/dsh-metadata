# Explanatory notes

## Objective and scope
- Farm Scale Evaluations (FSE) set up to determine whether genetically-modified herbicide-tolerant (GMHT) crops might have significant effects on farmland wildlife due to management practices.

## Datasets and crops covered
- Four crops: Beet, Maize, Spring-sown oilseed rape, Winter-sown oilseed rape.
- Data collected across multiple domains and time points to capture ecological responses and management influences.

## Data collection domains and protocols
- Seedbank
  - Seedbank: counts of germinating plant species from a pre-plant soil sample.
  - Seedbank Follow-ups: Follow-up 1 (one year after initial), Follow-up 2 (two years after initial).
- Vegetation in the crop
  - First-seedling: first vegetation survey before herbicide.
  - Mezzanine: Beet has an additional survey between herbicide applications on conventional vs GM sides; Winter rape has a spring pre-herbicide survey.
  - Post-herbicide: vegetation surveyed after herbicide on both sides.
  - Final Counts: vegetation survey concurrent with biomass sampling prior to harvest.
  - Seed rain: collection of seeds produced during the growing season.
  - Follow-ups: Follow-up 1 (one year after), Follow-up 2 (two years after).
- Field edge vegetation
  - Margin Attributes: physical features around field boundary.
  - Edge Veg Cover: plant cover in June.
  - Edge Veg Flower: flowering from April to August.
  - Edge Veg Seed: seed setting in July and August.
  - Edge Bare Ground: percent bare ground.
  - Edge Spray Damage: vegetation damage due to spraying.
- Invertebrates
  - Bee and Butterfly transects: monthly counts April–August in crop and margins; Pollinators combines bees and butterflies.
  - Crop Pests: herbivores on the crop early and late in the season.
  - Gastropod Search: gastropods in field margins.
  - Gastropod Trap: gastropods trapped in the crop (spring and autumn).
  - Pitfall: surface-active invertebrates captured early, mid, late in season.
  - Vortis: arthropods on plants in field verge and crop (early and late).
- Additional tables
  - Date crops were drilled.
  - Herbicides applied.
  - Height/Cover of weeds and crops.

## Data structure, naming, and conventions
- Table naming convention
  - Always in the form: abbreviatedprefix_crop_(sample date)_protocol
  - Examples: sum_b_seedrain (Beet crop, seed rain); sum_b_early_pitfall (Beet crop, early pitfall).
- Generic table properties
  - Each row represents half-field totals (counts/biomass/mean percent cover) for a separate site.
  - Group totals and individual species contributing to groups are provided.
  - Sites are referenced within Defra Government regions; South-eastern and Eastern England regions are aggregated for confidentiality.
  - Nulls appear where no verified data were collected.
  - Some counts include decimals, calculated from a subset of transects.
- Specific table properties
  - For crop_pest tables, the suffix 'W +' or 'W-' indicates winged or wingless forms.
- Column headings (examples)
  - conv_count, conv_count_FL, conv_count_GE4TL, conv_count_L4TL, conv_count_SE
  - crop_cover, crop_unit, crop_height
  - gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE
  - name (species or group name)
  - site_ref (site identifier)
  - Region (Defra government region or aggregation)
  - VEG/ARTHROPOD/GASTROPOD/BB_BRC (codes for data type)
  - weed_cover_pc (percent cover of non-crop vegetation)

## Data governance and metadata notes
- Regions: Sites are tied to Defra regions; for confidentiality, some regional data are aggregated.
- Metadata and documentation accompany the dataset, including table naming conventions and lot-specific definitions.
- Data are used to assess effects on weed and invertebrate abundance/diversity in relation to GMHT herbicide management.

## References and further information
- The spring-crop theme issue: The Farm Scale Evaluations of spring-sown genetically modified crops, Phil. Trans. Royal Soc. B, 358 (2003).
- Winter rape study: Effects on weed and invertebrate abundance and diversity of herbicide management in GMHT winter-sown oilseed rape, Proc. R. Soc. B, 272:463-474 (2005).