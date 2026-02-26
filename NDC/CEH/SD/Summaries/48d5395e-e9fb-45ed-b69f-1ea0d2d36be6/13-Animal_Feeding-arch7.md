# Supporting documentation for 13-Animal_Feeding.csv

## Overview
- Provides metadata and field definitions for the 13-Animal_Feeding.csv dataset, which captures feeding-related information for different animals and sample collection locations.

## Field Definitions
- Animal
  - Description: General type of animal
  - Units: n/a
  - Notes: n/a
- Location
  - Description: Name of the location where the sample was collected
  - Units: n/a
  - Notes: n/a
- Feeding
  - Description: Description of the feeding regime
  - Units: n/a
  - Notes: n/a
- Daily_Ingestion
  - Description: Amount of dry matter ingested by an animal per day
  - Units: kg dry matter per day
  - Notes: n/a
- Composition_Animal_Feed
  - Description: Equation for the weighted composition of the total diet
  - Units: n/a
  - Notes: Information about animal feed composition provided by producers
- Abbreviations
  - Description: Abbreviations are based on Sample Codes
  - Units: n/a
  - Notes: Derived from Sample Codes

## GIS and Spatial Considerations
- Location is the collection site and can be linked to a spatial feature (point) in a GIS.
- To enable map-based analyses, consider geocoding Location or adding explicit coordinates (latitude/longitude).
- Attributes (Animal, Feeding, Daily_Ingestion, Composition_Animal_Feed) can be visualized as thematic layers (e.g., ingestion rates by location) or joined to other spatial datasets.

## Data Quality and Standardization
- Daily_Ingestion has a defined unit (kg dry matter per day); other fields list Units as n/a and may require interpretation during GIS integration.
- Ensure consistent naming for Location to support reliable geocoding and joining with external spatial datasets.
- Composition_Animal_Feed is an equation and may require parsing or metadata to interpret; ensure proper handling in data products.
- Abbreviations are based on Sample Codes; maintain a mapping to full codes for clarity in analyses.

## Practical Use for GIS Specialists
- Create spatial layers showing ingestion metrics and feeding regimes by location.
- Combine with environmental or management data to explore factors influencing feeding patterns.
- Use the data dictionary to inform data cleaning, standardization, and schema design for GIS workflows.