# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Eddy Covariance Flux Data for Abbotts Hall, Essex

## Overview
- Dataset provides eddy covariance flux measurements at the Abbotts Hall Salt Marsh site in Essex, part of coastal ecosystems monitoring.
- Location: Abbotts Hall, Salcott channel, near the Blackwater Estuary; coordinates 51°47'9"N, 0°52'1"E.
- Timeframe: Half-hourly mean values from 15 December 2012 to 27 January 2015.
- Purpose: Support assessment of coastal biodiversity and ecosystem service sustainability through detailed flux measurements and environmental drivers.

## Data collected and variables
- Monitoring rate and site description
  - Half-hourly means; site described as a sheltered salt marsh with dendritic drainage, clay/organic sediments, and fragmented marsh network.
- Observed/derived variables (examples)
  - Meteorological and environmental: Air temperature (T_air), soil temperatures at 10 cm/20 cm/30 cm (T_soil_10cm, T_soil_20cm, T_soil_30cm), relative humidity (RH), vapour pressure deficit (VPD), net radiation (Net_rad), photosynthetically active radiation (PAR), precipitation (Precip), wind speed (Wind_Spd), wind direction (Wind_Dir).
  - Fluxes and energy terms: CO2 flux (Fc), CO2 flux filled (Fc_Filled), CO2 flux quality flag (Fc_QC), latent energy (LE) and filled (LE_Filled) with QC (LE_QC), sensible heat (H) and filled (H_Filled) with QC (H_QC), respiration modelled flux, u* friction velocity (ustar), Monin-Obukhov stability (MO).
- Data processing and processing notes
  - All fluxes corrected for frequency losses and WPL; CO2 fluxes corrected for storage terms.
  - Data were processed using EdiRe and Matlab; mean half-hour values calculated in Matlab; time stamps refer to the middle of the half-hour period.

## Data collection methods and instrumentation
- Instrumentation
  - Campbell Scientific (CS) data loggers; Closed Path Eddy Covariance (CPEC200) system with CSAT3A anemometer on a 4.3 m lattice tower.
  - Fluxes measured at 10 Hz; data logged with CS CR3000 and CR1000 dataloggers.
  - Air temperature and humidity measured with Vaisala HMP155A; precipitation with EML ARG100 tipping bucket; net radiation with Kipp and Zonen NR Lite; PAR with Skye Instruments SKP215; soil temperatures with CS 107 thermistors.
- Data processing
  - Fluxes processed using REddyProc gap-filling package; respiration modelled by Lloyd & Taylor model applied to nocturnal QC=0 CO2 flux data for separate months.
  - Data quality control based on diagnostic flags from gas analyser and anemometer; basic reality checks include radiation-bin based QC and sigma-based outlier detection.

## Quality control, gap filling, and data governance
- Quality control
  - QC flags defined: LE_QC, Fc_QC, and H_QC with classifications QC = 0 (best), 1 (marginal), 2 (poor), 3 (very poor); best data used for gap filling.
  - Data binned by radiation into 15 populated bins; within-bin outliers (>3.5 SD) flagged, and extreme outliers (>5 SD) flagged with higher QC.
  - Data affected by tower wind-shadow given QC = 3.
- Gap filling and modelling
  - Gaps filled using REddyProc, applied to QC=0 data only.
  - Respiration flux modeled using Lloyd & Taylor 1994 respiration model on nocturnal QC=0 CO2 flux data.
- Data provenance and governance
  - Emphasis on transparency of processing steps, quality flags, and data transformation; metadata and QC procedures are explicitly stated to support reproducibility and data governance.

## Data formats and metadata structure
- File formats
  - CSV format for data storage and sharing.
- Dataset field descriptions
  - Comprehensive field descriptions cover site, habitat, spatial scale, temporal components (year, month, day, hour, minute), and each measured/derived variable with units and coding (e.g., season, location, site, habitat, etc.).
- Time and spatial indexing
  - Time references correspond to the middle of each half-hour period; multiple site locations and habitat types are encoded to allow multi-site comparisons.
- Accessibility of metadata
  - Detailed metadata fields (e.g., variable names, units, qc flags, scale, row numbers) are included to support data interpretation and reuse.

## Data gaps, limitations, and caveats
- Data gaps exist due to sensor malfunctions or power loss; NA cells indicate missing data.
- Some metadata fields repeat or reference “See above,” indicating the need to consult the dataset’s metadata structure for full context.
- Data transformation and calibration require careful handling (e.g., QC filtering, gap-filling eligibility).

## Relevance for monitoring frameworks
- Demonstrates end-to-end data workflow for environmental monitoring: from on-site data collection and instrumentation to data processing, quality assurance, gap filling, and transparent metadata.
- Highlights critical governance aspects: robust metadata, standardized QC flags, data provenance, and reproducible processing steps.
- Illustrates how detailed environmental drivers (PAR, Net Radiance, meteorology) link to ecosystem fluxes (CO2, energy) and the importance of openness and data sharing considerations in monitoring programs.

## Key takeaways for policy-supporting monitoring
- Emphasizes thorough quality control and documentation to ensure data reliability for policy analysis.
- Shows how to handle missing data and maintain data quality through gap filling and model-based respiration estimates.
- Underlines the importance of detailed metadata and standardized data formats to enable cross-site comparability and informed decision-making.