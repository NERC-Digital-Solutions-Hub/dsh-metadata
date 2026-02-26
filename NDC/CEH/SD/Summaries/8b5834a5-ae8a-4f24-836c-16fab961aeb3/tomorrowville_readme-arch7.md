# Tomorrowville

## Overview
- A synthetic, future-focused urban dataset representing a Global South context, centered on Kathmandu/Nepal (~500 ha).
- Designed for multi-hazard risk assessment and GIS-based analysis; explores 50-year horizons with and without climate adaptation considerations.
- Uses publicly available and generated data to create a holistic, map-based exposure model for policy, planning, and public communication.

## Data types and content
- Buildings
  - TV0: current building footprints with attributes.
  - TV50_s1: future buildings at 50 years without climate adaptation.
  - TV50_s2: future buildings at 50 years with climate adaptation considerations.
- Land uses
  - Polygons for TV0 (existing) and TV50 (future) land-use plans.
- Vulnerability
  - vulnerabilityInventory_TV0.csv and vulnerabilityInventory_TV50.csv (earthquake and flood exposure functions).
- Household
  - householdTV50.json: socio-demographic attributes (age, education, gender, poverty, employment, etc.) by household.
- Hazards
  - Earthquake: EQ_PGA_eq1 (PGA-based raster).
  - Earthquake PGD: EQ_PGD_eq1 (peak ground displacement).
  - Earthquake PGV: EQ_PGV_eq1 (peak ground velocity).
  - Floods: FL_depth_fl1.tif, FL_depth_fl2.tif (flood depth scenarios with/without climate change).
  - Debris flows: DF_depth_df1.tif (debris-flow scenario with climate change).
- Example attributes by layer
  - Polygons TV50: id, type, population, densityCap, density, typeSocial, newBuild, newPop, area.
  - Buildings TV0/TV50_s1/TV50_s2: polyID, polyType, polytypeSo, Nhouse, population, BldArea, xcoord, ycoord, and hazard exposure strings (vulnStrEQ, vulnStrFL, etc.).
  - Household: Age, College, Education_A, Gender, Poverty, School, Unemployed, Work, Household_no.

## File formats and naming
- Formats used: .csv, .shp, .shx, .prj, .dbf, .cpg, .qpj, .tif, .json.
- Examples of file groups: buildingsTV0*, buildingsTV50_s1*, buildingsTV50_s2*, polygonsTV0*, polygonsTV50*, vulnerabilityInventory_TV0.csv, vulnerabilityInventory_TV50.csv, householdTV50.json, EQ_PGA_eq1.tif, FL_depth_fl1.tif, DF_depth_df1.tif.

## Spatial coverage and data scope
- Geographic focus: Kathmandu Valley, Nepal.
- Extent and resolution described for raster hazards (pixel size and dimensions) and vector layers (polygon footprints, building centroids).

## Data generation, structure, and workflow
- GIS-centric design
  - All data layers are GIS-compatible (vector and tabular).
  - Vector features (points, lines, polygons) with integrated attribute tables; geometry-derived measures (area, coordinates) stored at backend.
  - Household and individual data stored relationally in tabular form.
- Time dimension and scenarios
  - Exposure data produced for a future time tf, using a hybrid scenario development (predictive + exploratory) to reflect multiple urban development options.
  - TV0, TV50_s1, TV50_s2 represent different urbanization and adaptation assumptions.
- Data structure process
  - Planning extent is subdivided into zones with aggregated projected land-use types.
  - Build locations and attributes are generated from land-use assumptions, hazards, infrastructure, and socio-economic projections.
  - Household and individual data derived from socio-economic projections; building layer enriched for disaster impact quantification.
- Interdisciplinary approach
  - Involves engineers, geoscientists, social scientists, and GIS specialists.
  - GIS used as a mediator to integrate social and physical characteristics, supporting holistic urban exposure modeling.
- Data production methods
  - Flood simulations: Caesar-Lisflood (Lisflood-FP + CAESAR) and stereo imagery for landslides.
  - Debris-flow: rainfall-driven LaharFlow hazard model.
  - Vulnerabilities: developed with local partners and JRC global datasets; supported by cited literature.
  - Social data: synthetic population generated via MATLAB algorithms; building footprints adjusted from OpenStreetMap data.
- Supporting materials
  - Documentation of hazard and vulnerability data sources, and links to relevant methodological references.

## Quality control and validation
- Spatial topological errors removed using QGIS topological debugging modules.
- Interdisciplinary reviews and expert input to align spatial and socio-economic representations.

## Supporting information and references
- Hazard modeling and exposure methodologies aligned with recent disaster risk reduction literature (Jenkins et al., Gentile et al., Menteşe et al.).
- Local and regional collaboration with Kathmandu and Nairobi experts for realism in spatial context and planning relevance.
- References provided for hazard, vulnerability, and exposure procedures to support reproducibility.

## Practical use and limitations
- Purpose: to produce map-based data products for risk-informed urban planning, policy support, and disaster risk reduction analyses.
- Intended use: comparative assessments across scenarios; not a forecast of actual future realization but a tool for relative risk insights and decision support.
- Limitations: synthetic socio-demographic data and hypothetical future scenarios; reliance on multiple models and data sources with inherent uncertainties.