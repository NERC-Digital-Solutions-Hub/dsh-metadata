# Climoor field site in Clocaenog forest Supporting documentation for data

- A climate change manipulation field experiment (Climoor) using automated roof technology to simulate drought and warming over upland moorland, reflecting UK climate projections for 20–30 years ahead.
- Location: Clocaenog Forest, North East Wales (53°03'19" N, -3°27'55" W; grid SJ019519). Site features nine plots (4 m x 5 m): three warming (W), three drought (D), and three controls (C), arranged in replicates across three blocks. Appendix 3 provides detailed plot layout.

- Experimental design and treatments
  - Treatments and replicates: warming (W), drought (D), and control (C) with three replicates each; total of 9 plots.
  - Drought treatment: retractable polyethylene roof reduces annual rainfall by ~20% (historically May–Sept; since 2012 Apr–Oct; excludes ~80% of rain during drought periods).
  - Warming treatment: retractable aluminium mesh curtains; minimizes heat loss at night; rain retraction timed to avoid rainfall loss, reducing annual rainfall by ~14%.
  - Curtains blocked in high winds (>10 m/s) to prevent damage.
  - Experimental design linked to block structure to help balance spatial variability.

- Site information and ecology
  - Habitat: upland west-atlantic moorland dominated by Calluna vulgaris (heather); associated species include Vaccinium myrtillus and Empetrum nigrum.
  - Soil: humo-ferric podzol with variable E and Bh horizons (often partially visible; E horizon typically 6–17 cm depth).
  - Vegetation dynamics reported across multiple years; canopy and biomass data collected via pin-point methods, litter traps, and species-specific measurements.

- Data types and datasets (scope, time, and spatial relevance)
  - Meteorological data
    - AWS meteorological data: daily measurements since 1999 (on-site automated weather station, mounted at 4 m after thefts); variables include temperature, humidity, rainfall, wind, solar radiation, net radiation, PAR, pressure.
    - Micro-meteorological plot data: daily measurements (soil temp, soil moisture, etc.) at plot level since 1998.
  - Rainfall and chemistry
    - Rainfall_Clocaenog.csv: site-level rainfall and rain chemistry (biweekly collection; storage rain gauge robust against logger downtime).
    - Throughfall_Clocaenog.csv: plot-level rainfall (biweekly); percent difference calculations applied to derive plot rainfall from site rainfall; data may be excluded or infilled when compromised.
  - Hydrology and soil
    - Water table depth_Clocaenog.csv: biweekly measurements from 2009 onward using permeable tubes (varied maximum detectable depths per plot).
  - Biogeochemistry and physiology
    - Fortnightly soil respiration_Clocaenog.csv and Automated soil respiration_Clocaenog.csv: soil CO2 efflux measurements using collar-based chambers; data converted to mg CO2-C m-2 hr-1 with multiple instrument histories (1999–present, daily-weekly campaigns in 2013–2014 for automation).
    - Trace gases_Clocaenog.csv: CH4 and N2O fluxes from same collars using static chambers; sampling at 0, 15, 30 minutes; analyzed via gas chromatography.
    - Net ecosystem exchange_Clocaenog.csv: NEE measurements in 2002–2004 and 2011; different chamber systems; flux units converted to mg CO2-C m-2 hr-1; adjustments made for biomass.
    - Photosynthesis_Clocaenog.csv: infrequent measurements (2001–2003; 2001 for E. nigrum) using CIRAS-2 and leaf cuvettes.
  - Vegetation and biomass
    - Vegetation survey_Clocaenog.csv: Pin-point biomass estimates across years (1998–2012; quadrats C7, D4, F6); conversion from pin-hits to biomass using species-specific calibration; includes bryophyte pooling and a correction factor for missing pins.
    - Canopy reflectance_Clocaenog.csv: NDVI and PRI derived from ground-based spectrometer (2001–2002, 2003–2004) with background and species spectra for calibration.
    - Phenology Growth Pathogens_Clocaenog.csv: shoot elongation and phenophase data for C. vulgaris, V. myrtillus, E. nigrum (2000, 2002, 2004; annual growth measures through late summer).
    - Vegetation chemistry_Clocaenog.csv: chemical analysis (C, N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates) from green and litter material (1998–present; external lab analyses).
    - Litterfall_Clocaenog.csv: litter collection and drying/weighting; conversion to g m-2; carbon and nitrogen analyses.
  - Soil biology and chemistry
    - Root biomass_Clocaenog.csv and Root biomass.csv: multiple years (2003–2013) using soil cores and varying methodologies (distinct organic vs inorganic layers; WinRHIZO for some analyses).
    - Soil microbial biomass_Clocaenog.csv: chloroform fumigation method (2000, 2001, 2012).
    - Nitrogen mineralisation_Clocaenog.csv: incubation-based NH4+/NO3− analysis (1998–2004).
    - SOM, SOC and bulk density: soil organic matter and carbon density derived from cores; conversions to g m-2.
    - Soil solution and leachate chemistry: lysimeters and tension lysimeters (1998–2008); pH, NO3−, Cl−, SO4 2−, DOC; analyzed via ion chromatography and TOC.
  - Appendix and layout
    - Appendix: Site and plot layout; quadrat layout; plot-specific references to LYS (Lysimeters), PQ (Point quadrats), SS (Soil suction samplers) for 2012 Climoor plot layout.

- Data quality, completeness, and caveats
  - Some data are legacy and not always documented to current best practices; data outside the EIDC storage (post-2015) may exist elsewhere.
  - Throughfall and rain data require calculations against site rainfall; occasionally data are excluded or infilled when measurements are compromised.
  - Equipment changes over time (e.g., AWS sensor height, transition to automated soil respiration) may introduce methodological discontinuities.
  - Spatial data are tied to plot and quadrat layouts; some plots or measurements may have missing pins or damaged samplers; conversion factors and calibration applied for biomass and CO2 fluxes.

- GIS-ready considerations and recommendations
  - Spatial schema
    - Use a plot-level polygon layer for the 9 experimental plots with attributes: plot_id, treatment (W, D, C), block_id, location coordinates, area (m2).
    - Include a quadrat/ collar layer for pin-point biomass, soil respiration collars, and lysimeters with plot_id and collar_id associations.
    - Optional: site-wide raster for elevation, aspect, and vegetation type to contextualize microclimate data.
  - Temporal schema
    - Time-stamped time series per dataset (daily to biweekly to monthly) with standardized date fields; ensure a consistent time zone.
    - Data joins via common keys: plot_id, collar_id, quadrat_id, and species when applicable.
  - Metadata and provenance
    - Document measurement methods, instruments, and unit conversions (e.g., CO2 flux units, biomass calibration factors, NDVI/PRI calculations).
    - Note data gaps, quality flags, and data processing notes (e.g., manual infill, exclusion criteria).
  - Data integration
    - Create a master data model linking climate treatment (W/D/C), plot layout, and all derived variables (e.g., NEE, Rs, Q, biomass, litter, soil chemistry) to support map-based and time-series visualisations.
  - Potential map-based products
    - Time-lapse maps of treatment plots showing drought and warming extents, canopy condition indices (NDVI/PRI), and plot-level rainfall reductions.
    - Interactive dashboards combining plot-level climate manipulation with soil respiration, NEE, and litterfall spatial trends.
    - Bedrock/soil depth and soil property layers (where available) to support 3D or cross-sectional GIS views.
  - Data access and contact
    - Primary data contact: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor for data details and access.

- Contacts for further information
  - Sabine Reinsch (CEH Bangor) and Bridget Emmett (CEH Bangor)
  - For data queries and access to datasets and supporting documentation (RTF files) referenced in the data catalogue.

- Note
  - This document consolidates a broad range of data streams (climate, hydrology, soil, vegetation, and biogeochemical processes) collected over multiple years. While highly rich for GIS-based data products, careful data governance and cross-dataset harmonisation are essential for accurate spatial analyses and map-based visualisations.