# Explanatory notes

- The Farm Scale Evaluations (FSE) were set up to determine whether genetically-modified herbicide-tolerant (GMHT) crops might have any significant effects on farmland wildlife resulting from the way the crops would be managed.

## Dataset scope and crops

- Four crops studied: Beet, Maize, Spring-sown oilseed rape, Winter-sown oilseed rape.
- Data collected across multiple trial areas with standardized protocols.

## Data categories and timing

- Seedbank: counts of plant species germinating from soil samples taken before planting; includes follow-up samples at 1 year and 2 years.
- Vegetation in the crop: surveys at multiple stages, including first-seedling, post-herbicide, biomass/weeds, seed rain, and follow-ups at 1 and 2 years.
- Field edge vegetation: measurements around field boundaries and margins, including edge vegetation cover, flowering, seed setting, bare ground, and spray damage.
- Invertebrates: monthly transects (April–August) for Bees & Butterflies (Pollinators), crop pests, gastropods, pitfall traps, and Vortis plant-sample arthropods in verge and crop.
- Additional tables: crop drill dates, herbicide applications, weed/crop height and cover data.

## Data organization and naming conventions

- Table naming convention: [abbreviatedprefix]_[crop]_[sample date]_protocol (e.g., sum_b_seedrain, sum_b_early_pitfall).
- Generic table properties:
  - Each row represents half-field totals for a separate site.
  - Group totals and species-level contributions are included.
  - Sites referenced within Defra government regions; South-eastern and Eastern England regions aggregated for confidentiality.
  - Nulls indicate missing verified data.
  - Some counts/values may be decimal due to partial transect calculations.
- Specific table properties:
  - All crop_pest tables include a name suffix indicating winged (‘W’) or wingless (‘-’).

## Column headings and data semantics

- Key columns include:
  - conv_count, conv_count_FL, conv_count_GE4TL, conv_count_L4TL, conv_count_SE: conventional crop counts for different plant states.
  - gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE: GMHT crop counts for corresponding states.
  - crop_cover, crop_unit, crop_height: percent cover, crop type (C or GM), and crop height in cm.
  - name: species or group name (scientific or common UK name).
  - region, site_ref: site and Defra region identifiers; site_ref consistent across all related tables.
  - weed_cover_pc: percent cover of non-crop vegetation.
- Data semantics:
  - “Site” references are consistent across all related tables (e.g., Beet_Bees and Maize_Gastropod_Search share site numbering).
  - Regions may be aggregated for confidentiality.
  - Some data are aggregated totals (half-field totals) rather than per-plant counts.

## Spatial and geographic considerations

- Sites are associated with Defra government regions, with cross-table linking via site_ref.
- Field-scale features tracked include field margins, verges, and field edges, enabling spatial analyses of edge effects and habitat features.
- Data support map-based visualization of species abundance and habitat characteristics around trial fields and margins.

## Data quality, limitations, and provenance

- Data may be incomplete in some cells (nulls) where no verified data were collected.
- Decimal values indicate calculations based on subsets of transects, requiring careful interpretation in spatial analyses.
- Some region-level data are aggregated to protect farmer confidentiality.

## Usage notes for GIS applications

- Suitable for creating map layers of:
  - Seedbank and vegetation patterns by crop and time period.
  - Edge and margin vegetation attributes around trial fields.
  - Invertebrate and gastropod distribution in crops and margins.
  - Temporal change layers based on follow-up surveys (1-year and 2-year follow-ups).
- Requires careful join via site_ref and region to combine tables (and respect confidentiality aggregations).
- Data can support analyses of GMHT vs conventional management effects on wildlife indicators and habitat features.

## Additional references

- For spring crops: The Farm Scale Evaluations of spring-sown genetically modified crops (Phil. Trans. Royal Soc., 2003).
- For winter rape: Effects on weed and invertebrate abundance and diversity of herbicide management in GM winter-sown oilseed rape (Proceedings of the Royal Society B, 2005).