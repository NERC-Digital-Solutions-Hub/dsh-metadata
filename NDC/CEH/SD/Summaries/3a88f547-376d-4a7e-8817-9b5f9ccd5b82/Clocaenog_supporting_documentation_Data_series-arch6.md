# Climoor field site in Clocaenog forest Supporting documentation for data

## Overview
- Climate change manipulation experiment at Clocaenog Forest, North East Wales (upland moorland).
- Automated roof technology implements drought and warming treatments to reflect 20–30 year climate projections.
- Established 1998; site comprises replicated drought and warming treatments with control plots.
- Data spanning abiotic and biotic variables across multiple measurement programs, intended to enable data use and self-serve exploration.

## Site and treatments
- Location and ecosystem: upland heath dominated by Calluna vulgaris (heather); diverse associated mosses and vascular plants; humo-ferric podzol soil with variable horizons.
- Experimental design: 9 plots total (3 warming W, 3 drought D, 3 control C) arranged in blocks; each plot sized 4 m × 5 m.
- Climate treatments:
  - Drought: retractable polyethylene roof during growing season (May–Sept; later Apr–Oct), excluding ~80% of rain; reduces annual rainfall by ~20%.
  - Warming: retractable aluminum mesh curtains that reduce night-time heat loss; roof timing auto-based on light; sometimes retracts during rain to preserve rainfall; approximately 14% annual rainfall reduction.
  - Wind constraint: curtains do not operate in winds >10 m/s to prevent damage.
- Treatment schedules and replicate arrangement documented in the included tables.

## Data collection and data types
- AWS meteorological data (on-site automated weather station):
  - Sensors: air temperature, relative humidity, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction.
  - Frequency: hourly averages from 1999–present; minute-level measurements with on-site quality checks.
- Micro-meteorological plot data:
  - Soil and air temperature at multiple depths; soil moisture (varied methods over time).
  - Sampling frequency: daily (log method changed over years; post-2016 half-hourly averages in some datasets).
- Rainfall and rainfall chemistry:
  - Storage rain gauge (site-level rainfall) biweekly; rain chemistry sampling biweekly (pH, NO3, Cl, SO4, DOC, ammonium, etc.).
- Throughfall data (plot-level rainfall):
  - Plot-level rainfall collected biweekly; used to derive percent change relative to site-level rainfall; data occasionally excluded if compromised; infill used in some years.
- Hydrology:
  - Water table depth measured biweekly (2009–present) using permeable tubes; maximum detectable depths per plot recorded.
- Soil respiration:
  - CO2 efflux measured with soil collars; methods evolved (static chambers with IRGA, LICOR LI-8100 system, automated campaigns from 2013–2014).
  - Data converted to mg CO2-C m^-2 h^-1 with specified unit conversions.
- Trace gases (CH4 and N2O):
  - Measured with static chambers; samples collected at 0.25, 15, and 30 minutes; analyzed by gas chromatography; calibration procedures documented.
- Net ecosystem CO2 exchange (NEE):
  - 2002–2004 and 2009–2011; used CIRAS-2 and LI-6400 systems; adjustments for biomass based on above-ground measurements.
  - Data expressed as CO2 flux (mg CO2-C m^-2 h^-1) with unit conversions noted.
- Photosynthesis:
  - Ambient photosynthesis and response curves (PAR and Ci) for Calluna vulgaris, Vaccinium myrtillus, and Empetrum nigrum (2001–2007; select years).
  - Measurements using CIRAS-2 with leaf-level cuvettes; leaf area estimated via dry mass for standardization.
- Vegetation biomass (Pin-Point method):
  - Surveys in 1998–2012; three quadrats per plot; 100 pins per quadrat; touches recorded by species and life form; conversion to biomass using species-specific calibration (Table of pin-hit to biomass).
- Canopy reflectance:
  - Ground-based spectral measurements (NDVI at 680 and 570; PRI) using Ocean Optics spectrometer; data from 2001–2004 with pre-/post-noon sampling.
- Vegetation phenology and growth:
  - Spring phenology, shoot elongation, budburst, leaf counts, and pathogen signs for C. vulgaris, V. myrtillus, and E. nigrum; repeated over multiple years.
- Vegetation chemistry:
  - Carbon, nitrogen, phosphorus, potassium, calcium, magnesium, lignin, tannin, alpha-cellulose, carbohydrates; collected from green and senesced material.
- Litterfall:
  - 12 collectors per plot; monthly collection 1999–2002; later sampling less frequent; litter dried and weighed; carbon and nitrogen analyses on pooled yearly samples.
- Root biomass:
  - Multiple years (2003–2011) with soil cores or cores extracted via sieving and WinRHIZO analysis; depths and extraction protocols documented.
- Soil microbial biomass:
  - Chloroform fumigation method (2000, 2001, 2012) to estimate microbial biomass carbon.
- Nitrogen mineralisation:
  - Soil core incubations (1998–2004) to determine ammonium and nitrate fluxes; paired initial/final cores used to derive net mineralisation rates.
- SOM, SOC and bulk density:
  - Derived from soil cores tied to mineralisation study; moisture, SOM, SOC, and bulk density calculated and expressed per area.
- Soil solution and leachate chemistry:
  - Lysimeters and tensioned samplers; monthly/bimonthly sampling; analysis of pH, NO3, Cl, SO4, DOC, ammonium.

## Data processing and structure
- Data sources and file naming:
  - Numerous data files (e.g., SD_…rtf series) describing data structure, sensors, methods, and time scales.
  - Some legacy data may lack current documentation or have non-standard processing notes.
- Data handling and quality control:
  - On-site quality checks primarily via visual inspection in Excel; acknowledges gaps where automated QC would be preferable.
  - Throughfall data handling includes exclusion of plots with compromised measurements and occasional infilling by averages.
  - Acknowledgment that not all data are stored in a centralized European data center (EIDC); check with data custodians for access.
- Unit conversions and standardization:
  - Explicit conversion factors for translating raw instrument outputs to standardized CO2 flux units (e.g., g CO2 m^-2 h^-1 to mg CO2-C m^-2 h^-1; µmol m^-2 s^-1 to mg CO2-C m^-2 h^-1).
  - Biomass and carbon content conversions for vegetation and soil fractions (e.g., SOM to SOC using 0.55 factor; pin-hit to biomass calibrations in Table 6).
- Data access and contact:
  - Primary data contact persons: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor for details.
  - Data may not all be in the EIDC; some datasets reside with field researchers or CEH Bangor staff.

## Notable considerations and limitations
- Data continuity: long-running program with multiple methodological updates; older data may have inconsistent practices or incomplete metadata.
- Data gaps: some datasets are infrequent or sporadic (e.g., certain years for root biomass, soil microbial biomass, nitrogen mineralisation); throughfall and rainfall datasets may have occasional losses.
- Output usability: throughfall and certain plot-level data require careful treatment to derive plot-specific rainfall and treatment effects; some data are subject to infilling or exclusion due to measurement issues.
- Access limitations: not all data are stored in the centralized repository; direct contact with data custodians is recommended for full access.

## Appendices and layout information
- Appendix 1: Site layout overview.
- Appendix 2: Quadrat layout and plot schematics (2012 Climoor plot layout; lysimeters, pin quadrats, etc.).
- Appendix 3: Plot layout with quadrats and measurement areas marked.

## Key takeaways for data users
- Comprehensive, multi-domain dataset covering abiotic and biotic responses to drought and warming in a upland moorland ecosystem.
- Rich time series across decades with diverse measurement techniques, standardized conversions, and calibration data to support cross-variable analyses.
- Data processing notes and potential limitations should be considered when performing longitudinal or meta-analyses.
- For access and detailed data dictionaries, contact the CEH Bangor data custodians listed above.