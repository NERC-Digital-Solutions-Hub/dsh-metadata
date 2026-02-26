# The Farm Scale Evaluations (FSE)

## Purpose and scope
- Set up to determine whether genetically-modified herbicide-tolerant (GMHT) crops might affect farmland wildlife via management practices.
- Data collected for four crops: Beet, Maize, Spring-sown oilseed rape, Winter-sown oilseed rape.
- Data categories cover multiple ecological facets across sites and time points.

## Dataset descriptions and data categories
- Seedbank
  - Seedbank counts of plant species germinating from soil samples taken before planting.
  - Follow-up samples taken one year and two years after the initial sample.
- Vegetation in the crop
  - Various surveys before and after herbicide application (e.g., First-seedling, Post-herbicide, Final Counts).
  - Special surveys (Beet Mezzanine, Winter Rape Mezzanine) at specific stages relative to herbicide timing.
  - Biomass sampling and Seed Rain data across the growing season.
  - Follow-up vegetation surveys conducted one and two years after trial.
- Field edge vegetation
  - Margin Attributes and Edge Veg measurements around field boundaries.
  - Metrics include cover, flowering, seed setting, bare ground, and spray-damage assessments.
- Invertebrates
  - Monthly transects for bees and butterflies within crops and margins.
  - Pollinators combined counts; Crop Pests, Gastropod surveys (in margins and crop), Pitfall traps, and Vortis counts in verge and crop.
- Additional tables
  - Crop-related dates (drilled), herbicide applications, and height/cover measurements for weeds and crops.
- Naming conventions
  - All tables follow a consistent naming scheme, e.g., sum_b_seedrain (Beet crop, seed rain), sum_b_early_pitfall (Beet crop, early pitfalls).
  - Table names encode crop, sample date, and protocol.

## Data structure and identifiers
- Each row represents half-field totals (counts, biomass, mean percent cover) for a single site.
- Both group totals and species-specific contributions are provided.
- Sites are tagged within Defra Government regions; South-eastern and Eastern England regions are aggregated for confidentiality.
- Nulls indicate no verified data were collected.
- Some counts are decimals because values were calculated using only a subset of transects.

## Column headings and data semantics
- Examples of column types:
  - conv_count, conv_count_FL, conv_count_GE4TL, conv_count_L4TL, conv_count_SE (conventional crop counts by category)
  - gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE (GMHT crop counts by category)
  - crop_cover, crop_unit, crop_height, name (species or group name)
  - site_ref, Region, VEG/ARTHROPOD/GASTROPOD/BB_BRC (coding for data type and provenance)
  - weed_cover_pc (percent cover of non-crop vegetation)
- Units and interpretation are defined within the dataset documentation; provides a consistent framework for cross-site comparisons.

## Data quality, provenance, and limitations
- Data are linked to specific crop trials and time points (e.g., pre-treatment, post-treatment, and follow-ups).
- Aggregation due to confidentiality limits regional granularity.
- Some data are missing (nulls) where verification did not occur.
- Decimals reflect calculations based on partial sampling; users should account for sampling intensity when analyzing. 
- References to published work provide provenance and context (e.g., Royal Society theme issue and related 2005 findings).

## Governance, storage, and sharing considerations for Data Stewards
- Standardized structure and naming conventions support discoverability, interoperability, and reuse.
- Documentation includes explicit table naming, column semantics, and region aggregation rules to maintain consistency across datasets and over time.
- Data stewardship needs:
  - Metadata compliance: ensure full definitions of variables, units, and protocols accompany the dataset.
  - Versioning and updates: follow-up data (Follow-up 1, Follow-up 2) should be appended with consistent schema.
  - Privacy and confidentiality: maintain aggregated regional reporting where necessary to protect farmer confidentiality; track which data require anonymization or aggregation.
  - Cross-platform compatibility: the standardized schema facilitates integration with other Defra datasets and reporting portals.
- Data should be stored with clear lineage to the four crop types and the various thematic data (seedbank, vegetation, margins, invertebrates, etc.) to support reproducibility and meta-analyses.

## Usage notes and references
- The dataset and its conventions are complemented by the literature:
  - The Farm Scale Evaluations of spring-sown GM crops (context and methodology) in Phil. Trans. Royal Soc. B (2003).
  - Effects on weed and invertebrate abundance and diversity in winter-sown oilseed rape (2005 Royal Society Proceedings B paper).

## Practical implications for dataset maintenance
- Ensure consistent site_ref mappings across crops and tables to support joined analyses.
- Maintain region aggregation metadata and any changes to confidentiality rules.
- Preserve the alignment between follow-up surveys and their respective time points for longitudinal analyses.
- Provide guidance for users on interpreting complex columns (e.g., species-level vs. group totals, W+ vs W- designations in pest tables).