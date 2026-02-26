# Dataset Descriptions

- The Farm Scale Evaluations (FSE) were set up to determine whether genetically-modified herbicide-tolerant (GMHT) crops might have significant effects on farmland wildlife resulting from how the crops are managed.

## What was collected and where

- Four crops studied: Beet, Maize, Spring-sown oilseed rape, Winter-sown oilseed rape.
- Data collected across multiple data domains:
  - Seedbank: soil samples to count germinating plant species before planting; follow-up samples at 1 year and 2 years after.
  - Vegetation in the crop: multiple surveys including First-seedling (before herbicide), Mezzanine (Beet only), Winter rape Mezzanine (spring, pre-herbicide), Post-herbicide (after application on both conventional and GM sides), Final Counts (crop vegetation when biomass sampled), Biomass (weed biomass before harvest), Seed Rain (seed production during the growing season), Follow-up 1 (1 year after), Follow-up 2 (2 years after).
  - Field edge vegetation: Margin Attributes with measurements around field boundaries; data collected for Edge Veg Cover, Edge Veg Flower (April–August), Edge Veg Seed (July–August), Edge Bare Ground, Edge Spray Damage.
  - Invertebrates: Bee and Butterfly transects monthly (April–August); Pollinators (combined bee & butterfly counts); Crop Pests; Gastropod Surveys (Search and Trap); Pitfall (surface-active invertebrates); Vortis (arthropods on plants in verge and crop).
  - Additional tables: Crop drilling dates; Herbicides applied; Height/Cover of weeds and crop.

## Data naming and structure

- Table naming convention: abbreviatedprefix_crop_(sample date)_protocol (e.g., sum_b_seedrain for Beet seedrain; sum_b_early_pitfall for Beet early-season pitfall).
- Each row represents half-field totals (counts, biomass, or mean percent cover) for a separate site.
- Data are organized by Defra government region; South-eastern and Eastern England regions are aggregated.
- Null values denote no verified data; some counts are decimal because they reflect data from only a proportion of transects.

## Table and column properties

- Generic table properties:
  - Rows cover half-field totals per site; both group totals and individual species are included.
  - Sites are referenced within Defra regions; regional aggregation applies to some regions for confidentiality.
  - Nulls indicate missing/absent data; decimals result from partial transects.
- Specific table properties:
  - Crop pest tables include a suffix indicating winged (W+) or wingless (W−) forms.
- Column headings commonly include:
  - conv_count, conv_count_FL, conv_count_GE4TL, conv_count_L4TL, conv_count_SE (conventional crop counts by life-stage or trait).
  - crop_cover (percent cover of the crop), crop_unit (C = conventional crop, GM = GM crop).
  - crop_height (crop height in cm).
  - gm_count, gm_count_FL, gm_count_GE4TL, gm_count_L4TL, gm_count_SE (GMHT crop counts by category).
  - name (scientific or common name of species or group).
  - site_ref (site reference number, consistent across tables).
  - Region (Defra government region).
  - VEG/ARTHROPOD/GASTROPOD/BB_BRC codes (coding for data type/classification).
  - weed_cover_pc (percent cover of non-crop vegetation).

## Provenance and external references

- For spring crops: describes broader context in The Farm Scale Evaluations of spring-sown GM crops (Phil. Trans. Royal Soc., 2003; 358(1439)).
- For winter oilseed rape: Effects on weed and invertebrate abundance and diversity of herbicide management in GM herbicide-tolerant winter-sown oilseed rape (Proceedings of the Royal Society B, 2005).

## Data governance, quality and access considerations

- Data are aggregated to protect farmer confidentiality (regions aggregation in certain cases).
- Data quality considerations noted via nulls and decimal values resulting from sampling methods (partial transects).
- The dataset emphasizes standardization of table and column naming to facilitate cross-site and cross-crop analyses.
- Metadata and lineage are important for enabling users to understand timing (years after planting, before/after herbicide), sampling methods, and definitions of terms across crop types.

## Implications for Data Leaders

- View as a multi-domain data asset with temporal, spatial, and taxonomic dimensions that require careful metadata governance.
- Key opportunities:
  - Integrate across crop types to assess GMHT vs conventional management effects on wildlife.
  - Link seedbank, vegetation, edge habitat, and invertebrate data for ecosystem-level analyses.
  - Leverage standard naming conventions and region-based aggregation to support discoverability and reuse.
- Data governance considerations:
  - Maintain clear provenance, sampling timelines, and method definitions to ensure comparability over time.
  - Manage region-aggregation rules to balance analytical value and confidentiality.
  - Ensure robust metadata to support cross-table joins (site_ref, Region, crop_unit, etc.).
- Practical challenges to address:
  - Handling missing/null data and partial transect-derived measurements.
  - Aligning life-stage and trait classifications across conventional and GM datasets.
  - Maintaining consistency in units, scales, and species naming across years and crops.