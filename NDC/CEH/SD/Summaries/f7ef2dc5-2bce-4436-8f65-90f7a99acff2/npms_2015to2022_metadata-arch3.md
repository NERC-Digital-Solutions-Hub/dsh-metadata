# Introduction

- The National Plant Monitoring Scheme (NPMS) is a habitat-based plant monitoring scheme designed by BSBI, UK CEH, Plantlife and JNCC.
- Purpose: collect data to provide an annual indication of changes in plant abundance and diversity.
- Scope: supports volunteer plant recorders to monitor plants and habitat attributes in small plots selected via a structured UK-wide methodology (including Isle of Man and Channel Islands).
- Objectives:
  - Detect change in the quality of priority habitats.
  - Understand why change is occurring (pressures and drivers).
  - Contribute data for the UK Biodiversity Indicator 'C7 Plants of the wider countryside' by measuring changes in plant communities across important habitats.
- Data are updated annually and stored in the NPMS database at UKCEH Wallingford; accompanying field guidance and resources are provided to surveyors.

## NPMS Data Holdings

- The dataset snapshot provided here reflects the NPMS data for 2015–2022 and includes multiple interlinked files.
- Key data management and access principles:
  - Metadata and data quality considerations are addressed through an evidence quality assurance (EQA) framework.
  - Data and resources are publicly referenced; data governance and sharing are emphasized, with transparency about methods and limitations.

## File Descriptions and Contents

- locations_2015to2022.csv
  - location_id: unique location identifier
  - location_type: type of survey plot (e.g., square or linear)
  - Links to sampling events in sampleInfoWithLatLong_2015to2022.csv
- sampleInfoWithLatLong_2015to2022.csv
  - id: sample identifier
  - survey_id: NPMS survey code (e.g., 87 = Wildflower, 154 = Inventory, 155 = Indicator)
  - date_start: sample date
  - location_id: link to locations_2015to2022.csv
  - entered_sref and entered_sref_system: spatial reference details
  - created_on and created_by_id: data entry metadata
  - LATITUDE and LONGITUDE: coordinates
  - monad and monadCRS: 1 km square context and CRS (OSGB, OSIE, UTM)
  - country: territory context
- sampleAttributes_2015to2022.csv
  - sample_attribute_id: attribute value identifier
  - sample_id: links to sampleInfoWithLatLong_2015to2022.id
  - caption: describes the attribute category (e.g., NPMS Habitat)
  - text_value: attribute value
- occurrences_2015to2022.csv
  - id: occurrence identifier
  - sample_id: links to sampleInfoWithLatLong_2015to2022.id
  - taxonversionkey and preferred_taxon: taxon identity
  - domin: Domin cover-abundance score
  - record_status: verification status (e.g., C, V, R)
  - sensitivity_precision: indicates if records are spatially blurred
- npmsHabitatLookup.csv
  - NPMS_broad_habitat and NPMS_fine_scale_habitat: habitat classifications
- dominScores.csv
  - domin: original Domin score
  - dominIndex: harmonised Domin category
  - midPoint: interpreted cover mid-points used in NPMS
- Example workflow: demonstrates joining sampleInfoWithLatLong_2015to2022.csv with sampleAttributes_2015to2022.csv to extract habitat information via a join on sample_id

## Evidence Quality Assurance (EQA) and Governance

- EQA framework supported by key publications and internal reports:
  - Pescott et al. 2019; Pescott et al. 2015; Pescott et al. 2016 (design, implementation, and modeling of NPMS and related citizen-science monitoring)
  - Additional articles and internal reports documenting NPMS development, data use, and methodological considerations
  - NPMS-related technical and evaluation reports (e.g., JNCC Technical Review No. 622; internal Defra-related reports)
- Q&A on quality assurance and governance:
  - Q1: NPMS methods and publications underwent partnership peer review; design decisions were informed by statistical and botanical expertise; field testing, surveys, and participant questionnaires informed improvements.
  - Q2: Oversight by a project Steering Group; external peer review when risk warranted (e.g., survey design).
  - Q3: Outputs are checked by scientists to ensure claims are supported by evidence; ongoing external engagement and critique are expected.
  - Q4: Bias avoidance through robust statistical design enabling uncertainty estimation via models.
  - Q5: Document tracking and version control via a Data Management Plan; archival of report versions; off-site backups; adherence to PRINCE2 project management standards.

## Data Publication, Uncertainty, and Communication

- Outputs include newsletters and reports; results are publishable for independent review.
- Uncertainty and limitations are addressed in the outputs; claims are supported by evidence, and ongoing expert engagement provides critical feedback.
- Transparent communication of assumptions, limitations, and methodological uncertainties is integral to reporting.

## Data Access, Sharing, and Governance Practices

- Data from NPMS are publicly available for scrutiny and use by researchers and policy makers.
- Data input and verification processes emphasize structured data entry, a species dictionary, date controls, map-based locations, and controlled habitat terms.
- Verification workflows involve iRecord and expert review for higher-level taxonomic records.
- Data analysis is performed by experienced ecologists using R; results and interpretations are disseminated by a multidisciplinary project team.

## Implications for Monitoring Framework Authors

- NPMS demonstrates a comprehensive approach to designing and running a volunteer-based monitoring framework with:
  - Clear objectives aligned to policy-relevant indicators
  - Structured data architecture with linked, well-documented files
  - Rigorous EQA practices, peer review, and governance
  - Transparent data sharing while managing data quality and provenance
  - Explicit handling of uncertainty, biases, and communication of results
  - Documentation and version control to support reproducibility and auditability

## References and Further Information

- Key sources and documents:
  - Pescott et al. (2019, 2015, 2016) on NPMS design, implementation, and analysis
  - Walker et al. (2015) on plant monitoring developments
  - Pescott et al. (2019) on Bayesian occupancy/abundance indicators for NPMS
  - Various NPMS internal and external reports and guidance
  - NPMS official resources: NPMS website and related conservation and research content