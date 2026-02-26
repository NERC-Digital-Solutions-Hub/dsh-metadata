# Meteorology, soil physics, and eddy covariance measurements of carbon dioxide, energy, and water exchange from a distributed network of sites across England and Wales, 2023 to 2024

## Overview
- Time series of land surface–atmosphere exchanges of sensible heat (H) and latent heat (LE), with supporting meteorological and soil physics data.
- Data collected at six eddy covariance (EC) flux towers across England and Wales during 2023–2024.
- Accompanied by site metadata describing each flux site’s characteristics and instruments.

## Dataset contents
- UK-SCAPE_Y6_Flux_Dataset: time series of H and LE, plus meteorological and soil data from six EC sites.
- UK-SCAPE_Y6_Site_Metadata.csv: site-level metadata including location, land use, soil type, climate, and instrument details.
- UK-SCAPE_Data_Dictionary.csv: description of variables, units, and data structure.

## Study sites and metadata
- Six flux monitoring sites covering a range of ecosystems:
  - Three croplands (two on peat, one on mineral soil)
  - One grassland on peat
  - One lowland fen under conservation management
  - One upland raised bog
- Elevation range: −2 m to 565 m above sea level.
- Mean annual temperature (MAT): 5–10 °C; Mean annual precipitation (MAP): 534–1815 mm.
- Site metadata fields include: site name, description, file name, start/end dates, land use, soil type, crop year, sensor models, measurement heights (Zm), GPS coordinates, and more.

## Data collection details
- Flux measurements: open-path EC systems measuring turbulent fluxes of H and LE above the canopy.
- Instruments: sonic anemometer, LI-7500 IRGA (CO2 and H2O concentration), data logged at 20 Hz.
- Data logging and telemetering to secure server; measurement heights vary by site (Zm fixed at most sites; raised to ~5 m for maize crops).

## Ancillary data
- Air temperature (TA) and relative humidity (RH) at 2.0 m; barometric pressure (PA) from IRGA internal sensors.
- Net radiation (NETRAD) and components (SW_IN, SW_OUT, LW_IN, LW_OUT).
- Soil heat flux (G) at 0.03 m depth; volumetric water content (SWC) at various depths; soil temperature (TS).
- Precipitation (P); water table depth (WATER_TABLE_DEPTH) where available.
- Vegetation data: canopy height, LAI, biomass; biomass samples processed to estimate carbon export; sometimes separated into plant components.

## Vegetation data
- Time-series measurements of canopy height, LAI, and biomass where applicable.
- LAI measured with LAI-2000/LAI-2200 devices; destructive biomass samples collected and processed in lab.

## Data processing, quality control (QC), and processing workflow
- Flux calculations: EddyPro software (V7.0.6) used to derive 30-minute fluxes with quality-control steps.
- Corrections applied: angle-of-attack adjustments, 2D rotation for terrain, cospectral attenuation, density corrections for humidity and air density.
- Turbulence and quality checks: 
  - Statistical outlier removal (median absolute deviation method)
  - Stationarity and turbulence tests (Mauder & Foken)
  - Turbulence thresholds (USTAR) to filter low-turbulence periods
  - Footprint analysis to ensure >80% of flux originates within target ecosystem (Kljun footprint model via FFP)
  - Visual inspection and manual cleanup of obvious errors
- Data gaps and uncertainties: QC'd EC data and ancillary data; gaps identified and flagged (-9999 when missing).

## Gap-filling and flux partitioning
- Gap-filling: Marginal Distribution Sampling (Reichstein et al., 2005) for EC (NEE, LE, H) and ancillary variables.
- Flux partitioning: 
  - NEE into gross primary production (GPP) and ecosystem respiration (Reco) using established day/night methods (Reichstein et al. 2005; Lasslop et al. 2010).
  - Implemented with REddyProc (R) and, where possible, ancillary data gap-filled using COSMOS-UK data (Cooper et al., 2021).

## Data structure and formats
- Time series data provided as separate CSV files for each of the six sites.
- Data are complete time series from START_DATE to END_DATE in UK-SCAPE_Y6_Site_Metadata.csv; missing records flagged with -9999.
- TIMESTAMP_START and TIMESTAMP_END may appear in scientific notation in some software.
- Vegetation data available as non-continuous time-series CSVs; details described in UK-SCAPE_Data_Dictionary.csv.

## Nature, units, and data provenance
- Flux, micrometeorological, and soil-physics variables described with units in UK-SCAPE_Data_Dictionary.csv.
- Measurements and processing methods referenced to established micrometeorology literature and tools (EddyPro, REddyProc) and metadata documented for traceability.

## GIS-relevant considerations
- Rich geolocation context: site coordinates, elevation, land use, soil type, and canopy/vegetation metrics suitable for spatial analysis and mapping.
- Footprint modeling information enables spatial interpretation of flux measurements and their representativeness for target ecosystems.
- Data are suitable for integration with GIS raster/vector layers (climate grids, land cover, soils) to map flux dynamics over time and space.

## Acknowledgments and references
- Data collected with landowner cooperation and funding from NERC UK-SCAPE programme; site-specific support acknowledged.
- Methodological references include Reichstein et al. (2005, 2016), Lasslop et al. (2010), Mauder et al. (2006, 2013), Moncrieff et al. (1997, 2004), Nakai et al. (2006), Papale et al. (2006), Kljun et al. (2015), and related EddyPro and REddyProc documentation.