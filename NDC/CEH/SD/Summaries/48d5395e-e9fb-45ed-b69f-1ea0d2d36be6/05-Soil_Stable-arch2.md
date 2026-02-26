# Supporting documentation for 05-Soil_Stable.csv

## Purpose and scope
- Provides a data dictionary for the soil dataset 05-Soil_Stable.csv.
- Documents metadata, measurement fields, units, and handling of non-detects to support standardized environmental monitoring.
- Focuses on soil collected at shallow depth (0–10 cm) and measured concentrations of multiple stable elements and radionuclides.

## Metadata and samples
- Sample metadata includes:
  - Sample_Code: unique sample identifier.
  - Sample_Type: Soil.
  - Location: site name where the sample was collected.
  - Sample_Description: additional details; soil collected at depth 0–10 cm.
  - Collection_Date: formatted as dd-mm-yyyy.
  - Sample_size_g_dm: amount of sample analyzed (g dry matter).

## Measured constituents and units
- Concentrations provided on a dry matter basis (mg/kg_dm) for:
  - Cs_mg/kg_dm, Sr_mg/kg_dm, K_mg/kg_dm, Na_mg/kg_dm, Ca_mg/kg_dm, Mg_mg/kg_dm, P_mg/kg_dm, Pb_mg/kg_dm, U_mg/kg_dm, Th_mg/kg_dm (with multiple entries for Th).
- Each concentration field typically has accompanying:
  - Unc_<element>_mg/kg_dm: combined measurement uncertainty (mg/kg dry mass).
  - Detection_Limit_<element>_mg/kg_dm: detection limit (mg/kg dry mass).
- Notes indicate measurement context and data handling:
  - If a value is blank, the concentration is below the detection limit.
  - Some fields explicitly state "on a dry matter basis" and/or provide alternative wording for mass-based equivalents.
- Th_mg/kg_dm is presented with sub-indices (1, 2, 3) representing multiple measurements or replicates, each with corresponding uncertainty and detection-limit fields.

## Data quality and handling
- The documentation standardizes definitions of units and formats to enable consistent QA/QC.
- Non-detects are clearly flagged via blanks and linked to detection limits.
- Field explanations sometimes reuse different phrasing (e.g., “on a dry matter basis,” “mg per kg dry mass”) but convey the same unit context.

## Relevance for environmental monitoring
- Enables consistent assessment of soil composition and potential contaminants/nutrients across sites and over time.
- Supports standardized outputs (reports, maps, charts) and data integration into portals.
- Facilitates data verification, quality assurance, cleaning, and transformation required for policy performance monitoring.

## How analysts use this documentation
- Verify data against the defined fields, units, and handling rules.
- Perform quality assurance and data cleaning to produce standardized datasets.
- Create outputs (maps, charts, reports) and store/upload datasets to appropriate data portals.