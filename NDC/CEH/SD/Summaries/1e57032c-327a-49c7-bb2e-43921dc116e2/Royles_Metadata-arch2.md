# Physiology and stable isotope ecology of moss growth for modelling spatial and temporal climatic signals NERCDMP-555 - monthly field and dark adapted PAM fluorescence measurements

## Overview
- A field- and lab-based study to model spatial and temporal climatic signals using moss physiology and stable isotope ecology.
- Monthly field sampling (April 2017 – September 2018) across multiple sites with diverse moss lifeforms and habitats.
- Standardised measurements to produce time-series data suitable for environmental monitoring and palaeoclimate analogue work.

## Study sites and sampling
- Dersingham Bog, Brandon Country Park, Wicken Fen and surrounding areas (specific coordinates and habitat types listed).
- Target species include a range of mosses (e.g., Sphagnum spp., Dicranum scoparium, Pleurozium schreberi, Calliergonella cuspidate, Kindbergia praelonga, etc.).
- Fieldwork involved identifying representative species, collecting voucher specimens, and harvesting three samples per target species per visit.
- Permissions obtained from land owners/managers; samples stored on collection bags for transport.

## Field measurements and data collected
- Chlorophyll fluorescence measurements using Walz MINI-PAM II:
  - In-field: three measurements per sample (F, Fm, PAR, ETR).
  - Dark adaptation: at least 30 minutes, followed by three additional measurements in the dark (F', Fm').
  - Calculations: fluorescence yield (dark and light), non-photochemical quenching, and electron transport rate (ETR = 0.84 × PAR × 0.5 × Φ).
  - Outputs averaged across the three in-field measurements with associated standard errors.
- Water content measurements:
  - Fresh moss sample (~0.3 g) weighed; dry to constant mass at 70°C to derive field relative water content (RWC = (Fresh − Dry) / Dry).
- Additional field sampling:
  - Fresh water collected at each site; precipitation collected near the center of the field area.
  - A subset of moss samples subjected to enzymatic sucrose content analysis.

## Laboratory analyses and isotopes
- Water and moss distillates analyzed for isotopes:
  - δD (D/H) and δ18O (18O/16O) analyzed at Lancaster Environment Centre (duplicates run; standards traceable to VSMOW/GISP).
  - δD precision ~ ±1‰; δ18O precision ~ ±0.5‰.
  - Oxygen isotopes additionally analyzed by EA-IRMS at Cambridge; precision better than 0.4‰; calibrated to V-SMOW using IAEA standards.
  - Carbon isotopes (δ13C) analyzed at Cambridge; precision better than 0.1‰; calibrated with IAEA standards.
- Method references and standard procedures used for cellulose extraction, water extraction times, and metabolite analyses.

## Datasets and data structure
- Four CSV datasets produced:
  - Royles_Field_data_by_time: structured fields for time, location, species, sampling session, measurement types (RWC, C13, O18), etc.
  - Royles_RWC_and_Isotope_data: weights, dry/wet masses, isotope ratios (d13C, d18O, dD) and related calculations.
  - Royles_Sample_Number_Key: mapping of sample numbers to reference numbers, collection details, location, species, herbarium info.
  - Royles_Water_Samples: date, location, water type/source, d18O and dD values with metadata.
- Data fields include sample reference numbers, dates, locations, collection sites, species, descriptions, and measurement results.

## Data quality, QA, and standards
- Duplicates performed for isotope analyses; glass wool filtration and standardized filtration/setup.
- Field and lab procedures aligned with established protocols (e.g., cellulose extraction, cryogenic distillation, and stable isotope analyses).
- Analytical standards included VSMOW, IAEA references, and in-house TAP standards; inter-lab calibration ensured comparability.

## Data management and accessibility
- Emphasis on storing and uploading created datasets to appropriate portals.
- Clear documentation of dataset structure to enable reuse, interoperability, and potential integration with other environmental monitoring data.

## Permissions and ethics
- Land access permissions secured prior to field work; voucher specimens verified by bryologists.

## References
- Loader et al. (1997) on cellulose extraction techniques.
- Stitt et al. (1989) on metabolite analyses in plant leaves.
- West et al. (2006) on water extraction times for isotope analysis.