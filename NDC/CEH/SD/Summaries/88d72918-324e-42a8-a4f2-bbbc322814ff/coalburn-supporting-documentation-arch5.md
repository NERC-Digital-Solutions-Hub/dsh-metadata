# Coalburn Forest Research Catchment

- The Coalburn catchment (1.5 km²) in Kielder forest, Northumberland, is the UK's longest-running forest research catchment. Instrumented in 1967; conifer planting in 1972/73; mature stands with around 30% of the catchment felled since.

## Data Scope and Timeline
- 55 years of data (1967–2022) covering:
  - Precipitation
  - Discharge
  - Potential evapotranspiration (PET)
  - Other meteorological data
  - Snow depths
- Temporal resolution:
  - Hourly data available from 1993 onward
  - Mixed hourly and daily data from 1967–1993
  - Much hourly data derived from 15-minute measurements (hourly values are means or sums of 15-minute observations)
- Primary use: hydrological modelling and analysis of forest impacts on river flows
- PET data source: Eskdalemuir (45 km NW); PET calculated with Penman–Monteith; CHEPS PET values are ~10% higher

## Data Formats and File Inventory
- File formats: CSV, GEOTIFF, JPG, PNG, GPKG
- Representative file types include:
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
  - catchment.gpkg
  - dem-catch-5m.tif, catch-50m.tif, dem-50m.tif
  - landuse-2016-prelogging.tif, landuse-2018-postlogging.tif
  - aerial-image-and-boundary.png, OS-map-and-boundary.png
  - felled-forest-2016-2018.jpg, met-station-photo.jpg
- Spatial data uses GB Ordnance Survey grid coordinates (OSGB 1936/British National Grid EPSG:27700)

## Metadata, Variables and Documentation
- Time Series data describe variables in dedicated tables (e.g., Tables 1–6 for key datasets):
  - Table 1: rainfall-PET-1993-2022-daily.csv
  - Table 2: rainfall-PET-1993-2022-hourly.csv
  - Table 3: discharge-1993-2022-daily.csv
  - Table 4: discharge-1993-2022-hourly.csv
  - Table 5: metdata-1993-2022-hourly.csv
  - Tables 6–11 describe historical pre/post-1993 datasets and hourly data
  - Table 22: snow-depth-2004-2022-daily.csv
  - Table 33: water-balance-1967-2022-annual.csv
- Detailed variable descriptions include date formats, units, and the period covered (e.g., 1993–2022 for many datasets; 1967–1971 or 1976–1980 for older, specialized datasets)

## Data Quality, Processing, and Provenance
- Extensive quality control applied; datasets suitable for hydrological analysis
- Time alignment and data construction:
  - Hourly data often derived from 15-minute measurements (e.g., rainfall sums, discharge means)
  - Pre-1990 daily data aligned 09:00–08:00; post-1990 daily data aligned 01:00–00:00
- Pre-1993 precipitation (post-1990s): derived from multiple storage gauges and nearby stations; undercatch during snow events acknowledged
- Post-1993 precipitation: Environment Agency tipping bucket (TBR) gauge at site 12; corrections applied to align with storage gauges:
  - Overall adjustment: +14% to match storage gauges
  - Areal-average comparisons show ~9% difference due to gauge type and site location
  - Additional 5% adjustment accounts for wind effects; long-term average correction, not event-scale
- Infilling and adjustments:
  - Gaps infilled using readings from nearby gauges or daily totals distributed across 24 hours when necessary
  - Hourly data for 1977–1980, 1986–1989, 2015, and 2020 periods include infilling from daily data or adjacent gauges
  - Wiley Sike data used for some infilling in 2015 and 2020 with multiplicative factor to match Coalburn conditions
- Water balance:
  - 1967–2002 rainfall derived from multiple storage gauges (Birkinshaw et al. 2014)
  - 2003–2022 rainfall corrected to align with TBR-based data
  - Infilling for gaps using adjacent data sources where feasible
- Snow depth data:
  - Eskdalemuir snow depth (09:00) measured 2004–2022
- Catchment boundary:
  - Catchment boundary is precisely defined; a CEH-provided boundary file cited as incorrect and should not be used
- Land use and forestry changes:
  - Noted tree heights over time (e.g., 7 m in 1992 to ~19 m in 2014)
  - Canopy closure: 60% by 1996; entire canopy by 1996
  - Logging event: ~30% of forest felled between 2016–2018; potential hydrological effects discussed
- Data gaps and data quality notes:
  - Discharge data missing for several periods (e.g., 22/10/1972–11/7/1973; 21/12/1974–4/1/1975; 1981; 1985; 1990–1991; 2019)
  - 2010–01–14 to 2010–01–21 discharge data questionable (snowmelt effects)
  - 2013–01–07 to 2013–03–07 discharge data suspect due to subzero conditions
  - Post-2019 data gap: 26/06/2019–22/08/2019 missing
- Spatial data and units:
  - All spatial data adheres to OSGB coordinates; bounding box provided (lat 55.08943 to 55.10761; long -2.49526 to -2.46651)

## Data Gaps, Limitations and Important caveats for Stewardship
- Known missing periods in discharge data across several decades
- Some periods with questionable data quality due to environmental conditions (snowmelt, freezing temperatures)
- Boundary shapefile caution: avoid using CEH’s boundary file; use the provided catchment.gpkg boundary
- Long-term corrections for precipitation are aggregations and may not reflect instantaneous event-scale accuracy
- Land-use change (logging) occurred 2016–2018; implications for hydrology acknowledged but not quantified here
- PET data derived from Eskdalemuir with standard FAO/PM equations; CHEPS PET is higher, indicating potential alternative estimates

## Data Governance, Access, and Use Considerations
- Comprehensive metadata and descriptive documentation accompany the data, enabling discoverability and reuse
- Data are suitable for adoption into data portals and institutional catalogs, with attention to:
  - Time series provenance and data transformation steps (hourly/daily derivations)
  - Documentation of corrections, infilling, and data gaps
  - Clear noting of boundary definitions and non-use of incorrect boundary shapefiles
- Recommended practices for Data Stewards:
  - Maintain explicit versioning of time series when processing or infilling
  - Preserve and publish data provenance notes (sources, corrections, QA steps)
  - Ensure metadata remains aligned with variable definitions and units
  - Ensure spatial data uses consistent CRS (OSGB 27700) and document any reprojection decisions
  - Highlight data gaps and uncertainty due to missing periods or potential measurement issues
  - Provide context on forestry changes (logging, canopy closure) and their potential hydrological impacts
  - Cross-reference related literature (Birkinshaw et al., Robinson et al.) for methodological context

## References
- Birkinshaw, S. J., Bathurst, J. C., & Robinson, M. (2014). 45 years of non-stationary hydrology over a forest plantation growth cycle, Coalburn catchment, Northern England. Journal of Hydrology, 519, 559-573
- Robinson, M. (1998). 30 years of forest hydrology changes at Coalburn: water balance and extreme flows. Hydrological Processes, 2, 233-238
- Robinson, M., Moore, R.E., Nisbet, T.R., Blackie, J.R. (1998). From moorland to forest: the Coalburn catchment experiment. Institute of Hydrology Report no. 133