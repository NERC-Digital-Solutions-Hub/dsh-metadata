# Field measurements of peatland carbon cycling at a wind farm hosting peatland in Scotland, UK.

## Overview
- Field-based investigation of spatio-temporal variability in abiotic and biotic controls on peatland carbon cycling at Black Law Wind Farm, Scotland.
- Timeframe: fieldwork Feb 2011–Apr 2013; year-long GHG and pore water DOC campaign May 2011–May 2012.
- Study site: blanket bog peatland within Black Law Wind Farm (55°46′01″N, 3°44′20″W; 250–320 m altitude), covering 18.6 km2 with bog, grassland, and plantation forestry.
- Design: four sites (A–D) along a SW–NE transect; within each site, 12 plots (n=48 total) across four blocks dominated by plant functional types (PFTs: mosses, sedges, shrubs).

## Spatial and Temporal Coverage
- Spatial
  - 4 sites, 48 plots across transect.
  - Each plot sampled within a 400 cm2 quadrat; plots distributed to capture microtopography and vegetation diversity.
  - Detailed site descriptions include peat depth variation, hummocky vs. shrubby conditions.
- Temporal
  - Sampling of plant–soil properties Feb 2011.
  - Ongoing measurements Feb 2011–Apr 2013 for belowground temperature (5 cm) and soil moisture.
  - One-year continuous GHG flux and pore water DOC monitoring (May 2011–May 2012).
  - Litter decomposition study conducted March 2012–April 2013 (litter bags retrieved after 386 days).

## Data Components and Key Variables
- Plant–soil properties
  - Total carbon (%), total nitrogen (%), C:N ratio for peat, litter, and vegetation.
  - C and N stocks (g C or N m-2) for surface peat and litter (to 15 cm depth) and bulk density (g m-3).
  - Soil moisture (%), pH.
  - Peat microbial community composition via phospholipid fatty acids (PLFAs); includes bacteria (Gram+ and Gram−), fungi (saprotrophic and ectomycorrhizal), and total PLFA; derived ratios (F:B; Gram+ vs Gram−).
- Peatland carbon cycling
  - Litter decomposition (% initial mass remaining) for each PFT.
  - Dissolved organic carbon [DOC] in pore water (mg L−1).
  - Greenhouse gas fluxes: CH4 and CO2 (fluxes and flux components), net ecosystem exchange (NEE), ecosystem respiration (Reco), photosynthesis (Pcal).
  - Data processing notes: exclusion of extreme CH4 fluxes (ebullition events) using established thresholds; flux units standardized to mg CO2–C or CH4–C m−2 h−1.
- Physical parameters
  - Belowground peat temperature (5 cm depth) and soil moisture content (various blocks/sites).
  - Temperature logged at 30-minute intervals; moisture logged at 30-minute intervals (sites A–D with varying logger configurations).
- Litter and decomposition methods
  - Litter bags: 0.50 g air-dried litter per bag; 1 mm mesh; deployed March 2012; retrieved April 2013; percent mass remaining calculated.
  - Litter sources: Calluna vulgaris, Eriophorum vaginatum, Sphagnum litter; fresh deposition represented by capitulum tissue for Sphagnum.
- Sampling and analytical methods
  - Instruments: LECO CN analyzer; pH meter; GC with FID; EGM-4 portable IR gas analyser; Thermalox Total C analyser; Onset Hobo loggers; Campbell loggers (CR1000, CR200) with CS616/CS625s probes.
  - Pore water collection from 22 mm dip wells; samples stored at 4 °C, filtered to 0.7 µm, analyzed within two months.
  - PLFA extraction and GC quantification with internal standards; microbial group identification following established references.

## Field Design and Sampling Details
- Study area and sampling framework
  - Four sites along a SW–NE transect within an 18.6 km2 blanket bog landscape.
  - At each site, 12 plots organized into blocks dominated by a single PFT; 48 plots total.
  - In each plot: peat, litter, and vegetation samples collected from a 400 cm2 quadrat.
  - Peat cores (5 cm diameter, 15 cm depth) collected for C and N content and bulk density calculations.
- Litter and decomposition
  - Litter collected by PFT; decomposition monitored via 0.50 g air-dried litter in 5 mm × 5 mm bags with 1 mm mesh; bags placed beneath litter layer March 2012 and retrieved April 2013.
- GHG and pore water monitoring
  - Static chamber method for CO2 and CH4 fluxes; collars inserted at least six weeks prior to first measurement.
  - Pore water DOC sampled from surface to 15 cm depth; analyzed with Total C analyser.
- Microbial and chemical analyses
  - PLFA-based microbial community profiling from peat cores collected seasonally (Feb, Apr, Jul, Oct 2011).
  - Comprehensive PW and plant–soil chemistry analyses to support C and N stock calculations.

## Measurements and Instrumentation
- Temperature and moisture
  - Peat temperature: 5 cm depth; continuous 2011–2012 at most blocks/sites.
  - Soil moisture: multiple blocks/sites; continuous 2011–2013 with various Campbell loggers and probes.
- GHG fluxes
  - CO2 and CH4 fluxes measured with static chambers and portable gas analysis; fluxes expressed as mg CO2–C or CH4–C m−2 h−1.
  - PCal and NEE derived from flux data; extreme flux events filtered to reduce measurement error.
- DOC and carbon/nitrogen
  - [DOC] measured in pore water; C and N in peat, litter, vegetation via CN analyzer; bulk density used to compute surface C and N stocks (g m−2).
- Litter decomposition
  - Mass loss from litter bags used to quantify decomposition rates (% initial dry mass).

## Data Processing, Quality, and Documentation
- Data quality controls include calibration against standards, cross-checks against institutional references, and exclusion of anomalous CH4 fluxes.
- Spatially explicit data enable aggregation to plot-level and site-level GIS representations; temporal data support time-series visualization across plots and sites.
- Documentation references standard methods (e.g., Levey et al., Ward et al., Frostegård et al.) to ensure reproducibility.

## GIS and Data Visualization Opportunities
- Build GIS layers from the dataset:
  - Plot points with attributes: site, block, PFT, litter type, peat depth, pH, bulk density, C/N, C and N stocks, moisture, temperature, PLFA-derived microbial metrics.
  - Site polygons representing the four transect sites; overlay with wind farm infrastructure and land cover.
  - Time-series layers for GHG fluxes (CO2, CH4), NEE, PCal, Reco, and DOC across plots and through time.
  - Litter decomposition rates by PFT and plot.
- Potential analyses
  - Spatial patterns of carbon stocks and fluxes in relation to microtopography, PFT distribution, and moisture.
  - Correlations between microbial community composition (PLFAs) and CO2/CH4 fluxes or DOC.
  - Temporal dynamics of CH4 flux with ebullition-excluded data.

## Limitations and Considerations for GIS Specialists
- Data are rich but heterogeneous across data types (chemical, microbial, physical, GHG, and decompositional metrics); plan for metadata alignment and unit standardization.
- CH4 fluxes include ebullition-excluded subsets; ensure clear documentation of filtering criteria when visualizing or modeling.
- Spatial resolution is plot-level (48 plots) within four sites; derive interpolations or aggregations carefully to avoid over-interpretation of fine-scale variability.
- Temporal coverage varies by variable (e.g., continuous temperature/moisture vs. annual/panel GHG measurements); align time series accordingly for analyses.