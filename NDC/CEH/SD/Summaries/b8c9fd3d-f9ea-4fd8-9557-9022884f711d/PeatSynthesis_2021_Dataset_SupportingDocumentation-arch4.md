# Net ecosystem CO2 exchange and meteorological observations collected at peatland ecosystems across Wales, Scotland and England, 2008 to 2020

## Overview
- Time series of land surface–atmosphere net ecosystem CO2 exchange (NEE) and supporting micrometeorological data.
- Collected at thirteen peatland eddy covariance (EC) flux sites across Wales, Scotland and England.
- Sites were active at different times from 2008 to 2020; subset of variables provided in the UK_Peatlands_NEE_Flux_Dataset.zip as supplementary material to Evans et al. (in press).
- Full range of variables available via Environmental Data Centre (EIDC) records or by contacting the authors.

## Study sites
- thirteen peatland EC flux observation sites covering a range of semi-natural and managed peatlands, including blanket bogs, valley fens, and agricultural peatlands.
- Geographic spread across Wales, Scotland and England; site types include ombrogenous upland bogs and cropland/grassland–intensively managed peatlands.
- Site coordinates are not included in the dataset for security reasons; coordinates can be obtained by contacting the authors.
- Table 1 (described in the document) provides site descriptions, start/end dates, and references for each site (e.g., Crosslochs, Conwy, Moor House, Auchencorth Moss, Cairngorms, Anglesey sites, Wicken/Fen, Bakers/Fen, Tadham Moor, Redmere, Rosedene).

## Data collection and sampling regime
- Automated flux and meteorological measurements provided for different time intervals across 2008–2020.
- Turbulent fluxes of NEE measured above the canopy using eddy covariance (EC) systems.
- Raw data include 20 Hz measurements of wind components, sonic temperature, water vapour density, and CO2 density; additional meteorological measures include air temperature (TA), relative humidity (RH), and incoming shortwave radiation (SWIN) at specified heights.
- Instrumentation details are site-specific (e.g., Zm height, datalogger type, sensors for CO2, HR, SWin) and summarized in Table 2.

## Flux data processing and quality control
- Fluxes computed as 30-minute block-averaged flux densities using EddyPRO® Flux Calculation Software.
- Processing includes:
  - QC of 20 Hz data (outliers, plausible ranges)
  - Angle-of-attack correction for certain sonic anemometers
  - Coordinate rotation to align with local terrain
  - Corrections for high/low-frequency co-spectral attenuation
  - Corrections for humidity effects on sensible heat flux and density effects on latent heat and CO2 fluxes
- Positive NEE fluxes indicate CO2 source to the atmosphere; negative fluxes indicate uptake.
- Quality control performed by data providers, including:
  - Removal of statistical outliers and data during unfavourable conditions or low turbulent mixing
  - Footprint assessment to ensure representativeness (≥80% flux originating within target ecosystem) using the ART Footprint Tool
  - Weekly visual checks to remove clearly erroneous values
- Data gaps and uncertainty addressed in subsequent processing steps.

## Data gap-filling and flux partitioning
- Gaps in EC data (LE, H) filled using Marginal Distribution Sampling approach via REddyProc in R.
- Longer gaps at Crosslochs site filled with a generalised additive model.
- NEE partitioned into component fluxes (e.g., assimilation vs. respiration) using established methods referenced in the dataset documentation.

## Biomass fluxes for agricultural peatland sites
- Table 3 summarizes imports/exports of biomass for grassland and cropland peatlands (positive values = exports, negative = imports).
- Includes site-specific data (e.g., Tadham Moor, Redmere Farm, Rosedene Farm) across multiple years and crops (hay, lettuce, maize, sugar beet, potato, etc.).
- Data obtained from direct measurements and/or farm records.

## Data structure and units
- Time series data delivered as separate CSV files for each of the thirteen sites.
- Data cover the full site-specific time windows; missing records marked as -9999.
- Key variables and units (examples):
  - DateTime: dd/mm/yyyy HH:MM
  - NEE: g CO2-C m^-2 d^-1 (gap-filled daily sums; positive = source)
  - NEEunc: g CO2-C m^-2 d^-1 (2 SD)
  - TA: degrees Celsius
  - VPD: hPa (vapour pressure deficit)
  - SWIN: W m^-2
- The dataset in the zip is a subset; full variable range is available via EIDC or by contacting authors.

## Access, metadata, and usage notes
- Full range of variables for each site is accessible via Environmental Data Centre (EIDC) records and/or by contacting the authors.
- The document provides substantial metadata, instrumentation details, processing steps, quality-control criteria, and data provenance to support reproducibility and cross-site comparisons.
- Coordinates and some site-specific details require direct inquiry to the authors due to security considerations.

## Acknowledgments and references
- Supported by Defra (Projects SP1210 and SP1218) and additional support from UK NERC, Scottish Government, NRW, and other programs.
- Methods and tools referenced include EddyPRO, footprint analyses, QC standards, REddyProc, and related literature on eddy-covariance processing and peatland CO2 flux research.