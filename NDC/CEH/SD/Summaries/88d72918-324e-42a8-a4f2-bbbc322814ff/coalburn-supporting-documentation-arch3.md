# Coalburn Forest Research Catchment

- The Coalburn catchment in Kielder forest, Northumberland, is the UK’s longest-running forest research catchment. Instrumented in 1967; a conifer forest was planted in 1972/73; about 30% of the catchment has since been felled. The dataset covers 55 years (1967–2022) with extensive meteorological, hydrological, snow-depth, and PET data, suitable for hydrological modelling and analysis of forest impacts on river flows.

## Data coverage and content

- Time series span: 1967–2022 (precipitation, discharge, PET, other meteorological data, snow depths); hourly data from 1993 onward; mix of hourly and daily data before 1993.
- Primary variables: rainfall/precipitation, discharge (flow), potential evapotranspiration (PET), air temperature, humidity, wind, radiation, snow depth, and water balance components.
- PET is computed via the Penman–Monteith method; meteorological data are sourced from Eskdalemuir (≈45 km NW) for PET and related variables.
- Data quality-controlled and suitable for hydrological modelling or analysis of forest effects on river flows.

## File formats and data products

- Data files (examples): 
  - rainfall-PET-1993-2022-daily.csv
  - rainfall-PET-1993-2022-hourly.csv
  - discharge-1993-2022-daily.csv
  - discharge-1993-2022-hourly.csv
  - metdata-1993-2022-hourly.csv
  - rainfall-discharge-PET-1967-1971-daily.csv
  - rainfall-discharge-PET-1976-1980-daily.csv
  - rainfall-discharge-PET-1986-1989-daily.csv
  - rainfall-discharge-March1977-July1978-hourly.csv
  - rainfall-discharge-January1986-December1989-hourly.csv
  - rainfall-discharge-June1979-December1980-hourly.csv
  - snow-depth-2004-2022-daily.csv
  - water-balance-1967-2022-annual.csv
- Spatial data:
  - catchment.gpkg (Geopackage boundary)
  - dem-catch-5m.tif, catch-50m.tif, dem-50m.tif (DEM at various resolutions)
  - landuse-2016-prelogging.tif, landuse-2018-postlogging.tif
- Additional context:
  - Aerial and OS map visuals; felled forest imagery; station photos
- Coordinate system: GB Ordnance Survey grid (OSGB 1936, EPSG:27700)

## Time conventions and data construction

- Pre-1990: daily data recorded 09:00–08:00; example 13/12/1977 covers 12/12/1977 09:00 to 13/12/1977 08:00.
- Post-1990: daily data recorded 01:00–00:00; hourly data (when from 15-minute intervals) derived by aggregating 15-minute measurements (e.g., hourly discharge is the mean; rainfall is the sum).
- Post-1993: precipitation data primarily from Environment Agency tipping-bucket gauge at site 12; adjustments applied to align with areal precipitation estimates.

## Data quality, gaps, and quality control

- General QC: extensive quality control; some periods with missing or questionable data identified (see discharge gaps and specific date ranges below).
- Discharge data gaps: 22/10/1972–11/7/1973; 21/12/1974–4/1/1975; 1/10/1981–13/10/1981; 5/12/1985–16/12/1985; 18/6/1990–1/7/1991; 4/12/1991–16/12/1991; 26/6/2019–22/08/2019 missing.
- Specific questionable periods for discharge (e.g., 2010 mid-January to late January; 2013 early year subzero/ freezing conditions).
- Pre-1993 precipitation: reconstructed from monthly storage gauges within the catchment, disaggregated using nearby daily rainfall stations (Spadeadam, Bower, Chirdon, Kielder Dam); undercatch during snow events acknowledged.
- Post-1993 precipitation: EA tipping-bucket data at site 12, corrected to be consistent with areal precipitation estimates; 9% long-term consistency adjustment (and wind-adjustment factor of ~5% for certain conditions) to align with historical records.
- Infill and adjustments: selective infilling of hourly data using nearby gauges (Wiley Sike data) and daily rainfall data where gaps existed; infilling is documented and limited to periods with available guidance.
- Water balance and annual totals: rainfall data up to 2003 harmonized with Birkinshaw et al. (2014) work; post-2003 totals rely on corrected TBR data with overlap-based corrections.
- Boundary correctness: catchment boundary is well-defined due to 1967 instrumentation and ditching; a different boundary shapefile from CEH should not be used.

## Spatial context and land cover

- Landscape evolution: forest canopy closure progressed through the 1990s; logging activity between 2016–2018 removed ~30% of the forest.
- Tree height history: ~7 m (1992) to ~19 m (2014) with canopy closure by the mid-1990s.
- Land use change captured via pre- and post-logging rasters; forest vs grass classifications provided.

## Data governance, metadata, and sharing

- Metadata quality varies; some datasets require direct contact with dataset originators to verify provenance and characteristics.
- Data are publicly shareable with appropriate governance, but some historical data may have constraints or depend on provenance notes.
- Clear data lineage and transformation notes are provided for many files, aiding reproducibility and governance.

## Limitations and caveats

- Multiple data gaps across decades; specific months/years with missing or suspect measurements.
- Pre-1993 rainfall reconstruction relies on nearby stations; potential undercatch and spatial variability remain sources of uncertainty.
- Post-1993 corrections introduce long-term calibration factors that may not hold at event scales.
- Some spatial boundary data require caution: not to rely on alternative boundary file due to known inaccuracies.

## Use cases for monitoring frameworks and policy

- Long-term hydrological response of a forested catchment to growth, logging, and climatic variation.
- Evaluation of measurement strategies, data gaps, and governance needs for monitoring programmes.
- Baseline for non-stationary hydrology analyses and forest-hydrology interaction studies.
- Data-driven support for modelling river flows, flood risk, and catchment water balance under management scenarios.

## References

- Birkinshaw, S. J., Bathurst, J. C., & Robinson, M. (2014). 45 years of non-stationary hydrology over a forest plantation growth cycle, Coalburn catchment, Northern England. Journal of Hydrology, 519, 559-573.
- Robinson, M. (1998). 30 years of forest hydrology changes at Coalburn: water balance and extreme flows. Hydrol. Earth Syst. Sci. 2, 233-238.
- Robinson, M., Moore, R.E., Nisbet, T.R., Blackie, J.R. (1998). From moorland to forest: the Coalburn catchment experiment. Institute of Hydrology Report no. 133.