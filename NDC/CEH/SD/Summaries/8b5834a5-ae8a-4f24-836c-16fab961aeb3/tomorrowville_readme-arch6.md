# Tomorrowville

- Tomorrowville is a synthetic, virtual city representing a future Global South urban area. It uses real-world inspirations but is spatially modified to function as a fictitious dataset for analysis and risk assessment.
- Geographic focus: Kathmandu, Nepal, around the Kathmandu Valley, covering approximately 500 hectares.
- Purpose: to enable understanding of urban context, hazard exposure, vulnerabilities, and socio-economic dynamics in a future scenario; designed for risk-informed planning and disaster risk reduction.

## Data types (five data categories)

- Buildings
  - Footprints for today (TV0) and for 50 years ahead (TV50) under two scenarios: s1 (without climate change adaptation) and s2 (with climate change adaptation).
  - Attributes include polyID, polyType, polytypeSo (socioeconomic status), Nhouse (number of households), BldArea (building footprint area), coordinates, and hazard exposure strings (vulnStrEQ, vulnStrFL).
- Land uses
  - Land-use polygons for today (polygonsTV0) and 50 years ahead (polygonsTV50).
  - Attributes include id, type, population, densityCap, density, typeSocial, newBuild, newPop, area.
- Vulnerability
  - Vulnerability inventories (e.g., vulnerabilityInventory_TV0.csv, vulnerabilityInventory_TV50.csv) describing how buildings are exposed to hazards (earthquake, flood) via vulnerability functions.
- Household
  - Socio-demographic attributes projected for 50 years (householdTV50.json): Age, College, Education_A, Gender, Poverty, School, Unemployed, Work, Household_no.
- Hazards
  - Hazard rasters and depth maps for earthquake, floods, and debris flows, including:
    - Flood depth rasters (FL_depth_fl1.tif, FL_depth_fl2.tif)
    - Earthquake rasters (EQ_PGA_eq1.tif, EQ_PGD_eq1.tif, EQ_PGV_eq1.tif)
    - Debris flow depth (DF_depth_df1.tif) with two bands
  - Each file includes spatial extent, resolution, data type, and statistical metadata.

## File formats and naming

- File formats used: .csv, .shp, .shx, .prj, .dbf, .cpg, .qpj, .tif, .json (GIS-compatible and raster/tabular formats).
- Representative file examples:
  - vulnerabilityInventory_TV0.csv, vulnerabilityInventory_TV50.csv
  - buildingsTV0*.shp, buildingsTV0*.dbf, buildingsTV50_s1.* (shp/dbf/prj/shx), buildingsTV50_s2.* 
  - polygonsTV0.* and polygonsTV50.* (land-use GIS layers)
  - householdTV50.json
  - Hazard rasters: EQ_PGA_eq1.tif, EQ_PGD_eq1.tif, EQ_PGV_eq1.tif, FL_depth_fl1.tif, FL_depth_fl2.tif
  - DF_depth_df1.tif (debris-flow, two bands)

## Data structure and content details

- Land-use polygons (polygonsTV0 and polygonsTV50)
  - Key attributes: id, type, population, densityCap, density, typeSocial, newBuild, newPop, area.
- Building footprints (buildingsTV0, buildingsTV50_s1, buildingsTV50_s2)
  - TV0: existing buildings with attributes such as polyID, polyType, polytypeSo, Nhouse, population, BldArea, xcoord, ycoord, and hazard exposure strings.
  - TV50_s1: future buildings without climate adaptation; includes width, height, Nhouse, population, xcoord, ycoord, and vulnerability strings.
  - TV50_s2: future buildings with climate adaptation; similar attributes to s1.
- Household data (householdTV50.json)
  - Individual-level socio-demographic attributes: Age, College, Education_A, Gender, Poverty, School, Unemployed, Work, Household_no.
- Hazards (raster and tabular)
  - Earthquake: PGA (PGA_eq1), PGD (PGD_eq1), PGV (PGV_eq1)
  - Floods: depth rasters FL_depth_fl1, FL_depth_fl2
  - Debris flows: DF_depth_df1 (two-band raster)
  - Attributes include extent, pixel size, data type, and statistics (mean, max, min, stddev, etc.).
- Supporting spatial details
  - Each raster includes metadata such as extent, width, height, bands, origin, and pixel size.

## Spatial coverage and scale

- Region: Kathmandu Valley, Nepal.
- Scale: dataset integrates both polygon/vector layers (buildings, land use, households) and raster hazard layers to support multi-hazard risk assessments.

## Collection, generation, and transformation methods

- Data generation environment
  - Generated and used in a geospatial GIS context; manipulations performed with QGIS.
  - GIS-based data structure: layered approach with vector features (points/lines/polygons) and integrated tabular attributes.
  - Household and individual data are stored in relational/tabular formats; exposure data produced for a future time horizon (t_f) via interdisciplinary processes.
- Interdisciplinary process
  - Approximately 30 interdisciplinary online meetings in 2021 (engineering, geoscience, social science, GIS) to integrate perspectives.
  - The data model acts as a mediator to combine physical infrastructure, social dynamics, urban planning, and hazard modelling.
- Data production workflow
  - Planning extent subdivided into zones; land-use polygons generated.
  - Building locations and attributes derived by combining land-use, hazard assumptions, and socio-economic characteristics.
  - Household and individual data created using socio-economic projections to support exposure and vulnerability analyses.
  - Hybrid scenario development: predictive (projecting attributes realistically) and exploratory (creating multiple future scenarios for comparison).
  - Purpose: enable relative comparisons of disaster risk under uncertainty; outputs are intended as data products for decision support and scenario analysis.
- Data integration and storage
  - GIS layers store geometries with automatically computed geometrical attributes; attributes stored in integrated tables for analysis.
  - Exposure data produced through interdisciplinary collaboration to reflect combined social and physical urban characteristics.

## Supporting information and data sources

- Data sources and production procedures
  - Building footprints partly derived from Open Street Map data and refined for the study.
  - Flood simulations: Caesar-Lisflood (Lisflood-FP + CAESAR) for flood-based exposure; landslide analysis uses tri-stereo Pleiades DEM; debris-flow analysis uses LaharFlow.
  - Synthetic social data produced via bespoke MATLAB algorithms for population and household projections.
  - Vulnerability data developed in consultation with local partners and global databases (e.g., Joint Research Center flood depth-damage functions).
- Data generation references
  - Hazard modelling: Jenkins et al., 2023
  - Vulnerability modelling: Gentile et al., 2022
  - Exposure modelling: Mentese et al., 2023
- Local and collaborative context
  - Local researchers in Kathmandu and Nairobi contributed domain expertise (structural engineering, urban planning).
  - The dataset represents synthetic social and physical attributes to enable realistic but hypothetical future exposure scenarios.

## Quality control

- Spatial topological errors are addressed and removed using topological debugging modules in QGIS.

## How this data supports the Data Support archetype

- Provides ready-to-use data products enabling exploration of data across topics (buildings, land use, vulnerability, households, and hazards) for disaster risk assessments.
- Supports creation of dashboards, pivot analyses, and self-service exploration by end users through GIS-friendly formats and well-documented attributes.
- Demonstrates a reproducible, interdisciplinary workflow for building synthetic yet coherent urban exposure datasets, including data generation, validation, and scenario analysis.

## Notes and caveats

- The dataset is synthetic and framed within hybrid future scenarios; results are intended for relative risk comparisons and methodological exploration rather than exact forecasts.
- Climate adaptation is represented through separate future-building scenarios (TV50_s1 vs TV50_s2), illustrating how adaptation assumptions alter exposure and infrastructure characteristics.