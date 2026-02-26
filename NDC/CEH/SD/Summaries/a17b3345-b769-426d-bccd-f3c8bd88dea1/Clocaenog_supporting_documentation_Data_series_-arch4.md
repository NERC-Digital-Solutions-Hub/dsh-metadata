# Climoor field site in Clocaenog forest Supporting documentation for data

## Overview
- Climoor is a climate change manipulation experiment at Clocaenog Forest, North Wales, using automated roof technology to simulate drought and warming for upland moorland over the next 20–30 years.
- Established in 1998; comprises replicated drought and warming treatments with three replicates plus three control plots (total 9 plots configured in blocks) to mirror shading from the experimental structures.
- Site characteristics: upland heath with Calluna vulgaris-dominated vegetation; soil is humo-ferric podzol; growing season June–August; winter dormancy; extensive plant and soil measurements across abiotic and biotic parameters.

## Data scope and datasets
- AWS meteorological data: daily measurements (temperature, humidity, rainfall, radiation, PAR, wind, pressure) from an on-site automated weather station.
- Micro-meteorological plot data: daily soil and air temperature, soil moisture at multiple depths.
- Rainfall data: site-level storage rain gauge (biweekly) and rainfall chemistry (pH, nitrate, chloride, sulfate, DOC, ammonium).
- Throughfall data: plot-level rainfall collected biweekly; used to estimate treatment rainfall changes relative to site rainfall.
- Water table depth data: biweekly measurements from permeable tubes to bedrock (post-2009).
- Soil respiratory and gas data: fortnightly to high-resolution soil respiration; trace gases CH4 and N2O via static chambers; automated and manual methods across years.
- Net ecosystem CO2 exchange (NEE): sparse historical measurements (2002–2004, 2011) using different chamber systems; includes respiration adjustments using biomass data.
- Photosynthesis: ambient and response-curve measurements (2001–2003; species include Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum).
- Vegetation biomass and structure: Pin-point vegetation surveys (1998–2012) across plots; biomass conversions for multiple species; canopy structure and leaf area proxies.
- Canopy reflectance: NDVI and PRI indices from ground-based spectrometry (2001–2004).
- Phenology, growth and pathogens: shoot elongation, budburst and phenophase data for key species; annual maximum growth measurements.
- Vegetation chemistry: C, N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates on green and litter material.
- Litterfall: monthly to yearly litter outputs (1999–2002; later less frequent); biomass and carbon/nitrogen analyses.
- Root biomass: soil cores across years (2003–2013), with varying extraction methods.
- Soil microbial biomass: chloroform fumigation methodology (2000, 2001, 2012) with DOC measurements.
- Nitrogen mineralisation and SOM/SOC/bulk density: annual to periodic measurements; KCl extractables for NH4+/NO3-; SOM and SOC by loss-on-ignition and fractionation; bulk density calculations.
- Soil solution and leachate chemistry: lysimeters and tensioned samplers; pH, NO3-, Cl-, SO4^2-, DOC, NH4+ analyses; biweekly sampling.

## Data collection, processing, and metadata
- Instruments and methods:
  - AWS met data: hourly-averaged, minute-level sensor data (temperature, humidity, rainfall, radiation, PAR, wind, pressure); sensors moved from 1 m to 4 m height after 2007 due to theft.
  - Micro-meteorological data: daily measurements from plot-level sensors; depth-specific soil temperature and moisture via T107 and TDR probes.
  - Rainfall and chemistry: biweekly site-level rainfall; laboratory analyses for major ions and carbon content; sample preservation details (4 C, filtered).
  - Throughfall: plot-level rainfall collected and processed to derive treatment-specific rainfall changes; some data gaps excluded from treatment means.
- Data processing notes:
  - Various years used different equipment (CIRAS-2, LICOR 8100, LI-COR chambers) with unit conversions provided (CO2 flux to mg C m^-2 h^-1).
  - Soil respiration: alternative collars and analyzers over time; careful calibration and conversion factors applied; 120 s measurement windows; some modernization in 2013–2014 with automated systems.
  - Trace gases: static chambers with gas sampling and storage for later GC analysis; legacy data with less tightly documented processing steps.
  - NEE and photosynthesis: biomass adjustments using plot-specific above-ground biomass to standardize flux measurements.
- Data quality and limitations:
  - QA primarily via basic manual checks (Excel); acknowledgment that legacy data may not meet current best-practice data processing standards.
  - Throughfall and rainfall matching can exclude plots or apply infill to maintain treatment means; occasional data loss due to equipment issues; some years have NA in certain metrics.
  - Some long-term datasets not stored in EIDC; consult CEH Bangor contacts for access to smaller or post-2015 data.

## Data governance, access, and stewardship
- Primary data repository note: not all data are stored within the EIDC; some legacy/infrequently collected datasets reside elsewhere.
- Contact points for data access and details: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor.
- Data processing and documentation: supporting documentation files accompany each dataset (RTF files referenced); dataset names are listed alongside each description.
- Site layout and appendix: detailed site and quadrat layout provided in Appendices (Appendix 1–3) for plot/quadrat placements and measurement areas.

## Notable challenges and considerations for data leaders
- Understanding user needs and data gaps: scattered data types across multiple years and methods; some data require reconstruction or cross-referencing with original field notes.
- Data standards and metadata: varying methods and units across years; need harmonization for cross-study analyses; some metadata inconsistently documented due to legacy practices.
- Access barriers: some data outside centralized stores; need to coordinate with CEH Bangor for complete datasets and provenance.
- Coordination and community: a broad, multi-dataset ecosystem requiring careful governance to maintain discoverability and reusability across the data system.

## Appendices and site layout
- Appendix 1: Site layout and plot configuration (Lysimeters, Pin-point quadrats, Soil suction samplers).
- Appendix 2: Quadrat layout and measurement areas.
- Appendix 3: Plot layout with quadrats and measurement areas (Climoor plot layout context).