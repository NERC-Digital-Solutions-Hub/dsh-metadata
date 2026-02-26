# TREE_Northumbria_Soil_Sample_Info

## Overview
- A metadata schema for soil samples, capturing location, collection timing, sample identifiers, physical and chemical measurements, and notes on preparation and analysis.
- Designed to support GIS-enabled mapping and spatial analysis by providing key attributes for each soil sample.

## Key Fields

- CEH_Sample_Description — Units: n/a; Explanation: CEH sample name
- Site — Units: n/a; Explanation: Sampling site
- National_Grid_Reference — Units: n/a; Explanation: National grid reference of soil sampling site
- Date_Sample_Collected — Units: n/a; Explanation: Date sample collected
- CEH_Sample_Code — Units: n/a; Explanation: CEH sample code related to soil sample
- pH — Units: n/a; Explanation: pH of soil sample
- LOI — Units: n/a; Explanation: LOI (loss on ignition) of soil sample
- Soil_Sampling_Depth_cm — Units: cm; Explanation: Soil sampling depth in centimeters
- Mass_Fresh_Soil_kg — Units: kg; Explanation: Fresh mass of soil sample in kilograms
- Mass_Dry_Soil_kg — Units: kg; Explanation: Dry mass of soil sample in kilograms
- General_Notes — Units: n/a; Explanation: General notes
- Sample_Preparation_And_Analysis_Performed — Units: n/a; Explanation: Sample preparation and analysis performed

## Data Quality and Standards Considerations
- Data may be held in multiple locations
- Potential lack of data at appropriate resolutions
- Inconsistent data standards across sources
- Large or complex datasets may not be packaged into manageable units
- Requires cleaning and transformation processes
- Skill development within teams may be needed to support data quality

## GIS Use and Integration
- National_Grid_Reference and Site enable spatial joins to map sample locations
- Depth (Soil_Sampling_Depth_cm) and mass/LOI/pH values provide thematic attributes for maps
- CEH_Sample_Code and CEH_Sample_Description support traceability to source records
- Date_Sample_Collected allows temporal analyses and time-series mapping of sampling efforts
- General_Notes and Sample_Preparation_And_Analysis_Performed provide context for data interpretation and comparability across samples

## Practical Considerations for Analysts
- Verify unit consistency (e.g., all masses in kg, depth in cm)
- Consolidate metadata from multiple sources before GIS integration
- Implement data cleaning to address missing or inconsistent values
- Establish standards for future data collection to improve interoperability across datasets