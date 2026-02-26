# Climoor field site in Clocaenog forest Supporting documentation for data

- A climate change manipulation experiment at Clocaenog Forest (upland moorland) using automated roof technology to simulate drought and warming for the next 20–30 years.
- Location: Clocaenog Forest, North East Wales. Grid reference SJ019519; Lat/Lon 53.055°N, -3.465°W (53°03′19″N, -03°27′55″W).
- Experimental design: 9 plots (4 m x 5 m) arranged as three treatments (drought, warming, control) with three replicates each; arrangement includes blocks to mirror shading from treatment structures.
- Site characteristics: dominated by Calluna vulgaris (heather) with additional vascular and bryophyte species; humo-ferric podzol soil with variable eluvial/illuvial horizons.

## Climate change treatments and timings

- Drought treatment
  - Mirrors drought in UK, implemented May–Sept from 1999–2011; April–October since 2012.
  - Mechanism: retractable polyethylene roof over each drought plot, excluding rainfall and reducing annual rainfall by ~20% (and up to ~80% of growing-season rainfall during active drought periods).
  - Operation: roof extends when rainfall is detected by tipping-bucket sensor; curtains blocked in high winds (>10 m/s).
- Warming treatment
  - Uses retractable aluminium mesh curtains over warming plots; reflects infrared radiation to reduce nighttime heat loss.
  - Rainfall management: roof retracts during rain to minimize rainfall exclusion on warming plots; some rainfall loss persists due to sensor lag.
  - Winds: curtains disabled in high winds to prevent damage.
- Control plots
  - Mirror shading effects via scaffolding to equalize non-treatment shading.
- Documentation includes year-by-year details of drought and warming timings, site rainfall, and warming growing degree days.

## Spatial design and site layout

- Plot arrangement and quadrats documented in Appendix 1 (Site layout) and Appendix 2 ( Quadrat layout with experimental plots).
- Plot layout supports spatial comparisons across treatments and provides a framework for GIS-based analysis and mapping of measurements by plot and time.
- Key coordinates and grid references are provided for site localization and cross-referencing with GIS layers.

## Data collected and data processing methodology

- Data collection framework
  - On-site automated weather station (AWS) for meteorological data (daily, 1999–present).
  - Micro-meteorological plot sensors for soil and air temperature, soil moisture (daily, 1998–present).
  - Rainfall and rainfall chemistry using storage rain gauge and Warren spring collectors (biweekly sampling; 1998–present).
  - Throughfall data (plot-level rainfall) collected biweekly; plot-level rainfall derived by applying treatment-specific percent changes to site rainfall.
  - Water table depth using permeable tubes (installed 2009; biweekly measurements).
  - Soil respiration and trace gases (CH4, N2O) measured using soil collars and closed-chamber methods; both historic (1999–2000, 2007–2009) and automated (2013–2014) measurements.
  - Net ecosystem CO2 exchange (NEE) measured in select years (2002–2004, 2011) with different chamber systems.
  - Photosynthesis data (2001–2003 for certain species) using CIRAS-2 and leaf cuvettes.
  - Vegetation biomass surveys using Pin-point method across multiple years (1998–2012); calibration of pin-hits to biomass using species-specific factors.
  - Canopy reflectance (NDVI and PRI indices) from ground-based spectrometry (2001–2004 with some 2000–2003 measurements).
  - Vegetation phenology, annual growth, and pathogen assessments (1998–present; major measurements in 1999–2009 and thereafter).
  - Vegetation chemistry (green and senesced material) and litterfall (1998–2002; adjacent years with variable sampling).
  - Root biomass (2003–2013 with multiple methods), soil microbial biomass (2000–2001, 2012), nitrogen mineralisation (1998–2004), SOM/SOC and bulk density (1999–2004, 2013), soil solution and leachate chemistry (1998–2008).
- Data processing and units
  - Data converted to consistent flux units (e.g., mg CO2-C m^-2 h^-1 for respiration and NEE; µmol m^-2 s^-1 for some instruments).
  - Calibration and conversion factors provided (e.g., soil respiration unit conversions from CIRAS-2 and LI-COR 8100; biomass conversions from pin-hits).
  - Throughfall adjustments: percent-change method applied to site rainfall to derive plot-level rainfall; data loss leads to plot exclusion or infill with year-average reductions.
- Quality and data stewardship
  - On-site data quality control using visual checks; legacy data may not follow current best practices.
  - Some datasets are not stored in the EIDC; contact CEH Bangor for details and access (Sabine Reinsch, Bridget Emmett).

## Data storage and access

- Summary datasets described with supporting documentation; not all data stored within the EIDC beyond June 2015.
- Primary contacts for data details and access: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor.

## Appendix and site specifics

- Appendix: Site layout and Quadrat layout details for replicability and GIS mapping.
- Plot and quadrat references align with the grid used in field measurements, enabling spatial analyses across treatments and time.

## GIS-focused considerations and potential uses

- Map-ready structure: nine 4 m x 5 m plots with explicit treatment assignments and spatial layout; supports per-plot time-series analysis across multiple variables.
- Multimodal datasets: meteorological, soil moisture/temperature, rainfall throughfall, water table, soil respiration, trace gases, NEE, vegetation biomass and chemistry, litterfall, root biomass, microbial biomass, and soil solution chemistry.
- Data fusion opportunities: integrate plot-level measurements with AWS data to model spatial-temporal patterns of climate treatment effects on ecosystem processes.
- Data gaps and legacy caveats: expect some missing data or inconsistent documentation in older datasets; exercise caution when combining legacy datasets with newer measurements.
- Practical GIS outputs: treatment-specific rainfall adjustments, plot-level flux maps, biomass distribution maps, canopy indices (NDVI, PRI), phenology maps, and soil/solution chemistry gradients across the plot grid.