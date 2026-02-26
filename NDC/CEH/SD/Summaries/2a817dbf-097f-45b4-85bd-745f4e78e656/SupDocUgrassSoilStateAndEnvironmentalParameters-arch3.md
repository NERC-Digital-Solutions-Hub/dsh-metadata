# U-GRASS (Understanding and enhancing soil ecosystem services and resilience in UK grass and croplands) UK grasslands: Soil state and environmental parameters across geo linked sampling locations

## Overview
- Study of soil state and environmental parameters from paired intensive and extensive grassland systems across 32 UK sites, including low and high pH parent soils.
- Samples collected during winter and spring 2015–2016; cores taken along 100 m land-use interfaces at 25 m intervals (5 paired replicates per site).
- Analyses cover total Nitrogen, total Carbon, total Organic Carbon, total Phosphorus, soil pH, soil moisture, loss on ignition, sand/silt/clay texture, FT-IR spectra, and bulk density.
- Aimed to understand soil functional change under different management and climatic scenarios as part of the NERC U-GRASS Soil Security Programme.

## Data collection design and lineage
- 32 sites chosen to contrast low vs high intensity agricultural practices near land-use interfaces.
- Soil cores (15x5 cm) collected November 2015–February 2016; stored frozen at -20°C prior to analyses.
- Analyses conducted by specialized laboratories:
  - Total N, total C, TOC by CEH Lancaster
  - Total P by CEH Lancaster
  - pH by CEH Wallingford
  - LOI and soil moisture by CEH Lancaster and Wallingford
  - Sand, silt, clay texture by NRM Laboratories
  - FT-IR spectra by CEH Wallingford
  - Bulk density by CEH Wallingford
- Results compiled into an Excel spreadsheet and deposited as a CSV file for the EIDC repository.

## Measured parameters and methods
- Chemical and physical soil properties:
  - Total Nitrogen (N), Total Carbon (C), Total Organic Carbon (TOC)
  - Total Phosphorus (P)
  - Soil pH (in water)
  - Soil moisture
  - Loss on ignition (LOI) as a measure of organic matter
  - Sand, silt, clay texture (percentage components)
  - Bulk density (g/cm3)
- Spectroscopic data:
  - Mid-infrared FT-IR spectra (MIR-ATR) with specific peak-based indicators:
    - clay1_IR (3600–3640 cm-1) and clay2_IR (3715–3680 cm-1) for clay bonds
    - sat_C_IR (3830–3970 cm-1) for saturated carbon
    - calc_IR (1340–1475 cm-1) for carbonate
  - Derived metrics include clay_quality_IR (ratio clay1_IR/clay2_IR)
- Metadata:
  - Id (unique sample identifier)
  - Latitude and longitude (GPS coordinates)

## Data structure and content
- Data file: UgrassSoilStateAndEnvironmentalParameters.csv
- Structure: 1 flat CSV with 450 data rows and 19 columns
- Key columns (examples):
  - Id, latitude, longitude
  - organic_C (%), total_C (%), total_N (%), total_P (mg/kg)
  - pH, soil_moisture (%), LOI (%)
  - sand (%), silt (%), clay (%)
  - clay1_IR, clay2_IR, clay_quality_IR, sat_C_IR, calc_IR
  - bulk_density (g/cm3)

## Data management and sharing
- Samples stored at -20°C prior to processing; analyses performed by designated CEH and partner laboratories.
- Results compiled into an Excel file and exported to CSV for deposition into the EIDC data archive.
- Data product: UgrassSoilStateAndEnvironmentalParameters.csv
- Emphasizes traceability of data provenance and lab-specific processing steps.

## Relevance for monitoring frameworks
- Provides a robust, geo-linked dataset across multiple management contrasts suitable for evaluating how grassland management and climate influence soil state and ecosystem services.
- Enables cross-site benchmarking of soil chemical, physical, and functional properties, informing policy monitoring and decision-making on sustainable soil management.
- Demonstrates a transparent data workflow from field collection to public data deposition, highlighting data governance and openness considerations for monitoring initiatives.