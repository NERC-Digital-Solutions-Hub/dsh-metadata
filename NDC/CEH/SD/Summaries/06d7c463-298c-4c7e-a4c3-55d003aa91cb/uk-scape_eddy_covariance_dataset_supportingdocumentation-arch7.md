# Meteorology, soil physics, and eddy covariance measurements of carbon dioxide, energy, and water exchange from a distributed network of sites across England and Wales, 2018-2023

## Overview for GIS specialists
- The UK-SCAPE Eddy Covariance dataset provides time series of land surface–atmosphere exchanges (sensible heat H, latent heat LE) plus supporting meteorological, soil physics, and vegetation data from ten EC flux tower sites across England and Wales.
- Data are organized into site metadata, per-site flux and ancillary data files, vegetation data, and a data dictionary.

## Spatial coverage and study sites
- Ten flux monitoring sites spanning a range of land uses: two croplands, four managed grasslands, one cropland converted from grassland, two lowland fens, and a upland blanket bog.
- Elevation from -2 m (below sea level) to 565 m above sea level; mean annual temperature 5–10 °C; annual rainfall 534–1815 mm.
- Site metadata file: UK-SCAPE_Site_Metadata.csv describing each site (ID, name, start/end dates, land use, soil type, coordinates, and instrument models).

## Data structure and file organization
- Time series data are provided as separate CSV files per site in three categories:
  - Flux data (H, LE, NEE, etc.)
  - Ancillary data (TA, RH, NETRAD, G, SWC, P, water table depth, etc.)
  - Vegetation data (Biomass; Canopy height and LAI)
- File naming format for flux/ancillary data: <SITE_ID>_<SOIL_TYPE>_<LAND_USE>_<START_DATE>_<END_DATE>.csv
- Vegetation data: UK-SCAPE_Biomass.csv and UK-SCAPE_Canopy_Height_LAI.csv
- Data dictionary: UK-SCAPE_Data_Dictionary.csv describes variables and units.

## Variables and units
- Variables cover fluxes (H, LE, NEE), micrometeorology (TA, RH, PA, NETRAD, SW_IN/OUT, LW_IN/OUT), soil physics (G, SWC, TS, WATER_TABLE_DEPTH), precipitation (P), and vegetation metrics (CANOPY_HEIGHT, LAI), with associated sensor depths where applicable.
- Missing data flagged as -9999; non-applicable metadata as NA.

## Temporal coverage and sampling
- Continuous flux, meteorological, and soil measurements for periods defined by START_DATE and END_DATE in UK-SCAPE_Site_Metadata.csv.
- Vegetation data are non-continuous time series where available.
- Raw EC data at 20 Hz; fluxes and 30-minute means derived via processing.

## Instrumentation and measurement details
- Fluxes measured above canopy using open-path EC systems: sonic anemometer + LI-7500 IRGA.
- Sensor heights varied by site (Zm; fixed at most sites; raised for maize in croplands).
- Ancillary data include air temperature, humidity, barometric pressure, net radiation (and components), soil heat flux, soil moisture/temperature, precipitation, and water table depth at peatlands.

## Data processing and quality control
- Flux processing performed with EddyPro software (version 7.0.6) to produce 30-minute flux averages.
- Quality control includes: outlier removal (MAD method), stationarity and turbulence tests, multiple USTAR thresholds, and footprint checks to ensure ≥80% of flux within target ecosystem.
- EddyPro adjustments for tilt, coordinate rotation, spectral corrections, density corrections, etc.
- Visual QC: all flux and ancillary data plots reviewed; clearly erroneous values removed.

## Gap-filling and flux partitioning
- Gaps in fluxes and ancillary/derived data filled using Marginal Distribution Sampling (Reichstein et al., 2005).
- Partitioning NEE into GPP and RECO using established day/night methods (Reichstein et al., Lasslop et al., 2010) with REddyProc (R package).
- Where possible, ancillary data gap-filled using co-located COSMOS-UK sites.

## Vegetation data
- Biomass data (Lab moisture content, dry biomass weight) used to estimate carbon export at harvest (C_EXPORT) where applicable.
- Canopy height and LAI measurements obtained via manual methods and LAI-2000/LAI-2200 devices.

## Metadata, provenance, and access
- Metadata include site coordinates (latitude/longitude in decimal degrees), soil type, land use, measurement heights, instrument models, and measurement windows.
- Data provenance includes COSMOS-UK and other funding sources; detailed references and author contributions provided.
- Data are structured for GIS workflows: per-site spatial metadata, time-stamped measurements, and explicit variable definitions.

## Practical GIS considerations
- Spatial alignment via site coordinates in UK-SCAPE_Site_Metadata.csv; use for mapping site locations and footprint validation.
- Time-series data are per-site; best for layering over base maps with temporal analysis (e.g., seasonal CO2 exchange, energy balance components).
- Data quality flags are embedded in processing outputs; apply QC screening when integrating into GIS analyses.
- Data gaps and gap-filled values should be treated with appropriate uncertainty considerations in spatial analyses and visualizations.

## Summary of relevance for GIS work
- Provides a high-quality, site-level, time-resolved dataset of land-surface fluxes and supporting variables across a representative UK landscape.
- Rich metadata and standardized file naming facilitate batch ingestion, spatial joins, and temporal analyses in GIS.
- Suitability for mapping spatial patterns of fluxes, energy balance components, and vegetation influences across diverse ecosystem types.