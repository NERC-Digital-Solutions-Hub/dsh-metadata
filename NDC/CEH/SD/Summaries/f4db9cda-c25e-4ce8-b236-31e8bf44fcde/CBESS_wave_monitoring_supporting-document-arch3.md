# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) wave monitoring in saltmarsh and mudflat habitats

## Overview
- Longitudinal dataset measuring wave parameters derived from bottom pressure records across shore-normal transects at the saltmarsh–mudflat boundary.
- Part of the CBESS initiative, focusing on coastal biodiversity and ecosystem service sustainability.

## Study sites and context
- Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS).
- Site selection aims: contrast sediment types (Essex vs. Morecambe mudflats) and, for saltmarsh sites, two soil types (clay in Essex, sandy in Morecambe) with differing inundation frequency, creek structure, and vegetation.
- Habitats: saltmarsh and mudflat, with navigation of vegetation boundaries.

## Monitoring design and data collection
- Instrumentation: an array of Druck pressure transducers (PDCR1830 and PTX1830) connected to Campbell CR1000 data loggers.
- Sampling: continuous monitoring with automated 4 Hz bursts triggered to coincide with high-tide slack water; data telemetered via GPRS.
- Recording rules: burst records 4096 measurements across all channels once inundation criteria are met.
- Maintenance: regular site visits to ensure sensor cleanliness and function; manual data downloads if telemetry fails.
- Data outputs: raw and processed data stored as ASCII (.dat and .txt) with accompanying schematics and site details.

## Variables and observations
- Per sensor (PT1–PT12) measurements include:
  - ValidPTn (sensor data validity)
  - hPTn (mean water depth during event)
  - EPTn (total spectral energy)
  - HsPTn (significant wave height)
  - TpPTn (dominant wave period)
- Metadata fields for each event: Site, Habitat, Quadrat, Scale, Record, Date, Time.

## Data processing workflow
- Raw data processing:
  - Convert raw millivolt readings to pressure (Pa) using manufacturer calibration and offsets.
  - Compute mean depth from pressure time series.
  - Apply established methodology (Möller et al.) to derive EPT, Hs, Tp.
- Event compilation:
  - Create an 'All output' dataset, then curate a 'Filtered for reliability' subset by excluding flawed records.
- Quality control steps:
  - Remove data from known equipment problems (e.g., barnacle growth on diaphragms, damaged cables).
  - Check for sensor submergence by comparing depths across adjacent sensors (PT2/PT3; PT1 where applicable).
  - Acknowledge depth-related limitations in detectability of higher-frequency components, especially at mudflat sites with deeper water.
- Validity criteria for inclusion in analyses:
  - Minimum mean depth per sensor event: at least 20 cm (to avoid exposure issues).
  - Breaking-wave check: H(max)/hPT ≤ 0.78, where H(max) = 1.86 × HsPT.
  - PT4–PT8 records meeting both criteria are flagged as valid (green); records passing criteria marked accordingly.
- Data formats and processing tools:
  - Data retrieved from loggers in ASCII, processed in MATLAB, saved as ASCII .txt.
  - Validation tests performed in Excel.
- Handling incomplete events:
  - Events may not have all sensors inundated for the full duration; per-sensor validity flags manage inclusion.

## Data quality, limitations, and caveats
- Depth-attenuation issues: deeper water reduces detectable high-frequency components, causing underestimation of EPT for some mudflat sensors (notably PT2/PT3 at AH and FW).
- Site-specific constraints: marsh cliff and limited fetch at certain mudflat sites further affect wave energy representation and comparability.
- Sensor-specific issues: occasional data gaps (e.g., PT2/PT3 submergence checks, barnacle growth) require careful filtering.
- Cross-site comparability: different depths and fetches necessitate caution when comparing EPT, Hs, and Tp across sites.

## Data management and accessibility
- Data storage: ASCII outputs and spreadsheets ('All output', 'Filtered for reliability'), with detailed field descriptions.
- Metadata and lineage: comprehensive documentation of sensor types, site locations, transect layouts, processing steps, and validity criteria.
- Public sharing: while data processing and QC are documented, explicit public data sharing policies are not stated in the dataset description; the dataset is structured for transparency and reproducibility.

## Implications for monitoring frameworks
- Demonstrates an end-to-end data lifecycle for environmental health monitoring:
  - Thoughtful site selection to capture habitat contrasts.
  - Robust, automated data collection aligned with tidal events.
  - Clear processing pipeline from raw measurements to actionable metrics (EPT, Hs, Tp).
  - Transparent quality assurance, with per-sensor validity flags and documented exclusion criteria.
  - Metadata-rich outputs enabling reproducibility and governance.
- Addresses common framework challenges:
  - Proactively tackles data gaps and metadata quality through standardized procedures and checks.
  - Reduces data silos via explicit data formats, processing steps, and validation criteria.
  - Provides a model for communicating complex findings through structured datasets and documentation.
- Potential enhancements for policy use:
  - Explicit data sharing mechanisms and governance to facilitate reuse in decision-making.
  - Continued emphasis on metadata completeness and standardized field definitions to ease cross-program comparisons.