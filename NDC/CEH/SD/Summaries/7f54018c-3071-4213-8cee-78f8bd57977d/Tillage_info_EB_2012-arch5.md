# Nitrous oxide fluxes from an intensively managed grazed grassland in Scotland

## Overview
- Study location: Easter Bush, Scotland (55° 51' 55.30"N, 3° 12' 22.17"W).
- Timeframe: Measurements before and after tillage on 1 May 2012.
- Experimental setup: Two 5.4 ha fields with intensive livestock production; tilled field compared with an adjacent non-tilled field managed for grazing.
- Objectives: Quantify N2O fluxes using eddy covariance and chamber methods to assess effects of tillage and management.

## Data Collected
- Eddy covariance data (flux-scale and micrometeorology)
  - Gas species: N2O, CO2, H2O; mixing ratios measured at 10 Hz.
  - Instrumentation: Ultrasonic anemometer (WindMaster Pro, 2.4 m height); quantum cascade laser (QCL) gas analyser; 13.5 m sample line; approx. 13 L/min flow.
  - Primary outputs (half-hourly): co2_flux, h2o_flux, n2o_flux; wind_speed; wind_dir; u*, L, TKE, (z-d)/L, bowen_ratio; tau; H; LE.
  - Processing/derivation: Fluxes calculated via covariance (χ′w′); 30-min intervals; corrections and quality controls described below.
- Chamber measurements (soil N2O fluxes)
  - Static chambers: PVC cylinders, 38 cm ID, 22 cm height; measurements over 40 minutes; gas samples every 0, 20, 40 minutes; analysis by GC with ECD.
  - Dynamic chambers: QCL-based closed system; 30 m sampling radius; 6–7 L/min flow; fluxes computed from 1 Hz data over 3 minutes using linear and non-linear regression approaches; detection limit ~0.04 nmol m⁻² s⁻¹.
  - Footprint: Ten static chambers per field within the eddy covariance footprint (10–200 m from mast); occasional repositioning to minimize microclimate bias.
- Field management event data
  - Tillage event: 1 May 2012 (South tilled field); plough to 30 cm; harrow, roll, and ryegrass seeding within days after tillage.
  - Fertilisation: Nitram (NH4NO3) applications and timing differ between tilled and un-tilled fields; roading of grazing and continuous sheep grazing documented.
  - Documentation format: Table 1 listing events and dates; detailed event timeline provided.
  
## Methods and Processing
- Eddy covariance processing
  - Software: EddyPro (Version 5.2.1).
  - Data treatment: Double coordinate rotation (vertical and crosswind); spike removal; block averaging; time lag removal by covariance maximisation.
  - Corrections: System frequency response (high/low-frequency losses) per Moncrieff et al. (1997); density fluctuations corrected (Burba et al., 2012).
  - Quality control: Foken et al. (2005) QC scheme; data with wind directions 180–270° labeled as tilled; >330° to <100° labeled as untiled; remaining data discarded due to obstruction.
- Chamber processing
  - Static chamber Flux Calculation: F = (dC/dt) × (ρV)/A; dC/dt from linear regression; chamber volume estimated from height measurements.
  - Dynamic chamber Flux Calculation: 1 Hz data over 3 minutes; linear and non-linear asymptotic regression methods; best-fit method selected per measurement.
  - Detection limits: Static chambers ~0.4 nmol m⁻² s⁻¹; dynamic chambers ~0.04 nmol m⁻² s⁻¹.
- Data integration and provenance
  - Two complementary approaches (eddy covariance and chambers) to cross-validate N2O fluxes.
  - Field events provide contextual metadata for interpreting flux responses to tillage and fertilisation.

## Datasets and Metadata
- File: Easter_Bush_EddyC_Tillage_2012
  - Contains: Tau, corrected momentum flux; H, LE (sensible/latent heat); co2_flux, h2o_flux, n2o_flux; wind_speed and wind_dir; u*, TKE, L, (z-d)/L; bowen_ratio; other related EC diagnostics.
- File: Easter_Bush_Chambers_Tillage_2012
  - Contains: Field name, method, chamber method; dates/times; flux values (nmol N2O m⁻² s⁻¹); ancillary measurements (air temperature, soil temperature, pressure, PAR, rainfall, etc.).
- Field management context
  - Table 1: Detailed field management events and timing (tillage, harrowing, sowing, fertilisation, grazing) for both tilled and un-tilled fields.
- References and methods
  - Documentation of processing approaches and supporting literature (e.g., Moncrieff et al. 1997; Burba et al. 2012; Foken et al. 2005; Levy et al. 2011; Pedersen et al. 2010; Skiba et al. 2013).

## Quality Control and Uncertainty
- Eddy covariance
  - Quality control excludes low-quality data (Foken category 2) and data obstructed by equipment geometry (cabin/fence line).
  - Corrections applied to account for instrument limitations and atmospheric conditions.
- Chamber methods
  - Static chamber detection limit higher than dynamic chamber method; dynamic method provides more sensitive flux measurements.
  - Calibration and regression-based flux estimation with cross-method comparison recommended for robust interpretation.

## Data Availability and Reuse
- Datasets encompass raw sensor outputs and processed flux estimates, with explicit documentation of methods, corrections, and QC steps.
- Metadata and event timeline enable contextual reuse for studies of tillage impacts, grazing systems, and soil-atmosphere N2O exchange in temperate maritime climates.
- Clear file naming and structured metadata support reproducibility and cross-study aggregation.

## Practical Guidance for Data Stewards
- Ensure metadata coverage includes:
  - Sensor models, installation heights, and sampling lines; calibration procedures; clock synchronization details; and data processing software versions.
  - Exact flux calculation formulas and QC criteria used (e.g., equation forms, thresholds for spike removal, density corrections, and frequency-response corrections).
  - Field management events with precise dates/times and treatment details to enable interpretation of flux responses.
- Data formats and interoperability:
  - Maintain consistent units across datasets (e.g., N2O flux in nmol m⁻² s⁻¹; CO2 and H2O fluxes similarly defined).
  - Preserve both raw (10 Hz) and processed (30-min) flux data to support reprocessing or alternative processing pipelines.
  - Include footprint and obstruction notes to contextualize data selection criteria (e.g., wind-direction-based data separation).
- Reproducibility and provenance:
  - Archive processing scripts (EddyPro configurations, regression methods for chamber fluxes) alongside datasets.
  - Document decisions about data inclusion/exclusion (e.g., which data were discarded due to obstruction or QC category).
- Data governance considerations:
  - If applicable, attach data usage licenses and cite related publications and software.