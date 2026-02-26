# National Plant Monitoring Scheme survey data (2015-2023)

## Overview
- Plot-level plant occurrence data for 2015–2023 covering the UK, Channel Islands, and Isle of Man.
- Observations include plant occurrences and habitat characteristics at metre scale, with Domin frequency-abundance cover data.
- Includes plot type, habitat, sampling date, and precise spatial location.
- Enables reconstruction of the sampling history (including gaps) for any NPMS plot within 2015–2023.

## Data collection and structure
- Data collected directly by volunteers into a custom Indicia database (PostgreSQL/PostGIS) via the NPMS website or app.
- Indicia data extracted from the master database using SQL queries.
- NPMS aims to provide an annual indication of changes in plant abundance and diversity; supports volunteer recorders to monitor plants and habitat attributes.

## Files provided (and their purposes)
- locations_2015to2023.csv: unique location_id, location_type (plot type), samplecount (number of samples per location).
- sampleInfoWithLatLong_2015to2023.csv: sample identifiers, survey_id (type: Wildflower, Inventory, Indicator), date_start, location_id, coordinates and spatial reference, created_on/by, latitude/longitude, monad (1 km square) and monadCRS, country.
- sampleAttributes_2015to2023.csv: sample_attribute_id, sample_id, caption, text_value (attributes such as habitat).
- occurrences_2015to2023.csv: id, sample_id, taxonversionkey, preferred_taxon, domin (Domin score), record_status (verification), sensitivity_precision (records potentially blurred).
- npmsHabitatLookup.csv: mapping between NPMS broad and fine habitats.
- dominScores.csv: harmonised Domin category mapping and mid-point interpretations.
- Notes: sample habitat can be accessed by joining sampleInfoWithLatLong_2015to2023.csv with sampleAttributes_2015to2023.csv where caption = 'NPMS Habitat'; example SQL/R snippet provided in the document.

## Accessing and working with the data
- Example provided: join sampleInfoWithLatLong_2015to2023.csv with sampleAttributes_2015to2023.csv to extract NPMS Habitat information (via R or SQL).

## Evidence Quality Assurance (EQA) and governance
- EQA is supported by numerous publications and project reports; users are advised to consult the listed sources.
- QA elements and processes:
  - Sample stratification and survey design developed with statistical and botanical experts; random, landscape-aware plot grids and linear plot lines.
  - Habitat definitions peer-reviewed; target species lists developed with an objective approach and project team review.
  - Field recording involves volunteers with multiple expertise levels; training and guidance provided; formal QA of field recording not currently in place but planned.
  - Data input/verification through online capture with a species dictionary, standardized date entries, map-based locations, controlled terms, and automated geographic checks; iRecord verification by botanical experts for certain records.
  - Data publishing: data will be publicly available for independent review.
  - Analysis conducted by experienced quantitative ecologists using R; results disseminated via NPMS newsletters and peer-reviewed journals.
- Governance and review:
  - Project overseen by a Steering Group; external peer review undertaken when warranted by risk level.
  - Outputs include uncertainty and limitations clearly checked by scientists prior to publication.
  - Robusta design to minimize bias through statistical methods.
  - Documentation and version control: design work documented, versions archived, off-site backups; Data Management Plan aligned with PRINCE2 standards.

## Key questions addressed (QA and process insights)
- Q1: Evidence of partnership peer review and involvement in methods (sample design, habitat definitions, target species selection; field recording and data verification processes; openness of data publishing; roles of experts and project team).
- Q2: Appropriateness of review level relative to risk (Steering Group oversight; external peer review as needed; expert workshops for survey design).
- Q3: Transparency of uncertainty and limitations (scientist-reviewed outputs; open to critique from monitoring scientists; plans for clear communication in reports and newsletters).
- Q4: Bias mitigation (robust statistical design enabling uncertainty estimation through models).
- Q5: Documentation and version control (designs reported and archived; off-site backups; Data Management Plan in place; PRINCE2-compliant project management).

## Relevance for monitoring framework authors
- Demonstrates a comprehensive, volunteer-driven monitoring framework with clearly defined data structures, QA mechanisms, governance, and public data sharing.
- Highlights integration of metadata, standardized vocabularies, and data harmonisation (Domin scores) to enable cross-study comparability.
- Provides a practical example of addressing common data access and quality challenges through structured processes, peer review, and transparent documentation.