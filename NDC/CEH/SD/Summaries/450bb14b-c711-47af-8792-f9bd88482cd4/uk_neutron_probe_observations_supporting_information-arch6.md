# Collated neutron probe measurements and derived soil moisture data, UK, 1966-2013: Supporting Information

## 1. Summary of dataset
- UK Soil Moisture Databank (UKSMD) compiles neutron probe soil moisture observations for 428 locations across hundreds of UK sites.
- Temporal coverage spans 1966–2013 with series lengths from 1 to 20 years.
- Data types provided: neutron probe readings (R), volumetric soil moisture content (θ, m3 water/m3 soil), and depth-integrated profile moisture content (PMC, m3 water/m3 soil or depth in mm water).
- Includes metadata and links to publications for individual datasets.
- Tube locations are georeferenced (British National Grid and latitude/longitude).

## 2. Dataset structure
- Four CSV files (two data files and two metadata files):
  - Volumetric_soil_moisture_UKSMD.csv: Time-series of NP count rate R and volumetric soil moisture θ at multiple depths.
  - Profile_moisture_content_UKSMD.csv: Time-series of depth-integrated profile moisture content (PMC1 in mm water, PMC2 in m3 water/m3 soil).
  - Tube_metadata_UKSMD.csv: Tube identity, location, dates, depths, vegetation, land-use, soil type, geology, coordinates, dates, and comments.
  - Site_publications_UKSMD.csv: Published papers and reports associated with each site and URLs if available.
- Data are in CSV format for easy import into spreadsheets or programmatic analysis (R, Python, Fortran).

## 3. Data production and recovery
- UKSMD consolidates older SMDB data (1960s–1980s) recovered from magnetic tapes and newer data up to 2013 from spreadsheets/databases.
- Original SMDB data were lost during system migrations; recovered data were quality controlled and converted to SI units.
- Data recovery produced three representations of soil moisture: NP counts (R), volumetric moisture (θ), and depth-integrated PMC, enabling flexible analyses.
- Final dataset covers 441 tube locations in 45 study areas across England, Wales, and Scotland (no data yet for Northern Ireland).

### 3.1 The data recovery process
- Older data from 1960s–1980s were reassembled from Univac tapes and other sources; newer NP data were gathered from various archives.
- The aim was to create a consistent, long-term dataset (1966–2013) from disparate sources.

### 3.2 Neutron probe readings
- Measurements involve lowering NP into soil access tubes; readings reflect moisture in a surrounding soil sphere (roughly 0.2–0.3 m radius).
- NP readings are time-consumptive and site-specific; depth-specific readings underpin θ and PMC derivations.

### 3.2.2 Volumetric soil moisture
- θ derived from NP count rate R using calibration: θ = a (R/Rw) + b, where Rw is the water count and a, b are calibration parameters.
- Field calibrations exist; if unavailable, Wallingford calibration may be used.
- Top-layer measurements (<15–20 cm) may underestimate θ due to neutron escape; often these depths are deleted or assigned to deeper layers.
- For this dataset, θ and R/Rw values are recovered for about 73% of observations; θ recovered for about 78%.
- When θ is missing but R and Rw are available, θ is recalculated using calibration equations; when not possible, θ is left missing or derived from available site information with caveats.

### 3.2.3 Depth-integrated profile moisture content
- PMC is derived by integrating θ over depth with layer factors Fi, converting to a depth-integrated water content.
- PMC1 provides mm of water stored to depth zn; PMC2 provides m3 water/m3 soil.
- When PMC values are missing, the authors derive PMC down to the maximum measurement depth using the θ-based approach described.

## 4. Dataset format and availability
### 4.1 Dataset format
- Four files as described above, with detailed metadata columns:
  - Tube_metadata_UKSMD.csv includes: TUBE_ID, TUBE_NAME, AREA_ID, AREA_NAME, SITE_ID, SITE_NAME, coordinates (EASTING, NORTHING, LATITUDE, LONGITUDE), dates, depth coverage, vegetation, land-use, soil type, geology, calibration notes, and comments.
  - Site_publications_UKSMD.csv includes: AREA_ID, SITE_ID, REFERENCE, URL/DOI, and REFERENCE_COMMENT.
  - Volumetric_soil_moisture_UKSMD.csv includes: DATE_TIME, TUBE_ID, AREA_ID, RW (water count), DEPTH, COUNT (raw), VOLUMETRIC_SOIL_MOISTURE (θ), COMMENT, QUALITY1, QUALITY2.
  - Profile_moisture_content_UKSMD.csv includes: DATE_TIME, TUBE_ID, AREA_ID, DEPTH, PMC1 (mm water), PMC2 (m3 water/m3 soil), COMMENT, QUALITY1, QUALITY2.
- Site publications provide references to original research; users are encouraged to acknowledge data origins.

### 4.2 Soil-moisture data availability
- Data are available for 45 geographic areas with readings at 112 sites and 428 NP tubes.
- Data formats available: raw NP counts (R and Rw), θ (volumetric moisture), and PMC (depth-integrated moisture).
- Northern Ireland has no recovered NP observations to date.
- Notable long-term datasets include extended measurements in the Tern catchment (SMDBH) and multiple sites with 10+ years of data (e.g., Hodnet Heath, Driby).

## 5. Data quality, missing data, and uncertainty
### 5.1 Missing data
- All recovered data indicate missing values as -1.
- When some data forms are missing for a site, authors attempted to compute missing values where possible; such values are flagged with COMMENT='c' to indicate calculated values.
- If original metadata are missing (elevation, etc.), alternative sources are used and noted in Tube_comment.

### 5.2 Quality control and uncertainty
- θ values are expected to lie between 0 and 1; negative values are treated as missing.
- Some areas show θ > 1.0 (e.g., Balquidder, Crinan, Nant Iago/Cyff), due to peat-rich, high-rainfall soils; these are flagged with QUALITY1.
- QUALITY2 flags abnormal jumps/spikes in PMC values; such data may be retained if they align with original observations and are supported by other values.
- Neutron-probe-derived soil moisture is most reliable for detecting changes rather than providing exact absolute moisture content; calibration uncertainty can be substantial, particularly when site-specific calibration is unavailable.
- Values calculated by the authors (not originally measured) are labeled with 'c', indicating greater uncertainty.

## 6. How to use the data
- Acknowledge original studies; reference Site_publications_UKSMD.csv for citations and URLs.
- Use available formats according to need:
  - For depth-specific analysis: Volumetric_soil_moisture_UKSMD.csv (R, rw, θ across depths).
  - For site comparisons across soils with varying depths: Profile_moisture_content_UKSMD.csv (PMC1 and PMC2).
- NP-derived data are most robust for detecting moisture changes over time rather than delivering exact absolute moisture values.
- Consider quality flags (q1 for values >1.0, q2 for jumps) and compare results with and without flagged data to assess sensitivity.
- When combining with other datasets, LOCAR meteorological data and international soil moisture datasets (ISMN, COSMOS-UK) can provide broader context.
- NP observations complement remotely sensed soil moisture products, though NP is less reliable in the topmost 10 cm for direct satellite comparisons.
- Potential applications include hydrological model evaluation and data assimilation, drought analysis (1966–2013 span includes the 1976 drought), and historical soil moisture research linked to greenhouse gas studies.

## Acknowledgements
- Data recovery and analyses supported by NERC-CEH Water Programme and FP7 MELODIES project; dataset preparation supported by NERC ASSIST program.
- Acknowledgement of individuals who assisted with site identification and references.

## References (selected context)
- Core methodologies and calibration approaches for neutron probes and soil moisture estimation.
- Related hydrological and land-surface studies (LOCAR, ISMN COSMOS-UK, etc.) and historical data recovery efforts.