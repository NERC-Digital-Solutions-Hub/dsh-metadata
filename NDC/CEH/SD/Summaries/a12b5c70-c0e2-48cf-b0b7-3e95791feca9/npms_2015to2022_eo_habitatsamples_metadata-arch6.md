# Introduction The National Plant Monitoring Scheme (NPMS) is a habitat-based plant monitoring scheme designed by BSBI, UK CEH, Plantlife and JNCC.

## Overview
- NPMS is a volunteer-based plant and habitat monitoring program across the UK, Isle of Man, and Channel Islands.
- Aims to detect changes in priority habitats, understand drivers of change, and contribute to the UK Biodiversity Indicator for plants in the wider countryside.
- The dataset described (Habitat samples) is intended to support training and validation of Earth Observation (EO)-based data products.

## Habitat samples dataset (npmsHabitatSamples_2015to2022.csv)
- Based on NPMS data update for 2015–2022; pre-joined samples with surveyor habitat and additional habitat classification information.
- Primary purpose: enable training/validation of EO-derived products; describe samples of plant communities over time at fixed plots.
- Key content and structure:
  - sample_id: unique NPMS fixed-plot sample identifier
  - survey_id: NPMS survey code (e.g., 87 = Wildflower, 154 = Inventory, 155 = Indicator)
  - entered_sref / entered_sref_system: spatial reference and its CRS (OSGB, Irish Grid, 4326)
  - created_on / created_by_id: data entry timestamps and submitter identifiers
  - LATITUDE / LONGITUDE: precise sample coordinates
  - monad / monadCRS: 1 km square (monad) and its CRS
  - country: Britain, Channel Islands, Northern Ireland
  - surveyorHabitat: habitat as reported by the surveyor (fine or broad scale)
  - NPMS_hab_type / NPMS_broad_habitat: fine vs broad habitat classifications
  - multipleHabs: flag if broad habitat changed across samples for a fixed plot
- Note: “changed” in multipleHabs may reflect data entry errors or plot relocation, not necessarily true habitat change.

## Evidence Quality Assurance (EQA) for NPMS
- EQA guidance and supporting publications are recommended for data users.
- Supporting materials include:
  - Journal articles on design, implementation, and modelling of NPMS and related ecological monitoring (e.g., PLoS ONE 2019; Biological Journal of the Linnean Society 2015; PeerJ Preprints 2016).
  - Reports on design, use of NPMS data for air pollution inferences, Bayesian indicators, and cross-scheme considerations.
- EQA-covered elements:
  - Sample design and survey methodology developed with statistical and botanical input; random plot selection via grid-based designs.
  - Habitat definitions created with habitat experts; species indicators chosen to be unbiased and fit for volunteer engagement.
  - Field recording accommodates varying botanical expertise; training provided; three contribution levels for participants.
  - Data input workflows use online capture with a species dictionary, date calendars, map-based locations, controlled terms, and geographic range checks.
  - Verification uses iRecord for expert review of exceptional records; data publication planned for public access.
  - Analysis conducted with R by experienced quantitative ecologists; results disseminated through NPMS newsletters and peer-reviewed publications.

## Governance, review, and uncertainty
- Q1: Methods and publications reviewed by a partnership Steering Group and external experts; design and survey methods tested via workshops, field trials, and questionnaires.
- Q2: Quality assurance levels determined by risk; external peer review used where necessary; survey design issues subjected to expert workshop.
- Q3: Outputs clearly communicate uncertainty and limitations; claims are checked against evidence by the review team.
- Q4: Bias avoidance via robust statistical design enabling uncertainty estimation through models.
- Q5: Document tracking and version control in line with a Data Management Plan; versions archived and backed up off-site following PRINCE2 standards.

## Usage notes and caveats
- The dataset is intended for training/validation of Earth Observation data products and for broader ecological analysis.
- Interpret habitat change flags with caution due to potential data entry errors or plot relocation.
- Outputs are designed for public data sharing and independent review, with transparency about methods and uncertainties.