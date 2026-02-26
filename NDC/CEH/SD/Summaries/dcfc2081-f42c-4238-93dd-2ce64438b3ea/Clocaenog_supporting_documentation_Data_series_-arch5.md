# Climoor field site in Clocaenog forest Supporting documentation for data

## Scope and purpose
- Documentation of climate manipulation experiments at Climoor, Clocaenog Forest, UK.
- Describes site information, climate treatments (drought and warming), equipment, data collection, processing methodologies, and data inventories.
- Serves as a governance and metadata resource to support discovery, reuse, and appropriate data management.

## Experimental design and climate treatments
- Automated roof-based drought and warming treatments to simulate climate change for upland moorland over the next 20–30 years.
- Site established in 1998; replicated plots with three warming, three drought, and three control plots per block across nine plots per block (total of 9 plots, with scaffolding controls to mirror shading).
- Drought treatment: annual May–Sept (1999–2011 originally; April–October since 2012) reduction of ~20% rainfall; implemented via retractable polyethylene roof triggered by tipping-bucket rainfall sensor.
- Warming treatment: nighttime warming via retractable aluminium mesh curtains; infrared-reflective roof reduces heat loss; some rainfall exclusion during warming events due to roof retraction delay.
- Treatments governed by weather cues and wind-speed limits (curtains not operated in winds >10 m/s).
- Climate data include long-term trends (e.g., annual rainfall, growing-season rainfall reductions, and warming degree-day indicators) across multiple years.

## Data categories and datasets (overview)
- AWS meteorological data: daily measurements from on-site automated weather station (1999–present).
- Micro-meteorological (plot-level) data: daily plot-scale soil and air temperatures, soil moisture (1998–present).
- Rainfall data: storage rain gauge (site-level, biweekly) and rainfall chemistry (biweekly sampling; pH, NO3, Cl, SO4, DOC, ammonium analyses).
- Throughfall data: plot-level rainfall collected biweekly; used to compute treatment-specific rainfall reductions.
- Hydrology: water table depth data (from 2009 onward) via permeable tubes.
- Biogeochemistry and biology: soil respiration (fortnightly to high-resolution campaigns), trace gases (CH4 and N2O), net ecosystem CO2 exchange (NEE; intermittent years), photosynthesis, vegetation biomass (Pin-point method), canopy reflectance (NDVI and PRI), vegetation phenology and pathogens, vegetation chemistry (C, N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates), litterfall, root biomass, soil microbial biomass, nitrogen mineralisation, SOM/SOC/bulk density, soil solution and leachate chemistry.
- Data processing notes: conversions between measurement systems (e.g., g CO2 m-2 h-1, µmol m-2 s-1, mg CO2-C m-2 h-1), biomass calibration from pin hits, and vegetation biomass adjustments for NEE.

## Data collection methods and formats
- Equipment and sensors: on-site AWS (air temp, RH, rainfall, pressure, net radiation, solar radiation, PAR, wind) plus plot-based soil and air temperature, soil moisture, rainfall collectors, lysimeters, and CO2/trace gas chambers.
- Sampling frequency: typically daily (AWS and micro-meteo), biweekly to monthly for chemical and hydrological samples, fortnightly for soil respiration and trace gases, occasional measurements for NEE, photosynthesis, and litterfall.
- Data formats and storage: multiple datasets with named CSV files (e.g., Daily automated weather station data_1999to2015_Clocaenog.csv, Rainfall_Clocaenog.csv, Throughfall_Clocaenog.csv, Net ecosystem exchange_Clocaenog.csv, etc.). Some data are not stored in the centralized EIDC, particularly infrequent or post-2015 data; contact CEH Bangor for details.
- Documentation: supporting RTF datasheets accompanying CSVs; legacy data may not conform to current best-practice documentation standards.

## Data processing, quality control, and methodology notes
- Data processing varies by dataset and era; for example:
  - Soil respiration and associated Rs calculations via different instruments over time (CIRAS-2, LICOR LI-8100, automated LI-COR with chamber systems).
  - Unit conversions and standardizations to mg CO2-C m-2 h-1 or µmol m-2 s-1 with explicit conversion factors.
  - Pin-point vegetation surveys translated into biomass using species-specific calibration factors; controls for missing pins and cross-year consistency.
  - Litterfall and vegetation chemistry analyses following standard UK labs procedures; some data were collected at varying frequencies across years.
  - NEE calculations adjusted for biomass differences within chamber bases using above-ground biomass estimates.
- Quality control: data quality checks described as primarily visual/manual (e.g., in Excel) and some legacy practices; dataset notes acknowledge inconsistencies and potential gaps due to historical data handling.
- Data limitations and caveats: some datasets labeled as legacy with incomplete or non-standardized documentation; not all data are housed in a central repository; throughfall and rainfall datasets may require careful reconciliation to compute treatment-specific rainfall reductions.

## Data governance, storage, and access considerations
- Data ownership and stewardship: data produced from a multi-year climate manipulation experiment; governance relies on CEH Bangor contacts for data access and interpretation.
- Storage and accessibility: central note that not all data (especially infrequently collected and post-2015 data) are stored in the EIDC; some datasets require direct contact with data custodians.
- Documentation and metadata: extensive documentation exists for datasets (supporting rtf files and appendices), but some data processing steps are not fully documented as current best practice.
- Key contacts: Sabine Reinsch and Bridget Emmett (CEH Bangor) are primary points of contact for data details and access.

## Particular considerations for data stewards
- Ensure long-term preservation and discoverability of diverse datasets spanning meteorology, hydrology, ecosystem fluxes, vegetation, soil processes, and chemistry.
- Maintain and update metadata to capture dataset provenance, measurement methods, instruments, unit conventions, and any conversion factors applied during processing.
- Harmonize legacy datasets with current data standards where possible and document any deviations or undocumented steps.
- Proactively address data gaps and gaps in the central repository by coordinating with data custodians and clarifying storage locations (EIDC vs. other archives).
- Provide guidance on data sharing limitations due to wind conditions, equipment changes, and treatment-specific data adjustments (e.g., throughfall-based rainfall corrections).

## Appendix and site layout references
- Appendix 1: Site and plot layout; Appendix 2: Quadrat layout and measurement areas.
- Appendix 3: Plot layout with quadrats and measurement areas (including lysimeters, pin quadrats, soil collars).