# Supporting documentation for 02-Sample_List.csv

## Purpose and use
- Provides a data dictionary for the 02-Sample_List.csv, describing each field to support GIS mapping and spatial analysis.
- Documents sample identity, type, location, description, collection timing, spatial coordinates, analyses performed, and any additional notes.

## Field descriptions
- Sample_Code — Unique sample identifier.
- Sample_Type — General description of the sample (e.g., foodstuff group). Units: n/a. Notes: n/a.
- Location — Name of the location where the sample was collected. Units: n/a. Notes: n/a.
- Sample_Description — Further description of the sample (e.g., when the organism/foodstuff was divided and analysed separately). Units: n/a. Notes: n/a.
- Collection_Date — Date of sample collection. Format: dd-mm-yyyy. Units: n/a. Notes: n/a.
- Coordinates_of_the_Sample — Latitude and longitude coordinates of the sampling location. Units: decimal degrees and minutes. Notes: n/a.
- Analysis — Analyses carried out (Gamma = gamma spectrometry; Stable = stable elements by ICP-MS). Units: n/a. Notes: n/a.
- Notes — Additional comments (where applicable). Units: n/a. Notes: n/a.

## Spatial data considerations
- Coordinates are provided for spatial plotting and GIS analysis; ensure proper handling of decimal degrees and minutes and convert to a consistent coordinate system (e.g., WGS84) as needed.
- Location and sample descriptions help in geospatial storytelling and filtering by area or sampling context.

## Data quality considerations
- Several fields list Units as n/a and Notes as n/a, indicating placeholders or missing metadata in some records.
- Collection_Date uses the format dd-mm-yyyy; ensure robust date parsing and validation.
- Consistency between Location names and coordinates should be checked to avoid mismatches in spatial joins.

## How this supports GIS workflows
- Enables map-based visualization by sample location, type, and collection timing.
- Allows filtering by Sample_Type and Analysis to produce focused thematic layers.
- Supports joining with external datasets on Sample_Code for enriched spatial analyses and temporal trends.