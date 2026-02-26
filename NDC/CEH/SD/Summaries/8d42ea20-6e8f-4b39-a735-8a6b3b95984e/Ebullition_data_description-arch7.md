# Ebullition dataset (5 files), details as follows:

## Overview
- Dataset comprises 5 files in total; described as 4 MS Excel spreadsheets containing methane flux and related environmental data from two lowland floodplain fens (Sutton and Strumpshaw) collected in 2013. A ancillary metadata/description file appears to accompany the spreadsheets.

## Datasets / Data Structure
- Ebullition flux
  - Measurements of methane ebullition fluxes (mg CH4 m^-2 h^-1), methane concentration in bubbles (ppmv), and bubble volume flux (ml m^-2 h^-1) obtained using ebullition funnels.
- Chamber flux
  - Methane fluxes (mg CH4 m^-2 h^-1) measured using static chambers; data for both fens (Sutton and Strumpshaw) across 2013.
- Controlling factors
  - Means, standard deviations, and slopes for: water level relative to ground during funnel deployment; net radiation; soil temperature; air pressure; Vascular Green Area per adjacent quadrats.
  - Location: Strumpshaw and Sutton Fens.
- Environmental variables
  - Hourly measurements of soil temperature (°C), air pressure (cm), and water table depth relative to ground surface (cm).
- Location
  - Strumpshaw (1°27′E, 52°36′N) and Sutton (1°30′E, 52°45′N).
- NA entries indicate missing data; measurements span various Julian days in 2013 as described below.

## Temporal coverage
- Ebullition flux: From Julian Day 72 to 245, 2013.
- Chamber flux: From Julian Day 17 to 313, 2013.
- Controlling factors: From Julian Day 17 to 213, 2013.
- Environmental variables: From Julian Day 91 to 243, 2013.

## Spatial coverage
- Two fen sites: Strumpshaw and Sutton Fens.
- Measurements were collected within 0.04 km² at each site.
- Coordinates provided for site localization; suitable for point or small-area GIS representations.

## Measurements, units, and data quality
- Methane and related fluxes measured via field instruments (funnels and static chambers) and analyzed with gas chromatography (FID).
- Calibration: instrument calibration with certified gases; routine calibration runs.
- Precision (relative standard deviation): ~6% for CO2 and ~7% for CH4.
- Data fields:
  - Ebullition flux measurements and components (flux, methane concentration, bubble volume flux).
  - Chamber flux measurements (mg CH4 m^-2 h^-1); NA indicates missing data.
  - Controlling factors as summary statistics (means, SDs, slopes) of environmental/water-level metrics.
  - Hourly environmental variables (soil temperature, air pressure, water level).

## Field methods and QA
- Protocols from Defra SP1210: Lowland Peatland Systems in England and Wales.
- Field apparatus: 12 inverted glass funnels per site (ebullition) and 6 tall static chambers per site (chamber flux).
- Vegetation: Phragmites australis-dominated area; measurements within 0.04 km² per site.
- Meteorological and hydrological monitoring: automatic weather station (MiniMet) and Levelogger pressure transducers; monthly calibration dips.
- Vascular Green Area monitored non-destructively within chamber collars (Wilson et al., 2007).
- Full instrumentation details available in Stanley, KM (2015) PhD thesis; download link provided in the dataset description.

## Data usage notes for GIS specialists
- Suitable for creating map-based data products showing spatial patterns of methane fluxes and environmental controls across the two fens.
- Can be developed into multiple GIS layers:
  - Ebullition flux layer (point or small-area polygons around funnel locations).
  - Chamber flux layer (point locations corresponding to static chambers).
  - Controlling factors layer (statistical summaries linked to deployment periods).
  - Environmental variables layer (hourly time series georeferenced to site locations).
- Temporal dimension: combine with deployment windows (Julian days) to create time-enabled visualizations and analyses.
- Data quality considerations: missing values (NA), differences in measurement windows across datasets, and the need to harmonize units and time references for integrated analyses.

## Provenance and contact
- Field and laboratory methods grounded in Defra SP1210 protocols.
- Related literature cited: Wilson et al. (2007); Stanley (2015) PhD thesis.
- For queries: Kate Heppell (c.m.heppell@qmul.ac.uk).