# GPS tracking data for 32 individual European nightjars on the Humberhead Peatlands NNR from 2015 - 2018

## Overview
- Dataset of latitude/longitude (WGS84) GPS fixes for 32 European nightjars.
- Collected at Thorne and Hatfield Moors, Humberhead Peatlands NNR, South Yorkshire.
- Sampling window: June–August, 2015–2018.
- Fix intervals: 3 minutes (2015–2016) and 5 minutes (2017–2018).
- Tags were archival (not transmitting) and required recapture after 7–10 days.
- Tags were calibrated to estimate location error (roughly 5–25 metres depending on habitat).

## Data and formats
- File format: CSV with columns:
  - ID: unique bird identifier
  - Date: DD/MM/YYYY
  - Year: factorial covariate for analyses
  - Time: 24-hour clock (nearest minute; typically 21:30–04:30)
  - Lat: latitude (degrees north)
  - Long: longitude (degrees east)
  - Site: Thorne or Hatfield Moors
  - Fix_int: 3 or 5 (minutes between fixes)
  - Day: tracking day number for the period 21:30–04:30
  - Days: period length used in analyses
- GPS data were manually checked for missing points; points with fewer than 3 satellites were removed.

## Methods and quality assurance
- Nightjars captured by mist nets from 21:00 to 01:00; equipped with nanoFix mini GPS tags (Pathtrack, Otley, UK).
- Tags preprogrammed with 3/5 minute schedules; archival data retrieved via recapture.
- Data checked in ArcMap to verify foraging range plausibility (points outside plausible range removed).
- Location error estimated from calibration (5–25 m depending on habitat).

## Use and aims
- Data used to:
  - Construct foraging tracks
  - Estimate home range sizes
  - Assess habitat selection
- Intended to support monitoring of behavioural responses to landscape change.
- Data were cleaned to ensure reliability for analyses and potential publication use (link to submitted manuscript on fix rate vs. tracking duration).

## Documentation and metadata
- Provides explicit definitions for each CSV column to support reuse and interoperability.
- Links to related manuscript: Mitchell et al. on trade-offs between fix rate and tracking duration for small vertebrates.
- Clear provenance: collectors and affiliations listed (including multiple authors and institutions).

## Governance, sharing, and implications for data stewards
- Dataset is clearly documented with collection sites, time window, and methods, facilitating discoverability and reuse.
- Metadata includes instrument type, calibration status, fix intervals, and quality checks, supporting data integrity assessments.
- Data are suited for repository deposition and future sharing, with explicit notes on data quality and processing steps.
- Potential considerations for updates or new releases: documentation of any additional fixes, corrections, or extended analyses beyond 2015–2018.