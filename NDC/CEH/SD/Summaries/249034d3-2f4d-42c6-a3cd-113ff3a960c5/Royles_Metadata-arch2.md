# Physiology and stable isotope ecology of moss growth for modelling spatial and temporal climatic signals NERCDMP-555 - monthly field and dark adapted PAM fluorescence measurements

## Overview
- Field and laboratory study to model spatial and temporal climatic signals using moss physiology and stable isotope ecology.
- Conducted across multiple sites (Dersingham Bog, Brandon Country Park, Wicken Fen) from April 2017 to September 2018.
- Combines in situ chlorophyll fluorescence with water content, cellulose extraction, and water/isotope analyses to build climate-related proxies from mosses.

## Study sites and target organisms
- Sites include Dersingham Bog (bog/heathland), Brandon Country Park (heathland), and Wicken Fen (fen/shaded woodland).
- Target moss species representing diverse lifeforms and habitats; vouchers verified by bryologists.
- Species examples mentioned: Aulacomnium palustre, Dicranum scoparium, Sphagnum spp., Pleurozium schreberi, Polytrichum formosum, among others.

## Field sampling and measurements
- Monthly field sampling from April 2017 to September 2018.
- On each visit: collect three subsamples (≈2 x 2 x 2 cm) per target species.
- In-field chlorophyll fluorescence using Walz MINI-PAM II:
  - Measurements: F, Fm, PAR, ETR; three readings per sample.
  - Post-field dark adaptation (≥30 minutes) with three additional dark measurements (F', Fm').
  - Calculations: fluorescence yield (F/Fm and F'/Fm'), non-photochemical quenching, and ETR (0.84 x PAR x 0.5 x Φ).
- Leaf/tip-level focus for photosynthetic assessment.

## Laboratory analyses and data types
- Water content: determine field relative water content (RWC) by fresh/dry weight after drying at 70°C.
- Cellulose extraction: standard batch procedure (Loader et al. 1997) from dried moss material.
- Water extraction: cryogenic vacuum distillation for water isolated from fresh moss samples (West et al. 2006).
- Fresh water samples collected at each site; precipitation collected near the study area (Ely, UK).
- Additional enzymatic analysis: sucrose content via spectrophotometric methods (Stitt et al. 1989).

## Dataset structure and file metadata
- Dataset comprises 14 monthly CSV files (01_Jul_2017 to 14_Oct_2018).
- 18 columns per record, including:
  - Session, Date, Sample, Site, Species, Notes
  - Measurements: F, Fm, Dark_Y, Field_F, Field_Fm, Field_PAR, Field_Y, ETR, NP
  - Moss metrics: RWC, Cellulose (with reference for cellulose data)
  - Value and type (mean / SE)
- Data entries include sample collection numbers and site/species metadata; field and lab procedures linked to standard references.

## Data provenance and governance
- Voucher specimens identified and verified by experienced bryologists.
- Permissions obtained from landowners/managers prior to fieldwork.
- Data generated using established, quality-assured protocols and traceable references.

## Data processing and quality assurance
- Multiple measurements per sample with mean and standard error calculated.
- Standardized calculations for chlorophyll fluorescence metrics and photosynthetic parameters.
- Data structured to support monitoring outputs and cross-site comparisons.

## Reuse, sharing, and accessibility
- Data organized for storage in appropriate data portals and for downstream analysis.
- Methods and references provided to facilitate reproducibility and reuse in climate- and environment-focused monitoring contexts.

## Relevance to environmental monitoring and policy
- Demonstrates a rigorous, standardized approach to collecting, processing, and reporting environmental proxy data from mosses.
- Enables spatially explicit and temporally resolved assessment of environmental health signals and climate-related trends.
- Supports integration with other datasets to enhance the value of monitoring products and policy evaluations.

## Key challenges and opportunities for Analysts Monitoring the Environment
- Challenge: increasing the value of moss-derived datasets by integrating with broader environmental data to avoid single-use outputs.
- Opportunity: enabling broad access to underlying data and metadata to support transparency, reproducibility, and secondary analyses for environmental health monitoring.