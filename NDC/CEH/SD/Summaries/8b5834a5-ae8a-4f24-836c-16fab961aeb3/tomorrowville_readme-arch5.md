# Tomorrowville

## Overview
- Synthetic dataset representing a future Global South urban area, centered on Kathmandu/Nepal, created from publicly available data.
- Five data types integrated: Buildings, Land uses, Vulnerability, Household, and Hazards.
- Purpose: support multi-hazard risk assessments and urban planning with scenarios for 50 years in the future.

## Data types and content
- Buildings (TV0, TV50_s1, TV50_s2): footprints and attributes for existing and future buildings, including geometry and exposure-related fields (e.g., Nhouse, BldArea, coordinates, vulnerability strings for EQ/FL).
- Land uses (polygonsTV0 and polygonsTV50): present and 50-year future land-use types with socio-economic indicators, population, density, and capacity fields.
- Vulnerability (vulnerabilityInventory_TV0.csv, vulnerabilityInventory_TV50.csv): vulnerability functions for earthquakes and floods mapped to buildings/areas.
- Household (householdTV50.json): socio-demographic attributes at the household level (age, education, gender, poverty, employment, etc.).
- Hazards (raster and related files): Earthquake (PGA/PGD/PGV rasters), Flood (depth rasters for flood scenarios with/without climate change), Debris Flow (DF_depth df1). Each contains extent, data type, statistics, and metadata describing the scenario and units.
- Supporting file types include shapefiles (.shp, .shx, .prj, .dbf, .cpg, .qpj) and GeoTIFFs (.tif), as well as .csv and .json metadata files.

## File formats and naming conventions
- Formats used: CSV, Shapefiles, GeoTIFFs, JSON, and related GIS metadata files.
- Examples of naming conventions reflect data type and scenario (e.g., TV0 vs TV50, s1 vs s2 for scenarios with/without climate adaptation):
  - vulnerabilityInventory_TV0.csv, vulnerabilityInventory_TV50.csv
  - buildingsTV0.* and buildingsTV50_s1.*, buildingsTV50_s2.*
  - polygonsTV0.*, polygonsTV50_b1.*, polygonsTV50_b2.* (land-use variants)
  - householdTV50.json
  - Hazard rasters: EQ_PGA_eq1.tif, EQ_PGD_eq1.tif, EQ_PGV_eq1.tif, FL_depth_fl1.tif, FL_depth_fl2.tif, DF_depth_df1.tif
- Data are stored in both vector (polygons/buildings) and raster (hazard) formats, with associated projection files and style definitions (e.g., polygonsTV0.shp, polygonsTV0.prj, polygonsTV0.shx; polygonsTV50_b1.*; polygonsTV50.cpg).

## Spatial and temporal scope
- Spatial coverage: Kathmandu Valley, Nepal, approximately 500 hectares.
- Temporal scope: present-day baseline (TV0) and two future-building scenarios (TV50_s1 without climate adaptation; TV50_s2 with climate adaptation) plus land-use and exposure projections for 50 years ahead.

## Data structure, semantics, and units
- Land-use polygons (polygonsTV0 and polygonsTV50): attributes include id, type, population, densityCap, density, typeSocial, newBuild, newPop, area.
- Buildings (buildingsTV0, buildingsTV50_s1, buildingsTV50_s2): attributes include polyID, polyType, polytypeSo, Nhouse, population, specialFac, BldArea, xcoord, ycoord, and vulnerability descriptors for earthquakes and floods.
- Household (householdTV50.json): attributes cover Age, College, Education_A, Gender, Poverty, School, Unemployed, Work, Household_no.
- Hazards: FP raster layers with detailed metadata, including extent, dimensions, data type, statistics (mean, max, min, stddev), and description of the hazard scenario (earthquake PGA/PGD/PGV; flood depth under climate change and baseline; debris-flow).
- The dataset is designed to enable combined exposure assessments through a GIS-based, layered structure where geometry (points, lines, polygons) and tabular attributes are linked within a relational framework.

## Data generation, provenance, and workflow
- Data sources:
  - Spatial baselines from OpenStreetMap (buildings footprints) and land-use types.
  - Socio-economic projections derived from World Bank and UN repositories.
- Modeling tools and methods:
  - Flood and hazard simulations using Caesar-Lisflood (hydrologic and flood modeling) and LaharFlow for debris-flow hazard.
  - Landslide context informed by high-resolution elevation data (tri-stereo Pleiades).
  - Vulnerability alignment with Global Vulnerability datasets from JRC and related literature.
  - Synthetic social data generated via MATLAB-based bespoke algorithms to project population characteristics.
- Workflow:
  - GIS-centric, iterative process with interdisciplinary coordination (hazard modelling, social data modelling, urban planning) to create a holistic, structured database.
  - Creation of a hybrid, scenario-based exposure dataset for future time t_f, balancing predictive and exploratory elements to cover uncertainty.
  - Data structure designed to allow integrated analysis across land use, buildings, households, and hazards.

## Quality control and governance
- Quality control: spatial topological errors corrected using QGIS tools.
- Documentation and metadata presence: detailed variable descriptions per file, statistics, and dataset descriptions to support discoverability and reuse.
- Governance considerations for Data Stewards:
  - Clear provenance from multiple authoritative sources and synthetic data generation processes.
  - Interoperability across vector and raster formats with standard GIS projections and metadata.
  - Update mechanisms implied by the “future” scenarios; explicit sharing restrictions not stated, but the synthetic nature should be communicated to users.
  - Emphasis on reproducibility through documented data structure, naming conventions, and transformation methods.

## Supporting information and methodological context
- Interdisciplinary collaboration (engineers, geoscientists, social scientists, GIS experts) to develop a cohesive Tomorrowville database.
- Local input from Kathmandu and Nairobi researchers to ground assumptions.
- Synthetic population and exposure data produced with bespoke algorithms (MATLAB) and GIS-based processing.
- Grounding and validation references include:
  - Hazard modeling and multi-hazard risk assessment literature (Jenkins et al. 2022; Gentile et al. 2022; Menteşe et al. 2023).

## Limitations and considerations for users
- The dataset is synthetic and designed for illustrative disaster risk planning and decision support, not as exact real-world data.
- Some components (e.g., future housing and socio-economic projections) are scenario-based and not guaranteed realizations.
- Users should review metadata to understand scenario assumptions, data lineage, and potential applicability to their context.

## References
- Jenkins et al., 2022; Gentile et al., 2022; Menteşe et al., 2023 (as cited in the document).