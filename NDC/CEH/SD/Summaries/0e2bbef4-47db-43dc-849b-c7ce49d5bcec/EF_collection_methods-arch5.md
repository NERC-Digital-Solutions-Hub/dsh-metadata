# Vegetation work

- The document describes a multi-component ecological data collection protocol covering vegetation structure, gas fluxes, and soil biogeochemistry at field sites.
- Data are intended to support analyses of plant community characteristics, carbon exchange, greenhouse gas fluxes, and soil nutrient dynamics.

## Data collection design and scope
- Vegetation measurements:
  - Four 50 cm x 50 cm quadrats placed randomly per site.
  - Visual estimation of species percent cover; calculation of species richness and combined grasses/forbs cover.
  - Biomass harvested from each quadrat at ground level, dried at 80°C for 24 hours, and summed across quadrats to yield site-level biomass (g).
  - Shannon's diversity index calculated for community diversity.
- Net ecosystem CO2 exchange, photosynthesis, and respiration:
  - Four plastic collars with transparent chambers connected to an infrared gas analyser (IRGA) to measure CO2 influx over two minutes; a reflective cover used to obtain dark efflux.
  - Concurrent measurements of soil moisture (WET sensor), soil temperature, and photosynthetically active radiation (PAR) in triplicate.
  - CO2 flux computed from 27 measurements per two-minute cycle and converted to mg CO2 m^-2 h^-1; two time points (t0 and t120) used to derive hourly flux.
  - Additional calculations involve predicted CO2, time-based adjustments, and standard gas constants for flux estimation.
- Greenhouse gases (CH4, CO2, N2O):
  - Chambers covered with reflective material; gas samples collected at 10, 20, and 30 minutes.
  - Gas concentrations measured by Gas Chromatograph; final flux values derived using the same framework as IRGA-derived CO2 flux.
- Soil sampling and analyses:
  - Six soil samples per site collected to 10 cm depth, sieved to 2 mm, stored at 5°C until processing.
  - Bulk density measured from two cores (0–5 cm and 5–10 cm) after drying for BD calculations.
  - pH measured on fresh soil mixed with water (1:1) using a pH meter.

## Soil physical and chemical properties
- Volumetric moisture content:
  - Fresh soil weighed (approximately 5 g) and dried at 80°C for 48 hours; moisture content calculated from weight difference.
- Water extractable N and C:
  - 5 g soil shaken in 25 ml Milli-Q water for 1 hour; filtrate analyzed for DIN (NH4+, NO3-, total N) and DOC (via autoanalyser and TOC analyser).
  - Extract concentrations adjusted for soil moisture to yield DIN/DOC per kg soil.
- KCl extractable N and potential mineralisation:
  - 5 g soil with 25 ml 1 M KCl; filtration and dilution prior to DIN analysis.
  - An additional 5 g soil incubated at 25°C for 14 days to assess mineralisation (NO3 + NH4) over time; results adjusted for soil moisture and expressed as mineralisation rate (g m^-2 day^-1).
- Microbial biomass:
  - Fumigation-extraction method: fumigate 5 g soil with chloroform to lyse microbes, compare to unfumigated sample.
  - Extraction with 25 ml 0.5 M K2SO4; analysis for DIN, PO4, and dissolved carbon; corrections applied using KE constants (0.35 for C, 0.54 for N) to estimate microbial biomass.

## Data processing and calculations
- Standardized calculations for CO2 flux and gas concentrations are described (e.g., deriving flux from chamber measurements, volume, area, and gas constants).
- Concentration conversions rely on explicit constants (e.g., molar masses, gas constant).
- Moisture corrections and extraction efficiencies are applied to nutrient and carbon measurements to yield comparable soil property metrics.

## Data management and provenance considerations
- Equipment and instrument details are documented (e.g., IRGA model EG M-4, GC model Agilent 7890B, PAR, WET sensor) to support traceability and calibration needs.
- Explicit measurement timelines and replication (e.g., multiple collars, repeated measurements, time stamps) support data lineage and reproducibility.
- Data include both field-derived metrics (vegetation cover, biomass, fluxes) and lab-derived biochemical properties (DIN, DOC, mineralisation, microbial biomass).

## Metadata and governance implications for Data Stewards
- Essential metadata to capture:
  - Site identifiers, plot/quadrat IDs, geographic coordinates, sampling dates/times, and operator names.
  - Instrument models, calibration status, and measurement conditions (chamber volume/area, ambient temperature, moisture, PAR).
  - Detailed method notes and calculation steps, including constants and unit definitions.
- Data curation goals:
  - Maintain consistent units across datasets (e.g., mg CO2 m^-2 h^-1, g biomass, DIN/DOC mg/kg).
  - Document all data transformations and calculation algorithms for reproducibility.
  - Plan for deposition into data portals or catalogues with clear variable definitions and provenance.

## Challenges and considerations for Data Stewards
- Complex, multi-system data with diverse formats (field measurements, lab analyses, gas chromatography outputs) requiring harmonization.
- Timeliness of data submission and updates, as well as handling large volumes of data from multiple replicates and time points.
- Ensuring completeness of user needs (vegetation, gas fluxes, soil chemistry) and alignment with standards for metadata and data sharing.