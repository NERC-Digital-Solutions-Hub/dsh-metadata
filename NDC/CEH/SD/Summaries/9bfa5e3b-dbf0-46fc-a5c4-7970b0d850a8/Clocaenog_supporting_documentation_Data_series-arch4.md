# Climoor field site in Clocaenog forest Supporting documentation for data

- A climate change manipulation experiment (Climoor) using automated roof technology to simulate drought and warming over upland moorland in Clocaenog Forest, North Wales.
- Established in 1998; powered by solar and wind.
- Experimental design comprises replicated drought and warming treatments plus controls:
  - 3 warming plots, 3 drought plots, 3 control plots (total 9 plots).
  - Treatments organized in blocks; drought aims to reduce growing-season rainfall, warming uses night-time infrared reflectance curtains. Curtains retract in rain to limit rainfall effects; operation disabled in high winds (>10 m/s).
- Data scope spans multiple abiotic and biotic measurements collected from 1997/1998 onward, across numerous data streams and methodologies.

## Data streams and data collection highlights

- AWS meteorological data (on-site automated weather station)
  - Sensors: air temperature, relative humidity, rainfall, air pressure, net/radiation, solar radiation, PAR, wind speed/direction.
  - Frequency: daily data; time series from 1999 to present (with earlier data as context).
  - Structure: minute-level measurements aggregated to hourly/daily; quality control via visual checks.
- Micro-meteorological plot data
  - Soil temperature at 5, 10, 20 cm; soil moisture via TDR and earlier methods.
  - Frequency: daily (hourly averages after 2016).
- Rainfall data and rainfall chemistry
  - Storage rain gauge for site-level rainfall (biweekly collection; robust to logger power issues).
  - Warren spring collectors for chemical analyses (pH, NO3, Cl, SO4, DOC, NH4).
- Throughfall data
  - Plot-level rainfall collected biweekly; used to compute treatment-specific rainfall changes (percent reductions) relative to site-level rainfall.
  - Data gaps and quality control lead to occasional exclusion or infilling with year-averaged reductions.
- Water table depth
  - Measured with permeable tubes to bedrock; biweekly measurements since 2009.
  - Maximum detectable depths recorded per plot.
- Soil respiration
  - Fortnightly measurements since 1999 across three soil collars per plot.
  - Methods evolved: CIRAS-2 (2001–2008), LI-COR 8100 (2008–2013), automated 2013–2014 with updated collars.
  - Output: CO2 flux in mg CO2-C m-2 h-1; conversions provided to harmonize units.
- Trace gases (CH4 and N2O)
  - Measured with the same collars using static chambers; sampling at 0.25, 15, and 30 minutes.
  - Lab analysis via gas chromatography; calibration checks described.
- Net ecosystem CO2 exchange (NEE)
  - Years: 2002–2004 and 2011 (two different chamber systems used).
  - Conversion to mg CO2-C m-2 h-1; adjustments for biomass variation inside chambers.
- Photosynthesis
  - Ambient measurements and response curves (PAR and Ci) for key species; years include 2001–2003 and 2005–2007 with varying PAR/Ci settings.
  - Leaf-level measurements with species-specific mass/area calibrations.
- Vegetation survey (pin-point biomass)
  - Annual surveys (1998–2012, with gaps thereafter noted) using pin-grid method in fixed quadrats; conversion from pin hits to biomass via species-specific calibration factors.
  - Destructive calibration in 2000 to relate pin hits to biomass.
- Canopy reflectance
  - Ground-based spectral reflectance (400–950 nm) for NDVI and PRI indices; measurements around solar noon in 2001–2004.
- Vegetation phenology, annual growth, and pathogens
  - Longitudinal measurements of shoot elongation, budburst, leaf counts, and pathogen indicators (e.g., rust).
  - Species tracked: Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum.
- Vegetation chemistry
  - Analyses on green and senesced material; nutrients and carbon fractions (C, N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates).
- Litterfall
  - Litter traps; monthly collection 1999–2002, then irregular collection thereafter.
  - Litter dried, weighed, and converted to g m-2; subsequent chemical analyses performed on pooled yearly samples.
- Root biomass
  - Root cores collected in multiple years (2003–2011 range); methods include manual extraction and WinRHIZO analyses; multiple core diameters and depths used.
- Soil microbial biomass
  - Chloroform fumigation technique (2000, 2001, 2012); DOC difference between fumigated and unfumigated samples; express as mg microbial biomass C per g soil organic matter.
- Nitrogen mineralisation
  - Incubation cores (1998–2004); NH4+ and NO3- analyzed to determine net mineralisation rates.
- SOM, SOC and bulk density
  - Derived from paired cores (N-mineralisation study cores); SOM/SOC content and bulk density calculated and scaled to g m-2.
- Soil solution and leachate chemistry
  - Lysimeters and tensioned soil water samplers (biweekly); analysis of pH, NO3-, Cl-, SO4-, DOC, NH4+.

## Data management, storage, and access

- Data infrastructure
  - Data collected across a wide range of formats and management systems; some datasets are stored in the EIDC, but not all (notably infrequently collected or post-2015 data).
  - Contact points for data availability and details: Sabine Reinsch and Bridget Emmett at CEH Bangor.
- Data processing and units
  - Explicit unit conversions and data processing details provided for key datasets (e.g., converting raw CO2 flux measures to mg CO2-C m-2 h-1; multiple instrument harmonizations for Rs and NEE).
  - Calibration steps described for specific datasets (e.g., pin-hit to biomass conversions; LICOR/CIRAS data reconciliations).
- Data quality and legacy notes
  - Quality checks primarily performed via visual inspection in Excel; automated QA/QC scripts not uniformly applied.
  - Document notes acknowledge legacy data practices; some methodological descriptions and processing steps reflect evolution over time.
- Data gaps and treatment of missing data
  - Throughfall and some plot-level data may be excluded when measurements are compromised; in some years data infilled using year-average reductions.
  - Drought and warming treatment data show variations over time (dates, durations, and wind-related operational limits).

## Key considerations for Data Leaders

- Longitudinal integrity
  - The dataset spans multiple decades with changing measurement technologies and protocols; rigorous metadata and provenance are essential to enable cross-year analyses.
- Data harmonization
  - Harmonize units and calibrations across instruments (e.g., Rs, NEE, CO2 flux conversions) to facilitate integration across data streams.
- Documentation and discoverability
  - Ensure clear metadata for each dataset (methodology, sensors, time scale, spatial scope, quality flags) and maintain up-to-date archival locations.
- Access and governance
  - Centralize data access points and specify contact persons for datasets; clearly denote which datasets are stored in EIDC vs. external archives.
- Data quality management
  - Move beyond ad hoc visual QC toward automated QA/QC where feasible; document data gaps, infilling methods, and any assumptions used in processing.
- Data reuse and collaboration
  - The project’s scale and cross-disciplinary data (climate, ecology, soil science) make this a rich resource for collaborators; maintain consistent licensing and usage guidelines.

## Appendices and layout references

- Appendix 1–3 include site layout, quadrat arrangement, and plot infrastructure (e.g., lysimeters, pin quadrats).
- The document collectively serves as a comprehensive overview of site characteristics, treatment regimes, and the extensive suite of data collected over time.