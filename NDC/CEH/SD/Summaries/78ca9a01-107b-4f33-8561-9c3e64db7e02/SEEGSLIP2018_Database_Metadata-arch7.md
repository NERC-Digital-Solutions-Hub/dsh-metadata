# Soil metrics and vegetation data from pasture fed livestock farms across Great Britain, 2018

## Overview
- Dataset from UK Centre of Ecology & Hydrology, funded by BBSRC.
- Aimed to evidence effects of pasture-fed livestock on grassland parameters, especially sward composition and soil qualities.
- Covers pasture grasslands across Great Britain, including four broad habitat types: Acid, Calcareous, Neutral, and Improved grasslands.
- Focuses on farms belonging to the Pasture Fed Livestock Association (PFLA); data include vegetation, soil metrics, and field management per field sampled.
- 56 farms recruited in 2018; sampling May–September 2018.
- Anonymised farm identifiers; includes Ordnance Survey 5km grid references for locational context.

## Experimental design and sampling
- Farms recruited through PFLA; balance of certification statuses (25 fully certified, 7 provisionally certified, others members with near-term certification).
- Each farm visited; data collected from a single field per farm where vegetation and soils were sampled.
- Sampling method aligned with Countryside Survey (CS) protocols to enable cross-study comparisons.
- In each field, a large 200 m² plot was randomly positioned and surveyed for vegetation and soil characteristics.
- Location validation performed on-site; pre-visit maps used when available.

## Data collection and measurements

- Vegetation
  - All species present within the 200 m² plot; species presence and cover recorded.
  - Vegetation height categories assigned (0–15 cm, 15–50 cm, 15–40 cm, 40 cm–1 m, >1 m).
  - Data collected electronically; additional field management data obtained from farmer via questionnaire.

- Soils
  - One soil core per plot (15 cm depth, 7 cm diameter) analysed for multiple properties following CS protocols (with some CS measures excluded).
  - Key soil metrics include:
    - Loss-on-Ignition (LOI) as a proxy for soil organic matter and carbon concentration.
    - Total soil organic carbon (SOC) and nitrogen (via elemental analysis after inorganic carbon removal).
    - Total and Olsen phosphorus (P) with standard QA controls.
    - pH in deionised water and in CaCl2.
    - Electrical conductivity (EC) of soil solution.
    - Bulk density of fine earth; particle size distribution (PSD) via laser diffraction and hydrometer method.
    - Aggregate stability via wet sieving and NaOH treatment.
    - Calcium carbonate (CaCO₃) content via thermogravimetric analysis.
  - Quality controls include internal standards, duplicate checks, and batch-level controls to ensure data reliability.

- Field management
  - On-site interview data with farmers covering current and historic management practices:
    - Sward longevity, grazing management, inputs, pasture type, and certification status.
    - Detailed pasture-management variables (e.g., grazing duration, rotations, stocking, fertiliser use, lime, herbicide usage, organic fertilisers, timing, and amount).

## Data structure and content

- Four CSV data sheets (anonymised data with farm/site IDs):
  - SEEGSLIP_PLOTS_2018.csv: Basic plot attributes and vegetation plot data (site code, plot type, plot number, survey dates, habitat descriptions, canopy/shrub/ground heights, soil sampling, OS reference).
  - SEEGSLIP_SPECIES_2018.csv: Species-level vegetation data (plot ID, species name and code, nested plot coverage, total cover, nesting counts).
  - SEEGSLIP_SOIL_2018.csv: Soil measurements by plot (dry content, conductivity, total C and LOI, total N, pH in water and CaCl₂, Olsen P, total P, bulk density, clay/silt/sand fractions, aggregate stability, CaCO₃ content).
  - SEEGSLIP_FIELD_MGT.csv: Field management data (PFLA membership and certification years, pasture type, age of pasture, grazing practices, stocking details, cutting/fertility practices, lime and herbicide usage, organic fertiliser details, timing and amounts).
- All farms anonymised; each farm assigned a site code; OS 5 km grid reference included for locational context.

## Data quality and comparability
- Methods closely follow established CS protocols to enable benchmarking against national data.
- Thorough on-site validation of plot locations; use of pre-visit maps when available.
- Implemented QA/QC measures across soil analyses, including internal standards, duplicates (1 in 10), and batch-level checks.
- Data are cross-compatible with Countryside Survey data, facilitating integrative analyses of soil and vegetation across time.

## GIS considerations and potential applications
- Spatially explicit dataset suitable for GIS-based analysis of:
  - Spatial patterns of vegetation composition and height classes across pasture fields.
  - Relationships between soil properties (C, N, P, pH, EC, PSD, bulk density) and vegetation structure.
  - Management practices (grazing regimes, fertilisation, lime use) and their spatially distributed impacts on soil and sward characteristics.
- Os 5 km references and plot-level data enable linkage with broader land cover and habitat layers, and potential integration with policy or public-facing map products.
- Data enable cross-seasonal and cross-study comparisons with CS datasets, supporting assessments of pasture-fed livestock impacts on grassland soil health and biodiversity.

## Limitations and accessibility
- Study limited to 56 farms sampled in 2018; field data reflect one field per farm, which may not capture within-farm heterogeneity.
- Anonymised data protect landowner confidentiality; precise farm identities are not publicly disclosed.
- Some CS measures were excluded or differ slightly from CS protocols; datasets are designed for comparability where possible, but users should review methods for any nuances.