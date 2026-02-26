# Explanatory notes

- The Farm Scale Evaluations (FSE) were set up to determine whether genetically-modified herbicide-tolerant (GMHT) crops might have any significant effects on farmland wildlife resulting from the way the crops would be managed.

## Dataset scope and crops

- Data collected for four crops: Beet, Maize, Spring-sown oilseed rape, and Winter-sown oilseed rape.

## Data collection domains

- Seedbank
  - Seedbank: counted plant species germinating from a soil sample taken before planting.
  - Seedbank Follow-up 1: repeat soil sample one year after the initial seedbank sample.
  - Seedbank Follow-up 2: final soil sample two years after the initial sample.

- Vegetation in the crop
  - First-seedling: first vegetation survey before herbicide.
  - Mezzanine (Beet): additional vegetation survey between herbicide applications on conventional and GM sides.
  - Winter Rape Mezzanine: vegetation survey in spring before any herbicide.
  - Post-herbicide: vegetation survey after herbicide on both conventional and GM sides.
  - Final Counts: vegetation survey concurrent with biomass sampling before harvest.
  - Biomass: weed biomass sampled in the month before harvest.
  - Seed Rain: seeds collected throughout the growing season.
  - Follow-up 1: vegetation survey one year after the trial.
  - Follow-up 2: vegetation survey two years after the trial.

- Field edge vegetation
  - Margin Attributes: physical features around the field edge.
  - Edge Veg Cover: percent cover of plant species in June.
  - Edge Veg Flower: plant flowering from April to August.
  - Edge Veg Seed: seed setting in July and August.
  - Edge Bare Ground: percent bare ground.
  - Edge Spray Damage: vegetation damage from spraying.

- Invertebrates
  - Bee and Butterfly transects: monthly counts in crop and field margins (April–August).
  - Pollinators: combined Bee and Butterfly counts.
  - Crop Pests: counts of herbivores on the crop early and late in the season.
  - Gastropod Search: gastropods in the field margin.
  - Gastropod Trap: gastropods trapped in the crop (spring and autumn).
  - Pitfall: counts of surface-active invertebrates (early, mid, late).
  - Vortis: arthropods on plants (early and late) in field verge and crop.

- Additional tables
  - Date drilled; Herbicides applied; Height/Cover of weeds and crops.

## Table naming convention

- All tables are named and referenced using the format: abbreviatedprefix_crop_(sample date)_protocol
  - Examples: sum_b_seedrain (Beet crop, seed rain), sum_b_early_pitfall (Beet crop, early pitfall).

## Generic table properties

- Each row represents half-field totals (counts/biomass/mean percent cover) for a separate individual site.
- Group totals are provided alongside individual species totals.
- Sites are referenced within Defra government regions; South-eastern and Eastern England regions are aggregated for confidentiality.
- Nulls appear where no verified data were collected.
- Some counts are shown with decimal places; values may be calculated using only a proportion of the transects.

## Specific table properties

- All crop_pest tables have a name suffix of 'W +' or 'W-' to indicate winged or wingless forms.

## Column headings (key fields)

- conv_count, conv_count_FL, conv_count_GE4TL, conv_count_L4TL, conv_count_SE
  - Conventional crop counts at various life-stage or threshold levels.
- crop_cover, crop_unit, crop_height
  - Percent cover of the crop, crop unit (C = conventional crop, GM = GM crop), height in centimetres.
- gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE
  - GMHT crop counts at corresponding life-stages or thresholds.
- name
  - Species or group name (scientific or common British name).
- site_ref
  - Site reference number (consistent across all tables; same site across crops).
- Region
  - Defra Government region or aggregate region.
- VEG/ARTHROPOD/GASTROPOD/BB_BRC
  - Codes for vegetation, arthropods, gastropods, or Bees & Butterflies (Biological Records Centre codes).
- weed_cover_pc
  - Percent cover of non-crop vegetation.

## Data quality, provenance, and references

- Documentation provides guidance for broader context and methods.
- For further information on spring crops: Phil. Trans. Royal Soc., 2003 theme issue.
- For further information on winter rape: Bohan et al. (2005) on effects of GM herbicide management.