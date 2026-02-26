# Climoor field site in Clocaenog forest Supporting documentation for data

- The Clocaenog field site is an automated climate change manipulation experiment in upland moorland, using drought and warming treatments to simulate future conditions (20–30 years ahead). Established in 1998, it aims to reflect climate projections through roof-enabled drought and infrared/heat-like warming treatments.
- Location and ecosystem: Clocaenog Forest, North East Wales (53°03'19"N, 3°27'55"W). Dominant vegetation includes Calluna vulgaris (heather) with Vaccinium myrtillus and Empetrum nigrum also present. Soil is humo-ferric podzol with variable eluvial and illuvial horizons.

## Geographic scope and site layout

- Plot structure: 9 plots total (3 warming, 3 drought, 3 controls) arranged in replicates; each plot measures 4 m × 5 m.
- Appendix references include site layout and quadrat layout. Plot and quadrat coordinates/figures are provided to support GIS mapping of treatments and sampling points.

## Climate change treatments and design

- Treatments:
  - Warming (W): retractable aluminium mesh curtains over warming plots; curtains reflect infrared radiation to reduce heat loss at night; rain is partially excluded via automatic retraction after rainfall detection.
  - Drought (D): retractable polyethylene roof to exclude rainfall on drought plots during growing seasons.
  - Controls (C): scaffolding to mirror shading effects of treatment structures.
- Replication: 3 warming plots, 3 drought plots, and 3 control plots (total n = 9). Each treatment is organized in blocks to reduce experimental bias.
- Timings:
  - Drought: originally May–Sept (1999–2011) to mimic UK droughts; extended to Apr–Oct since 2012.
  - Warming: continuous night-time warming with rain-responsive roof retraction; wind limits (>10 m/s) prevent curtain operation to protect structures.
- Site-specific climate context: Mean annual rainfall around 1411 mm; mean annual temperatures and other site data are recorded, with long-term adjustments noted in Tables 1 and 2 (noting yearly drought timing and warming GDD changes).

## Data collection and data types

- Data governance: Data are gathered from AWS (on-site automated weather station) and plot-level sensors, complemented by numerous biotic and abiotic measurements. Some smaller or post-2015 data may not be stored in the main data centre (EIDC); contact CEH Bangor for full access.
- Data cadence:
  - AWS meteorological data: daily, 1999–present.
  - Micro-meteorological plot data: daily, 1998–present.
  - Rainfall (site level) and rainfall chemistry: biweekly collection; also throughfall data (plot-level rainfall) biweekly.
  - Water table depth: biweekly measurements from 2009 onward.
  - Soil respiration and trace gases (CH4, N2O): fortnightly to monthly, with high-resolution and automated measurements introduced in later years.
  - Net ecosystem CO2 exchange (NEE): in 2002–2004 and 2011; additional respiration and photosynthesis estimates derived in later years.
  - Photosynthesis: ambient and response-curve measurements across multiple years (2001–2007, with specific years highlighted).
  - Vegetation biomass and composition: Pin-point based vegetation surveys across multiple years (1998–2012, with various intervals).
  - Canopy reflectance: NDVI and PRI indices from ground-based spectroscopy (2001–2004; subset measurements in 2000–2004).
  - Vegetation phenology, growth, and pathogens: measurements from 1998 onward, with annual or periodic sampling.
  - Vegetation chemistry: carbon, nitrogen, phosphorus, potassium, calcium, magnesium, lignin, tannin, alpha-cellulose, carbohydrates, etc. (1998–present in various forms).
  - Litterfall: collected 1999–2002 (monthly), subsequently less frequent but with annual consolidation.
  - Root biomass: multiple years (2003–2013) with several sampling schemes.
  - Soil microbial biomass: chloroform-fumigation method (2000, 2001, 2012).
  - Nitrogen mineralisation: intermittent measurements (1998–2004).
  - SOM, SOC and bulk density: derived from soil cores associated with N-mineralisation studies.
  - Soil solution and leachate chemistry: lysimeters and tensioned samplers; monthly to biweekly sampling (1998–2008).
- Data formats: CSV datasets; supporting documentation in RTF; data processing notes accompany several datasets.

## Datasets and data processing highlights (examples)

- AWS meteorological data: Daily measurements (temperature, humidity, rainfall, pressure, radiation, PAR, wind); data quality control via visual/manual inspection.
- Micro-meteorological plot data: Soil/air temperature and soil moisture; daily data with hourly logging; data QC via manual review.
- Rainfall and rainfall chemistry: Biweekly rainfall measurements with chemistry analyses (pH, NO3, Cl, SO4, DOC, ammonium, etc.); biweekly sample handling and lab analyses described.
- Throughfall data: Plot-level rainfall; data used to derive percent differences from site-level rainfall; occasional data gaps and infill with year-averaged reductions when necessary.
- Soil respiration and trace gases: Legacy methods (CIRAS-2, LICOR 8100, LI-COR analyzers) with detailed conversion factors to express fluxes as mg CO2-C m-2 h-1; cautious note on legacy data processing practices.
- NEe and photosynthesis: Conversion factors between CO2 flux units; biomass-adjusted flux estimates to account for plot biomass differences.
- Vegetation measurements: Pin-point biomass calibration (Tables 5–6 provide conversion factors); annual or periodic biomass estimates across multiple species.
- Canopy reflectance: NDVI and PRI indices derived from ground-based spectrometry; data indicate spectral bands from 400–950 nm with NDVI680 and NDVI570 definitions.
- Litterfall, root biomass, soil microbial biomass, nitrogen mineralisation, SOM/SOC, soil solution: Diverse sampling schemes (destructive sampling, cores, lysimeters) with detailed lab analyses and conversion steps documented.

## GIS-relevant considerations and data readiness

- Spatial design: Plot-level geography (4 m × 5 m plots) enables GIS mapping of treatment locations, canopy, microclimate, and biotic sampling sites. Appendix materials provide exact plot and quadrat layouts to support spatial indexing.
- Temporal depth: Longitudinal data spanning 1998–present for many datasets enables trend analysis and time-series mapping of climate treatments and ecological responses.
- Data integration: Multiple data streams (weather, soil, vegetation, gas fluxes) can be integrated to create map-based data products showing treatment effects, abiotic conditions, and vegetation dynamics across the site.
- Data provenance and standards: Documentation exists for measurement methods, units, and calibration; however, some legacy datasets may not adhere to current best practices. Users should account for potential inconsistencies when integrating older data.
- Data access: Not all data are stored in the central EIDC repository; contact the listed CEH Bangor colleagues for full data access and potential data rights considerations.
- Metadata and references: Tables, appendices, and procedural notes accompany datasets, aiding reproducibility and GIS tagging (e.g., grid reference SJ019519 and lat/long coordinates in site layout).

## Key figures and access points

- Site coordinates and layout: Grid reference SJ019519; latitude/longitude 53.055°N, 3.465°W; Clocaenog field site layout and quadrat diagrams provided.
- Contact for data details: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor for specifics on datasets not in EIDC.

## Data quality, limitations, and caveats

- Legacy data handling: Some data processing steps reflect older practices; best-practice documentation may be incomplete for certain datasets.
- Data gaps and infilling: Throughfall and other plot-level datasets may have missing values; occasional infilling used, with methodology described.
- Treatment timings and hardware: Warming and drought treatments rely on mechanical systems with wind- and rain-responsive controls; data reflect these operational nuances and timing variations.
- Data scope: While many core datasets are robust and well-documented, smaller or post-2015 datasets may reside outside the central repository.

## Appendices and supplementary materials

- Appendix: Site layout and plot arrangement (useful for GIS mapping and spatial analyses).
- Appendix 1 & 2: Quadrat and plot references for mapping measurement areas.
- Appendix 3: Specific plot and quadrat identifiers (LYS, PQ, SS) and modernized plot layouts.