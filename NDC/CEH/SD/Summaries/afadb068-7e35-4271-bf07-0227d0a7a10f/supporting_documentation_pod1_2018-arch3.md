# Ozone flux dataset using POD IAM for semi-natural vegetation (grasslands) in the UK and USA, 2018

## Overview
- Provides daily POD IAM-based ozone flux (phytotoxic ozone dose) for grasslands during the 2018 growing season, focusing on UK and USA.
- Used to assess potential impacts of ozone pollution on semi-natural vegetation and to inform risk assessment and policy.

## Data sources and model chain
- Collection/generation: Based on the EMEP-WRF global model, version 4.45, built on the EMEP MSC-W framework.
- Meteorology: World Weather Research and Forecast (WRF) model (v4.2.2) driven by ECMWF IFS data; WRF initialized and nudged every six hours with GFS-FNL.
- Emissions: IIASA ECLIPSE v6a GAINS for 2015.
- Ozone uptake modeling: DO3SE model embedded in EMEP to compute POD values; outputs PODyIAM (POD IAM) and POD3 IAM, with emphasis on POD1 IAM for grasslands in this dataset.
- Grid and units: Global 1° x 1° grid; ozone flux values in mmol m^-2; geographic coordinates in WGS 1984.

## Parameterisation and calculations
- DO3SE parameterisation used to calculate POD1 IAM for sunlit leaves at the top of semi-natural vegetation canopies.
- Time window and seasonality: Typically a 90-day daylight period within April–September; the start/end dates are chosen to maximize flux or reflect local seasonality.
- Grassland-specific settings: Parameter values for POD IAM include parameters such as maximum stomatal conductance and related vegetation-specific inputs (Table 1 in the source).
- Data aggregation: For the current dataset, daily POD1 IAM values were summed for the 90-day grassland growing season (mid-April to mid-July) in 2018 for the UK and USA.

## Spatial and temporal data structure
- Spatial resolution: Gridded data at 1° x 1°.
- Attributes (5 columns): FID (grid cell identifier), Lon (centre longitude), Lat (centre latitude), NAME (country: USA or UK), POD1 (accumulated POD1 IAM for the grassland growing season, 2018, in mmol m^-2).

## Quality assurance and validation
- Model validation: Described in Mills et al. (2018); comparison of model output with Global Atmosphere Watch (GAW) observations demonstrates the model’s ability to capture spatial and temporal ozone variability, including high-ozone episodes.
- Stomatal uptake validation: Relationship between AET/PET and model-estimated POD3 IAM (divided by 7h mean ozone, as a proxy for growing-season stomatal conductance) showed a strong correlation (r^2 = 0.63), indicating credible estimation of stomatal ozone uptake.

## Use for monitoring and policy
- Potential applications: 
  - Tie POD IAM flux values to crop and vegetation impact functions to estimate yield loss, biomass reduction, and flower number changes (per CLRTAP Modelling and Mapping Manual).
  - Support risk assessment with grassland-specific ozone critical levels and thresholds.
  - Inform monitoring frameworks and governance by providing open, model-derived VOC (vegetation ozone dose) metrics for policy discussions.

## Limitations and challenges
- Data-related barriers: Incomplete metadata, varying data formats requiring transformation, and challenges around data accessibility and timely sharing.
- Data governance: Public sharing of underlying datasets can be a barrier; requires clear data management, provenance, and openness standards.
- Generalisability: Model-based estimates depend on input data quality (emissions, meteorology) and parameterisation; species- or region-specific variations may affect applicability.

## Background and references
- CLRTAP Mapping Manual (2017) for POD-based impact assessments.
- Emberson et al. (2000); CLRTAP methods for stomatal ozone flux.
- Hayes et al. (2021); ozone flux and grassland responses.
- Mills et al. (2018); model validation and relation to wheat production.
- Simpson et al. (2012); EMEP MSC-W model description.
- Vieno et al. (2016); emissions sensitivity related to UK PM2.5.
- Useful background: emep.int; icpvegetation.ceh.ac.uk