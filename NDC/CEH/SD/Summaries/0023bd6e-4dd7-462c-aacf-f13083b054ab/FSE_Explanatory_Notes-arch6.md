# Explanatory notes

- The Farm Scale Evaluations (FSE) were set up to determine whether genetically-modified herbicide-tolerant (GMHT) crops might have any significant effects on farmland wildlife resulting from the way the crops would be managed.

## Datasets and crops

- Four crops studied: Beet, Maize, Spring-sown oilseed rape, and Winter-sown oilseed rape.
- Data categories collected across these crops:
  - Seedbank: counts of plant species germinating from soil samples before planting; Follow-up 1 (one year later); Follow-up 2 (two years later).
  - Vegetation in the crop: First-seedling (pre-herbicide); Beet Mezzanine (between herbicide applications on conventional vs. GM sides); Winter Rapemezzanine (spring, pre-herbicide); Post-herbicide; Final Counts; Biomass (weeds) measured before harvest; Seed Rain during the growing season; Follow-up 1 and Follow-up 2.
  - Field edge vegetation: Margin Attributes; Edge Veg Cover (June); Edge Veg Flower (April–August); Edge Veg Seed (July–August); Edge Bare Ground; Edge Spray Damage.
  - Invertebrates: Bee and Butterfly transects monthly (April–August) to produce Pollinators counts; Crop Pests; Gastropod Search (field margin) and Gastropod Trap (in crop, spring and autumn); Pitfall (surface-active invertebrates); Vortis (arthropods on plants, early and late season) in verge and crop.
  - Additional tables: Crop drilling date; Herbicides applied; Height/Cover of weeds and crop.

## Data collection protocols

- Data captured per protocol across crops, with standardized naming and timing as above.
- Data entries include counts, biomass, and percent cover where applicable.

## Table naming convention

- All tables use a consistent abbreviated prefix, crop, date, and protocol in the name, e.g. sum_b_seedrain (Beet crop, seedrain) or sum_b_early_pitfall (Beet crop, early season pitfalls).

## Generic table properties

- Each row represents half-field totals (counts, biomass, mean percent cover) for a separate site.
- Both group totals and individual species are included.
- Sites are referenced within Defra government regions; South-eastern and Eastern England regions are aggregated for confidentiality.
- Nulls appear where no verified data were collected.
- Some counts are shown with decimal places due to calculation across a proportion of transects.

## Specific table properties

- All crop_pest tables use a name suffix of 'W+' or 'W-' to indicate winged or wingless forms.

## Column headings and data fields

- Conventional crop counts:
  - conv_count
  - conv_count_FL (flowering)
  - conv_count_GE4TL (≥ 4 true-leaved)
  - conv_count_L4TL (< 4 true-leaved)
  - conv_count_SE (seeding)
- Crop metrics:
  - crop_cover (percent cover of crop)
  - crop_unit (C for conventional crop, GM for GM crop)
  - crop_height (crop height in cm)
- GMHT crop counts:
  - gm_count
  - gm_count_FL
  - gm_count_GE4TL
  - gm_count_L4TL
  - gm_count_SE
- Name and location fields:
  - name (species or group name)
  - site_ref (site reference number; consistent across all tables)
  - Region (Defra Government region or aggregate)
- Metadata codes:
  - VEG/ARTHROPOD/GASTROPOD/BB_BRC (Biological Records Centre codes)
  - weed_cover_pc (percent cover of non-crop vegetation)

## Data organization and metadata

- The dataset is designed for cross-site, multi-protocol analysis with region-based aggregation and consistent cross-referencing across crops.
- References and background information:
  - The spring crop theme issue: Phil. Trans. Royal Soc. B, 2003; 358(1439)
  - Winter rape study: Bohan et al., 2005, Proceedings of the Royal Society B, 272: 463-474

## Usage notes for data support

- The data structure supports creating self-serve analyses and dashboards to compare GMHT vs. conventional management, across crops and ecological indicators (seedbank, vegetation, invertebrates, edge habitat).
- When integrating datasets, account for regional aggregation and potential missing data (nulls) at sites or protocols.
- Data provenance and protocol documentation are essential to interpret species-level counts and agricultural timing (drilling dates, herbicide applications, sampling windows).