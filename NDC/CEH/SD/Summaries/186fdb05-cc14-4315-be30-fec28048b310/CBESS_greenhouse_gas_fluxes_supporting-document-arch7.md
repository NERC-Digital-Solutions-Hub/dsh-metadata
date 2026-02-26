# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) greenhouse gas fluxes in saltmarsh and mudflat habitats

- Purpose and content
  - Dataset of greenhouse gas fluxes measured from small benthic chambers in saltmarsh and mudflat habitats.
  - Observed CO2 fluxes (as Net Primary Productivity NPP and Benthic Community Respiration BCR), and CH4 and N2O fluxes under darkness.
  - Additional measurements: Photosynthetically Active Radiation (PAR), air temperature, and air pressure.
  - Two incubations per quadrat (ambient light and dark) to derive NPP, BCR, and GPP (GPP = NPP + BCR).

- Study sites and locations
  - Essex (two habitat contrasts): Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay (two habitat contrasts): Cartmel Sands (CS), Warton Sands (WS), West Plain (WP)
  - Coordinates provided for each site (degrees and minutes). Essex sites use clay-rich sediments; Morecambe Bay sites use sandy sediments. Saltmarsh sites differ in inundation, creek structure, and vegetation. Mudflat sites differ in sediment type (Essex: cohesive clays; Morecambe: coarse, mobile sediments).

- Temporal scope
  - Field campaign conducted in winter and summer 2013.

- Data collection and methods
  - CO2 fluxes
    - Measured at the substratum/air interface with a benthic chamber (~0.091 m2) inserted ~1.5 cm into sediment.
    - Instrument: infrared CO2 gas analyser; data logged every 30 seconds.
  - CH4 and N2O fluxes
    - Headspace gas samples (20 mL) collected at five time points during the dark incubation using gas-tight syringes; samples stored in Exetainer bottles.
    - Analysis: gas chromatography (Thermo TRACE GC Ultra) with Flame Ionisation Detector for CH4 and Electron Capture Detector for N2O.
  - Calculations and interpretations
    - CO2: NPP and BCR derived from linear regression of CO2 concentration over time; GPP = NPP + BCR.
    - CH4 and N2O: fluxes derived via Linear Regression (LR) or Hierarchical Multiple Nonlinear Regression (HMR) depending on concentration rise dynamics.
    - Fluxes standardised to surface area and chamber volume; calculations use temperature-corrected molar volume and a gas constant R.
  - Transport assumptions
    - CH4 and N2O fluxes deduced under diffusion-dominated transport or ebullition as appropriate per method (LR or HMR).

- Data formats and quality control
  - CO2 flux data: exported from data logger as TXT and opened in Excel; later saved as Excel workbook.
  - CH4 and N2O data: exported from Gas Chromatograph as CSV and opened in Excel; later saved as Excel workbook.
  - NA values indicate measurements not performed.
  - Quality control fields exist (with placeholders indicating levels of data checking); some entries are not filled.
  - Dataset fields described include metadata such as season, location, site, habitat, Quadrat, scale, time, chamber size, PAR, air pressure, air temperature, and flux measurements.

- Dataset schema and key fields (examples)
  - Sequence and description headers; row numbering for sorting.
  - Season (Winter or Summer), Location (Morecambe or Essex), Site (CS, WS, WP, AH, FW, TM).
  - Habitat (Mudflat or Saltmarsh), Quadrat number (1–22), Scale categories (A–D with corresponding ranges).
  - Metadata: Time of Day/Date, Chamber size/volume, PAR, Air Pressure, Air Temperature.
  - Flux fields: NPP.flux, BCR.flux, GPP.flux, CH4 flux, N2O flux.
  - Processing notes: Linear regression type (LR or HMR), Comments on sample availability for CH4/N2O analysis.

- Practical GIS implications and potential map products
  - Spatially explicit maps of CO2, CH4, and N2O fluxes by site and habitat type (saltmarsh vs mudflat) across Essex and Morecambe Bay.
  - Seasonal or time-of-day layers to compare winter vs summer flux patterns and light vs dark incubations.
  - Habitat-specific risk or influence analysis by soil type (clay vs sandy) and inundation regime.
  - Integrated data layer combining flux metrics with environmental covariates (PAR, temperature, pressure) for spatial modelling.
  - Data prepared for standard GIS formats and map-based dashboards highlighting spatial distribution of gas fluxes and productivity (GPP, NPP, BCR).