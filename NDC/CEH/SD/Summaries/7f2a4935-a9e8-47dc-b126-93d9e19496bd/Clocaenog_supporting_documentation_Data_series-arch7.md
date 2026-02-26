# Climoor field site in Clocaenog forest Supporting documentation for data

## Overview
- Climoor is a climate change manipulation experiment at Clocaenog Forest, North East Wales, using automated roof technology to simulate drought and warming conditions over the next 20–30 years.
- Operated on solar and wind power; established in 1998 with replicated drought and warming treatments plus controls.
- Data cover a wide range of abiotic and biotic measurements, described in detail for data users and GIS practitioners.

## Location and Site Context
- Location: Clocaenog Forest, upland west-atlantic moorland in Wales (grid reference SJ019519; Lat/Lon 53.055°N, 3.465°W; 53°03'19"N, -03°27'55"W).
- Dominant vegetation: Calluna vulgaris (heather) >60% of plant biomass; other species include Vaccinium myrtillus and Empetrum nigrum.
- Soil: humo-ferric podzol with variable eluvial (E) and illuvial (Bh) horizons; typical E horizon 6–17 cm deep.
- Experimental plots: 9 plots in total (3 warming, 3 drought, 3 controls) arranged in blocks to mirror shading and other structural effects.

## Experimental Design (Climate Change Treatments)
- Treatments and replication: drought (D) and warming (W) each with 3 replicate plots; 3 control plots to mirror shading from the experimental structure (total n=9).
- Drought treatment: May–Sept (1999–2011), April–October since 2012; uses retractable polyethylene roof to exclude rainfall, reducing annual rainfall by ~20% (and ~80% of rainfall during the growing season for some periods).
- Warming treatment: retractable aluminum curtains that reflect infrared radiation at night, reducing heat loss; rainfall can be excluded briefly due to a sensor-driven retraction, averaging ~14% annual rainfall reduction; curtains avoid operation in winds >10 m/s.
- Spatial layout: blocks and plot numbering described in tables; ensures comparability across treatments and controls.

## Equipment, Protocols and Data Processing
- On-site Automated Weather Station (AWS) and plot-level sensors for multi-parameter monitoring; extensive data collection across years (1998–current datasets referenced).
- Data modalities include:
  - AWS meteorological data: daily, minute-level sampling with hourly averages; temperature, relative humidity, rainfall, air pressure, net radiation, solar radiation, PAR, wind.
  - Micro-meteorological (plot-level) data: daily soil and air temperatures, soil moisture (multiple methods over time; TDR and earlier probes).
  - Rainfall and rainfall chemistry: site-level storage rain gauge (biweekly) and biweekly chemical analyses of rainfall (pH, NO3, Cl, SO4, DOC, ammonium).
  - Throughfall (plot-level rainfall): biweekly collection; used with site rainfall to compute plot-level rainfall changes per treatment.
  - Water table depth: from 2009 onward via permeable tubes; biweekly measurements.
  - Soil respiration: fortnightly with collars; transitions across measurement systems (CIRAS-2, LI-COR 8100, automated 2013–2014); unit conversions provided.
  - Trace gases (CH4 and N2O): measured with closed chambers; sampling at 0.25, 15, and 30 minutes; gas chromatography analysis; legacy data notes.
  - Net ecosystem CO2 exchange (NEE): measured in select years (2002–2004, 2011) with different chamber systems; biomass-adjusted using above-ground measurements.
  - Photosynthesis: infrequent measurements (2001–2003) using CIRAS-2 and leaf cuvettes; light-response and ambient-light data.
  - Vegetation biomass (pin-point method): annual surveys (1998–2012, and beyond) with three quadrats per plot; 100 pins per quadrat; pin hits converted to biomass using species-specific calibration.
  - Canopy reflectance: ground-based spectral measurements (NDVI at two bands, PRI) in 2000–2004.
  - Vegetation phenology, growth and pathogens: annual shoot elongation and phenophase assessments for C. vulgaris, V. myrtillus, E. nigrum; multi-year data.
  - Vegetation chemistry: elemental analysis (C, N, P, K, Ca, Mg, lignin, tannin, cellulose, carbohydrates) for green and litter material.
  - Litterfall: collectors monthly (1999–2002); later less frequent; carbon and nitrogen analyses.
  - Root biomass: multiple methods over years (soil cores, sectioning, washing, WinRHIZO analysis).
  - Soil microbial biomass: chloroform fumigation technique (2000, 2001, 2012).
  - Nitrogen mineralisation: incubation cores (1998–2004) with NH4+/NO3 analysis.
  - SOM, SOC and bulk density: derived from soil cores; lab-based measurements and calculations to express in g m-2.
  - Soil solution and leachate chemistry: lysimeters and suction samplers; pH, nitrate, chloride, sulfate, DOC, ammonium analyses.
- Data handling notes:
  - Some datasets are legacy with variable documentation quality; not all data stored in the EIDC; contact CEH Bangor for details.
  - Data quality in some sections relies on manual quality checks or described methods; fill-ins and data loss are addressed with transparent exclusions and adjustments.

## Spatial and Data-Product Implications for GIS Specialists
- Spatial context: plot-level arrangement, treatment assignments, and plot layout described in appendices; useful for building GIS layers of treatments, canopy indices, biomass distributions, and soil properties.
- Temporal scope: long-running, multi-decadal data with yearly to sub-daily resolution across diverse variables; enables time-series GIS analyses and space-for-time substitution studies.
- Data types suitable for GIS product development:
  - Treatment maps: drought, warming, and control plot boundaries and blocks.
  - Plot-level climatic and soil layers: AWS-derived climate variables, soil moisture, soil temperature, water table depth.
  - Vegetation layers: biomass estimates by species, litterfall production, canopy reflectance indices (NDVI, PRI).
  - Biogeochemical layers: SOM/SOC densities, soil nutrient concentrations, N mineralisation rates, litter chemistry, root biomass distributions.
  - Hydrological layers: rainfall throughfall adjustments, lysimeter-derived leachate chemistry, water-table depth contours.
- Access considerations: some datasets are not stored in centralized repositories; for full data access and provenance, contact Sabine Reinsch and Bridget Emmett at CEH Bangor.

## Appendices and Site Layout
- Appendix 1–2: Detailed site layout and quadrat configuration; plot references, quadrat IDs, and measurement areas.
- Plot layout and grid reference: Grid SJ019519; latitude/longitude 53.055N, -3.465W; precise plot and quadrat placements documented for GIS georeferencing.

## Contacts and Data Access
- Primary contacts for further details and data access: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor.

## Endnotes
- The Climoor dataset collection represents a comprehensive, long-term, multi-disciplinary field data resource with substantial potential for GIS-driven analyses of climate treatment effects on upland moorland ecosystems. Users should anticipate legacy-data caveats and coordinate with data stewards for access and lineage information.