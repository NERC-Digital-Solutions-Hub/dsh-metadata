# U-GRASS (Understanding and enhancing soil ecosystem services and resilience in UK grass and croplands) UK grasslands: Soil state and environmental parameters across geo linked sampling locations

## Executive summary
- Data describe soil state and environmental parameters from paired intensive and extensive grassland systems, including low and high pH parent soils, across 32 UK sites.
- Sampling occurred in winter–spring 2015–2016; cores collected at 15x5 cm along a 100 m land-use interface, every 25 m, yielding 5 paired replicates per site.
- Analyzed for total nitrogen (N), total carbon (C), total organic carbon (TOC), total phosphorus (P), soil pH, soil moisture, loss on ignition (LOI), sand, silt, clay, FT-IR spectra, and bulk density.
- Purpose: to understand soil functional change under different management and climatic scenarios as part of the NERC U-GRASS programme, addressing soil security and ecosystem services.
- Data lineage: samples stored frozen at -20°C; analyses conducted at CEH Lancaster and Wallingford, and NRM Laboratories; results compiled into an Excel file and exported as a CSV for deposition into the Environmental Information Data Centre (EIDC).

## Data collection and scope
- 32 UK grassland sites chosen with contrasting land-use (low vs. high intensity) in proximity to each other.
- Sampling occurred between November 2015 and February 2016; samples stored at -20°C prior to analysis.

## Measurements and methods
- Total Nitrogen, total Carbon, and total Organic Carbon:
  - Measured by combustion (Elementar Vario EL) after ball milling and drying; TOC via decarbonation with HCl.
- Total Phosphorus (P):
  - Digestion with H2O2/H2SO4 mix; colorimetric analysis (molybdenum blue) at 880 nm.
- Soil pH:
  - Measured in deionised water (soil:water ratio 1:2.5) using a calibrated electrode.
- Soil moisture and Loss on ignition (LOI):
  - LOI as a proxy for organic matter; moisture at 25°C drying, LOI after 375°C furnace heating.
- Texture (sand, silt, clay):
  - Percent composition measured by NRML Laboratories (sums to 100%).
- FT-IR spectra:
  - Mid-infrared spectroscopy (MIR-ATR) on dried, milled samples; spectral range 4000–650 cm^-1; specific peak areas used to estimate clay bonds, saturated carbon, and carbonate.
- Bulk density:
  - Estimated from core weight (adjusted for moisture) and core volume; stones excluded.

## Data structure and contents
- File format: flat CSV (UgrassSoilStateAndEnvironmentalParameters.csv).
- Contents: 450 data rows and 19 columns.
- Key fields include:
  - Geographic: latitude, longitude (GPS coordinates).
  - Soil chemistry and properties: organic_C (%), total_C (%), total_N (%), total_P (mg/kg), pH, soil_moisture (%), LOI (%).
  - Texture: sand (%), silt (%), clay (%).
  - FT-IR metrics: clay1_IR, clay2_IR, clay_quality_IR, sat_C_IR, calc_IR.
  - Physical: bulk_density (g/cm3).
  - Identifiers: Id (unique reference).
- NA indicates data not recorded.

## Data provenance and storage
- Source material: soil cores from 32 UK grassland sites; paired sampling design; storage and processing as described above.
- Data processing: laboratories performed chemical and physical analyses; results compiled in Excel; exported to CSV for deposition.
- Storage and sharing: data deposited to the EIDC (Environmental Information Data Centre).

## Associated outputs and access
- Analysis outputs file: UgrassSoilStateAndEnvironmentalParameters.csv
- Intended use: support monitoring and analysis of soil state and environmental parameters across geo-linked locations; suitable for integration with GIS and other environmental datasets to track soil health and ecosystem services over time.