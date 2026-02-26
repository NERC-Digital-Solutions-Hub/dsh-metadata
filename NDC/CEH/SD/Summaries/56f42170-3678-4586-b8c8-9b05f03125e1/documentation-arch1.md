# Documentation A description of the data files and their creation, for the dataset 'Hydro-epidemiological datasets for a selection of place studies'.

## Overview
- A dataset collection linking hydro-meteorological indicators with leptospirosis case data across multiple place studies.
- Includes polygonal place definitions (geojson) and corresponding case counts (csv), plus hydro variables (daily) derived per place.
- Polygons represent areas where hydrometeorological indicators are averaged and leptospirosis cases are recorded.

## Places
- Geojson files define place studies as spatial polygons; hydrometeorological indicators are averaged within these polygons.
- Polygon sources:
  - Chinese provinces: provided by a collaborating MSc student from an official Chinese data store.
  - Smaller Chinese areas (2 counties) and other countries: obtained from OpenStreetMap (relevant search results).
- Coordinates: vertices are in degrees (longitude/latitude).
- Quality: geospatial data are open source or from official instances.

## Cases
- Leptospirosis case data are stored as CSV files with weekly or monthly counts for each place study.
- China-specific data:
  - For most provinces, two CSV files exist: total cases per month and, where available, cases by age group (filename format [province name]_casesByAge.csv).
  - Ningxia, Qinghai, Shanghai, and Tianjin have no files due to zero cases reported 2004–2017.
- Other places: data descriptions summarized in a table (length/resolution, diagnosis type, digitisation, area, remarks, references).
  - Examples include Salvador (Brazil), Negeri Sembilan (Malaysia), Manila (Philippines), Florianópolis (Brazil), Parana/ Rosario/ Santa Fe/ Gualeguaychú (Argentina), Yilong/Mengla (China), Anuradhapura/Nuwara Eliya/Ratnapura/Galle (Sri Lanka).
- Data provenance: health department statistics or peer-reviewed literature.
- Data structure: first column is 'datum' (date); subsequent columns are case counts, either a single column or multiple columns by age bracket (age brackets indicated by lower_highest age in years separated by an underscore).

## Hydrometeorological variables
- Variables originate as raster data and are converted to area-weighted daily averages for each place study.
- Precipitation: CHIRPS dataset, 0.05° x 0.05° resolution.
- Discharge: GloFAS-ERA5 dataset, 0.1° x 0.1° resolution.
- Soil moisture: ESA CCI Soil Moisture v05.2, 0.25° x 0.25° resolution.
- Units:
  - Precipitation: daily rainfall depth in mm.
  - Discharge: daily average discharge in m^3/s.
  - Soil moisture: daily relative volumetric soil moisture content.
- File structure: each hydrometeorological variable has its own directory; filenames begin with the place name.
  - Each file uses 'datum' as the first column (date) and the second column as the value.
  - NA indicates missing data for a given place/time.
- Quality control: source data are widely used and peer-reviewed.

## Data structure details
- Places: directory per place study containing the polygon (geojson) and associated case CSVs.
- Hydrometeorological variables: separate directories for precipitation, discharge, and soil moisture; per-place files with daily values and the date column.

## Collection and generation methods
- Geographic data:
  - Polygons for place studies generated from official data stores (China) or OpenStreetMap (other areas).
- Case data:
  - Sourced from health department statistics or peer-reviewed literature; for China, official statistics (in Chinese).
  - For non-China studies, compilation described in accompanying table with methodological notes.
- Hydrometeorological data:
  - Derived by converting raster data to area-weighted daily averages per place study.
  - CHIRPS, GloFAS-ERA5, and ESA CCI data are cited with specific references for reproducibility.

## References (selected)
- Dorigo, W. et al., 2017. ESA CCI Soil Moisture – state-of-the-art and future directions.
- Gruber, A. et al., 2017. Triple Collocation-Based Merging of Satellite Soil Moisture Retrievals.
- Gruber, A. et al., 2019. Evolution of the ESA CCI Soil Moisture climate data records.
- Funk, C. et al., 2015. The Climate Hazards Infrared Precipitation with Stations (CHIRPS) dataset.
- Harrigan, S. et al., 2020. GloFAS-ERA5 operational global river discharge reanalysis.