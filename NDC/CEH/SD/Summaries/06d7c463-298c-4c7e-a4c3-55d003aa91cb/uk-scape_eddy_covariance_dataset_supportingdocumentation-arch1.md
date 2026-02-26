# Meteorology, soil physics, and eddy covariance measurements of carbon dioxide, energy, and water exchange from a distributed network of sites across England and Wales, 2018-2023

## Overview
- UK-SCAPE Eddy Covariance dataset provides time series of land surface–atmosphere exchanges of sensible heat (H) and latent heat (LE), plus supporting meteorological, soil physics, and vegetation data.
- Collected at ten eddy covariance (EC) flux tower sites across England and Wales (2018–2023).
- Includes site metadata, site-specific flux and ancillary data, vegetation data, and a data dictionary.

## Dataset contents
- Site metadata file: UK-SCAPE_Site_Metadata.csv
- Flux and ancillary data: one file per site (site-specific CSVs)
- Vegetation data: UK-SCAPE_Biomass.csv and UK-SCAPE_Canopy_Height_LAI.csv
- Data dictionary: UK-SCAPE_Data_Dictionary.csv

## Study sites
- Ten EC flux monitoring sites with diverse land uses:
  - Croplands (including drained lowland peat)
  - Managed grasslands (peat and mineral soils)
  - Cropland converted from grassland
  - Lowland fens under conservation management
  - Upland blanket bog
- Elevation range from 2 m below sea level to 565 m above sea level.
- Mean annual temperature: 5–10 °C; mean annual precipitation: 534–1815 mm yr−1.
- Metadata fields include site name, ID, file naming, start/end dates, land use, soil type, and sensor/model details.

## Data collection and instrumentation
- Flux data:
  - Open-path eddy covariance system measuring with a sonic anemometer and LI-7500 IRGA.
  - Observations at 20 Hz, logged to a CR3000 Micrologger and telemetered.
  - Turbulent fluxes (H and LE) computed as 30-minute block averages.
  - Measurement heights (Zm) varied by site; croplands had Zm increased during maize production.
- Ancillary data:
  - Air temperature (TA) and relative humidity (RH) at 2.0 m; barometric pressure from IRGA; NETRAD and SW components; soil heat flux (G); soil moisture (SWC) and temperature (TS); precipitation (P); water table depth (peatlands).
  - Data logged at high frequency and aggregated to 15–30 minute means.
- Vegetation data:
  - Biomass (destructive sampling when possible) and canopy height/LAI measurements.
  - Biomass used to estimate carbon export (C_EXPORT); crop yields and dates obtained where available.

## Instrument calibration
- Sensors repaired or replaced as faults detected.
- Gas analysers calibrated per manufacturer specifications; in-house or manufacturer calibration as available; details available on request.

## Nature and units of recorded values
- Flux, ancillary, and vegetation variables and units described in UK-SCAPE_Data_Dictionary.csv.
- Missing data indicated as -9999; non-applicable metadata as NA.

## Flux data processing and quality control
- Fluxes computed with EddyPro software (v7.0.6) using 30-minute averaging.
- QC steps:
  - Outliers removed using median absolute deviation criteria.
  - Stationarity and turbulence tests applied (Mauder & Foken 2006).
  - Periods of low turbulence filtered with USTAR thresholds.
  - Footprint assessment with the FF P tool; fluxes considered representative if >80% originated within target ecosystem.
  - Visual QA with manual inspection and removal of clearly erroneous values.

## Gap filling and flux partitioning
- Gaps in EC fluxes (LE, H, NEE) and ancillary/derived data filled using Marginal Distribution Sampling (Reichstein et al., 2005).
- NEE partitioned into GPP and RECO using day/night approaches (Reichstein et al., 2005; Lasslop et al., 2010).
- Gap filling and partitioning performed with REddyProc (R).
- Ancillary data gap-filled using co-located COSMOS-UK data where possible.

## Data structure and access
- Time series data provided as separate CSV files per site; vegetation data as non-continuous time series.
- File naming for flux and ancillary data: <SITE_ID>_<SOIL_TYPE>_<LAND_USE>_<START_DATE>_<END_DATE>.csv
- Data dictionary explains variables; missing values and metadata follow -9999 and NA conventions, respectively.

## Data provenance, usage, and acknowledgments
- Data acquisition supported by NERC award NE/R016429/1 (UK-SCAPE) and Defra SP1219 Lowland Peatlands Phase 2; additional site support from various organizations.
- Authors acknowledge landowners and site managers for access to flux towers.
- References provided for QC, processing, and methods (e.g., Reichstein et al., Mauder & Foken, Moncrieff et al., Laslop et al., Kljun et al.).