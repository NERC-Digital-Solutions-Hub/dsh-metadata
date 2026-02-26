# Tomorrowville

## Overview
- Tomorrowville is a synthetic, future-focused urban dataset representing a Global South context, centered on Kathmandu Valley, Nepal (~500 hectares).
- Combines publicly available basemaps (e.g., OpenStreetMap) with World Bank/UN socio-economic data to model a future urban environment for multi-hazard risk assessment and policy monitoring.

## Data types and purpose
- Buildings: footprints today and 50 years ahead, with attributes for multi-hazard risk.
- Land uses: current and 50-year land use plans.
- Vulnerability: tabular functions describing building vulnerability to earthquakes and floods.
- Household: socio-demographic attributes of households (education, age, gender, employment status, etc.).
- Hazards: spatial representations of earthquake (eq), floods (fl), and debris flows (df) for study areas.
- Purpose: support monitoring, evaluation, and decision-making for environmental health and disaster risk across different urban development scenarios.

## File formats and naming
- Formats: .csv, .shp, .shx, .prj, .dbf, .cpg, .qpj, .tif, .json (combining spatial and tabular data).
- Scenarios and structure:
  - TV0: current baseline
  - TV50_s1: future buildings with urbanization not considering climate adaptation
  - TV50_s2: future buildings with climate adaptation
- Examples of file names include vulnerabilityInventory_TV0.csv, vulnerabilityInventory_TV50.csv, buildingsTV0*.shp, buildingsTV50_s1*.tif, polygonsTV0/TV50*, householdTV50.json, and hazard rasters (EQ_PGA_eq1.tif, FL_depth_fl1.tif, DF_depth_df1.tif), among others.

## Variables and data structure
- PolygonsTV50: land-use plan for 50 years with attributes such as id, type, population, densityCap, density, typeSocial, newBuild, newPop, area.
- PolygonsTV0: current land-use polygons with similar attributes (excluding 50-year changes).
- BuildingsTV0: current building footprints with polyID, polyType, Nhouse, vulnerability strings (vulnStrEQ, vulnStrFL), population, BldArea, xcoord, ycoord, and other identifiers.
- BuildingsTV50_s1: future buildings (without climate adaptation) with attributes like id, polyid, polytype, width, height, Nhouse, population, vulnerability, coordinates.
- BuildingsTV50_s2: future buildings (with climate adaptation) with similar attributes to TV50_s1.
- HouseholdTV50.json: socio-demographic attributes per household (Age, College, Education_A, Gender, Poverty, School, Unemployed, Work, Household_no).
- Hazards rasters (e.g., FL_depth_fl1.tif, FL_depth_fl2.tif; EQ_PGA_eq1, EQ_PGD_eq1, EQ_PGV_eq1) with metadata on extents, pixel size, data type, and statistical summaries.
- Supporting metadata describes units (Integer64, Real, etc.), and spatial extents for each dataset.

## Spatial coverage and data sources
- Geographic focus: Kathmandu, Nepal (approx. 500 ha).
- Data sources:
  - Spatial foundations from OpenStreetMap (buildings, roads, land use)
  - Socio-economic data from World Bank and United Nations
  - Hazard modeling data and methods (flood, earthquake, debris flows) with references to established models and local partners
- Extents and coordinate details provided for each dataset, including pixel sizes and spatial resolutions.

## Collection, transformation, and process
- GIS-based workflow using QGIS to manipulate, visualize, and store data.
- Interdisciplinary collaboration (approx. 30 meetings across structural engineering, geoscience, social science, and GIS) to integrate social and physical dimensions.
- Data structure development emphasizes a GIS-based layered approach: land-use plan (vector), buildings (vector), households (tabular), and hazards (rasters).
- Exposure data generation is a hybrid process: predictive (projecting physical and socio-economic attributes) and exploratory (creating multiple future scenarios) to support risk-informed decision making under uncertainty.
- Population and exposure are generated via bespoke algorithms (MATLAB) and synthetic social data produced to reflect projected characteristics.
- Building footprints derive from sample OpenStreetMap data, modified for realism; hazards are modeled with specialized tools:
  - Floods: Caesar-Lisflood (integrated hydrological and landscape evolution)
  - Landslides: DEM-based analysis from tri-stereo imagery
  - Debris flows: LaharFlow dynamic hazard model
- Vulnerability functions are informed by local partners and global databases (e.g., Joint Research Center).
- Data governance considerations include metadata enrichment and public data sharing constraints.

## Quality control
- Spatial topological errors addressed with QGIS topology debugging modules.

## Monitoring framework implications and governance
- Demonstrates the value of an integrated, GIS-based exposure monitoring framework that can:
  - Support multi-hazard risk assessment under different urban development and adaptation scenarios
  - Enable policy monitoring and evaluation over time with standardized data structures
  - Highlight data governance needs: metadata quality, data provenance, openness vs. governance, and mechanisms to share underlying data
  - Address common monitoring challenges: data gaps, access barriers, organizational data silos, and the burden of metadata and data management
- The hybrid scenario approach (TV0, TV50_s1, TV50_s2) provides a basis for comparing risk outcomes under different urban planning and adaptation choices.

## Supporting information and references
- Real-world methods and literature informing hazard, vulnerability, and exposure modeling:
  - Jenkins et al., 2022 (multi-hazard physics-based simulations)
  - Gentile et al., 2022 (physical impact models for multi-hazard risk)
  - Menteşe et al., 2023 (future exposure modeling for urban planning)
- Data production procedures and partnerships include local urban planning experts and international datasets.