# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) greenhouse gas fluxes in saltmarsh and mudflat habitats

## Overview
- Dataset documents greenhouse gas fluxes (CO2, CH4, N2O) in saltmarsh and mudflat habitats using small benthic chambers.
- Includes measurements of CO2 fluxes linked to Net Primary Productivity (NPP) and Benthic Community Respiration (BCR); CH4 and N2O fluxes measured under darkness.
- Field campaign conducted in winter and summer 2013.
- Staff responsible: Claire Golléty.
- Observations from two regions in the UK: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands, West Plain).

## Data contents and design
- Sampling design: one replicate in seven of 22 quadrats for CO2, CH4, and N2O fluxes.
- Variables observed: CO2 fluxes (NPP, BCR), CH4 and N2O fluxes under darkness, Photosynthetically Active Radiation (PAR), air temperature, and air pressure.
- Location and habitat diversity: Essex and Morecambe Bay include contrasting sediment/soil types (clay vs. sandy soils) and habitat types (saltmarsh vs. mudflat), with differences in inundation, creek structure, and vegetation.
- Instruments and measurements:
  - CO2: benthic chamber at substratum/air interface (about 1.5 cm into sediment), connected to infrared gas analyser; two incubations per quadrat (ambient light and darkness) to derive NPP and BCR.
  - CH4 and N2O: headspace gas samples analyzed by gas chromatography (CH4 by FID; N2O by Electron Capture Detector).
- Derived metrics:
  - CO2: GPP calculated as NPP + BCR.
  - CH4/N2O: fluxes derived via Linear Regression or Hierarchical Multiple nonlinear Regression, depending on gas behavior.
- Standardization and units:
  - CO2 fluxes expressed as μmol CO2 m^-2 h^-1; CH4 and N2O as nmol m^-2 s^-1.
  - Flux calculations normalized to chamber surface area and volume, temperature, atmospheric pressure, and gas constants.

## Methods, data processing, and quality control
- Observation procedures:
  - CO2: 0.091 m^2 substrate chamber inserted ~1.5 cm into sediment; 30-second data logging for CO2 mole fraction changes.
  - CH4/N2O: five headspace samples collected during dark incubation; samples stored in pre-evacuated bottles and analyzed via GC.
- Processing details:
  - CO2: slope of CO2 concentration vs. time used to estimate NPP and BCR.
  - CH4/N2O: fluxes computed using LR or HMR depending on diffusion vs. ebullition dynamics.
- Data availability and formats:
  - CO2 data exported from data logger as TXT, opened in Excel; CH4/N2O data exported as CSV, opened in Excel.
  - Data subsequently saved as Excel workbooks.
- Quality control and metadata:
  - NA values indicate non-performed measurements.
  - Metadata fields include a detailed dataset description and a structured set of variables for sorting and analysis.

## Dataset structure and field descriptions
- Key fields include:
  - Season (Winter or Summer)
  - Location (Morecambe or Essex)
  - Site (e.g., CS, WS, WP for Morecambe; AH, FW, TM for Essex)
  - Habitat (Mudflat or Saltmarsh)
  - Quadrat (1–22)
  - Scale (A-D with corresponding numeric ranges)
  - Record (data entry order)
  - Time of Day/Date
  - Chamber size/Volume
  - PAR (photosynthetically active radiation)
  - Air Pressure and Air Temperature
  - NPP.flux, BCR.flux, GPP.flux (CO2 fluxes)
  - CH4 flux, N2O flux
  - Linear regression type (LR or HMR)
  - Comments (notes on sample availability or other considerations)
- Data notes:
  - NA values denote missing measurements.
  - Some fields are represented with paired descriptors (e.g., Season 1=Winter, Season 2=Text) indicating data organization in the source files.
  
## Access, provenance, and reuse considerations
- Provenance: field campaign conducted in 2013 across two UK regions; data collected via standardized chamber methods and GC analysis, with explicit calculation procedures documented.
- Data formats support: text/CSV data from field instruments and GC, plus Excel-ready outputs for analysis.
- Reuse considerations for data leaders:
  - Ensure consistent units and methods when integrating with other CBESS datasets (CO2, CH4, N2O fluxes, PAR, temperature, and pressure).
  - Account for partial replication (seven out of 22 quadrats) and per-quadrat missing data (NA entries).
  - Leverage detailed metadata and field-level descriptions to support cross-site comparisons and data discovery.

## Notable limitations and opportunities
- Limitations:
  - Replication is limited (one replicate per selected quadrat), which may affect spatial representativeness.
  - Data are from a specific field campaign (2013); temporal scope is limited to winter/summer seasons.
  - Some measurements are incomplete (NA entries) and require careful handling during analysis.
- Opportunities for data leaders:
  - Integrate with other CBESS datasets to build broader GHG budgets across habitats.
  - Consolidate formats and metadata into a standardized schema to improve discoverability and reusability.
  - Use the rich methodological details to support benchmarking, quality assurance, and cross-study comparisons.