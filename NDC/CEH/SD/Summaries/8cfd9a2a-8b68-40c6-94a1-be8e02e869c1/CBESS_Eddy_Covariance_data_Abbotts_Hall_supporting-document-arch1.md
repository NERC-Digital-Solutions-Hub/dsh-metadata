# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Eddy Covariance Flux Data for Abbotts Hall, Essex

## Overview
- Eddy covariance flux measurements collected at Abbotts Hall (Essex) salt marsh.
- Time period: 15 December 2012 to 27 January 2015.
- Data are half-hourly mean values; some variables are recorded at higher frequency (10 Hz for fluxes and wind, 1 Hz for other measurements).
- Used for analysing ecosystem exchanges (CO2, energy) and related environmental drivers.

## Location and Site Context
- Site: Abbotts Hall salt marsh, Salcott channel, ~3 km from the Blackwater Estuary.
- Environment: Sheltered from SW and NE winds, part of a network of connected salt marshes; marsh is highly dissected with dendritic drainage, clay/organic sediments, and evidence of fragmentation.

## Data Collection and Instruments
- Instrumentation: Campbell Scientific data loggers; Closed Path Eddy Covariance (CPEC200) system with CSAT3A 3D sonic anemometer on a 4.3 m mast; CS CR3000 and CR1000 loggers with multiplexers.
- Sampling: Fluxes and wind at 10 Hz; remaining variables at 1/60 Hz (every minute).
- Auxiliary measurements: Air temperature, soil temperature (10/20/30 cm), relative humidity, net radiation, PAR, precipitation, wind speed/direction, vapour pressure deficit, CO2 flux, and modelled components (Respiration, u*, Monin-Obukhov stability).
- Processing software: EdiRe and Matlab for flux processing; REddyProc for gap-filling.

## Variables Observed
- Environmental drivers: T_air, T_soil_10cm, T_soil_20cm, T_soil_30cm, RH, Net_rad, PAR, Precip, Wind_Spd, Wind_Dir, VPD.
- Fluxes and energy terms: LE (latent heat), LE_Filled, LE_QC; Fc (CO2 net ecosystem exchange), Fc_Filled, Fc_QC; H (sensible heat), H_Filled, H_QC.
- Quality and modelling: FC_QC, LE_QC, H_QC with QC codes; Resp (modelled respiration); u* (friction velocity); MO (Monin-Obukhov stability).
- Metadata columns: Year, Month, Day, Hour, Minute, Location/Site codes, Habitat, Quadrat Number, Scale, etc.

## Data Processing and Quality Control
- Corrections: Fluxes corrected for frequency losses (WPL) and CO2 fluxes corrected for storage terms.
- Quality flags: QC flags derived from instrument diagnostics; basic reality checks with radiation-based binning; within-bin outlier removal (fluxes outside 3.5 SD or 5 SD from bin mean labeled accordingly).
- Data binning: Flux data binned into 15 populated radiation bins; flagged by QC values (0 = best, 1 = marginal, 2 = poor, 3 = very poor).
- Gap-filling: Fluxes filled using the REddyProc gap-filling package, using QC = 0 data only.
- Respiration modelling: Lloyd & Taylor (1994) respiration model fitted to nocturnal QC = 0 CO2 flux data for separate months.
- Data integrity checks: Basic diagnostics from gas analyser and anemometer; timestamps reflect half-hour periods (e.g., 00:15 denotes 00:00–00:30 interval).

## File Formats and Data Access
- Primary format: CSV.
- Time representation: Half-hour means with mid-interval timestamps; explicit notes on missing data (gaps) and NA values.
- Field descriptions: Includes extensive dataset metadata (site, habitat, scale categories, and parameter mappings) to support analysis and data discovery.

## Data Gaps and Limitations
- Gaps indicate sensor malfunctions or power loss.
- Some data may be missing or incomplete due to equipment issues; complexity of local marsh environment can affect data continuity.
- Data gaps and QC flags help identify data suitability for specific analyses (e.g., energy balance studies, gap-filled flux estimates).

## Relevance for Analysts
- Provides a rich, processed EC flux dataset suitable for examining CO2 exchange, energy fluxes, and environmental drivers in a salt-marsh ecosystem.
- Suitable for correlation analyses, model validation (e.g., respiration models), and evaluation of data quality across QC levels.
- Comprehensive metadata and standardized QC/gap-filling procedures facilitate reproducibility and data reuse in research and policy contexts.