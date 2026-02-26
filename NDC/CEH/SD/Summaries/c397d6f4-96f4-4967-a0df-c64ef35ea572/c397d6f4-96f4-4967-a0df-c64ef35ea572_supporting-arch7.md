# Soil respiration under Miscanthus x giganteus and an adjacent barley crop.

## Overview
- A data descriptor presenting two datasets on soil respiration (Rs) and accompanying environmental variables from a UK field trial comparing Miscanthus x giganteus and adjacent spring barley.
- Measurements used automated chambers and IRGAs, with data processing conducted in SAS 9.3. Data are available via the NERC Environmental Information Data Centre.

## Study site and experimental design
- Location: farm in eastern United Kingdom; fields planted with Miscanthus x giganteus (7-year-old stand) and April-sown spring barley.
- Experimental setup: one IRGA and one multiplexer per crop; six chambers placed at random within separate plots (independent replicates), 1.5 m apart.
- Sampling period: May to August 2013.
- Chamber and collar details: PVC collars (diameter 20 cm, height 10 cm) inserted ~2 cm into soil to minimize root disturbance; collars remained in place throughout the study.
- Measurements alongside Rs: soil temperature and soil moisture at 5 cm depth measured every 15 minutes; hourly meteorological data (solar radiation, air temperature) collected onsite.

## Data collection and processing
- Rs measurement method: CO2 concentration regressed against time to compute flux; corrections for chamber volume and temperature applied via manufacturer’s software.
- Data analysis: all analyses conducted in SAS 9.3.
- Replicates treated as independent due to random chamber placement within plots.

## Datasets

- Dataset 1. Flux_and_soil_data
  - Date fields: DATE (dd/mm/yyyy); DTHOUR (datetime rounded to nearest hour); DTQUART (nearest 15 minutes); TIME (hh:mm:ss).
  - Crop identifier: CROP (ARAB = barley, MISC = Miscanthus x giganteus).
  - Rs measurements: Rs_Umol (µmol m⁻² s⁻¹); Rs_mg (mg m⁻² h⁻¹); Rs_r2 (r² of Rs regression).
  - Chamber and environment: CHAMBERTEMP (°C); CHANNEL (chamber number); Rs_cv (coefficient of variation); AREA (cm²); ST_C (soil temperature at 5 cm, °C); SM_M3M3 (volumetric soil moisture, m³ m⁻³).
  - Additional data: TIME-related fields and descriptive units.

- Dataset 2. Met_data
  - Datetime (dd/mm/yyyy hh:mm:ss).
  - Meteorological/environmental variables: AIRTEMP_C (air temperature, °C); RAD_WMSQ (solar radiation, W m⁻²).

## Data formatting and metadata
- File formats and field descriptions are provided to enable integration with GIS and time-series workflows.
- Dataset references include precise units and data types for each field, supporting consistent ingestion into analysis or mapping tools.

## Access, citations, and references
- Data citation: Keane, B.; Ineson, P. (2017). Soil respiration under Miscanthus x giganteus and an adjacent barley crop. NERC Environmental Information Data Centre. DOI: https://doi.org/10.5285/c397d6f4-96f4-4967-a0df-c64ef35ea572
- Related methodological references:
  - Drewer et al. (2012). How do soil emissions of N2O, CH4 and CO2 from perennial bioenergy crops differ from arable annual crops? Global Change Biology Bioenergy, 4, 408-419.
  - Heinemeyer et al. (2011). Soil respiration: implications of the plant-soil continuum and respiration chamber collar-insertion depth on measurement and modelling of soil CO2 efflux rates in three ecosystems. European Journal of Soil Science, 62, 82-94.

## GIS considerations and potential uses
- Potential uses: time-resolved Rs data mapped across crop types to compare soil CO2 efflux under Miscanthus vs. barley; integration with soil temperature and moisture layers; correlation with hourly meteorological data for spatial-temporal analyses.
- Coordinate information is not provided in the dataset description; users may need site geolocation (and any available parcel boundaries) to create spatial maps.
- Data can serve as a basis for map-based data products comparing crop effects on soil respiration and linking respiration fluxes with environmental drivers.

## Limitations and notes for reuse
- Spatial scope: single farm site with two crop treatments; limited number of replicates (six chambers per field).
- Temporal scope: May–August 2013; results are site-specific and may not generalize beyond similar UK agroecosystems.
- Measurement depth: soil temperature and moisture measured at 5 cm depth; deeper soil processes not captured.
- Data processing specifics: Rs fluxes calculated using chamber-based regressions and corrected per manufacturer’s software; analyses performed in SAS 9.3.