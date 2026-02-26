# TREE_Northumbria_Gamma_Soil

## Overview
- Dataset containing radiochemical soil sample data from UKCEH Radiochemistry Laboratory.
- Includes unique sample identifiers, descriptive metadata, sampling site, sample mass, and date used as decay date.
- Provides activity concentrations for K-40 and Cs-137 in Bq per kg dry mass, with associated counting errors and minimum detectable activities (MDA).
- Flags for concentrations not measured or below MDA are included.

## Key Variables (schema snapshot)
- CEH_Sample_Identifier: UKCEH Radiochemistry Laboratory unique sample identifier.
- CEH_Sample_Description: UKCEH sample description.
- Site: Sampling site.
- Mass_of_Sample_Analysed_g: Mass of sample analysed (grams).
- Sampling_Date_Used_As_Decay_Date: Date the sample was taken, used as decay date.
- Fresh_Mass_Dry_Mass_Ratio: Fresh mass to freeze dry mass ratio of soil.
- K-40_Bq_per_kg_DM: Activity concentration of K-40 in Bq per kg dry mass at the day of sampling.
- Counting_Error_K-40_Bq_per_kg_DM: Two sigma counting error of K-40 (Bq/kg DM).
- K-40_<: Marker indicating concentration is less than the MDA.
- MDA_K-40_Bq_per_kg_DM: Minimum detectable activity concentration of K-40 (Bq/kg DM).
- Cs-137_Bq_per_kg_DM: Activity concentration of Cs-137 in Bq per kg dry mass.
- Counting_Error_Cs-137_Bq_per_kg_DM: Two sigma counting error of Cs-137 (Bq/kg DM).
- Cs-137_<: Marker indicating Cs-137 concentration is less than the MDA.
- MDA_Cs-137_Bq_per_kg_DM: Minimum detectable activity concentration of Cs-137 (Bq/kg DM).

## Measurement Details
- Units:
  - Activity: Bq per kg dry mass (Bq/kg_DM).
  - Mass: grams (g).
- Sample-derived fields:
  - Fresh_Mass_Dry_Mass_Ratio describes sample preparation context (fresh vs. freeze-dried mass).
  - Decay/date reference is taken from Sampling_Date_Used_As_Decay_Date.

## Data Quality and Handling
- Not measured flags indicate measurements below the detectable threshold (MDA).
- The “<” markers denote values below the MDA for K-40 or Cs-137.
- Clear unit definitions aid integration with other datasets; be mindful of potential inconsistencies if combining with data at different resolutions or from other laboratories.

## Spatial and GIS Considerations
- Site provides sampling location; to map, geocode Sites or join with spatial layers to assign coordinates.
- Data suitable for map-based visualisations of radiometric concentration (K-40 and Cs-137) at sampling sites.
- When creating GIS products, consider:
  - Filtering by MDA or Not Measured tokens.
  - Representing < values appropriately (e.g., capped values, or separate categorical flag).
  - Integrating with other spatial datasets for context (e.g., soil type, land use).

## Relevance for GIS Specialists
- Enables creation of thematic maps showing spatial distribution of natural radionuclide activity (K-40) and anthropogenic radionuclide (Cs-137) in soils.
- Supports data cleaning and transformation tasks necessary for map production (handling Not measured and below-MDA values).
- Requires careful data standardization and potential georeferencing of the Site field to produce accurate spatial visualisations.