# Soil metrics and vegetation data from pasture fed livestock farms across Great Britain, 2018

## Aim and scope
- Evidence the impacts of pasture-fed livestock approaches on grassland parameters, focusing on sward composition and associated soil qualities.
- Context: grassland is significant in the UK for farmers and public interests; Pasture Fed Livestock Association (PFLA) provides certification standards related to environmental and animal health concerns.
- Data cover vegetation, soil metrics, and aspects of farm management from pasture fields on PFLA member farms.

## Who collected and dataset context
- Collected by the UK Centre for Ecology & Hydrology (UKCEH) for a project funded by BBSRC.
- Sampling on farms belonging to the PFLA; farms recruited via PFLA contacts.
- 56 farms across Great Britain visited between May and September 2018; inclusion includes fully certified, provisionally certified, and members-in-waiting.
- Methods align with the Countryside Survey (CS) to enable comparison with long-term GB vegetation and soil data.

## Experimental design and sampling
- Each farm contributed data from a single field where vegetation and soils were sampled.
- Plot design: a large 200 m² plot per field, randomly positioned and pre-visited/validated on-site.
- Within each plot, vegetation and soil sampling followed CS-inspired protocols, enabling cross-site comparability.
- Data collected across GB with anonymised farm identifiers (site codes) to protect landowner confidentiality.

## Vegetation sampling
- Recorded all species present within the plot and percentage covers for nested sub-plots.
- Vegetation height categorized into discrete classes (0–15 cm, 15–50 cm, 15–40 cm, 40 cm–1 m, >1 m) and measured with an electronic device.
- On-site collection included a questionnaire on current and historic field management practices related to sward longevity, grazing management, and inputs.

## Soils and laboratory analyses
- Soil sampling: one soil core per plot (depth 15 cm, diameter 7 cm).
- Measured soil properties (CS-aligned methods with some CS-excluded measures):
  - Bulk Density (BD), Carbon (SOC derived from Loss-on-Ignition), Total Nitrogen (TOT_N)
  - Loss-on-Ignition (LOI) and conversion to soil carbon concentration
  - Total Phosphorus (TOT_P) and Olsen Phosphorus (OLSON_P) for arable/grassland samples
  - Soil pH in water and CaCl2 solution
  - Conductivity (EC) of soil solution
  - Particle Size Distribution (PSD) via laser diffraction and hydrometer methods; calibration and duplicate checks
  - Aggregate stability using wet sieving methodology
  - Calcium carbonate (CaCO3) content via thermogravimetric analysis
  - Additional measures include moisture content, and total soil macro-fauna counts for CS comparison
- Quality control: LOI standardization with internal references; two internal standards per batch; duplicate samples and blanks; UKAS-aligned laboratory practices; cross-validation with CS soil methods.

## Field management and context data
- Data captured on management practices for each field, including:
  - PFLA membership duration and years as a certified producer
  - Pasture type (Permanent, Temporary, Hay meadow)
  - History and use of field prior to pasture
  - Grazing patterns: average grazing duration, winter grazing, grazing type, number of grazings per year
  - Stocking: presence of cows and/or sheep, total cattle and sheep numbers, cuts taken, fertilization (mineral and organic), lime application, herbicide use, and other management notes
  - Fertilizer timing, organic fertilizer type and amount, and lime amount
- The field-management dataset (FIELD_MGT) provides rich context for interpreting vegetation and soil metrics.

## Data structure and files
- Four CSV data sheets containing anonymised data:
  - SEEGSLIP_PLOTS_2018.csv: basic plot attributes and vegetation data per plot
  - SEEGSLIP_SPECIES_2018.csv: species-level vegetation data within plots (species codes, cover, nesting, etc.)
  - SEEGSLIP_SOIL_2018.csv: soil measurements per plot (various chemical, physical, and moisture properties)
  - SEEGSLIP_FIELD_MGT.csv: field management context (grazing, fertilization, pasture type, history)
- Farms are anonymised with site codes/IDs to preserve landowner confidentiality.
- Data fields include Os5km references, survey dates, habitat classifications, slope/shade descriptors, soil date of sampling, and farm-level management descriptors.

## Data quality, standardisation, and comparability
- Methods mirror those used in the Countryside Survey to enable integration with long-term GB vegetation and soil data.
- LOI-derived carbon concentrations are calculated with a fixed formula and validated with internal standards.
- Soil analyses conducted under UKAS-accredited protocols; multiple quality controls (duplicates, blanks, reference materials) applied.
- Cross-comparability with CS data supports temporal and spatial trend analyses in grassland soils and vegetation.

## Outputs and potential uses
- A comprehensive 2018 GB dataset linking pasture-fed livestock management to grassland vegetation structure and soil quality.
- Enables assessment of how PFLA-certified practices influence sward composition, soil organic matter, nutrient status (P, N), soil physical properties, and overall ecosystem condition.
- Useful for environmental monitoring, policy performance evaluation, and longitudinal studies when integrated with other GB datasets (e.g., Countryside Survey).

## Access and limitations
- Data are anonymised at the farm level; identifiers are site codes.
- Snapshot from 2018; cross-referencing with Countryside Survey data enhances interpretability for trend analyses.