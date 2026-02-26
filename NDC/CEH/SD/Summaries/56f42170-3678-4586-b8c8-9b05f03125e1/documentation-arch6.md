# Documentation

- Purpose
  - Describes the data files and their creation for the dataset "Hydro-epidemiological datasets for a selection of place studies," including place-study polygons, leptospirosis case data, and hydrometeorological variables (precipitation, discharge, soil moisture).

- Places
  - A collection of geojson polygons representing place studies; hydrometeorological indicators are averaged over each polygon and leptospirosis cases are recorded within them.
  - Polygons for Chinese provinces provided by an MSc student from an official data store; smaller Chinese areas (2 counties) and other countries sourced from OpenStreetMap.

- Nature and units of polygons
  - Polygons have vertices in degrees longitude and latitude.
  - Quality controlled by open-source or official sources.
  - Data structure: standard geojson format.

- Cases (leptospirosis)
  - CSV files with weekly or monthly case numbers per place study. For most Chinese provinces, two CSVs exist: total cases per month and cases by age group (filename format: [province name]_casesByAge.csv).
  - Chinese data origins: official Chinese statistics; some provinces (Ningxia, Qinghai, Shanghai, Tianjin) have no data (2004–2017 covered by others).
  - For non-China place studies, details vary and are summarized in a following table (length/resolution, diagnosis type, digitisation, area, remarks, references).
  - Data columns: first column 'datum' (date), subsequent columns contain case counts (one or more by age bracket, age brackets indicated by "low_high" in column naming).

- Hydrometeorological variables: collection and generation
  - Source data are in raster format and are converted to area-weighted daily averages per place study.
  - Precipitation: derived from CHIRPS (0.05° x 0.05°); cited reference Funk et al. 2015.
  - Discharge: derived from GloFAS-ERA5 (0.1° x 0.1°); cited reference Harrigan et al. 2020.
  - Soil moisture: derived from ESA CCI Soil Moisture v05.2 (0.25° x 0.25°); cited references Dorigo et al., Gruber et al. 2017/2019.
  - Units:
    - Precipitation: daily rainfall depth in mm.
    - Discharge: daily average discharge in m^3/s.
    - Soil moisture: daily relative volumetric soil moisture content.
  - Quality control: sources are widely used and peer-reviewed.
  - Data structure: each variable has its own directory; file names begin with the place name; first column 'datum' (date), second column the value; NA indicates missing data.

- Additional details and references
  - Detailed data structure notes, including the use of area-weighted daily averages and the exact data sources.
  - References provided for CHIRPS, GloFAS-ERA5, ESA CCI Soil Moisture, and related methodological sources.