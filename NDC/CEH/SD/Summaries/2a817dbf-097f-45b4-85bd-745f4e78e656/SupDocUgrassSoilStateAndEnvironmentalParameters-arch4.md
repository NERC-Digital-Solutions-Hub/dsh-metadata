# U-GRASS (Understanding and enhancing soil ecosystem services and resilience in UK grass and croplands) UK grasslands: Soil state and environmental parameters across geo linked sampling locations

## Executive summary
- Study of soil state and environmental parameters from 32 paired grassland sites across the UK, covering low/high pH parent soils and various management regimes.
- Winter–spring 2015–2016 sampling; cores collected along 100 m land-use interface with five paired replicates per site.
- Samples subdivided for analyses of total nitrogen, total carbon, total organic carbon, total phosphorus, soil pH, soil moisture, loss on ignition, sand/silt/clay texture, FT-IR spectra, and bulk density.
- Data generation aligned with the NERC U-GRASS program to understand soil functions under different management and climatic scenarios; samples stored at -20°C prior to analyses.
- Data compiled from multiple CEH laboratories and deposited as a CSV in the EIDC.

## Data collection design and sampling
- 32 sites across the UK chosen to represent land-use contrasts between low and high intensity practices.
- Soil cores (15x5 cm) collected along 100 m interface, with sampling every 25 m; 5 replicates per site.
- Cores stored at -20°C before downstream chemical, physical, molecular, and functional analyses.

## Measurements and methods
- Total Nitrogen (total_N), Total Carbon (total_C), Total Organic Carbon (organic_C): measured by combustion and detection (Elementar Vario EL) after prep steps; organic_C determined after decarbonation.
- Total Phosphorus (total_P): acid digestion followed by colorimetric analysis using molybdenum blue method.
- Soil pH: measured in deionised water with standard soil-to-water ratio and electrode measurement.
- Soil moisture and Loss on Ignition (LOI): LOI method with drying and furnace steps to determine organic matter content.
- Texture (sand, silt, clay): percentage composition determined by NR Laboratories.
- FT-IR spectra (FT-IR): mid-infrared MIR-ATR spectroscopy on dried, milled soils; specific peak areas used to estimate clay bonds, saturated carbon, and carbonate.
- Bulk density: calculated from core dry weight and total core volume, adjusted for stone volume/weight.

## Data structure and schema
- Single flat CSV file with 450 rows and 19 columns.
- Key fields include:
  - Id: unique cross-reference identifier
  - latitude, longitude: GPS coordinates
  - organic_C, total_C, total_N: percentages
  - total_P: mg/kg
  - pH: pH units
  - soil_moisture, LOI: percentages
  - sand, silt, clay: percentages (sum to 100)
  - FT-IR related: clay1_IR, clay2_IR, clay_quality_IR, sat_C_IR, calc_IR
  - bulk_density: g/cm3
- NA indicates missing data; units and descriptions provided for all fields.
- Additional context: data were initially compiled in Excel and then exported to CSV for deposition into the EIDC.

## Lineage, provenance, and data governance
- Soil samples collected from 32 grassland sites with contrasting land use; stored at -20°C prior to analysis.
- Analyses performed by CEH Lancaster (carbon, nitrogen, phosphorus, LOI, FT-IR), CEH Wallingford (pH, bulk density, LOI), and NRM Laboratories (texture).
- Results aggregated into an Excel spreadsheet and then deposited as a CSV to the Environmental Information Data Centre (EIDC).
- Authorship includes researchers from CEH and partner institutions, reflecting multi-site data generation and processing workflows.

## Data accessibility and associated files
- Primary analysis outputs: UgrassSoilStateAndEnvironmentalParameters.csv
- Associated with the project report and metadata describing sampling design, analytical protocols, and data structure.

## Relevance for data strategy and governance (Data Leaders perspective)
- Demonstrates end-to-end data lifecycle: standardized sample collection design, multi-lab analytical workflows, and consolidated data provisioning.
- Rich, multi-parameter soil dataset enabling cross-cutting analyses of soil state, organic matter, nutrient status, texture, and spectral properties across management regimes.
- Clear metadata in the data structure, including units, descriptions, and handling of missing values, supporting data discoverability and reuse.
- Geographic tagging (latitude/longitude) facilitates integration with spatial analyses and broader soil security/functional studies.
- Potential for establishing data standards across labs (methodologies summarized) and promoting co-ownership of data products through a shared dataset.
- Data are deposited in a recognized data centre (EIDC), improving long-term accessibility and governance.

## Practical considerations for use
- Researchers can examine relationships among organic carbon, total carbon/nitrogen, phosphorus, and physical properties across contrasting land-use contexts.
- FT-IR spectra-derived variables enable investigation of organic and mineral components influencing soil functionality.
- The dataset supports assessments of soil resilience and ecosystem services under varied management and climatic scenarios.