# Farm Scale Evaluations

- The Farm Scale Evaluations (FSE) were set up to determine whether genetically-modified herbicide-tolerant (GMHT) crops might have any significant effects on farmland wildlife resulting from the way the crops would be managed.

## Datasets and Crops

- Crops studied: Beet, Maize, Spring-sown Oilseed Rape, Winter-sown Oilseed Rape.
- Data categories:
  - Seedbank: initial soil seedbank counts, followed by Seedbank Follow-up 1 (one year later) and Seedbank Follow-up 2 (two years after initial).
  - Vegetation in the crop: includes First-seedling, Mezzanine surveys (Beet and Winter Rape), Post-herbicide, Final Counts, Biomass, Seed Rain, and Follow-ups 1 and 2.
  - Field edge vegetation: Margin Attributes with Edge Veg Cover, Edge Veg Flower, Edge Veg Seed, Edge Bare Ground, Edge Spray Damage.
  - Invertebrates: Bee and Butterfly transects (Pollinators), Crop Pests, Gastropod searches and traps, Pitfall, Vortis sampling in verge and crop.
  - Additional tables: crop drill dates, herbicide applications, and height/cover measurements of weeds and crops.
- Data are organized by site within Defra regions, with some regional aggregation for confidentiality (South-eastern and Eastern England).

## Data Structure and Naming

- Table naming convention: abbreviatedprefix_crop_(sample date)_protocol, e.g., sum_b_seedrain (Beet crop, seedrain), sum_b_early_pitfall (Beet crop, early pitfall).
- Generic properties:
  - Each row represents half-field totals (counts/biomass/mean percent cover) for a separate site.
  - Includes both group totals and contributing species.
  - Sites are referenced within Defra regions; confidentiality leads to regional aggregation in some cases.
  - Nulls appear where no verified data were collected.
  - Some counts are decimal due to partial transect calculations.
- Specific table properties (crop_pest tables):
  - Name suffix indicates winged ('W+') or wingless ('W-') pests.

## Columns and Measurements

- Examples of column headings:
  - conv_count, conv_count_FL, conv_count_GE4TL, conv_count_L4TL, conv_count_SE (conventional crop counts and subsets)
  - gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE (GMHT crop counts and subsets)
  - crop_cover, crop_unit, crop_height
  - name (species or group name), site_ref (site reference), Region (Defra region)
  - VEG/ARTHROPOD/GASTROPOD/BB_BRC (coded group identifiers), weed_cover_pc (non-crop vegetation cover)
- Purpose of columns: quantify weed and crop characteristics, plant abundance, and invertebrate indicators across conventional and GMHT crops.

## Temporal and Spatial Context

- Data cover multiple timepoints within a growing season (e.g., seedbank samples, first-seedling, post-herbicide, final vegetation surveys) and follow-ups years after the trial.
- Sites are geographically organized by Defra government regions, with some regional aggregation for confidentiality.

## Data Quality, Gaps, and Access

- Null values indicate missing or unverified data.
- Some decimal values arise from calculating counts using a subset of transects.
- The dataset provides detailed protocol-based observations intended to support analyses of weed and invertebrate abundance and diversity under different herbicide management strategies.

## References and Further Information

- For spring crops: The Farm Scale Evaluations of spring-sown genetically modified crops (Philosophical Transactions of the Royal Society B, 2003; 358, 1439).
- For winter rape: Effects on weed and invertebrate abundance and diversity of herbicide management in GMHT winter-sown oilseed rape (Proceedings of the Royal Society B, 2005).

## Implications for Data Leaders

- Data scope demonstrates end-to-end data lifecycle: collection protocols, site-level aggregation, and longitudinal follow-ups across multiple crop types.
- Highlights importance of:
  - Comprehensive metadata and standardized naming conventions to ensure discoverability and reuse.
  - Clear documentation of data structure (generic vs. specific table properties) and column definitions.
  - Handling of confidentiality-driven regional aggregation while preserving analytical value.
  - Transparent treatment of missing data and decimal representations arising from partial transects.
- Potential data governance actions:
  - Establishing a data catalog entry with the described naming conventions and column schemas.
  - Implementing data quality checks to flag missing or inconsistent entries across timepoints.
  - Mapping related datasets (seedbank, vegetation, invertebrates, margins) to a unified data model for cross-domain analyses.
  - Ensuring provenance and references to external publications (e.g., Phil. Trans. R. Soc. B. 2003; 2005) are linked for contextual interpretation.