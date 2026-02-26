# National Plant Monitoring Scheme

## Objective and scope
- Habitat-based plant monitoring scheme designed to provide annual indicators of changes in plant abundance and diversity.
- Aims to detect change in priority habitats, understand drivers/pressures, and contribute data for the UK Biodiversity Indicator C7 (plants of the wider countryside).
- Uses volunteer recorders to monitor plants and habitat attributes across the UK, Isle of Man, and Channel Islands.
- The dataset is updated annually and stored at UKCEH Wallingford.

## Data structure and files provided
- locations_2015to2021.csv
  - Unique location_id; location_type describing the survey plot (square or linear) and associated habitat type.
- sampleInfoWithLatLong_2015to2021.csv
  - Sample-level information: id, survey_id (NPMS survey type), date_start, location_id, entered_sref, entered_sref_system, created_on, created_by_id, LATITUDE, LONGITUDE, monad, monadCRS, country, etc.
- sampleAttributes_2015to2021.csv
  - Additional sample data linked by sample_id; includes caption and text_value describing the attribute (e.g., habitat) and its value.
- occurrences_2015to2021.csv
  - Species occurrences linked to samples; fields include id, sample_id, taxonversionkey, preferred_taxon, domin (Domin score), record_status, sensitivity_precision.
- npmsHabitatLookup.csv
  - Mapping between NPMS broad habitats and fine-scale habitats.
- dominScores.csv
  - Harmonised Domin score lookup: domin, dominIndex, midPoint (mid-points for cover scores across survey levels).

## Key data contents and relationships
- Location data links to sampling events via location_id.
- Samples (sampleInfoWithLatLong) link to occurrences (occurrences_2015to2021) via sample_id.
- Habitat and other attributes are accessible via sampleAttributes (e.g., NPMS Habitat) with sample_id as the key.
- Spatial references use various CRS (OSGB, OSIE, 4326) and monad-based geography for 1 km squares.

## Example: accessing habitat information
- Demonstrates combining sampleInfoWithLatLong with sampleAttributes to obtain habitat data for each sample.
- R example: merge samples with habitat attributes where caption == 'NPMS Habitat' and join on id vs. sample_id.
- Similar operations can be performed in SQL or other database frameworks.

## Evidence Quality Assurance (EQA) and governance
- EQA is supported by a body of publications and internal guidance to ensure data quality and transparency.
- Publications span journal articles, other published articles, and internal/external reports (listed in the document).
- EQA questions and responses outline the governance, review, and transparency processes (summarised below).

## EQA: how quality is ensured (Q1–Q5)
- Q1: Peer review of partnership methods and publications
  - Design and survey methods developed via a workshop with statistical and botanical experts; grid-based (square plots) and linear plots favored for landscape randomness.
  - Habitat definitions peer-reviewed; target species lists developed with project team input to balance objectivity, usefulness for volunteers, and avoiding bias.
  - Field recording uses volunteer participants; training and guidance provided; formal QA of field recording not currently part of NPMS but being considered.
- Q2: Appropriate level of review/QA based on risk
  - Project Steering Group oversees work; external peer review undertaken as needed, especially for high-risk outputs.
- Q3: Communicating uncertainty, quality, assumptions, limitations
  - Outputs are checked by scientists to ensure claims are supported by evidence; results subjected to constructive critique within CEH monitoring science community.
  - Data openness aimed through public data availability for independent review.
- Q4: Avoiding biases in statistical outputs
  - Robust statistical design enables uncertainty to be estimated via models applied to the data.
- Q5: Document tracking and version control
  - Design work reported; versions archived and backed up off-site per CEH Data Management Plan using PRINCE2 project management standards.

## Data usage, access, and publication
- Data from NPMS will be publicly available to allow independent review of results.
- Analysis is performed by experienced quantitative ecologists using R; results disseminated via NPMS newsletters and peer-reviewed journals.
- The NPMS dataset is stored as a current snapshot and is periodically updated; historical context and methods are documented in accompanying guidance and papers.

## Additional context and resources
- Survey guidance and related resources are available on the NPMS website, with links to updated guidance if the original URLs change.
- The dataset provides a practical example of combining field-recorded habitat data with species occurrences to study plant community change and drivers across multiple years and locations.