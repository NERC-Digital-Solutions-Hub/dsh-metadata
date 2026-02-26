# The National Plant Monitoring Scheme (NPMS)

- Purpose and scope
  - A habitat-based plant monitoring scheme designed by BSBI, UK CEH, Plantlife and JNCC.
  - Aims to collect data to indicate annual changes in plant abundance and diversity.
  - Supports volunteer plant recorders to monitor plants and habitat attributes in fixed plots across the UK, Isle of Man, and Channel Islands.
  - Contributes to the UK Biodiversity Indicator C7 (plants of the wider countryside) and supports understanding of pressures and drivers of change.

- Data assets highlighted
  - Habitat Samples dataset (based on NPMS data update 2015–2022) created to train and validate Earth Observation–based data products.
  - Pre-joined NPMS samples with recorded surveyor habitat; adds NPMS habitat classification and change information for each plot/location.

- NPMS Habitat Samples dataset: file details
  - npmsHabitatSamples_2015to2022.csv (4287 KB) contains samples of plant communities at fixed plots over time.
  - Key fields include:
    - sample_id: unique NPMS fixed plot sample
    - survey_id: NPMS survey code (e.g., 87 = Wildflower, 154 = Inventory, 155 = Indicator)
    - entered_sref / entered_sref_system: spatial reference used
    - monad / monadCRS: 1 km square context and coordinate system
    - LATITUDE / LONGITUDE: sample location
    - country, surveyorHabitat, NPMS_hab_type, NPMS_broad_habitat: habitat classifications and scales
    - multipleHabs: whether broad habitat reported changed between samples
  - Purpose: support training/validation of Earth Observation data products; documents include habitat classification and potential changes at plots.

- Evidence Quality Assurance (EQA) framework
  - Based on published guidance and internal project documentation; encourages users to consult NPMS papers and reports.
  - Core components addressed by EQA:
    - Design and sampling: stratification and survey design developed with statisticians and botanists; plots selected via regular grids to ensure landscape randomness.
    - Habitat definitions and target species: habitat definitions peer-reviewed; plant indicators selected to be unbiased and practical for volunteers.
    - Field recording and participation: volunteer-based field recording with variable expertise; three contribution levels; comprehensive guidance and training.
    - Data input, verification, and quality control: online data capture with a species dictionary, date calendars, map-based locations, controlled habitat terms; geographic range checks; verification via the iRecord system for expert review where needed.
    - Data publishing and access: data will be publicly available for independent review.
    - Analysis and reporting: results analyzed by experienced quantitative ecologists; dissemination through NPMS newsletters and peer-reviewed publications.

- Q&A highlights (how NPMS manages quality and risk)
  - Q1: Peer review and involvement
    - Design developed via expert workshop; habitat definitions peer-reviewed; target species method reviewed by project team; field recording guided by training; data input/verification standardized; analysis by experienced ecologists; dissemination through newsletters and journals.
  - Q2: Level of external review based on risk
    - Steering Group oversight; external peer review invoked when necessary, e.g., for survey-design issues.
  - Q3: Communicating uncertainty and limitations
    - Outputs undergo reviewer checks to ensure claims align with evidence; openness to critique from the wider monitoring science community.
  - Q4: Avoiding biases
    - Robust statistical design allows uncertainty to be estimated through models.
  - Q5: Documentation and version control
    - Design work and outputs are versioned and archived; off-site backups; Data Management Plan; adherence to PRINCE2 project management standards.

- Data handling and stakeholder engagement
  - Data capture includes structured, validated entries, with support for volunteer participation and scalable quality checks.
  - Results intended for broad audiences, including researchers, policy-makers, volunteers, and the general public.
  - Ongoing governance through project management and steering oversight, with emphasis on transparency and continuous improvement.