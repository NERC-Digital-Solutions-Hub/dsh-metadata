# Supporting Document for 'A systematic review of common measurement methods of global soil protease activity between 1970-2020' dataset

## Overview
- Provides the supporting metadata and structure for the dataset accompanying a systematic review of soil protease activity measurement methods (1970–2020).
- Highlights the importance of robust, comparable protease assays for understanding soil nitrogen cycling.
- Describes how studies were identified, selected, and how data were extracted and organized for meta-analysis.

## Methodology of the systematic review
- Timeframe and objective: Systematic review conducted in March 2020 to collect studies measuring soil protease activity.
- Data sources: Web of Science (primary) and ScienceDirect (full-text screening for substrates).
- Search strategy: Complex search strings focusing on soil, protease/peptidase activity, and relevant substrates and assay terms; Table S1 and Table S2 document the search term strategy and substrates.
- Study inclusion: Predetermined criteria (Table S3); 680 studies met inclusion criteria and were eligible for data extraction.
- Data extraction and export: Mean soil protease activity data exported using predetermined criteria (Table S4). PRISMA diagram (Fig. S1) documents the study selection process.

## Dataset structure and contents
- Files: Two raw data files are provided to reflect differences in measurement modality.
  - Fluorimetric_methods.csv
  - Colorimetric_methods.csv
- Layout: Both files share the same structure but are split by measurement method (fluorimetric vs colorimetric).
- Data nature: Raw data extracted directly from the included studies.
- Documentation: Table S6 describes all variables present in the dataset and their units; cells marked as 'not stated' indicate missing information from the study.

## Metadata and variables
- Dataset layout and variables (as described in Table S6):
  - Identification
    - ID: Individual assay identifier
    - author: Surnames of all authors
    - date: Year of publication
    - title: Title of the journal article
    - DOI: DOI of the article
  - Study context and location
    - soil_type: FAO (1990) soil classification (or World Reference Base)
    - location: Location where soil was collected
    - altitude: Elevation of soil site (m.a.s.l)
    - MAT: Mean annual temperature (°C)
    - MAP: Mean annual precipitation (mm)
    - soil_depth: Depth of soil sampling (cm)
  - Soil properties
    - ph_mean: Average soil pH
    - ph_sd: SD of soil pH
    - ph_reps: Replicates for pH
    - soc_mean: Average soil organic carbon content
    - soc_unit: Unit for soil organic carbon
    - soc_sd: SD of SOC
    - soc_reps: Replicates for SOC
    - clay_mean: Average clay content (% w/w)
    - clay_sd: SD of clay content
    - clay_reps: Replicates for clay content
  - Protease assay data
    - protease_mean: Average protease activity
    - protease_unit: Unit of protease activity
    - protease_sd: SD of protease activity
    - protease_reps: Replicates for protease activity
    - method_cited: Source method/type of protease assay used
    - description: Description of the method protocol
    - substrate: Substrate used to measure protease activity
    - substrate_conc: Substrate concentration (mM)
    - assay_buffer: Buffer used in the assay
    - assay_buffer_conc: Buffer concentration (M)
    - assay_ph: pH at which the assay was performed
    - assay_time: Incubation time (hours)
    - assay_temp: Incubation temperature (°C)
    - termination: Method to terminate the assay (if applicable)
    - wavelength: Wavelengths used for fluorimetric/absorbance measurements (excitation/emission for fluorimetry; in nm)
- Substrates and modalities
  - Common substrates identified include 7-Amino-4-Methylcoumarin (AMC), N-benzoyl L-arginine amide, casein, gelatin, p-nitroaniline, haemoglobin, benzyloxycarbonyl phenylalanyl leucine, azocoll/azocasein.
  - Both fluorimetric and colorimetric measurement approaches are captured with their respective parameters.
- Data completeness
  - Some fields may be marked as not stated, reflecting reporting gaps across primary studies.

## Data governance and sharing considerations for Data Stewards
- Standards and interoperability
  - Dataset emphasizes standardized recording of study metadata (location, climate, soil properties) and assay conditions to enable cross-study comparisons.
  - Clear separation of measurement modalities (fluorimetric vs colorimetric) supports reproducibility and method-specific analyses.
- Provenance and traceability
  - Dataset explicitly links each record to its source publication (author, date, title, DOI) and documents the method cited.
  - Tables S1–S4 provide transparency on search strategy, substrate choices, inclusion criteria, and data export rules.
- Metadata completeness and quality
  - Variables include explicit units and descriptive fields; however, some values are incomplete or not stated in primary sources, flagged accordingly.
  - Raw data extraction preserves original measurements, enabling reprocessing or reanalysis with updated criteria.
- Documentation and reuse
  - Supplementary tables (S1–S4, S6) provide comprehensive documentation to support data reuse, meta-analyses, and methodological comparisons.
  - References to foundational soil classifications (FAO 1990 World Reference Base) support consistent soil categorization.
- Governance implications for data stewardship
  - Maintain versioning of the dataset, noting the March 2020 processing date and any subsequent updates.
  - Provide clear licensing and access terms to enable reuse while preserving provenance.
  - Consider gap-filling or imputation strategies for 'not stated' fields only in alignment with transparent reporting.

## Access, provenance, and related resources
- Data origin: Supplementary material accompanying the systematic review; includes PRISMA diagram (Fig. S1) and Tables S1–S4.
- Reference framework: Cited materials include Booker Tropical Soil Manual and FAO World Reference Base for Soil Resources (Table C.4 Annex C, pp. 238–239).
- Dataset purpose and usage
  - Designed to support meta-analyses and cross-study comparisons of global soil protease activity measurement methods.
  - Enables evaluation of methodological variance and potential biases across studies and substrates.

## Endnotes
- The document documents a comprehensive workflow from literature search to raw data extraction and dataset compilation, with emphasis on transparent methodological reporting to facilitate data governance, discovery, and reuse by the scientific community.