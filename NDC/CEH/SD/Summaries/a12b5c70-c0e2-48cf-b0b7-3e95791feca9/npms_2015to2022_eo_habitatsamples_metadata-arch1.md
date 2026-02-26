# Habitat samples dataset

- Overview: The National Plant Monitoring Scheme (NPMS) is a UK-led, habitat-based plant monitoring program designed to track annual changes in plant abundance and diversity. It supports volunteer recorders across the UK, Isle of Man, and Channel Islands, with the aim to detect habitat change, understand drivers, and contribute to a national biodiversity indicator (C7 Plants of the wider countryside). The 2015–2022 NPMS data update is pre-joined with surveyor habitat information to support Earth Observation-based data product development.

- Dataset purpose and scope:
  - Based on NPMS data update 2015–2022; pre-joined with surveyor habitat and enriched with habitat classification and per-plot change information.
  - Aims to support training and validation of EO-derived products and to document evidence quality assurance (EQA) for NPMS.

- File description:
  - npmsHabitatSamples_2015to2022.csv (size ~4.3 MB)
  - Contains information about plant-community samples collected at fixed plot locations over time. Key fields include sample identifiers, survey identifiers, spatial references, timestamps, recorder identifiers, location coordinates, habitat classifications, and change indicators.

- Key data fields (sample contents):
  - sample_id: unique identifier for an NPMS fixed plot sample
  - survey_id: NPMS survey code (e.g., 87 = Wildflower survey; 154 = Inventory; 155 = Indicator)
  - entered_sref / entered_sref_system: spatial reference entered by the surveyor and the CRS used (e.g., OSGB, OSIE, 4326)
  - created_on / created_by_id: record creation timestamp and submitting user
  - LATITUDE / LONGITUDE: geographic coordinates of the sample
  - monad / monadCRS: 1 km grid square and its coordinate system (OSGB, OSIE, UTM30)
  - country: Britain, Channel Islands, or Northern Ireland
  - surveyorHabitat: habitat reported by the surveyor (fine or broad scale NPMS habitat)
  - NPMS_hab_type: fine- or broad-scale habitat designation
  - NPMS_broad_habitat: corresponding broad habitat
  - multipleHabs: indicator whether broad habitat changed between samples for a fixed plot
  - Other metadata: habitat classification details, change indicators, and related notes

- Application and purpose:
  - Designed to support training and validation of Earth Observation-based data products.
  - Enables analysis of habitat change over time at plot locations.
  - Data are intended to be publicly available for independent review and reuse.

- Evidence Quality Assurance (EQA) and references:
  - EQA framework supported by multiple publications and guidance, including:
    - Design, launch, and assessment of NPMS (PLOS ONE, 2019)
    - Monitoring schemes for plants in Britain and Ireland (Biol. J. Linnean Soc., 2015)
    - Models for interval-censored plant cover data (PeerJ Preprints, 2016)
  - Additional articles and reports on NPMS design, implementation, and methodological developments.
  - Documentation recommends consulting these sources alongside NPMS guidance on the website.

- QA processes and governance:
  - Project overseen by a Steering Group; external peer review used where risk is higher (e.g., survey design).
  - Uncertainty and limitations addressed through robust statistical design; outputs checked by scientists before dissemination.
  - Data management plan adheres to PRINCE2 standards; design work tracked, with version-controlled documents and off-site backups.
  - Data publication policy ensures results are publicly accessible for independent review; analyses conducted by experienced quantitative ecologists using R.

- Outputs, communication, and limitations:
  - Results communicated via NPMS newsletters and peer-reviewed publications; interpretations reviewed by botanical and statistical experts.
  - Limitations and uncertainties explicitly considered in outputs; caveats accompany results.
  - Potential data issues to note:
    - Surveyor-reported habitats may be at fine or broad scale; misclassification or changes may reflect data entry or plotting relocations.
    - “multipleHabs” flag indicates reported changes that may not reflect true habitat change due to data issues.
    - Recording and data entry processes include potential errors, though automated checks and a species dictionary mitigate many risks.

- How to access and use:
  - The NPMS and accompanying resources provide survey guidance, habitat classifications, indicator species lists, and ID guides.
  - Data are intended to be discoverable and usable, with metadata and documentation to support reproducibility and transparent interpretation.

- Relevance for data-driven analysis:
  - Provides a structured, longitudinal, plot-level habitat dataset with standardized metadata and quality assurance context.
  - Facilitates correlation analyses between habitat change signals and environmental drivers, as well as validation of remote sensing/EO-derived habitat products.
  - Clear documentation of design choices, review processes, and data handling enhances trust and reproducibility for analysts.