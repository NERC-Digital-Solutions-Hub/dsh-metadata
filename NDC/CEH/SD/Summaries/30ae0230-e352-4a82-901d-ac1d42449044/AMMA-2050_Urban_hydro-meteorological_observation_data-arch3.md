# Urban hydro-meteorological observation data 2016-2018  - Ouagadougou, Burkina Faso

## Summary
- Represents hydro-meteorological monitoring in Ouagadougou, Burkina Faso during 2016–2018 as part of the DFID-funded AMMA-2050 project.
- Data types: rainfall (tipping bucket), water level, and river flow (pressure level sensors and derived flows from rating curves).
- Monitoring network designed by UK Centre for Ecology and Hydrology (UKCEH); processing by UKCEH with Burkina Faso’s 2iE.
- Sites and coverage: Dam3, 2ie, Saaba, Rimkieta south, Rimkieta north, Kamboince.
- Time steps vary by site (hourly, 5–15 minutes, 5 minutes) with data start/end dates per location; includes data gaps due to equipment issues.
- Purpose: to understand hydrological function and support hydrological model development; data intended for quality assurance, transformation, analysis, and dissemination.

## Experimental design and sampling regime
- In-situ instruments:
  - Pressure level sensors (PLS) for water level measurement.
  - Tipping bucket rain gauges for rainfall (Casella models, 0.2 mm) and MFPro for spot gauging during storms.
- Sampling frequency by site:
  - Dam3: hourly depth; data 2016–2018 with monthly inspections; significant data gaps due to equipment malfunction.
  - 2ie: rainfall at 15-min intervals (2016–2018) in city center.
  - Saaba, Rimkieta South/North: PLS level (flow) at 5-min intervals (and related metadata); data start 2016 with varying end dates.
  - Kamboince: rainfall at 15-min intervals (2016–2017).
- Site context: urban catchments with mixed land use; some sites near central dam system; upstream areas vary in development density and land cover.
- Data gaps: equipment malfunctions and dry-season periods where gauges were withdrawn.

## Transformation and quality control methods
- Derivation of flows at three level-flow sites via rating curves:
  - Intermittent spot gauging of storm flows to measure velocity and depth across transects.
  - Flow from depth using cross-sectional area and measured velocity; rating curves developed for each site.
  - Outliers/erroneous measurements removed after visual inspection; final rating curves applied to time series in an Oracle database.
- Rainfall and dam level data subjected to visual inspection to remove erroneous values.
- Data processing workflow: data collected in situ, processed for QA, cleaned, transformed, and prepared for analysis and dissemination.

## Data structure and recorded values
- DataFiles: six CSV files containing time-series data plus one metadata CSV summarizing sites.
- Flow data: date_time, flow (m3/s), missing data index; minimum flow value 0 m3/s.
- Dam level data: date_time, level (mAOD), missing data index; minimum depth 0 m.
- Rainfall data: date_time, rainfall (mm), missing data index; minimum rainfall 0.2 mm per 15 min; zero values indicate no rain.
- Missing values denoted by M, representing data gaps due to equipment malfunction or QC.

## Metadata and provenance
- Metadata CSV provides site summaries and a metadata overview, including data start/end dates and units.
- Data processing and quality control performed by UKCEH; data are stored and accessible via the provided CSVs and metadata, with the processing context documented for model development and analysis.

## Data gaps and limitations
- Notable data gaps from equipment malfunction and dry-season instrument withdrawal.
- Rating curves rely on spot gauging; potential limitations in representativeness during extreme events.
- Some sites exhibit sediment/flow measurement complexities (e.g., Boulimougou dam attenuation considerations).