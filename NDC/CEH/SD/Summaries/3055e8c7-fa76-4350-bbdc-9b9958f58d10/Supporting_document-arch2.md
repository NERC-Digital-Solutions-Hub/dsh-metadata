# A systematic review of common measurement methods of global soil protease activity between 1970-2020

## Overview
- Purpose: evaluate variance in soil protease activity measurements and identify common laboratory methods; emphasize the role of proteases in the soil nitrogen cycle and the need for robust, comparable measurement protocols.
- Scope: global, spanning studies from 1970–2020; systematic review of methods and their outputs.
- Output focus: meta-analysis-ready data and understanding of methodological differences that affect cross-study comparisons.
- Key finding highlighted by the dataset: standardised protocols are lacking, complicating comparisons across studies.

## Methodology
- Systematic search conducted in March 2020.
- Primary database: Web of Science; search terms targeting soil protease activity and related concepts.
- ScienceDirect used to locate full texts for common assay substrates (e.g., AMC, BAA, casein, gelatin, p-nitroaniline, haemoglobin, benzyloxycarbonyl amino acids, azocoll/azocasein).
- Supplementary materials (Tables S1–S6) detail search strategies, substrates, selection criteria, and data export rules.
- Studies included: 680 meeting predetermined inclusion criteria (PRISMA diagram in Fig. S1).

## Dataset structure
- Two raw data files: Fluorimetric_methods.csv and Colorimetric_methods.csv.
- Structure is the same across files; data are raw, extracted directly from studies.
- Cells marked “not stated” indicate missing information.
- Table S6 describes variables and their units.

## Variables and data layout (Table S6)
- Core identifiers: ID (assay ID), author (list of authors), date (year), title, DOI.
- Soil context: soil_type (FAO 1990 classification), location, altitude.
- Climate context: MAT (mean annual temperature), MAP (mean annual precipitation).
- Soil properties: soil_depth, ph_mean, ph_sd, ph_reps, soc_mean (soil organic carbon), soc_unit, soc_sd, soc_reps, clay_mean, clay_sd, clay_reps.
- Protease data: protease_mean, protease_unit, protease_sd, protease_reps.
- Method details: method_cited (source of protocol), description, substrate, substrate_conc, assay_buffer, assay_buffer_conc, assay_ph, assay_time, assay_temp, termination, wavelength (two values for fluorimetric methods: excitation and emission; otherwise nanometres).

## Dataset layout and data extraction
- Data exported using predefined criteria (Table S4) for meta-analysis compatibility.
- Selection criteria (Table S3): protease activity measured in soil; exclude studies with unresolved conditions; allow inclusion of studies examining effects of assay conditions (e.g., pH, temperature).

## Substrates and measurement approaches
- Common substrates captured in datasets:
  - Fluorimetric: 7-Amino-4-Methylcoumarin (AMC), BAA-protease, others.
  - Colorimetric: casein, gelatin, p-nitroanilide, haemoglobin, benzyloxycarbonyl amino acids, azocoll/azocasein.
- Measurement modalities: fluorimetric and colorimetric assays; substrate specifics and concentrations are recorded to enable method comparison.

## Geographic and soil context
- Soil classification aligned with FAO 1990 framework (and related references).
- Site-specific data include location, altitude, mean climate metrics (MAT, MAP), soil depth, pH, soil organic carbon, and clay content.

## Data use and monitoring relevance
- Purpose for analysts monitoring environmental health: provide a harmonised, transparent dataset to compare soil protease activity across studies and regions.
- Supports evaluation of environmental health and policy performance through standardized data capture and metadata.
- Highlights the need for standard protocols and accessible underlying data to improve long-term environmental monitoring and data interoperability.

## Limitations and considerations
- High heterogeneity in measurement methods across studies; standardisation remains a challenge.
- Some variables may be incomplete or not reported in primary studies, limiting full comparability.
- Dataset emphasizes raw data extraction, which requires careful handling for cross-study meta-analyses.

## References and supplementary materials
- Supplements include detailed search term strategies, study selection criteria, data export criteria, and the PRISMA diagram (Figure S1).
- referenced materials: Annex C and related soil manual references (e.g., Booker Tropical Soil Manual) for soil classification frameworks.