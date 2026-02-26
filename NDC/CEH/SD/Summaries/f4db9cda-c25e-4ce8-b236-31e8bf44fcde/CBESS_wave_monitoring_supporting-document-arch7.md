# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) wave monitoring in saltmarsh and mudflat habitats

## Overview
- A dataset of wave parameters derived from bottom pressure records along shore-normal transects crossing the vegetated–unvegetated boundary between saltmarsh and mudflat habitats.
- Sites represent contrasting habitats and sediment/soil types in two regions: Essex (saltmarsh with clay soils) and Morecambe Bay (saltmarsh with sandy soils); mudflat sediments differ between sites.
- Designed to support GIS-based visualization and analysis of coastal hydrodynamics and ecosystem services.

## Location and Habitat Details
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS).
- Habitat types: Mudflat (MF) and Saltmarsh (SM); soils include clay (Essex) and sand (Morecambe Bay).
- Coordinates (approximate):
  - AH: 51.78°N, 0.87°E
  - FW: 51.82°N, 0.97°E
  - TM: 51.69°N, 0.93°E
  - CS: 54.17°N, 3.00°W
  - WS: 54.13°N, 2.80°W

## Data Collection and Processing
- Continuous monitoring with automated high-tide (still water) events; pressure transducers record at 4 Hz during events.
- Sensor array: PT1–PT12 (types include PDCR1830 and PTX1830), wired to Campbell CR1000 data loggers.
- Data workflow:
  - Raw mV data converted to pressure (Pa) using calibration data and offsets.
  - Mean depth per sensor computed and converted to depth (hPTn) using a depth equation.
  - Spectrally-derived total energy (EPTn), significant wave height (HsPTn), and peak period (TpPTn) calculated (per Möller et al. methodology).
- Data stored as ASCII .dat, processed in Matlab, saved as .txt; validation performed in Excel.

## Variables Observed
- For each sensor PT1–PT12: 
  - ValidPTn (0/1)
  - hPTn (mean water depth, m)
  - EPTn (total spectral energy)
  - HsPTn (significant wave height, m)
  - TpPTn (dominant wave period, s)
- Metadata fields cover Site, Habitat, Quadrat, Scale, Date, Time, and Record identifiers.

## Data Quality Control and Filtering
- Two main data sets: All output vs. Filtered for reliability.
- Filtering steps:
  - Remove data during known equipment problems (e.g., barnacle growth, damaged cables).
  - Exclude records with submergence issues by assessing PT2/PT3 depth consistency; remove implausible events.
  - Acknowledge depth-attenuation: tall depth reduces high-frequency components, biasing EPT especially at mudflat sensors AH and FW.
  - Apply continuous-inundation criteria: minimum mean depth (≥20 cm) and breaking-wave criterion (Hmax/hPT ≤ 0.78).
  - PT4–PT8 records marked with green if valid; validity flags (0/1) indicate suitability for analysis.
- Limitations documented: depth-related attenuation, limited fetch at some sites, and potential non-detection of certain short-period waves.

## Dataset Format and Access
- Formats:
  - Primary: ASCII .dat files (per event)
  - Processed: ASCII .txt files (Matlab workflow)
  - Validation: Excel spreadsheets (All output and Filtered for reliability)
- Output includes per-event sensor data, including validity flags and spectral parameters.

## GIS-Specific Considerations
- Spatially explicit data: sensor locations along shore-normal transects with site-, habitat-, and boundary-crossing context.
- Suitable GIS outputs:
  - Layered point data for PT1–PT12 with attributes: hPTn, EPTn, HsPTn, TpPTn, ValidPTn.
  - Site-level and habitat metadata (Essex vs Morecambe Bay; mudflat vs saltmarsh; soil types).
  - Time-enabled layers showing wave energy and significant wave height across events.
  - Data quality indicators (validity flags, notes on attenuation and sensor issues).

## Practical Notes for Visualization and Analysis
- Expect depth- and location-dependent biases in energy estimates, especially at deeper mudflat sites near marsh cliffs.
- Some events may lack data from certain sensors due to inundation patterns or sensor issues; use ValidPTn flags to filter analyses.
- When combining across sites, consider differences in inundation frequency, vegetation, and fetch which influence wave measurements.

## Additional Context
- Observations and processing rely on established methodologies (Möller et al. 1999; Möller 2006) and cross-site calibration considerations.
- Data quality rationale emphasizes reproducibility and transparency for downstream GIS analyses and map-based data products.