# Explanatory notes

## Overview
- Purpose: The Farm Scale Evaluations (FSE) were set up to determine if genetically-modified herbicide-tolerant (GMHT) crops have significant effects on farmland wildlife due to management practices.
- Datasets cover four crops: Beet, Maize, Spring-sown oilseed rape, and Winter-sown oilseed rape.
- Data collected across multiple domains: Seedbank, Vegetation in the crop, Field edge vegetation, Invertebrates, and Additional tables (date drilled, herbicides applied, height/cover).

## Dataset Descriptions and Structure
- Seedbank
  - Collects counts of plant species germinating from pre-plant soil samples.
  - Follow-up samples taken 1 year and 2 years after the initial seedbank sample.
- Vegetation in the crop
  - First-seedling survey before herbicide applications.
  - Beet includes an additional Mezzanine survey; Winter rape has a spring Mezzanine survey.
  - Post-herbicide survey after herbicide applications on both conventional and GM sides.
  - Final Counts survey coincides with biomass sampling; Seed Rain tracks seeds produced during the season.
  - Follow-ups 1 and 2 occur one and two years after the trial crop.
- Field edge vegetation
  - Margin Attributes describe physical features around the trial field edge.
  - Protocols record Edge Veg Cover (June), Edge Veg Flower (April–August), Edge Veg Seed (July–August), Edge Bare Ground, and Edge Spray Damage.
- Invertebrates
  - Bee and Butterfly transects monthly (April–August) in crop and field margins.
  - Pollinators combines Bee and Butterfly counts.
  - Crop Pests, Gastropod Search (field margin), Gastropod Trap (crop), Pitfall (surface-active invertebrates), and Vortis (arthropods on plants) with season timing.
- Additional tables
  - Data on drilling date, herbicides applied, and height/cover of weeds and crop.
- Table naming convention
  - sum_<prefix>_<crop>_(sample date)_protocol (examples: sum_b_seedrain for Beet seedrain; sum_b_early_pitfall for Beet early pitfall).

## Data Properties and Metadata
- Generic table properties
  - Each row represents half-field totals (counts/biomass/mean percent cover) for a separate site.
  - Both group totals and individual species totals are included.
  - Sites are referenced within Defra Government regions; South-eastern and Eastern England regions are aggregated for confidentiality.
  - Nulls indicate missing verified data.
  - Some counts have decimals due to calculations from only a proportion of transects.
- Specific table properties
  - For crop_pest tables, the name suffix uses 'W +' or 'W-' to denote winged or wingless forms.
- Column headings (examples)
  - conv_count, conv_count_FL, conv_count_GE4TL, conv_count_L4TL, conv_count_SE
  - crop_cover, crop_unit (C for conventional crop, GM for GM crop), crop_height
  - gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE
  - name (species or group name), site_ref, Region
  - VEG/ARTHROPOD/GASTROPOD/BB_BRC (codes for data type)
  - weed_cover_pc (percent cover of non-crop vegetation)

## Data Governance, Standards and Access
- Regional attribution and aggregation
  - Sites are linked to Defra regions, with some regional aggregation for confidentiality.
- Documentation and provenance
  - Explanatory notes describe the structure, protocols, and conventions used throughout the dataset.
  - References to related publications for further methodological context (e.g., Royal Society Proceedings 2005; Phil. Trans. R. Soc. B 2003/2005).
- Updates and reuse
  - Data is organized to support reuse and comparison across crops and measurement domains, with clear naming conventions to aid discovery.
- Considerations for Data Stewards
  - Ensure consistent adherence to the naming conventions (table names, sample dates, protocol suffixes).
  - Maintain alignment between site_ref and regional classifications; preserve aggregation decisions in metadata.
  - Manage potential gaps or missing data indicated by nulls; document reasons (e.g., non-collection, confidentiality).
  - Prepare for data uploads to relevant portals and for re-use in multidisciplinary analyses (ecology, agronomy, biodiversity).

## Challenges and Implications for Stewardship
- Complex, multi-protocol datasets across multiple crops and years require rigorous metadata and consistent data validation.
- Large, high-dimensional data with many tables and derived metrics necessitates clear lineage and version control.
- Interoperability across systems and formats is needed to enable external discovery and reuse, given regional aggregation and confidentiality constraints.