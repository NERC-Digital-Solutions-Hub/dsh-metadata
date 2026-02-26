# Documentation A description of the data files and their creation, for the dataset 'Hydro-epidemiological datasets for a selection of place studies'

## Overview
- Describes the data files and creation process for hydro-epidemiological datasets focused on selected place studies.
- Combines spatial polygons with averaged hydrometeorological indicators and registered leptospirosis cases within those polygons.
- Data are organized into geospatial (place) data and epidemiological (case) data, linked with corresponding hydrometeorological measurements.

## Data components
- Places: collection of geojson files; each file contains spatial polygons used to average hydrometeorological indicators and to register leptospirosis cases.
- Cases: collection of csv files with weekly or monthly leptospirosis case counts for each place study; for many Chinese provinces, there are two csv files (total monthly cases and possibly by age group for some provinces).
- Hydrometeorological variables: raster-derived data converted to area-weighted daily averages for each place study, including precipitation, discharge, and soil moisture.

## Spatial data (Places)
- Polygons are defined in degrees longitude/latitude.
- Polygons for Chinese provinces provided by an MSc student from an official data store; smaller areas in China and other countries sourced from OpenStreetMap.
- Quality control: geospatial data are open source or from official sources.
- Data structure: standard geojson format.

## Case data
- Data format: csv files with the first column 'datum' representing the date; subsequent columns contain case counts (one column or multiple by age brackets, labeled with age ranges).
- Chinese data: provided from official statistics (in Chinese); for Ningxia, Qinghai, Shanghai, and Tianjin there are no files due to zero cases reported 2004–2017.
- Other place studies: include a variety of locations with differing lengths and resolutions; sources include official health statistics and peer-reviewed literature.
- Nature of recorded values: number of cases referred to the first day of the period covered by the file; some datasets include cases by date of admission, diagnosis type, or other definitions as noted in source references.

## Hydrometeorological data
- Variables and data sources:
  - Precipitation: CHIRPS dataset (0.05° x 0.05° resolution), daily rainfall depth in mm.
  - Discharge: GloFAS-ERA5 dataset (0.1° x 0.1° resolution), daily average river discharge in m^3/s.
  - Soil moisture: ESA CCI Soil Moisture v05.2 (0.25° x 0.25° resolution), daily relative volumetric soil moisture content.
- Processing: raster data converted to area-weighted daily values for each place study.
- References: CHIRPS, GloFAS-ERA5, and ESA CCI Soil Moisture datasets with associated methodological papers cited.

## Data structure and access
- Each hydrometeorological variable has its own directory; file names start with the corresponding place name.
- File format: tabular with a first column 'datum' (date) and a second column containing the value; missing data are indicated as NA.
- For cases and hydrometeorological data, the time granularity matches the source data (weekly/monthly for cases; daily for hydro variables).

## Quality control and provenance
- Geospatial data: open source or official origin; intended to be reliable for spatial analysis.
- Case data: sourced from health department statistics or peer-reviewed literature, ensuring traceability to primary sources.
- Hydrometeorological data: derived from widely used, peer-reviewed climate and hydrology datasets; processing methods documented (area-weighted averaging from raster sources).

## Notes for Data Leaders
- The dataset emphasizes a holistic, place-based view of the hydro-epidemiological system, aligning with governance needs for end-to-end data handling.
- Open data sources with clear provenance support reproducibility and collaborative data improvements.
- Users should be aware of data gaps and granularity issues, such as:
  - Zero-case provinces lacking case files (Ningxia, Qinghai, Shanghai, Tianjin for the 2004–2017 period).
  - Variability in time resolution and age-group breakdown across places.
  - Data may be localized to specific administrative units or hospitals, affecting generalizability.
- The structure supports updating and extending datasets as new place studies or time periods become available.

## References
- CHIRPS precipitation dataset and associated methodology papers.
- GloFAS-ERA5 river discharge reanalysis and associated methodology papers.
- ESA CCI Soil Moisture dataset and related climate data reference works.