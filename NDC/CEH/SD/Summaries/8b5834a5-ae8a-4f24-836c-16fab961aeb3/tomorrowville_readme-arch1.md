# Tomorrowville

## Overview
- Tomorrowville is a synthetic, future-focused urban dataset representing a Global South city, inspired by Global South characteristics but adapted spatially for use as a fictitious dataset.
- Built from publicly accessible sources (OpenStreetMap for buildings/roads/land use; World Bank and UN data for socio-economic context).
- Contains five data types to support multi-hazard risk assessments: Buildings, Land uses, Vulnerability, Household, and Hazards.
- Time horizons include present (TV0) and 50 years from now (TV50), with two 50-year scenarios:
  - TV50_s1: urbanization without climate change adaptation
  - TV50_s2: urbanization with climate change adaptation
- Spatial focus around Kathmandu Valley, Nepal (approximately 500 hectares).
- Data is synthetic and designed to enable analysis of exposure, vulnerability, and hazard interactions for disaster risk prevention and planning.

## Data types and key attributes
- Buildings (TV0; TV50_s1; TV50_s2)
  - Attributes cover location (xcoord, ycoord), footprint area (BldArea), building dimensions (width, height), socio-economic context (polytypeSo, Nhouse, population), facility status (specialFac), and hazard exposure strings (vulnStrEQ, vulnStrFL) for earthquakes and floods.
- Land uses (polygonsTV0; polygonsTV50)
  - Attributes include id, type, population, densityCap, density, typeSocial, newBuild, newPop, area.
- Vulnerability
  - Vulnerability files (vulnerabilityInventory_TV0.csv, vulnerabilityInventory_TV50.csv) contain earthquake and flood exposure taxonomy and related functions.
- Household (householdTV50.json)
  - Socio-demographic attributes such as Age, College, Education_A, Gender, Poverty, School, Unemployed, Work, Household_no.
- Hazards
  - Earthquakes: EQ_PGA_eq1, EQ_PGD_eq1, EQ_PGV_eq1 (rasters with statistical summaries and metadata).
  - Floods: FL_depth_fl1.tif, FL_depth_fl2.tif (flood depth rasters for scenarios with and without climate change influence).
  - Debris flow: DF_depth_df1 (Table 9) with two-band raster data for debris-flow exposure.
- Supporting spatial data
  - PolygonsTV0 and polygonsTV50 provide baseline and future land-use, including population and density characteristics.
  - Additional raster hazards and exposure data are described with extent, data type, statistics, and pixel/area details.

## File formats and naming
- Data is delivered as a mix of GIS (vector), tabular, and raster formats: .csv, .shp, .shx, .prj, .dbf, .cpg, .qpj, .tif, .json.
- Examples of file names include:
  - vulnerabilityInventory_TV0.csv, vulnerabilityInventory_TV50.csv
  - buildingsTV0_false_storey.dbf, buildingsTV0.cpg, buildingsTV0.dbf, buildingsTV0.shp, buildingsTV0.shx, buildingsTV50_s1.shp, buildingsTV50_s2.shp
  - polygonsTV0.*, polygonsTV50_*
  - householdTV50.json
  - EQ_PGA_eq1.tif, EQ_PGD_eq1.tif, EQ_PGV_eq1.tif
  - FL_depth_fl1.tif, FL_depth_fl2.tif
  - DF_depth_df1.tif
  - polygonsTV0_style.qml
- File naming reflects data type, time frame (TV0, TV50), and scenario (s1, s2) where applicable.

## Spatial coverage
- Kathmandu, Nepal, focusing on the Kathmandu Valley region (approximately 500 hectares).

## Generation, transformation, and structure
- Data generation and visualization performed in a GIS environment (primarily QGIS).
- Interdisciplinary collaboration (structural engineers, geoscientists, social scientists, GIS experts) to build a holistic, interoperable database of urbanization characteristics.
- GIS-based data structure:
  - Separate layers for land use, buildings, households, and exposure, with linked attributes and integrated tabular data.
  - Vector features (points, lines, polygons) for spatial features; raster layers for hazard data.
  - Household and individual data stored in relational/tabular form to support demographic analyses.
- Exposure development uses a hybrid approach:
  - Predictive: project physical and socio-economic attributes for future scenarios.
  - Exploratory: create multiple future exposure scenarios to capture uncertainties.
- Synthetic social data produced with MATLAB-based algorithms to generate future population and household characteristics.
- Hazard modelling and data sources:
  - Floods: Lisflood-Caesar (CAESAR-based) for floods; other flood depth rasters reflect different scenarios (with/without climate change).
  - Debris flows: LaharFlow dynamic hazard model.
  - Earthquakes: PGA/PGD/PGV rasters representing earthquake scenarios.
  - Vulnerability: based on expert input and global databases (e.g., Joint Research Centre vulnerability datasets).
- Data provenance and structure:
  - Emphasizes trackable data sources and metadata, with the goal of making datasets discoverable via portals.
  - Aimed at combining qualitative and quantitative approaches to represent both social and physical urban characteristics.

## Quality control and references
- Spatial topological errors were addressed using GIS-based debugging tools in QGIS.
- Foundational references for hazard and exposure modelling include:
  - Jenkins et al. (2022) on physics-based multi-hazard simulations for urban planning.
  - Gentile et al. (2022) on physical impact models for multi-hazard risk assessment.
  - Mentese et al. (2023) on future exposure modelling for risk-informed urban planning.

## How analysts can use Tomorrowville
- Identify correlations among exposure (buildings, land use) and hazard intensities (earthquake, flood, debris-flow), moderated by vulnerability and socio-demographic factors.
- Compare scenarios:
  - TV50_s1 (no climate adaptation) vs. TV50_s2 (with climate adaptation) to assess potential risk reduction from adaptation strategies.
  - Assess differences between present (TV0) and future (TV50) baselines to understand urban growth impacts.
- Inform risk-informed urban planning decisions by quantifying potential physical and social impacts under various futures.
- Leverage the integrated GIS structure to link spatial features with socio-economic data, enabling targeted analyses at local scales around Kathmandu Valley.
- Use documented metadata and data lineage to reproduce analyses and ensure transparency.

## Supporting information and context
- The dataset reflects interdisciplinary collaboration and real-world urban context adaptation, with local input from Kathmandu and Nairobi.
- Data production procedures draw on established hazard, exposure, and vulnerability methodologies and literature.