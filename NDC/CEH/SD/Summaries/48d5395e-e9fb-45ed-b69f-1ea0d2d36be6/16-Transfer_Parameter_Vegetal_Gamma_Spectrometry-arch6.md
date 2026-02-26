# Supporting documentation for 16-Transfer_Parameter_Vegetal_Gamma_Spectrometry.csv

## Overview
- Provides supporting metadata and measurement fields for 16-Transfer_Parameter_Vegetal_Gamma_Spectrometry.csv.
- Captures sample identifiers, sample context, collection date, and transfer parameter values (Fv) for radionuclides.
- Includes uncertainties and detection limits for each Fv measurement.
- Indicates that blank values denote values below the detection limit.

## Data schema and fields
- Sample_Code
  - Explanation: Unique sample identifier.
  - Units: n/a
  - Notes: n/a
- Sample_Type
  - Explanation: Type of sample (e.g., Soil).
  - Units: n/a
  - Notes: n/a
- Location
  - Explanation: Location where the sample was collected.
  - Units: n/a
  - Notes: n/a
- Sample_Description
  - Explanation: Part of the plant analysed (e.g., where the whole plant was divided and analysed separately).
  - Units: n/a
  - Notes: n/a
- Collection_Date
  - Explanation: Date of sample collection.
  - Units: dd-mm-yyyy
  - Notes: n/a

## Measurement fields (Fv values, uncertainties, and detection limits)
- Ra-226_Fv
  - Explanation: Fv value for Ra-226.
  - Units: Unitless or kg dry matter per L for olive oil and wine.
  - Notes: If blank, Fv value was below the detection limit.
- Unc_Ra-226_Fv
  - Explanation: Uncertainty of the Ra-226 Fv value.
  - Units: Unitless or kg dry matter per L for olive oil and wine.
  - Notes: If blank, Fv value was below the detection limit.
- Detection_Limit_Ra-226_Fv
  - Explanation: Detection limit of the Ra-226 Fv value.
  - Units: Unitless or kg dry matter per L for olive oil and wine.
  - Notes: If blank, Fv value was above the detection limit.
- Cs-137_Fv
  - Explanation: Fv value for Cs-137.
  - Units: Unitless or kg dry matter per L for olive oil and wine.
  - Notes: If blank, Fv value was below the detection limit.
- Unc_Cs-137_Fv
  - Explanation: Uncertainty of the Cs-137 Fv value.
  - Units: Unitless or kg dry matter per L for olive oil and wine.
  - Notes: If blank, Fv value was below the detection limit.
- Detection_Limit_Cs-137_Fv
  - Explanation: Detection limit of the Cs-137 Fv value.
  - Units: Unitless or kg dry matter per L for olive oil and wine.
  - Notes: If blank, Fv value was above the detection limit.
- Ra-228_Fv
  - Explanation: Fv value for Ra-228.
  - Units: Unitless or kg dry matter per L for olive oil and wine.
  - Notes: If blank, Fv value was below the detection limit.
- Unc_Ra-228_Fv
  - Explanation: Uncertainty of the Ra-228 Fv value.
  - Units: Unitless or kg dry matter per L for olive oil and wine.
  - Notes: If blank, Fv value was below the detection limit.
- Detection_Limit_Ra-228_Fv
  - Explanation: Detection limit of the Ra-228 Fv value.
  - Units: Unitless or kg dry matter per L for olive oil and wine.
  - Notes: If blank, Fv value was above the detection limit.
- K-40_Fv
  - Explanation: Fv value for K-40.
  - Units: Unitless or kg dry matter per L for olive oil.
  - Notes: If blank, Fv value was below the detection limit.
- Unc_K-40_Fv
  - Explanation: Uncertainty of the K-40 Fv value.
  - Units: Unitless or kg dry matter per L for olive oil and wine.
  - Notes: If blank, Fv value was below the detection limit.
- Detection_Limit_K-40_Fv
  - Explanation: Detection limit of the K-40 Fv value.
  - Units: Unitless or kg dry matter per L for olive oil and wine.
  - Notes: If blank, Fv value was above the detection limit.

## Data quality considerations
- Missing values indicate measurements below the detection limit for the respective Fv field.
- Date format is specified as dd-mm-yyyy.
- Field names and units vary slightly in wording (e.g., some references to “Fv” values and detection-limit notes include formatting inconsistencies); interpretation should follow the explained meanings above.
- All measurements relate to transfer parameters for radionuclides in vegetal samples (olive oil and wine contexts mentioned in units).

## Data usage and transformations
- Use Sample_Code to join with sample metadata (Sample_Type, Location, Sample_Description, Collection_Date).
- Treat blank Fv and Unc_Fv values as censored data (below detection limit) in analyses; consider appropriate handling (e.g., use detection limit as a substitute or statistical methods for censored data).
- Combine Fv values with corresponding Unc_Fv and Detection_Limit fields to assess measurement reliability and detection status.
- Create self-service data products (dashboards/pivot analyses) showing Fv values by radionuclide across samples and by collection date or location.

## Practical notes for data handlers
- Ensure consistent interpretation of units across radionuclides, noting that K-40 and others may reference olive oil and wine contexts in the units description.
- Be aware of potential minor formatting inconsistencies in field names when integrating with other datasets; align to the defined meanings above.