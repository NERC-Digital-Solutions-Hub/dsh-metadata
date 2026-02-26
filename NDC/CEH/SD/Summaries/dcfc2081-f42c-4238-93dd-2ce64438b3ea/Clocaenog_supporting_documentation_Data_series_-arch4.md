# Climoor field site in Clocaenog forest Supporting documentation for data

- The Climoor project is a climate change manipulation experiment at Clocaenog field site using automated roof technology to simulate drought and warming scenarios for the next 20–30 years.
- Established in 1998, the site features replicated drought and warming treatments with a control condition, designed to operate in remote upland moorland environments powered by solar and wind.

## 1) Experimental design and climate treatments

- Treatments and replication:
  - Warming (W), Drought (D), and Control (C) with three replicates per treatment across nine plots total (4 m x 5 m each).
  - Treatment structure organized into blocks to mirror shading and microclimate effects.
- Drought treatment:
  - Operated mainly May–Sep (1999–2011); since 2012, Apr–Oct.
  - Mechanism: retractable polyethylene roof over plots excludes rainfall, reducing annual rainfall by about 20% (and greater reductions during the growing season, up to about 80% of rain excluded in some periods).
- Warming treatment:
  - Retractable aluminium mesh curtains that reflect infrared radiation, reducing heat loss at night and increasing canopy temperature.
  - Roofs retract during rain to prevent rainfall exclusion; wind limits prevent curtain operation at >10 m/s.
- Control plots:
  - Scaffolding installed to mirror shading effects of the experimental structure on treatment plots.
- Site and climate context:
  - Location: Clocaenog Forest, North East Wales (53°03'19"N, -3°27'55"W).
  - Upland moorland with dominant Calluna vulgaris (heather) and accompanying bryophytes and other vascular plants.
  - Soil: humo-ferric podzol with variable horizons; E horizon typically 6–17 cm, Bh below, depth to bedrock varies.
  
## 2) Data assets and data types

- A broad suite of abiotic and biotic data collected from AWS and plot-scale instrumentation, including but not limited to:
  - AWS meteorological data (daily, 1999–present): temperature, humidity, rainfall, wind, radiation components, etc.
  - Micro-meteorological plot data (daily): soil and air temperature, soil moisture.
  - Rainfall: storage rain gauge (site-level, biweekly), rainfall chemistry (pH, NO3, Cl, SO4, DOC, ammonium).
  - Throughfall data (plot-level, biweekly): plot rainfall capture to estimate treatment-specific rainfall reductions.
  - Water table depth (since 2009).
  - Soil respiration (fortnightly high-resolution and low-frequency datasets): CO2 fluxes using various chamber-based methods and LICOR/EGM systems; adjustments for biomass.
  - Trace gases (CH4, N2O) measurement via static chambers and GC analysis.
  - Net ecosystem CO2 exchange (NEE) across selected years (2002–2004, 2011) with calibration for biomass differences.
  - Photosynthesis data (ambient and response curves) for Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum (2001–2003; earlier years with variable methods).
  - Vegetation survey data (Pin-point biomass, 1998–2012): seed/plant presence, biomass calibration, cross-year consistency with fixed quadrats and multiple plots.
  - Canopy reflectance (NDVI and PRI indices) from ground-based spectrometer (2001–2004, 2000–2004 in sub-samples).
  - Vegetation phenology, annual growth and pathogen assessment (shoot elongation, budburst, leaf number; several species across years).
  - Vegetation chemistry (C, N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates).
  - Litterfall (1999–2009): monthly sampling with litter traps; conversion to g m-2.
  - Root biomass (2003–2013): multiple soil core methods across years and plots.
  - Soil microbial biomass (chloroform fumigation, 2000–2001, 2012).
  - Nitrogen mineralisation (1998–2004): initial/final cores with NH4+/NO3- analyses.
  - SOM, SOC and bulk density (derived from soil cores).
  - Soil solution and leachate chemistry (pH, NO3, Cl, SO4, DOC, NH4+): lysimeters and suction samplers (biweekly to monthly; 1998–2008).
- Note: Some datasets are legacy and not fully stored in a single repository post-2015; some data require direct contact with data custodians for access and additional details.

## 3) Data collection methods, processing and units

- Instrumentation and data capture:
  - AWS met data: continuous minute-level measurements with hourly averages; sensors migrated from 1 m to 4 m height after 2007 due to theft.
  - Micro-met plots: daily measurements of soil and air temperature and soil moisture; parsing and quality checks conducted visually in Excel.
- Processing and centralization:
  - Data were consolidated into various CSV datasets with accompanying documentation; some legacy datasets pre-date formal standardization.
  - Conversion between raw data units to common flux units (e.g., soil respiration and NEE) described (e.g., g CO2 m-2 h-1 or µmol m-2 s-1 to mg CO2-C m-2 h-1 using gas laws).
  - Litter throughfall and rainfall adjustments to align plot-level data with site-level rainfall.
- Data availability and contact points:
  - Primary data are stored with CEH Bangor; some data not yet in a centralized data hub (EIDC). For details, contact Sabine Reinsch or Bridget Emmett.

## 4) Data governance, quality, and challenges

- Data quality considerations:
  - Legacy data may have documentation gaps; some measurements rely on manual QA in Excel rather than automated script-based validation.
  - Throughfall data can be incomplete due to equipment issues (funnel detachments, overflow) and sometimes infilled with averages from other years.
  - Equipment changes over time (e.g., soil respiration instrumentation) require careful cross-calibration using specified conversion factors.
- Gaps and limitations:
  - Not all data are stored in a single centralized repository; accessibility may require contacting data custodians.
  - Some years have limited or infrequent measurements (e.g., NEE and photosynthesis data in certain years).
  - Environmental and operational constraints (e.g., wind limits on curtains) can introduce treatment-related data complexity and potential biases in rainfall exclusion.
- Metadata and documentation:
  - Each dataset is accompanied by a metadata document (RTF) describing sensors, frequency, and time scales.
  - Appendix provides site and plot layout to support spatial interpretation and replication.

## 5) Implications for data strategy and reuse

- For data leaders, the Climoor dataset presents a rich, multi-domain, long-term ecosystem data resource suitable for:
  - Integrating climate treatment effects across abiotic and biotic responses.
  - Cross-dataset analyses requiring biomass adjustments (e.g., NEE adjustments using pin-point biomass data).
  - Validating process-based ecosystem models under drought and warming scenarios.
- Key considerations for governance and reuse:
  - Improve data discoverability by centralizing datasets and providing up-to-date metadata and data dictionaries.
  - Ensure consistent unit definitions and cross-walks for legacy datasets to enable seamless data integration.
  - Establish clear data stewardship roles, versioning, and access permissions, especially for legacy data still housed outside centralized repositories.
  - Consider cross-network collaboration to harmonize methodologies and enable wider community use of climate manipulation datasets.
- Suggested next steps for data leadership:
  - Create or update a comprehensive data dictionary covering all datasets, variables, units, and calibration factors.
  - Develop a data access plan that consolidates storage in a centralized data hub (or clearly documents access paths).
  - Implement data quality checks and automated validation pipelines, leveraging the metadata and conversion rules described in the documentation.
  - Facilitate data sharing with partner networks by aligning with common standards for ecological datasets.

## 6) Appendix references and contacts

- Site layout and quadrat mapping are provided in Appendix 1 and Appendix 2.
- Plot layout and measurement areas are detailed in Appendix 3.
- Primary contacts for data details and access: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor.