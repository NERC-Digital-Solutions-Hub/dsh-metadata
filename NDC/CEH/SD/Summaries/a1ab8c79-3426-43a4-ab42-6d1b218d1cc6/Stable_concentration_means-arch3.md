# Supporting documentation for Stable_concentration_means.csv

## Overview
- Provides metadata and column definitions for the Stable_concentration_means.csv dataset.
- Documents how sample and species data are described, how concentrations are represented, and how statistics (means and standard deviations) are stored for multiple elements.
- Aims to support data transparency, provenance, and reuse in environmental monitoring analyses.

## Key fields and data structure
- Sample_Code
  - Explanation: Unique sample identifier
  - Units: n/a
  - Notes: .
- Species
  - Explanation: Latin name of species sampled
  - Units: n/a
  - Notes: .
- RAP
  - Explanation: ICRP Reference Animals and Plant (RAP) to which the sampled species can be attributed
  - Units: n/a
  - Notes: .
- Sample_Description
  - Explanation: Part of the sample that was analysed
  - Units: n/a
  - Notes: .
- Mean_Value
  - Explanation: Geometric mean or arithmetic mean
  - Units: n/a
  - Notes: .
- I-127_mg_kg
  - Explanation: Mean concentration expressed on a fresh weight basis
  - Units: Milligrams per kilogram
  - Notes: Geometric or arithmetic mean as identified by Mean_Value
- Standard_Deviation_I-127_mg_ kg
  - Explanation: Standard deviation expressed on a fresh weight basis
  - Units: Milligrams per kilogram
  - Notes: Geometric or arithmetic standard deviation as identified by Mean_Value
- Li_mg_kg, Be_mg_kg, B_mg_kg, Na_mg_kg, Mg_mg_kg, Al_mg_kg, P_mg_kg, S_mg_kg, K_mg_kg, Ca_mg_kg, Ti_mg_kg, Mn_mg_kg, Fe_mg_kg, Co_mg_kg, Ni_mg_kg, Cu_mg_kg, Zn_mg_kg, As_mg_kg, Se_mg_kg, Rb_mg_kg, Sr_mg_kg, Mo_mg_kg, Ag_mg_kg, Cd_mg_kg, Cs_mg_kg, Ba_mg_kg, Pb_mg_kg, U_mg_kg
  - Explanation: Mean concentrations for each respective element, expressed on a fresh weight basis
  - Units: Milligrams per kilogram
  - Notes: Geometric or arithmetic mean as identified by Mean_Value
- Standard_Deviation_<element>_mg_kg (for each listed element)
  - Explanation: Standard deviation expressed on a fresh weight basis
  - Units: Milligrams per kilogram
  - Notes: Geometric or arithmetic standard deviation as identified by Mean_Value
- The document also includes several lines with placeholder or misformatted fields (e.g., empty column names) indicating inconsistent or garbled entries, all intended to represent standard deviation and mean fields for the corresponding elements.

## Unit and measurement details
- All concentration values are expressed on a fresh weight basis.
- Units used across concentration fields: milligrams per kilogram (mg/kg).
- Mean_Value indicates whether the mean is geometric or arithmetic; Standard_Deviation fields correspond to that choice.

## Data quality and metadata notes
- Metadata coverage is essential for reuse; the document highlights the need for clear, complete metadata (origin of datasets, data governance, and provenance).
- Some entries show formatting inconsistencies and garbled column naming, indicating potential data quality issues that may require cleaning or verification.
- Explicit linkage between Mean_Value and the appropriate Standard_Deviation field is required to interpret the statistics correctly.

## Implications for monitoring framework authors
- Use as a reference schema when designing or evaluating concentration-mean datasets for environmental monitoring.
- Ensure metadata completeness, especially regarding data provenance, measurement methods, and the choice between geometric versus arithmetic statistics.
- When integrating into dashboards or reports, align displays with the fresh weight basis and clearly indicate whether means are geometric or arithmetic and which type of standard deviation is used.
- Be mindful of potential garbled or missing field names in the source data; implement data validation to catch inconsistencies before analysis.