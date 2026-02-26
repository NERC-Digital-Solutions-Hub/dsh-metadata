# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) wave monitoring in saltmarsh and mudflat habitats.

## Overview
- Wave parameters calculated from bottom pressure records along shore-normal transects crossing the vegetation boundary between saltmarsh and mudflat habitats.
- Staff responsible: Tom Spencer, Ben Evans.
- Sites: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands).

## Location and site context
- Essex sites (AH, FW, TM) represent contrasting habitats and sediment types (clays; marsh morphology; varied inundation).
- Morecambe Bay sites (CS, WS) represent sandy sediments with different inundation regimes and marsh structures.
- Mudflat sites differ in sediment type (cohesive clays vs. coarse, mobile sediments) and exposure.

## Data collection and instrumentation
- Monitoring approach: continuous automated recording events designed to coincide with high tide slack water.
- Sensors: pressure transducers (primarily PDCR1830; some PTX1830 for longer distances) connected to Campbell CR1000 data loggers.
- Sampling: pressure data recorded at 4 Hz during each event; events trigger 4096 measurements over ~17 minutes.
- Telemetry: data transmitted via GPRS; regular maintenance visits; manual data downloads if telemetry fails.
- Sensor details: 12 PT sensors (PT1–PT12) with associated calibration, ranges, and output types.

## Data processing and quality control
- Raw data processing: convert raw mV to pressure (Pa) using manufacturer calibrations and zero offsets; compute mean water depth from pressure time series.
- Wave parameter derivation: apply Möller et al. (1999, 2005/2006) methodology to obtain spectrally-derived total spectral energy (EPT), significant wave height (Hs), and dominant wave period (Tp) per sensor.
- Data compilation: event-level summaries organized in an Excel workbook with two sheets—All output and Filtered for reliability.
- Data quality checks and filtering:
  - Exclude periods with known equipment problems (e.g., barnacle growth on diaphragms; damaged cables).
  - Remove records where submergence indicators (PT2/PT3) suggest unreliable readings.
  - Acknowledge depth-attenuation limitations that reduce the detection of small/short-period waves at greater depths.
  - Apply validity criteria for PT4–PT8 (minimum mean depth ≥ 20 cm; Hmax/hPT ≤ 0.78) and flag records as valid (green) or not.
- Output formats: raw data retrieved in ascii .dat, processed data saved as ascii .txt; processing performed in Matlab; validation tests conducted in Excel.
- Data limitations: depth-related attenuation affects EPT estimates, particularly for mudflat sensors ahead of marsh cliffs; occasional events may not be comparable across sensors due to high-frequency loss.

## Metadata and dataset structure
- Dataset field descriptions include:
  - Site (Essex CS/WS, AH, FW, TM; Morecambe variants)
  - Habitat (Mudflat MF, Saltmarsh SM)
  - Quadrat, Scale (spatial references)
  - Record (entry order)
  - Date, Time (measurement timestamp)
  - For each PTn: ValidPTn, hPTn, EPTn, HsPTn, TpPTn
- Data quality indicators and site-specific notes accompany the dataset to support discovery and reuse.

## Data governance, sharing, and maintenance
- The dataset adheres to a documented processing and QA workflow, enabling reuse with clear provenance (sensor types, processing steps, validity criteria).
- Data are intended to be uploaded to relevant portals and catalogues for discovery and sharing.
- Ongoing maintenance considerations include sensor calibration, equipment checks (to mitigate barnacle growth and cable damage), and updating validity criteria as needed.
- Documentation includes explicit caveats about depth attenuation and site-specific limitations to support proper interpretation and interoperability.

## Key considerations for data stewards
- Ensure ongoing calibration and maintenance records are attached to the dataset to preserve data lineage.
- Maintain versioned metadata and processing scripts to support reproducibility across sites and time.
- Capture and communicate all data validity flags, including sensor-specific issues and environmental limitations.
- Promote interoperability by documenting sensor types, data formats, and processing methodologies (e.g., Möller et al. references) for future integration.