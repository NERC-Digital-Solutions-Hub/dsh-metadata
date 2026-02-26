# Explanatory notes

- The Farm Scale Evaluations (FSE) were established to determine whether genetically-modified herbicide-tolerant (GMHT) crops might have significant effects on farmland wildlife due to management practices.

## Datasets and crop coverage

- Crops studied: Beet, Maize, Spring-sown oilseed rape, Winter-sown oilseed rape.
- Data collection domains:
  - Seedbank: initial soil sample, plus Seedbank Follow-up 1 (one year later) and Seedbank Follow-up 2 (two years after initial).
  - Vegetation in the crop: First-seedling survey; Mezzanine surveys (Beet and Winter rape) around herbicide timing; Post-herbicide survey; Final Counts (coinciding with biomass sampling); Biomass of weeds; Seed Rain during the growing season; Follow-up vegetation surveys at 1 and 2 years.
  - Field edge vegetation: Margin Attributes; Edge Veg Cover (June); Edge Veg Flower (April–August); Edge Veg Seed (July–August); Edge Bare Ground; Edge Spray Damage.
  - Invertebrates: Bee and Butterfly transects (monthly April–August); Pollinators (combined Bee & Butterfly counts); Crop Pests; Gastropod Search (in field margin) and Gastropod Trap (in crop); Pitfall traps (early, mid, late); Vortis (arthropods on plants) in verge and crop.
  - Additional tables: Dates crops were drilled; Herbicides applied; Height/Cover of weeds and crop.
- Data organization principle:
  - Each row represents half-field totals (counts/biomass/mean percent cover) for a separate site.
  - Both group totals and species-level contributions are included.
  - Sites are referenced within Defra Government regions (with South-eastern and Eastern England regions aggregated for confidentiality).
  - Nulls appear where no verified data were collected; some counts are decimals from partial transects.

## Table naming conventions

- Tables are named and referenced using the convention: prefix_crop_(sample date)_protocol, e.g., sum_b_seedrain (Beet crop seed rain) or sum_b_early_pitfall (Beet crop early-season pitfall).

## Generic table properties

- Each row: half-field totals for a specific site.
- Groups and individual species are represented.
- Sites are mapped to Defra regions.
- Null values indicate missing verified data.
- Decimal values can arise from averaging across only a subset of transects.

## Specific table properties

- All crop_pest tables use a suffix to indicate winged ('W+') or wingless ('W-') status.

## Column headings and data fields

- Examples of columns:
  - conv_count, conv_count_FL, conv_count_GE4TL, conv_count_L4TL, conv_count_SE
  - crop_cover (percent cover of crop)
  - crop_unit (C = conventional crop, GM = GM crop)
  - crop_height (crop height in cm)
  - gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE
  - name (species or group name)
  - site_ref (site reference number, consistent across tables)
  - Region (Defra Government region or aggregate)
- Vegetation, arthropod, gastropod, and other data are coded with DEFRA Biological Records Centre (VEG/ARTHROPOD/GASTROPOD/BB_BRC) aliases.
- Additional fields include weed_cover_pc (percent cover of non-crop vegetation).

## Context and references

- For further information on the spring crops: The theme issue The Farm Scale Evaluations of spring-sown genetically modified crops, Philosophical Transactions of the Royal Society B, 2003.
- For winter rape: Related study by Bohan et al. (2005) on effects of herbicide management on weed and invertebrate abundance and diversity in GMHT winter-sown oilseed rape, Proceedings of the Royal Society B.