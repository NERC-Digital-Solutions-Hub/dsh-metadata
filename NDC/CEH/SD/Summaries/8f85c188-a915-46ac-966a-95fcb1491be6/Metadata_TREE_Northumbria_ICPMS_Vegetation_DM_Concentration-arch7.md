# TREE_Northumbria_ICPMS_Vegetation_DM_Concentration

## Overview
- A data dictionary/schema for a vegetation ICP-MS concentration dataset.
- Captures species information, sampling details, and concentrations of multiple elements in vegetation.
- Concentrations are reported as milligrams per kilogram of dry mass (mg/kg DM).
- Includes UKCEH sample identifiers and descriptions for linking to physical samples.

## Key fields
- Latin_Species_Name: Latin name of species.
- Common_Species_Name: Common name of species.
- Site: Sampling site.
- Date_Sample_Collected: Date when the sample was collected.
- CEH_Sample_Identifier: UKCEH sample identifier.
- CEH_Sample_Description: UKCEH sample description.
- I_mg_kg_DM: Concentration of Iodine in mg/kg DM.
- Li_mg_kg_DM: Concentration of Lithium in mg/kg DM.
- Be_mg_kg_DM: Concentration of Beryllium in mg/kg DM.
- Na_mg_kg_DM: Concentration of Sodium in mg/kg DM.
- Mg_mg_kg_DM: Concentration of Magnesium in mg/kg DM.
- Al_mg_kg_DM: Concentration of Aluminum in mg/kg DM.
- P_mg_kg_DM: Concentration of Phosphorus in mg/kg DM.
- K_mg_kg_DM: Concentration of Potassium in mg/kg DM.
- Ca_mg_kg_DM: Concentration of Calcium in mg/kg DM.
- Ti_mg_kg_DM: Concentration of Titanium in mg/kg DM.
- V_mg_kg_DM: Concentration of Vanadium in mg/kg DM.
- Cr_mg_kg_DM: Concentration of Chromium in mg/kg DM.
- Mn_mg_kg_DM: Concentration of Manganese in mg/kg DM.
- Fe_mg_kg_DM: Concentration of Iron in mg/kg DM.
- Co_mg_kg_DM: Concentration of Cobalt in mg/kg DM.
- Ni_mg_kg_DM: Concentration of Nickel in mg/kg DM.
- Cu_mg_kg_DM: Concentration of Copper in mg/kg DM.
- Zn_mg_kg_DM: Concentration of Zinc in mg/kg DM.
- As_mg_kg_DM: Concentration of Arsenic in mg/kg DM.
- Se_mg_kg_DM: Concentration of Selenium in mg/kg DM (with possible additional related columns for interpretation).
- Rb_mg_kg_DM: Concentration of Rubidium in mg/kg DM.
- Sr_mg_kg_DM: Concentration of Strontium in mg/kg DM.
- Mo_mg_kg_DM: Concentration of Molybdenum in mg/kg DM (with possible additional related columns).
- Ag_mg_kg_DM: Concentration of Silver in mg/kg DM.
- Cd_mg_kg_DM: Concentration of Cadmium in mg/kg DM.
- Cs_mg_kg_DM: Concentration of Cesium in mg/kg DM.
- Ba_mg_kg_DM: Concentration of Barium in mg/kg DM.
- Tl_mg_kg_DM: Concentration of Thallium in mg/kg DM (with possible additional related columns).
- Pb_mg_kg_DM: Concentration of Lead in mg/kg DM.
- U_mg_kg_DM: Concentration of Uranium in mg/kg DM.
- Additional related columns (e.g., Se_mg_kg_DM_1/Se_mg_kg_DM_2, Mo_mg_kg_DM_1/Mo_mg_kg_DM_2, etc.) indicating paired data fields or interpretation notes.

## Data details
- Units: mg/kg dry mass (DM) for all element concentrations.
- Date and site information facilitate spatial and temporal analyses.
- Some concentration values may be reported as “less than” values, indicated by a < marker in the relevant columns.
- Explanatory text accompanies many fields to clarify species names, sample identifiers, and measurement context.

## Special markers and structure
- “<” markers denote censored or “less than” concentration values in certain columns.
- Some elements have paired columns (e.g., Se_mg_kg_DM, 1 and Se_mg_kg_DM, 2) to capture different aspects of the measurement or interpretation per the dataset’s design.

## GIS use and implications
- Rich, multi-element vegetation concentration data suitable for map-based visualization across sites and species.
- Can support:
  - Point or site-level mapping of element concentrations.
  - Species-specific or site-comparison choropleth maps if spatial geometry is available.
  - Temporal analysis using Date_Sample_Collected to observe changes over time.
- Requires linking to spatial coordinates (via Site or CEH_Sample_Identifier) and consistent data standards across elements.
- Must handle less-than values appropriately in visualizations (e.g., censored data treatment, transparency, or separate categories).

## Data quality and challenges (aligned to GIS practitioner perspective)
- Data may be distributed across multiple sources; normalization and standardization may be needed.
- Variability in data resolution and the presence of censored (<) values can complicate mapping and interpretation.
- Ensuring consistent unit interpretation (mg/kg DM) is essential for accurate cross-site comparisons.
- Handling of paired or additional related columns (e.g., Se_mg_kg_DM_1/2) requires clear metadata for correct GIS integration.