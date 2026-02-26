# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) greenhouse gas fluxes in saltmarsh and mudflat habitats

## Overview
- Dataset measuring greenhouse gas fluxes (CO2, CH4, N2O) in saltmarsh and mudflat habitats using small benthic chambers.
- Terminal aim: provide data to analyse productivity and respiration dynamics and to assess GHG exchange in coastal ecosystems.
- Temporal scope: field campaign conducted in winter and summer 2013.
- Coverage: two UK regions (Essex and Morecambe Bay) across multiple sites and habitat types.

## Locations and sampling design
- Staff responsible: Claire Golléty.
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Habitat representation:
  - Saltmarsh: two contrasting soil types in Essex (clay) and Morecambe Bay (sandy).
  - Mudflat: Essex (cohesive clay/mud/silt) vs. Morecambe Bay (coarse, mobile sediments).
- Quadrat sampling: 22 quadrats in total, with one replicate in seven of them.
- Spatial scale: site-level coordinates provided; precise location descriptions include latitude/longitude.

## Measurements and observed variables
- Primary fluxes:
  - CO2 fluxes with benthic Net Primary Productivity (NPP) and Benthic Community Respiration (BCR); Gross Primary Productivity (GPP) = NPP + BCR.
  - CH4 and N2O fluxes measured under darkness.
- Additional variables:
  - Photosynthetically Active Radiation (PAR), air temperature, air pressure.
- Specifics:
  - CO2 fluxes measured at the substratum/air interface using a benthic chamber (0.091 m2 substrate area), inserted ~1.5 cm into sediment.
  - CO2 data collected with an infrared gas analyser; data logger recorded at 30-second intervals.
  - CH4 and N2O fluxes derived from 20 mL headspace gas samples taken at five time points during the dark incubation.
  - Gas samples analyzed with a Thermo TRACE GC Ultra: CH4 by Flame Ionisation Detector (FID) and N2O by Electron Capture Detector (ECD).

## Procedures and data processing
- CO2 flux determination:
  - Fluxes calculated by fitting a linear regression to CO2 concentration versus time; slope yields NPP and BCR.
  - GPP derived as the sum of NPP and BCR.
- CH4 and N2O processing:
  - Fluxes calculated using either linear regression (diffusion-dominated) or Hierarchical Multiple nonlinear Regression (HMR) for non-linear increases (ebullition scenarios) following Hutchinson and Mosier (1981); significance set at p < 0.05.
  - Fluxes standardized to a per-area and per-time basis using chamber dimensions and environmental conditions (temperature, pressure) via ideal gas relationships.
- Unit conventions:
  - CO2: μmol CO2 m-2 h-1
  - CH4: nmol CH4 m-2 s-1
  - N2O: nmol N2O m-2 s-1

## Data formats and accessibility
- Data handling:
  - CO2 flux data downloaded as TXT from data loggers and opened in Excel.
  - CH4 and N2O data downloaded as CSV from the gas chromatograph and opened in Excel.
- Metadata and data structure:
  - Dataset includes comprehensive field descriptions and a consistent header schema to aid interpretation.
  - Key fields captured: season, location, site, habitat, quadrat, scale, record, time, chamber size, PAR, air pressure, air temperature, flux values (NPP, BCR, GPP, CH4, N2O), regression type, and comments.

## Dataset fields and structure
- Field categories:
  - Temporal and sampling details: Season, Time of Day/Date, Record.
  - Spatial and habitat identifiers: Location (Morecambe or Essex), Site (CS, WS, WP, AH, FW, TM), Habitat (Mudflat, Saltmarsh), Quadrat.
  - Measurement scale and data packaging: Scale (A-D), Chamber size, PAR, Air Pressure, Air Temperature.
  - Flux measurements: NPP.flux, BCR.flux, GPP.flux, CH4 flux, N2O flux.
  - Data processing: Linear regression type, Comments.
- Data quality note:
  - NA values indicate measurements not performed, with accompanying metadata in the comments where applicable.

## Quality control and data management
- Quality control indicators exist within the dataset (e.g., notes on data availability and method-specific notes).
- Clear documentation of methods, calibration assumptions, and standardization procedures to enable reproducibility and cross-study comparisons.
- Metadata-rich design facilitates discoverability and re-use, including site-level context and procedural details.

## Potential analyses and uses
- Correlation analyses between environmental drivers (PAR, temperature, pressure) and GHG fluxes (CO2, CH4, N2O).
- Comparative analysis of flux dynamics across habitat types (saltmarsh vs mudflat) and soil types (clay vs sand) between Essex and Morecambe Bay.
- Modelling of Net Primary Productivity and respiration dynamics to estimate ecosystem carbon balance.
- Meta-analyses across sites to assess regional differences in GHG fluxes in coastal ecosystems.

## Limitations and considerations for analysts
- Spatial and temporal coverage is limited to two regions and a 2013 field campaign; replication at each quadrat is limited (one replicate in seven quadrats).
- Data processing relies on specific modeling choices (LR vs HMR) for CH4/N2O fluxes; interpretation may depend on transport mechanisms (diffusion vs ebullition).
- Data formats and accessibility are described, but researchers may need to align to their own data pipelines (e.g., convert Excel-derived files back to raw formats if needed).
- The dataset provides rich metadata but template-specific fields may require careful alignment when integrating with other data sources.