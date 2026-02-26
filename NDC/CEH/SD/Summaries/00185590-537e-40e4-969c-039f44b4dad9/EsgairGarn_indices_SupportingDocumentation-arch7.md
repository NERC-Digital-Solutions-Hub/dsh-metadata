# Nant Esgair Garn catchment - 20 year derived statistics of rainfall, streamflow and acidity

## Overview
- 20-year record of monthly statistics (1982-04-01 to 2013-04-01) for rainfall, streamflow, and stream acidity (pH) related to the Nant Esgair Garn catchment near Llyn Brianne, Wales, UK.
- Data were collected at two Lancaster University stations and modelled to derive a consistent 20-year monthly dataset.
- Purpose: support understanding of long-term controls on aquatic biodiversity in the catchment.

## Data provenance and lineage
- Observations from a stream gauging station and a nearby water quality station installed by Lancaster University.
- 15-minute resolution observations for 2013 used to develop a dynamic model (CAPTAIN Toolbox for Matlab) to simulate the 20-year record.
- Supporting Documentation contains full site and data lineage.
- Data are vetted for Intellectual Property Rights by the NERC Environmental Information Data Centre (EIDC).

## Experimental design and sampling
- Location: Nant Esgair Garn experimental catchment (LI6) near Llyn Brianne; contributory areas ~0.57–0.69 km².
- Geology: shales, mudstones, greywackes and grits; soils include Podzols and Histosols; land cover historically moorland and improved pasture.
- Observations: streamflow and pH at 15-minute intervals in 2013; rainfall and temperature data assembled from multiple sources dating 1982–2013.
- Rainfall data: assembled from Nant Y Mean records; gaps filled using nearby raingauges (Llanerch YRFA, Swyddffynnon, Ystradffin).
- Temperature data: derived from Felindre weather station (Met Office MIDAS data).
- NAO index: sourced from public CRU datasets.
- IP rights: all data released via the Environmental Information Data Centre vetted.

## Field instrumentation and calibration
- Field instruments: a trapezoidal flume for streamflow; pressure transmitter for water level; pH sensor with digital controller; Campbell Scientific data loggers.
- Calibration: salt-dilution gauging for stage-discharge; SC200 controller recalibration every 2–3 months; periodic pH sensor calibration with standard solutions.

## Data processing and analytical methods
- Daily rainfall, streamflow, and pH models developed from observed daily data and validated within 2013.
- Modelling approach: CAPTAIN Toolbox RIVC algorithm to identify model structures and parameters; daily rainfall-to-streamflow and rainfall-to-pH models.
- Daily simulations from 1982–2013 used to derive monthly statistics.
- Software: Matlab (R2013); code examples describe statistical functions for mean, percentiles, moving averages, pulses, durations, rates, and growth indicators.

## Nature, units, and structure of recorded values
- Dataset consists of one CSV with 159 columns (columns 2–5 intentionally blank); 32 rows.
- Column meanings include various rainfall, temperature, flow, pH statistics and derived metrics (means, percentiles, moving-average features, growing season indicators, pulse counts and durations, rates, NAO-derived values, etc.).
- Temporal framing: statistics correspond to the first day of each month from 1 April 1982 to 1 April 2013; estimation periods for metrics range from 365 days to 120 days prior to sampling; many metrics are threshold-based (e.g., 75th percentile, 25th percentile).

## Quality control
- CR1000 logger data checked for erroneous values (e.g., power-failure artifacts); such values replaced with NaN in QA processes.

## Data structure and access
- File type: a single .csv containing the 20-year derived statistics.
- Documentation note: rows 2–32 correspond to statistics for the first day of each month within the 1982–2013 window.
- Author contact: Dr Nick A. Chappell (Lancaster University). ORCID: 0000-0001-6683-951X.