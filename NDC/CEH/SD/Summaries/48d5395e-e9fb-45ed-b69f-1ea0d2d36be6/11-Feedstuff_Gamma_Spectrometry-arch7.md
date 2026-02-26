# Supporting documentation for 11-Feedstuff_Gamma_Spectrometry.csv

## Overview
- Metadata for a CSV containing gamma spectrometry results on feedstuff samples.
- Captures: sample identifiers, sample description, location, collection date, sample size, and activity concentrations of multiple radionuclides.
- Radionuclides covered: Ra-226, Cs-137, Ra-228, K-40 (all on a dry mass basis, Bq/kg_dm or Bq/kg_dry mass).
- Includes uncertainties and detection limits (per ISO 11929) for several radionuclides.
- Notes indicate equilibrium relationships (e.g., Ra-226 in equilibrium with Pb-214 and Bi-214; Ra-228 in equilibrium with Ac-228) and when values are below detection limits.

## Data schema (key fields and meaning)
- Sample_Code: Unique identifier for each sample.
- Sample_Type: General category of the sample (e.g., feedstuff group).
- Location: Location where the sample was collected.
- Sample_Description: Part of the organism analyzed (e.g., tissue or section).
- Collection_Date: Date of collection (dd-mm-yyyy).
- Sample_size: Amount of sample analyzed (units: kg fresh mass).
- Ra-226_Bq/kg_dm: Activity concentration of Ra-226 (Bq/kg dry mass); notes on equilibrium.
- Unc_Ra-226_Bq/kg_dm: Uncertainty of Ra-226 concentration.
- Detection_Limit_Ra-226_Bq/kg_dm: Detection limit for Ra-226 (ISO 11929).
- Cs-137_Bq/kg_dm: Activity concentration of Cs-137 (Bq/kg dry mass); notes on detection limit.
- Unc_Cs-137_Bq/kg_dm: Uncertainty for Cs-137 concentration.
- Detection_Limit_Cs-137_Bq/kg_dm: Detection limit for Cs-137 (ISO 11929).
- Ra-228_Bq/kg_dm: Activity concentration of Ra-228 (Bq/kg dry mass); notes on equilibrium.
- Unc_Ra-228_Bq/kg_dm: Uncertainty for Ra-228 (with sub-notes indicating equilibrium with Ac-228).
- Detection_Limit_Ra-228_Bq/kg_dm: Detection limit for Ra-228 (ISO 11929).
- K-40_Bq/kg_dm: Activity concentration of K-40 (Bq/kg dry mass); notes on detection limit.
- Unc_K-40_Bq/kg_dm: Uncertainty for K-40 concentration.
- Detection_Limit_K-40_Bq/kg_dm: Detection limit for K-40 (ISO 11929).

## Spatial and temporal aspects
- Location provides the spatial reference for mapping; can be linked to coordinates or regional identifiers in a GIS.
- Collection_Date enables temporal analysis of radionuclide concentrations across time.
- Sample_Description and Sample_Type support stratification by tissue/part and sample category for GIS-based thematic mapping.

## Measurement details and data quality
- Units are consistently reported as Bq/kg_dry mass (dry mass basis) for all radionuclides, with some entries explicitly labeled as Bq/kg_dm.
- Where values are blank, the note indicates the concentration was below the detection limit.
- Detection limits are calculated according to ISO 11929.
- Uncertainties accompany each activity concentration where provided.
- Equilibrium notes (e.g., Ra-226 with Pb-214/Bi-214; Ra-228 with Ac-228) help interpret related radionuclide data.
- Some fields include multi-part notes (e.g., “1 = … 2 = …”) likely indicating subfields or documentation conventions; ensure consistent parsing during data ingestion.

## Data interpretation cautions
- Non-detects are represented by blank entries and should be treated as censored data using the corresponding detection limit.
- Ensure consistent unit usage when integrating with GIS workflows (verify whether Bq/kg_dm or Bq/kg_dry mass is used uniformly).
- Be mindful of equilibrium relationships when interpreting paired radionuclide concentrations (e.g., Ra-226 vs. Pb-214/Bi-214).

## GIS-specific usage and integration
- Potential visualizations:
  - Spatial distribution maps of each radionuclide’s concentration by Location.
  - Thematic maps showing concentration ranges (e.g., deciles or predefined thresholds) for Ra-226, Cs-137, Ra-228, and K-40.
  - Temporal trends by Location using Collection_Date, where multiple samples from the same location exist.
- Data preparation steps:
  - Normalize units to a single standard (preferably Bq/kg dry mass) across all records.
  - Resolve Location to coordinates if only names are present, enabling GIS layering.
  - Handle non-detects via detection limits to avoid bias in choropleth or heatmap visualizations.
  - Incorporate Sample_Size and Sample_Description as metadata fields to contextualize mapped values (e.g., represent as population-weighted estimates if needed).
- QA/QA steps:
  - Validate that all isotope fields align with their corresponding uncertainties and detection limits.
  - Check for inconsistent formatting in fields with multi-part notes and harmonize during ingestion.

## Practical considerations for archiving and reuse
- This documentation provides the schema and interpretation rules required to load the CSV into GIS tools and create map-based data products for policy, client reports, or public-facing visuals.
- Clear handling of below-detection-limit values and equilibrium relationships improves comparability across datasets and over time.