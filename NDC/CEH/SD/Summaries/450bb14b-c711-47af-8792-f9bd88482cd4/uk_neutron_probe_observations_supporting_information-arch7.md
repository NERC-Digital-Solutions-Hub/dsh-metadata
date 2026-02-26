# Collated neutron probe measurements and derived soil moisture data, UK, 1966-2013: Supporting Information

- The UK Soil Moisture Databank (UKSMD) compiles neutron probe (NP) soil moisture observations and derived data for hundreds of UK locations, spanning 1966–2013.
- Data cover 428 locations across 45 study areas with NP observations at 112 sites and 441 tube locations (Northern Ireland has no recovered observations).
- Data products include:
  - Neutron probe count rate (R) and volumetric soil moisture (θ) at various depths.
  - Depth-integrated profile moisture content (PMC) to specified depths.
  - Comprehensive metadata and links to relevant publications.
- Spatial information is provided in Great Britain national grid (Easting/Northing) and latitude/longitude.

## Dataset structure

- Four CSV files total, two data files and two metadata files:
  - Volumetric_soil_moisture_UKSMD.csv: Time-series of NP count rate R and volumetric soil moisture θ at multiple depths.
  - Profile_moisture_content_UKSMD.csv: Time-series of depth-integrated profile moisture content (PMC) in two formats (PMC1: m water in soil to depth zn; PMC2: m3 water per m3 soil).
  - Tube_metdata_UKSMD.csv: Tube-level metadata (name, location, dates, depths, vegetation, land-use, soil type, geology, coordinates, start/end dates, depth availability, etc.).
  - Site_publications_UKSMD.csv: Publications and reports linked to each site/area, with URLs/DOIs when available.
- Units and data formats are provided in Tables 1–3 of the document; all data are CSV for easy import into GIS, R, Python, etc.

## Data production and recovery

- UKSMD consolidates older SMDB data (Gardner, 1981; 1960s–1980s) with more recent NP data (up to 2013) from various sources (spreadsheets, databases).
- Old data recovered from magnetic tapes and reprocessed; all data and metadata quality controlled and converted to SI units.
- The dataset combines NP counts (R) and derived θ, plus PMC values, to maximize temporal and spatial continuity from 1966–2013.
- The effort spans 441 tube locations in 45 study areas across England, Wales, and Scotland.

## Data contents and methods

- 3.2.1 Neutron probe readings (NP counts)
  - NP measurements are made by lowering a probe into access tubes; readings apply to a surrounding soil sphere (roughly 0.2–0.3 m radius).
  - NP counts (R) and water counts (Rw) are the primary inputs for deriving moisture.
- 3.2.2 Volumetric soil moisture (θ)
  - θ is derived from R using a calibration equation θ = a(R/Rw) + b, with site-calibrated or Wallingford calibration constants.
  - Topsoil readings (<15–20 cm) are often excluded due to neutron escape; where θ is missing, it may be reconstructed using calibration equations.
  - About 73% of observations have recovered R and Rw with θ; about 78% have θ recovered.
- 3.2.3 Depth-integrated profile moisture content (PMC)
  - PMC_i values are computed from θ_i and layer factors Fi, representing water content over vertical soil layers.
  - PMC is provided from surface to specified depths or to the maximum measured depth; when PMC is not originally available, it is derived using standard formulas.
  - PMC values are reported as PMC1 (mm water) and PMC2 (m3 water/m3 soil).

## Data availability and spatial coverage

- Data cover 45 geographic areas (AREA_ID) with varying numbers of sites and NP tubes per area; a map (Figure 1) shows NP tube locations and years of data availability.
- Summary of data availability:
  - 428 NP tube locations with observations, across 112 sites in 45 areas.
  - No observations from Northern Ireland.
- Metadata tables provide detailed area, site, and tube information, including coordinates in GB grid and geographic coordinates, start/end dates, vegetation, land use, soil type, and geology.

## Metadata details

- Tube_metadata_UKSMD.csv includes:
  - TUBE_ID, TUBE_NAME, AREA_ID, AREA_NAME, SITE_ID, SITE_NAME
  - Coordinates: EASTING, NORTHING, LATITUDE, LONGITUDE
  - Dates: TUBE_START_DATE, TUBE_END_DATE
  - Data availability: DEPTH_SPECIFIC, DEPTH_INTEGRATED, MAX_DEPTH
  - ALTITUDE, VEGETATION, LAND_USE, SOIL_TYPE, GEOLOGY, CALIBRATION_COMMENT, TUBE_COMMENT
- Site_publications_UKSMD.csv includes:
  - AREA_ID, SITE_ID, REFERENCE, URL/DOI, REFERENCE_COMMENT
- Data files use -1 to indicate missing data; recalculated θ values are flagged with COMMENT = 'c' when provided or estimated.

## Quality control and uncertainty

- Missing data are flagged; quality flags are used:
  - QUALITY1: 1 if θ values exceed 1.0 (possible overestimation in peat soils or high rainfall regions); otherwise 0.
  - QUALITY2: 1 for jumps/spikes in time series that are questionable, otherwise 0.
- Caution: NP-derived θ is better for detecting moisture changes than for absolute soil moisture; calibration uncertainties contribute to absolute-value uncertainty, especially when site-specific calibration is unavailable.
- Around 20%–30% uncertainty in θ can occur depending on R and calibration method; values with potential high uncertainty are flagged as q1 or q2.
- For some tubes where calibration data are missing, θ values are reconstructed using generalized calibration formulas (flagged as 'c'), indicating higher uncertainty.
- Top 10 cm soil moisture is less reliable for comparison with satellite or cosmic-ray sensors.

## How to use the UKSMD data (GIS-relevant guidance)

- Format and accessibility
  - Data are provided in CSV format, suitable for import into GIS workflows and spatial analyses.
  - Coordinates are available in GB National Grid and geographic coordinates, enabling precise georeferencing and mapping of NP tubes and study areas.
- Data products for GIS analyses
  - Time-series θ by depth for each tube/location allows creation of vertical moisture profiles and spatial maps of moisture gradients.
  - PMC time-series provides depth-integrated moisture content up to specified depths, useful for regional water-balance analyses.
  - Metadata enables spatial joins to site attributes (vegetation, land use, soil type, geology, altitude) for stratified analyses.
- Applications
  - Integration with hydrological and land-surface models, including data assimilation and validation against remote sensing products (ISMN, COSMOS-UK, etc.).
  - Historical drought analysis and soil-moisture variability studies spanning 1966–2013, including the 1976 drought period.
  - Studies on moisture sensitivity to vegetation, land use, and soil types across UK landscapes.
- Usage notes
  - Acknowledge original publications and data sources when using UKSMD data in GIS analyses.
  - Use quality flags (q1, q2) and the 'COMMENT' field to conduct sensitivity analyses by including/excluding suspect data.
  - When comparing with EO soil moisture products, be aware NP measurements are less reliable in the top 10 cm and calibration uncertainties exist.

## Acknowledgements and references

- Data recovery and analysis supported by NERC-CEH Water Programme and FP7 MELODIES project; dataset preparation supported by NERC ASSIST program.
- References and original data sources are provided in Site_publications_UKSMD.csv and Appendix A1 of the document.