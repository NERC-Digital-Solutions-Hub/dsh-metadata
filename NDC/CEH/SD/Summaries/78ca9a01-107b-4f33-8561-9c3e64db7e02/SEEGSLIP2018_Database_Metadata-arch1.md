# Soil metrics and vegetation data from pasture fed livestock farms across Great Britain, 2018

## Overview
- Data collection by UK Centre for Ecology & Hydrology (UKCEH) in a project funded by BBSRC to evidence the impacts of pasture-fed livestock approaches on grassland parameters, particularly sward composition and soil qualities.
- Context: UK grasslands are important for farming, biodiversity, water filtration, nutrient cycling, and carbon storage. The Pasture Fed Livestock Association (PFLA) provides certification standards linked to environmental and animal health outcomes.
- Dataset comprises vegetation species and characteristics, soil quality metrics, and farm management aspects from farms belonging to the PFLA (and related intentions to certify).

## Experimental design and sampling
- 56 farms across Great Britain, all members of or linked to PFLA; recruitment via PFLA.
- Fieldwork conducted May–September 2018; plots sampled on farms that were either fully certified, provisionally certified, or members aiming for certification.
- Sampling unit: a large 200 m² plot per field, randomly positioned (validated on-site where possible).
- In each field, a single 200 m² plot was sampled for vegetation and soil; a large plot-level survey was paired with field management data.
- Vegetation data collected alongside field management practices, using methods aligned with the Countryside Survey (CS).

## Data collected and measurements
- Vegetation
  - All species recorded within the plot; percent cover for nested subplots; vegetation height categories (0–15 cm, 15–50 cm, 15–40 cm, 40 cm–1 m, >1 m).
  - Data captured electronically.
- Field management
  - On-site questionnaire with current and historic field practices: sward longevity, grazing management, inputs, and other management variables.
- Soils
  - One soil core per plot (depth 15 cm, diameter 7 cm) with a range of soil properties analyzed.
  - Key measurements:
    - Loss-on-ignition (LOI) to estimate soil organic matter and derive soil carbon concentration (C) using a standard LOI-based formula.
    - Total organic carbon (SOC) and total nitrogen (N) via elemental analysis after removing inorganic carbon.
    - Total phosphorus (P) and Olsen phosphorus (Olsen-P) for arable and improved grassland.
    - Soil pH (in deionised water and CaCl2), electrical conductivity (EC), and bulk density.
    - Particle size distribution (PSD) via laser diffraction and hydrometer methods; caution about organic matter interference in LD measurements.
    - Aggregate stability via a wet sieving method.
    - Calcium carbonate (CaCO3) content via thermogravimetric analysis.
  - Quality control
    - LOI quality checks with internal standards; repeated batches if outliers exceeded 2 standard deviations.
    - Duplicate samples and matrix blanks used in phosphorus analyses; calibrations with standards for all colorimetric/fluorometric steps.
- Data alignment with CS methods to ensure comparability, including use of equivalent soil and vegetation metrics.

## Data structure and access
- Four CSV data sheets, anonymised to protect landowner confidentiality:
  - SEEGSLIP_PLOTS_2018.csv: Plot-level vegetation data and basic plot attributes (site code, plot type, plot number, survey dates, habitat descriptors, plant structure, soil sampling status, OS 5 km reference, and more).
  - SEEGSLIP_SPECIES_2018.csv: Species-level vegetation data per plot (REP_ID), with species name, coded numbers, cover details, nest levels, and nested plot information.
  - SEEGSLIP_SOIL_2018.csv: Soil data per plot (site, REP_ID) including moisture, conductivity, total carbon, LOI, total nitrogen, pH in water and CaCl2, Olsen-P, total P, bulk density, PSD fractions (clay/silt/sand), aggregate stability, CaCO3, etc.
  - SEEGSLIP_FIELD_MGT.csv: Field management data per plot (PFLA membership, years as a PFLA member/certified producer, pasture type, age of pasture, grazing practices, duration and type of grazing, cattle/sheep presence, numbers, cutting/fertilising practices, lime use, herbicide, etc.).
- Anonymisation
  - Farms anonymised; assigned site IDs/code for privacy; OS reference data available at grid scale (5 km) for locational context.
- Coding conventions
  - NI = no information; N/A = not applicable (common codes like 998 or 999 used in management fields).

## Data quality and validation
- Methods for soils and vegetation aligned with long-running Countryside Survey protocols to enable cross-year comparability.
- LOI-to-C conversion standardized; quality controls applied using internal standards and batch-level checks.
- Laser diffraction PSD cross-validated with sieve-based sand fraction measurements; organic matter content can influence LD results, especially at high LOI values.
- Data quality emphasis on consistent sampling, on-site validation of plot locations, and QA across chemical and physical soil measurements.

## Scope, limitations, and context for analysts
- Cross-sectional snapshot from 2018; results reflect pasture-fed systems within the PFLA network at that time.
- Farms are anonymised; some metadata (e.g., exact location) limited to preserve confidentiality.
- Comparability with Countryside Survey methods enhances potential for temporal or cross-dataset analyses, including soil carbon stock estimation and vegetation–soil interactions.
- The dataset supports analyses of:
  - Relationships between sward composition and soil properties across different pasture types and certification statuses.
  - Impacts of farm management practices (grazing duration, stocking density, fertilisation, liming, and cutting) on soil quality and carbon indicators.
  - Variation across Broad Habitat classifications (Acid, Calcareous, Neutral, Improved grasslands) and PFLA certification.

## Potential analytical questions and uses
- How do vegetation composition and sward structure relate to soil carbon, nitrogen, and phosphorus pools?
- Do certified PFLA producers show distinct soil quality or nutrient profiles compared with non-certified or prospective producers?
- How do soil physical properties (bulk density, PSD, aggregate stability) correlate with land management practices and grazing regimes?
- How do LOI-derived carbon estimates align with SOC measurements across different plots and habitat types?
- How do management practices (fertilisation, liming, grazing intensity, cutting frequency) influence soil health indicators and biodiversity (via vegetation data) on pasture-fed farms?