# Climoor field site in Clocaenog forest Supporting documentation for data

## Overview
- Climate change manipulation experiment at Clocaenog Forest, North East Wales, using automated roof technology to simulate drought and warming over the next 20–30 years.
- Site established in 1998; replicated drought and warming treatments with scaffolding-mirrored controls.
- Data cover a wide range of abiotic and biotic measurements across on-plot and site-scale contexts, suitable for GIS-based spatial analyses and map-based data products.

## Site, location, and climate treatments
- Location: upland west-atlantic moorland dominated by Calluna vulgaris (heather); grid reference SJ019519, coordinates 53.055N, -3.465W.
- Treatments and layout: two climate treatments (drought and warming) each with three replicates, plus three control plots that mirror shading from experimental structures (total n = 9 plots). Plots sized 4 m x 5 m.
- Drought treatment: operated primarily May–Sept 1999–2011 (updated Apr–Oct since 2012); rain-reducing via retractable polyethylene roof triggered by tipping-bucket sensors, removing ~20% of annual rainfall and up to ~80% of rainfall during the growing season.
- Warming treatment: retractable aluminum-curtain roofs reducing heat loss at night; rainfall-reducing effect mitigated by a rain-retraction delay after rain events; underestimated rainfall reduction around 14% annually.
- Wind considerations: curtains do not operate in winds >10 m/s to prevent damage.
- Data note: drought roofs not in operation in 2016 due to refurbishment; data logs cover 1997–2016 with varying completeness.

## Plot layout and spatial references
- Nine 4 m x 5 m plots organized into blocks; Appendix figures provide site layout and quadrat layouts.
- Spatial indexing includes quadrats within plots; detailed mapping and plot-level coordinates support GIS layering and provenance tracking.
- Appendix references indicate specific plot and quadrat designations (e.g., LYS, PQ, SS) and the overall Clocaenog site layout.

## Data types and measurements (scope, scale, and cadence)
- AWS meteorological data: daily measurements of temperature, humidity, rainfall, solar and net radiation, PAR, wind, pressure; data from 1999–present.
- Micro-meteorological (plot-level) data: daily soil and air temperature, soil moisture; 1998–present (log cadence shifted to hourly/half-hourly in later years).
- Rainfall and rainfall chemistry: site-level storage rain gauge (biweekly to monthly data) and plot-level throughfall data (biweekly); chemical analyses for NO3, Cl, SO4, DOC, NH4, pH using standardized methods.
- Water table depth: biweekly measurements since 2009 using permeable tubes to bedrock (plot-level depth limits noted).
- Soil respiration and trace gases: soil CO2 efflux, CH4, and N2O measured with collars and closed-chamber methods; protocols evolved from 1999–2000 to 2014+; automated and manual campaigns with varying frequency.
- Net ecosystem CO2 exchange (NEE): measurements in 2002–2004 and 2011; different chamber systems used; flux units converted to mg C m-2 h-1 with biomass-adjusted corrections.
- Photosynthesis: ambient and response-curve measurements (2001–2007, with several years focusing on ambient, Ci, PAR, and A-Ci curves); leaf-level measurements on Calluna vulgaris, Vaccinium myrtillus, and Empetrum nigrum.
- Vegetation biomass and structure: Pin-point (three quadrats per plot) biomass estimates from 1998–2012 with conversion factors; annual or periodic biomass calibrations; bryophytes pooled in some conversions.
- Canopy reflectance: NDVI and PRI derived from ground-based spectrometry (2001–2004, with limited 2003–2004 measurements).
- Vegetation phenology and growth: shoot elongation, budburst, leaf emergence, flowering for dominant shrubs; multi-year tracking (1998–2009+).
- Vegetation chemistry: carbon, nitrogen, phosphorus, potassium, calcium, magnesium, lignin, tannin, alpha-cellulose, carbohydrates from green and litter material; annual analyses.
- Litterfall: monthly to annual collection (1999–2002; later years less frequent); values converted to g m-2 and processed for carbon and nitrogen.
- Root biomass: multiple core-based assessments (2003–2004, 2008, 2011) with varied methods; roots separated by soil horizon and size classes.
- Soil microbial biomass: chloroform fumigation methods (2000, 2001, 2012) with DOC-based biomass estimates.
- Nitrogen mineralisation and soil properties: 1998–2004 measurements; KCl extraction for NH4 and NO3; SOM, SOC, and bulk density derived from parallel cores.
- Soil solution and leachate chemistry: lysimeters and tension samplers (1998 onward); pH, nitrate, chloride, sulfate, DOC analyses; biweekly sampling.
- Data organization: scattered across multiple data files (RTF/CSV) with some data not stored in the EIDC after mid-2015; metadata includes data provenance, sensors, methods, and time scales (see Table 3 in the document for a data summary and contact points for details).

## Data processing, quality, and caveats
- Data processing spans multiple instruments and methods (CIRAS-2, LICOR 8100, EGM analyzers, LI-6400, etc.); standardized unit conversions documented for CO2 flux data.
- Quality control relies on manual visual checks (Excel-based) in addition to instrument-based QA; some legacy processing steps not fully aligned with current best practices.
- Biomass and conversion factors (pin hits to biomass) derived from calibration experiments; ongoing adjustments and species-specific calibrations noted.
- Canopy reflectance and phenology data have limited time windows and are not uniformly available across all plots/years.
- 2016 drought roofs not in operation during refurbishment; some data gaps and reduced measurement continuity in later years.
- Data access: not all data are stored in the EIDC; for complete details and access, contact CEH Bangor staff (Sabine Reinsch and Bridget Emmett).

## Data accessibility and contacts
- Primary contacts: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor.
- Documentation references: extensive table of data types, sensors, time scales, and data structure; Appendix 1–3 provide site, quadrat, and plot layouts.

## GIS-oriented takeaways for map-based data products
- The dataset offers rich geospatial context: nine defined plots with fixed boundaries, on-plot quadrats, and a well-documented site layout suitable for layering climate treatments on maps.
- Multi-scale data coverage enables linking plot-level treatments to abiotic and biotic responses, supporting spatial-temporal analyses and visualization of drought and warming effects on vegetation, soils, and atmosphere.
- Important GIS workflows enabled by this documentation:
  - Create layers for plot treatments (W, D, C) and replicate blocks; map overlays with soil type, vegetation type, and biomass distribution.
  - Integrate climate data (AWS and micro-meteorological) with plot-level response metrics (soil respiration, NEE, litterfall, etc.) for spatial trend analyses.
  - Attach phenology, canopy reflectance, and litterfall data to plot-level polygons for time-series mapping.
  - Use plot and quadrat layouts to regionalize sampling points and generate spatially explicit summaries.