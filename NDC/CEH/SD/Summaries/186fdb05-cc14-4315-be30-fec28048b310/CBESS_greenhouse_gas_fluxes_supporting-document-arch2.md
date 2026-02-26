# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) greenhouse gas fluxes in saltmarsh and mudflat habitats.

## Overview
- Dataset of greenhouse gas fluxes (CO2, CH4, N2O) measured from small benthic chambers in saltmarsh and mudflat habitats.
- Derived metrics include: CO2 fluxes as Net Primary Productivity (NPP) and Benthic Community Respiration (BCR); CH4 and N2O fluxes under darkness; ancillary variables include PAR, air temperature, and air pressure.
- Data processing standardizes fluxes to units: μmol CO2 m-2 h-1 (CO2), nmol CH4 m-2 s-1 (CH4), nmol N2O m-2 s-1 (N2O).

## Study sites and sampling design
- Locations and sites:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP)
- Coordinates provided for each site; habitat types include saltmarsh and mudflat.
- Soil/habitat contrasts:
  - Essex: clay soils (saltmarsh), cohesive clays/mud for mudflats.
  - Morecambe Bay: sandy soils (saltmarsh), coarser sediments in mudflats.
- Temporal coverage: field campaign conducted in winter and summer 2013.
- Sampling design: one replicate in seven of twenty-two quadrats (coverage across sites and habitats).

## Variables and measurements
- Primary gas fluxes:
  - CO2: calculated as NPP and BCR; GPP = NPP + BCR.
  - CH4 and N2O: fluxes measured under darkness.
- Ancillary measurements: Photosynthetically Active Radiation (PAR), air temperature, air pressure.
- Observation scope included both biogeochemical fluxes and environmental context.

## Methods and calculations
- Field methods:
  - Benthic chamber setup: ~0.091 m2 substrate enclosure inserted ~1.5 cm into sediment.
  - CO2 fluxes measured at the substratum/air interface using an infrared CO2 gas analyzer; data logged at 30-second intervals.
  - CH4 and N2O: headspace gas samples (20 mL) collected at five time points during dark incubation; analyzed by gas chromatography (CH4 via Flame Ionisation Detector; N2O via Electron Capture Detector).
- Data processing:
  - CO2: CO2 fluxes derived from linear regression of CO2 concentration against time; slope converted to μmol CO2 m-2 h-1.
  - CH4/N2O: fluxes derived via linear regression or hierarchical nonlinear regression (HMR) depending on transport mechanism (diffusion vs. ebullition); significance threshold p < 0.05.
  - Standardization uses chamber volume, surface area, temperature, pressure, and gas constants to express fluxes consistently.
- Weather/local reference:
  - Temperature and pressure values obtained from Blackpool or Southend airports for Morecambe Bay and Essex sites, respectively.

## Data formats and quality control
- Data formats:
  - CO2 flux data: downloaded as TXT from data logger, opened in Excel; saved as Excel workbook.
  - CH4/N2O data: downloaded as CSV from GC, opened in Excel, saved as Excel workbook.
- Quality control:
  - NA values indicate measurements not performed.
  - Metadata includes dataset field descriptions and operational details for traceability.
- Data storage and accessibility:
  - Data are prepared for standard CBESS data practices and uploaded to appropriate data portals.

## Dataset fields and schema
- Key fields (examples):
  - Season (Winter/Summer)
  - Location (Morecambe/M), Essex (E)
  - Site (CS, WS, WP; AH, FW, TM)
  - Habitat (Mudflat, Saltmarsh)
  - Quadrat (1–22)
  - Scale (A–D with corresponding numeric ranges)
  - Time/Date, Record
  - Chamber size (volume in litres)
  - PAR, Air Pressure, Air Temperature
  - NPP.flux, BCR.flux, GPP.flux
  - CH4 flux, N2O flux
  - Linear regression type (LR or HMR)
  - Comments (notes on sample availability or processing)
- The dataset provides two variants of field descriptions and header details to support data interpretation and sorting.

## Practical considerations for analysis and use
- Comparisons across habitats and soil types (clay vs. sand) and inundation regimes are facilitated by standardized flux calculations.
- CH4 and N2O fluxes require careful interpretation due to transport mechanisms (diffusion vs. ebullition) and the chosen regression approach.
- Missing data are clearly indicated (NA), and site-specific context is essential when aggregating results.
- Metadata enables reproducibility of calculations and downstream ecological interpretation within CBESS monitoring frameworks.