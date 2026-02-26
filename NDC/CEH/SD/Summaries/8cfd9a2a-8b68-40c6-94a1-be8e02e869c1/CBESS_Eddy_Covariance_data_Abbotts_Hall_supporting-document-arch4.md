# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Eddy Covariance Flux Data for Abbotts Hall, Essex

## Overview
- A dataset of eddy covariance flux measurements at the Abbotts Hall site in Essex, describing energy and carbon fluxes along with meteorological variables.

## Data Content
- Variables observed
  - Meteorology: Air temperature (T_air), soil temperatures at 10 cm, 20 cm, 30 cm (T_soil_10cm, T_soil_20cm, T_soil_30cm), relative humidity (RH), net radiation (Net_rad), photosynthetically active radiation (PAR), precipitation (Precip), wind speed (Wind_Spd), wind direction (Wind_Dir), vapour pressure deficit (VPD).
  - Fluxes: CO2 flux (Fc) and CO2 flux filled (Fc_Filled), latent heat (LE) and LE filled (LE_Filled), sensible heat (H) and H filled (H_Filled), modelled respiration (Resp), U* friction velocity (ustar), Monin-Obukhov stability (MO).
  - Quality and processing: QC flags for LE, Fc, H; respiration modelling; data fill indicators.
- Temporal coverage and cadence
  - Half-hourly mean values from 15 Dec 2012 to 27 Jan 2015.
  - Fluxes and wind measured at 10 Hz; most other variables recorded at 1/60 Hz (every minute).
  - Time reference is the middle of each half-hour period (e.g., 00:15 covers 00:00–00:30).
- Site and location
  - Site: Abbotts Hall salt marsh, Essex, UK; coordinates 51°47'9"N, 0°52'1"E.
  - habitat context: sheltered embayment salt marsh with dendritic drainage, clay/organic sediments, part of a network of connected marshes.

## Instrumentation and Data Collection
- Equipment
  - Campbell Scientific data loggers and a Closed Path Eddy Covariance system (CPEC200) with CSAT3A anemometer on a 4.3 m lattice tower.
  - Air temperature/humidity sensors (Vaisala HMP155A), net radiation (Kipp and Zonen NR Lite), PAR (Skye Instruments SKP215), soil thermistors (CS 107), rain gauge (EML ARG100).
- Processing and software
  - Flux processing with EdiRe and Matlab.
  - Additional data handling with REddyProc for gap filling.
  - Additional temperature/humidity data conversion to VPD; mean half-hour values computed in Matlab.

## Data Processing and Quality Control
- Corrections and processing
  - Fluxes corrected for frequency losses (WPL corrections).
  - CO2 fluxes corrected for storage terms.
  - Gap filling performed using REddyProc (based on QC = 0 data).
- Quality control
  - QC flags derived from gas analyser and anemometer diagnostic flags; basic reality checks by radiation binning into 15 bins.
  - Within each radiation bin: fluxes beyond 3.5 standard deviations from the bin mean get QC = 1; beyond 5 standard deviations get QC = 2.
  - Data affected by tower wind shadow receive QC = 3.
  - QC = 0 indicates best quality data; QC = 1 marginal; QC = 2 or 3 poor or very poor.
- Data gaps and notes
  - Gaps indicate sensor malfunction or power loss.
  - NA cells indicate no data.
- Modelling
  - Respiration modelled using Lloyd & Taylor (1994) fitted to nocturnal QC = 0 CO2 flux data for separate months.

## Data Format and Metadata
- File format
  - CSV files.
- Metadata and schema
  - Dataset includes field descriptions and header definitions; columns include both raw and processed variables (e.g., T_air, T_soil_10cm, Fc, Fc_Filled, QC flags, etc.).
  - Headers and field descriptions available to clarify unit, scale, and meaning.
- Data organization notes
  - Time, location, site, habitat, and scale metadata provided (e.g., Site codes, Location codes, Habitat types, Quadrat/Scale definitions).

## Data Quality and Reliability
- Primary reliability factors
  - Frequency loss corrections, storage term corrections for CO2, and QC-based data filtering.
  - Gaps due to instrument/power issues; some variables recorded at higher frequency than others, requiring careful alignment during analysis.
- Documentation of data quality
  - Clear QC scheme with defined thresholds and meanings.
  - Explicit notes on data gaps and their causes.

## Implications for Data Leaders
- Data discoverability and reuse
  - Rich metadata, standardized QC flags, and documented processing steps facilitate reuse for cross-site comparisons and meta-analyses.
- Data stewardship considerations
  - Well-documented instrumentation, processing chain, and gap-filling approach support data governance and reproducibility.
  - Clear indication of data limitations (gaps, potential quality variations) informs risk assessment for analyses requiring high data completeness.
- Potential for integration
  - Dataset is part of CBESS and aligned with standard flux measurement practices, enabling integration with broader coastal biodiversity and ecosystem service assessments.