# Please note that the units used in the data base are as listed below.

## Overview
- This document lists the units used for each variable in the database.
- It notes that database units may differ from the units quoted by chemical analysts, as documented in Metadata_Analytical methods_conwy catchment spatial water chemistry.xlsx.
- A crosswalk or reference file is provided to clarify the mapping between database variables and analyst-reported units.

## Data structure and contents
- The dataset uses a columnar structure where:
  - Column 1 shows column names (e.g., Master_Site, Site_Code, Date, Rep, CaQual, Ca, MgQual, Mg, NaQual, Na, etc.).
  - Column 2 shows the units for the corresponding database values.
- Parameter groups include major ions, nutrients, and a wide range of chemical analytes (examples include Ca, Mg, Na, Cl, NO3, NH4, NO2, DOC, pH, Alkalinity, Al, Total_N, PO4_P, TON, Conductivity, Si, Fe, Mn, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Cd, Sb, Cs, Ba, Pb, U, B, S, La, Ce, Pr, W, Ti, Sn, among others).
- For many variables, there are accompanying Qual fields (e.g., CaQual, MgQual, NO3Qual, etc.) that indicate data quality or qualifier status.
- A variety of unit types appear, including:
  - ueq/l (microequivalents per liter)
  - ug/l (micrograms per liter)
  - mg/l (milligrams per liter)
  - us/cm (microsiemens per centimeter for conductivity)
  - mg/l for some particulate or dissolved forms (e.g., POM, POC, PO4_P)
- Some measurements or qualifiers may reference additional metadata (e.g., “Qual” fields) rather than the primary value alone.

## Unit conventions and crosswalk
- The units in the database are defined per variable and may not match the units in analyst-issued metadata.
- A crosswalk to clarifying metadata exists in the referenced Excel file: Metadata_Analytical methods_conwy catchment spatial water chemistry.xlsx.
- Typical patterns (illustrative, not exhaustive) include:
  - Major ions and alkalinity often reported in ueq/l
  - Cations/anions and trace elements frequently in ug/l
  - Conductivity reported in us/cm
  - Nutrients like PO4_P and TON may be in mg/l or related forms
  - Si, POM, POC, and related measures in mg/l
- The presence of Qual fields alongside each primary variable helps communicate data quality, provenance, or measurement context.

## Data quality and governance considerations
- Data Stewards should note potential inconsistencies between database units and analyst-quoted units and ensure alignment via the crosswalk.
- Ensure proper documentation of unit conventions in dataset metadata and data catalogs.
- Maintain synchronization between the primary values and their corresponding Qual fields to preserve data quality context.
- When importing or sharing data, verify unit compatibility and plan for unit conversions if a single canonical unit is required for downstream use.

## Practical implications for data stewardship
- Implement a clear unit mapping table and reference it in data ingestion pipelines.
- Validate that each variable’s unit is consistent with the documented crosswalk and metadata.
- Preserve provenance by maintaining both the database value and its Qual flag where applicable.
- Provide guidance to data users on supported units and any required conversions to a canonical unit.
- Monitor for updates to the crosswalk or metadata and apply changes to maintain alignment.

## Related challenges (context from the document)
- Incomplete understanding of user needs and data priorities.
- Timely acquisition of data and adherence to metadata standards.
- Getting data creators to meet standards, including comprehensive metadata.
- Working with multiple systems and formats, including non-interoperable or legacy databases.
- Handling large datasets and potential data transfer bottlenecks.
- Dealing with outdated databases that require bespoke solutions.