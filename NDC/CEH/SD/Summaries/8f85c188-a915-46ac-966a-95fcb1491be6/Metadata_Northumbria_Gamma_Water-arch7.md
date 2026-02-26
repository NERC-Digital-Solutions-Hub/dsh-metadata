# TREE_Northumbria_Gamma_Water

## Overview
- A dataset of radiochemical analyses in water samples, containing sample identifiers, site, description, mass analyzed, sampling/decay date, and activity concentrations for K-40 and Cs-137 in Becquerel per kilogram fresh mass (Bq/kg FM).
- Includes measurement uncertainties (two-sigma counting errors), and minimum detectable activity (MDA) values, with markers for concentrations below detection.

## Data fields and meanings
- CEH_Sample_Identifier: UKCEH radiochemistry laboratory unique sample identifier.
- CEH_Sample_Description: Description of the sample.
- Site: Sampling site (spatial reference for GIS use).
- Mass_of_Sample_Analysed_g: Mass of the sample analyzed (grams).
- Sampling_Date_Used_As_Decay_Date: Date the sample was taken (also used as decay date).
- K-40_Bq_per_kg_FM: Activity concentration of potassium-40 at sampling date (Bq/kg FM).
- Counting_Error_K-40_Bq_per_kg_FM: Two-sigma counting error for K-40.
- K-40_<: Indicator that the K-40 concentration is a "<" (below MDA) value.
- MDA_K-40_Bq_per_kg_FM: Minimum Detectable Activity for K-40 (Bq/kg FM).
- Cs-137_Bq_per_kg_FM: Activity concentration of cesium-137 at sampling date (Bq/kg FM).
- Counting_Error_Cs-137_Bq_per_kg_FM: Two-sigma counting error for Cs-137.
- Cs-137_<: Indicator that the Cs-137 concentration is a "<" (below MDA) value.
- MDA_Cs-137_Bq_per_kg_FM: Minimum Detectable Activity for Cs-137 (Bq/kg FM).
- General_Notes: Additional notes.

## Units and measurement details
- Bq per Kg FM: Becquerel per kilogram of fresh mass.
- Mass: Grams (g).
- Date fields: Calendar dates (sampling date, used as decay date).
- Counting errors: Two-sigma uncertainties.
- MDA: Minimum Detectable Activity values for each isotope.

## Spatial integration and GIS considerations
- Site serves as the spatial reference for mapping sample locations.
- Data can be mapped to visualize spatial patterns of K-40 and Cs-137 distributions across sampling sites.
- Suitable for joining with geographic layers to produce map-based visualisations of radiochemical measurements.

## Data quality and challenges (GIS perspective)
- Data may be dispersed across sources; ensure consistent data standards and harmonisation.
- Possible missing values or "<" entries requiring handling in analyses and visualisations.
- Large or complex datasets may need cleaning and efficient packaging for mapping.
- Resolution may vary; ensure alignment with GIS coordinate references when linking to sites.

## Usage tips for map-based visualisations
- Visualise K-40 and Cs-137 concentrations with graduated color scales; consider separate layers per isotope.
- Represent uncertainties (counting errors) as tooltips or error indicators (e.g., error bars) on map features.
- Use MDA fields to indicate censoring; decide on handling "<" values (e.g., substitution, censored visualization).
- Include General_Notes as metadata in map popups to aid interpretation.
- Link Site to spatial layers (e.g., sampling locations, hydrology, land use) to provide context.