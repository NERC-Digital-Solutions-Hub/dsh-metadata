# National Plant Monitoring Scheme survey data (2015-2023)

- This resource provides plot-level plant occurrence data for 2015–2023 across the UK, Channel Islands, and Isle of Man, with metre-scale observations and Domin frequency-abundance cover data, plus plot type, habitat, sampling date, and precise location. It enables reconstruction of sampling history for NPMS plots, including gaps.

- Data are volunteered by participants and stored in a custom Indicia/PostgreSQL/PostGIS database. The NPMS data shown here were extracted directly from the master NPMS database via SQL queries.

- NPMS objectives (context for analysts):
  - Detect changes in quality of priority habitats.
  - Understand drivers and pressures behind changes.
  - Contribute to the UK Biodiversity Indicator for plants in the wider countryside by tracking plant communities across habitats.

- The dataset represents a current snapshot (2015–2023) of the NPMS database held at UKCEH Wallingford and is designed for public access and independent review.

- Key components and files (described briefly):
  - locations_2015to2023.csv: Unique location_id, location_type (plot type), and samplecount (number of samples per location).
  - sampleInfoWithLatLong_2015to2023.csv: Sample-level metadata including id, survey_id (e.g., Wildflower, Inventory, Indicator), date_start, location_id, spatial reference (entered_sref and entered_sref_system), created_on, created_by_id, LATITUDE, LONGITUDE, monad, monadCRS, and country.
  - sampleAttributes_2015to2023.csv: Additional sample attributes linked to samples via sample_id, with caption and text_value (e.g., habitat information).
  - occurrences_2015to2023.csv: Species-level observations linked to samples via sample_id, including taxon names (taxonversionkey, preferred_taxon), domin (Domin score), record_status (verification), and sensitivity_precision (blur/redaction if applicable).
  - npmsHabitatLookup.csv: Mapping between NPMS broad and fine-scale habitat categories.
  - dominScores.csv: Harmonised Domin scoring framework (domin, dominIndex, midPoint) to standardise cover-abundance interpretation across survey types.
- Example workflow highlight: To access habitat information for each sample, you can join sampleInfoWithLatLong_2015to2023.csv with sampleAttributes_2015to2023.csv on sample_id where caption is "NPMS Habitat" (illustrated with sample R or SQL code in the documentation).

- Data details and formats:
  - location_id links to sampleInfoWithLatLong_2015to2023.csv for repeated sampling events at a location.
  - sample_id in sampleAttributes_2015to2023.csv links to the id field in sampleInfoWithLatLong_2015to2023.csv.
  - survey_id codes: 87 = Wildflower survey; 154 = Inventory survey; 155 = Indicator survey.
  - entered_sref systems include OSGB (British National Grid), OSIE (Irish National Grid), and 4326 (WGS84).
  - monad and monadCRS describe 1 km squares and their coordinate references.
  - sensitivity_precision in occurrences indicates privacy protections (e.g., records blurred to 10 km when flagged as sensitive).

- Data quality assurance and governance (EQA):
  - NPMS design and implementation have been peer-reviewed and documented, with ongoing external review by a project Steering Group.
  - Data input is structured via online capture with a species dictionary, date calendars, map-based locations, and controlled terms; automated geographic range checks and iRecord verification by botanical experts support data validity.
  - Public data publishing supports independent review; results are checked by science staff to ensure claims are evidence-based.
  - Documentation and versions are tracked under a Data Management Plan following PRINCE2 standards, with off-site backups.

- Analytical and reporting context:
  - Prior work includes developing Bayesian occupancy/abundance indicators for NPMS and a formal technical review; analyses are conducted with R scripts by experienced quantitative ecologists.
  - Outputs include newsletters, reports, and peer-reviewed publications, aimed at researchers, volunteers, policy-makers, and the general public.

- How this data supports analysts:
  - Enables detection of habitat quality changes and attribution to drivers.
  - Supports occupancy and abundance modeling across habitats and time.
  - Provides a structured, standards-based, and QA-documented dataset with transparent provenance and uncertainty handling.
  - Facilitates reproducible analyses by offering explicit data relations (locations, samples, attributes, and occurrences) and harmonised categorisations (domin scores and habitat lookups).

- Key references and resources:
  - Foundational NPMS design and evaluation papers (2015–2019) and reviews.
  - Technical reports and project documentation detailing design choices, QA processes, and data use considerations.
  - Public NPMS resources and survey guidance documents.

- Important considerations for users:
  - Some occurrence records may be blurred for sensitive locations; spatial precision is adjusted accordingly.
  - The dataset emphasizes a robust sampling design and explicit uncertainty handling to support reliable inferences across time and space.
  - Users are encouraged to consult NPMS guidance and QA publications in tandem with the data for proper interpretation and methodological alignment.