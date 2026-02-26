# Farm Scale Evaluations (FSE) dataset descriptions

## Overview
- Datasets from the Farm Scale Evaluations (FSE) study, designed to assess potential effects of genetically-modified herbicide-tolerant (GMHT) crops on farmland wildlife through field-based management practices.
- Data collected across four crops: Beet, Maize, Spring-sown oilseed rape, and Winter-sown oilseed rape.
- Focuses on a wide range of spatially-referenced measurements at the field/site level, suitable for map-based analysis and visualization in GIS.

## Datasets and data structure
- Seedbank
  - Seed germination counts from soil samples taken before planting; follow-up samples at 1 and 2 years after the initial seedbank sample.
- Vegetation in the crop
  - First-seedling surveys (pre-herbicide).
  - Beet Mezzanine (between herbicide applications on conventional vs GM sides).
  - Winter Rape Mezzanine (spring, pre-herbicide).
  - Post-herbicide surveys (after herbicide on both sides).
  - Final Counts (same time as biomass sampling).
  - Biomass of weeds (one month before harvest).
  - Seed Rain (seasonal seed production).
  - Follow-up 1 (one year after), Follow-up 2 (two years after).
- Field edge vegetation
  - Margin Attributes around field edges; boundary, margin, verge protocols.
  - Edge Veg Cover (percent cover, June).
  - Edge Veg Flower (flowering April–August).
  - Edge Veg Seed (seed setting in July–August).
  - Edge Bare Ground (percent bare ground).
  - Edge Spray Damage (vegetation damage from spraying).
- Invertebrates
  - Bee and Butterfly transects (monthly, April–August).
  - Pollinators (combined Bee & Butterfly counts).
  - Crop Pests (herbivores on crop, early and late season).
  - Gastropod Search (gastropods in field margins).
  - Gastropod Trap (gastropods trapped in crop, spring and autumn).
  - Pitfall (surface-active invertebrates, early/mid/late season).
  - Vortis (arthropods on plants, early/late season; in verge and crop).
- Additional tables
  - Dates crops were drilled; herbicides applied; height/cover of weeds and crops.
- Table naming
  - Format: abbreviatedprefix_crop_(sample date)_protocol (e.g., sum_b_seedrain for Beet crop seedrain; sum_b_early_pitfall for Beet crop early pitfall).

## Spatial and temporal aspects
- Each row represents half-field totals for a separate site; sites are tied to Defra Government regions (regional aggregation exists for Southeastern and Eastern England).
- Temporal dimensions include pre- and post-management timings, herbicide applications, and multi-year follow-ups (up to two years after initial sampling).

## Data organization and labeling
- Generic table properties
  - Group totals and species-level contributions are provided.
  - Nulls appear where data were not collected.
  - Some counts are decimal due to partial transect calculations.
- Specific table properties
  - crop_pest tables use a suffix of 'W +' or 'W-' to denote winged vs wingless forms.
- Column headings (examples)
  - conv_count, conv_count_FL, conv_count_GE4TL, conv_count_L4TL, conv_count_SE
  - crop_cover, crop_unit, crop_height
  - gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE
  - name (species or group name), site_ref, Region
  - VEG/ARTHROPOD/GASTROPOD/BB_BRC (coding codes)
  - weed_cover_pc (percent non-crop vegetation cover)

## Data quality, standards, and limitations
- Data sourced from multiple protocols across crops and study years; potential variation in collection methods and resolutions.
- Southeastern and Eastern England regional data are aggregated for confidentiality.
- Nulls indicate missing or unverified data; decimal values reflect partial transect calculations.
- Users should anticipate the need for cleaning and transformation when combining datasets from different crops or survey periods.

## How GIS specialists can use this data
- Build multi-layer maps by linking datasets through site_ref and regional codes; create per-site spatial features (fields, field edges, and margins) and time-series layers.
- Visualize spatial patterns in seedbank, vegetation cover, edge habitat, and invertebrate activity across crops and years.
- Integrate with other DEFRA or environmental datasets using the Defra regions and site references to compare wildlife responses under GMHT vs conventional management.
- Derive indicators such as:
  - Species richness and abundance per site per survey
  - Vegetation cover and flowering dynamics over time
  - Edge habitat quality and spray damage distribution
  - Pollinator presence across crop margins and fields
- Use the dataset naming conventions to systematically organize GIS project files and metadata, ensuring traceability across crops and sampling dates.
- Consider data confidentiality constraints by respecting regional aggregations during visualization and publication.

## References and further information
- For spring crop details: Theoretical theme issue on The Farm Scale Evaluations of spring-sown GM crops, Philosophical Transactions of the Royal Society B (2003/2005 references).
- For winter rape: Effects on weed and invertebrate abundance and diversity related to herbicide management in GMHT winter-sown oilseed rape; Proceedings of the Royal Society B (2005).