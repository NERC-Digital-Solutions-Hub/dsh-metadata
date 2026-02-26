# TREE_Northumbria_ICPMS_Vegetation_FM_Concentration

## Overview
- A dataset of ICP-MS measured concentrations of multiple elements in vegetation samples from Northumbria, with accompanying metadata about species, sampling site, and sample identifiers.
- Includes both taxonomic metadata (Latin and common names) and detailed concentration measurements in mg/kg fresh mass (FM).
- Contains indicators for “less than” values and several fields that may have missing information.

## Data structure and key fields

- Taxonomic and sample metadata
  - Latin_Species_Name: Latin name of the plant species
  - Common_Species_Name: Common name of the species
  - Site: Sampling site
  - Date_Sample_Collected: Date the sample was collected
  - CEH_Sample_Identifier: UKCEH sample identifier
  - CEH_Sample_Description: Description of the UKCEH sample
  - Fresh_Mass_Dry_Mass_Ratio: Ratio of fresh mass to dry mass for the sample
  - Notes indicating that some fields may be “n/a” (no information)

- Data quality and formatting notes
  - The dataset uses specific markers to denote concentration values that are below a detection limit, indicated by a leading < (e.g., <I, <Li, etc.)
  - Some fields and explanations are labeled as “n/a” (not applicable or no information)

- Element concentration data (mg/kg, fresh mass)
  - I_mg_kg_FM: Iodine concentration
  - Li_mg_kg_FM: Lithium concentration
  - Be_mg_kg_FM: Beryllium concentration
  - Na_mg_kg_FM: Sodium concentration
  - Mg_mg_kg_FM: Magnesium concentration
  - Al_mg_kg_FM: Aluminum concentration
  - P_mg_kg_FM: Phosphorus concentration
  - K_mg_kg_FM: Potassium concentration
  - Ca_mg_kg_FM: Calcium concentration
  - Ti_mg_kg_FM: Titanium concentration
  - V_mg_kg_FM: Vanadium concentration
  - Cr_mg_kg_FM: Chromium concentration
  - Mn_mg_kg_FM: Manganese concentration
  - Fe_mg_kg_FM: Iron concentration
  - Co_mg_kg_FM: Cobalt concentration
  - Ni_mg_kg_FM: Nickel concentration
  - Cu_mg_kg_FM: Copper concentration
  - Zn_mg_kg_FM: Zinc concentration
  - As_mg_kg_FM: Arsenic concentration
  - Se_mg_kg_FM: Selenium concentration
  - Rb_mg_kg_FM: Rubidium concentration
  - Sr_mg_kg_FM: Strontium concentration
  - Mo_mg_kg_FM: Molybdenum concentration
  - Ag_mg_kg_FM: Silver concentration
  - Cd_mg_kg_FM: Cadmium concentration
  - Cs_mg_kg_FM: Cesium concentration
  - Ba_mg_kg_FM: Barium concentration
  - Tl_mg_kg_FM: Thallium concentration
  - Pb_mg_kg_FM: Lead concentration
  - U_mg_kg_FM: Uranium concentration

- Value conventions
  - All concentration values are in mg/kg of fresh mass (FM)
  - Some concentrations may be reported with a “less than” value using a < marker (e.g., <I)
  - For certain columns, the accompanying explanations may indicate “n/a” where information is not available

## Units and value conventions

- Primary unit: milligrams per kilogram (mg/kg) on a fresh mass basis (FM)
- “Less than” values are indicated with a leading <
- Several fields may be missing or not applicable (n/a)

## Data quality considerations

- Data may be patchy and come from multiple formats/systems
- Some fields contain “n/a” (no information)
- Concentration values may include detection-limit indicators (e.g., < marker), requiring careful handling for analyses

## How this data supports analysis and end use

- Enables cross-species and site comparisons of trace element uptake in vegetation
- Supports creation of self-serve data products (dashboards, pivot tables) for end users to explore element concentrations by species, site, or date
- Facilitates data quality checks, cleaning, and transformation to harmonize formats across datasets
- Provides metadata for proper interpretation of concentrations (species names, sampling context, sample identifiers)
- Useful for further data sharing and collaboration, potentially guiding better data creation and sharing practices in future sampling programs