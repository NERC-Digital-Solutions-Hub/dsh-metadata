# Soil Gas Flux Measurement Dataset: Field Descriptions and Parameters

## Overview
- A dataset of soil gas flux measurements across individual soil cores with associated treatments.
- Includes timepoints, soil treatments (biochar addition and periodic wetting), environmental conditions, and multiple gas flux metrics.
- Gas measurements cover CO2, CH4, and N2O using static chamber methods, with both raw flux values and log-transformed equivalents.
- Accompanied by soil physical properties, chamber characteristics, and sampling metadata to support robust analysis and data governance.

## Key Variables and Data Structure
- Core and time identifiers
  - soilcoreno: Individual soil core number
  - timepoint: Timepoint of measurements
  - dayfromstart: Days since start of gas analysis
  - daysfromwettingevent: Days since last wetting event
  - datetime: Date/time of the soil gas flux analysis (and a separate datetime field for measurement time)
- Treatments
  - temperaturetreatment: Soil temperature condition during sampling
  - biochartreatment: Whether biochar was amended
  - wettingtreatment: Whether the sample was periodically wetted to high water content
  - fulltreatname: Full name of the soil treatment (biochar and wetted)
- Gas flux measurements and transformations
  - mgCO2-Cfluxm2h1: CO2 flux (mg C per m2 per hour)
  - log10co2: Log10(flux + 1) for CO2, with handling for prior negative values
  - ugCH4-Cfluxm2h1: CH4 flux (µg C per m2 per hour)
  - log10ch4: Log10(flux + 1) for CH4, with handling for prior negative values
  - ugN2O-Nfluxm2h1: N2O flux (µg N per m2 per hour)
  - log10n2o: Log10(flux + 1) for N2O, with handling for prior negative values
- Static chamber initial measurements
  - CO2ppmt0: CO2 concentration in ppm in the chamber headspace at t0
  - CH4ppmt0: CH4 concentration in ppm in the headspace at t0
  - N2Oppmt0: N2O concentration in ppm in the headspace at t0
- Environmental and chamber context
  - tempair: Air temperature at the time of gas measurement
  - gravwatercontentproportion: Gravimetric soil water content as a proportion
  - chambaream2: Soil area within the static chamber (m2)
  - headvolm3: Volume of the static chamber headspace (m3)
  - datetime: Date/time of the soil gas flux measurement
- Soil mass and composition
  - drysoilweightg: Dry soil weight in grams
  - biocharweightg: Dry biochar weight added to soil (g)
  - biocharfraction: Biochar as a proportion of dry soil weight
  - particledensitygcm3: Particle density of the soil (g/cm3)
  - totalporosity: Total porosity (calculated as 1 - (bulk density / particle density))
  - wfpsproportion: Water-filled pore space (gravimetric water content × (bulk density / total porosity))

## Treatments and Experimental Design
- Treatments capture key manipulations:
  - Biochar addition (biochartreatment) and explicit full treatment name (fulltreatname)
  - Periodic wetting regimen (wettingtreatment)
  - Temperature conditions (temperaturetreatment)
- The design supports assessing how soil amendments and moisture regimes influence gas flux dynamics over time, controlling for chamber and soil properties.

## Measurement and Transformation Details
- Gas flux values are recorded in standardized units (CO2: mg CO2-C flux m-2 h-1; CH4: µg CH4-C flux m-2 h-1; N2O: µg N2O-N flux m-2 h-1).
- Raw flux values are complemented by log-transformed equivalents (log10 of flux + 1) to handle skewness and stabilize variance, with specific handling when previous flux values were negative (use the magnitude of the negative value in the transformation).
- Initial gas concentrations in the chamber headspace (t0) are recorded in ppm for each gas.
- A comprehensive set of soil and chamber properties (e.g., gravimetric water content, porosity, chamber area, headspace volume) supports normalization and interpretation of flux measurements.

## Metadata, Data Quality, and Sharing Considerations
- The dataset provides explicit metadata for each field, facilitating data reuse and governance.
- For monitoring framework authors, important considerations include:
  - Ensuring metadata completeness and clarity to enable data verification and replication.
  - Handling transform rules (especially log transformations with negative flux cases) transparently in analyses and reports.
  - Balancing openness with data-sharing constraints when publishing underlying data.
  - Maintaining data quality throughout collection, storage, transformation, and dissemination, including updates to metadata as needed.

## Relevance for Monitoring Frameworks
- This dataset exemplifies a structured approach to environmental health monitoring, combining treatment manipulation, temporal measurements, and comprehensive metadata.
- It supports evaluating policy-relevant questions about soil amendments and moisture management on greenhouse gas emissions.
- The clear documentation of measurements, units, transformations, and derived variables aligns with best practices for transparency, comparability, and governance in monitoring frameworks.

## Challenges and Considerations for Practitioners
- Potential data gaps or inconsistent metadata can hinder cross-study comparability; the field descriptions aim to mitigate this, but vigilance is needed during integration.
- Siloed data and access constraints may affect timely analysis; the dataset’s explicit structure and transformation rules can help with data harmonization and sharing if governance processes are in place.
- Complex transformations (e.g., log10 with flux-based handling of negatives) require careful documentation in any onward analyses and dashboards.