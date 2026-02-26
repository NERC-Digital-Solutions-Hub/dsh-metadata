# TREE_Northumbria_ICPMS_Earthworm_DM_Concentration

## Overview
- A dataset describing elemental concentrations in earthworm tissue, measured by ICP-MS, with concentrations reported as mg/kg dry mass (DM).
- Context implies Northumbria sampling with UK CEH (Centre for Ecology & Hydrology) codes and descriptions.
- Includes both biological metadata (species) and sampling metadata (site, date, sample codes, notes).

## Data structure and fields
- Sample metadata
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - CEH_Sample_Description
  - Notes
- Concentration measurements (per sample), all with Units = mg/kg_DM
  - I_mg_kg_DM (Iodine)
  - Li_mg_kg_DM (Lithium)
  - Be_mg_kg_DM (Beryllium)
  - Na_mg_kg_DM (Sodium)
  - Mg_mg_kg_DM (Magnesium)
  - Al_mg_kg_DM (Aluminium)
  - P_mg_kg_DM (Phosphorus)
  - K_mg_kg_DM (Potassium)
  - Ca_mg_kg_DM (Calcium)
  - Ti_mg_kg_DM (Titanium)
  - V_mg_kg_DM (Vanadium)
  - Cr_mg_kg_DM (Chromium)
  - Mn_mg_kg_DM (Manganese)
  - Fe_mg_kg_DM (Iron)
  - Co_mg_kg_DM (Cobalt)
  - Ni_mg_kg_DM (Nickel)
  - Cu_mg_kg_DM (Copper)
  - Zn_mg_kg_DM (Zinc)
  - As_mg_kg_DM (Arsenic)
  - Se_mg_kg_DM (Selenium)
  - Rb_mg_kg_DM (Rubidium)
  - Sr_mg_kg_DM (Strontium)
  - Mo_mg_kg_DM (Molybdenum)
  - Ag_mg_kg_DM (Silver)
  - Cd_mg_kg_DM (Cadmium)
  - Cs_mg_kg_DM (Cesium)
  - Ba_mg_kg_DM (Barium)
  - Tl_mg_kg_DM (Thallium)
  - Pb_mg_kg_DM (Lead)
  - U_mg_kg_DM (Uranium)

## Measurements and units
- All elemental concentrations are reported as mg/kg on a dry mass basis (DM).
- The dataset uses a consistent set of concentration columns corresponding to a wide range of trace elements.

## Metadata and provenance
- CEH_Sample_Codes and CEH_Sample_Description indicate linkage to UK CEH lab codes and associated descriptions.
- Latin and Common species names provide taxonomic context for cross-referencing species.
- Date and site fields support temporal and spatial analyses; Notes capture any extra sampling information or anomalies.

## Data quality and challenges
- The data dictionary contains some typographical irregularities (e.g., trailing punctuation, formatting inconsistencies) that may require cleaning for automated processing.
- Potential missing values across some concentration fields; interpretation requires handling below-detection values where applicable.
- Consistency checks needed across fields to ensure accurate joins between species names, sample codes, and site metadata.

## Using the data (potential analyses)
- Compare elemental burden across sites or species to identify spatial or taxonomic patterns.
- Create summary dashboards or pivot tables to enable self-serve exploration of element concentrations by site, date, or species.
- Combine with environmental or soil data to explore drivers of elemental uptake in earthworms.
- Perform data quality checks, such as verifying units (mg/kg DM), ensuring date formats, and cross-validating CEH codes with public records.

## Data preparation and integration tips
- Normalize to a long format if enforcing multi-element comparisons or visualizations.
- Map Latin_Species_Name to Common_Species_Name consistently for user-friendly reporting.
- Validate CEH_Sample_Codes against external CEH records to ensure traceability.
- Check for and address any inconsistent or missing values in concentration columns before analysis.
- Maintain dry mass basis across all analyses to ensure comparability.