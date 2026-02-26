# Human impact on long-term organic carbon export to rivers

## Overview
- Presents a long-term monthly time series of dissolved organic carbon (DOC) concentration for the Thames River (1883–2014) in mg/L.
- Colour data available 1883–1990; DOC data 1990–2014; DOC before 1990 estimated via calibration with colour data.
- The study area is the River Thames basin upstream of London; basin area ~9,948 km² with a temperate, lowland, mineral-soil-dominated catchment.
- Fluvial DOC concentration shows an upward trend over the study period.
- Data are provided as one master table and one accompanying metadata file.

## Study site and collection
- Measurement sites: Hampton (DOC at ~51.42°N, 0.37°W) and Teddington (colour data, ~51.43°N, 0.33°W).
- Thames basin upstream of London contains urban centers and substantial sewage treatment works, with tertiary treatment installed at the largest 36 works since 2003.
- While urban areas are prominent, the upstream Thames basin remains predominantly rural (87.7% land area in 2007) and is geologically characterized by Cretaceous Chalk with other rock types.
- Data were collected by statutory authorities over 1883–2014.

## Measurement techniques
- Colour (1883–1974): Burgess method using a two-tube comparison with potassium dichromate/cobalt sulphate solution.
- Colour (1974–1990): Hazen units measured with absorptiometer; Hazen units correspond closely to ~2.2 Burgess units.
- DOC (1883–1905): Eudiometric method after acidification with potassium permanganate.
- DOC (1990–2014): Established under the Harmonised Monitoring Scheme (HMS).
- Data sources include Grand Junction Water Company, London Metropolitan Water Board, Thames Water Authority, Environment Agency, and data.gov.uk (for later data).

## Calibration of DOC and water colour
- Calibration for 1899–1905 used weekly samples: DOC = 0.0955 Colour + 0.2103; R² = 0.66, n = 194.
- This calibration allowed estimation of DOC from colour data for 1883–1990.
- Acknowledges non-stationarity: Worrall & Burt (2010) show DOC–color relationships shift across periods since 1974, but the study cross-validated estimates with independent DOC data (1883–1905 Grand Junction data; 1990–1998 Thames Water data; 1998–2014 EA data) and found consistency.

## Data provenance
- Data periods and variables:
  - 1883–1905: Colour, Burgess units, Grand Junction Water Company, daily (and weekly for OC in some cases).
  - 1905–1974: Colour, Burgess units, London Metropolitan Water Board, varying sampling (daily then weekly).
  - 1974–1988: Colour (Hazen units), Thames Water Authority, monthly.
  - 1974–1990: Colour (Hazen), Environment Agency, weekly to monthly.
  - 1990–1998: DOC (mg/L), Thames Water, approximately monthly.
  - 1998–2014: DOC (mg/L), Environment Agency, approximately monthly.
- Data are organized into a single table with a supporting metadata file detailing provenance, units, sampling frequency, and measuring bodies.

## Data availability and notes
- DOC data from 1990–2014 and associated colour data for 1883–1990; older data linked via calibration and cross-validation.
- The 1974 onward data are accessible via data.gov.uk (Historic UK water quality, Harmonised Monitoring Scheme).

## Key considerations for data stewards
- Documentation of measurement methods across periods is essential due to methodological changes (Burgess vs. Hazen vs. eudiometric) and unit changes.
- Calibration reliance on an assumed stationary DOC–colour relationship for 1883–1990, with acknowledgement of non-stationarity since 1974.
- Integration of multiple data sources (different organizations and time periods) requires robust provenance records, harmonized metadata, and clear data-versioning.
- Users should consider potential biases or uncertainties arising from method changes, unit translations, and the long temporal span when reusing the dataset.