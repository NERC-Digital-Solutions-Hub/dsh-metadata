# Supporting documentation for Stable_concentration_means.csv

## Overview
- Provides a data dictionary for the Stable_concentration_means.csv file.
- Documents the fields used to describe samples, their species, reference animal/plant category, and the concentration means (with associated standard deviations) for multiple elements on a fresh weight basis.

## Data structure and key fields
- Sample_Code
  - Explanation: Unique sample identifier.
  - Units: n/a
  - Notes: .
- Species
  - Explanation: Latin name of species sampled.
  - Units: n/a
  - Notes: .
- RAP
  - Explanation: ICRP Reference Animals and Plants (RAP) category to which the sampled species can be attributed.
  - Units: n/a
  - Notes: .
- Sample_Description
  - Explanation: Part of the sample that was analysed.
  - Units: n/a
  - Notes: .
- Mean_Value
  - Explanation: Indicates whether the mean is geometric or arithmetic.
  - Units: n/a
  - Notes: Geometric or arithmetic mean as identified by Mean_Value.
- Element concentration fields (for each element, the same structure applies)
  - I-127_mg_kg, Li_mg_kg, Be_mg_kg, B_mg_kg, Na_mg_kg, Mg_mg_kg, Al_mg_kg, P_mg_kg, S_mg_kg, K_mg_kg, Ca_mg_kg, Ti_mg_kg, Mn_mg_kg, Fe_mg_kg, Co_mg_kg, Ni_mg_kg, Cu_mg_kg, Zn_mg_kg, As_mg_kg, Se_mg_kg, Rb_mg_kg, Sr_mg_kg, Mo_mg_kg, Ag_mg_kg, Cd_mg_kg, Cs_mg_kg, Ba_mg_kg, Pb_mg_kg, U_mg_kg
  - Explanation: Mean concentration expressed on a fresh weight basis for the respective element.
  - Units: Milligrams per kilogram (mg/kg)
  - Notes: Geometric or arithmetic mean as identified by Mean_Value.
- Standard_Deviation_<element>_mg_kg
  - Explanation: Standard deviation expressed on a fresh weight basis for the respective element.
  - Units: Milligrams per kilogram (mg/kg)
  - Notes: Geometric or arithmetic standard deviation as identified by Mean_Value.

## Measurement units and mean type
- All element concentrations are on a fresh weight basis and expressed in mg/kg.
- For each element, the associated standard deviation corresponds to the same mean type (geometric or arithmetic) as indicated by Mean_Value.

## Data provenance and quality considerations
- RAP provides taxonomic/biological context (ICRP RAP).
- Mean_Value specifies the nature of the central tendency used for the reported concentrations.
- Users should ensure consistent interpretation ofMean_Value across samples and align analyses accordingly (e.g., log-transformations may be appropriate for geometric means).
- The dataset structure is designed to support cross-sample comparisons by species, RAP category, and sample description, with standardized units across a wide panel of elements.

## Practical considerations for analysts
- Useful for identifying correlations between species/RAP category and element concentrations.
- Facilitates comparisons across samples and potential modelling of exposure or ecological risk.
- When combining datasets, ensure consistent handling of geometric vs arithmetic means and the corresponding standard deviations.
- Be mindful of potential missing values in any of the element fields or metadata (Sample_Code, Species, RAP, Sample_Description, Mean_Value).

## Notes and caveats
- The documentation text shows some formatting inconsistencies and repeated lines; the intended schema includes the fields described above with clear associations between Means and their corresponding standard deviations for each element.
- Administrative boundaries or local-scale data limitations may apply if integrating with other datasets; refer to data provenance (RAP and sample metadata) to contextualize comparisons.