# Supporting Document for 'A systematic review of common measurement methods of global soil protease activity between 1970-2020' dataset

## Overview
- Documents the dataset supporting a systematic review of global soil protease activity measurement methods (1970–2020).
- Emphasizes the importance of proteases in soil N cycling and the need to evaluate and standardize measurement methods.
- Describes how studies were identified, selected, and how data were extracted and organized for meta-analysis.

## Data collection and study selection
- Primary search in Web of Science; supplementary full-text search in ScienceDirect targeting common assay substrates.
- Search strategy included terms related to soil protease activity and specific substrates.
- Screening applied predetermined criteria; 680 studies met inclusion (PRISMA diagram in Fig. S1).
- Data exported using predefined criteria (Table S4).

## Dataset structure and contents
- Two raw-data files: Fluorimetric_methods.csv and Colorimetric_methods.csv.
- Both files share the same layout but are split by assay type (fluorimetric vs colorimetric).
- Data are extracted directly from individual studies (raw data); missing values indicated as "not stated".
- Table S6 provides a description of all variables and their units.

## Key variables and metadata
- Identification and bibliographic details:
  - ID, author, date, title, DOI.
- Study and site context:
  - soil_type (FAO 1990; also mapped to World Reference Base), location, altitude, MAT (mean annual temperature), MAP (mean annual precipitation).
  - soil_depth, ph_mean, ph_sd, ph_reps.
  - soc_mean, soc_sd, soc_unit, soc_reps.
  - clay_mean, clay_sd, clay_reps.
- Protease measurement data:
  - protease_mean, protease_sd, protease_reps, protease_unit.
  - substrate, substrate_conc.
  - assay_buffer, assay_buffer_conc, assay_ph, assay_time, assay_temp.
  - termination (method to stop assay, if applicable).
  - wavelength details (for fluorimetric methods, both excitation and emission wavelengths; reported in nm).
- Method and protocol details:
  - method_cited (source of the protease activity method).
  - description (brief description of the protocol as written in the article).

## Dataset semantics and notes
- Layout designed to accommodate two measurement modalities (fluorimetric vs colorimetric); facilitates cross-method comparisons.
- All fields align with the variables described in Table S6; some cells may be unreported (empty) or marked as not stated.
- Data support meta-analysis and harmonization efforts by providing structured method-specific protease activity data across diverse soils.

## Quality considerations and limitations
- Data are heterogeneous due to varied protocols, substrates, and reporting standards across studies.
- Standardization relies on documented units and descriptors; missing metadata can affect comparability.
- The absence of universal standard protocols necessitates careful interpretation when aggregating across methods.

## Usage and access
- Dataset comprises two CSV files (fluorimetric and colorimetric) for subsequent analyses or reproducibility.
- Supplementary materials (Tables S1–S4 and S6; Fig. S1) provide detailed search strategies, selection criteria, and variable definitions.
- References include foundational soil classification resources (FAO World Reference Base) and classic soil manuals.