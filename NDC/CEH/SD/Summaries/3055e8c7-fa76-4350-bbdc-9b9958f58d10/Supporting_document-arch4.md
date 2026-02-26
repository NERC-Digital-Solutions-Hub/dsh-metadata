# Supporting Document for 'A systematic review of common measurement methods of global soil protease activity between 1970-2020' dataset

## Purpose and context
- Proteases are key to soil nitrogen cycling, converting protein to peptides and amino acids; protease activity is a potential bottleneck in N cycling.
- There is a need for robust, comparable methods and standardized protocols to understand global patterns of soil protease activity.
- The document documents a systematic review and the resulting dataset to assess variance in soil protease activity measurements and the methods used.

## Data and methods overview
- Systematic review conducted in March 2020 to identify studies measuring soil protease activity.
- Primary database: Web of Science; search strategy includes broad terms for soil protease activity.
- Secondary search: ScienceDirect for common assay substrates (e.g., 7-Amino-4-Methylcoumarin, N-benzoyl L-arginine amide, casein, gelatin, p-nitroaniline, azocoll/azocasein, etc.).
- Study selection based on predefined criteria (Table S3); 680 studies met criteria for inclusion.
- Data extracted according to predefined criteria (Table S4); results summarized and organized.

## Dataset structure and layout
- Two dataset files:
  - Fluorimetric_methods.csv
  - Colorimetric_methods.csv
- Both files share the same layout and contain raw data extracted directly from the studies.
- Table S6 describes each variable and its units; missing values are denoted as 'not stated'.

## Key data elements and schema (variables)
- Identification and publication data:
  - ID, author, date, title, DOI
- Study context and location:
  - soil_type (FAO 1990 or World Reference Base), location, altitude
  - MAT (mean annual temperature), MAP (mean annual precipitation)
  - soil_depth
- Soil properties:
  - ph_mean, ph_sd, ph_reps
  - soc_mean, soc_sd, soc_reps (soil organic carbon)
  - clay_mean, clay_sd, clay_reps
- Protease assay details:
  - protease_mean, protease_sd, protease_reps
  - protease_unit
  - method_cited (source of method)
  - description (method protocol as stated)
  - substrate (substrate used)
  - substrate_conc
  - assay_buffer, assay_buffer_conc
  - assay_ph, assay_time, assay_temp
  - termination
  - wavelength (fluorimetric: excitation/emission; colorimetric: nm)
- Data collection and reporting specifics:
  - groundwater-like or other contextual notes as applicable
  - notes on whether data are raw measurements or summarized metrics

## Data quality, standards, and provenance
- Data are “raw data” extracted from individual studies, enabling re-analysis and meta-analysis.
- Standardized variable descriptions and units (Table S6) to enable cross-study comparisons.
- Some fields may be missing or labeled as 'not stated', reflecting variability in primary reporting.
- Soil type and environmental metadata use recognized standards (FAO/World Reference Base), aiding interoperability.

## Use cases and implications for data governance
- Enables meta-analyses of soil protease activity across decades (1970–2020) and across substrates and assay types.
- Supports evaluation of methodological variance and potential biases due to assay choice (colorimetric vs. fluorimetric) and substrate selection.
- Highlights the need for consistent documentation of methods, units, and environmental context to improve data discoverability and reuse.
- Can inform data strategy around standardization of measurement methods and metadata for soil protease studies.

## Accessibility, constraints, and references
- References Annex C and standard soil science manuals (Booker Tropical Soil Manual; FAO World Reference Base) for context and methodology.
- Acknowledges broader data-access challenges that can impede data reuse, such as paywalls and variable data reporting quality in primary studies.

## Endnotes and supplementary materials
- Figures and tables referenced (Figure S1 PRISMA diagram; Tables S1–S4; Table S6) provide detailed search strategies, inclusion criteria, and dataset variable definitions.
- Dataset supports transparent, reproducible synthesis of global soil protease activity measurements and their methodologies.