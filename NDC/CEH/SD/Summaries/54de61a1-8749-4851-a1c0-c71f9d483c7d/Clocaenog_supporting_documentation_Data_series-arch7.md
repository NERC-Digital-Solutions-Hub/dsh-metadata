# Climoor field site in Clocaenog forest Supporting documentation for data

- Overview
  - A climate change manipulation experiment (Climoor) using automated roof technology to simulate drought and warming for upland moorland over the next 20–30 years.
  - Located in Clocaenog Forest, North East Wales; replicated drought and warming treatments with control plots.
  - Site actively monitored since 1998 with a wide suite of abiotic and biotic measurements.

- Spatial design and geography (GIS-relevant)
  - 9 plots total: 3 warming (W), 3 drought (D), 3 controls (C), arranged in a block design for replication.
  - Plot and quadrat layout documented in Appendix 1 and Appendix 2; quadrats of 0.5 m x 0.5 m; grid reference SJ019519, 53.055N, -3.465W.
  - Dominant ecosystem: wet upland heath with Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum; shrub and bryophyte communities mapped via Pin-point vegetation surveys.
  - Site and plot data suitable for linking to GIS layers (plot polygons, treatment attributes, survey quadrats, and sampling points).

- Climate change treatments
  - Drought (D): retractable polyethylene roof over 4 m x 5 m plots; reduces annual rainfall by ~20% (and ~80% of growing-season rainfall during active drought months). Operational May–Sept (1999–2011); since 2012, Apr–Oct; curtains paused in high winds (>10 m/s).
  - Warming (W): retractable aluminium mesh curtains over plots, reflecting infrared radiation to reduce night-time heat loss; rain retraction triggered by rainfall to minimize rainfall exclusion; average annual rainfall reduction ~14%. Curtains paused in high winds.
  - Each treatment type has 3 replicates; 3 control plots mirror shading from structures (n=9 total).
  - Timing and intensity varied by year (drought and warming tables included for multiple years).

- Data types and datasets (GIS-ready potential)
  - AWS meteorological data: minute-scale sensors with hourly averages; variables include temperature, relative humidity, rainfall, pressure, net radiation, solar radiation, PAR, wind. Data since 1999.
  - Micro-meteorological data (plot level): daily measurements of soil/air temperature and soil moisture; soil moisture measured via TDR and earlier methods; started around 1998–2008 onward.
  - Rainfall and rainfall chemistry: storage rain gauge (biweekly), ground-level rainfall; throughfall data collected biweekly and used to derive plot-level rainfall adjustments.
  - Water table depth: biweekly measurements using permeable tubes to bedrock (from 2009 onward).
  - Soil respiration: fortnightly measurements using collars and various CO2 flux methods (CIRAS-2, LICOR 8100, LI-COR automated systems) from 1998 onward; data converted to mg CO2-C m-2 h-1.
  - Trace gases (CH4 and N2O): measurements with static chambers; samples analyzed via gas chromatography (1999–2000, 2007–2009).
  - Net ecosystem CO2 exchange (NEE): measurements in 2002–2004 and 2011 with different chamber systems; includes respiration and photosynthesis adjustments using biomass data.
  - Photosynthesis: ambient and controlled Ci/PAR measurements across multiple years; leaf area metrics for standardization.
  - Vegetation survey data (Pin-point biomass): annual surveys (1998–2012, with additional years) using a 3-quadrat, 100-pin grid; conversion from pin-hits to biomass with species-specific calibration.
  - Canopy reflectance: NDVI and PRI indices from ground-based spectrometer (2001–2004; limited epochs).
  - Vegetation phenology, annual growth and pathogens: shoot elongation, budburst, leaf counts, and pathogen observations (1999–2009, and later years).
  - Vegetation chemistry: carbon, nitrogen, phosphorus, potassium, calcium, magnesium, lignin, tannin, alpha-cellulose, carbohydrates; green and senesced material.
  - Litterfall: monthly (1999–2002) and later less frequent; conversion to g m-2 and later to carbon/nitrogen analyses.
  - Root biomass: multiple core-based measurements (2003–2011) with varying methods; detailed biomass extraction and calibration.
  - Soil microbial biomass: chloroform fumigation method (2000, 2001, 2012).
  - Nitrogen mineralisation: soil core incubations with nitrate and ammonium analyses (1998–2004).
  - SOM, SOC and bulk density: core-based analyses aligned with N-mineralisation study (lab protocols described).
  - Soil solution and leachate chemistry: lysimeters and tensioned samplers; major ions and DOC analyses (1998–2008).

- Data processing, quality, and metadata notes
  - Data collection and processing span multiple eras and instruments; some datasets are legacy with non-uniform processing practices.
  - Units conversions provided for CO2 flux (g CO2 m-2 h-1 and µmol m-2 s-1 to mg CO2-C m-2 h-1) and explicit notes on calibration factors.
  - Throughfall and rainfall data require adjustment to derive plot-level rainfall; data gaps and infill policies documented (plot exclusion when data are compromised).
  - Biomass calibrations rely on pin-hit to biomass conversions; site-specific calibration tables provided.
  - Data quality control described as visual checks in Excel; some automated quality controls missing in legacy datasets.
  - Not all data stored in a single repository; as of the documentation, some datasets were outside the EIDC since June 2015; contact CEH Bangor for data availability.

- Ancillary site information
  - Appendix 1: Site layout overview; Appendix 2: Quadrat layout with plots; Appendix 3: Plot layout with quadrats and measurement areas.
  - Grid reference: SJ019519; coordinates 53.055N, -3.465W; upland moorland ecosystem.
  - Soil: humo-ferric podzol with variable E and Bh horizons; typical depths of eluvial horizon 6–17 cm.

- Practical implications for GIS specialists
  - Rich, multi-temporal, multi-layer dataset ideal for map-based data products: plot-level treatment maps, biomass distributions, soil carbon pools, canopy indices, phenology maps, and flux mosaics.
  - Opportunities to create GIS layers for: treatment classification (W/D/C), plot geometry, quadrat points, sampling locations, and time-series overlays (e.g., NEE, soil respiration, rainfall, soil moisture).
  - Need for data harmonization: unify plot IDs, treatment labels, units, and coordinate systems; integrate legacy processing notes into metadata for reproducibility.
  - Data gaps and variability in collection methods across years require careful handling in GIS analyses (e.g., excluding plots/times with incomplete data, documenting imputation or exclusion criteria).

- Key considerations and caveats
  - Data are dispersed across multiple datasets and years; not all data are currently stored in a single, centralized system (EIDC); coordinate with CEH Bangor for access.
  - Legacy data processing details may differ from current best practices; document provenance and methodological changes when building GIS products.
  - Throughfall and plot-level rainfall require transformation steps; ensure reproducible scripts for rainfall allocation to treatments.
  - The site’s design (replicated plots, blocks, and quadrats) provides robust spatial structure; leverage this for spatial analyses of treatment effects and ecological responses.

- How this informs GIS workflows
  - Build a geodatabase including: plot polygons with attributes (treatment, block, replication), quadrat points, sampling collars, and time-stamped measurements.
  - Create raster layers or time-enabled datasets for continuous variables (soil moisture, temperature, CO2 flux proxies) and vector layers for categorical attributes (treatment type, species presence).
  - Integrate spectral indices (NDVI680, NDVI570, PRI) with ground-truth vegetation data to map vegetation condition over time.
  - Design time-series visualizations and maps showing spatial patterns of drought and warming responses across the nine plots.

- Summary of the document’s structure (for quick GIS reference)
  - 1.0 Site information: climate manipulation site details, ecosystem description, soil type.
  - 2.0 Climate change treatment information: drought and warming treatment designs, timings, replicate layout.
  - 3.0 Equipment, protocols and data processing methodology: data types, collection methods, data processing notes.
  - 3.1–3.19: Detailed dataset sections (AWS met data, micro-meteorological data, rainfall/rainfall chemistry, throughfall, water table, soil respiration, trace gases, NEE, photosynthesis, vegetation surveys, canopy reflectance, phenology, vegetation chemistry, litterfall, root biomass, microbial biomass, nitrogen mineralisation, SOM/SOC/bulk density, soil solution).
  - Appendix: Site layout, quadrat layout, plot layout with measurement areas.