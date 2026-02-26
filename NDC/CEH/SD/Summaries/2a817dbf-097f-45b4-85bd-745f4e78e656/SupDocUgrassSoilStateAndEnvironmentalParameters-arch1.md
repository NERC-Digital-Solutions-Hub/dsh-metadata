# U-GRASS (Understanding and enhancing soil ecosystem services and resilience in UK grass and croplands) UK grasslands: Soil state and environmental parameters across geo linked sampling locations

## Executive summary
- Data describe soil state and environmental parameters from 32 UK grassland sites with land-use contrasts (low vs. high intensity) sampled across paired intensive/extensive systems.
- Winter–spring 2015–2016 sampling; cores collected along a 100 m land-use interface with 5 paired replicates per site.
- Samples subdivided for analyses of: total nitrogen, total carbon, total organic carbon, total phosphorus, soil pH, soil moisture, loss on ignition, sand, silt, clay, FT-IR spectra, and bulk density.
- Purpose: to understand soil functional change under different management and climatic scenarios; part of the NERC U-GRASS programme (NE/M017125/1) within the Soil Security Programme.
- Lineage: samples stored at -20°C prior to chemical, physical, molecular, and functional analyses; analyses conducted by CEH Lancaster, CEH Wallingford, and NRMLab; results compiled in Excel and exported as CSV for deposition into the EIDC.
- Context: background emphasis on soil organic matter, soil biodiversity, and the role of edaphic context in modulating soil processes under management and climate change.

## Protocols and measurements (highlights)
- 2.1 Soil sampling
  - 32 sites across the UK with a land-use intensity contrast.
  - Soil cores (15 × 5 cm) collected along 100 m interface, every 25 m; 5 paired replicates per site.
  - Sampling Nov 2015–Feb 2016; cores stored frozen at -20°C prior to analysis.
- 2.2 Total nitrogen, total carbon, total organic carbon
  - Ball-milled samples; oven-dried at ~105°C; 20 mg weighed into tin cups.
  - Total C and N measured by Elementar Vario EL (oxidative combustion with thermal conductivity detection).
  - Total organic C determined after decarbonation with HCl.
- 2.3 Total phosphorus (P)
  - H2O2/H2SO4 digestion with Se and Li2SO4; colorimetric analysis on a SEAL discrete analyser.
  - 0.36 g soil per digestion; absorbance measured at 880 nm after complex formation and reduction.
- 2.4 Soil pH
  - Measured in deionised water (25 mL water to 10 g soil; equilibrated; pH read with electrode).
- 2.5 Soil moisture and loss on ignition (LOI)
  - LOI and moisture: dried at 105°C and 25°C sequence; LOI represents organic matter content.
- 2.6 Sand, silt, clay and texture
  - Texture analysis performed by NRMLab; values reported as percent sand, silt, clay (sum = 100%).
- 2.7 FT-IR spectra
  - Mid-infrared ATR (MIR-ATR) on Nicolet iS10; 4000–650 cm-1, 8 cm-1 resolution, 16 scans per replicate.
  - Peaks used to estimate: clay bonds (3600–3640 cm-1; Al-AL), additional clay bonds (3715–3680 cm-1), saturated carbon (3830–3970 cm-1), carbonate (1340–1475 cm-1).
- 2.8 Bulk density
  - Calculated from core weight and volume; corrected for stone volume/weight.

## Data structure and contents
- Data file: UgrassSoilStateAndEnvironmentalParameters.csv
- Contents: single flat CSV with 450 data rows and 19 columns.
- Key columns and meanings
  - id: unique cross-reference identifier
  - latitude, longitude: GPS coordinates
  - organic_C (%): soil organic carbon content
  - total_C (%): total soil carbon content
  - total_N (%): total nitrogen content
  - total_P (mg/kg): total phosphorus
  - pH: soil pH (in water)
  - soil_moisture (%): soil moisture
  - LOI (%): loss on ignition (organic matter proxy)
  - sand (%), silt (%), clay (%): soil texture components
  - clay1_IR, clay2_IR: FT-IR-derived metrics (areas under defined peaks)
  - clay_quality_IR: ratio clay1_IR/clay2_IR (clay type indicator)
  - sat_C_IR: saturated carbon (FT-IR)
  - calc_IR: carbonate estimate (FT-IR)
  - bulk_density (g/cm3): corrected bulk density
- Notes
  - NA indicates data were not recorded for a given field.

## Associated files
- Analysis outputs: UgrassSoilStateAndEnvironmentalParameters.csv

## Context and aims
- Rationale: understanding soil security and the capacity of soils to perform multiple functions under changing land use and climate.
- Focus: link soil physical/chemical properties with soil biodiversity and ecosystem services, and assess how edaphic context modulates soil processes and resilience across different management regimes.