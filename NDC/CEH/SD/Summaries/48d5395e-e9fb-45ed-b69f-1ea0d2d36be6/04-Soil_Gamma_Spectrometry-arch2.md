# Supporting documentation for 04-Soil_Gamma_Spectrometry.csv

## Purpose and scope
- Provides metadata and definitions for the 04-Soil_Gamma_Spectrometry.csv dataset.
- Documents soil samples and gamma-spectrometry-derived activity concentrations of key radionuclides on a dry mass basis.
- Supports consistent environmental monitoring, enabling time-series analysis and policy performance assessment.

## Data structure and fields
- Sample_Code: unique sample identifier.
- Sample_Type: Soil.
- Location: name of the collection site.
- Sample_Description: additional description; for these samples, soil collected at 0–10 cm depth.
- Collection_Date: date of sampling (format: dd-mm-yyyy).
- Sample_size: amount analyzed (Kg dry matter).
- Radionuclide concentrations and related fields:
  - Ra-226_Bq/kg_dm: activity concentration of Ra-226 on a dry mass basis; notes indicate equilibrium with Pb-214 and Bi-214; blank = below detection limit.
  - Unc_Ra-226_Bq/kg_dm: uncertainty of Ra-226 concentration; same equilibrium note; blank = below detection limit.
  - Detection_Limit_Ra-226_Bq/kg_dm: ISO 11929-based detection limit; equilibrium note included; blank not specified.
  - Cs-137_Bq/kg_dm: activity concentration of Cs-137; blank = below detection limit.
  - Unc_Cs-137_Bq/kg_dm: uncertainty for Cs-137 concentration; blank = below detection limit.
  - Detection_Limit_Cs-137_Bq/kg_dm: ISO 11929-based detection limit; “n/a” in some entries.
  - Ra-228_Bq/kg_dm: activity concentration of Ra-228; notes indicate equilibrium with Ac-228; blank = below detection limit.
  - Unc_Ra-228_Bq/kg_dm: uncertainty for Ra-228; with enumerated notes (1–3) describing units and equilibrium; blank = below detection limit.
  - Detection_Limit_Ra-228_Bq/kg_dm: detection limit for Ra-228; enumerated notes (1–3) describing units and equilibrium; blank = below detection limit.
  - K-40_Bq/kg_dm: activity concentration of K-40; enumerated notes (1–3) describe units and detection limit status.
  - Unc_K-40_Bq/kg_dm: uncertainty for K-40; enumerated notes (1–3) describe units and detection limit status.
  - Detection_Limit_K-40_Bq/kg_dm: detection limit for K-40; enumerated notes (1–3) describe units; blank = not specified.

## Measurement specifics
- All radionuclide concentrations are reported on a dry mass basis (Bq/kg_dm).
- Values may be blank to indicate concentrations below the detection limit, with detection limits defined per ISO 11929 for each nuclide.
- Equilibrium relationships noted for some nuclides (e.g., Ra-226 with Pb-214/Bi-214; Ra-228 with Ac-228).

## Data quality, interpretation, and usage
- Intended for verification, quality assurance, cleaning, and transformation into standardised outputs (e.g., reports, maps, charts).
- Clear interpretation rules: blanks imply below-detection-limit values; uncertainties accompany concentration estimates.
- Facilitates cross-site and temporal comparisons within environmental monitoring programs.

## Practical relevance for analysts and monitoring objectives
- Supports standardised environmental health assessments and policy performance monitoring over time.
- Enables integration with other environmental datasets to enhance the value and applicability of the radiological soil data.
- Aids data sharing by documenting measurement context, detection capabilities, and equilibrium assumptions.

## Data management and accessibility implications
- Dataset examples should be stored and uploaded to appropriate portals with consistent metadata.
- Encourages making underlying data accessible to stakeholders to enable broader analysis and transparency.