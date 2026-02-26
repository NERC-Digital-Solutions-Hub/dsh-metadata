# The Farm Scale Evaluations

- Purpose: Explanatory notes for datasets from the Farm Scale Evaluations (FSE) designed to determine whether genetically-modified herbicide-tolerant (GMHT) crops affect farmland wildlife under typical management.

## Datasets and scope

- Crops studied: Beet, Maize, Spring-sown oilseed rape, Winter-sown oilseed rape.
- Data domains and survey types:
  - Seedbank: initial soil sample; Seedbank Follow-up 1 (one year later); Seedbank Follow-up 2 (two years after initial).
  - Vegetation in the crop: First-seedling; Mezzanine surveys (Beet; Winter rape) around herbicide applications; Post-herbicide; Final Counts; Biomass; Seed Rain; Follow-ups 1 and 2.
  - Field edge vegetation: Margin Attributes; Edge Veg Cover; Edge Veg Flower; Edge Veg Seed; Edge Bare Ground; Edge Spray Damage.
  - Invertebrates: Bee and Butterfly transects (monthly Apr–Aug); Pollinators counts; Crop Pests; Gastropod Search; Gastropod Trap; Pitfall; Vortis.
  - Additional tables: Crop drilling date; Herbicide applications; Height/Cover of weeds and crop.
- Table naming convention: prefix_crop_(sample date)_protocol (e.g., sum_b_seedrain; sum_b_early_pitfall).
- Data structure per table: each row represents half-field totals for a single site; group totals and individual species are included; sites are linked to Defra regions.

## Data structure, keys, and standards

- Column headings and variables commonly used:
  - conv_count, conv_count_FL, conv_count_GE4TL, conv_count_L4TL, conv_count_SE (conventional crop counts at various plant stages)
  - gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE (GMHT crop counts)
  - crop_cover, crop_unit, crop_height
  - name (species or group name)
  - site_ref (site identifier shared across tables)
  - Region (Defra region or aggregated)
  - VEG/ARTHROPOD/GASTROPOD/BB_BRC codes for dataset domains
  - weed_cover_pc (percent cover of non-crop vegetation)
- Specific table property notes:
  - All crop_pest tables use suffixes W+ or W- to denote winged vs wingless individuals.
- Data quality notes:
  - Null values appear where data were not collected or verified.
  - Some counts have decimals due to partial transect computations.

## Data governance, metadata, and documentation

- Provenance and linkage:
  - Site_ref ensures cross-table traceability across vegetation, invertebrates, and other measurements.
  - Region aggregation applied to protect farmer confidentiality (South-eastern and Eastern England combined).
- Documentation and external references:
  - See related publications for methodological context (e.g., effects on weed and invertebrate abundance in GM crops; Spring and Winter rape studies).
- Metadata considerations:
  - Clear abbreviations, units, and protocol-specific details to support reuse and interoperability across datasets.

## Data sharing, updating, and maintenance

- Data should be uploaded to appropriate portals and cataloged with consistent naming to support discovery and reuse.
- Updates should preserve the original conventions (table naming, site_ref linkage) to maintain longitudinal consistency.
- Documentation should accompany data releases to explain protocols, timing, and measurement definitions.

## Particular challenges for stewardship

- Managing data across multiple domains (seedbank, vegetation, field margins, invertebrates) with consistent protocols.
- Ensuring completeness and timeliness of data collection across sites and crops.
- Balancing data richness with confidentiality constraints through regional aggregation.

## References and context

- Related methodological and results publications:
  - The Farm Scale Evaluations of spring-sown GM crops (Phil. Trans. R. Soc. B, 2003).
  - Effects on weed and invertebrate abundance and diversity of herbicide management in GM herbicide-tolerant winter-sown oilseed rape (Proc. R. Soc. B, 2005).