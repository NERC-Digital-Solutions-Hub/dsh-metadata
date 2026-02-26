# Supporting Document for 'A systematic review of common measurement methods of global soil protease activity between 1970-2020' dataset

- Purpose and significance
  - Proteases drive soil nitrogen cycling by converting protein to oligopeptides and amino acids; understanding global patterns requires robust, comparable measurement methods.
  - Systematic review undertaken to assess variance in soil protease activity measurements and the substrates/methods used, due to lack of standardised protocols.

- Methodology and scope
  - Study period: 1970–2020.
  - Primary search: Web of Science using targeted terms for soil protease activity; follow-up ScienceDirect search for common assay substrates.
  - Selection criteria (Table S3): soil protease activity measured in soil medium; inclusion of studies addressing assay conditions (e.g., pH, temperature); exclusion of studies with unobtainable data or lacking controls.
  - Study inclusion: 680 studies included for data export (PRISMA diagram Fig. S1).
  - Data extraction: mean soil protease activity values exported using predefined criteria (Table S4).

- Dataset structure and layout
  - Two raw data files: Fluorimetric_methods.csv and Colorimetric_methods.csv.
  - Same variable layout across both files; split by measurement type (fluorimetric vs. colorimetric).
  - Cells marked 'not stated' indicate missing information in the source study.

- What the dataset contains (variables and units)
  - Identification and publication details
    - ID, author, date, title, DOI
  - Study context and location
    - soil_type (FAO 1990 classification / World Reference Base equivalents)
    - location (as reported)
    - altitude (m above sea level)
    - MAT (mean annual temperature, °C)
    - MAP (mean annual precipitation, mm)
  - Sampling and soil properties
    - soil_depth (cm)
    - ph_mean, ph_sd, ph_reps (pH-related)
    - soc_mean, soc_sd, soc_reps (soil organic carbon)
    - clay_mean, clay_sd, clay_reps (clay content, % w/w)
  - Protease activity data
    - protease_mean, protease_sd, protease_reps
    - protease_unit
    - substrate (substrate used to measure activity)
    - substrate_conc (substrate concentration, mM)
    - assay_buffer, assay_buffer_conc
    - assay_ph (pH at which assay was performed)
    - assay_time (incubation time, h)
    - assay_temp (incubation temperature, °C)
    - termination (method to stop assay, if applicable)
    - wavelength (fluorometric/absorbance wavelengths; fluorimetric first value = excitation, second = emission; unit: nm)
  - Method-specific details
    - method_cited (citation of the study/method baseline)
    - description (description of the method protocol as written)
  - Data provenance and structure
    - Table S6 provides variable descriptions and units
    - Table S1–S4 and Figure S1 (PRISMA) document search strategy, inclusion criteria, and data export criteria

- Data quality, gaps, and challenges
  - Many fields marked as 'not stated' reflect missing detail in primary studies.
  - Heterogeneity across substrates, assay types (fluorimetric vs. colorimetric), buffer conditions, and reporting units complicates cross-study comparisons.
  Potential issues include inconsistent soil classifications, varying depths and climate contexts, and non-standardized protocols across decades.

- How the data can be used
  - Meta-analysis and cross-study comparisons of global soil protease activity, stratified by substrate type, assay method, and soil/climate variables.
  - Investigations into how assay conditions (pH, temperature, incubation time) influence measured activity.
  - Assessing relationships between soil properties (texture, organic carbon) and protease activity.
  - Informing methodological standardization efforts by identifying common substrates and protocol elements.

- Access and supplementary material
  - Supplementary materials include:
    - Table S1–S4: search strategies, selection criteria, and data export criteria
    - Figure S1: PRISMA diagram of the systematic review process
    - Table S6: description of dataset variables and units
  - References to foundational soil classification manuals (e.g., Booker Tropical Soil Manual; FAO World Reference Base) cited for soil_type mapping.

- Practical notes for analysts
  - Expect substantial variability due to non-standardized historical methodologies; careful harmonization and sensitivity analyses recommended.
  - When aggregating data, prioritize explicit substrate type and measurement method to minimize heterogeneity.
  - Use Table S6 as a guide to unit conversions and variable definitions during data cleaning and analysis.