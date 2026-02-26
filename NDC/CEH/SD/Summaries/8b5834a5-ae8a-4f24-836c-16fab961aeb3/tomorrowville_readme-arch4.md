# Tomorrowville

## Overview
- Tomorrowville is a synthetic, future Global South urban-context dataset representing Kathmandu, Nepal, around 500 hectares.
- Built from publicly available sources (Open Street Map for buildings/roads, World Bank and UN for socio-economic data).
- Represents five data types across a 50-year horizon, including two future scenarios: TV50_s1 (no climate adaptation) and TV50_s2 (with climate adaptation).

## Data Types and Structure
- Buildings
  - Existing (TV0) and future (TV50_s1, TV50_s2) footprints with attributes.
  - Key fields include polyID, polyType, polytypeSo, Nhouse, population, BldArea, xcoord, ycoord, and vulnerability strings for EQ/FL; specialFac; width/height in future datasets.
- Land Uses
  - PolygonsTV0 (current) and polygonsTV50 (future) with population, densityCap, density, typeSocial, newBuild, newPop, area, and related identifiers.
- Vulnerability
  - vulnerabilityInventory_TV0.csv and vulnerabilityInventory_TV50.csv (vulnerability functions for seismic and flood hazards).
- Household
  - householdTV50.json with socio-demographic attributes (Age, College, Education_A, Gender, Poverty, School, Unemployed, Work, Household_no).
- Hazards
  - Earthquakes (EQ), Floods (FL), Debris Flows (DF) represented as raster datasets (e.g., EQ_PGA_eq1.tif, FL_depth_fl1.tif, DF_depth_df1.tif) plus supporting metadata.

## File Formats and Naming
- Formats: .csv, .shp, .shx, .prj, .dbf, .cpg, .qpj, .tif, .json
- Representative file names include:
  - vulnerabilityInventory_TV0.csv, vulnerabilityInventory_TV50.csv
  - buildingsTV0.* (e.g., buildingsTV0.shp, buildingsTV0.dbf, etc.)
  - buildingsTV50_s1.* and buildingsTV50_s2.* (future scenarios)
  - polygonsTV0.* and polygonsTV50_b1.* / polygonsTV50_b2.* (land-use variations)
  - householdTV50.json
  - hazard/raster datasets such as EQ_PGA_eq1.tif, FL_depth_fl1.tif, DF_depth_df1.tif

## Spatial Coverage and Context
- Focused on Kathmandu, Nepal, with approx. 500 hectares around Kathmandu Valley.
- Combines spatial (vector/raster) and tabular data to represent a synthetic urban system for disaster risk modelling.

## Generation, Transformation, and Provenance
- Methodology
  - Data generated and manipulated in a GIS environment (primarily QGIS) to ensure GIS compatibility and discoverability.
  - Interdisciplinary process with around 30 meetings across engineers, geoscientists, social scientists, and GIS experts to build a holistic database.
  - A GIS-based data structure with separate layers for land use (vector), buildings (vector), households/individuals (tabular), and hazards (raster).
- Data Structure and Workflow
  - Land-use planning extent is subdivided into zones; projected land-use types feed building locations/attributes and household demographics.
  - Building layer enriched with taxonomy for disaster-impact quantification.
  - Exposure development uses a hybrid scenario approach (predictive + exploratory) to cover uncertainties for disaster risk assessment.
  - Time frame tf used to generate future exposure data; future scenarios enable comparative risk analysis.
- Data Production Details
  - Synthetic social data produced via bespoke MATLAB algorithms.
  - Building footprints derived from OpenStreetMap data, modified for aims.
  - Flood simulations: Caesar-Lisflood (Lisflood-FP + CAESAR), landslide analysis: tri-stereo Pleiades DEM; debris flows: LaharFlow model.
  - Vulnerability data informed by local partners and JRC global datasets.
- Documentation and References
  - Hazard modeling and vulnerability/exposure references include Jenkins et al. (2022/2023), Gentile et al. (2022), Menteşe et al. (2023).
  - Detailed dataset descriptions, metadata, and variable definitions provided in Tables and Supporting Information.

## Data Quality, Governance, and Accessibility
- Quality control
  - Topological errors addressed with QGIS debugging tools.
- Governance and discoverability
  - Emphasizes integrated, GIS-based, multi-disciplinary data governance to support transparent exposure and risk analyses.
  - Metadata and structured data organization facilitate reuse and cross-disciplinary collaboration.

## Supporting Information and Provenance
- Expert collaboration from Kathmandu and Nairobi with urban planning and structural engineering insights.
- Population synthesis and algorithms ensure synthetic but context-relevant demographic projections.
- Data provenance includes explicit descriptions of data sources, generation methods, and modelling tools (MATLAB, Lisflood, LaharFlow, DEM sources).
- Spatial/topological integrity and references provided to support reproducibility and methodological rigor.

## Relevance for Data Leaders
- Demonstrates a comprehensive, end-to-end data system for disaster risk planning:
  - System-wide view across land use, buildings, households, and hazards.
  - Scenario-based exposure modelling to support robust decision-making under uncertainty.
  - Clear data lineage, metadata, and governance practices enabling co-ownership and collaboration across disciplines.
  - Practical example of managing both spatial and tabular data assets within a GIS-enabled framework.