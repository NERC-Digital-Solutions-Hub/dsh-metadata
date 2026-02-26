# Documentation

- Overview
  - Describes the data files and their creation for the dataset "Hydro-epidemiological datasets for a selection of place studies."
  - Focuses on two main data components: polygons representing place studies and leptospirosis case counts, plus associated hydrometeorological variables.

- Places (polygons)
  - Collection: geojson files, each representing a place study; polygons are spatial areas over which hydrometeorological indicators are averaged and leptospirosis cases are recorded.
  - Provenance for polygons:
    - China provinces: provided by a collaborating MSc student from an official Chinese data store.
    - Smaller Chinese areas (2 counties) and other countries: sourced from OpenStreetMap.
  - Geography: polygon vertices in degrees (longitude/latitude).
  - Quality: data are open source or from official sources; standard geojson format.
  - Data structure: per-place geojson files.

- Cases (leptospirosis)
  - Collection: csv files with weekly or monthly case numbers for each place study.
  - China: for most provinces, two csv files per province (total monthly cases; plus optional [province]_casesByAge.csv for age groups). Ningxia, Qinghai, Shanghai, Tianjin absent due to zero cases 2004–2017.
  - Other place studies: curated details summarized in a long table (length/resolution, diagnosis type, digitisation status, area, remarks, references). Examples include Salvador (Brazil), Negeri Sembilan (Malaysia), Manila (Philippines), Florianópolis (Brazil), Paraná/Rosario/Santa Fe/Gualeguaychú (Argentina), Yilong/Mengla (China), Anuradhapura/Nuwara Eliya/Ratnapura/Galle (Sri Lanka).
  - Data characteristics: first column 'datum' = date; subsequent columns = case counts, either a single column or multiple by age bracket (labeled with age ranges).
  - Collection: case data for Chinese provinces derived from official statistics; non-Chinese place studies documented with provided metadata and sources.
  - Data sources: health department statistics or peer-reviewed literature.

- Hydrometeorological variables (linked to each place study)
  - Variables and data sources:
    - Precipitation: daily rainfall depth (mm) from CHIRPS (0.05° x 0.05° resolution).
    - Discharge: daily average discharge (m^3/s) from GloFAS-ERA5 reanalysis (0.1° x 0.1° resolution).
    - Soil moisture: daily relative volumetric soil moisture from ESA CCI Soil Moisture v05.2 (0.25° x 0.25° resolution).
  - Data sources and references:
    - CHIRPS methodology and data description (Funk et al., 2015; Scientific Data).
    - GloFAS-ERA5 discharge reanalysis (Harrigan et al., 2020; Earth System Science Data Discussions).
    - ESA CCI Soil Moisture climate data records (multiple supporting papers by Dorigo et al. and Gruber et al.; Remote Sensing of Environment).
  - Processing: raster data converted to area-weighted daily averages for each place study.
  - Units:
    - Precipitation: mm/day.
    - Discharge: m^3/s (daily values).
    - Soil moisture: relative volumetric content (daily values).
  - Quality control: source datasets are widely used, peer-reviewed, and considered reliable for hydrometeorological analyses.

- Data organization and structure
  - Polygons (Places): each place in its own GeoJSON file; coordinates in degrees; open data or official sources.
  - Cases: per-place CSV files; date in the first column; subsequent columns hold case counts (by time period and optional age brackets).
  - Hydrometeorological: separate directories for each variable; within each, files named after the place; first column 'datum', second column value; NA indicates missing data.

- Usage notes for GIS applications
  - Enables map-based visualisations of leptospirosis by place study, overlaid with hydrometeorological indicators.
  - Allows area-weighted aggregation of raster data to polygons for spatial analysis and visualization.
  - Requires handling of different temporal resolutions and potential gaps (NA values) across datasets.
  - Useful for cross-study comparisons, data fusion, and policy/public-facing map products.

- Metadata and references
  - Includes detailed references for hydrometeorological data sources (CHIRPS, GloFAS-ERA5, ESA CCI Soil Moisture) and the publications underpinning their datasets.
  - Provides notes on data provenance (official statistics, health department data, OpenStreetMap) and digitisation status for various place studies.