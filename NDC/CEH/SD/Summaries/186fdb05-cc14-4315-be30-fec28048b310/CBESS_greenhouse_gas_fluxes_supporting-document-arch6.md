# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) greenhouse gas fluxes in saltmarsh and mudflat habitats

## Overview
- Dataset of greenhouse gas fluxes (CO2, CH4, N2O) measured from small benthic chambers in saltmarsh and mudflat habitats.
- Includes related ecosystem process metrics: Net Primary Productivity (NPP), Benthic Community Respiration (BCR), and Gross Primary Productivity (GPP).
- Collected during winter and summer 2013 as part of a fieldwork campaign.
- Staff: Claire Golléty.

## Sampling and Study Sites
- Locations: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands, West Plain).
- Coordinates provided for each site.
- Habitat context:
  - Saltmarsh: two contrasting soil types (clay in Essex; sandy in Morecambe Bay).
  - Mudflat: Essex (cohesive clays, mud, silt) and Morecambe Bay (coarse, mobile sediments).
- Design: seven replicates across 22 quadrats; one replicate per Quadrat in seven out of 22 quadrats for CO2, CH4, and N2O fluxes.

## Measurements and Parameters
- Primary variables: CO2 fluxes (NPP, BCR), CH4 fluxes, N2O fluxes.
- Supporting observations: Photosynthetically Active Radiation (PAR), air temperature, air pressure.
- Timeframe: winter and summer 2013.
- Units:
  - CO2 fluxes: μmol CO2 m-2 h-1 (NPP, BCR, GPP).
  - CH4 flux: nmol CH4 m-2 s-1.
  - N2O flux: nmol N2O m-2 s-1.

## Methods
- CO2: benthic chamber placed at substratum/air interface (chamber ~0.091 m2; inserted ~1.5 cm) connected to an infrared CO2 gas analyser. Two incubations per quadrat: ambient light and darkness to derive NPP and BCR.
- CH4 and N2O: headspace gas samples (20 ml) collected at five time points during the dark incubation; analyzed by gas chromatography (Thermo TRACE GC Ultra) with FID for CH4 and Electron Capture Detector for N2O.
- Calculations:
  - CO2: linear regression of CO2 concentration vs time; slope yields NPP and BCR; GPP = NPP + BCR.
  - CH4/N2O: linear regression (LR) or Hierarchical Multiple nonlinear Regression (HMR) depending on gas behavior; fluxes derived from initial rise, with p < 0.05 criterion.
- Standardization: fluxes expressed per area and chamber volume; account for temperature, pressure, and molar volume of air.

## Data Formats and Quality Control
- Data formats:
  - CO2 fluxes: text files downloaded from data logger; processed in Excel.
  - CH4 and N2O: CSV files from gas chromatograph; processed in Excel.
- Quality control: NA values indicate measurements not performed.
- Documentation: dataset includes comprehensive field descriptions and metadata for interpretation and re-use.

## Dataset Structure (Fields)
- Core fields include:
  - Season (Winter, Summer)
  - Location (Morecambe, Essex)
  - Site (CS, WS, WP; AH, FW, TM)
  - Habitat (Mudflat, Saltmarsh)
  - Quadrat (1–22)
  - Scale (A-D; subnumeric ranges)
  - Record (entry order)
  - Time (date/time)
  - Chamber size (volume in litres)
  - PAR (μmol m-2 s-1)
  - Air Pressure (atm)
  - Air Temperature (°C)
  - NPP flux (μmol CO2 m-2 h-1)
  - BCR flux (μmol CO2 m-2 h-1)
  - GPP flux (μmol CO2 m-2 h-1)
  - CH4 flux (nmol CH4 m-2 s-1)
  - N2O flux (nmol N2O m-2 s-1)
  - Linear regression type (LR or HMR)
  - Comments (context on sample availability or data processing)
- Additional metadata fields include:
  - Time of day/date, Record order, Row number, Scale categories, and descriptive headers for dataset structure.

## Access and Notes for Data Support
- The dataset is prepared with explicit field descriptions to enable self-serve analysis and integration with other data products.
- Useful for creating dashboards, pivot tables, or reports to compare fluxes across habitats, sites, and seasons, and to support meta-analyses of coastal GHG flux dynamics.