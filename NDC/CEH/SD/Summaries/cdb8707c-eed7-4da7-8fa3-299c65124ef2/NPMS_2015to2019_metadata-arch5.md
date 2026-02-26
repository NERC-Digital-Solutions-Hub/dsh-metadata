# Introduction

- The National Plant Monitoring Scheme (NPMS) is a habitat-based plant monitoring initiative designed by BSBI, CEH, Plantlife and JNCC to provide annual indications of changes in plant abundance and diversity.
- It supports volunteer plant recorders to monitor plants and habitat attributes using small plots selected by a structured methodology across the UK, Isle of Man and Channel Islands.
- Objectives:
  - Detect change in the quality of priority habitats.
  - Understand drivers and pressures behind changes.
  - Contribute data for the UK Biodiversity Indicator “C7 Plants of the wider countryside” by measuring changes in plant communities across key habitats.
- The documentation describes the current NPMS dataset held at CEH Wallingford and the evidence quality assurance (EQA) process behind NPMS.

## Data holdings and file contents

- locations_2015to2019.csv: Unique location_id, location_type (plot type: square or linear) describing survey plot related to habitat type; links to sampling events via location_id.
- sampleInfoWithLatLong_2015to2019.csv: Information about individual samples at a location; includes id, survey_id (type of NPMS survey), date_start, location_id, spatial reference (entered_sref and entered_sref_system), created_on, created_by_id, lat/long coordinates, monad and monadCRS, country.
- sampleAttributes_2015to2019.csv: Additional volunteer-collected data about samples; links to samples via sample_id; includes attribute category (caption) and text_value.
- occurrences_2015to2019.csv: Records of species occurrences observed during sampling; includes id, sample_id, taxonversionkey, preferred_taxon, domin (Domin score), record_status (verification), sensitivity_precision (for blurred records).
- npmsHabitatLookup.csv: Mapping between NPMS broad habitats and fine-scale habitats.
- dominScores.csv: Mapping between Domin values and a harmonised Domin category with mid-point values for cover-abundance interpretation.

## How the data are structured and linked

- Key links:
  - location_id in locations_2015to2019.csv connects to sampleInfoWithLatLong_2015to2019.csv to attach sampling events to locations.
  - sample_id (id in sampleInfoWithLatLong_2015to2019.csv) links to sampleAttributes_2015to2019.csv to attach additional attributes (e.g., habitat) to samples.
  - occurrences_2015to2019.csv links to samples via sample_id to associate species observations with specific samples.
- Data fields include spatial references, coordinate reference systems (OSGB, OSIE, 4326), and monad-based locality coding, enabling geographic analyses.
- The dataset supports a practical example of combining habitat information by joining sampleInfoWithLatLong_2015to2019 with sampleAttributes_2015to2019 where caption equals "NPMS Habitat".

## Evidence Quality Assurance (EQA) and data quality

- EQA framework supported by publications and guidance on the NPMS, including:
  - Design and evaluation of NPMS as a volunteer-based plant monitoring scheme.
  - Methods for interval-censored plant cover data and ecological monitoring with citizen science.
- Data management and QA practices include:
  - Online data capture with structured spatial database, a species dictionary, date standardization, map-based locations, and controlled habitat terms.
  - Automated verification checks (e.g., geographic range checks) and a verification pathway via iRecord for expert review (affiliated BSBI botanists).
  - Public data publishing to enable independent review of results.
  - Analysis by experienced quantitative ecologists using R.
  - Reporting through a project team with botany, statistics, and communications expertise; results disseminated via NPMS newsletters and peer-reviewed publications.
- QA governance and risk management:
  - NPMS is overseen by a project Steering Group; external peer review has been conducted where necessary.
  - Uncertainty and limitations are communicated in outputs; robust statistical design supports bias reduction and uncertainty estimation.
  - Design, outputs, and versioning are tracked; documents and report versions are archived and backed up off-site according to a CEH Data Management Plan following PRINCE2 standards.

## Data access, sharing, and stewardship

- Data from NPMS are intended to be publicly available to enable independent review and broader use.
- The scheme employs multiple data standards and controlled vocabularies to facilitate interoperability across systems and users.
- Field data collection emphasizes training and guidance for volunteers; data input supports data quality through structured entry and verification processes.
- Acknowledgement of potential limitations includes that formal quality assessment of field recording has not historically been part of NPMS but is under consideration for the future.

## Practical example: accessing habitat information

- To retrieve habitat information for samples:
  - Load sampleInfoWithLatLong_2015to2019.csv.
  - Load sampleAttributes_2015to2019.csv.
  - Filter sampleAttributes to those with caption equal to "NPMS Habitat".
  - Merge (left join) samples with their habitat attributes on sample id (sampleInfo id and sampleAttributes.sample_id) to obtain habitat data for each sample.

## Additional resources and references

- NPMS survey guidance and related resources are available on the NPMS website, with updates at:
  - https://www.npms.org.uk/content/survey-guidance
  - https://www.npms.org.uk/content/resources
- Supporting publications and reports cover design, analysis methods, and QA approaches used by NPMS, including:
  - Pescott et al. on design, launch, and assessment of the NPMS
  - Methods comparisons for interval-censored plant cover data
  - Reports and technical reviews detailing NPMS design, data use, and QA considerations