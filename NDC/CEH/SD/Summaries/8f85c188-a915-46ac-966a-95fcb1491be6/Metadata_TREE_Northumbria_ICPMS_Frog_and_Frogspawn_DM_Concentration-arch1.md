# TREE_Northumbria_ICPMS_Frog_and_Frogspawn_DM_Concentration

## Overview
- Metadata table describing concentrations of multiple elements in frog tissue or frogspawn from Northumbria, using ICP-MS measurements.
- Contains sample identifiers, taxonomy, site and collection details, tissue type, and mass-related metrics alongside concentrations for a wide range of elements.
- Concentrations are reported in milligrams per kilogram of dry mass (mg/kg DM).
- Some concentration entries are annotated as below detection limit using specialized "<" markers (e.g., <Be, <Ni, <Se, <U, <Ag, <Ba, etc.).

## Key fields

### Sample identifiers and taxonomy
- Latin_Species_Name
- Common_Species_Name
- Site
- Date_Sample_Collected
- CEH_Sample_Codes
- CEH_Sample_Description

### Sample characteristics
- Tissue (frog tissue sampled or frogspawn)
- Fresh_Mass_Dry_Mass_Ratio

### Concentration measurements (mg/kg DM)
- I_mg_kg_DM
- Li_mg_kg_DM
- Be_mg_kg_DM
- B_mg_kg_DM
- Na_mg_kg_DM
- Mg_mg_kg_DM
- Al_mg_kg_DM
- P_mg_kg_DM
- S_mg_kg_DM
- K_mg_kg_DM
- Ca_mg_kg_DM
- Ti_mg_kg_DM
- V_mg_kg_DM
- Cr_mg_kg_DM
- Mn_mg_kg_DM
- Fe_mg_kg_DM
- Co_mg_kg_DM
- Ni_mg_kg_DM
- Cu_mg_kg_DM
- Zn_mg_kg_DM
- As_mg_kg_DM
- Se_mg_kg_DM
- Rb_mg_kg_DM
- Sr_mg_kg_DM
- Mo_mg_kg_DM
- Ag_mg_kg_DM
- Cd_mg_kg_DM
- Cs_mg_kg_DM
- Ba_mg_kg_DM
- Tl_mg_kg_DM
- Pb_mg_kg_DM
- U_mg_kg_DM
- I_mg_kg_DM (Iodine)

### Data qualifiers and special markers
- Be, Al, Ni, Se, Ag, Ba, U columns have accompanying "<Be", "<Al", "<Ni", "<Se", "<Ag", "<Ba", "<U" metadata describing that those values are “less than” the reported concentration in the corresponding column.
- Some fields include “n/a” where not applicable or not provided.

## Data provenance and structure
- CEH_Sample_Codes and CEH_Sample_Description provide the UK Centre for Ecology & Hydrology sample identifiers and descriptions.
- The dataset is organized to capture species and site context, sampling date, tissue type, and broad elemental concentrations in a consistent unit framework.

## Usage notes for analysts
- Suitable for identifying correlations between species, site, timing, tissue type, and elemental concentrations.
- Enables cross-dataset comparisons by leveraging consistent metadata fields (Latin_Species_Name, Site, Date_Sample_Collected, etc.).
- Handle censored (<) values appropriately in analyses (consider detection limits implied by the corresponding markers).
- All concentration values are reported on a dry-mass basis (mg/kg DM); ensure consistency when integrating with other datasets (e.g., moisture content adjustments if needed).

## Data quality and limitations
- The dataset uses a broad suite of elements, including trace and major elements, with some entries below detection limits.
- Some fields show typographical irregularities (e.g., minor formatting in field names) but the intended meanings are clear (concentration values, tissue type, sample metadata).
- Several fields may be “n/a” where not applicable or missing.