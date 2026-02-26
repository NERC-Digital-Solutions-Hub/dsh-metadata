# Supporting documentation for 16-Transfer_Parameter_Vegetal_Gamma_Spectrometry.csv

## Overview
- Metadata guide for a CSV containing transfer parameters (Fv values) of radionuclides in vegetal samples.
- Radionuclides covered: Ra-226, Cs-137, Ra-228, K-40.
- Sample type indicated as soil; sample descriptions refer to plant parts analyzed (e.g., whole plant sections).
- Includes Fv values, uncertainties, and detection limits; empty cells indicate values below detection limits.
- Units for Fv values may vary by radionuclide and matrix (olive oil and wine context mentioned).

## Field definitions and data types
- Sample_Code
  - Type: string
  - Description: Unique sample identifier.
- Sample_Type
  - Type: string
  - Description: Sample classification (e.g., Soil).
- Location
  - Type: string
  - Description: Name of the collection location (to be linked to a spatial layer).
- Sample_Description
  - Type: string
  - Description: Part of the plant analyzed (e.g., section of the whole plant).
- Collection_Date
  - Type: date
  - Description: Date of sample collection (formatted dd-mm-yyyy).
- Ra-226_Fv
  - Type: numeric
  - Description: Fv transfer parameter for Ra-226.
  - Units: Unitless or kg dry matter per L for olive oil and wine.
- Unc_Ra-226_Fv
  - Type: numeric
  - Description: Uncertainty of Ra-226_Fv.
  - Units: Unitless or kg dry matter per L for olive oil and wine.
- Detection_Limit_Ra-226_Fv
  - Type: numeric
  - Description: Detection limit for Ra-226_Fv.
  - Units: Unitless or kg dry matter per L for olive oil and wine.
- Cs-137_Fv
  - Type: numeric
  - Description: Fv transfer parameter for Cs-137.
  - Units: Unitless or kg dry matter per L for olive oil and wine.
- Unc_Cs-137_Fv
  - Type: numeric
  - Description: Uncertainty of Cs-137_Fv.
  - Units: Unitless or kg dry matter per L for olive oil and wine.
- Detection_Limit_Cs-137_Fv
  - Type: numeric
  - Description: Detection limit for Cs-137_Fv.
  - Units: Unitless or kg dry matter per L for olive oil and wine.
- Ra-228_Fv
  - Type: numeric
  - Description: Fv transfer parameter for Ra-228.
  - Units: Unitless or kg dry matter per L for olive oil and wine.
- Unc_Ra-228_Fv
  - Type: numeric
  - Description: Uncertainty of Ra-228_Fv.
  - Units: Unitless or kg dry matter per L for olive oil and wine.
- Detection_Limit_Ra-228_Fv
  - Type: numeric
  - Description: Detection limit for Ra-228_Fv.
  - Units: Unitless or kg dry matter per L for olive oil and wine.
- K-40_Fv
  - Type: numeric
  - Description: Fv transfer parameter for K-40.
  - Units: Unitless or kg dry matter per L for olive oil.
- Unc_K-40_Fv
  - Type: numeric
  - Description: Uncertainty of K-40_Fv.
  - Units: Unitless or kg dry matter per L for olive oil and wine (text contains inconsistencies; treat as applicable to olive oil and wine).
- Detection_Limit_K-40_Fv
  - Type: numeric
  - Description: Detection limit for K-40_Fv.
  - Units: Unitless or kg dry matter per L for olive oil and wine (text contains inconsistencies).

> Note: The documentation contains typographical inconsistencies in units and notes (e.g., references to olive oil, wine, and missing/ambiguous terms). Treat units and notes as guidance and validate during data ingestion.

## Spatial and temporal context for GIS
- Location: can be linked to a spatial layer to map sample sites.
- Collection_Date: enables time-series or seasonal analyses of transfer parameters.
- Sample_Description and Sample_Type provide contextual spatial attributes for interpretation (e.g., plant parts vs. soil context).

## Data quality, cleaning, and harmonisation considerations
- Missing values indicate measurements below detection limits (per Notes column references).
- Units for Fv values vary by radionuclide and matrix; standardise to a consistent unit across the dataset before mapping.
- Inconsistencies in notes and units (especially for K-40) require verification during data ingestion.
- Data may be spread across multiple sources; plan for integration with location-based layers and potential resampling to a common spatial resolution.

## How GIS specialists can use this data
- Create feature-level maps of Fv transfer parameters by location (Location linked to a basemap or shapefile).
- Visualise temporal trends by using Collection_Date as a time dimension.
- Combine Fv fields with environmental layers (soil type, vegetation, land use) to explore drivers of transfer differences.
- Use uncertainty fields (Unc_Ra-226_Fv, Unc_Cs-137_Fv, etc.) to generate confidence intervals on maps or risk assessments.
- Apply data cleaning steps to address below-detection values (e.g., flagging, censoring, or imputation) prior to visualization.

## Practical considerations and caveats
- Ensure consistent units across all Fv fields for reliable comparisons.
- Handle detection-limit values appropriately to avoid misinterpretation on maps (e.g., using censoring or tiered symbology).
- Be mindful of the soil sample type while interpreting transfer parameters intended for olive oil and wine matrices.
- Document any assumptions made during unit standardisation and data cleaning to maintain reproducibility.

## Summary of value for GIS workflows
- Enables spatial visualization and analysis of radionuclide transfer from environmental samples to vegetal matrices.
- Supports integrated risk assessment and policy-oriented visualization by location and time.
- Provides essential metadata and uncertainty information to support robust GIS-informed decision making.