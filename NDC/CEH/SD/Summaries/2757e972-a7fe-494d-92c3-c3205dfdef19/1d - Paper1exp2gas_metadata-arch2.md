# Soil Core Gas Flux Measurements with Biochar Treatment

- Overview
  - A dataset capturing soil gas flux measurements from soil cores, with and without biochar amendments, across multiple timepoints.
  - Designed to monitor environmental conditions and greenhouse gas emissions over time, supporting environmental health assessments and policy evaluation.

- Data structure and scope
  - Each record documents a soil core (identified by soilcoreno) and its associated measurements at a given timepoint.
  - Includes both cumulative gas flux measurements and initial gas concentrations, along with comprehensive soil, chamber, and treatment metadata.
  - Time-related fields capture progression from the start of measurements (dayfromstart, hourfromstart) and precise timing (datetimefirst).

- Key variables (categories)
  - Core and treatment metadata
    - soilcoreno, biochartreatment, dayfromstart, hourfromstart, datetimefirst
    - drysoilweightg, biocharweight, biocharfraction, bulkdensitygcm3
  - Gas flux (cumulative)
    - ugCO2-Cfluxg-1cumu, ngCH4-Cfluxg-1cumu, ngN2O-Nfluxg-1cumu, ugCO-Cfluxg-1cumu
  - Gas concentrations at t0
    - CO2ppmt0, CH4ppmt0, N2Oppmt0, COppmt0
  - Environmental and chamber context
    - tempair, gravwatercontentproportion, chambaream2, headvolm3
    - wfpsproportion, maximumwhc, proportionofwhc

- Measurements and units
  - Cumulative gas fluxes
    - CO2: ug CO2-C flux g-1 dry soil
    - CH4: ng CH4-C flux g-1 dry soil
    - N2O: ng N2O-N flux g-1 dry soil
    - CO: ug CO-C flux g-1 dry soil
  - Concentrations in static chamber headspace at t0
    - CO2, CH4, N2O, CO in ppm
  - Soil and chamber properties
    - soil weight (g), surface area (m2), headspace volume (m3), bulk density (g/cm3)
  - Soil moisture and water capacity
    - gravimetric water content proportion, f(water-filled porosity), maximum water holding capacity, proportion of WHC

- How this supports environmental monitoring aims
  - Enables consistent, standardized tracking of soil gas emissions over time to assess environmental health and policy outcomes.
  - Facilitates comparisons between biochar-amended and unamended treatments under varying soil and moisture conditions.
  - Provides data suitable for visualization (maps, charts) and reporting to stakeholders.

- Data quality, provenance, and stewardship
  - Structured with explicit descriptions for each field, supporting verification and quality assurance.
  - Designed to be stored and uploaded to institutional portals, enabling data sharing and long-term accessibility.
  - Clear links between timepoints, treatments, and measured outputs support reproducibility and auditability.

- Practical use for analysts
  - Time-series analysis of gas fluxes by treatment and soil properties.
  - Assessment of how biochar amendments influence greenhouse gas emissions under different soil moisture conditions.
  - Integration with other environmental datasets to enhance the value and reuse of monitoring data.