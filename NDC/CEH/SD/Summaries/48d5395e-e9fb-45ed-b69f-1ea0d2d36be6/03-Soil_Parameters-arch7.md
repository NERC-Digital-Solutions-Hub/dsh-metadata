# Supporting documentation for 03-Soil_Parameters.csv

## Overview
- Defines the metadata and measurement fields for soil samples in the 03-Soil_Parameters.csv dataset.
- Covers sample identifiers, sample type, location description, sample description (including depth), collection date, and key soil properties.
- Focuses on map-ready soil attributes suitable for GIS visualisations and analyses.

## Fields and definitions
- Sample_Code
  - Explanation: Unique sample identifier.
  - Units: n/a
  - Notes: n/a

- Sample_Type
  - Explanation: General description of sample (e.g., foodstuff group).
  - Units: n/a
  - Notes: Soil

- Location
  - Explanation: Name of the location where the sample was collected.
  - Units: n/a
  - Notes: n/a

- Sample_Description
  - Explanation: Further description of the sample.
  - Units: n/a
  - Notes: Soil 0 - 10 cm

- Collection_Date
  - Explanation: Date of sample collection.
  - Units: dd-mm-yyyy
  - Notes: n/a

- pH
  - Explanation: Soil pH in water.
  - Units: n/a
  - Notes: n/a

- Conductivity_uS/cm
  - Explanation: Soil conductivity.
  - Units: μS/cm
  - Notes: n/a

- %_Clay
  - Explanation: Percentage of clay in soil.
  - Units: %
  - Notes: n/a

- %_Silt
  - Explanation: Percentage of silt in soil.
  - Units: %
  - Notes: n/a

- %_Fine_sand
  - Explanation: Percentage of fine sand in soil.
  - Units: %
  - Notes: n/a

- %_Coarse_sand
  - Explanation: Percentage of coarse sand in soil.
  - Units: %
  - Notes: n/a

## Data quality and GIS considerations
- Location field provides only a location name; coordinates are typically needed for spatial mapping and should be added or linked to spatial features.
- Depth description in Sample_Description indicates topsoil (0–10 cm) coverage; ensure consistency when integrating with other soil depth layers.
- Date format (dd-mm-yyyy) should be validated or converted to a standard GIS-friendly date format if used in time-enabled maps.
- Percentage fields (%_Clay, %_Silt, %_Fine_sand, %_Coarse_sand) may require validation to ensure sensible sums and data quality checks.

## GIS workflow implications
- Use Sample_Code to join soil measurements to spatial features (points or polygons) representing sampling locations.
- Use Collection_Date to explore temporal patterns in soil properties if multiple sampling events exist.
- Use texture fractions (clay, silt, sands) to classify soil texture classes or to create surface geology/soil maps.
- Leverage pH and conductivity rasters or symbology to illustrate soil chemical properties alongside physical texture.

## Notes and limitations
- Most fields have notes listed as n/a; the primary depth information is embedded in Sample_Description (0–10 cm).
- The Location field contains location names rather than explicit coordinates; integration with GIS workflows will require geocoding or linking to a spatial dataset.