# Topsoil carbon concentration estimates from the Countryside Survey of Great Britain, 2007 using a Generalized Additive Model

## Aim and scope
- Presents 2007 national topsoil carbon concentration estimates (0–15 cm depth) for Great Britain at 1 km2 resolution.
- Demonstrates a Generalized Additive Mixed Model (GAMM) approach to model topsoil carbon as a function of climate, deposition, habitat/soil variables, and space.
- Serves as a data product to support environmental health monitoring and policy evaluation.

## Data sources and predictors
- Field data: 2446 sampling locations from the Countryside Survey (CS) 2007.
- Spatial unit: samples nested within 1 km2 CS squares.
- Predictors include:
  - Climate: 5-year mean summer/winter/spring temperatures and precipitations (5 km resolution, 2003–2007).
  - Atmospheric deposition: 3-year mean NH4, NO3, and SO4 deposition (5 km resolution, 2005+; data from CBED/Met Office sources).
  - Land/habitat variables: Broad Habitat classes, Land Cover 2007, Soil Group, Soil Parent Material Model.
  - Spatial terms: two-dimensional tensor product smooths over easting/northing (1 km resolution) to capture large-scale spatial variation.
- Statistical framework:
  - Tweedie distribution (variance function ~ 1.99) within a GAMM (mgcv in R).
  - Random effect to account for nesting within 1 km2 CS squares.
  - Non-linear smooths for climate and deposition; smooth spatial interactions via te terms.

## Model specifics and outputs
- Model: Generalized Additive Mixed Model (GAMM) applied to 2007 soil carbon data.
- Outcome: mean topsoil carbon concentration ( Soil_OrgC_Conc ) in g kg-1; includes standard error ratio (VAR).
- Modelling notes:
  - Based on 2446 locations; uses a combination of climate, deposition, habitat, soil variables, and spatial structure.
  - Full methodological details are published in Thomas et al. (2020) and earlier CS technical reports (Emmett et al. 2008, 2010).
- Data product:
  - Dataset: CS_topsoil_carbon_gam.nc
  - Key attributes: Soil_OrgC_Conc (mean 2007 modeled carbon concentration; units g kg-1); VAR (standard error/ratio); coordinates in OSGB 1936 / British National Grid (x, y in metres).

## Data attributes and data governance
- Metadata and data attributes:
  - x (Easting) and y (Northing) coordinates; spatial reference OSGB 1936; 1 km and 5 km resolution handling for inputs.
  - Transverse Mercator mapping reference provided.
- Data provenance and QA:
  - Field sampling and laboratory methods described (LOI-based carbon estimation, conversion factor 0.55; CEH SOP3102; QA procedures per Defra/NERC Joint Codes).
  - Technical reports underpinning the methodology (Emmett et al. 2008; 2010; Reynolds et al. 2013).
- Accessibility and sharing:
  - The dataset is documented with detailed metadata and is designed to be shareable, aligning with data governance and openness expectations; references to supporting data sources and versions are provided.

## Sampling, calibration, and quality control
- Sampling method: 15 cm long, 5 cm diameter soil cores; LOI on 10 g dried sample; carbon concentration estimated by LOI × 0.55 based on regression with total carbon measured by elemental analysis.
- Calibration and quality control follow UK CEH and DEFRA/NERC practice; methodology published in Countryside Survey technical reports.

## Supporting documents and references
- Thomas et al. (2020): Patterns and trends of topsoil carbon in the UK; complex interactions of land use change, climate, and pollution (Science of the Total Environment).
- Reynolds et al. (2013); Emmett et al. (2008, 2010): Countryside Survey soils manuals and soils reports.
- Henrys et al. (2012); Morton et al. (2014); CBED/Met Office materials cited for predictor data sources.
- BGS Soil Parent Material Model (2010) and Land Cover Map 2007 references.
- Additional context: related atmospheric deposition model inter-comparisons (Dore et al. 2015).

## Implications for monitoring frameworks
- Demonstrates integrating multi-source data (climate, deposition, land cover, soil/class predictors) to produce spatially explicit health indicators for policy scrutiny.
- Shows practical handling of data gaps and spatial heterogeneity via GAMM, improving the reliability of national-scale monitoring indicators.
- Highlights data governance considerations: metadata completeness, provenance, and transparency of modelling choices to support reproducibility and stakeholder scrutiny.
- Illustrates how a monitoring framework can convert survey data into model-based estimates with clear documentation, enabling consistent reporting and informing future decision-making.