# Introduction The National Plant Monitoring Scheme (NPMS) is a habitat-based plant monitoring scheme designed by BSBI, UKCEH, Plantlife and JNCC.

## Purpose and Objectives
- NPMS collects annual data to indicate changes in plant abundance and diversity; supports volunteer recorders to monitor plants and habitat attributes.
- Objectives:
  - Detect change in the quality of priority habitats.
  - Understand drivers and pressures behind change.
  - Contribute data to the UK Biodiversity Indicator 'C7 Plants of the wider countryside' by measuring changes in plant communities across important habitats.
- The document provides an annual snapshot of the NPMS database held at UKCEH Wallingford and outlines the files and the evidence quality assurance (EQA) process.

## Data Holdings and File Descriptions
- locations_2015to2021.csv: unique location_id and location_type describing plot type (square or linear).
- sampleInfoWithLatLong_2015to2021.csv: sampling event details per location_id, including survey_id, date_start, coordinates (entered_sref and system), creation timestamps and creator, plus latitude/longitude, monad and CRS, country.
- sampleAttributes_2015to2021.csv: additional sample data linked by sample_id; includes attribute category and value (text_value).
- occurrences_2015to2021.csv: species occurrences with unique id, sample_id linkage, taxon information (taxonversionkey, preferred_taxon), Domin cover value, verification status, and sensitivity flag.
- npmsHabitatLookup.csv: mapping between NPMS broad habitats and fine-scale habitats.
- dominScores.csv: harmonised Domin score mappings (dominIndex and midPoints for cover-abundance categories).
- File sizes are provided for context and to indicate data scale.

## Data Linkages and Access
- location_id links locations_2015to2021.csv to sampleInfoWithLatLong_2015to2021.csv for repeated sampling events.
- sample_id in sampleAttributes_2015to2021.csv links to id in sampleInfoWithLatLong_2015to2021.csv, enabling habitat attribute retrieval.
- sample_id in occurrences_2015to2021.csv links to the corresponding sample in sampleInfoWithLatLong_2015to2021.csv.
- Guidance example provided for accessing habitat information via R or SQL (join sampleInfoWithLatLong and sampleAttributes where caption is NPMS Habitat).

## Evidence Quality Assurance (EQA) Framework
- EQA publications underpin the methods and data handling; users are advised to consult these sources alongside NPMS guidance.
  - Key journal articles on design, methodology, and interpretation of NPMS and related plant-monitoring approaches.
  - Additional reports and CEH/BSBI/Plantlife contributions outlining development, Bayesian occupancy/abundance indicators, and cross-scheme considerations.
- QA questions addressed in NPMS context (Q1–Q5) outline governance, review, uncertainty communication, bias mitigation, and document/version control.

### Q1. How have partnership methods/publications been peer reviewed?
- NPMS design elements (sample stratification, survey design, habitat definitions, indicator species selection, field recording, data input/verification, data publishing, analysis, reporting) were developed with expert input and peer review processes; results are published and subject to ongoing critique from the monitoring community.

### Q2. How is the appropriate level of review/QA determined?
- The project is overseen by a Steering Group; external peer review is employed when risk warrants it (e.g., survey design workshops with experts).

### Q3. How are uncertainty, quality, assumptions, and limitations communicated?
- Outputs are checked by scientists to ensure claims are evidence-based; ongoing scrutiny from CEH’s monitoring science community expected; uncertainty is accounted for in modeling and interpretation.

### Q4. How are biases avoided in statistics and outputs?
- Robust statistical design enables uncertainty to be estimated through models; design choices are driven by expert input to minimize bias.

### Q5. Is document tracking and version control in place?
- Design outputs are versioned and archived; backups are maintained off-site; project follows a Data Management Plan and PRINCE2 project-management standards.

## Governance, Access, and Publication
- Data from NPMS are intended to be publicly available to allow independent review and reuse.
- The NPMS project emphasizes transparent data management, versioning, and availability to researchers, volunteers, policymakers, and the public.
- Analytical work is conducted by experienced quantitative ecologists using established tools (e.g., R); reporting is handled by a multidisciplinary team with botany, statistics, and communication expertise.