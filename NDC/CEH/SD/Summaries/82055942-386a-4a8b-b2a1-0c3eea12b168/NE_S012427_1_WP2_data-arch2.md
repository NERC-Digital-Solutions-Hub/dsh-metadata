# Flood risk assessment of the Luanhe river basin under different development strategies and climate scenarios

## Objective
- Assess flood risk in the Luanhe river basin under multiple development strategies and climate scenarios up to 2030.
- Support socio-economic planning for the Beijing–Tianjin–Hebei region by providing standardized, reproducible flood risk outputs.

## Data and inputs
- Climate projections to 2030:
  - Uplifts of future climate scenarios derived from NASA Earth Exchange Global Daily Downscaled Projections (NEX-GDDP).
  - Used to modify the future 100-year design rainfall for the basin.
- Historical validation data:
  - 2012 flood event used to validate the flood model (HiPIMS) with remote sensing observations.
- Flood predictions:
  - Inundation results to 2030 under different development strategies and climate scenarios (HiPIMS outputs).
- Population vulnerability:
  - Gridded population data from GPWv4 to assess resident exposure.
- Location context:
  - Luanhe river basin in northeast North China Plain (around 115°30′–119°45′ E, 39°10′–42°40′ N).

## Methods and outputs
- Modeling tool:
  - HiPIMS flood modelling framework; previously validated and widely used in related studies.
- Scenarios and inputs:
  - Land use in 2015 baseline, plus development strategies: Trend, Expansion, Sustainability, Conservation.
  - Climate scenarios: RCP4.5 and RCP8.5.
  - Reservoir configurations: P (Panjiakou) and S (Shuangfengsi) as part of scenario delineations.
  - Outputs combine land-use, climate inputs, and infrastructure to generate flood inundation results.
- Outputs produced:
  - Flood inundation maps in meters under each scenario.
  - Flood risk maps produced by overlaying inundation with population density maps.

## Data formats and structure
- Formats:
  - Climate uplifts: CSV (dimensionless uplift values).
  - Other data (inundation, validation, population): TIFF.
- Data organization:
  - Described across two tabs (Tab 1 and Tab 2) with datasets including validation data, climate uplifts, inundation maps, and population data.
- Example data products:
  - Validation.tif and RemoteSensing_validation.tif (historical 2012 event).
  - rcp45.csv and rcp85.csv (city-wide climate uplifts).
  - Inundation map data (various scenarios).
  - Population data (GPWv4-derived).

## Quality control and provenance
- HiPIMS validation:
  - Has been used to support flood risk assessments in prior projects.
  - Demonstrated to provide robust estimates; dataset is well documented and under peer-reviewed submission.
- Open data foundations:
  - NEX-GDDP and GPWv4 are widely used open datasets.
- Documentation and reproducibility:
  - Data and methods are published with detailed descriptions; designed for reproducibility and external verification.

## Data access, licensing, and stewardship
- Licensing:
  - Open Government Licence for climate, inundation, and related datasets, with GPWv4 and NEX-GDDP as open data sources.
- Data sharing and portals:
  - Datasets are prepared for storage and uploading to appropriate data portals to enable broader accessibility.

## Dataset details (structure and records)
- Datasets include:
  - Flood model validation data: Validation.tif; RemoteSensing_validation.tif (2012 event); contributed by Loughborough University; Open Government Licence.
  - Climate change uplifts: rcp45.csv and rcp85.csv; first column city, second column uplift value; contributed by Loughborough University; Open Government Licence.
  - Inundation map data: flood simulation results for different climate and infrastructure scenarios; contributed by Loughborough University; Open Government Licence.
  - Population data: GPWv4-derived; resampled to local scale; contributed by Loughborough University; Open Government Licence.
- Contributing authors:
  - Loughborough University (multiple components).
- References for data and methods:
  - Doxsey-Whitfield et al. (GPWv4), Thrasher and Nemani (NEX-GDDP), Xia et al. (HiPIMS framework), Xing et al. (city-scale hydrodynamic modelling), Zhao et al. (2021 Sustainability Science forthcoming).

## Relevance for environmental analysts
- Provides a standardized, open-data pipeline to evaluate flood risk under multiple development and climate futures.
- Demonstrates integration of climate projections, historical validation, hydrodynamic modelling, and population exposure to produce actionable risk maps.
- Aligns with goals of making environmental data more valuable through cross-dataset integration and enabling access to underlying data for scrutiny and reuse.