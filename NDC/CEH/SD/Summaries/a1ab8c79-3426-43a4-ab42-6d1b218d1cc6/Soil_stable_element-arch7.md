# Supporting documentation for Soil_Stable_Element.csv

## Overview
- Provides metadata and field definitions for Soil_Stable_Element.csv.
- Describes sample identifiers, sample types, descriptions, collection dates, and a comprehensive set of soil element concentrations measured on a dry mass basis (mg/kg_dw).
- Includes corresponding detection-limit fields and notes on how to interpret missing values and detection limits.
- Notes that certain samples are replicated and that dates use a specific format.

## Core data fields
- Sample identification and context
  - Sample_Code: Unique sample identifier
  - Sample_Type: Type of sample
  - Sample_Description: Further explanation of the sample
  - Collection_Date: Date of soil sample collection (format: dd month yyyy)
  - Sample_Description units: cm = centimetres (context for description field)

- Concentration measurements (selected examples)
  - I-127_mg_kg_dw
  - Li_mg_kg_dw
  - Be_mg_kg_dw
  - B_mg_kg_dw
  - Na_mg_kg_dw
  - Mg_mg_kg_dw
  - Al_mg_kg_dw
  - P_mg_kg_dw
  - S_mg_kg_dw
  - K_mg_kg_dw
  - Ca_mg_kg_dw
  - Ti_mg_kg_dw
  - V_mg_kg_dw
  - Cr_mg_kg_dw
  - Mn_mg_kg_dw
  - Fe_mg_kg_dw
  - Co_mg_kg_dw
  - Ni_mg_kg_dw
  - Cu_mg_kg_dw
  - Zn_mg_kg_dw
  - As_mg_kg_dw
  - Se_mg_kg_dw
  - Rb_mg_kg_dw
  - Sr_mg_kg_dw
  - Mo_mg_kg_dw
  - Ag_mg_kg_dw
  - Cd_mg_kg_dw
  - Cs_mg_kg_dw
  - Ba_mg_kg_dw
  - Tl_mg_kg_dw
  - Pb_mg_kg_dw
  - U_mg_kg_dw
  - Additional element and “given sample” variants appear in the data dictionary

- Detection limits (one per element)
  - Detection_Limit_<element>_mg_kg_dw
  - Note: Units typically Milligrams per kilogram. In many entries, a blank concentration value indicates below the detection limit (referenced by the corresponding Detection_Limit field); conversely, a blank detection-limit field often indicates the concentration was detectable (interpretation variations noted in the table).

## Replicates and sampling notes
- Replicates: Sample_Description notes that RC N119, 120, and 121 are replicate soil samples.
- Collection context: The dictionary provides guidance on how to interpret replication and measurement details across samples.

## Measurement semantics and data interpretation
- Measurements are presented as concentrations on a dry mass basis (mg/kg_dw) for the listed elements.
- Detection limits accompany each concentration to indicate the smallest measurable quantity for a given sample.
- Interpretation guidance (as stated in the dictionary):
  - If a concentration value is blank, it often indicates the concentration was below the detection limit, with the corresponding Detection_Limit field providing the limit.
  - In many entries, blanks in the Detection_Limit field imply that the concentration was detectable (i.e., above the detection limit). The exact interpretation can vary by element and column wording.

## Data quality and GIS considerations
- Data fragmentation: Data may be held in multiple places and across numerous fields, presenting integration challenges for GIS workflows.
- Consistency and standards: The dictionary highlights potential inconsistencies in data standards that GIS analysts should harmonize before visualizing or analyzing.
- Handling of detection limits: When mapping or analyzing, decide on strategies for censored data (below detection limit) to avoid bias in spatial representations.
- Replicates and resolution: Replicate samples and variable detection limits require careful aggregation and uncertainty handling in map products.
- Unit alignment: Most concentrations are in mg/kg_dw; ensure consistent unit usage when joining with other datasets or when converting for display.

## Practical guidance for GIS use
- Join soil concentration data to spatial units (polygons/points) using Sample_Code or equivalent keys.
- Represent detection-limit information clearly, e.g., via symbology that indicates “below detection limit” or by showing detected values with a separate layer for censored data.
- Use replication notes to assess uncertainty and to inform aggregation (e.g., mean concentrations across replicates within a spatial unit).
- Validate date formatting (Collection_Date) to support time-enabled GIS applications or temporal analyses.
- Consider data cleaning steps to harmonize fields with long or inconsistent names and to resolve any ambiguous entries before mapping.

## Cautions and caveats
- The document contains irregular formatting and inconsistent phrasing in places, so users should verify column meanings against the source when implementing data pipelines.
- Some entries include “given sample” qualifiers or mixed wording in the detection-limit descriptions; apply consistent interpretation rules during data processing.
- The wide range of elements and detection-limit columns requires careful schema design to avoid misinterpretation during GIS integration.