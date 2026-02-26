# TREE_Northumbria_ICPMS_Earthworm_FM_Concentration

## Purpose and scope
- Data dictionary/dataset for earthworm tissue concentrations measured via ICP-MS at Northumbria, with concentrations reported as mg/kg fresh mass (FM).
- Captures taxonomic details, sampling context, and multi-element concentration data to support environmental monitoring and policy evaluation over time.

## Data structure and key fields
- Taxonomy
  - Latin_Species_Name (with Explanation)
  - Common_Species_Name (with Explanation)
- Sampling context
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes (UKCEH sample codes)
  - CEH_Sample_Description (UKCEH sample description)
  - Notes (sampling notes)
- Concentration data (elements; all units mg/kg FM)
  - I_mg_kg_FM (Iodine)
  - Li_mg_kg_FM (Lithium)
  - Be_mg_kg_FM (Beryllium)
  - Na_mg_kg_FM (Sodium)
  - Mg_mg_kg_FM (Magnesium)
  - Al_mg_kg_FM (Aluminium)
  - P_mg_kg_FM (Phosphorus)
  - K_mg_kg_FM (Potassium)
  - Ca_mg_kg_FM (Calcium)
  - Ti_mg_kg_FM (Titanium)
  - V_mg_kg_FM (Vanadium)
  - Cr_mg_kg_FM (Chromium)
  - Mn_mg_kg_FM (Manganese)
  - Co_mg_kg_FM (Cobalt)
  - Ni_mg_kg_FM (Nickel)
  - Cu_mg_kg_FM (Copper)
  - Zn_mg_kg_FM (Zinc)
  - As_mg_kg_FM (Arsenic)
  - Se_mg_kg_FM (Selenium)
  - Rb_mg_kg_FM (Rubidium)
  - Sr_mg_kg_FM (Strontium)
  - Mo_mg_kg_FM (Molybdenum)
  - Ag_mg_kg_FM (Silver)
  - Cd_mg_kg_FM (Cadmium)
  - Cs_mg_kg_FM (Cesium)
  - Ba_mg_kg_FM (Barium)
  - Tl_mg_kg_FM (Thallium)
  - Pb_mg_kg_FM (Lead)
  - U_mg_kg_FM (Uranium)
- Field metadata notes
  - Some entries include inconsistencies or typographical errors in the Explanation/Description for certain elements (e.g., Co_mg_kg_FM and Ni_mg_kg_FM contain descriptions referencing iron or incorrect attribution). These indicate the need for data cleaning and quality assurance.

## Data quality and governance considerations
- Data are organized to support verification, quality assurance, cleaning, and transformation consistent with environmental monitoring practices.
- Output formats from analyses are intended to be clear and support dissemination via reports, maps, and charts.
- Data should be stored and uploaded to appropriate data portals to enable broader access, in line with standard monitoring workflows.

## How this supports monitoring goals
- Provides a consistent, auditable format for environmental health indicators across sites and time.
- Facilitates cross-dataset integration by standardizing taxonomic, site, sample, and multi-element concentration fields.
- Enables analysts to produce standardized outputs for policy evaluation and public reporting.

## Practical considerations and potential improvements
- Address typographical/label inconsistencies in element descriptions to ensure accurate interpretation (e.g., correct attribution of element concentrations and units).
- Maintain robust QA processes to ensure integrity of species, site, sampling, and multi-element concentration data for long-term trend analyses.