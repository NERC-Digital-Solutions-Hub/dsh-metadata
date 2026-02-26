# GMEP_TOPSOIL_MESOFAUNA_2013_14.csv

## Overview
- Describes the Glastir Monitoring and Evaluation Programme (GMEP) soil mesofauna monitoring method used in Wales.
- Aims to monitor soil quality and ecosystem responses to Glastir interventions, as well as baseline status and trends related to drivers of change (land use, climate, pollution).
- Data are intended for integration into a central CEH (Centre for Ecology & Hydrology) database and for informing national reporting on Glastir outcomes.

## Data Scope and Purpose
- Collects multi-metric ecosystem data at multiple scales in a single snap-shot visit, within a rolling 4-year survey cycle.
- Two main components:
  - Wider Wales Component: baseline estimation and national trends.
  - Targeted Component: focus on Glastir priority areas.
- Uses a common spatial unit of 1 km2 to enable integration with other surveys and future analyses.
- Data support assessment of soil fauna communities (mesofauna and mites/collembolans) and related soil health indicators.

## Survey Design and Sampling Framework
- 4-year rolling survey cycle (2013–2016 initial cycle; soil mesofauna collected in years 1–2: 2013 and 2014 only).
- Sampling frame: 300 x 1 km squares across Wales.
  - Half are Wider Wales squares (randomly sampled within strata defined by the GB Land Classification).
  - Half are targeted at Glastir priority areas.
- Exclusions: random squares with >75% urban land or >90% sea are excluded.
- Spatial distribution: mapped at 10 km for confidentiality.
- Within each 1 km square:
  - Five pre-determined, randomly dispersed soil sample locations.
  - Soil cores collected using white plastic core (F-core), 8 cm long, co-located with vegetation surveys.
  - Cores posted promptly to CEH Lancaster labs for faunal extraction.

## Data Collection and Processing
- Data capture on field recording sheets; regular transfer to Excel spreadsheets.
- Sample preparation and dry extraction:
  - Use Tullgren funnels (6+ units) with 40 W bulbs to drive fauna from soil into 70% ethanol preservative, typically over 5 days.
  - Pre-extraction checks include equipment status and ensuring ethanol-filled collection bottles.
- Invertebrate Identification Protocol:
  - Separation of mesofauna from soil debris; identification to broad groups (e.g., Acari: Oribatida, Mesostigmata; Collembola: Poduromorpha, Entomobryomorpha, Symphypleona/Neelipleona; Enchytraeids; Other mites; total counts).
  - Specimens placed in labeled glass blocks/vials; tallied against SQXN (sample identifiers) in a recording notebook.
  - Re-extraction and re-counting steps to ensure completeness.
  - Quality control: 1 in 20 samples double-checked by another staff member to compare identifications and counts; data later entered into Excel.
- Data integration:
  - Data from Excel templates fed to CEH Bangor for database integration.
  - Data file example: GMEP_TOPSOIL_MESOFAUNA_2013_14.csv, with explicit column definitions and calculated totals (see data file reference below).

## Data Outputs and Metadata
- Primary data file: GMEP_TOPSOIL_MESOFAUNA_2013_14.csv.
- Columns capture counts for major groups and totals:
  - MITE_ORIB_BOX, MITE_ORIB_OTHER, MITE_MESO, MITE_OTHER (mite-related groups).
  - COL_POD, COL_ENTO, COL_SYMP (Collembola groups: Poduromorpha, Entomobryomorpha, Symphypleona/Neelipleona).
  - OTHERS (other invertebrates), TOTAL_MITES, TOTAL_COLL, TOTAL_MESO, TOTAL_INVERT (overall totals).
- Additional site metadata included:
  - YEAR, SQ_ID (1 km square identifier), PLOT_TYPE, PLOTNUM (plot number within square).
  - Easting/Northing (10 km resolution coordinates), LC (ITE Land Classification).
  - CORE_TAKEN status (Yes/Not received).
- Data definitions include explicit calculations:
  - TOTAL_MITES = sum of MITE_ORIB_BOX and MITE_ORIB_OTHER.
  - TOTAL_COLL = sum of COL_POD, COL_ENTO, COL_SYMP.
  - TOTAL_MESO = sum of mite and collembola counts.
  - TOTAL_INVERT = TOTAL_MITES + TOTAL_COLL.
- Related references and reading material provided to support methodology and taxonomy.

## Training, Health & Safety, and Quality Assurance
- Training:
  - Staff receive at least one week of hands-on training in identifying broad groups, using voucher specimens, and processing mock samples.
- Health & Safety:
  - Risk assessments for sample handling and Ethanol use (ethanol as a health hazard; minimize exposure).
- Quality Assurance:
  - Compliance with the DEFRA Joint Code of Practice for Research (JCoPR).
  - Independent verification: 1 in 20 samples checked by a second staff member; cross-identification conducted to ensure comparability.
  - QA process repeated in a staggered manner as identifications proceed.
  - Data entry into Excel completed when convenient after field/lab processing.

## Roles, Tasks, and Responsibilities
- Appendix 1 lists roles across the GMEP team:
  - Key individuals for soil mesofauna topics, data management, sample management, field coordination, and project management.
  - Field survey teams comprise a large roster of named staff across Wales.
- Roles include field team managers, data managers, sample sorting and tracking, field coordination, and project leadership.

## Data Governance Implications for Data Stewards
- Data standards and interoperability:
  - Uses a standardized 1 km grid and common sampling units to enable integration with other surveys (e.g., Countryside Survey methodologies).
  - Data are prepared in structured templates (SQXN, plot descriptors, LC, depth, etc.) for consistent ingestion into CEH Bangor’s database.
- Metadata and provenance:
  - Documents year of survey (2013–2014 for mesofauna portion), sample locations, land classification, and easting/northing coordinates.
  - Clear lineage from field collection to lab extraction, data capturing, and database integration.
- Data availability and confidentiality:
  - Spatial confidentiality is maintained by presenting distribution maps at a 10 km scale in published materials.
- Update cycle and maintenance:
  - Part of a rolling 4-year survey design; future cycles feed into national reporting and trend analyses.
  - Data likely updated via successive annual/biannual reports and the CEH Bangor database.
- Potential challenges and considerations:
  - Complex multi-component design (Wider Wales vs. Targeted) requiring careful data tagging to maintain consistency over time.
  - Managing large, heterogeneous datasets across multiple sites, years, and taxonomic groups; ensuring QA across field and lab steps.

## References and Documentation
- Supporting literature and formal reports cited for methodology, land classification, and soil biodiversity surveys.
- Includes guidance documents (e.g., JCoPR) and related technical references to support taxonomy and data handling practices.