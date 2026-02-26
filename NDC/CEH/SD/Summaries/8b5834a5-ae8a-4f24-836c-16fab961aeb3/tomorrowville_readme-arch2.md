# Tomorrowville

- A synthetic, future-oriented dataset representing a Global South urban area (centered around Kathmandu, Nepal) designed to study multi-hazard risk in urban planning. The context is inspired by Global South cities but spatially/content-wise adapted for fictitious analysis.

## What the dataset contains

- Buildings (TV0, TV50_s1, TV50_s2)
  - Footprints for today and 50 years hence, with attributes for multi-hazard risk assessment (e.g., polyID, polyType, Nhouse, population, vulnStrEQ, vulnStrFL, coordinates, BldArea).
  - TV50_s1: future buildings without climate adaptation.
  - TV50_s2: future buildings with climate adaptation considerations.
- Land uses
  - PolygonsTV0 (current) and polygonsTV50 (future) detailing land-use types, population, density, social type, new/buildable areas.
- Vulnerability
  - vulnerabilityInventory_TV0.csv and vulnerabilityInventory_TV50.csv containing earthquake and flood vulnerability functions.
- Household and individuals
  - householdTV50.json with socio-demographic attributes (age, education, gender, poverty, employment, school, etc.) and Household_no linkage.
- Hazards
  - Earthquake: EQ_PGA_eq1, EQ_PGD_eq1, EQ_PGV_eq1 rasters (tif).
  - Floods: FL_depth_fl1.tif, FL_depth_fl2.tif.
  - Debris flows: DF_depth_df1.tif (2-band raster with debris-flow attributes).
- Supporting files
  - Example style and metadata files (e.g., polygonsTV0_style.qml, various .prj, .shp/.dbf/.shx/.cpg/.qpj) to accompany GIS features.

## File formats and naming

- Formats used: .csv, .shp, .shx, .prj, .dbf, .cpg, .qpj, .tif, .json.
- Naming conventions illustrate layered GIS data and scenario variants (e.g., vulnerabilityInventory_TV0.csv, vulnerabilityInventory_TV50.csv; buildingsTV50_s1, buildingsTV50_s2; polygonsTV0, polygonsTV50; X_TVDatasets and hazard rasters).

## Spatial and temporal scope

- Spatial coverage: Kathmandu/Nepal region, approximately 500 hectares around the Kathmandu Valley.
- Temporal framing: present day (TV0) and 50-year horizon (TV50) with two future scenarios:
  - TV50_s1: urbanization without climate adaptation.
  - TV50_s2: urbanization with climate adaptation adjustments.

## Data structure and how it’s built

- GIS-based, multi-layer structure
  - Vector layers for features (buildings, land uses) with integrated attribute tables.
  - Tabular data linked to spatial features (e.g., households, vulnerability functions).
- Hybrid exposure development
  - Combines predictive and exploratory scenario approaches to project physical and socio-economic attributes for the future.
  - Time horizon for exposure development is defined as tf; not a single fixed outcome but a set of comparative scenarios to support risk-informed planning.
- Data integration process
  - Land-use and hazard assumptions feed into building locations, infrastructure attributes, and household demographics.
  - Socioeconomic projections characterize households and individuals for exposure assessment.

## Methods and workflow

- Data generation and manipulation
  - GIS-centric workflow, using QGIS for storage, analysis, and presentation; GIS serves as the core mediator among disciplines.
  - MATLAB used to generate synthetic social data (population characteristics and projections).
- Hazard and vulnerability modelling
  - Floods modeled with Lisflood-based tools (Caesar-Lisflood) and debris-flow with LaharFlow dynamics; earthquakes represented via PGA/PGD/PGV-based rasters.
  - Vulnerability functions derived from local·partners and global databases (e.g., JRC flood depth-damage methods).
- Interdisciplinary collaboration
  - About 30 interdisciplinary meetings since June 2021; team includes structural engineers, geoscientists, social scientists, and GIS experts; local researchers contributed urban context insights.
- Quality control
  - Spatial topological errors addressed with QGIS topological debugging modules.

## Data quality, access, and reuse

- Quality assurance
  - Topology cleaning and GIS-based validation to ensure consistent spatial relationships.
- Data accessibility
  - Dataset is synthetic and built from publicly available sources (OpenStreetMap, World Bank, UN). The project emphasizes making underlying data accessible to others to support transparency and reuse, addressing the challenge of data accessibility.

## How this supports environmental monitoring and policy evaluation

- Standardized, comparable data across time
  - Enables monitoring of environmental health indicators and policy performance through multiple future scenarios.
- Multi-hazard exposure assessment
  - Integrates physical (buildings, land use, infrastructure) with social (households, education, poverty) layers to quantify exposure and vulnerability under earthquakes, floods, and debris flows.
- Scenario-based policy analysis
  - Facilitates risk-informed decision making by comparing no-adaptation and adaptation scenarios, helping assess the effectiveness of climate adaptation measures.
- Long-term data value and stewardship
  - GIS-based, layered structure supports ongoing monitoring, with datasets stored and uploaded to appropriate portals; encourages re-use and integration with other datasets.

## Supporting information and references

- Data production draws on hazard, exposure, and vulnerability methodologies from recent disaster risk reduction literature.
- Key sources include work on multi-hazard risk modelling, physical impact models, and urban exposure modelling to inform scenario development and risk assessment.
- References provide methodological grounding for hazard simulations, vulnerability scoring, and exposure development in urban planning contexts.