# Supporting documentation for Stable_concentration_means.csv

## Overview
- Provides the data dictionary and field definitions for the Stable_concentration_means.csv dataset.
- Supports environmental monitoring by detailing how sample concentrations are defined, measured, and reported.

## Data structure and key fields
- Sample_Code: Unique sample identifier.
- Species: Latin name of the species sampled.
- RAP: ICRP Reference Animals and Plants (RAP) attribution for the sampled species.
- Sample_Description: Part of the sample analyzed.
- Mean_Value: Mean concentration (geometric or arithmetic) as identified by Mean_Value.
- Standard_Deviation_<element>_m g_kg: Standard deviation for each element, expressed on a fresh weight basis.

## Analyte coverage and units
- Analytes covered include I-127, Li, Be, B, Na, Mg, Al, P, S, K, Ca, Ti, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Pb, U, and others (with varying availability and naming in the documentation).
- Units: Milligrams per kilogram (mg/kg) on a fresh weight basis.
-Measurements for each analyte are supplied as either geometric or arithmetic means, with corresponding standard deviations.

## Measurement details and statistics
- Mean_Value interpretation: Geometric or arithmetic mean as identified in the Mean_Value field.
- Standard_Deviation fields: Correspond to the same mean basis (geometric or arithmetic) and are tied to the respective element (e.g., Standard_Deviation_I-127_mg_kg, Standard_Deviation_Li_mg_kg, etc.).
- Some fields in the documentation show formatting inconsistencies, but the intended structure is to pair each analyte’s mean with its standard deviation on a fresh weight basis.

## Data quality, standardization, and processing
- Data undergoes verification, quality assurance, cleaning, and transformation prior to analysis.
- Analyses use standardized methods to yield outputs like categorized environmental health measures.
- Clear formats (reports, maps, charts) are used for presenting findings.

## Data management and accessibility
- Created datasets are stored and uploaded to appropriate data portals.
- Emphasizes enabling access to the underlying data used to generate final outputs, supporting transparency and reuse.

## Relevance to environmental monitoring practice
- Enables consistent, time-series assessment of environmental concentrations against standards.
- Supports scrutiny of policy performance and environmental health through standardized data representations and accessible underlying data.