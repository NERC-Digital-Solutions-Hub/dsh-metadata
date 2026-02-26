# Soil respiration under Miscanthus x giganteus and an adjacent barley crop

## Purpose and scope
- Data describing soil respiration (Rs) under a Miscanthus x giganteus stand and an adjacent spring barley crop.
- Collected in a farm in eastern United Kingdom, May–August 2013.
- Aimed to compare Rs between a perennial bioenergy crop and an arable crop and enable data exploration and analysis by others.

## Experimental design
- Two crops: Miscanthus (MISC) and barley (ARAB).
- Chambers: 6 per field, placed randomly within separate plots, at least 1.5 m apart; collars inserted ~2 cm into soil.
- Measurement cycle: chambers closed for 2 minutes per measurement with a 30-second dead band; cycle alternates among chambers.
- Independent replicates: chambers treated as independent within each crop field.
- Environmental context: soil temperature and moisture measured at 5 cm depth; hourly solar radiation and air temperature recorded onsite.
- Equipment: automated chambers and infrared gas analysers (IRGA, Licor LI-8100-101A) with multiplexers; one IRGA and one multiplexer per crop.
- Study period: May–August 2013.
- Study design references: full site description in Drewer et al. (2012); measurement considerations discussed in Heinemeyer et al. (2011).

## Data collection and structure
- Data collection method: Rs fluxes calculated as linear regressions of CO2 concentration against time; corrections for volume and temperature applied via manufacturer software; subsequent analyses conducted in SAS 9.3.
- Dataset 1: Flux_and_soil_data
  - Key fields: DATE, DTHOUR, DTQUART, TIME; CROP (ARAB or MISC); Rs_Umol (µmol m^-2 s^-1); Rs_mg (mg m^-2 h^-1); Rs_r2; CHAMBERTEMP; CHANNEL; Rs_cv; AREA; ST_C (soil temp 5 cm); SM_M3M3 (volumetric soil moisture 5 cm depth).
- Dataset 2: Met_data
  - Key fields: Datetime; AIRTEMP_C (air temperature); RAD_WMSQ (solar radiation).

## Variables and data description
- Temporal resolution: hourly and sub-hourly time stamps (DTQUART, TIME).
- Rs metrics: Rs_Umol and Rs_mg with fit quality (Rs_r2) and variability (Rs_cv).
- Microclimate: CHAMBERTEMP, ST_C, SM_M3M3; meteorological context: AIRTEMP_C, RAD_WMSQ.
- Spatial context: CROP, CHANNEL (chamber identifier), AREA.

## Data quality and processing notes
- Rs values derived from CO2 concentration vs time regression; adjustments for chamber volume and temperature applied per instrument manual.
- Data processing and statistical analyses performed in SAS 9.3.
- Data are organized to enable self-service exploration of Rs by crop, time, and environmental conditions.

## Access, citation, and references
- Data citation: Keane, B.; Ineson, P. (2017). Soil respiration under Miscanthus x giganteus and an adjacent barley crop. NERC Environmental Information Data Centre. DOI: 10.5285/c397d6f4-96f4-4967-a0df-c64ef35ea572
- References:
  - Drewer, J. et al. 2012. How do soil emissions of N2O, CH4 and CO2 from perennial bioenergy crops differ from arable annual crops? Global Change Biology Bioenergy, 4, 408-419.
  - Heinemeyer, A. et al. 2011. Soil respiration: implications of the plant-soil continuum and respiration chamber collar-insertion depth on measurement and modelling of soil CO2 efflux rates in three ecosystems. European Journal of Soil Science, 62, 82-94.